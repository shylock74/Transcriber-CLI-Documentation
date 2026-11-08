# transcriber probe

Media file information: duration, frame rate, size, audio, codecs, timecode.

## Synopsis

```
transcriber probe [options] <media>...
```

## Description

Also tells whether Transcriber accepts the file.

Examples:

```
transcriber probe interview.mov
transcriber probe *.wav --json
```

## Arguments

- `<media>...`: Media files.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
