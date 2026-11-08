# transcriber preset save

Save settings as a preset (replaces one with the same name).

## Synopsis

```
transcriber preset save [options] <name>
```

## Description

Saves the app settings (with this command's --set/--config), a document's settings (--from-doc) or a settings file (--from-file, over the factory defaults). Example: transcriber preset save "Interviews IT" --set whisperSettings.language=it

## Arguments

- `<name>`: Preset name.

## Options

- `--from-doc <document>`: Take the settings of this document.
- `--from-file <file>`: Take the settings of this YAML/JSON file.
- `--dry-run`: Show what would change; write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber preset](transcriber-preset.md)
- [Output, JSON and exit codes](output.md)
