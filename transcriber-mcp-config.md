# transcriber mcp config

Print the configuration that adds this MCP server to a client.

## Synopsis

```
transcriber mcp config [options]
```

## Description

Clients: claude-desktop (paste into claude_desktop_config.json), claude-code (a 'claude mcp add' command), cursor (~/.cursor/mcp.json), vscode (.vscode/mcp.json), generic. The command is the installed 'transcriber' (Transcriber ▸ Install Command Line Tool) when there is one, else the binary inside the app. Nothing is written: copy the output where it goes.

Examples:

```
transcriber mcp config --client claude-code
transcriber mcp config --client claude-desktop --read-only
```

## Options

- `--read-only`: Only the tools that read (list, show, info, export to stdout…).
- `--only <glob>`: Only the tools matching this glob (tool or command name, e.g. 'subs_*'). Repeatable. Repeatable.
- `--exclude <glob>`: Leave out the tools matching this glob. Repeatable. Repeatable.
- `--client <client>`: claude-desktop, claude-code, cursor, vscode or generic. Default: `claude-desktop`. Values: `claude-desktop`, `claude-code`, `cursor`, `vscode`, `generic`.
- `--name <name>`: Server name in the client. Default: `transcriber`.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber mcp](transcriber-mcp.md)
- [Output, JSON and exit codes](output.md)
