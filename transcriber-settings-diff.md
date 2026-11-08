# transcriber settings diff

Compare two sets of settings.

## Synopsis

```
transcriber settings diff [options] [<a>] [<b>]
```

## Description

Sources: app, effective, factory, preset:<name>, a .transcriber document, or a settings file. One source is compared with the app settings; none compares the app settings with the factory defaults. Examples: transcriber settings diff preset:Interviews · transcriber settings diff talk.transcriber app

## Arguments

- `<a>`: First source (default: factory). Optional.
- `<b>`: Second source (default: app). Optional.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber settings](transcriber-settings.md)
- [Output, JSON and exit codes](output.md)
