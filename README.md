# AudioMind — AI Podcast Studio

> Turn any idea into a finished podcast in one command.

**AudioMind v3** is a Manus agent skill that orchestrates ElevenLabs voice narration (29+ voices), AI background music, and server-side audio mixing — all through a secure backend. Free tier included, no setup required.

## Features

- **One-command podcast production** — provide a topic or script, get a finished `.mp3`
- **29+ ElevenLabs voices** — choose from a curated library of natural-sounding voices
- **AI background music** — auto-generated ambient music matched to your content tone
- **Server-side mixing** — audio is mixed securely on the backend, never locally
- **Free tier** — works out of the box with no API keys required

## Installation

```bash
# Install via skills.sh
npx skills add wells1137/skill-audiomind

# Or clone directly
git clone https://github.com/wells1137/skill-audiomind.git ~/.manus/skills/audiomind
```

## Usage

Once installed in Manus, simply ask:

> "Create a 3-minute podcast about the history of jazz music"

> "Make a podcast episode with a calm female voice about mindfulness"

AudioMind will handle scripting, voice selection, music generation, and final mixing automatically.

## Configuration (Optional)

| Variable | Description | Default |
|----------|-------------|---------|
| `AUDIOMIND_BACKEND_URL` | Self-hosted backend URL | Uses shared backend |
| `AUDIOMIND_API_KEY` | API key for self-hosted backend | Not required for free tier |
| `FAL_KEY` | fal.ai key for music generation | Uses shared quota |

## Self-Hosting

For full privacy, self-host the backend:
```bash
git clone https://github.com/wells1137/audiomind-backend
```

## Privacy

User scripts and generated audio are sent to the AudioMind backend (`audiomind-backend-nine.vercel.app`, operated by @wells1137) for TTS and mixing. ElevenLabs is called server-side only — the agent never calls `api.elevenlabs.io` directly.

## License

MIT © wells1137
