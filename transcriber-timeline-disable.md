# transcriber timeline disable

Disable sentences or chapters (left out of the edit, kept in the timeline).

## Synopsis

```
transcriber timeline disable [options] <document>
```

## Description

Example:

```
transcriber timeline disable talk.transcriber --unmarked
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--timeline <timeline>`: Timeline: name, id or number (default: the selected one).
- `--select <selector>`: Sentences: 12 · 3..7 · 3,5,9 · #<id> · @<time> · all (numbers as in 'timeline show').
- `--from <time>`: Only sentences starting at or after this time.
- `--to <time>`: Only sentences starting before this time.
- `--match <regex>`: Only sentences (or chapter titles) matching this regular expression.
- `--ignore-case`: Case-insensitive --match.
- `--marked`: Only marked sentences.
- `--unmarked`: Only sentences that are not marked.
- `--enabled-only`: Only enabled sentences.
- `--disabled-only`: Only disabled sentences.
- `--adherence <level>`: Only sentences with this AI adherence to the context: much, little, zero.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber timeline](transcriber-timeline.md)
- [Output, JSON and exit codes](output.md)
