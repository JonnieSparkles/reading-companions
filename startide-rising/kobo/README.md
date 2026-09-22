# Startide Rising — Kobo companion dictionary

A book-specific glossary for David Brin's *Startide Rising*, designed for Kobo's normal long-press dictionary popup.

**Installable file:** [dicthtml-x1startide.zip](./dicthtml-x1startide.zip) — a Kobo-compatible filename. Its `x1` prefix is a deliberately unused custom locale code, followed by `startide` so you can identify the book. The original `dicthtml-startide.zip` started with `st`, the ISO language code for Sesotho, causing Kobo to mislabel it.

**Editable source:** [startide-rising.df](./startide-rising.df), in the [dictgen](https://github.com/pgaskin/dictutil) dictionary format.

The glossary has **76 entries**: 60 headwords from the glossary in the supplied EPUB, paraphrased and expanded, plus 16 companion additions for terms that occur in the book but weren't explained in that glossary (including Trinary, Anglic, Whale Dream, Streaker, and Kithrup). Available pronunciation hints and alternative spellings are included. The EPUB's prose is not redistributed.

## Install (no software required)

1. Delete the old `dicthtml-startide.zip` from your Kobo if you previously installed it (it was incorrectly displayed as Sesotho). Download `dicthtml-x1startide.zip` above. **Do not unzip it.**
2. Connect your Kobo by USB, show hidden folders, and copy the ZIP to `KOBOeReader/.kobo/custom-dict/` (create `custom-dict` if necessary).
3. Safely eject your Kobo. Open *Startide Rising*, long-press a known term such as **Creideiki**, then select **dicthtml-x1startide.zip** in the dictionary picker (on recent Kobo firmware it will usually show the literal filename because `x1` is not a built-in language).
4. Kobo remembers the selected dictionary independently for each book (confirmed by device testing). To look up an ordinary English word, switch to the built-in English dictionary in the same popup; switching back to the book glossary is straightforward.

Recent Kobo firmware (4.24.15672+) supports custom dictionaries in `.kobo/custom-dict/`. Older firmware may need patches. The prefix `dicthtml-` is required; using an arbitrary book name immediately after it can collide with a real language code. `x1` avoids that collision, but Kobo may show the raw filename instead of a pretty title. On the tested Kobo, the glossary works in the native popup and per-book dictionary choice persists. Other models or firmware versions may behave differently.

### Normal English words

This edition is **glossary-only**. It does not replace the Kobo's English dictionary. For an ordinary word not covered here, choose your existing English dictionary. Because Kobo remembers the dictionary selected for each book and switching to English is straightforward, a merged English dictionary is optional, not necessary for this workflow.

## Rebuild (optional)

Download `dictgen` from [pgaskin/dictutil](https://github.com/pgaskin/dictutil/releases), then run this command from this folder:

```bash
dictgen -o dicthtml-x1startide.zip startide-rising.df
```

You do **not** need dictgen to use the supplied ZIP.

## Scope

The original headword list and pronunciations came from the EPUB's *Glossary and Cast of Characters*. The 16 additions describe terms present in the novel. Definitions are paraphrases, kept to introductory information or details already revealed by the novel's front-matter glossary. This is not a chapter-aware, spoiler-filtered dictionary.

No Kobo database edits, firmware replacements or permanent GitHub Actions are required.
