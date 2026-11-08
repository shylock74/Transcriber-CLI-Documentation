# transcriber subs

List, search and edit the subtitles of a document.

## Synopsis

```
transcriber subs <command> [options]
```

## Description

Subtitles are chosen with a selector:

```
Subtitles: 12 · 3..7 · 3,5,9 · #<id> · @<time> · all
```

Indices are 1-based and refer to the track's order (see 'subs list'). Every editing command accepts -o, --dry-run, --backup and --force.

## Commands

- [`list`](transcriber-subs-list.md): List the subtitles of a track (with filters).
- [`get`](transcriber-subs-get.md): Show subtitles in full: text, timing, id, speaker, notes, AI state.
- [`search`](transcriber-subs-search.md): Find text in the subtitles (plain text or regular expression).
- [`set`](transcriber-subs-set.md): Change the text, timing, speaker, notes or state of subtitles.
- [`add`](transcriber-subs-add.md): Add a subtitle (placed in time order).
- [`delete`](transcriber-subs-delete.md): Delete subtitles.
- [`enable`](transcriber-subs-enable.md): Enable subtitles (they are exported again).
- [`disable`](transcriber-subs-disable.md): Disable subtitles (kept in the document, left out of exports).
- [`split`](transcriber-subs-split.md): Split subtitles at line breaks, at given strings, or at the soft separators.
- [`merge`](transcriber-subs-merge.md): Merge subtitles: a range into one, or one subtitle with the next.
- [`split-soft`](transcriber-subs-split-soft.md): Split every subtitle at the soft separators (commas, etc.) and sentence ends.
- [`join-soft`](transcriber-subs-join-soft.md): Join subtitles that end with a soft separator to the next one.
- [`split-long`](transcriber-subs-split-long.md): Split subtitles that do not fit in max lines × max characters per line.
- [`split-newlines`](transcriber-subs-split-newlines.md): Make one subtitle of each line of multi-line subtitles.
- [`join-newlines`](transcriber-subs-join-newlines.md): Replace line breaks inside subtitles with spaces.
- [`compact`](transcriber-subs-compact.md): Merge short neighbours while the result fits a length (never across sentence ends).
- [`shift`](transcriber-subs-shift.md): Move subtitles in time.
- [`replace`](transcriber-subs-replace.md): Find and replace text (plain or regular expression, with $1 groups).

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
