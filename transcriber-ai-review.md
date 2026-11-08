# transcriber ai review

Review the AI changes one by one: accept, reject or edit each (interactive).

## Synopsis

```
transcriber ai review [options] <document>
```

## Description

For each subtitle changed by the AI, the previous and the new text are shown; answer with one key and Return:

```
y  accept the new text          n  reject it (restore the previous text)
e  edit the text (↑ recalls it)  s  skip (decide later)
a  accept all the remaining      r  reject all the remaining
u  undo the last answer          q  stop here (the answers so far are kept)
```

The document is written at the end (--dry-run: only shown). Needs a terminal; in scripts use 'ai diff', then 'ai accept' / 'ai reject' with --select.

Examples:

```
transcriber ai review talk.transcriber
transcriber ai review talk.transcriber --track en --select 100..
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
