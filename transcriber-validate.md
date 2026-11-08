# transcriber validate

Check subtitles against the SRT rules: length, lines, duration, overlaps, reading speed.

## Synopsis

```
transcriber validate [options] <document>
```

## Description

Limits come from the document's SRT settings unless overridden. Issues are listed with their subtitle; --strict exits with code 65 when any error is found (CI use).

Checks: line length and line count, minimum duration, overlaps, reading speed (cps), empty text, subtitles past the end of the media, missing media file.

Examples:

```
transcriber validate talk.transcriber
transcriber validate talk.transcriber --track fr --max-cps 17 --strict
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--all-tracks`: Every track.
- `--max-chars <N>`: Characters per line (default: SRT settings).
- `--max-lines <N>`: Lines per subtitle (default: SRT settings).
- `--min-duration <s>`: Shortest subtitle, seconds (default: SRT settings).
- `--max-cps <cps>`: Highest reading speed, characters per second (default 20; 0 = off). Default: `20.0`.
- `--strict`: Exit with code 65 when errors are found.
- `--errors-only`: Hide warnings.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
