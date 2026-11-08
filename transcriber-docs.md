# transcriber docs

Generate the manual (man pages, Markdown, HTML) from the commands.

## Synopsis

```
transcriber docs <command> [options]
```

## Description

The manual is made from the command tree itself, so it always matches what the parser accepts. The man pages ship inside the app and are installed with the command (Transcriber > Install Command Line Tool).

Examples:

```
transcriber docs generate --format man --output-dir man
transcriber docs generate --format all --output-dir ~/Desktop/cli-docs
transcriber docs show subs list
```

## Commands

- [`generate`](transcriber-docs-generate.md): Write the manual as man pages, Markdown files and/or an HTML site.
- [`show`](transcriber-docs-show.md): Print the manual page of a command as Markdown.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
