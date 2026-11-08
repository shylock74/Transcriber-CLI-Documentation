# transcriber keys test

Check keys with a tiny request to the provider (costs a few tokens).

## Synopsis

```
transcriber keys test [options] [<provider>]
```

## Description

Without a provider, tests every provider that has a key.

Examples:

```
transcriber keys test
OPENAI_API_KEY=sk-… transcriber keys test openai
```

## Arguments

- `<provider>`: Provider (default: every configured one). Optional.

## Options

- `--api-key-file <path>`: Test the key in this file ('-' = stdin).

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber keys](transcriber-keys.md)
- [Output, JSON and exit codes](output.md)
