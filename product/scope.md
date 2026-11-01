# Scope

Everything in [jobs](jobs.md) is part of the product. This file says what to build first, what the proof of concept does that this spec does not yet adopt, and which decisions are still open.

Phase 1 is decided. Later phases are still a proposal. Guild registration stays behind Premium, because a member-registered guild freezes when Premium lapses and a member may only register one guild.

## Build order

### 1. Read, sign in, publish, Benben, and free calculators

- Read news, guides, and event write-ups. Each of the five languages has its own URL. See [Published pieces](../features/reading/published-pieces.md) and [Language URLs](../features/reading/language-urls.md).
- Sign in with Discord or with a username and password. The stored site rank is kept; a first sign-in is a Normal user. A password account can link Discord. See [Sign in](../features/identity/sign-in.md).
- Free calculators, each with its documented rules and tests. See [Free tools](../features/calculators/free-tools.md).
- Editors prepare content. Editors with the publish permission, and site admins, publish it. See [Prepare](../features/content/prepare.md) and [Publish](../features/content/publish.md).
- Site admins assign site rank. The matching Discord role follows once Discord is linked. See [Site rank](../features/identity/site-rank.md) and [Discord role sync](../features/identity/discord-role-sync.md).
- Care for Benben: the shared community pet, and a separate pet for each Discord channel that opens one. See [Community pet](../features/benben/community-pet.md) and [Discord channel pet](../features/benben/discord-channel-pet.md).

This is the shell every later job assumes: a session, a rank, public content in a language URL, free calculators, and the communal pet.

### 2. Guild membership and chat

- Request to join, officer review, roster, member chat, and officer chat. See [Join and roster](../features/guilds/join-and-roster.md), [Member chat](../features/guilds/member-chat.md), and [Officer chat](../features/guilds/officer-chat.md).
- Permanent alliances and their two chats. See [Alliances](../features/guilds/alliances.md).
- Site admins create and edit guilds. See [Registration](../features/guilds/registration.md).

Guilds in this phase are admin-created. Members do not register guilds yet, and guilds do not freeze, because Premium does not exist yet. Event-alliance offers wait for event planning, because an offer carries the guild's chosen base.

### 3. Premium

- Pay, submit a claim, admin approval, manual grants, and history. See [Claims](../features/premium/claims.md).
- Premium tools lock and unlock with the entitlement. See [Premium lock](../features/calculators/premium-lock.md) and [Entitlement](../features/premium/entitlement.md).
- One guild registration per Premium member, transfer, removal, and freeze. See [Registration](../features/guilds/registration.md).
- Discord Premium role sync. See [Entitlement](../features/premium/entitlement.md).
- Premium calculators. The lock is real in this phase, so these tools ship with it.
- Early Supporter: a site admin awards one of 20 permanent places to a member with active Premium. The public list is opt-in. The Early Supporter and Test Version Discord roles follow the award. See [Early Supporter](../features/premium/early-supporter.md).

### 4. Guild event planning

- Turning events on and off, day scores, and end-invest pledges. See [Day scores](../features/events/day-scores.md).
- Siege boards. See [Siege board](../features/events/siege-board.md).
- Territory boards for Dawn of Rome and Crown of the Nile, including event alliances. See [Territory board](../features/events/territory-board.md) and [Alliances](../features/guilds/alliances.md).

This phase depends on guild posts and officer chat from phase 2. Event alliances depend on the base marker from the siege and territory boards.

## In the product, not sequenced above

Simulations are the same job as calculators. They stay in phase 3, free or Premium according to each simulation. Free calculators are already in phase 1. See [Free tools](../features/calculators/free-tools.md).

## Departures from the proof of concept

On the proof of concept, mapped Discord roles are the source of Editor and site admin, and the highest mapped role wins. Here the stored site rank is master data. A site admin assigns it, and the Discord role follows. Recorded in [Stored site rank is master](../decisions/0001-stored-rank-is-master.md).

## Present on the proof of concept, not yet adopted

These exist today. They are not jobs in this spec until the open questions below are closed.

- Sharing a published piece into Discord as a formatted post.
- Volunteer translation packs maintained outside the editor.

## Open decisions

1. **Publish permission.** This spec uses one Editor rank, plus a permission to publish. The proof of concept uses two ranks (guide writer and manager). Confirm the single rank. See [Publish](../features/content/publish.md).
2. **Discord share.** Keep posting a published piece into Discord, or treat that as part of the community Discord bot rather than the site. Benben's own Discord command is already in phase 1.
3. **Event categories.** Should events use the same categories as the game? See [Published pieces](../features/reading/published-pieces.md).
