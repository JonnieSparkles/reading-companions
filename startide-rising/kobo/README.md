# Startide Rising — Kobo companion dictionary

A book-specific glossary for David Brin's *Startide Rising*, designed for Kobo's normal long-press dictionary popup.

**Installable file:** [dicthtml-startide.zip](./dicthtml-startide.zip) — a descriptive Kobo custom-dictionary filename, not the earlier cryptic `s1` name.

**Editable source:** [startide-rising.df](./startide-rising.df), in the [dictgen](https://github.com/pgaskin/dictutil) dictionary format.

The glossary has **76 entries**: 60 headwords from the glossary in the supplied EPUB, paraphrased and expanded, plus 16 companion additions for terms that occur in the book but weren't explained in that glossary (including Trinary, Anglic, Whale Dream, Streaker, and Kithrup). Available pronunciation hints and alternative spellings are included. The EPUB's prose is not redistributed.

## Install (no software required)

1. Download `dicthtml-startide.zip` above. **Do not unzip it.**
2. Connect your Kobo by USB, show hidden folders, and copy the ZIP to `KOBOeReader/.kobo/custom-dict/` (create `custom-dict` if necessary).
3. Safely eject your Kobo. Open *Startide Rising*, long-press a known term such as **Creideiki**, then select the **Startide** custom dictionary in the dictionary picker.
4. Close and reopen the book; test a second word. Switch to another book and back to see whether your Kobo remembers the selected dictionary separately. **Per-book persistence still needs a device test.**

Recent Kobo firmware (4.24.15672+) supports custom dictionaries in `.kobo/custom-dict/`. Older firmware may need patches. Descriptive custom dictionary names work on many models, but device-specific naming or remembered-selection behavior is not guaranteed.

### Normal English words

This edition is **glossary-only**. It does not replace the Kobo's English dictionary. For an ordinary word not covered here, choose your existing English dictionary. A later edition could merge a separately licensed English source if Kobo remembers the custom choice.

## Rebuild (optional)

Download `dictgen` from [pgaskin/dictutil](https://github.com/pgaskin/dictutil/releases), then run this command from this folder:

```bash
dictgen -o dicthtml-startide.zip startide-rising.df
```

You do **not** need dictgen to use the supplied ZIP.

## Scope

The original headword list and pronunciations came from the EPUB's *Glossary and Cast of Characters*. The 16 additions describe terms present in the novel. Definitions are paraphrases, kept to introductory information or details already revealed by the novel's front-matter glossary. This is not a chapter-aware, spoiler-filtered dictionary.

No Kobo database edits, firmware replacements or permanent GitHub Actions are required.
