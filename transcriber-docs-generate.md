# transcriber docs generate

Write the manual as man pages, Markdown files and/or an HTML site.

## Synopsis

```
transcriber docs generate [options]
```

## Description

man: transcriber.1 (overview and guides) and one page per command (transcriber-subs-list.1). markdown: README.md plus one file per page. html: index.html plus one file per page and style.css. Existing files with the same names are replaced.

Example:

```
transcriber docs generate -f html -d site
```

## Options

- `-f, --format <format>`: man, markdown, html or all. Default: `all`.
- `-d, --output-dir <folder>`: Folder to write into (created if needed). Man pages go to <dir>/man1 with --format all. Default: `.`.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber docs](transcriber-docs.md)
- [Output, JSON and exit codes](output.md)
