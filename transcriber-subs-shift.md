# transcriber subs shift

Move subtitles in time.

## Synopsis

```
transcriber subs shift [options] <document> <offset>
```

## Description

Examples:

```
transcriber subs shift talk.transcriber -- -1.5  (all, 1.5 s earlier)
transcriber subs shift talk.transcriber 0.250 --select 40..
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<offset>`: Offset: seconds or a time, negative = earlier (write '-- -1.5').

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--select <selector>`: Only these subtitles. Subtitles: 12 · 3..7 · 3,5,9 · #<id> · @<time> · all
- `--all-tracks`: Shift every track (ignores --track and --select).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber subs](transcriber-subs.md)
- [Output, JSON and exit codes](output.md)
