# transcriber colors palette add

Add a color.

## Synopsis

```
transcriber colors palette add [options] [<document>]
```

## Description

Examples:

```
transcriber colors palette add talk.transcriber Brand '#E4002B'

    transcriber colors palette add --app Product cyan
```

## Arguments

- `<document>`: Transcriber document (omit with --app). Optional.

## Options

- `--app`: Work on the app's defaults (the palette and rules new documents start from).
- `--name <name>`: Name of the color.
- `--color <color>`: #RRGGBB, #RGB or a color name.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber colors palette](transcriber-colors-palette.md)
- [Output, JSON and exit codes](output.md)
