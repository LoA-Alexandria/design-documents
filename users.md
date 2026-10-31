# Users

Two kinds of visitor exist: someone who is not signed in, and someone who is. A signed-in person always has exactly one site rank, and may also hold Premium and one or more guild posts. Those attributes combine. A site admin can be a Premium member and a guild officer at the same time. Premium does not replace the site rank, and a guild post does not replace either.

A member signs in with Discord or with a username and password. A password account can link Discord later. GitHub, Google, and other providers can be added later as further ways into the same account.

## Anonymous user

A person with no session.

They can read published news, guides, and event write-ups, choose a language, and use tools that are not limited to Premium. They cannot join a guild, chat, publish, pay, or open a Premium tool. When they hit one of those jobs, the site asks them to sign in with Discord or with a username and password.

## Authenticated user

A person with a session. Four attributes describe what they may do.

### Site rank

Exactly one of the following.

| Rank | Who they are |
| --- | --- |
| Normal user | A signed-in member with no staff duties. They use the site, join guilds, and chat. |
| Editor | A staff member who prepares news, guides, and event write-ups. Publishing to the public site is a separate permission, not a different rank. In the proof of concept this is split: a guide writer may only prepare, and a manager may also publish. This spec keeps one Editor rank and treats "may publish" as a permission on that rank. |
| Site admin | A staff member who can do everything an Editor can do, including publish, and who runs the site: assign site ranks, manage members, review Premium claims, grant or revoke Premium, and administer guilds. |

Site rank is master data stored for the member. A site admin assigns it. The first site admin is recorded on the site. A new sign-in with no stored rank becomes a Normal user. Site admin is above Editor, and Editor is above Normal user, in what the rank allows.

The Discord role follows the stored rank once Discord is linked. Setting Editor or site admin gives the member the matching role on the community Discord server. Setting Normal user removes those staff roles. A username-and-password account has its rank before Discord is linked, and receives the Discord role at that link. The same direction applies to Premium: the Discord Premium role follows the entitlement. A role someone adds or removes on Discord leaves the stored rank as it is.

Hiding a control is not permission. Every staff action is checked on the server against the stored rank.

### Premium

On or off, independent of site rank. Any Normal user, Editor, or Site admin may hold it.

Active Premium unlocks tools marked Premium, allows the member to register one guild, and is what the Discord Premium role follows. It is a time-limited entitlement (or a lifetime grant), not a subscription that charges by itself.

A guild registered by a member freezes when that member's Premium lapses. People can still read the guild. Writes stop, except that members can still leave and the registering member can still hand the guild on or take it down. A guild a site admin created, with no registering member, does not freeze. A site admin can still write in a frozen guild.

### Early Supporter

A separate mark from Premium and from site rank. A site admin awards it to a member who has active Premium. There are 20 places. Revoking an award does not free its place, so the cohort cannot grow past the first 20 assignments. The mark does not grant, extend, or replace Premium.

The member may opt in to showing a chosen name and the award date on a public list. Anyone can read that list. It shows only the people who opted in.

Once Discord is linked, the Early Supporter and Test Version Discord roles follow the mark. They stay if Premium later ends. They are removed if the award is revoked.

### Guild post

Separate from site rank and Premium. A person may have a different post in each guild, or none.

| Post | Who they are |
| --- | --- |
| Applicant | Has asked to join and is waiting for review. |
| Member | An accepted member. Can read the guild and use member chat. |
| Officer | A member who can review join requests, write guild news, run event plans, and use officer chat. |
| Master | The person responsible for the guild. Can do what an officer can do, edit guild settings, promote officers, and hand the master post to someone else. The master cannot leave their own guild; they hand it on or the listing is removed. |

A site admin can act in a guild the way its master can, including while the guild is frozen. That power comes from the site rank, not from a guild post.

## What each user can start

This is the map from person to job. The jobs themselves are in [jobs](jobs.md).

| Job | Anonymous | Normal | Editor | Site admin | Also requires |
| --- | --- | --- | --- | --- | --- |
| Read news, guides, and event write-ups | yes | yes | yes | yes | — |
| Choose a language | yes | yes | yes | yes | — |
| Use a free tool | yes | yes | yes | yes | — |
| Use a Premium tool | no | if Premium | if Premium | if Premium | Active Premium |
| Sign in | yes | — | — | — | Discord, or username and password |
| See Benben | yes | yes | yes | yes | — |
| Care for Benben | no | yes | yes | yes | Three actions per Benben per UTC day |
| Prepare content | no | no | yes | yes | — |
| Publish content | no | no | if granted | yes | Publish permission |
| Request to join a guild | no | yes | yes | yes | — |
| Review join requests, run plans, officer chat | no | if officer or master | if officer or master | yes | Guild post, or site admin |
| Member chat and alliance member chat | no | if member | if member | yes | Accepted membership |
| Register a guild | no | if Premium | if Premium | yes | Active Premium, except site admin |
| Pay for Premium and submit a claim | no | yes | yes | yes | — |
| Approve claims, grant Premium, award Early Supporter, assign site ranks | no | no | no | yes | Early Supporter also requires the member's active Premium |
| Opt in to the public Early Supporter list | no | if awarded | if awarded | if awarded | — |
