# Sign in

Status: draft.

A player signs in with Discord, or with a username and password, and keeps the site rank stored for them. Someone signing in for the first time is a Normal user. They can sign out.

A username is 3 to 24 letters, numbers, or underscores, and it stays the sign-in name. The member does not enter an email address. A password account can link Discord later. Linking adds Discord to that account. It does not merge two accounts that already exist. A public display name can be changed after Discord is linked.

GitHub, Google, and other providers can be added later. Each one is another way into the same account. Adding a provider does not create a new site rank or a second membership.

Who may do what after sign-in is defined in [Site rank](site-rank.md). How the Discord role follows that rank is defined in [Discord role sync](discord-role-sync.md).

## Done when

- A successful sign-in, with Discord or with a username and password, produces a session and exactly one site rank: the rank already stored, or Normal user when none is stored.
- Linking Discord attaches it to the account that is already signed in, and leaves any other existing account as it is.
- A refused or incomplete sign-in leaves the person anonymous and tells them what to do next, without showing raw error text from the provider.
