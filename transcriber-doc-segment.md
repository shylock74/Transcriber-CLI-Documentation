# transcriber doc segment

Show or set the In/Out segment to transcribe (licensed copies).

## Synopsis

```
transcriber doc segment [options] <document>
```

## Description

Times are seconds or timecodes from the start of the file. Examples: transcriber doc segment talk.transcriber --in 1:30 --out 12:00 · transcriber doc segment talk.transcriber --clear

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--in <time>`: In point.
- `--out <time>`: Out point.
- `--clear`: Remove the segment (transcribe the whole file).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber doc](transcriber-doc.md)
- [Output, JSON and exit codes](output.md)
