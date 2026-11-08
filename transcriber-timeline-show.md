# transcriber timeline show

Show a timeline's sentences: number, state, timecodes, text.

## Synopsis

```
transcriber timeline show [options] <document>
```

## Description

Marks: ✓ enabled · ✗ disabled · ★ marked · ▸ chapter. With --text only the text of the enabled sentences is printed (as the edit would read).

Examples:

```
transcriber timeline show talk.transcriber
transcriber timeline show talk.transcriber --timeline "Cut 1" --marked
transcriber timeline show talk.transcriber --text > cut.txt
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
- `--text`: Only the text of the enabled sentences, one paragraph each.
- `--hide-disabled`: Leave out the disabled sentences.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber timeline](transcriber-timeline.md)
- [Output, JSON and exit codes](output.md)
