# transcriber contexts enrich

AI: add sounds-like variants (how speech recognition mishears them) to a YAML context.

## Synopsis

```
transcriber contexts enrich [options] <context>
```

## Description

Example:

```
transcriber contexts enrich "Product names" --dry-run
```

## Arguments

- `<context>`: YAML context: name, id or number.

## Options

- `--provider <provider>`: AI provider: gemini, openai, anthropic, deepseek, local (default: the app's).
- `--model <id>`: AI text model id (see 'transcriber ai models'; default: the provider's selected one).
- `--api-key-file <path>`: Read the provider's API key from this file ('-' = stdin).
- `--dry-run`: Print the enriched YAML, write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber contexts](transcriber-contexts.md)
- [Output, JSON and exit codes](output.md)
