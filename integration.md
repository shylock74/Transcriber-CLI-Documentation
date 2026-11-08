# Working with the app

The command and the app are two views of the same data.

- `transcriber open talk.transcriber` opens a document in the app. A media file becomes a new document with that media as its source; several media files ask whether to batch or concatenate them. `--reveal` shows files in the Finder, `--background` does not bring the app to the front.
- `export --open` and `--reveal` open or show the exported files; `export --send-to-fcp` and `timeline export --send-to-fcp` hand FCPXML to Final Cut Pro.
- A document open in the app cannot be written by the command without `--force` (exit `11`).
- Changes to settings, presets, dictionaries, Global Contexts and the batch queue made by the command show up in a running app.
- `batch queue add` fills the app's Batch window queue; `batch queue run` processes it from the command line.

## Scripting examples

Transcribe a folder, keep going past failures and collect a report:

```
transcriber batch run ~/Interviews -j 2 --format srt,txt --continue-on-error --report report.json
```

Fix a typo everywhere and export, failing loudly:

```
set -e
transcriber subs replace talk.transcriber "Jon" "John" --whole-word --yes
transcriber export talk.transcriber -f srt -o talk.srt
```

Use the JSON output with `jq`:

```
transcriber info talk.transcriber --json | jq '.result'
```