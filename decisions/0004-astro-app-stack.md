# 0004 — Astro app stack

Status: draft.

The community site is TypeScript on the Cloudflare platform in [Cloudflare platform](0002-cloudflare-platform.md). Astro renders the pages. Hono handles actions that change something. Calculator math stays in the browser as small client islands. This choice keeps free-plan Worker CPU low: rendering stays thin, and waits on D1, R2, or Discord do not spend that allowance.

`game-calculators` is Next.js and React. It is evidence for the jobs, not the stack to copy onto Workers. Next.js server render is too heavy for the free 10 ms CPU limit.

## What each part does

| Part | Holds |
| --- | --- |
| TypeScript | The language for the Worker, Durable Objects, migrations, and tests. |
| Astro | Language pages, published pieces, and the site shell. Prefer prerender when a page needs no session. SSR only what must change per request. |
| Hono | Sign-in, the session, permission checks, publishing, Discord role updates, Benben care actions, and other writes. Same Worker as Astro. |
| Client islands | Free and Premium calculators, and live UI that talks to a Durable Object. Prefer Preact, Solid, or plain TypeScript over a full React app shell. |
| D1, Durable Objects, R2 | Unchanged from [0002](0002-cloudflare-platform.md). |
| Wrangler and a GitHub Action | Tests, deploy of the Worker, D1 migrations, and Durable Object classes. |
| Vitest | Unit tests for calculator rules and permission checks. Broader browser tests can wait. |

Sessions are application cookies on the Worker. There is no separate Node server and no Supabase.

## Out of scope for this stack

- Next.js, Remix, or a heavy React SSR app on the Worker.
- A second backend outside Cloudflare.
- Piping R2 file downloads through the Worker.
- Long-lived WebSocket handling outside Durable Object hibernation.

## See also

[Cloudflare platform](0002-cloudflare-platform.md), [Scope](../product/scope.md), [Sign in](../features/identity/sign-in.md), [Publish](../features/content/publish.md), [Free tools](../features/calculators/free-tools.md), [Community pet](../features/benben/community-pet.md).
