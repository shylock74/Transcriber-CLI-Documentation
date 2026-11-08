# transcriber colors rules enable

Turn a rule on.

## Synopsis

```
transcriber colors rules enable [options] [<document>]
```

## Arguments

- `<document>`: Transcriber document (omit with --app). Optional.

## Options

- `--app`: Work on the app's defaults (the palette and rules new documents start from).
- `--rule <rule>`: The rule: its text, number or id.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber colors rules](transcriber-colors-rules.md)
- [Output, JSON and exit codes](output.md)
