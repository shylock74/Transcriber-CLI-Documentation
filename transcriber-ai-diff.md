# transcriber ai diff

Show the subtitles changed by the AI: previous text and new text.

## Synopsis

```
transcriber ai diff [options] <document>
```

## Description

Example:

```
transcriber ai diff talk.transcriber --track it
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

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber ai](transcriber-ai.md)
- [Output, JSON and exit codes](output.md)
