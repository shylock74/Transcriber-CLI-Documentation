# transcriber tracks fixed-text

Show, set or clear the fixed (reference) text of a translation track.

## Synopsis

```
transcriber tracks fixed-text [options] <document> <track>
```

## Description

The fixed text is the approved translation the subtitles must match (used by alignment).

Examples:

```
transcriber tracks fixed-text talk.transcriber it
transcriber tracks fixed-text talk.transcriber it \
    --from-file approved-it.txt
transcriber tracks fixed-text talk.transcriber it --clear
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<track>`: Translation track.

## Options

- `--from-file <file>`: Store the text of this file ('-' = stdin).
- `--clear`: Remove the fixed text.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber tracks](transcriber-tracks.md)
- [Output, JSON and exit codes](output.md)
