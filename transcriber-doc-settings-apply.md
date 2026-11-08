# transcriber doc settings apply

Replace the document's settings with the app settings, a preset or a settings file.

## Synopsis

```
transcriber doc settings apply [options] <document>
```

## Description

--from-file merges the file's keys into the document's settings. Examples: transcriber doc settings apply talk.transcriber --from-app · transcriber doc settings apply talk.transcriber --from-preset Interviews

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--from-app`: The app settings (with this command's --set/--config/--preset).
- `--from-preset <name>`: A preset.
- `--from-file <file>`: A YAML/JSON settings file (merged).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber doc settings](transcriber-doc-settings.md)
- [Output, JSON and exit codes](output.md)
