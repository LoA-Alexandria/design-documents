# Registration

Status: draft.

A member with active Premium may register one guild. The request names the guild, the server, and who the master is: the member themselves, or someone else identified by Discord id or by an exact site name. An unknown or ambiguous name is refused, and the member can try again with a Discord id. While that guild is still pending or active, another month of Premium does not grant a second guild. Removing the guild frees the slot.

A site admin can also create a guild directly, and can edit and unstick a guild, including one that is frozen. An admin-created guild has no Premium owner and does not freeze.

When the registering member's Premium lapses, the guild freezes: reads stay available, ordinary writes stop, members can still leave, and the owner can still transfer or remove the listing. A site admin can still write in a frozen guild. Leaving is defined in [Join and roster](join-and-roster.md). What Premium is, and when it ends, is defined in [Entitlement](../premium/entitlement.md).

Release: site admins create and edit guilds in phase 2, while guilds are admin-created and do not freeze. Member registration, the one-guild limit, transfer, removal, and freeze arrive in phase 3 with Premium. See [scope](../../product/scope.md).

## Done when

- A Premium member cannot hold two guild registrations at once. Removing the guild frees the slot.
- An unknown or ambiguous master name is refused. A Discord id can name the master instead.
- A site admin can create, edit, and unstick a guild, including one that is frozen. An admin-created guild does not freeze.
- In a frozen guild, reads stay available. Ordinary writes fail for anyone who is not a site admin and not the owner acting on the listing itself. Members can still leave, and the owner can still transfer or remove the listing.
