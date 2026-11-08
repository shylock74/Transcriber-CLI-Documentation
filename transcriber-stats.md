# transcriber stats

Statistics of a track: subtitles, words, reading speed, speakers.

## Synopsis

```
transcriber stats [options] <document>
```

## Description

The same numbers as the app's dashboard, for one track or all of them.

Examples:

```
transcriber stats talk.transcriber
transcriber stats talk.transcriber --all-tracks --json
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--all-tracks`: Every track.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
