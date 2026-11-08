# transcriber contexts set-content

Replace a context's content with a file or stdin.

## Synopsis

```
transcriber contexts set-content [options] <context> <path>
```

## Description

Example:

```
transcriber contexts set-content "Product names" products.yaml
```

## Arguments

- `<context>`: Context: name, id or number.
- `<path>`: Content file ('-' = stdin).

## Options

- `--dry-run`: Show the size change only.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber contexts](transcriber-contexts.md)
- [Output, JSON and exit codes](output.md)
