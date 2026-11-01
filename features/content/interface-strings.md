# Interface strings

Status: draft.

The site name, navigation, buttons, menus, footer, and short messages such as errors, plus the calculator labels, Benben’s wording, and the category names, are interface strings. English is the source and is part of the product. Adding or changing an English string ships with the app. A translation of an existing string is stored and shown on the next visit. Saving one does not deploy the app.

A site admin assigns a member one or more of German, French, Russian, and Spanish. Several members may hold the same language. An assigned member fills those languages and cannot change the English. When two people save the same string, the later save wins.

This is not the editor for news, guides, or event write-ups. Those translations are defined in [Prepare](prepare.md). The split is recorded in [Two translation flows](../../decisions/0003-two-translation-flows.md).

A missing translation shows the English source, as defined in [Language URLs](../reading/language-urls.md).

## Done when

- An assigned member can save a translation of an interface string in an assigned language.
- A member with no language assignment cannot change interface strings.
- Nobody with only a language assignment can change the English source.
- A saved interface translation is what the language URL shows on the next visit.
- An untranslated interface string shows its English source.
