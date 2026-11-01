# Community site — product spec

This spec describes the community site to build from scratch for Pop Epoch players maintained by LoA Alexandria. It records what people already do on the `game-calculators` proof of concept, written as jobs and feature specs. It does not describe pages, routes, or a technical design yet, but should have it later.

`game-calculators` is evidence for these jobs. It is not the architecture to copy.

## How to read it

1. [Users](product/users.md) — who can act, and which attributes combine.
2. [Jobs](product/jobs.md) — what each person is trying to get done. Each job links to the feature specs that define when it is complete.
3. [Scope](product/scope.md) — which jobs belong in the product, a suggested build order, and decisions still open.
4. [Features](features/README.md) — one spec per feature, grouped by the job it belongs to. Shared rules are stated once there and linked from the others.
5. [Decisions](decisions/0001-stored-rank-is-master.md) — choices that more than one feature depends on.
6. [Glossary](product/glossary.md) — short definitions, each pointing at the spec that owns the term.

A feature's folder is its domain, not its phase. Build order stays in [scope](product/scope.md).

Later documents (software design, working rules for agents) are intentionally absent. They come after this product spec is agreed.

## Status

Draft.
