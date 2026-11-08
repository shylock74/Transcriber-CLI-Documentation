# transcriber tracks remove

Delete a translation track (asks first; --yes skips).

## Synopsis

```
transcriber tracks remove [options] <document> <track>
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.
- `<track>`: Track (not 'source').

## Options

- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber tracks](transcriber-tracks.md)
- [Output, JSON and exit codes](output.md)
