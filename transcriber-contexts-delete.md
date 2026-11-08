# transcriber contexts delete

Delete contexts (their files go to the Trash; asks first, --yes skips).

## Synopsis

```
transcriber contexts delete [options] [<context>...]
```

## Description

Example:

```
transcriber contexts delete "Old guests" --yes
```

## Arguments

- `<context>...`: Contexts: name, id or number. Optional.

## Options

- `--dry-run`: Show what would be deleted.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber contexts](transcriber-contexts.md)
- [Output, JSON and exit codes](output.md)
