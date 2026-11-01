# Discord role sync

Status: draft.

Saving a member's site rank updates the matching Discord role when the member has Discord linked. Setting Editor or site admin gives the member the matching role on the community Discord server. Setting Normal user removes those staff roles. A username-and-password account keeps its rank before that link, and receives the Discord role when Discord is linked.

Adding or removing the role on Discord leaves the stored rank unchanged. The site is master. See [Stored site rank is master](../../decisions/0001-stored-rank-is-master.md).

The same direction applies to other marks. The Premium role is defined in [Entitlement](../premium/entitlement.md). The Early Supporter and Test Version roles are defined in [Early Supporter](../premium/early-supporter.md).

## Done when

- After the rank is saved, a member with linked Discord has the Discord role for that rank, and no longer has the Discord role for a rank they no longer hold.
- Adding or removing the role on Discord leaves the stored rank unchanged.
