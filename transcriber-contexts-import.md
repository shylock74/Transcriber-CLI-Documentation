# transcriber contexts import

Import files as new contexts (name from the file name).

## Synopsis

```
transcriber contexts import [options] <file>...
```

## Description

Example:

```
transcriber contexts import ~/Contexts/*.yaml
```

## Arguments

- `<file>...`: Files (.yaml, .json, .md, .txt; others are sniffed).

## Options

- `--disabled`: Not enabled by default.
- `--dry-run`: Show what would be imported.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber contexts](transcriber-contexts.md)
- [Output, JSON and exit codes](output.md)
