# transcriber ai punctuate

Add strong punctuation (full stops) to long run-on sentences of the source track.

## Synopsis

```
transcriber ai punctuate [options] <document>
```

## Description

Sentences longer than --longer-than characters are sent to the AI, which splits them with full stops. Changed subtitles can be reviewed with 'ai diff'.

Example: transcriber ai punctuate talk.transcriber --longer-than 160

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--provider <provider>`: AI provider: gemini, openai, anthropic, deepseek, local (default: the app's).
- `--model <id>`: AI text model id (see 'transcriber ai models'; default: the provider's selected one).
- `--api-key-file <path>`: Read the provider's API key from this file ('-' = stdin).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--longer-than <N>`: Sentence length threshold, characters. Default: `200`.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber ai](transcriber-ai.md)
- [Output, JSON and exit codes](output.md)
