# transcriber ai correct

Semantic correction: fix misheard words using the text and the global contexts.

## Synopsis

```
transcriber ai correct [options] <document>
```

## Description

Corrected subtitles keep their previous text: review them with 'ai diff', then 'ai accept' or 'ai reject'. The global contexts used are the document's (see 'doc contexts'), or the library defaults; --contexts/--no-contexts override. --dry-run calls the AI and prints the changes without writing.

Examples:

```
transcriber ai correct talk.transcriber
transcriber ai correct talk.transcriber --provider anthropic \
    --contexts "Product names"
transcriber ai correct talk.transcriber --select 10..40 --dry-run
```

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `-t, --track <track>`: Track: 'source' (default), or a translation's id, language code or title. Default: `source`.
- `--select <selector>`: Only these subtitles. Subtitles: 12 · 3..7 · 3,5,9 · #<id> · @<time> · all
- `--from <time>`: Only subtitles starting at or after this time.
- `--to <time>`: Only subtitles starting before this time.
- `--match <regex>`: Only subtitles whose text matches this regular expression.
- `--ignore-case`: Case-insensitive --match.
- `--speaker <name>`: Only subtitles of this speaker.
- `--enabled-only`: Only enabled subtitles.
- `--disabled-only`: Only disabled subtitles.
- `--ai-modified`: Only subtitles changed by AI and not yet reviewed.
- `--longer-than <N>`: Only subtitles longer than N characters.
- `--shorter-than <seconds>`: Only subtitles shorter than N seconds.
- `--provider <provider>`: AI provider: gemini, openai, anthropic, deepseek, local (default: the app's).
- `--model <id>`: AI text model id (see 'transcriber ai models'; default: the provider's selected one).
- `--api-key-file <path>`: Read the provider's API key from this file ('-' = stdin).
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.
- `--contexts <context>`: Global contexts to use (name, id or number; repeatable or comma separated). Repeatable.
- `--no-contexts`: Use no global context.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber ai](transcriber-ai.md)
- [Output, JSON and exit codes](output.md)
