# transcriber ai reject

Reject AI changes: restore the previous text.

## Synopsis

```
transcriber ai reject [options] <document>
```

## Description

Examples:

```
transcriber ai reject talk.transcriber
```

 transcriber ai reject

```
    talk.transcriber --select 12
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--select <selector>`: Only these subtitles. Subtitles: 12 · 3..7 · 3,5,9 · #<id> · @<time> · all
- `--from <time>`: Only subtitles starting at or after this time.
- `--to <time>`: Only subtitles starting before this time.
- `--match <regex>`: Only subtitles whose text matches this regular expression.
- `--ignore-case`: Case-insensitive --match.
- `--speaker <name>`: Only subtitles of this speaker.
- `--enabled-only`: Only enabled subtitles.
- `--disabled-only`: Only disabled subtitles.
- `--ai-modified`: Only subtitles changed by AI and not yet reviewed.
- `--longer-than <N>`: Only subtitles longer than N characters.
- `--shorter-than <seconds>`: Only subtitles shorter than N seconds.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber ai](transcriber-ai.md)
- [Output, JSON and exit codes](output.md)
