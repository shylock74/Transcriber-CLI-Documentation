# transcriber contexts convert

Change a context's declared format (the content is kept as it is).

## Synopsis

```
transcriber contexts convert [options] <context>
```

## Description

To turn free text into a YAML entity list with the AI, use 'contexts structure'.

## Arguments

- `<context>`: Context: name, id or number.

## Options

- `--to <format>`: yaml, json, md or txt. Values: `yaml`, `json`, `md`, `txt`.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber contexts](transcriber-contexts.md)
- [Output, JSON and exit codes](output.md)
