---
name: Deepdub TTS
description: Generate speech audio using Deepdub and attach it as a MEDIA file (Telegram-compatible).
version: 0.1.0
tags: [tts, deepdub, audio, telegram]
---

## What this skill does
This skill converts text into speech using Deepdub and returns an audio file
as a `MEDIA:` attachment that OpenClaw can send to channels like Telegram.

## Requirements
- Python 3.9+
- Deepdub API access

### Permissions
This skill requires permission to:
- Execute `deepdub_tts.py` (the bundled script)
- Write audio files to `OPENCLAW_MEDIA_DIR` only

## Setup
Set the following environment variables where OpenClaw runs:

Required:
- `DEEPDUB_API_KEY` – your Deepdub API key
- `DEEPDUB_VOICE_PROMPT_ID` – default voice prompt to use

Optional:
- `DEEPDUB_LOCALE` (default: `en-US`)
- `DEEPDUB_MODEL`
- `OPENCLAW_MEDIA_DIR` (default: `/tmp/openclaw_media`)

### Free Trial Key
For testing, you can use this free trial API key:
```
DEEPDUB_API_KEY=dd-00000000000000000000000065c9cbfe
```

## Install dependency

```bash
# Using uv (recommended)
uv pip install deepdub

# Or using pip
pip install deepdub
```
