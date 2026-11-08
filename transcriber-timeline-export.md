# transcriber timeline export

Export a timeline: FCPXML edit, text, text with timecodes, RTF, JSON or CSV.

## Synopsis

```
transcriber timeline export [options] <document>
```

## Description

Formats:

```
fcpxml  the edit for Final Cut Pro: one clip per enabled sentence (with the
        handles of 'settings get trEditing.handles'); chapters are left out
txt     the text of the enabled sentences
tc      the same, each sentence with its timecodes
rtf     rich text with timecodes (as the app's RTF export)
json    the sentences with state, times and text
csv     number, enabled, marked, in, out, duration, text
```

The format comes from --format or the -o extension (default txt, on stdout). --send-to-fcp opens the FCPXML in Final Cut Pro.

Examples:

```
transcriber timeline export talk.transcriber -o cut.fcpxml
transcriber timeline export talk.transcriber --timeline Selects \
    --send-to-fcp
transcriber timeline export talk.transcriber --format tc | pbcopy
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--timeline <timeline>`: Timeline: name, id or number (default: the selected one).
- `-o, --output <path>`: Output file ('-' = stdout).
- `--format <format>`: fcpxml, txt, tc, rtf, json or csv. Values: `fcpxml`, `txt`, `tc`, `rtf`, `json`, `csv`.
- `--send-to-fcp`: Open the FCPXML in Final Cut Pro.
- `--force`: Overwrite an existing file.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber timeline](transcriber-timeline.md)
- [Output, JSON and exit codes](output.md)
