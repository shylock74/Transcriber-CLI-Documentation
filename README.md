# Transcriber command line

`transcriber` 1.39.1: Transcribe, edit, translate and export subtitles with Transcriber, from the command line.

Works on .transcriber documents (the app's own format) and on media files. Every command accepts --json (one machine-readable envelope on stdout), --progress ndjson, --quiet, --verbose, --config/--preset/--set (settings layering) and more: see 'transcriber <command> --help' and 'man transcriber'.

Examples:

```
transcriber transcribe interview.mp4 --language it --export srt
transcriber export interview.transcriber --format srt,txt --track en
transcriber subs list interview.transcriber --match "budget" --ignore-case
transcriber translate interview.transcriber --to en,fr
transcriber batch run ~/Videos/*.mov --jobs 2 --export srt
```

## Guides

- [Getting started](getting-started.md): Install the command, transcribe a file, edit and export.
- [Documents, tracks and selectors](documents.md): How commands find documents, tracks and subtitles, and how they write.
- [Output, JSON and exit codes](output.md): Human and machine output, progress events, exit codes.
- [Settings and environment](configuration.md): How settings are layered, presets, and environment variables.
- [API keys](keys.md): Where the AI and translation keys come from.
- [The interactive shell](shell.md): Work on one document with undo, redo and save.
- [MCP server](mcp.md): Use Transcriber from Claude, Cursor, VS Code and other MCP clients.
- [Working with the app](integration.md): Open files in the app, protect open documents, share stores.
- [Global options](global-options.md): options every command accepts.

## Commands

- [`transcribe`](transcriber-transcribe.md): Transcribe media files into Transcriber documents (and export them).
- [`export`](transcriber-export.md): Export a document to subtitles, text, FCPXML or a burned-in video.
- [`import`](transcriber-import.md): Import SRT or WebVTT subtitles into a new or existing document.
- [`info`](transcriber-info.md): Show what a document holds: source media, tracks, subtitles, speakers, settings.
- [`stats`](transcriber-stats.md): Statistics of a track: subtitles, words, reading speed, speakers.
- [`validate`](transcriber-validate.md): Check subtitles against the SRT rules: length, lines, duration, overlaps, reading speed.
- [`text`](transcriber-text.md): Print the transcription as flowing text (optionally with timecodes).
- [`probe`](transcriber-probe.md): Media file information: duration, frame rate, size, audio, codecs, timecode.
- [`subs`](transcriber-subs.md): List, search and edit the subtitles of a document.
    - [`subs list`](transcriber-subs-list.md): List the subtitles of a track (with filters).
    - [`subs get`](transcriber-subs-get.md): Show subtitles in full: text, timing, id, speaker, notes, AI state.
    - [`subs search`](transcriber-subs-search.md): Find text in the subtitles (plain text or regular expression).
    - [`subs set`](transcriber-subs-set.md): Change the text, timing, speaker, notes or state of subtitles.
    - [`subs add`](transcriber-subs-add.md): Add a subtitle (placed in time order).
    - [`subs delete`](transcriber-subs-delete.md): Delete subtitles.
    - [`subs enable`](transcriber-subs-enable.md): Enable subtitles (they are exported again).
    - [`subs disable`](transcriber-subs-disable.md): Disable subtitles (kept in the document, left out of exports).
    - [`subs split`](transcriber-subs-split.md): Split subtitles at line breaks, at given strings, or at the soft separators.
    - [`subs merge`](transcriber-subs-merge.md): Merge subtitles: a range into one, or one subtitle with the next.
    - [`subs split-soft`](transcriber-subs-split-soft.md): Split every subtitle at the soft separators (commas, etc.) and sentence ends.
    - [`subs join-soft`](transcriber-subs-join-soft.md): Join subtitles that end with a soft separator to the next one.
    - [`subs split-long`](transcriber-subs-split-long.md): Split subtitles that do not fit in max lines × max characters per line.
    - [`subs split-newlines`](transcriber-subs-split-newlines.md): Make one subtitle of each line of multi-line subtitles.
    - [`subs join-newlines`](transcriber-subs-join-newlines.md): Replace line breaks inside subtitles with spaces.
    - [`subs compact`](transcriber-subs-compact.md): Merge short neighbours while the result fits a length (never across sentence ends).
    - [`subs shift`](transcriber-subs-shift.md): Move subtitles in time.
    - [`subs replace`](transcriber-subs-replace.md): Find and replace text (plain or regular expression, with $1 groups).
- [`speakers`](transcriber-speakers.md): List, rename and assign speakers.
    - [`speakers list`](transcriber-speakers-list.md): Speakers with subtitle counts and speaking time.
    - [`speakers rename`](transcriber-speakers-rename.md): Rename a speaker everywhere (every track).
    - [`speakers set`](transcriber-speakers-set.md): Assign a speaker to subtitles.
- [`tracks`](transcriber-tracks.md): List, add, duplicate, rename and remove tracks (translations).
    - [`tracks list`](transcriber-tracks-list.md): List the tracks with their subtitle counts.
    - [`tracks add`](transcriber-tracks-add.md): Add an empty track, or one with the source's timing and empty or copied text.
    - [`tracks duplicate`](transcriber-tracks-duplicate.md): Copy a track (source or translation) to a new translation track.
    - [`tracks rename`](transcriber-tracks-rename.md): Change the language code or title of a track ('source' renames the source title).
    - [`tracks remove`](transcriber-tracks-remove.md): Delete a translation track (asks first; --yes skips).
    - [`tracks fixed-text`](transcriber-tracks-fixed-text.md): Show, set or clear the fixed (reference) text of a translation track.
- [`colors`](transcriber-colors.md): Word Colors: the palette, automatic rules and manual marks on words.
    - [`colors palette`](transcriber-colors-palette.md): List and edit the palette.
    - [`colors rules`](transcriber-colors-rules.md): Automatic rules: a word or phrase always gets a color.
    - [`colors marks`](transcriber-colors-marks.md): Manual marks: one word of one subtitle gets a color (documents only).
- [`dictionaries`](transcriber-dictionaries.md): Search-and-replace dictionaries: list, edit, import/export, use in documents.
    - [`dictionaries list`](transcriber-dictionaries-list.md): List the dictionaries.
    - [`dictionaries show`](transcriber-dictionaries-show.md): Show a dictionary's items and prompt.
    - [`dictionaries create`](transcriber-dictionaries-create.md): Create a dictionary.
    - [`dictionaries edit`](transcriber-dictionaries-edit.md): Change a dictionary's description, prompt or favorite flag.
    - [`dictionaries rename`](transcriber-dictionaries-rename.md): Rename a dictionary.
    - [`dictionaries delete`](transcriber-dictionaries-delete.md): Delete a dictionary (asks first; --yes skips).
    - [`dictionaries import`](transcriber-dictionaries-import.md): Import a dictionary file (.TrDict, as exported by the app or 'dictionaries export').
    - [`dictionaries export`](transcriber-dictionaries-export.md): Write a dictionary to a .TrDict file (JSON; the app can import it).
    - [`dictionaries add-item`](transcriber-dictionaries-add-item.md): Add a replacement: texts to find → replacement.
    - [`dictionaries remove-item`](transcriber-dictionaries-remove-item.md): Remove an item (by number or id; see 'dictionaries show').
    - [`dictionaries use`](transcriber-dictionaries-use.md): Make a document apply dictionaries after transcription (and send their prompts to Whisper).
    - [`dictionaries unuse`](transcriber-dictionaries-unuse.md): Stop a document from using dictionaries ('all' = every one).
    - [`dictionaries apply`](transcriber-dictionaries-apply.md): Run dictionaries' replacements on a document's subtitles now.
- [`doc`](transcriber-doc.md): The document: new, source, segment, start timecode, contexts, settings, migrate.
    - [`doc new`](transcriber-doc-new.md): Create an empty document (optionally with its source media), without transcribing.
    - [`doc source`](transcriber-doc-source.md): Show or change the source media (relink a moved file) and the source track title.
    - [`doc segment`](transcriber-doc-segment.md): Show or set the In/Out segment to transcribe (licensed copies).
    - [`doc tc-start`](transcriber-doc-tc-start.md): Show or override the start timecode used by exports (e.g. 01:00:00:00).
    - [`doc contexts`](transcriber-doc-contexts.md): Show or choose the Global Contexts a document's AI correction uses.
    - [`doc settings`](transcriber-doc-settings.md): A document's own settings: show, set, unset, apply, diff.
    - [`doc migrate`](transcriber-doc-migrate.md): Rewrite a document in the current file format (older documents are read fine; this saves them upgraded).
- [`translate`](transcriber-translate.md): Translate a document's subtitles with DeepL into new translation tracks.
    - [`translate run`](transcriber-translate-run.md): Translate into one or more languages (one new track each).
    - [`translate languages`](transcriber-translate-languages.md): List DeepL's target languages (codes for --to).
- [`ai`](transcriber-ai.md): AI correction, punctuation, review of AI edits, questions and metadata.
    - [`ai correct`](transcriber-ai-correct.md): Semantic correction: fix misheard words using the text and the global contexts.
    - [`ai punctuate`](transcriber-ai-punctuate.md): Add strong punctuation (full stops) to long run-on sentences of the source track.
    - [`ai diff`](transcriber-ai-diff.md): Show the subtitles changed by the AI: previous text and new text.
    - [`ai review`](transcriber-ai-review.md): Review the AI changes one by one: accept, reject or edit each (interactive).
    - [`ai accept`](transcriber-ai-accept.md): Accept AI changes: keep the new text and forget the previous one.
    - [`ai reject`](transcriber-ai-reject.md): Reject AI changes: restore the previous text.
    - [`ai ask`](transcriber-ai-ask.md): Ask the AI a question about the transcript; the answer goes to stdout.
    - [`ai metadata`](transcriber-ai-metadata.md): AI metadata: run library prompts (summaries, titles, chapters…) on a document.
    - [`ai providers`](transcriber-ai-providers.md): List the AI providers, the selected one, and where each key comes from.
    - [`ai models`](transcriber-ai-models.md): List the text models of a provider (ids for --model).
- [`align`](transcriber-align.md): Align an official text onto the subtitles (forced alignment): same timing, official words.
- [`contexts`](transcriber-contexts.md): The Global Contexts library: terms, names and facts the AI correction knows.
    - [`contexts list`](transcriber-contexts-list.md): List the contexts: number, format, language, tokens, enabled.
    - [`contexts show`](transcriber-contexts-show.md): Print a context's content on stdout (--info for its details instead).
    - [`contexts create`](transcriber-contexts-create.md): Create a context, empty or from a file / stdin.
    - [`contexts import`](transcriber-contexts-import.md): Import files as new contexts (name from the file name).
    - [`contexts export`](transcriber-contexts-export.md): Write a context's content to a file (default: <name>.<format>).
    - [`contexts set-content`](transcriber-contexts-set-content.md): Replace a context's content with a file or stdin.
    - [`contexts add-entity`](transcriber-contexts-add-entity.md): Add an entity to a YAML context (or more sounds-like variants to an existing one).
    - [`contexts rename`](transcriber-contexts-rename.md): Rename a context.
    - [`contexts duplicate`](transcriber-contexts-duplicate.md): Duplicate a context ("<name> Copy", or --name).
    - [`contexts delete`](transcriber-contexts-delete.md): Delete contexts (their files go to the Trash; asks first, --yes skips).
    - [`contexts enable`](transcriber-contexts-enable.md): Enable contexts by default for new documents.
    - [`contexts disable`](transcriber-contexts-disable.md): Disable contexts by default for new documents.
    - [`contexts language`](transcriber-contexts-language.md): Set a context's reference language (BCP-47 such as it-IT, or 'auto').
    - [`contexts convert`](transcriber-contexts-convert.md): Change a context's declared format (the content is kept as it is).
    - [`contexts tokens`](transcriber-contexts-tokens.md): Estimated tokens of contexts, against the AI model's budget.
    - [`contexts validate`](transcriber-contexts-validate.md): Check that YAML contexts parse and list entities.
    - [`contexts structure`](transcriber-contexts-structure.md): AI: turn a free-text context (notes, Markdown, a list) into a YAML entity list.
    - [`contexts enrich`](transcriber-contexts-enrich.md): AI: add sounds-like variants (how speech recognition mishears them) to a YAML context.
    - [`contexts extract`](transcriber-contexts-extract.md): AI: extract the names and terms spoken in a document into a YAML context.
    - [`contexts path`](transcriber-contexts-path.md): Print the folder of the Global Contexts library.
- [`timeline`](transcriber-timeline.md): Text-based editing: timelines of sentences, marks, chapters, FCPXML export, AI selection.
    - [`timeline list`](transcriber-timeline-list.md): List the timelines: sentences, marked, chapters, duration.
    - [`timeline show`](transcriber-timeline-show.md): Show a timeline's sentences: number, state, timecodes, text.
    - [`timeline new`](transcriber-timeline-new.md): Create a timeline with every sentence of the transcription (or empty).
    - [`timeline from-marked`](transcriber-timeline-from-marked.md): Create a timeline from the marked sentences of another.
    - [`timeline rename`](transcriber-timeline-rename.md): Rename a timeline (and/or set its description).
    - [`timeline duplicate`](transcriber-timeline-duplicate.md): Duplicate a timeline ("<name> Copy", or --name).
    - [`timeline delete`](transcriber-timeline-delete.md): Delete timelines (asks first; --yes skips).
    - [`timeline select`](transcriber-timeline-select.md): Make a timeline the selected one (the default for the other commands and the app).
    - [`timeline mark`](transcriber-timeline-mark.md): Mark sentences (the selects: 'from-marked' and 'disable --unmarked' use them).
    - [`timeline unmark`](transcriber-timeline-unmark.md): Unmark sentences.
    - [`timeline enable`](transcriber-timeline-enable.md): Enable sentences or chapters (they are part of the edit).
    - [`timeline disable`](transcriber-timeline-disable.md): Disable sentences or chapters (left out of the edit, kept in the timeline).
    - [`timeline drop`](transcriber-timeline-drop.md): Remove sentences or chapters from a timeline (the transcription is untouched).
    - [`timeline sort`](transcriber-timeline-sort.md): Sort a timeline's sentences by time (chapters move with their first sentence's time).
    - [`timeline chapter`](transcriber-timeline-chapter.md): Chapters in a timeline: add, rename, remove (export as titles in the FCPXML).
    - [`timeline export`](transcriber-timeline-export.md): Export a timeline: FCPXML edit, text, text with timecodes, RTF, JSON or CSV.
    - [`timeline ai`](transcriber-timeline-ai.md): AI on a timeline: context, adherence rating, filtered and summarized cuts, chapters.
- [`batch`](transcriber-batch.md): Transcribe many files: now (run, N at a time) or through the app's batch queue.
    - [`batch run`](transcriber-batch-run.md): Transcribe files and folders now, N at a time, with a final report.
    - [`batch queue`](transcriber-batch-queue.md): The app's batch queue (Batch window): list, add, remove, clear, run.
- [`concat`](transcriber-concat.md): Join several audio or video files into one (to transcribe them as one).
- [`shell`](transcriber-shell.md): Interactive shell on one document: run commands without naming it, undo, save.
- [`mcp`](transcriber-mcp.md): Model Context Protocol server: Transcriber's commands as tools for AI assistants.
    - [`mcp serve`](transcriber-mcp-serve.md): Run the MCP server on stdin/stdout (started by the MCP client).
    - [`mcp tools`](transcriber-mcp-tools.md): List the MCP tools, or show one tool's definition and input schema.
    - [`mcp config`](transcriber-mcp-config.md): Print the configuration that adds this MCP server to a client.
- [`open`](transcriber-open.md): Open documents or media in the Transcriber app, or show them in the Finder.
- [`settings`](transcriber-settings.md): The app's settings (shared with the app): get, set, list, import, export, diff.
    - [`settings list`](transcriber-settings-list.md): Show the settings (all, or one section) as YAML.
    - [`settings get`](transcriber-settings-get.md): Print one setting's value.
    - [`settings set`](transcriber-settings-set.md): Change app settings: key=value pairs.
    - [`settings unset`](transcriber-settings-unset.md): Put settings back to their factory value (a key or a whole section).
    - [`settings keys`](transcriber-settings-keys.md): List every settings key with its type and current value.
    - [`settings reset`](transcriber-settings-reset.md): Put every app setting back to the factory defaults (asks first; --yes skips).
    - [`settings import`](transcriber-settings-import.md): Merge a settings file (YAML or JSON, all or some keys) into the app settings.
    - [`settings export`](transcriber-settings-export.md): Write the settings to a file (YAML or JSON) usable with --config and 'settings import'.
    - [`settings diff`](transcriber-settings-diff.md): Compare two sets of settings.
    - [`settings path`](transcriber-settings-path.md): Print where the app settings are stored.
- [`preset`](transcriber-preset.md): Named settings presets (shared with the app): list, save, apply, import, export.
    - [`preset list`](transcriber-preset-list.md): List the presets, newest first.
    - [`preset show`](transcriber-preset-show.md): Show a preset's settings (by default those that differ from the factory defaults).
    - [`preset save`](transcriber-preset-save.md): Save settings as a preset (replaces one with the same name).
    - [`preset apply`](transcriber-preset-apply.md): Apply a preset to the app settings (--app) or to a document's settings.
    - [`preset rename`](transcriber-preset-rename.md): Rename a preset.
    - [`preset delete`](transcriber-preset-delete.md): Delete a preset (asks first; --yes skips).
    - [`preset import`](transcriber-preset-import.md): Import a preset: a file from 'preset export', or any settings file (with --name).
    - [`preset export`](transcriber-preset-export.md): Write a preset to a JSON file (its changed settings), for 'preset import' on another Mac.
- [`models`](transcriber-models.md): List, download and remove the Whisper models.
    - [`models list`](transcriber-models-list.md): List the models, their size and whether they are installed.
    - [`models download`](transcriber-models-download.md): Download models (resumes nothing: a failed download starts over).
    - [`models remove`](transcriber-models-remove.md): Delete downloaded models to free disk space (asks first; --yes skips).
    - [`models path`](transcriber-models-path.md): Print the folder of the models (or the file of one model).
- [`keys`](transcriber-keys.md): Manage the API keys of the AI providers and DeepL.
    - [`keys list`](transcriber-keys-list.md): Show which providers have a key, and where it comes from (keys are masked).
    - [`keys set`](transcriber-keys-set.md): Store a provider's key (read from stdin or prompted; never an argument).
    - [`keys remove`](transcriber-keys-remove.md): Delete a provider's stored key (asks first; --yes skips).
    - [`keys test`](transcriber-keys-test.md): Check keys with a tiny request to the provider (costs a few tokens).
    - [`keys authorize`](transcriber-keys-authorize.md): Let the command line read the AI keys stored by the app (macOS asks once per key).
- [`license`](transcriber-license.md): Show the licence state (FxFactory) or open FxFactory to buy / unlock.
    - [`license status`](transcriber-license-status.md): Show whether this copy is licensed.
    - [`license unlock`](transcriber-license-unlock.md): Open FxFactory on Transcriber's page to buy or unlock it.
- [`doctor`](transcriber-doctor.md): Check the installation: licence, models, keys, settings, PATH, disk space.
- [`docs`](transcriber-docs.md): Generate the manual (man pages, Markdown, HTML) from the commands.
    - [`docs generate`](transcriber-docs-generate.md): Write the manual as man pages, Markdown files and/or an HTML site.
    - [`docs show`](transcriber-docs-show.md): Print the manual page of a command as Markdown.
