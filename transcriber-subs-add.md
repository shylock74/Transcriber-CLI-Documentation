# transcriber subs add

Add a subtitle (placed in time order).

## Synopsis

```
transcriber subs add [options] <document>
```

## Description

Example:

```
transcriber subs add talk.transcriber --in 1:02.5 --out 1:05 \
    --text "[Applause]"
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--in <time>`: Start time.
- `--out <time>`: End time, or '+duration'.
- `--text <text>`: Text ('\n' for a line break).
- `--speaker <name>`: Speaker.
- `--disabled`: Add it disabled.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber subs](transcriber-subs.md)
- [Output, JSON and exit codes](output.md)
