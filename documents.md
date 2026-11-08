# Documents, tracks and selectors

## Documents

Most commands take a `.transcriber` document. `transcribe` creates one from a media file (next to the media, or where `--output` says). `doc new` creates an empty one.

Commands that change a document share these options:

- `-o, --output <path>`: write the result there instead of changing the document in place.
- `--dry-run`: show what would change and write nothing.
- `--backup`: keep the previous file as `<name>.transcriber.bak` before overwriting.
- `--force`: write even if the document is open in the Transcriber app, or overwrite an existing output.

A document that is **open in the app** is protected: the app would overwrite the change at its next save, so commands that write it stop with exit code `11` unless `--force` is given. Reading is always allowed. The app tells the command which documents it has open; a crashed app leaves nothing behind that counts.

A document saved by a newer version of Transcriber than the command is read-only for the command (exit `65` if you try to write it) rather than damaged.

## Tracks

A document has one or more subtitle tracks: the original transcription and each translation. `--track <name>` picks one by language code or title. Commands default to the first track; `export --all-tracks` writes every one.

## Selectors

Commands that work on some subtitles take a selector:

- `12`: the 12th subtitle (1-based; `-1` is the last).
- `3..7` or `3-7`: an inclusive range. Ends can be left open: `..5`, `10..`.
- `3,5,9`: a list of any of these.
- `#1001`: the subtitle with that id (ids survive edits; indices do not).
- `@00:01:02.5`: the subtitle on screen at that time (or the next one).
- `all`: every subtitle.

## Times

Times are accepted as `HH:MM:SS.mmm`, `HH:MM:SS,mmm`, `MM:SS.s`, plain seconds (`62.5`), `1h2m3.5s`, `90s`, `250ms`, and `HH:MM:SS:FF` when the frame rate is known (`--fps`, or the document's). A leading `-` or `+` gives an offset: write `subs shift doc.transcriber -- -1.5` to move subtitles 1.5 seconds earlier (the `--` stops option parsing).

## Stdin and stdout

Where a path is expected, `-` means standard input or output: `export doc.transcriber -f srt -o -` prints the SRT, `align doc.transcriber --text - < script.txt` reads the script.