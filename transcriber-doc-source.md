# transcriber doc source

Show or change the source media (relink a moved file) and the source track title.

## Synopsis

```
transcriber doc source [options] <document> [<media>]
```

## Description

Example:

```
transcriber doc source talk.transcriber ~/Movies/talk-final.mov
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<media>`: New source media file. Optional.

## Options

- `--title <text>`: Title of the source track.
- `--clear`: Forget the source media.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber doc](transcriber-doc.md)
- [Output, JSON and exit codes](output.md)
