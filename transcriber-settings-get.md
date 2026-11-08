# transcriber settings get

Print one setting's value.

## Synopsis

```
transcriber settings get [options] <key>
```

## Description

Example:

```
transcriber settings get whisperSettings.language
```

## Arguments

- `<key>`: Key.

## Options

- `--effective`: Include --preset, --config and --set of this command.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber settings](transcriber-settings.md)
- [Output, JSON and exit codes](output.md)
