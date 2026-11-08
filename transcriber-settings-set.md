# transcriber settings set

Change app settings: key=value pairs.

## Synopsis

```
transcriber settings set [options] <key=value>...
```

## Description

Values are typed after the current value (true/false, numbers, strings; JSON for lists and objects). An invalid value is refused with the current one. Example: transcriber settings set whisperSettings.language=it srtSettings.maxCharPerLine=38

## Arguments

- `<key=value>...`: key=value pairs.

## Options

- `--dry-run`: Show what would change; write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber settings](transcriber-settings.md)
- [Output, JSON and exit codes](output.md)
