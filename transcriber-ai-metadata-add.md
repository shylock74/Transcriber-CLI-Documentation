# transcriber ai metadata add

Add library prompts (or a set) to a document.

## Synopsis

```
transcriber ai metadata add [options] <document> [<prompt>...]
```

## Description

Examples:

```
transcriber ai metadata add talk.transcriber Chapters "YouTube title"

    transcriber ai metadata add talk.transcriber --from-set Podcast
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<prompt>...`: Prompts: name, id or number (see 'ai metadata prompts'). Optional.

## Options

- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--from-set <set>`: Add every prompt of this set.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber ai metadata](transcriber-ai-metadata.md)
- [Output, JSON and exit codes](output.md)
