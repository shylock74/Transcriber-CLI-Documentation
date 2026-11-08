# transcriber settings list

Show the settings (all, or one section) as YAML.

## Synopsis

```
transcriber settings list [options] [<key>]
```

## Description

Examples:

```
transcriber settings list whisperSettings
transcriber settings list --changed
```

## Arguments

- `<key>`: A section or key (default: everything). Optional.

## Options

- `--changed`: Only the settings that differ from the factory defaults.
- `--effective`: Include --preset, --config and --set of this command (what a new document would get).

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber settings](transcriber-settings.md)
- [Output, JSON and exit codes](output.md)
