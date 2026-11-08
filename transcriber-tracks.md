# transcriber tracks

List, add, duplicate, rename and remove tracks (translations).

## Synopsis

```
transcriber tracks <command> [options]
```

## Description

A document has one source track (the transcription) and any number of translation tracks. Name a track by language code, title, id, or its number in 'tracks list'.

## Commands

- [`list`](transcriber-tracks-list.md): List the tracks with their subtitle counts.
- [`add`](transcriber-tracks-add.md): Add an empty track, or one with the source's timing and empty or copied text.
- [`duplicate`](transcriber-tracks-duplicate.md): Copy a track (source or translation) to a new translation track.
- [`rename`](transcriber-tracks-rename.md): Change the language code or title of a track ('source' renames the source title).
- [`remove`](transcriber-tracks-remove.md): Delete a translation track (asks first; --yes skips).
- [`fixed-text`](transcriber-tracks-fixed-text.md): Show, set or clear the fixed (reference) text of a translation track.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
