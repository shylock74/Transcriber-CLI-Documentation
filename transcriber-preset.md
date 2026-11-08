# transcriber preset

Named settings presets (shared with the app): list, save, apply, import, export.

## Synopsis

```
transcriber preset <command> [options]
```

## Description

Use a preset for one command with the global option --preset <name>; apply it to the app settings or to a document with 'preset apply'.

## Commands

- [`list`](transcriber-preset-list.md): List the presets, newest first.
- [`show`](transcriber-preset-show.md): Show a preset's settings (by default those that differ from the factory defaults).
- [`save`](transcriber-preset-save.md): Save settings as a preset (replaces one with the same name).
- [`apply`](transcriber-preset-apply.md): Apply a preset to the app settings (--app) or to a document's settings.
- [`rename`](transcriber-preset-rename.md): Rename a preset.
- [`delete`](transcriber-preset-delete.md): Delete a preset (asks first; --yes skips).
- [`import`](transcriber-preset-import.md): Import a preset: a file from 'preset export', or any settings file (with --name).
- [`export`](transcriber-preset-export.md): Write a preset to a JSON file (its changed settings), for 'preset import' on another Mac.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
