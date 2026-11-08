# transcriber timeline chapter rename

Rename a chapter.

## Synopsis

```
transcriber timeline chapter rename [options] <document> <N> <title>
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<N>`: Chapter number (as in 'timeline show').
- `<title>`: New title.

## Options

- `--timeline <timeline>`: Timeline: name, id or number (default: the selected one).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber timeline chapter](transcriber-timeline-chapter.md)
- [Output, JSON and exit codes](output.md)
