# Free tools

Status: draft.

A player uses a tool to answer a game question: a cost, a plan, a projection, or a simulation. Each tool states its assumptions, units, and the game data it is based on, including the date or version of that data. The calculation itself does not depend on being signed in.

A free tool works for an anonymous user. A tool that is not ready is visible as not ready, and only a site admin can open it. Free calculators ship in the first phase. See [scope](../../product/scope.md).

Simulations are the same job as calculators. They stay in phase 3, free or Premium according to each simulation. A simulation that is Premium uses the [Premium lock](premium-lock.md).

## Done when

- A free tool can be used with no session, and its result follows the documented rules at the boundaries that matter (zero, minimum, maximum, invalid input).
- Changing a formula or a game value updates the explanation the player sees in the same change.
- A tool that is not ready cannot be used by a Normal user, an Editor, or an anonymous user.
