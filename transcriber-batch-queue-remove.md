# transcriber batch queue remove

Remove items from the queue: by number, or --done, --failed, --missing.

## Synopsis

```
transcriber batch queue remove [options] [<items>...]
```

## Description

Example:

```
transcriber batch queue remove 2..4 7
```

## Arguments

- `<items>...`: Items: 3 · 2..5 · 1,4 · all (numbers as in 'batch queue list'). Optional.

## Options

- `--done`: The finished items.
- `--failed`: The items that failed.
- `--missing`: The items whose media file is gone.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber batch queue](transcriber-batch-queue.md)
- [Output, JSON and exit codes](output.md)
