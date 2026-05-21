# Wildbits F256K2 Syntax File For Fresh TUI 

This is my attempt to make a fresh language pack for the F256K2s SuperBasic language. In theory this is a sublime YAML format so it might work for sublime text as well though I haven't tried. The idea is just to provide some syntax highlighting features for SuperBasic so I don't have to start at all white in the editor :)

## Features

- Syntax highlighting via Sublime syntax grammar
- Language configuration (comments, indentation)
- LSP integration (if configured)

## Installation

### Now
1. Ctrl-P
2. Find Package Install From URL
3. Enter full path to this repo
4. Reopen fresh

### Eventually
(This won't work until you submit a PR into fresh's repo)
Install via Fresh's package manager:
```
:pkg install superbasic
```

## Configuration

This language pack provides:

### Grammar
- File extensions: `.ext` (update in package.json)
- Syntax highlighting rules in `grammars/syntax.sublime-syntax`

### Language Settings
- Comment prefix: `//`
- Tab size: 4 spaces
- Auto-indent: enabled

Update `package.json` to match your language's requirements.

## Development

1. Edit `grammars/syntax.sublime-syntax` for syntax highlighting
2. Update `package.json` with correct file extensions and LSP command
3. Test by copying to `~/.config/fresh/grammars/` and restarting Fresh

**Tip:** Search GitHub for existing `<language> sublime-syntax` files you can adapt.
If using an existing grammar, check its license and include a copy in `grammars/LICENSE`.

## Grammar Attribution

<!-- If you used an existing grammar, add attribution here: -->
<!-- The syntax grammar is derived from [original](https://github.com/user/repo) -->
<!-- by Original Author, licensed under MIT. See `grammars/LICENSE` for details. -->

## Resources

- [Sublime Text Syntax Documentation](https://www.sublimetext.com/docs/syntax.html)
- [Scope Naming Conventions](https://www.sublimetext.com/docs/scope_naming.html)

## License

MIT
