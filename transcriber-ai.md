# transcriber ai

AI correction, punctuation, review of AI edits, questions and metadata.

## Synopsis

```
transcriber ai <command> [options]
```

## Description

The provider and model are the app's (Settings ▸ AI); override them with --provider/--model, or for every command with --set aIMetadata.configuration…

## Commands

- [`correct`](transcriber-ai-correct.md): Semantic correction: fix misheard words using the text and the global contexts.
- [`punctuate`](transcriber-ai-punctuate.md): Add strong punctuation (full stops) to long run-on sentences of the source track.
- [`diff`](transcriber-ai-diff.md): Show the subtitles changed by the AI: previous text and new text.
- [`review`](transcriber-ai-review.md): Review the AI changes one by one: accept, reject or edit each (interactive).
- [`accept`](transcriber-ai-accept.md): Accept AI changes: keep the new text and forget the previous one.
- [`reject`](transcriber-ai-reject.md): Reject AI changes: restore the previous text.
- [`ask`](transcriber-ai-ask.md): Ask the AI a question about the transcript; the answer goes to stdout.
- [`metadata`](transcriber-ai-metadata.md): AI metadata: run library prompts (summaries, titles, chapters…) on a document.
- [`providers`](transcriber-ai-providers.md): List the AI providers, the selected one, and where each key comes from.
- [`models`](transcriber-ai-models.md): List the text models of a provider (ids for --model).

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
