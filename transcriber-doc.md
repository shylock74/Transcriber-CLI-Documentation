# transcriber doc

The document: new, source, segment, start timecode, contexts, settings, migrate.

## Synopsis

```
transcriber doc <command> [options]
```

## Commands

- [`new`](transcriber-doc-new.md): Create an empty document (optionally with its source media), without transcribing.
- [`source`](transcriber-doc-source.md): Show or change the source media (relink a moved file) and the source track title.
- [`segment`](transcriber-doc-segment.md): Show or set the In/Out segment to transcribe (licensed copies).
- [`tc-start`](transcriber-doc-tc-start.md): Show or override the start timecode used by exports (e.g. 01:00:00:00).
- [`contexts`](transcriber-doc-contexts.md): Show or choose the Global Contexts a document's AI correction uses.
- [`settings`](transcriber-doc-settings.md): A document's own settings: show, set, unset, apply, diff.
- [`migrate`](transcriber-doc-migrate.md): Rewrite a document in the current file format (older documents are read fine; this saves them upgraded).

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
