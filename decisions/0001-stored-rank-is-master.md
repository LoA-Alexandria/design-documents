# 0001 — Stored site rank is master

Status: decided.

On the proof of concept, mapped Discord roles are the source of Editor and site admin, and the highest mapped role wins. Here the stored site rank is master data. A site admin assigns it, and the Discord role follows.

A role someone adds or removes on Discord leaves the stored rank as it is. The same direction applies to Premium and to Early Supporter: the mark stored on the site is master, and the Discord role follows it.

See [Site rank](../features/identity/site-rank.md), [Discord role sync](../features/identity/discord-role-sync.md), [Entitlement](../features/premium/entitlement.md), and [Early Supporter](../features/premium/early-supporter.md).
