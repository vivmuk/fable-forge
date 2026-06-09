# The Fable Forge

A 5-chapter interactive game that teaches the capabilities of **Anthropic's Claude Fable 5** (via Venice API) by making you play through them.

Each chamber is engineered around one of Fable 5's signature traits:

| Chamber | Trait | How it's taught |
|---|---|---|
| I — The Long Memory | 1,000,000-token context | The keeper brings back something you said many turns ago |
| II — The Riddle of the Forge | Always-on adaptive thinking | A riddle that requires you to reason out loud |
| III — The Eye of Fable | Multimodal vision (10 images) | Upload a sigil; the seer reads it |
| IV — The Long Telling | 128,000-token output | Ask the chronicler to write a saga in one breath |
| V — The Apprentice | Agentic tool use | Give the apprentice multi-step instructions |

A live telemetry HUD shows context window filling, thinking tokens spent, images read, output length, and tools invoked — so you can *see* the model's capabilities at work.

## Setup

1. Get a Venice API key at https://venice.ai
2. Open the app, click the ⚙ icon in the header, paste your key
3. The key is stored only in your browser's localStorage and sent directly to `api.venice.ai` — no backend proxy

The first chamber is a free preview — you can read the intro and the system prompts for all 5 chambers before deciding to spend any API credits.

## Cost

Fable 5 pricing on Venice: $12/M input, $60/M output, $1.20/M cached input. A full 5-chapter playthrough uses roughly 30k input + 15k output tokens ≈ **$1.30 per game** (mostly from chapter 4's 12k-token saga). The first 2-3 chapters cost fractions of a cent.

## Tech

- Single HTML file, zero build step
- Pure client-side; no backend
- Streaming SSE for live thinking + content
- Dark forge aesthetic (Cormorant Garamond + Inter Tight + JetBrains Mono)

## Files

- `index.html` — the whole game
