# transcriber dictionaries unuse

Stop a document from using dictionaries ('all' = every one).

## Synopsis

```
transcriber dictionaries unuse [options] <document> <dictionaries>...
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<dictionaries>...`: Dictionaries: names, numbers, ids, or all.

## Options

- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber dictionaries](transcriber-dictionaries.md)
- [Output, JSON and exit codes](output.md)
