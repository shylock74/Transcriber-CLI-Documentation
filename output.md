# Output, JSON and exit codes

## Streams

Results go to **stdout**, everything else (progress, warnings, hints, prompts, logs) to **stderr**, so pipes carry only data. Colours are used only on a terminal and are turned off by `--no-color`, by the `NO_COLOR` environment variable and by `TERM=dumb`.

- `-q, --quiet`: only results and errors.
- `-v, --verbose`: details of what is being done.
- `--log-file <path>`: append a log of the run to a file.

## JSON

With `--json` a command prints exactly one JSON object on stdout:

```
{
  "schema": "transcriber.cli/1",
  "command": "subs list",
  "ok": true,
  "result": { … },
  "warnings": [ … ],
  "error": null
}
```

On failure `ok` is false, `result` is null and `error` has `code` (the exit code), `kind`, `message` and, when there is one, `hint`. The `result` of each command is documented by trying it: `transcriber subs list doc.transcriber --json`.

Some commands print data before the envelope (for example `text` prints the text); with `--json` the envelope is always the last object.

## Progress

`--progress auto|bar|ndjson|none` controls progress on stderr. `auto` (default) draws a bar on a terminal and prints nothing otherwise. `ndjson` prints one JSON object per line:

```
{"event":"progress","phase":"transcribing","fraction":0.42,"message":"…","item":1,"items":3}
```

`phase` names the step (loading, transcribing, aligning, translating…), `fraction` runs from 0 to 1 when known, `item` and `items` count the files of a batch.

## Confirmations

Commands that delete or replace something ask first on a terminal. `-y, --yes` answers yes; `--no-input` (or `TRANSCRIBER_NO_INPUT` in the environment) never prompts and fails with exit code `64` when an answer would be needed. Without a terminal the command behaves as with `--no-input`.

## Exit codes

- `0` (success): Success.
- `1` (failure): Generic failure.
- `3` (partialFailure): Partial failure: some items of a batch failed.
- `10` (licenseLimited): Completed, but limited by the missing licence (first 45 seconds only).
- `11` (documentOpenInApp): The document is open in Transcriber; use --force to write it anyway.
- `12` (providerError): AI or translation provider error.
- `13` (missingAPIKey): Missing API key for the selected provider.
- `14` (modelMissing): The Whisper model is not installed (transcriber models download).
- `64` (usage): Usage error: bad command, option or argument.
- `65` (dataError): Data error: corrupt or newer-format document, failed validation.
- `66` (inputNotFound): Input file not found or unreadable.
- `70` (internalError): Internal error.
- `73` (cannotCreateOutput): Cannot create the output (exists without --force, permission).
- `74` (ioError): I/O error.
- `75` (temporaryFailure): Temporary failure (network); retry later.
- `77` (notPermitted): Not permitted by the licence.
- `130` (cancelled): Cancelled (Ctrl-C).

A batch finishes with `3` when some items failed and others did not; with `1` when all did.

## Interrupting

Ctrl-C stops the command (exit `130`). Documents are written atomically, so one is never left half written.