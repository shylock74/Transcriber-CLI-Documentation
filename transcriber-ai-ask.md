# transcriber ai ask

Ask the AI a question about the transcript; the answer goes to stdout.

## Synopsis

```
transcriber ai ask [options] <document> <question>
```

## Description

The document is not changed. --timecodes sends the text with its timecodes (for questions like "when do they talk about pricing?").

Examples:

```
transcriber ai ask talk.transcriber "Summarise this in five bullet points"
transcriber ai ask talk.transcriber \
    --timecodes "List the chapters with their start times"
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<question>`: The question or instruction ('-' = read it from stdin).

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--provider <provider>`: AI provider: gemini, openai, anthropic, deepseek, local (default: the app's).
- `--model <id>`: AI text model id (see 'transcriber ai models'; default: the provider's selected one).
- `--api-key-file <path>`: Read the provider's API key from this file ('-' = stdin).
- `--timecodes`: Send the text with timecodes.
- `--max-tokens <N>`: Longest answer, tokens. Default: `8192`.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber ai](transcriber-ai.md)
- [Output, JSON and exit codes](output.md)
