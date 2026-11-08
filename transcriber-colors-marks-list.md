# transcriber colors marks list

Show the colored words (marks and rules) of a track.

## Synopsis

```
transcriber colors marks list [options] <document>
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--marks-only`: Only manual marks, not words colored by rules.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber colors marks](transcriber-colors-marks.md)
- [Output, JSON and exit codes](output.md)
