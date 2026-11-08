# transcriber export

Export a document to subtitles, text, FCPXML or a burned-in video.

## Synopsis

```
transcriber export [options] <document>
```

## Description

Formats:

```
txt, timecoded, rtf, csv, srt, vtt, itt, ass, fcpxml, burnin, json
```

Files are named after the document (<name>[_<track>].<ext>), beside it or in --output-dir. -o names the file for one format and one track ('-' = stdout). The document's export settings apply; the options below override them for this run.

Examples:

```
transcriber export talk.transcriber --format srt
transcriber export talk.transcriber -f srt,vtt,txt --all-tracks \
    --output-dir out/
transcriber export talk.transcriber -f vtt --track fr -o - | head
transcriber export talk.transcriber -f fcpxml --send-to-fcp
transcriber export talk.transcriber -f burnin --video-codec h265 \
    -o talk_sub.mp4
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-f, --format <formats>`: Formats, comma-separated (default: srt). Default: `srt`.
- `-t, --track <track>`: Track: source (default), a translation's language/title/id. Repeatable. Repeatable.
- `--all-tracks`: Export the source and every translation.
- `-o, --output <path>`: Output file (one format and track; '-' = stdout).
- `--output-dir <dir>`: Folder for the files (default: beside the document).
- `--force`: Overwrite existing files.
- `--send-to-fcp`: fcpxml: send the titles straight to Final Cut Pro instead of writing a file.
- `--reveal`: Reveal the exported files in the Finder.
- `--open`: Open the exported files with their default app.
- `--word-colors`: SRT/VTT: write Word Colors as color tags.
- `--no-word-colors`: SRT/VTT: write Word Colors as color tags.
- `--uppercase`: SRT/VTT/FCPXML/burn-in: subtitles in upper case.
- `--no-uppercase`: SRT/VTT/FCPXML/burn-in: subtitles in upper case.
- `--max-chars <N>`: SRT/VTT/FCPXML: characters per line.
- `--max-lines <N>`: SRT/VTT/FCPXML: lines per subtitle.
- `--source-timecode`: Keep the media's start timecode in the timings.
- `--no-source-timecode`: Keep the media's start timecode in the timings.
- `--double-timecodes`: timecoded: write the out time too.
- `--rtf-timecodes`: RTF: include the timecodes.
- `--no-rtf-timecodes`: RTF: include the timecodes.
- `--video-codec <codec>`: burnin: video codec (h264, h265, prores422, prores4444, webm…).
- `--video-bitrate <kbps>`: burnin: video bitrate, kbit/s.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
