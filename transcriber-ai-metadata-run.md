# transcriber ai metadata run

Run a document's prompts (by default only those without results).

## Synopsis

```
transcriber ai metadata run [options] <document> [<prompt>...]
```

## Description

Each run adds a result; the newest becomes the selected one. --again runs prompts that already have results too. Prompts can be added on the fly with --add.

Examples:

```
transcriber ai metadata run talk.transcriber
transcriber ai metadata run talk.transcriber Chapters --again \
    --provider openai
transcriber ai metadata run talk.transcriber --add Summary --print
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<prompt>...`: Prompts to run (default: every prompt without results). Optional.

## Options

- `--provider <provider>`: AI provider: gemini, openai, anthropic, deepseek, local (default: the app's).
- `--model <id>`: AI text model id (see 'transcriber ai models'; default: the provider's selected one).
- `--api-key-file <path>`: Read the provider's API key from this file ('-' = stdin).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--add <prompt>`: Add this library prompt first (repeatable). Repeatable.
- `--again`: Run prompts that already have results again.
- `--print`: Print the new results' text (human mode).

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber ai metadata](transcriber-ai-metadata.md)
- [Output, JSON and exit codes](output.md)
