# transcriber dictionaries

Search-and-replace dictionaries: list, edit, import/export, use in documents.

## Synopsis

```
transcriber dictionaries <command> [options]
```

## Description

Dictionaries are shared with the app. Each has items (texts to find → replacement) and an optional prompt (words Whisper should expect). A document uses the dictionaries in its settings (dictionaries.enable, dictionaries.dictionaryIdList) after transcription.

## Commands

- [`list`](transcriber-dictionaries-list.md): List the dictionaries.
- [`show`](transcriber-dictionaries-show.md): Show a dictionary's items and prompt.
- [`create`](transcriber-dictionaries-create.md): Create a dictionary.
- [`edit`](transcriber-dictionaries-edit.md): Change a dictionary's description, prompt or favorite flag.
- [`rename`](transcriber-dictionaries-rename.md): Rename a dictionary.
- [`delete`](transcriber-dictionaries-delete.md): Delete a dictionary (asks first; --yes skips).
- [`import`](transcriber-dictionaries-import.md): Import a dictionary file (.TrDict, as exported by the app or 'dictionaries export').
- [`export`](transcriber-dictionaries-export.md): Write a dictionary to a .TrDict file (JSON; the app can import it).
- [`add-item`](transcriber-dictionaries-add-item.md): Add a replacement: texts to find → replacement.
- [`remove-item`](transcriber-dictionaries-remove-item.md): Remove an item (by number or id; see 'dictionaries show').
- [`use`](transcriber-dictionaries-use.md): Make a document apply dictionaries after transcription (and send their prompts to Whisper).
- [`unuse`](transcriber-dictionaries-unuse.md): Stop a document from using dictionaries ('all' = every one).
- [`apply`](transcriber-dictionaries-apply.md): Run dictionaries' replacements on a document's subtitles now.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
