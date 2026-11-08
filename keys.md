# API keys

AI correction, translation, alignment, metadata and timelines call a provider: OpenAI, Gemini, Anthropic, DeepSeek, Magnific, DeepL, or the on-device model (`local`, no key). A command looks for the key in this order:

- `--api-key-file <path>` (`-` reads the key from stdin);
- the environment: `TRANSCRIBER_<PROVIDER>_API_KEY`, then the vendor's usual name (`OPENAI_API_KEY`, `GEMINI_API_KEY` or `GOOGLE_API_KEY`, `ANTHROPIC_API_KEY`, `DEEPSEEK_API_KEY`, `DEEPL_API_KEY`…);
- the key stored by the app (Keychain; DeepL's in the app's settings).

A key is never taken from an argument that would show in the process list, and is never printed in full: `keys list` masks it and tells where it comes from.

## Commands

- `keys list`: which providers have a key, and from where.
- `keys set <provider>`: store a key (read from stdin or prompted).
- `keys remove <provider>`: delete the stored key.
- `keys test`: a tiny request to each provider (costs a few tokens).
- `keys authorize`: the Keychain asks, once per key, whether the command may read the keys the app stored. Run it once in Terminal and choose **Always Allow**.

Without an authorization the command does not read the app's Keychain items on its own: it reports that a key needs approval instead of showing a dialog in the middle of a script.