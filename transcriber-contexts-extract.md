# transcriber contexts extract

AI: extract the names and terms spoken in a document into a YAML context.

## Synopsis

```
transcriber contexts extract [options] <document>
```

## Description

Entities are merged into --into (a YAML context), or a new context named --new (default "<document title> entities"). --dry-run lists them only.

Examples:

```
transcriber contexts extract talk.transcriber --dry-run
transcriber contexts extract talk.transcriber --into "Guests"
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--provider <provider>`: AI provider: gemini, openai, anthropic, deepseek, local (default: the app's).
- `--model <id>`: AI text model id (see 'transcriber ai models'; default: the provider's selected one).
- `--api-key-file <path>`: Read the provider's API key from this file ('-' = stdin).
- `--into <context>`: Merge into this YAML context.
- `--new <name>`: Name of the new context.
- `--dry-run`: List the entities, write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber contexts](transcriber-contexts.md)
- [Output, JSON and exit codes](output.md)
