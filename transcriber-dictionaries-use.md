# transcriber dictionaries use

Make a document apply dictionaries after transcription (and send their prompts to Whisper).

## Synopsis

```
transcriber dictionaries use [options] <document> <dictionaries>...
```

## Description

Example:

```
transcriber dictionaries use talk.transcriber "Brand names" Medical
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<dictionaries>...`: Dictionaries: names, numbers or ids.

## Options

- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber dictionaries](transcriber-dictionaries.md)
- [Output, JSON and exit codes](output.md)
