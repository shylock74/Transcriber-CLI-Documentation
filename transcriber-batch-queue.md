# transcriber batch queue

The app's batch queue (Batch window): list, add, remove, clear, run.

## Synopsis

```
transcriber batch queue <command> [options]
```

## Description

The queue is shared with the app: changes made here show in its Batch window. TRANSCRIBER_BATCH_QUEUE=<file> uses another queue file instead. Items use the queue's settings (copied from the batch settings when the queue was created) unless they have their own.

## Commands

- [`list`](transcriber-batch-queue-list.md): List the queue: status, media, duration, destinations.
- [`add`](transcriber-batch-queue-add.md): Add media files and folders to the queue.
- [`remove`](transcriber-batch-queue-remove.md): Remove items from the queue: by number, or --done, --failed, --missing.
- [`clear`](transcriber-batch-queue-clear.md): Empty the queue (asks first; --yes skips). --finished keeps the waiting items.
- [`run`](transcriber-batch-queue-run.md): Transcribe the waiting items of the queue now (here, not in the app).
- [`path`](transcriber-batch-queue-path.md): Print where the queue is stored.

## See also

- [transcriber batch](transcriber-batch.md)
- [Output, JSON and exit codes](output.md)
