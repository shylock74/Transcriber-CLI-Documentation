# transcriber info

Show what a document holds: source media, tracks, subtitles, speakers, settings.

## Synopsis

```
transcriber info [options] <document>
```

## Description

Examples:

```
transcriber info interview.transcriber
transcriber info interview.transcriber --json | jq '.result.tracks'
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
