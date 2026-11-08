# transcriber mcp

Model Context Protocol server: Transcriber's commands as tools for AI assistants.

## Synopsis

```
transcriber mcp <command> [options]
```

## Description

'transcriber mcp serve' speaks MCP on stdin/stdout, so Claude (Desktop or Code), Cursor, VS Code and other MCP clients can transcribe, edit, translate and export. Every command is a tool ('subs list' is subs_list) with the same options; 'keys set/remove', 'shell' and 'ai review' are not exposed. 'mcp config' prints the client configuration.

Examples:

```
transcriber mcp config --client claude-desktop
transcriber mcp tools
transcriber mcp serve --read-only
```

## Commands

- [`serve`](transcriber-mcp-serve.md): Run the MCP server on stdin/stdout (started by the MCP client).
- [`tools`](transcriber-mcp-tools.md): List the MCP tools, or show one tool's definition and input schema.
- [`config`](transcriber-mcp-config.md): Print the configuration that adds this MCP server to a client.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
