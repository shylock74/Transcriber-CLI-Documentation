# transcriber import

Import SRT or WebVTT subtitles into a new or existing document.

## Synopsis

```
transcriber import [options] <subtitles>
```

## Description

Without --into, a new document is created (-o, default <subtitles>.transcriber). With --into, the subtitles become a new track (--as-track <language>) or replace the source transcription (--replace-source). Unlicensed copies import 15 subtitles.

Examples:

```
transcriber import talk.srt --media talk.mp4
transcriber import talk_fr.vtt --into talk.transcriber --as-track fr
transcriber import fixed.srt --into talk.transcriber --replace-source \
    --backup
```

## Arguments

- `<subtitles>`: SRT or VTT file ('-' = stdin, SRT or VTT detected).

## Options

- `--into <doc>`: Add to this document instead of creating one.
- `--as-track <language>`: With --into: add as a track with this language/title.
- `--replace-source`: With --into: replace the source transcription.
- `--media <media>`: Media file of the new document (or the new source, with --into).
- `--language <code>`: New document: the source language code stored in the settings.
- `--no-colors`: Ignore color tags (no Word Colors).
- `--offset <time>`: Shift every timing by this amount (e.g. -1.5, 00:00:02).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
