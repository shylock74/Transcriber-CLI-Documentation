# transcriber contexts create

Create a context, empty or from a file / stdin.

## Synopsis

```
transcriber contexts create [options] <name>
```

## Description

The format is taken from --format, else the file extension, else sniffed.

Examples:

```
transcriber contexts create "Product names" --from products.yaml
pbpaste | transcriber contexts create "Guests" --from - --language it-IT \
    --disabled
```

## Arguments

- `<name>`: Name (made unique if taken).

## Options

- `--from <path>`: Content file ('-' = stdin).
- `--format <format>`: yaml, json, md or txt. Values: `yaml`, `json`, `md`, `txt`.
- `--language <code>`: Reference language (BCP-47, e.g. it-IT) or 'auto'. Default: `auto`.
- `--disabled`: Not enabled by default for new documents.
- `--dry-run`: Show what would be created.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber contexts](transcriber-contexts.md)
- [Output, JSON and exit codes](output.md)
