# transcriber mcp serve

Run the MCP server on stdin/stdout (started by the MCP client).

## Synopsis

```
transcriber mcp serve [options]
```

## Description

JSON-RPC 2.0, one message per line. Tool calls run the matching command with --json; its progress is sent as notifications/progress when the client gives a progress token, and cancelling a call stops the command. Logs: --log-file.

Example (client configuration): command "transcriber", args ["mcp", "serve"]

## Options

- `--read-only`: Only the tools that read (list, show, info, export to stdout…).
- `--only <glob>`: Only the tools matching this glob (tool or command name, e.g. 'subs_*'). Repeatable. Repeatable.
- `--exclude <glob>`: Leave out the tools matching this glob. Repeatable. Repeatable.
- `--directory <folder>`: Folder that relative paths start from.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber mcp](transcriber-mcp.md)
- [Output, JSON and exit codes](output.md)
