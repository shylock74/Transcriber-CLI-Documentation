# transcriber doc tc-start

Show or override the start timecode used by exports (e.g. 01:00:00:00).

## Synopsis

```
transcriber doc tc-start [options] <document> [<timecode>]
```

## Description

Examples:

```
transcriber doc tc-start talk.transcriber 01:00:00:00
transcriber doc tc-start talk.transcriber --off
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<timecode>`: New start timecode. Optional.

## Options

- `--off`: Stop overriding (use the media's own start).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber doc](transcriber-doc.md)
- [Output, JSON and exit codes](output.md)
