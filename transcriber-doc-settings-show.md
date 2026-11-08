# transcriber doc settings show

Show the document's settings (all, a section, or one key).

## Synopsis

```
transcriber doc settings show [options] <document> [<key>]
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<key>`: A section or key. Optional.

## Options

- `--changed`: Only the settings that differ from the factory defaults.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber doc settings](transcriber-doc-settings.md)
- [Output, JSON and exit codes](output.md)
