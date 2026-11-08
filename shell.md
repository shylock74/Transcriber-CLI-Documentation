# The interactive shell

`transcriber shell talk.transcriber` opens a prompt for one document. Type commands without `transcriber` and without the document: the shell adds it. Commands work on a **copy** of the document; nothing reaches the file until you `save`.

```
talk> subs list --select 1..5
talk> subs replace teh the
talk*> changes
talk*> ai correct
talk*> undo
talk*> save
```

The `*` in the prompt marks unsaved changes. Tab completes commands, options and the values of options; ↑ recalls history (kept between sessions).

## Built-in commands

- `help [command]`: this list, or the help of a command.
- `undo [N]`, `redo [N]`: step through the changes.
- `changes`: what changed since the last save.
- `save [path]`: write the document (with a path: save as, and go on there).
- `revert`: drop the unsaved changes (undoable).
- `status`, `pwd`, `cd <folder>`: where you are.
- `!command`: run a shell command.
- `quit`, `exit`: leave; with unsaved changes it asks whether to save.

`shell`, `mcp` and `doc new` are not available inside the shell.

## Scripts

Without a terminal the commands are read from stdin, one per line, and the shell stops at the first failing one (`--keep-going` goes on and finishes with exit `3`). `-c "<line>"` (repeatable) gives commands as options. Unsaved changes at the end are an error: finish with `save`, or use `--autosave`.

```
transcriber shell talk.transcriber -c "subs replace teh the" -c "ai correct" -c save
transcriber shell talk.transcriber --autosave < edits.txt
```

## Reviewing AI corrections

`ai review talk.transcriber` walks through the subtitles the AI changed: `y` accepts, `n` rejects, `e` edits (↑ brings the AI text back to edit), `s` skips, `a` accepts all the rest, `r` rejects all, `u` undoes, `q` quits.