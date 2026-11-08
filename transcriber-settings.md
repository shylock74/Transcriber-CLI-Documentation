# transcriber settings

The app's settings (shared with the app): get, set, list, import, export, diff.

## Synopsis

```
transcriber settings <command> [options]
```

## Description

Keys are dotted paths, as 'settings keys' lists them: whisperSettings.model, srtSettings.maxCharPerLine, whisperSettings.vad.threshold, defaultExport.0.format.

These settings are the defaults of new documents. One command can override them without changing them with the global --set key=value, --preset <name> and --config <file>. A document keeps its own settings: see 'transcriber doc settings'.

## Commands

- [`list`](transcriber-settings-list.md): Show the settings (all, or one section) as YAML.
- [`get`](transcriber-settings-get.md): Print one setting's value.
- [`set`](transcriber-settings-set.md): Change app settings: key=value pairs.
- [`unset`](transcriber-settings-unset.md): Put settings back to their factory value (a key or a whole section).
- [`keys`](transcriber-settings-keys.md): List every settings key with its type and current value.
- [`reset`](transcriber-settings-reset.md): Put every app setting back to the factory defaults (asks first; --yes skips).
- [`import`](transcriber-settings-import.md): Merge a settings file (YAML or JSON, all or some keys) into the app settings.
- [`export`](transcriber-settings-export.md): Write the settings to a file (YAML or JSON) usable with --config and 'settings import'.
- [`diff`](transcriber-settings-diff.md): Compare two sets of settings.
- [`path`](transcriber-settings-path.md): Print where the app settings are stored.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
