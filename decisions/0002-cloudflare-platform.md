# 0002 — Cloudflare platform

Status: draft.

The site runs on Cloudflare. One Worker renders pages and performs every action that changes something. D1 holds the records. A Durable Object holds each live room. R2 holds the editor asset library. A GitHub Action on the main branch runs the tests and deploys the Worker, the D1 migrations, and the Durable Object classes with Wrangler. Files in R2 are not part of that deploy. An editor uploads those directly.

This is the free tier of one vendor. The paid step that lifts the daily caps is Workers Paid, at $5 a month. Limits below are from Cloudflare’s docs dated 18–30 Oct 2026. On the free plan, a daily cap resets at 00:00 UTC, and further use of that kind fails until then.

## What each component holds

| Component | Holds |
| --- | --- |
| Worker | Language pages, sign-in, the session, permission checks, publishing, Discord role updates, and the Benben status message in a channel. Calculator math stays in the browser. |
| D1 | Accounts, site rank, drafts, published pieces, translations of existing interface strings, guilds, Premium, Early Supporter, and the asset catalog. The catalog is the name, kind, size, and storage key. The file itself is not a row. English interface strings ship inside the Worker. |
| Durable Object | One for Benben. A later community pet or community game can have its own. Guild chat and alliance chat each have their own. Open screens hear changes from the object. The object hibernates when nobody is connected. |
| R2 | Icons and images editors place in guides. A guide stores the catalog key, so one file used in many guides is stored once. Readers load the file from R2, not through the Worker. |

The asset library starts from about 1,500 icons, together 50 MB. Images may be a similar count and will take more space. Both fit the free R2 allowance unless an image averages several megabytes.

Waiting on D1, R2, or Discord does not spend CPU time. Rendering the page does. Cloudflare’s own note on the free plan is that a server render often takes 10–20 ms, and the free allowance is 10 ms. Pages stay thin so a request stays inside that allowance.

Benben’s hourly fade is applied when the pet is next read, from the time it was last saved. A scheduled job is not required for the numbers to be right.

## Pros

- One Action and one vendor deploy the app, the database, and the live rooms.
- Nothing pauses because a week was quiet.
- D1 can rewind 7 days on the free plan.
- R2 does not charge for downloads. The icon library and a similar number of guide images stay inside the free 10 GB.
- Benben is one live room. A later community pet or game, and each guild chat, can have its own without sharing that state.
- The paid step for the app, the database caps, and the live rooms is the same $5 Workers plan.

## Cons

- Sign-in, sessions, and linking Discord are application code.
- D1 has no row-level rules. The Worker is what rejects a publish, an officer-chat write, or a fourth Benben action.
- Each D1 database runs one query at a time. A full queue returns an overloaded error.
- The saved row and the live room are two stores. The Worker keeps them in agreement.
- A free request that renders too much page fails with a CPU limit error. Workers Paid is the fix.
- A single D1 database cannot grow past 10 GB, on the free plan or the paid plan.

## Workers

The app. Free plan, then Workers Paid.

| | Free | Paid |
| --- | --- | --- |
| Requests | 100,000 / day | No daily cap |
| CPU time | 10 ms per request | 5 min (default 30 seconds) |
| Memory | 128 MB per isolate | 128 MB per isolate |
| Subrequests per request | 50 | 10,000 |
| Cron triggers on the account | 5 | 250 |
| Worker bundle | 64 MiB | 64 MiB |
| Request body | 100 MB on a free zone | 100 MB on a free zone |

Past 100,000 requests in a UTC day, Cloudflare returns error 1027. The route for this site fails closed, so a signed-in action is not served as if the Worker were absent. Past 10 ms of CPU, the request fails with error 1102.

Calculator pages and other files shipped with the Worker count as static assets: 20,000 files per version on the free plan, 100,000 on the paid plan, 25 MiB each. The editor library does not use this quota. Those files live in R2.

## D1

Records only. One database is single-threaded. A query that takes about 1 ms allows on the order of 1,000 queries a second. A query that takes 100 ms allows about 10. A scan counts every row it looks at, not every row it returns.

| | Free | Paid |
| --- | --- | --- |
| Rows read | 5 million / day | 25 billion / month, then $0.001 / million |
| Rows written | 100,000 / day | 50 million / month, then $1 / million |
| Database size | 500 MB | 10 GB, and that cap cannot be raised |
| Account storage | 5 GB, 10 databases | 5 GB included, then $0.75 / GB-month |
| Queries in one request | 50 | 1,000 |
| Time Travel | 7 days | 30 days |
| One row | 2 MB | 2 MB |
| One statement | 100 KB, 100 parameters | Same |

When a daily read or write cap is hit, queries fail until 00:00 UTC. Writes include inserts, updates, and deletes. An index write counts as an extra written row.

Publishing and Benben care stay far under 100,000 writes a day. Many guilds saving a siege map or a chat as one row per action can reach it. Those writes should be batched.

## Durable Objects

Live rooms. Free plan objects use the SQLite backend. WebSocket hibernation is required: an open socket that cannot hibernate is billed for the whole time it stays connected, and on the free plan the duration cap is easy to spend that way.

| | Free | Paid |
| --- | --- | --- |
| Requests | 100,000 / day | 1 million / month, then $0.15 / million |
| Duration | 13,000 GB-s / day | 400,000 GB-s / month, then $12.50 / million GB-s |
| Rows read | 5 million / day | 25 billion / month, then $0.001 / million |
| Rows written | 100,000 / day | 50 million / month, then $1 / million |
| Stored data | 5 GB | 5 GB-month, then $0.20 / GB-month |
| Storage per object | 10 GB | 10 GB |

A request that opens a WebSocket counts as one request. Incoming WebSocket messages bill at 20 messages to one request. Outgoing messages are not billed. An idle object that is eligible to hibernate does not spend duration.

On the free plan, exceeding any one of these limits makes further operations of that kind fail until 00:00 UTC.

## R2

The asset library. Standard storage. Downloads are free. Infrequent Access is not used: it is outside the free tier and charges a retrieval fee.

| | Free | Past the free tier |
| --- | --- | --- |
| Storage | 10 GB-month | $0.015 / GB-month |
| Uploads and lists (Class A) | 1 million / month | $4.50 / million |
| Reads (Class B) | 10 million / month | $0.36 / million |
| Deletes | Free | Free |
| Downloads | Free | Free |

The icons at 50 MB are a small part of the 10 GB. About 1,500 images stay inside it until an image averages several megabytes. Ten image loads on a guide can happen about a million times a month before the free read allowance runs out.

A reader’s browser requests the file from R2. Those reads count as Class B operations and do not count as Worker requests. An editor upload goes through the Worker, which checks the site rank and then writes the object and the catalog row.

## See also

[Prepare](../features/content/prepare.md), [Publish](../features/content/publish.md), [Community pet](../features/benben/community-pet.md), [Benben on Discord](../features/benben/discord-channel-pet.md), [Member chat](../features/guilds/member-chat.md), [Sign in](../features/identity/sign-in.md).
