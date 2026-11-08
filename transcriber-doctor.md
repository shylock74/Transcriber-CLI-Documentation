# transcriber doctor

Check the installation: licence, models, keys, settings, PATH, disk space.

## Synopsis

```
transcriber doctor [options]
```

## Description

Exit code 1 when a check fails; warnings do not change it.

## Options

- `--test-keys`: Also call the providers to test the configured keys (costs a few tokens).

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
