# Site rank

Status: draft.

Staff do only what the stored rank allows. A site admin sets each member's site rank to Normal user, Editor, or site admin, and can see who holds which rank. The first site admin is recorded on the site.

Hiding a control is not permission. Every staff action is checked on the server against the stored rank.

The stored rank is master data, and the Discord role follows it. See [Stored site rank is master](../../decisions/0001-stored-rank-is-master.md) and [Discord role sync](discord-role-sync.md). The ranks themselves are defined in [users](../../product/users.md).

There is one Editor rank. Publishing is a separate permission on that rank, not another rank. A site admin always may publish and can grant or revoke the permission on an Editor. See [Publish](../content/publish.md) and [Users](../../product/users.md).

## Done when

- A site admin can change the stored rank, and the site then allows only what the new rank allows.
- A site admin can grant or revoke the publish permission on an Editor.
- A Normal user cannot prepare or publish.
