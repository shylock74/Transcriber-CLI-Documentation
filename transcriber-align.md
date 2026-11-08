# transcriber align

Align an official text onto the subtitles (forced alignment): same timing, official words.

## Synopsis

```
transcriber align [options] <document>
```

## Description

The official text is matched to the subtitles block by block. Engines:

```
algorithmic  local sequence alignment only: instant, free, deterministic
             (default)
hybrid       algorithmic first, then the AI only on blocks below --threshold
llm          every block redistributed by the AI, in windows of --window
             blocks
```

--apply all applies every change; confident only those whose similarity is at or above --threshold; none only prints the plan (nothing is written). --plan-out saves the plan as JSON for review.

Examples:

```
transcriber align talk.transcriber --text script.txt
transcriber align talk.transcriber --text script.txt --apply none \
    --plan-out plan.json
transcriber align talk.transcriber --text - --engine hybrid \
    --provider anthropic < script.txt
transcriber align talk.transcriber --text it-script.txt --track it \
    --respect-segmentation
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--provider <provider>`: AI provider: gemini, openai, anthropic, deepseek, local (default: the app's).
- `--model <id>`: AI text model id (see 'transcriber ai models'; default: the provider's selected one).
- `--api-key-file <path>`: Read the provider's API key from this file ('-' = stdin).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--text <path>`: The official text file ('-' = stdin).
- `--engine <engine>`: algorithmic, hybrid or llm. Default: `algorithmic`. Values: `algorithmic`, `hybrid`, `llm`.
- `--threshold <x>`: Similarity below which a block is uncertain (0…1, default 0.72). Default: `0.72`.
- `--window <N>`: Blocks per AI window (llm engine, default 25). Default: `25`.
- `--respect-segmentation`: Keep the subtitle boundaries: never split or merge blocks.
- `--apply <mode>`: all, confident or none. Default: `all`. Values: `all`, `confident`, `none`.
- `--plan-out <path>`: Write the alignment plan as JSON here ('-' = stdout).
- `--all`: Show unchanged blocks too in the plan.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
