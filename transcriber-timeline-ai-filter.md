# transcriber timeline ai filter

New timeline with the marked sentences and those rated 'much' (no AI call).

## Synopsis

```
transcriber timeline ai filter [options] <document>
```

## Description

Run 'timeline ai rate' first.

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--timeline <timeline>`: Timeline: name, id or number (default: the selected one).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--name <name>`: Name (default: "A2C Filtered").

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber timeline ai](transcriber-timeline-ai.md)
- [Output, JSON and exit codes](output.md)
