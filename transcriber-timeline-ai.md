# transcriber timeline ai

AI on a timeline: context, adherence rating, filtered and summarized cuts, chapters.

## Synopsis

```
transcriber timeline ai <command> [options]
```

## Description

```
context    describe what the timeline is about (stored; --text writes your
           own)
rate       rate each sentence's adherence to the context: much, little, zero
filter     new timeline with the marked sentences and those rated 'much' (no
           AI)
summarize  new timeline of the sentences that best tell the context
chapters   split the timeline into titled chapters
```

Typical: context → rate → filter → summarize → chapters.

## Commands

- [`context`](transcriber-timeline-ai-context.md): Generate (AI), show or set a timeline's context: what it is about.
- [`rate`](transcriber-timeline-ai-rate.md): AI: rate each sentence's adherence to the timeline context (much, little, zero).
- [`filter`](transcriber-timeline-ai-filter.md): New timeline with the marked sentences and those rated 'much' (no AI call).
- [`summarize`](transcriber-timeline-ai-summarize.md): AI: new timeline of the sentences that best tell the timeline context.
- [`chapters`](transcriber-timeline-ai-chapters.md): AI: split a timeline into titled chapters (replaces its chapters).

## See also

- [transcriber timeline](transcriber-timeline.md)
- [Output, JSON and exit codes](output.md)
