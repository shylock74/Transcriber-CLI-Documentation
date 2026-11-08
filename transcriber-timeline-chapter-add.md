# transcriber timeline chapter add

Insert a chapter before a sentence.

## Synopsis

```
transcriber timeline chapter add [options] <document>
```

## Description

Example:

```
transcriber timeline chapter add talk.transcriber --before 12 \
    --title "Part two"
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--timeline <timeline>`: Timeline: name, id or number (default: the selected one).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--before <N>`: Sentence number (as in 'timeline show'); omit to append at the end.
- `--title <text>`: Chapter title.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber timeline chapter](transcriber-timeline-chapter.md)
- [Output, JSON and exit codes](output.md)
