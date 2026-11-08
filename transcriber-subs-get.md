# transcriber subs get

Show subtitles in full: text, timing, id, speaker, notes, AI state.

## Synopsis

```
transcriber subs get [options] <document> <selector>
```

## Description

Example:

```
transcriber subs get talk.transcriber 12 --json
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<selector>`: Subtitles: 12 · 3..7 · 3,5,9 · #<id> · @<time> · all

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--text-only`: Print only the text (one subtitle per paragraph).

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber subs](transcriber-subs.md)
- [Output, JSON and exit codes](output.md)
