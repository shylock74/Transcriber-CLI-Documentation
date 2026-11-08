# transcriber shell

Interactive shell on one document: run commands without naming it, undo, save.

## Synopsis

```
transcriber shell [options] <document>
```

## Description

Type any transcriber command without 'transcriber' and without the document: the shell adds it ('subs list --select 1..20', 'ai correct', 'export -f srt -o talk.srt'). Commands work on a copy of the document: 'save' writes it, 'undo' and 'redo' step through the changes, 'changes' shows what changed since the last save.

Built-ins:

```
help [command]       the built-ins and commands, or a command's help
undo [N] / redo [N]  undo or redo the last N changes
changes              what changed since the last save
save [path]          write the document (with a path: save as, and go
                     on there)
revert               drop the unsaved changes (undoable)
status               document, unsaved changes, undo steps
cd <folder> / pwd    the folder relative paths start from
!<command>           run a system shell command
quit, exit, Ctrl-D   leave (asks to save unsaved changes)
```

Tab completes commands, options and their values; the history is kept between sessions. Ctrl-C stops the running command, not the shell.

Without a terminal the commands are read from stdin, one per line, and the shell stops at the first failing one (--keep-going goes on); -c gives them as options. Unsaved changes at the end are an error: finish with 'save', or use --autosave.

Examples:

```
transcriber shell talk.transcriber
transcriber shell talk.transcriber -c "subs replace teh the" \
    -c "ai correct" -c save
transcriber shell talk.transcriber --autosave < edits.txt
```

## Arguments

- `<document>`: Transcriber document (.transcriber).

## Options

- `-c, --command <line>`: Run this command line (repeatable), then leave. Repeatable.
- `--autosave`: Save after every command that changes the document.
- `--keep-going`: Without a terminal: go on after a failing command.
- `--force`: Save even if the document is open in Transcriber.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
