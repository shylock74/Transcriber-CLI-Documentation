# transcriber timeline

Text-based editing: timelines of sentences, marks, chapters, FCPXML export, AI selection.

## Synopsis

```
transcriber timeline <command> [options]
```

## Description

A timeline is an ordered list of sentences taken from the transcription. Mark the good ones, disable the rest, reorder, add chapters, then export an FCPXML edit for Final Cut Pro, or the text. The transcription itself is never changed here.

Typical session:

```
transcriber timeline new talk.transcriber --name "Cut 1"
transcriber timeline show talk.transcriber
transcriber timeline mark talk.transcriber --select 3..9,14
transcriber timeline from-marked talk.transcriber --name "Selects"
transcriber timeline export talk.transcriber --timeline Selects \
    -o selects.fcpxml
```

## Commands

- [`list`](transcriber-timeline-list.md): List the timelines: sentences, marked, chapters, duration.
- [`show`](transcriber-timeline-show.md): Show a timeline's sentences: number, state, timecodes, text.
- [`new`](transcriber-timeline-new.md): Create a timeline with every sentence of the transcription (or empty).
- [`from-marked`](transcriber-timeline-from-marked.md): Create a timeline from the marked sentences of another.
- [`rename`](transcriber-timeline-rename.md): Rename a timeline (and/or set its description).
- [`duplicate`](transcriber-timeline-duplicate.md): Duplicate a timeline ("<name> Copy", or --name).
- [`delete`](transcriber-timeline-delete.md): Delete timelines (asks first; --yes skips).
- [`select`](transcriber-timeline-select.md): Make a timeline the selected one (the default for the other commands and the app).
- [`mark`](transcriber-timeline-mark.md): Mark sentences (the selects: 'from-marked' and 'disable --unmarked' use them).
- [`unmark`](transcriber-timeline-unmark.md): Unmark sentences.
- [`enable`](transcriber-timeline-enable.md): Enable sentences or chapters (they are part of the edit).
- [`disable`](transcriber-timeline-disable.md): Disable sentences or chapters (left out of the edit, kept in the timeline).
- [`drop`](transcriber-timeline-drop.md): Remove sentences or chapters from a timeline (the transcription is untouched).
- [`sort`](transcriber-timeline-sort.md): Sort a timeline's sentences by time (chapters move with their first sentence's time).
- [`chapter`](transcriber-timeline-chapter.md): Chapters in a timeline: add, rename, remove (export as titles in the FCPXML).
- [`export`](transcriber-timeline-export.md): Export a timeline: FCPXML edit, text, text with timecodes, RTF, JSON or CSV.
- [`ai`](transcriber-timeline-ai.md): AI on a timeline: context, adherence rating, filtered and summarized cuts, chapters.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
