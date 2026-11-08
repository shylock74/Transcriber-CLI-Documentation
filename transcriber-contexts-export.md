# transcriber contexts export

Write a context's content to a file (default: <name>.<format>).

## Synopsis

```
transcriber contexts export [options] <context>
```

## Description

Examples:

```
transcriber contexts export "Product names"
```

 transcriber contexts

```
    export 1 -o - | less
```

## Arguments

- `<context>`: Context: name, id or number.

## Options

- `-o, --output <path>`: Output file ('-' = stdout).
- `--force`: Overwrite an existing file.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber contexts](transcriber-contexts.md)
- [Output, JSON and exit codes](output.md)
