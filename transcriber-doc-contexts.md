# transcriber doc contexts

Show or choose the Global Contexts a document's AI correction uses.

## Synopsis

```
transcriber doc contexts [options] <document>
```

## Description

Until chosen, a document uses the contexts enabled in the library ('library defaults'). Contexts are named by name, number or id (see 'transcriber contexts list'). Examples: transcriber doc contexts talk.transcriber --add "Ulti.Media" · transcriber doc contexts talk.transcriber --defaults

## Arguments

- `<document>`: Transcriber document (.transcriber), or - for stdin.

## Options

- `--add <context>`: Use this context. Repeatable. Repeatable.
- `--remove <context>`: Stop using this context. Repeatable. Repeatable.
- `--none`: Use no context.
- `--defaults`: Go back to the library defaults.
- `-o, --output <path>`: Write the document here instead of in place ('-' = stdout).
- `--dry-run`: Show what would change; write nothing.
- `--backup`: Copy the document to <name>.transcriber.bak before writing it.
- `--force`: Write even if the document is open in Transcriber, or the output exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber doc](transcriber-doc.md)
- [Output, JSON and exit codes](output.md)
