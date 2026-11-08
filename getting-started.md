# Getting started

`transcriber` is the command line edition of the Transcriber app. It is the same engine: Whisper on your Mac for the transcription, the same editing rules, the same AI and translation providers, the same `.transcriber` documents. Everything the command does can be opened in the app, and the other way round.

## Install

In the app choose **Transcriber ▸ Install Command Line Tool…**. It links `transcriber` into `/usr/local/bin` (macOS asks for an administrator password) and the manual pages into `/usr/local/share/man/man1`. If you decline, it can install into `~/.local/bin` instead and tells you how to add that folder to your `PATH`. **Uninstall Command Line Tool…** removes the links.

The command is the program inside the app (`Transcriber.app/Contents/MacOS/transcriber-cli`), so it is always the same version as the app, and an app update updates the command too.

Check the installation:

```
transcriber doctor
transcriber --version
```

## A first session

```
transcriber models list
transcriber transcribe interview.mp4 --language it --export srt
transcriber subs list interview.transcriber --match "budget" --ignore-case
transcriber subs set interview.transcriber 12 --text "Hello, world."
transcriber translate run interview.transcriber --to en,fr
transcriber export interview.transcriber --format srt,vtt --all-tracks
```

## Getting help

- `transcriber --help` lists the command groups; `transcriber <group> --help` lists a group; `transcriber <group> <command> --help` documents one command, with examples.
- `man transcriber` is this manual; `man transcriber-subs-list` documents one command.
- Misspelled commands and options are corrected with a suggestion.

## Licence

A copy without a licence transcribes only the first 45 seconds of each media and finishes with exit code `10`. Licensing is handled by FxFactory; `transcriber license status` tells which case you are in.