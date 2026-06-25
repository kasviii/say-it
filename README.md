# Say It

Record a voice memo. It gets transcribed, then split into tasks, calendar events, and notes — yours to confirm or toss.

**Live demo:** https://kasviii.github.io/say-it/

## How it works

1. Hit record and talk.
2. [Groq Whisper](https://console.groq.com) transcribes the audio.
3. Llama 3.3 (also via Groq) reads the transcript and pulls out actionable items, tagging each as a **task**, **event** (with date/time), or **note**.
4. Each item shows up as an editable card — fix the text, change the type, then confirm or discard it.
5. Play back the original recording next to its transcript anytime.

## Setup

No build step, no backend — it's a single HTML file.

1. Open `index.html` in a browser.
2. Paste in a free Groq API key ([get one here](https://console.groq.com/keys)) — it's saved to your browser's `localStorage` and never leaves your machine except to call Groq.
3. Start recording.

## Notes

- Needs microphone access, so use `https://` or `localhost` (or just open the file directly — most browsers allow mic access for local files too).
- Transcripts and extracted items live in memory only — refreshing the page clears them. The API key is the only thing that persists.
- Built entirely with vanilla HTML/CSS/JS.
