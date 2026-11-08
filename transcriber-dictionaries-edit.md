# transcriber dictionaries edit

Change a dictionary's description, prompt or favorite flag.

## Synopsis

```
transcriber dictionaries edit [options] <dictionary>
```

## Arguments

- `<dictionary>`: Dictionary: name, number or id.

## Options

- `--description <text>`: Description.
- `--prompt <text>`: Prompt ('' clears it).
- `--favorite <bool>`: Favorite: true or false.
- `--dry-run`: Show what would change; write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber dictionaries](transcriber-dictionaries.md)
- [Output, JSON and exit codes](output.md)
