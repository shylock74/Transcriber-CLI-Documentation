# transcriber concat

Join several audio or video files into one (to transcribe them as one).

## Synopsis

```
transcriber concat [options] <media>...
```

## Description

Video files are joined into a ProRes 422 / PCM .mov (their audio kept); audio files, or any mix with --audio-only, into a PCM .wav. Mixing video and audio-only files needs --audio-only (the video would be lost for some parts).

--trim N=IN-OUT keeps only that part of file N (in the final order; licensed copies). The order is the one given, or by name / creation date / modification date (--order), reversed with --reverse.

Examples:

```
transcriber concat part1.mp4 part2.mp4 part3.mp4 -o interview.mov
transcriber concat recordings/*.m4a --order date -o day.wav
transcriber concat a.mov b.mov --trim 2=00:00:05-00:12:30 -o cut.mov
transcriber concat *.mp4 -o all.mov && transcriber transcribe all.mov
```

## Arguments

- `<media>...`: Media files, at least two.

## Options

- `-o, --output <path>`: Output file: .mov for video, .wav for audio (default: beside the first file).
- `--order <order>`: given, name, date (creation) or modified. Default: `given`. Values: `given`, `name`, `date`, `modified`.
- `--reverse`: Reverse the order.
- `--audio-only`: Join only the audio (a .wav), also of video files.
- `--trim <N=IN-OUT>`: Keep only IN-OUT of file N, e.g. 2=00:01:00-00:05:30. Repeatable. Repeatable.
- `--force`: Overwrite the output.
- `--dry-run`: Show the order, durations and output; join nothing.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
