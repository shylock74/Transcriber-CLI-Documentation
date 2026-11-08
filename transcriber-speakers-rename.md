# transcriber speakers rename

Rename a speaker everywhere (every track).

## Synopsis

```
transcriber speakers rename [options] <document> <old> <new>
```

## Description

Example:

```
transcriber speakers rename talk.transcriber "SPEAKER 1" Anna
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<old>`: Current name (case-insensitive).
- `<new>`: New name ('' removes the speaker).

## Options

- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber speakers](transcriber-speakers.md)
- [Output, JSON and exit codes](output.md)
