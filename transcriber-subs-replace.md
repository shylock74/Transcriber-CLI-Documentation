# transcriber subs replace

Find and replace text (plain or regular expression, with $1 groups).

## Synopsis

```
transcriber subs replace [options] <document> <search> <replacement>
```

## Description

Examples:

```
transcriber subs replace talk.transcriber "Jon" "John" --whole-word
transcriber subs replace talk.transcriber '\s+([,.])' '$1' --regex \
    --dry-run
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<search>`: Text to find.
- `<replacement>`: Replacement ('' deletes; $1… with --regex).

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--regex`: The search is a regular expression.
- `-i, --ignore-case`: Ignore case.
- `--whole-word`: Match whole words only.
- `--select <selector>`: Only these subtitles. Subtitles: 12 · 3..7 · 3,5,9 · #<id> · @<time> · all
- `--all-tracks`: Replace in every track.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber subs](transcriber-subs.md)
- [Output, JSON and exit codes](output.md)
