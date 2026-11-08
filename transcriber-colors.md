# transcriber colors

Word Colors: the palette, automatic rules and manual marks on words.

## Synopsis

```
transcriber colors <command> [options]
```

## Description

Colored words appear in FCPXML titles, burn-in, ASS, and in SRT/VTT exported with --word-colors. Rules color every occurrence of a word or phrase; marks color one occurrence of a word in one subtitle (and win over rules).

## Commands

- [`palette`](transcriber-colors-palette.md): List and edit the palette.
- [`rules`](transcriber-colors-rules.md): Automatic rules: a word or phrase always gets a color.
- [`marks`](transcriber-colors-marks.md): Manual marks: one word of one subtitle gets a color (documents only).

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
