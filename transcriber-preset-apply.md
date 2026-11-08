# transcriber preset apply

Apply a preset to the app settings (--app) or to a document's settings.

## Synopsis

```
transcriber preset apply [options] <name> [<document>]
```

## Description

Examples:

```
transcriber preset apply Interviews --app
transcriber preset apply Interviews talk.transcriber
```

## Arguments

- `<name>`: Preset name.
- `<document>`: Transcriber document (omit with --app). Optional.

## Options

- `--app`: Apply to the app settings.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber preset](transcriber-preset.md)
- [Output, JSON and exit codes](output.md)
