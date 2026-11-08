# transcriber batch queue run

Transcribe the waiting items of the queue now (here, not in the app).

## Synopsis

```
transcriber batch queue run [options] [<transcribe options>...]
```

## Description

Statuses are written back to the queue as items finish, so the app shows them. Failed items run again with --retry-failed.

Example: transcriber batch queue run -j 2 --continue-on-error

## Arguments

- `<transcribe options>...`: After '--': options for every 'transcribe' (e.g. -- -m large-v3-turbo --vad). Optional.

## Options

- `--retry-failed`: Run the failed items again too.
- `-j, --jobs <N>`: Files transcribed at the same time (each in its own process; every one loads the Whisper model). Default: `1`.
- `--continue-on-error`: Go on after a failed file (default: stop starting new ones).
- `--report <path>`: Write a JSON report of every file here.
- `--force`: Overwrite existing documents and outputs.
- `--skip-existing`: Skip files whose document already exists.
- `--dry-run`: Show the plan (what goes where); transcribe nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber batch queue](transcriber-batch-queue.md)
- [Output, JSON and exit codes](output.md)
