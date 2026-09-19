# Startide Rising — Kobo glossary spike

Goal: use Kobo's native long-press dictionary popup for book-specific terms.

This spike uses a unique custom-dictionary locale, `s1`. On recent Kobo firmware, custom dictionaries can be copied into `.kobo/custom-dict/` and selected from the normal dictionary dropdown.

## Build

Download `dictgen` from [pgaskin/dictutil](https://github.com/pgaskin/dictutil/releases), then from this folder run:

```bash
dictgen -o dicthtml-s1.zip startide-rising.df
```

On Windows, the equivalent is:

```powershell
.\dictgen-windows.exe -o dicthtml-s1.zip startide-rising.df
```

## Install / device test

1. Connect the Kobo by USB.
2. Copy `dicthtml-s1.zip` to `.kobo/custom-dict/`.
3. Safely eject the Kobo.
4. Open *Startide Rising*.
5. Long-press a glossary term such as `Tymbrimi` or `Creideiki`.
6. Choose the `s1` custom dictionary from the dictionary selector.
7. Close the book, open another book, then return to *Startide Rising* and long-press another term.

The important test is whether Kobo remembers that dictionary choice for this book without affecting the dictionary selected in other books.

## Scope

This first dictionary is intentionally glossary-only. It does **not** yet merge a normal English dictionary. If the per-book persistence test works, the next version can merge an open English dictionary with these entries so ordinary-word lookup continues to work without switching dictionaries.

Definitions are intentionally short and spoiler-light.
