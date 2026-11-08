# transcriber doc settings diff

Compare the document's settings with the app settings (or another source).

## Synopsis

```
transcriber doc settings diff [options] <document>
```

## Description

Sources: app, effective, factory, preset:<name>, a .transcriber document, a settings file.

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--against <source>`: Compare with (default: app). Default: `app`.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber doc settings](transcriber-doc-settings.md)
- [Output, JSON and exit codes](output.md)
