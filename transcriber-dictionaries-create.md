# transcriber dictionaries create

Create a dictionary.

## Synopsis

```
transcriber dictionaries create [options] <name>
```

## Description

Example:

```
transcriber dictionaries create "Brand names" \
    --prompt "Ulti.Media, FxFactory, Transcriber"
```

## Arguments

- `<name>`: Name.

## Options

- `--description <text>`: Description.
- `--prompt <text>`: Prompt: words Whisper should expect.
- `--dry-run`: Show what would change; write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber dictionaries](transcriber-dictionaries.md)
- [Output, JSON and exit codes](output.md)
