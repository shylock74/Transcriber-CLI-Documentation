# transcriber tracks duplicate

Copy a track (source or translation) to a new translation track.

## Synopsis

```
transcriber tracks duplicate [options] <document> <track>
```

## Description

Example:

```
transcriber tracks duplicate talk.transcriber it --language it-CH \
    --title "Swiss Italian"
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<track>`: Track to copy.

## Options

- `--language <code>`: Language of the copy (default: the same).
- `--title <title>`: Title of the copy (default: '<title> copy').
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber tracks](transcriber-tracks.md)
- [Output, JSON and exit codes](output.md)
