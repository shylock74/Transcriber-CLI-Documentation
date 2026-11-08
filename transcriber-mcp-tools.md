# transcriber mcp tools

List the MCP tools, or show one tool's definition and input schema.

## Synopsis

```
transcriber mcp tools [options] [<tool>]
```

## Description

Examples:

```
transcriber mcp tools
transcriber mcp tools subs_list
transcriber mcp tools --read-only --json
```

## Arguments

- `<tool>`: A tool name (e.g. subs_list): its full definition. Optional.

## Options

- `--read-only`: Only the tools that read (list, show, info, export to stdout…).
- `--only <glob>`: Only the tools matching this glob (tool or command name, e.g. 'subs_*'). Repeatable. Repeatable.
- `--exclude <glob>`: Leave out the tools matching this glob. Repeatable. Repeatable.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber mcp](transcriber-mcp.md)
- [Output, JSON and exit codes](output.md)
