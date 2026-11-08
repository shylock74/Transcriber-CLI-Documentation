# transcriber tracks add

Add an empty track, or one with the source's timing and empty or copied text.

## Synopsis

```
transcriber tracks add [options] <document> <language>
```

## Description

To translate with DeepL use 'transcriber translate'; to import an SRT as a track use 'transcriber import file.srt --into doc --as-track it'.

Examples:

```
transcriber tracks add talk.transcriber it --copy-text
transcriber tracks add talk.transcriber de --title "German (client)"
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<language>`: Language code of the new track (e.g. it, fr, en-US).

## Options

- `--title <title>`: Title (default: the language).
- `--copy-text`: Start from a copy of the source subtitles.
- `--show`: Make it the track shown in the app.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber tracks](transcriber-tracks.md)
- [Output, JSON and exit codes](output.md)
