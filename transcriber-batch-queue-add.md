# transcriber batch queue add

Add media files and folders to the queue.

## Synopsis

```
transcriber batch queue add [options] <media|folder>...
```

## Description

Example:

```
transcriber batch queue add ~/Interviews/*.mp4 ~/Talks
```

## Arguments

- `<media|folder>...`: Media files and folders.

## Options

- `--recursive`: Search folders recursively (default: yes).
- `--no-recursive`: Search folders recursively (default: yes).
- `--allow-duplicates`: Add a file even if it is already waiting in the queue.
- `--dry-run`: Show what would be added.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber batch queue](transcriber-batch-queue.md)
- [Output, JSON and exit codes](output.md)
