# transcriber dictionaries add-item

Add a replacement: texts to find → replacement.

## Synopsis

```
transcriber dictionaries add-item [options] <dictionary>
```

## Description

Example:

```
transcriber dictionaries add-item "Brand names" --find "ultimedia" \
    --find "ultra media" --replace "Ulti.Media"
```

## Arguments

- `<dictionary>`: Dictionary: name, number or id.

## Options

- `--find <text>`: Text to find. Repeatable. Repeatable.
- `--replace <text>`: Replacement ('' deletes the found text).
- `--case-sensitive`: Match case.
- `--dry-run`: Show what would change; write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber dictionaries](transcriber-dictionaries.md)
- [Output, JSON and exit codes](output.md)
