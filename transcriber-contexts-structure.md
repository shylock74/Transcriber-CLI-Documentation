# transcriber contexts structure

AI: turn a free-text context (notes, Markdown, a list) into a YAML entity list.

## Synopsis

```
transcriber contexts structure [options] <context>
```

## Description

By default a new YAML context "<name> (YAML)" is created; --in-place replaces the content and the format of the context itself.

Example: transcriber contexts structure "Guest notes" --provider anthropic

## Arguments

- `<context>`: Context: name, id or number.

## Options

- `--provider <provider>`: AI provider: gemini, openai, anthropic, deepseek, local (default: the app's).
- `--model <id>`: AI text model id (see 'transcriber ai models'; default: the provider's selected one).
- `--api-key-file <path>`: Read the provider's API key from this file ('-' = stdin).
- `--in-place`: Replace the context itself.
- `--dry-run`: Print the YAML, write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber contexts](transcriber-contexts.md)
- [Output, JSON and exit codes](output.md)
