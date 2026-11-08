# transcriber colors marks set

Color a word in subtitles ('none' removes a rule's color there).

## Synopsis

```
transcriber colors marks set [options] <document> <selector>
```

## Description

Examples:

```
transcriber colors marks set talk.transcriber 12 --word Transcriber \
    --color Yellow
transcriber colors marks set talk.transcriber all --word "AI" \
    --color none --every
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<selector>`: Subtitles: 12 · 3..7 · 3,5,9 · #<id> · @<time> · all

## Options

- `--word <word>`: The word (letters/digits, any case).
- `--color <color>`: Palette color (name, number, id) or 'none'.
- `--occurrence <N>`: Which occurrence in each subtitle (1 = first). Default: `1`.
- `--every`: Every occurrence in each subtitle.
- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber colors marks](transcriber-colors-marks.md)
- [Output, JSON and exit codes](output.md)
