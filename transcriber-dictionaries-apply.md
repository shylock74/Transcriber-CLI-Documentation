# transcriber dictionaries apply

Run dictionaries' replacements on a document's subtitles now.

## Synopsis

```
transcriber dictionaries apply [options] <document> [<dictionaries>...]
```

## Description

Without dictionaries: the ones the document uses.

Example:

```
transcriber dictionaries apply talk.transcriber --dry-run
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<dictionaries>...`: Dictionaries (default: those of the document). Optional.

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber dictionaries](transcriber-dictionaries.md)
- [Output, JSON and exit codes](output.md)
