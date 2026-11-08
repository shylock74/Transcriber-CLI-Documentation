# transcriber ai metadata remove

Remove prompts (and their results) from a document.

## Synopsis

```
transcriber ai metadata remove [options] <document> [<prompt>...]
```

## Description

Examples:

```
transcriber ai metadata remove talk.transcriber Chapters
```

 transcriber

```
    ai metadata remove talk.transcriber --all --yes
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<prompt>...`: Prompts: name, id or number in the document's list. Optional.

## Options

- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--all`: Every prompt.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber ai metadata](transcriber-ai-metadata.md)
- [Output, JSON and exit codes](output.md)
