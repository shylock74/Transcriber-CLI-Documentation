# transcriber batch run

Transcribe files and folders now, N at a time, with a final report.

## Synopsis

```
transcriber batch run [options] <media|folder>...
```

## Description

Folders are searched recursively for audio and video. Every file becomes a document in the batch's session destination and, unless the format is 'project', an export in its output destination (both from the app's batch settings unless --sessions-dir/--outputs-dir). Options for every transcription go after '--'.

Exit status: 0 all done · 3 some failed or not run · 10 unlicensed (first 45 s) · the files' own code when every one failed the same way.

Examples:

```
transcriber batch run ~/Interviews --dry-run
transcriber batch run ~/Interviews -j 2 --format srt,txt \
    --outputs-dir ~/Subs
transcriber batch run *.mp4 --continue-on-error --report report.json -- \
    -m large-v3-turbo --vad
transcriber batch run talks/ --language it -- --ai-correct \
    --ai-provider anthropic
```

## Arguments

- `<media|folder>...`: Media files and folders; after '--', options for every 'transcribe' (e.g. -- -m large-v3-turbo --vad).

## Options

- `--format <formats>`: Exports: 'project' (document only) or formats, comma-separated (txt, timecoded, rtf, csv, srt, vtt, itt, ass, fcpxml, burnin, json). Default: the batch setting.
- `-l, --language <code>`: Spoken language (ISO code or 'auto'). Default: the batch setting.
- `--sessions-dir <dir>`: Folder for the documents (default: the batch setting).
- `--outputs-dir <dir>`: Folder for the exports (default: the batch setting).
- `--recursive`: Search folders recursively (default: yes).
- `--no-recursive`: Search folders recursively (default: yes).
- `-j, --jobs <N>`: Files transcribed at the same time (each in its own process; every one loads the Whisper model). Default: `1`.
- `--continue-on-error`: Go on after a failed file (default: stop starting new ones).
- `--report <path>`: Write a JSON report of every file here.
- `--force`: Overwrite existing documents and outputs.
- `--skip-existing`: Skip files whose document already exists.
- `--dry-run`: Show the plan (what goes where); transcribe nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber batch](transcriber-batch.md)
- [Output, JSON and exit codes](output.md)
