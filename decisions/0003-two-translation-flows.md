# 0003 — Two translation flows

Status: accepted.

English is the source language. German, French, Russian, and Spanish are the translations. A missing translation shows the English source. 

The two flows stay apart because the English is written by different people and becomes visible in a different way. 

While flows seems the same the core difference is that interface translation is a translation workbench while editable content translation is a content editing workbench.

## Interface strings

The fixed UI strings, the calculator labels, Benben’s wording, etc. The English is part of the product. Adding or changing an English string ships with the app. A translation of an existing string is stored and shown on the next visit. Saving one does not deploy the app.

A site admin assigns a member one or more of the four target languages. Several members may hold the same language. An assigned member can fill interface strings in those languages and cannot change the English. Two people saving the same string: the later save wins.

## Editable content

News, guides, and event write-ups. An Editor, or a site admin, writes the English piece. An assigned member fills that piece in their languages. The translation is stored with the piece. After the piece is public, the language URL shows it on the next visit. No deploy is required.

A language assignment does not allow creating a piece, changing the English, or publishing. Publishing stays the publish permission. See [Prepare](../features/content/prepare.md) and [Publish](../features/content/publish.md).

## See also

[Interface strings](../features/content/interface-strings.md), [Language URLs](../features/reading/language-urls.md), [Users](../product/users.md).
