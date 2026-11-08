# transcriber settings import

Merge a settings file (YAML or JSON, all or some keys) into the app settings.

## Synopsis

```
transcriber settings import [options] <file>
```

## Description

With --replace, keys the file does not have go back to the factory defaults.

## Arguments

- `<file>`: Settings file ('-' = stdin).

## Options

- `--replace`: Replace the settings instead of merging.
- `--dry-run`: Show what would change; write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber settings](transcriber-settings.md)
- [Output, JSON and exit codes](output.md)
