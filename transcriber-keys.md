# transcriber keys

Manage the API keys of the AI providers and DeepL.

## Synopsis

```
transcriber keys <command> [options]
```

## Description

AI keys live in the Keychain, shared with the app; the DeepL key in the app's settings. Commands use, in order: --api-key / --api-key-file, the environment (TRANSCRIBER_<PROVIDER>_API_KEY, then OPENAI_API_KEY, GEMINI_API_KEY, ANTHROPIC_API_KEY, DEEPSEEK_API_KEY, DEEPL_API_KEY…), then the stored key.

## Commands

- [`list`](transcriber-keys-list.md): Show which providers have a key, and where it comes from (keys are masked).
- [`set`](transcriber-keys-set.md): Store a provider's key (read from stdin or prompted; never an argument).
- [`remove`](transcriber-keys-remove.md): Delete a provider's stored key (asks first; --yes skips).
- [`test`](transcriber-keys-test.md): Check keys with a tiny request to the provider (costs a few tokens).
- [`authorize`](transcriber-keys-authorize.md): Let the command line read the AI keys stored by the app (macOS asks once per key).

## See also

- [transcriber](transcriber.md)
- [Output, JSON and exit codes](output.md)
