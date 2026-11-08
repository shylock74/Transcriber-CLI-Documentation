# transcriber transcribe

Transcribe media files into Transcriber documents (and export them).

## Synopsis

```
transcriber transcribe [options] <media>...
```

## Description

Every media file becomes a document named like it (<name>.transcriber), beside it or in --output-dir. Settings come from the app (or --preset/--config/--set); the options below override them for this run and are saved in the document.

Unlicensed copies transcribe the first 45 seconds (exit code 10).

Examples:

```
transcriber transcribe interview.mp4
transcriber transcribe interview.mp4 -l it -m large-v3-turbo \
    --export srt,txt
transcriber transcribe *.wav --output-dir ~/Transcripts --vad \
    --dictionary "Names"
transcriber transcribe talk.mov --in 00:10:00 --out 00:25:00 \
    --print srt > part.srt
transcriber transcribe a.m4a --no-project --export vtt --export-dir web/
transcriber transcribe talk.mp4 --ai-correct --ai-provider anthropic \
    --translate-to de,fr --export srt
```

After the transcription, --ai-punctuate, --ai-correct and --translate-to run in this order, before the document and the exports are written (the exports cover the source track).

## Arguments

- `<media>...`: Media files (audio or video).

## Options

- `-m, --model <model>`: Whisper model: small, medium, large-v2, large-v3, large-v3-turbo, parakeet.
- `-l, --language <code>`: Spoken language (ISO code, e.g. en, it) or 'auto'.
- `--translate-to-english`: Whisper translates the speech to English while transcribing.
- `--no-translate-to-english`: Whisper translates the speech to English while transcribing.
- `--threads <N>`: CPU threads used by Whisper.
- `--coreml`: Use the Core ML encoder (Apple Neural Engine).
- `--no-coreml`: Use the Core ML encoder (Apple Neural Engine).
- `--single-word`: One word per subtitle (word-level timing).
- `--no-single-word`: One word per subtitle (word-level timing).
- `--vad`: Voice activity detection (skip silence).
- `--no-vad`: Voice activity detection (skip silence).
- `--vad-threshold <p>`: VAD speech probability threshold (0…1).
- `--vad-min-speech <ms>`: VAD: shortest speech, milliseconds.
- `--vad-min-silence <ms>`: VAD: shortest silence, milliseconds.
- `--vad-padding <ms>`: VAD: padding around speech, milliseconds.
- `--dtw`: DTW token timestamps (more precise word timing).
- `--no-dtw`: DTW token timestamps (more precise word timing).
- `--align`: Forced alignment of the words to the audio after the transcription.
- `--no-align`: Forced alignment of the words to the audio after the transcription.
- `--channel <joint|N>`: Audio channel: 'joint' (all channels mixed) or a channel number from 1.
- `--prompt <text>`: Extra prompt for Whisper: names, terms, spelling, style.
- `--dictionary <name>`: Use this dictionary (name or id). Repeatable; added to the ones in the settings. Repeatable.
- `--in <time>`: Transcribe from this time (segment; licensed copies).
- `--out <time>`: Transcribe up to this time (segment; licensed copies).
- `--soft-separators <list>`: Where long sentences may split: any of commas,semicolons,colons,quotes, or 'none'.
- `--auto-split`: Split long subtitles while transcribing.
- `--no-auto-split`: Split long subtitles while transcribing.
- `--max-length <N>`: Auto-split length in characters (default: the SRT line limit).
- `--hallucination-filter`: Drop Whisper's typical hallucinations.
- `--no-hallucination-filter`: Drop Whisper's typical hallucinations.
- `--min-subtitle-duration <s>`: Drop subtitles shorter than this (hallucination filter), seconds.
- `--preprocess`: Pre-process the audio (speech detection, loudness) before Whisper.
- `--no-preprocess`: Pre-process the audio (speech detection, loudness) before Whisper.
- `--speech-threshold <p>`: Pre-processing speech threshold (0…1).
- `--beam-size <N>`: Beam search size (advanced).
- `--flash-attention`: Flash attention (advanced; faster on recent Macs).
- `--no-flash-attention`: Flash attention (advanced; faster on recent Macs).
- `--entropy-threshold <x>`: Entropy threshold (advanced).
- `--no-speech-threshold <x>`: No-speech threshold (advanced).
- `--max-context <N>`: Max context tokens (advanced; 0 = no context between windows).
- `--ai-punctuate`: AI: add strong punctuation to long sentences after the transcription.
- `--ai-correct`: AI: semantic correction of the transcription (uses the Global Contexts enabled by default).
- `--translate-to <codes>`: DeepL: add translation tracks, comma separated (e.g. de,fr,en-gb).
- `--ai-provider <provider>`: AI provider for --ai-*: gemini, openai, anthropic, deepseek, local.
- `--ai-model <id>`: AI text model id for --ai-* (see 'transcriber ai models').
- `--ai-key-file <path>`: Read the AI provider's API key from this file.
- `--deepl-key-file <path>`: Read the DeepL API key from this file.
- `-o, --output <path>`: Document path (one media file only; '-' = stdout).
- `--output-dir <dir>`: Folder for the documents (default: beside each media file).
- `--no-project`: Do not write the .transcriber document (use with --export or --print).
- `--export <formats>`: Also export these formats (txt, timecoded, rtf, csv, srt, vtt, itt, ass, fcpxml, burnin, json).
- `--export-dir <dir>`: Folder for the --export files (default: beside the document).
- `--print <format>`: Print one text format on stdout (txt, srt, vtt, itt, csv, json).
- `--download-model`: Download the model first if it is not installed.
- `--force`: Overwrite existing documents and exports.
- `--skip-existing`: Skip media files whose document already exists.

## Global options

Every command also accepts the [global options](global-options.md): `--json`, `--progress`, `-q`, `-v`, `--no-color`, `--log-file`, `-y`, `--no-input`, `--config`, `--preset` and `--set`.

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
