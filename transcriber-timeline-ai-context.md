# transcriber timeline ai context

Generate (AI), show or set a timeline's context: what it is about.

## Synopsis

```
transcriber timeline ai context [options] <document>
```

## Description

Examples:

```
transcriber timeline ai context talk.transcriber
transcriber timeline ai context talk.transcriber --show
transcriber timeline ai context talk.transcriber \
    --text "A product launch: price, features, availability"
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--timeline <timeline>`: Timeline: name, id or number (default: the selected one).
- `--provider <provider>`: AI provider: gemini, openai, anthropic, deepseek, local (default: the app's).
- `--model <id>`: AI text model id (see 'transcriber ai models'; default: the provider's selected one).
- `--api-key-file <path>`: Read the provider's API key from this file ('-' = stdin).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--show`: Print the stored context, change nothing.
- `--text <text>`: Store this context ('-' = stdin) instead of asking the AI.
- `--clear`: Remove the stored context.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber timeline ai](transcriber-timeline-ai.md)
- [Output, JSON and exit codes](output.md)
