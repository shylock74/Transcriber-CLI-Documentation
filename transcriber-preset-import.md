# transcriber preset import

Import a preset: a file from 'preset export', or any settings file (with --name).

## Synopsis

```
transcriber preset import [options] <file>
```

## Arguments

- `<file>`: File ('-' = stdin).

## Options

- `--name <name>`: Preset name (default: the one in the file).
- `--dry-run`: Show what would change; write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber preset](transcriber-preset.md)
- [Output, JSON and exit codes](output.md)
