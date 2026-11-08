# Settings and environment

The command uses the **same settings as the app**: what you choose in Transcriber ▸ Settings applies to the command, and `settings set` changes what the app uses next. Four layers are applied, each over the previous one:

- the app's settings;
- `--preset <name>`: a settings preset saved in the app;
- `--config <file>` (YAML or JSON, repeatable): only the keys the file mentions;
- `--set key=value` (repeatable): single keys, for example `--set srtSettings.maxCharPerLine=42`.

The layers apply to this run only; `settings set` is what writes the app's settings. A document keeps the settings it was made with; the layers decide the settings of new documents and the AI and translation services used by the run. `settings keys` lists every key with its type, `settings diff` compares sources, `preset save` stores the current layers as a preset.

```
transcriber transcribe talk.mp4 --preset Interviews --set whisperSettings.language=it
transcriber settings set srtSettings.maxCharPerLine=38
transcriber doc settings diff talk.transcriber --against app
```

## Shared with the app

Settings, presets, dictionaries, Global Contexts and the batch queue are the app's own: a change made by the command is picked up by a running app within a moment (the command posts the distributed notification `media.ulti.transcriber.storeChanged`), and the other way round.

## Environment variables

- `NO_COLOR`: no colours.
- `TRANSCRIBER_NO_INPUT`: never prompt (as `--no-input`).
- `TRANSCRIBER_BATCH_QUEUE=<file>`: use this file for the batch queue instead of the app's (`batch queue …`); handy for scripts and tests.
- `TRANSCRIBER_<PROVIDER>_API_KEY`, `OPENAI_API_KEY`, `GEMINI_API_KEY`, `GOOGLE_API_KEY`, `ANTHROPIC_API_KEY`, `DEEPSEEK_API_KEY`, `MAGNIFIC_API_KEY`, `DEEPL_API_KEY`: API keys, see [API keys](keys.md).
- `TRANSCRIBER_SHELL_DOC`, `TRANSCRIBER_IN_SHELL`, `TRANSCRIBER_REEXEC`, `TRANSCRIBER_CHILD`: set by the command for its own child processes; do not set them.

## Files

- `~/Library/Application Support/Transcriber/shell-history`: history of the interactive shell.
- The app's settings, presets, dictionaries and Global Contexts, in the app's own folders (`settings path` and `contexts path` print where they are).