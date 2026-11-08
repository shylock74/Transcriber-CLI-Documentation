# transcriber open

Open documents or media in the Transcriber app, or show them in the Finder.

## Synopsis

```
transcriber open [options] [<file>...]
```

## Description

A .transcriber document opens in its window. One audio or video file becomes a new document with that media as its source, as when it is dropped on the app; two or more ask whether to batch-transcribe or concatenate them. With no file, the app is just launched (or brought to the front).

A document open in the app is protected: commands that write it are refused (exit 11) unless --force, since the app would overwrite the change at its next save.

Examples:

```
transcriber open talk.transcriber
transcriber open interview.mov
transcriber open --reveal talk.transcriber talk.srt
transcriber open --background *.transcriber
```

## Arguments

- `<file>...`: Documents (.transcriber) or audio/video files. Optional.

## Options

- `--reveal`: Show the files in the Finder instead (any kind of file).
- `--background`: Do not bring Transcriber to the front.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
