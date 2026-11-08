# transcriber subs split

Split subtitles at line breaks, at given strings, or at the soft separators.

## Synopsis

```
transcriber subs split [options] <document> <selector>
```

## Description

Time is shared out in proportion to the length of each piece. Without --on: split at line breaks when there are any, else at the soft separators of the document's settings (whisperSettings.softSeparators).

Examples:

```
transcriber subs split talk.transcriber 12
transcriber subs split talk.transcriber 12 --on ", and" --on "; "
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<selector>`: Subtitles: 12 · 3..7 · 3,5,9 · #<id> · @<time> · all

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--on <string>`: Split after this string. Repeatable. Repeatable.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber subs](transcriber-subs.md)
- [Output, JSON and exit codes](output.md)
