# transcriber doc new

Create an empty document (optionally with its source media), without transcribing.

## Synopsis

```
transcriber doc new [options] <document>
```

## Description

Settings come from the app settings, with --preset, --config and --set. Example: transcriber doc new talk.transcriber --source talk.mov

## Arguments

- `<document>`: The new document ('-' = stdout).

## Options

- `--source <media>`: Source media file.
- `--title <text>`: Title of the source track.
- `--force`: Overwrite an existing file.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber doc](transcriber-doc.md)
- [Output, JSON and exit codes](output.md)
