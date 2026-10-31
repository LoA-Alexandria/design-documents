# Jobs

Each job is something a person is trying to finish. "Done when" is the product outcome, not a screen or a table. Actors are defined in [users](users.md). Release order is in [scope](scope.md).

## Read news, guides, and event write-ups

Anyone, including an anonymous user, can read what staff have published: news, guides, and event write-ups. News is listed newest first. Guides and event write-ups might be grouped and ordered by the category and \ or position chosen at publish time.

*OPEN QUESTION*: 
event categories - Main event (blue), Routine Event (orange), Ranking Challenge (Red). 

The reader picks one of five languages: English, German, French, Russian, or Spanish. Each language has its own URL, so a page can be shared and indexed in that language. With no language in the address, the browser's language preference decides, and the address becomes that language's URL. A missing translation shows the English source, so a gap is visible as English rather than a blank. Numbers and dates follow the chosen language.

Done when:

- An anonymous reader can open a published news item, guide, and event write-up without signing in.
- Each language has its own URL for the same page, and opening that URL shows that language.
- Changing language opens the same page at the other language's URL.
- An untranslated string shows its English source.
- Unpublished drafts are invisible to readers.

## Use calculators and simulations

A player uses a tool to answer a game question: a cost, a plan, a projection, or a simulation. Each tool states its assumptions, units, and the game data it is based on, including the date or version of that data. The calculation itself does not depend on being signed in.

Some tools are free. Some are limited to members with active Premium. A free tool works for an anonymous user. A Premium tool tells an anonymous user to sign in, and tells a signed-in member without Premium that the tool is part of Premium. A tool that is not ready is visible as not ready, and only a site admin can open it. Free calculators ship in the first phase. Premium calculators ship with Premium. See [scope](scope.md).

Done when:

- A free tool can be used with no session, and its result follows the documented rules at the boundaries that matter (zero, minimum, maximum, invalid input).
- A Premium tool stays locked until the signed-in member has active Premium.
- Changing a formula or a game value updates the explanation the player sees in the same change.
- A tool that is not ready cannot be used by a Normal user, an Editor, or an anonymous user.

## Sign in, and let site rank control editing

A player signs in with Discord, or with a username and password, and keeps the site rank stored for them. Someone signing in for the first time is a Normal user. They can sign out. Staff then do only what the stored rank allows. A site admin changes that rank on the site. After the change is saved, the member's Discord staff role matches it once Discord is linked.

A username is 3 to 24 letters, numbers, or underscores, and it stays the sign-in name. The member does not enter an email address. A password account can link Discord later. Linking adds Discord to that account. It does not merge two accounts that already exist. A public display name can be changed after Discord is linked.

GitHub, Google, and other providers can be added later. Each one is another way into the same account. Adding a provider does not create a new site rank or a second membership.

An Editor prepares news, guides, and event write-ups, including their translations. An Editor publishes only when they have the publish permission. A site admin always has that permission. Publishing makes the piece readable by everyone, including anonymous users. Publishing again with the same identity replaces the live piece. News needs no category. Guides and event write-ups need a category and a position in that category.

A site admin sets each member's site rank to Normal user, Editor, or site admin, and can see who holds which rank. Saving the rank updates the matching Discord role when the member has Discord linked. A username-and-password account keeps its rank before that link, and receives the Discord role when Discord is linked.

Done when:

- A successful sign-in, with Discord or with a username and password, produces a session and exactly one site rank: the rank already stored, or Normal user when none is stored.
- A site admin can change that stored rank, and the site then allows only what the new rank allows.
- After the rank is saved, a member with linked Discord has the Discord role for that rank, and no longer has the Discord role for a rank they no longer hold. Adding or removing the role on Discord leaves the stored rank unchanged.
- Linking Discord attaches it to the account that is already signed in, and leaves any other existing account as it is.
- An Editor without the publish permission can prepare a piece and cannot make it public.
- An Editor with the publish permission, or a site admin, can make a piece public, and anonymous readers then see it.
- A Normal user cannot prepare or publish.
- A refused or incomplete sign-in leaves the person anonymous and tells them what to do next, without showing raw error text from the provider.

## Care for Benben

Benben is a stone pyramid the community looks after together. Anyone can see how Benben is doing. A signed-in member can feed, polish, sunbathe, or let Benben rest. Each member has three of those actions per Benben per UTC day.

Each need fades every hour by 5 percent of its current value, and by at least 1 point, until it reaches zero. Every care action also moves one shared journey: seven landscapes, five milestones in each. Sunbathing fills a hidden shared goal; when the goal is reached, a phoenix visits for 24 hours.

A member's own daily games, souvenirs, and looks stay on that member's account. They do not change Benben's needs or the shared journey. An anonymous visitor can play on this browser only, and signing in keeps that personal progress on the account.

The community site has one shared Benben. A Discord channel has its own. A member opens that channel's Benben from Discord, and the channel keeps a single status message that updates when someone takes care of it. Care from Discord uses the same three daily actions and the same rules.

Done when:

- An anonymous visitor can see the community Benben and cannot spend a care action.
- A signed-in member can spend up to three care actions on one Benben per UTC day, and a fourth is refused.
- Needs fade on the hourly rule above, whether or not anyone is watching.
- Care advances the shared journey. Personal games, souvenirs, and looks do not.
- Reaching the sunbathing goal brings the phoenix for 24 hours, then it leaves.
- Each Discord channel that opens Benben has its own needs and journey, and one status message in that channel.

## Belong to a guild

A signed-in member can find guilds, ask to join one, and take part once accepted. Masters and officers decide who gets in. Members talk to each other. Officers talk separately. Guilds can ally, and allies get their own shared conversation.

### Join and roster

A signed-in member requests to join a guild and may add a note. Masters and officers accept or reject the request. Accepted members set the name they want on the roster. Officers are promoted by the master (or by a site admin). The master can edit the guild's name, server, description, and icon, and can hand the master post to someone else.

A member can leave. The master cannot leave; they hand the guild on, or the listing is removed. Leaving still works when the guild is frozen.

### Chat

Accepted guild members can read and write the guild's member chat. The master and officers can read and write a separate officer chat. Members who are not officers cannot read officer chat. An applicant cannot enter chat.

### Alliances

Two kinds of alliance exist.

- A permanent alliance has a member chat for accepted members of either guild, and an officer chat limited to officers of either guild.
- An event alliance is tied to one planned event. Its planning chat stays readable by both guilds, and only officers of either guild can write in it.

A guild can offer an event alliance only after it has marked its own base for that event. The invited guild sees the offer without having to open the event. Neither side can accept its own offer. Accepting turns that event on for the partnership.

### Registering a guild

A member with active Premium may register one guild. The request names the guild, the server, and who the master is: the member themselves, or someone else identified by Discord id or by an exact site name. An unknown or ambiguous name is refused, and the member can try again with a Discord id. While that guild is still pending or active, another month of Premium does not grant a second guild. Removing the guild frees the slot.

A site admin can also create a guild directly. An admin-created guild has no Premium owner and does not freeze.

When the registering member's Premium lapses, the guild freezes: reads stay available, ordinary writes stop, members can still leave, and the owner can still transfer or remove the listing.

Done when:

- A signed-in member can request to join, and a master or officer can accept or reject that request.
- Only accepted members can use member chat. Only the master and officers can use officer chat. The same boundary holds for alliance chats.
- A member can leave a frozen guild. Other writes in a frozen guild fail for anyone who is not a site admin and not the owner acting on the listing itself.
- A Premium member cannot hold two guild registrations at once.
- A site admin can create, edit, and unstick a guild, including one that is frozen.

## Plan guild events

Officers (and the master, and a site admin) run a guild's event plan. Members follow it. This job includes ordinary event planning and the siege and territory boards.

### Shared plan

Officers turn an event on and off. Turning an event off clears that event's plan — targets, scores, pledges, painted territory, and its alliance — after the officer confirms, so the next match starts empty.

For a scoreboard event, officers record day scores and members record what they will invest at the end. Members see the plan for the active event.

### Siege board

For an event that is fought over camps, the plan is a map. Officers mark the guild's base, put targets in an order, split Military Tokens (horns) across targets so the shares add to 100 percent, and say whether Draupnir Rings hit one camp or the whole field. Each member marks which targets they will attack. The map shows the order, the share, whether rings land there, and how many members attack it. The shares are visibly wrong when they do not add to 100 percent.

Members do not type an attack total. They only choose where their attacks go.

### Territory board

Dawn of Rome and Crown of the Nile share one territory plan, shown on one picture or its mirror. Officers paint which land and which places the guild, its allies, and its opponents hold. A place is painted as a whole. Prestige follows the painted land and places, at the rates transcribed from the game, and an unknown place shows as unknown rather than as zero. The board has no day-by-day score line; prestige is the score.

Up to four partner guilds may join this event. Each accepted partner uses one of five opponent colours, so four partners leave one colour for an enemy. Other siege events allow up to five partners. Each guild in a pair holds one place, and a guild must mark its own base before it can offer the alliance.

Done when:

- An officer can turn an event on, and members of that guild can see the plan. A Normal user who is only a member cannot change the shared plan.
- Ending an event, after confirmation, removes that event's plan and alliance.
- On a siege map, horn shares are visible and are flagged when they do not total 100 percent, and each member can set only their own attack targets.
- On the territory board, painting a place paints the whole place, prestige uses the known rates, and an unconfirmed place does not count as zero.
- Alliance and officer-only actions follow the same people as in [Belong to a guild](#belong-to-a-guild).

## Pay for Premium and sync the Discord role

A signed-in member pays through PayPal and submits a claim with the PayPal transaction id. A payment that arrived as two charges may include a second id. The same id cannot be used twice. A site admin approves the claim, and the member's Premium extends by 30 days from the later of now and the current expiry. The member can see how many days remain, and is reminded during the last five.

Nothing is charged automatically. A member may set a preference that they intend to renew; that preference does not take payment.

A site admin may also grant Premium for 1, 2, or 3 months, or for life, and may revoke a lifetime grant. Every grant, claim, and revocation is kept in a history the admin can search. Approving a claim and granting Premium are the only ways a member becomes Premium.

When a member with linked Discord has active Premium, the site can give them the Premium role on the community Discord server, and remove it when Premium is no longer active. The check uses the member's entitlement and their linked Discord id. A site admin may run that sync for another member.

A site admin may also award Early Supporter to a member who has active Premium. The award is one of 20 permanent places. Revoking it does not open the place again. Early Supporter does not change that member's Premium. The member can opt in to a public list that shows their chosen name and the award date, and nothing else. With Discord linked, the Early Supporter and Test Version roles follow the award and remain if Premium later ends.

Done when:

- A signed-in member can submit one claim for a payment, and cannot reuse a transaction id.
- Until a site admin approves it, the claim does not unlock Premium tools or guild registration.
- An approved claim or a manual grant makes Premium tools available and allows one guild registration for as long as the entitlement is active.
- After Premium ends, Premium tools lock again and a member-registered guild freezes as described in [users](users.md).
- The Discord Premium role matches active Premium for a linked Discord account, and is not given for any other mark.
- A site admin can award Early Supporter only while the member has active Premium, and only while fewer than 20 places have ever been assigned. Revoking an award leaves that place used.
- The public list shows an Early Supporter only after that member opts in, and then only their chosen name and award date.
- The Early Supporter and Test Version Discord roles follow the award for a linked Discord account, including after Premium ends, and are removed when the award is revoked.
