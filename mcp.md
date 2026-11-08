# MCP server

`transcriber mcp serve` speaks the Model Context Protocol on stdin/stdout, so an AI assistant can transcribe, edit, translate and export with Transcriber. Every command is a tool: `subs list` is `subs_list`, with the same options as properties. `mcp tools` lists them with their schemas.

## Configure a client

`transcriber mcp config --client <client>` prints what to add:

```
transcriber mcp config --client claude-desktop
transcriber mcp config --client claude-code
transcriber mcp config --client cursor
transcriber mcp config --client vscode
```

Nothing is written for you: copy the output where it goes (the command says where).

## What is exposed

- Every leaf command except `keys set`, `keys remove` (secrets), `shell`, `ai review` (interactive) and `mcp` itself.
- `--read-only` serves only commands that read; `--only <glob>` and `--exclude <glob>` narrow the list (`--only 'subs_*'`).
- Annotations: `readOnlyHint`, `destructiveHint` (delete, remove, clear, reset) and `openWorldHint` (calls an AI or translation provider).
- Each tool also accepts `yes`, `preset`, `set` (settings overrides) and `extra_args`.

## Behaviour

Each call runs the command as a child process with `--json --progress ndjson --no-input`; the result is returned as text and, with protocol 2025-06-18 or later, as `structuredContent`. Progress is sent as `notifications/progress` when the client gives a progress token. Cancelling a call stops the command. Errors come back as tool errors with the `kind` and the `hint`.

Relative paths start from the folder given by `--directory` (default: where the server was started): prefer absolute paths. A document open in the app is refused unless the call passes `force`. An unlicensed copy transcribes at most 45 seconds.