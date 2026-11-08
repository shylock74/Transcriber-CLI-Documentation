# transcriber ai metadata

AI metadata: run library prompts (summaries, titles, chapters…) on a document.

## Synopsis

```
transcriber ai metadata <command> [options]
```

## Description

A document holds a list of prompts and their results. Add prompts (or a whole set), run them, then print or export the results. Prompts and sets are edited in the app.

Examples:

```
transcriber ai metadata prompts
transcriber ai metadata add talk.transcriber "YouTube description" \
    "Chapters"
transcriber ai metadata run talk.transcriber
transcriber ai metadata show talk.transcriber "Chapters" > chapters.txt
```

## Commands

- [`prompts`](transcriber-ai-metadata-prompts.md): List the prompts of the library (shared with the app).
- [`sets`](transcriber-ai-metadata-sets.md): List the prompt sets of the library and their prompts.
- [`list`](transcriber-ai-metadata-list.md): List a document's prompts, their state and a preview of the results.
- [`add`](transcriber-ai-metadata-add.md): Add library prompts (or a set) to a document.
- [`remove`](transcriber-ai-metadata-remove.md): Remove prompts (and their results) from a document.
- [`run`](transcriber-ai-metadata-run.md): Run a document's prompts (by default only those without results).
- [`show`](transcriber-ai-metadata-show.md): Print a prompt's result text on stdout (the selected one, or every one).
- [`export`](transcriber-ai-metadata-export.md): Export every result of a document to Markdown, text or JSON.
- [`clear`](transcriber-ai-metadata-clear.md): Delete the results of prompts, keeping the prompts (asks first).

## See also

- [transcriber ai](transcriber-ai.md)
- [Output, JSON and exit codes](output.md)
