# transcriber models download

Download models (resumes nothing: a failed download starts over).

## Synopsis

```
transcriber models download [options] [<model>...]
```

## Description

Examples:

```
transcriber models download large-v3-turbo
transcriber models download --all
```

## Arguments

- `<model>...`: Models: small, medium, large-v2, large-v3, large-v3-turbo, parakeet. Optional.

## Options

- `--all`: Every model.
- `--force`: Download again even when installed.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber models](transcriber-models.md)
- [Output, JSON and exit codes](output.md)
