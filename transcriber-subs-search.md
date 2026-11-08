# transcriber subs search

Find text in the subtitles (plain text or regular expression).

## Synopsis

```
transcriber subs search [options] <document> <pattern>
```

## Description

Examples:

```
transcriber subs search talk.transcriber "machine learning" -i
transcriber subs search talk.transcriber '\bum+\b' --regex --all-tracks
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<pattern>`: Text to find.

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--regex`: The pattern is a regular expression.
- `-i, --ignore-case`: Ignore case.
- `--whole-word`: Match whole words only.
- `--all-tracks`: Search every track.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber subs](transcriber-subs.md)
- [Output, JSON and exit codes](output.md)
