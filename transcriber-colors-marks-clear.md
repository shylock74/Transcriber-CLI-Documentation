# transcriber colors marks clear

Remove manual marks (rules stay).

## Synopsis

```
transcriber colors marks clear [options] <document>
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--select <selector>`: Only these subtitles. Subtitles: 12 · 3..7 · 3,5,9 · #<id> · @<time> · all
- `--all-tracks`: Every track.
- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber colors marks](transcriber-colors-marks.md)
- [Output, JSON and exit codes](output.md)
