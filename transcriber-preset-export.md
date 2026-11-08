# transcriber preset export

Write a preset to a JSON file (its changed settings), for 'preset import' on another Mac.

## Synopsis

```
transcriber preset export [options] <name>
```

## Arguments

- `<name>`: Preset name.

## Options

- `-o, --output <path>`: Output file (default: <name>.json; '-' = stdout).
- `--force`: Overwrite an existing file.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber preset](transcriber-preset.md)
- [Output, JSON and exit codes](output.md)
