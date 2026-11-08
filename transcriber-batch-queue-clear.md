# transcriber batch queue clear

Empty the queue (asks first; --yes skips). --finished keeps the waiting items.

## Synopsis

```
transcriber batch queue clear [options]
```

## Options

- `--finished`: Remove only the done and failed items.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber batch queue](transcriber-batch-queue.md)
- [Output, JSON and exit codes](output.md)
