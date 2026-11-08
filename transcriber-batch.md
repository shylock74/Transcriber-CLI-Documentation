# transcriber batch

Transcribe many files: now (run, N at a time) or through the app's batch queue.

## Synopsis

```
transcriber batch <command> [options]
```

## Description

Destinations, name prefix/suffix, output format and language come from the app's batch settings ('transcriber settings get batchSettings'); the flags override them.

## Commands

- [`run`](transcriber-batch-run.md): Transcribe files and folders now, N at a time, with a final report.
- [`queue`](transcriber-batch-queue.md): The app's batch queue (Batch window): list, add, remove, clear, run.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
