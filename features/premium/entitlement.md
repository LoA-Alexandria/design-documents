# Entitlement

Status: draft.

Premium is on or off, independent of site rank. It is a time-limited entitlement, or a lifetime grant, not a subscription that charges by itself. Active Premium unlocks tools marked Premium and allows the member to register one guild.

How a member gains or extends Premium is defined in [Claims](claims.md). The tool lock is defined in [Premium lock](../calculators/premium-lock.md). The one guild, and what happens when Premium lapses, are defined in [Registration](../guilds/registration.md).

When a member with linked Discord has active Premium, the site can give them the Premium role on the community Discord server, and remove it when Premium is no longer active. The check uses the member's entitlement and their linked Discord id. A site admin may run that sync for another member. The Premium role is not given for any other mark. The site is master, as recorded in [Stored site rank is master](../../decisions/0001-stored-rank-is-master.md). Staff-rank roles are defined in [Discord role sync](../identity/discord-role-sync.md).

## Done when

- An approved claim or a manual grant makes Premium tools available and allows one guild registration for as long as the entitlement is active.
- After Premium ends, Premium tools lock again and a member-registered guild freezes as described in [Registration](../guilds/registration.md).
- The Discord Premium role matches active Premium for a linked Discord account, and is not given for any other mark.
