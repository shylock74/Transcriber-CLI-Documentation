# transcriber ai metadata show

Print a prompt's result text on stdout (the selected one, or every one).

## Synopsis

```
transcriber ai metadata show [options] <document> <prompt>
```

## Description

Example:

```
transcriber ai metadata show talk.transcriber Chapters > chapters.md
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<prompt>`: Prompt: name, id or number in the document's list.

## Options

- `--all-results`: Every result, oldest first, separated by a rule.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber ai metadata](transcriber-ai-metadata.md)
- [Output, JSON and exit codes](output.md)
