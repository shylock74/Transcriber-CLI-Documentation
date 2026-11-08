# transcriber contexts add-entity

Add an entity to a YAML context (or more sounds-like variants to an existing one).

## Synopsis

```
transcriber contexts add-entity [options] [<context>]
```

## Description

Examples:

```
transcriber contexts add-entity "Product names" --canonical "Transcriber" \
    --sounds-like "transcribe her,trans criber"
transcriber contexts add-entity Guests --canonical "Ilaria Rossi" \
    --category person --description "Host"
transcriber contexts add-entity --new "Brands" --canonical "Ulti.Media"
```

## Arguments

- `<context>`: YAML context: name, id or number (or --new). Optional.

## Options

- `--new <name>`: Create a new YAML context with this name instead.
- `--canonical <text>`: The correct spelling.
- `--sounds-like <list>`: Misheard variants, comma separated (repeatable). Repeatable.
- `--category <text>`: person, product, place, organisation, term…
- `--description <text>`: A short description.
- `--dry-run`: Print the resulting YAML, write nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber contexts](transcriber-contexts.md)
- [Output, JSON and exit codes](output.md)
