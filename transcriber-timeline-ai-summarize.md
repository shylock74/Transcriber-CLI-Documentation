# transcriber timeline ai summarize

AI: new timeline of the sentences that best tell the timeline context.

## Synopsis

```
transcriber timeline ai summarize [options] <document>
```

## Description

The context is generated first when missing.

Example:

```
transcriber timeline ai summarize talk.transcriber --timeline "A2C Filtered"
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
- `--name <name>`: Name (default: "A2C Remastered").

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber timeline ai](transcriber-timeline-ai.md)
- [Output, JSON and exit codes](output.md)
