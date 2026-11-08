# transcriber dictionaries import

Import a dictionary file (.TrDict, as exported by the app or 'dictionaries export').

## Synopsis

```
transcriber dictionaries import [options] <file>
```

## Description

An imported dictionary with the id of an existing one replaces it only with --replace.

## Arguments

- `<file>`: File ('-' = stdin).

## Options

- `--replace`: Replace a dictionary with the same id.
- `--dry-run`: Show what would change; write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber dictionaries](transcriber-dictionaries.md)
- [Output, JSON and exit codes](output.md)
