# transcriber ai metadata export

Export every result of a document to Markdown, text or JSON.

## Synopsis

```
transcriber ai metadata export [options] <document>
```

## Description

Example:

```
transcriber ai metadata export talk.transcriber -o talk-metadata.md
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-o, --output <path>`: Output file ('-' = stdout, the default). Default: `-`.
- `--format <format>`: md, txt or json (default: from the extension, else md).
- `--force`: Overwrite an existing file.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber ai metadata](transcriber-ai-metadata.md)
- [Output, JSON and exit codes](output.md)
