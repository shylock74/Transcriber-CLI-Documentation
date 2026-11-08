# transcriber tracks rename

Change the language code or title of a track ('source' renames the source title).

## Synopsis

```
transcriber tracks rename [options] <document> <track>
```

## Description

Example:

```
transcriber tracks rename talk.transcriber it --title "Italiano (rev. 2)"
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<track>`: Track.

## Options

- `--language <code>`: New language code.
- `--title <title>`: New title.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber tracks](transcriber-tracks.md)
- [Output, JSON and exit codes](output.md)
