# Global options

Every command accepts these options, wherever they appear on the command line.

- `--json`: Print one JSON envelope on stdout ({schema, command, ok, result, warnings, error}).
- `--progress <auto|bar|ndjson|none>`: Progress reporting on stderr. Default: `auto`. Values: `auto`, `bar`, `ndjson`, `none`.
- `-q, --quiet`: Print only results and errors.
- `-v, --verbose`: Print details of what is being done.
- `--no-color`: No ANSI colours (also: NO_COLOR environment variable).
- `--log-file <path>`: Append a log of the run to this file.
- `-y, --yes`: Answer yes to every confirmation.
- `--no-input`: Never prompt; fail when an answer would be needed.
- `--config <file>`: Settings file (YAML or JSON) layered over the app settings. Repeatable. Repeatable.
- `--preset <name>`: Settings preset (saved in the app) layered over the app settings.
- `--set <key=value>`: Override one setting, e.g. --set srtSettings.maxCharPerLine=42. Repeatable. Repeatable.

See [Output, JSON and exit codes](output.md) and [Settings and environment](configuration.md).