# Community site — product spec

This spec describes the community site to build from scratch for Pop Epoch players maintained by LoA Alexandria. It records what people already do on the `game-calculators` proof of concept, written as jobs and feature specs. The platform is decided. Pages and routes are not.

`game-calculators` is evidence for these jobs. It is not the architecture to copy.

## How to read it

1. [Users](product/users.md) — who can act, and which attributes combine.
2. [Jobs](product/jobs.md) — what each person is trying to get done. Each job links to the feature specs that define when it is complete.
3. [Scope](product/scope.md) — which jobs belong in the product, a suggested build order, and decisions still open.

Below stuff is WIP. Take it with a grain of salt.

4. [Features](features/README.md) — one spec per feature, grouped by the job it belongs to. Shared rules are stated once there and linked from the others.
5. [Decisions](decisions/0002-cloudflare-platform.md) — choices that more than one feature depends on. The platform is [Cloudflare](decisions/0002-cloudflare-platform.md). Stored rank is [master data](decisions/0001-stored-rank-is-master.md).
6. [Glossary](product/glossary.md) — short definitions, each pointing at the spec that owns the term.

A feature's folder is its domain, not its phase. Build order stays in [scope](product/scope.md).

The platform is decided. Page structure and working rules for agents are not.

## Status

Draft.
