# transcriber keys authorize

Let the command line read the AI keys stored by the app (macOS asks once per key).

## Synopsis

```
transcriber keys authorize [options]
```

## Description

Keys saved by the app trust only the app: macOS asks before another program reads them. Without this step the command line skips those keys (it never waits for a dialog). Run it in a terminal and answer "Always Allow" to each dialog.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber keys](transcriber-keys.md)
- [Output, JSON and exit codes](output.md)
