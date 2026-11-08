# transcriber docs show

Print the manual page of a command as Markdown.

## Synopsis

```
transcriber docs show [options] [<command>...]
```

## Description

Same text as --help with the arguments and options described. Without a command, the overview.

Example:

```
transcriber docs show subs list
```

## Arguments

- `<command>...`: The command words, e.g. subs list. Optional.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber docs](transcriber-docs.md)
- [Output, JSON and exit codes](output.md)
