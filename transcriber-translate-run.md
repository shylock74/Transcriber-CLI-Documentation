# transcriber translate run

Translate into one or more languages (one new track each).

## Synopsis

```
transcriber translate run [options] <document>
```

## Description

Each language becomes a translation track with the same timing as the source. --join-before translates whole sentences (better quality) and --split-after splits them again at the subtitle length limit. --dry-run translates but writes nothing (DeepL is still called).

Examples:

```
transcriber translate talk.transcriber --to it
transcriber translate talk.transcriber --to IT,FR,DE --join-before \
    --split-after
transcriber translate talk.transcriber --to EN-GB --from it --replace
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--to <codes>`: Target languages, DeepL codes, comma separated (e.g. IT,FR,EN-GB,PT-BR).
- `--from <track>`: Track to translate from: 'source' (default) or a translation. Default: `source`.
- `--source-language <code>`: Language of the text (default: the document's; 'auto' lets DeepL detect it).
- `--join-before`: Join the subtitles into sentences before translating.
- `--split-after`: Split the translated sentences at the subtitle length limit.
- `--title <text>`: Title of the new track (one language only; default: the language code).
- `--replace`: Replace existing tracks in the same language (default: refuse).
- `--keep-both`: Add a new track even when one in the same language exists.
- `--no-select`: Do not make the new track the displayed one.
- `--api-key-file <path>`: Read the DeepL key from this file ('-' = stdin).

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber translate](transcriber-translate.md)
- [Output, JSON and exit codes](output.md)
