# transcriber subs set

Change the text, timing, speaker, notes or state of subtitles.

## Synopsis

```
transcriber subs set [options] <document> <selector>
```

## Description

--text, --in, --out need a single subtitle; --speaker, --notes, --enable, --disable and --clear-ai apply to every selected one.

Examples:

```
transcriber subs set talk.transcriber 12 --text "Hello, world."
transcriber subs set talk.transcriber 12 --in 00:01:02.500 --out +2.5
transcriber subs set talk.transcriber 3..9 --speaker Anna
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<selector>`: Subtitles: 12 · 3..7 · 3,5,9 · #<id> · @<time> · all

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--text <text>`: New text ('\n' for a line break; '-' reads stdin).
- `--in <time>`: New start time.
- `--out <time>`: New end time; '+2.5' = start + 2.5 s.
- `--speaker <name>`: Speaker ('' clears it).
- `--notes <text>`: Notes ('' clears them).
- `--enable`: Enable the subtitles.
- `--disable`: Disable the subtitles (kept, but not exported).
- `--clear-ai`: Accept the AI change (forget the previous text).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber subs](transcriber-subs.md)
- [Output, JSON and exit codes](output.md)
