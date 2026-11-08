# transcriber contexts

The Global Contexts library: terms, names and facts the AI correction knows.

## Synopsis

```
transcriber contexts <command> [options]
```

## Description

Contexts are shared with the app. A document uses its own selection ('doc contexts') or, when it has none, every context enabled here. YAML contexts list entities (canonical spelling, category, description, sounds_like variants) and are the most effective; Markdown, JSON and text are passed as they are.

## Commands

- [`list`](transcriber-contexts-list.md): List the contexts: number, format, language, tokens, enabled.
- [`show`](transcriber-contexts-show.md): Print a context's content on stdout (--info for its details instead).
- [`create`](transcriber-contexts-create.md): Create a context, empty or from a file / stdin.
- [`import`](transcriber-contexts-import.md): Import files as new contexts (name from the file name).
- [`export`](transcriber-contexts-export.md): Write a context's content to a file (default: <name>.<format>).
- [`set-content`](transcriber-contexts-set-content.md): Replace a context's content with a file or stdin.
- [`add-entity`](transcriber-contexts-add-entity.md): Add an entity to a YAML context (or more sounds-like variants to an existing one).
- [`rename`](transcriber-contexts-rename.md): Rename a context.
- [`duplicate`](transcriber-contexts-duplicate.md): Duplicate a context ("<name> Copy", or --name).
- [`delete`](transcriber-contexts-delete.md): Delete contexts (their files go to the Trash; asks first, --yes skips).
- [`enable`](transcriber-contexts-enable.md): Enable contexts by default for new documents.
- [`disable`](transcriber-contexts-disable.md): Disable contexts by default for new documents.
- [`language`](transcriber-contexts-language.md): Set a context's reference language (BCP-47 such as it-IT, or 'auto').
- [`convert`](transcriber-contexts-convert.md): Change a context's declared format (the content is kept as it is).
- [`tokens`](transcriber-contexts-tokens.md): Estimated tokens of contexts, against the AI model's budget.
- [`validate`](transcriber-contexts-validate.md): Check that YAML contexts parse and list entities.
- [`structure`](transcriber-contexts-structure.md): AI: turn a free-text context (notes, Markdown, a list) into a YAML entity list.
- [`enrich`](transcriber-contexts-enrich.md): AI: add sounds-like variants (how speech recognition mishears them) to a YAML context.
- [`extract`](transcriber-contexts-extract.md): AI: extract the names and terms spoken in a document into a YAML context.
- [`path`](transcriber-contexts-path.md): Print the folder of the Global Contexts library.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
