# transcriber timeline chapter remove

Remove chapters (all with --all; the sentences stay).

## Synopsis

```
transcriber timeline chapter remove [options] <document> [<N>...]
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<N>...`: Chapter numbers (as in 'timeline show'). Optional.

## Options

- `--timeline <timeline>`: Timeline: name, id or number (default: the selected one).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--all`: Every chapter.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber timeline chapter](transcriber-timeline-chapter.md)
- [Output, JSON and exit codes](output.md)
