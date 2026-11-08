# transcriber text

Print the transcription as flowing text (optionally with timecodes).

## Synopsis

```
transcriber text [options] <document>
```

## Description

Examples:

```
transcriber text talk.transcriber | wc -w
transcriber text talk.transcriber --track fr --timecodes -o talk_fr.txt
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--timecodes`: Paragraphs with their timecode.
- `--double`: With --timecodes: in and out times.
- `--speakers`: Prefix speakers' names (default: the document's setting).
- `--no-speakers`: Prefix speakers' names (default: the document's setting).
- `--include-disabled`: Include disabled subtitles.
- `-o, --output <path>`: Write to this file instead of stdout.
- `--force`: Overwrite the output file.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
