# transcriber keys set

Store a provider's key (read from stdin or prompted; never an argument).

## Synopsis

```
transcriber keys set [options] <provider>
```

## Description

Examples:

```
transcriber keys set openai                 (prompts, input hidden)
pbpaste | transcriber keys set gemini
transcriber keys set deepl < ~/.secrets/deepl
```

## Arguments

- `<provider>`: Provider: gemini, openai, anthropic, deepseek, magnific, deepl.

## Options

- `--test`: Test the key before storing it.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber keys](transcriber-keys.md)
- [Output, JSON and exit codes](output.md)
