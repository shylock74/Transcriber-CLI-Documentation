# transcriber settings export

Write the settings to a file (YAML or JSON) usable with --config and 'settings import'.

## Synopsis

```
transcriber settings export [options]
```

## Description

Example:

```
transcriber settings export --changed -o my-settings.yaml
```

## Options

- `-o, --output <path>`: Output file (default: stdout). Default: `-`.
- `--format <format>`: yaml or json (default: from the extension, else yaml). Values: `yaml`, `json`.
- `--changed`: Only the settings that differ from the factory defaults.
- `--effective`: Include --preset, --config and --set of this command.
- `--force`: Overwrite an existing file.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber settings](transcriber-settings.md)
- [Output, JSON and exit codes](output.md)
