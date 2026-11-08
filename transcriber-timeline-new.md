# transcriber timeline new

Create a timeline with every sentence of the transcription (or empty).

## Synopsis

```
transcriber timeline new [options] <document>
```

## Description

Sentences are cut at strong punctuation (. ! ? …). The new timeline is selected unless --no-select.

Examples:

```
transcriber timeline new talk.transcriber
transcriber timeline new talk.transcriber --name "Short cut" \
    --enabled-subtitles-only
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--name <name>`: Name (default: "Transcribed Source").
- `--description <text>`: Description.
- `--empty`: An empty timeline.
- `--enabled-subtitles-only`: Leave out the disabled subtitles of the transcription.
- `--no-select`: Do not select the new timeline.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber timeline](transcriber-timeline.md)
- [Output, JSON and exit codes](output.md)
