# transcriber ai metadata clear

Delete the results of prompts, keeping the prompts (asks first).

## Synopsis

```
transcriber ai metadata clear [options] <document> [<prompt>...]
```

## Description

Example:

```
transcriber ai metadata clear talk.transcriber Chapters
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<prompt>...`: Prompts (default: every one). Optional.

## Options

- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber ai metadata](transcriber-ai-metadata.md)
- [Output, JSON and exit codes](output.md)
