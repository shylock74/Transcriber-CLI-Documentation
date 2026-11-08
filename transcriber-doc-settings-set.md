# transcriber doc settings set

Change the document's settings: key=value pairs.

## Synopsis

```
transcriber doc settings set [options] <document> <key=value>...
```

## Description

Example:

```
transcriber doc settings set talk.transcriber \
    srtSettings.maxCharPerLine=32 srtSettings.maxLines=1
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<key=value>...`: key=value pairs.

## Options

- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber doc settings](transcriber-doc-settings.md)
- [Output, JSON and exit codes](output.md)
