# transcriber dictionaries export

Write a dictionary to a .TrDict file (JSON; the app can import it).

## Synopsis

```
transcriber dictionaries export [options] <dictionary>
```

## Arguments

- `<dictionary>`: Dictionary: name, number or id.

## Options

- `-o, --output <path>`: Output file (default: <name>.TrDict; '-' = stdout).
- `--force`: Overwrite an existing file.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber dictionaries](transcriber-dictionaries.md)
- [Output, JSON and exit codes](output.md)
