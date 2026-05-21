# SuperBASIC Language Pack for Fresh

A small Fresh language pack for writing Foenix F256K2 SuperBASIC without staring
at a wall of plain white text. It is not a full IDE, but it does know enough
SuperBASIC to make programs easier to scan while you poke at retro hardware and
pretend the bugs are period-correct.

The grammar is written in Sublime's `.sublime-syntax` YAML format, so it may also
work in Sublime Text. Fresh is the target editor, though.

## What It Does

- Highlights SuperBASIC keywords, functions, operators, labels, numbers, and
  strings.
- Highlights comments written with `'` or `REM`.
- Recognizes common SuperBASIC file extensions in the grammar:
  `.bas`, `.sb`, `.sbas`, and `.superbasic`.
- Includes 65C02 mnemonics for inline assembly blocks.
- Provides a Fresh package manifest so the grammar can be installed locally.

## Current Rough Edges

This is still a tiny, practical language pack rather than a perfect language
definition.

- The Fresh language comment prefix is currently `//`, which is a placeholder.
  SuperBASIC comments are highlighted as `'` and `REM`.
- The LSP entry points at `language-server`, also as a placeholder. There is no
  SuperBASIC language server bundled here.

## Installation

For local testing in Fresh, use Fresh's package-from-URL flow:

1. Open the command palette with `Ctrl-P`.
2. Choose `Package Install From URL`.
3. Enter the full local path to this repository.
4. Restart or reopen Fresh if the grammar does not show up immediately.

Fresh's language-pack development docs cover the same workflow:
https://getfresh.dev/docs/plugins/development/language-packs#testing-with-local-path-recommended

Once this package is published through Fresh's package registry, installation
should eventually look like this:

```text
:pkg install superbasic
```

That command is future tense. For now, local path install is the useful bit.

## Files

- `package.json` defines the Fresh package metadata.
- `grammars/syntax.sublime-syntax` contains the SuperBASIC highlighting rules.
- `validate.sh` validates the package manifest against Fresh's package schema.

## Development

Most changes belong in `grammars/syntax.sublime-syntax`.

After editing the grammar:

1. Reinstall or reload the local package in Fresh.
2. Open a SuperBASIC source file.
3. Check strings, comments, labels, numbers, keywords, and any new syntax you
   touched.

To validate the package manifest, install `jsonschema` for Python if needed and
run:

```bash
./validate.sh
```

The validator downloads Fresh's current package validation script, so it needs
network access.

## Useful References

- [Fresh language-pack docs](https://getfresh.dev/docs/plugins/development/language-packs)
- [Sublime Text syntax documentation](https://www.sublimetext.com/docs/syntax.html)
- [Sublime scope naming conventions](https://www.sublimetext.com/docs/scope_naming.html)

## License

MIT
