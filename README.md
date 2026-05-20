# Weekend_Project_Batman_AI

<div align="center">

<img src="bat-logo.png" alt="Batman Oracle Logo" width="120" />

# 🦇 Batman — The Dark Knight Oracle

**An AI that doesn't just quote Batman. It thinks like him.**

*Built in a weekend by an embedded systems developer stepping into AI for the first time.*

[![Made with Groq](https://img.shields.io/badge/AI-Groq%20LLaMA%203-orange?style=flat-square)](https://groq.com)
[![Voice by Whisper](https://img.shields.io/badge/Voice%20Input-Whisper%20AI-yellow?style=flat-square)](https://groq.com)
[![TTS ElevenLabs](https://img.shields.io/badge/TTS-ElevenLabs-black?style=flat-square)](https://elevenlabs.io)
[![Vanilla JS](https://img.shields.io/badge/Frontend-Vanilla%20JS-blue?style=flat-square)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![License MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

</div>

---

## ⭐ Before You Use This

> **You need your own API keys to run this project.**
> The keys in the code are personal and will not work for you.
> Follow the setup section below to add yours — it takes 2 minutes and both services have free tiers.

---

## 📖 What Is This?

The Batman Dark Knight Oracle is a character-accurate AI chatbot trained to respond **exactly** like Batman — not as a quote machine, but using the real conversational rhythm of the *Batman Told Me This* reel series.

Most Batman AI bots throw a polished one-liner on the first message and go silent. That's not how the reels work. In the reels, Batman *earns* the punch line — short cold answer first, then deeper as you push, then the line that lands.

This project replicates that rhythm through careful prompt engineering across four canonical sources:

| Source | Voice |
|---|---|
| Nolan Trilogy (Christian Bale) | Exhausted certainty, gravelly restraint |
| Batman: The Animated Series (Kevin Conroy) | Cold, precise, detective logic |
| Frank Miller Comics | Raw, poetic inner monologue |
| *Batman Told Me This* Reels | Short devastating Q&A build-up |

---

## ✨ Features

- 🎙️ **Voice input** — speak directly using Groq Whisper AI transcription
- 🔊 **Cinematic voice output** — ElevenLabs TTS with a deep Batman-style voice
- ⌨️ **Typewriter effect** — responses type out character by character with dramatic pauses
- 🌧️ **Gotham rain** — toggleable rain canvas overlay
- ✨ **Particle atmosphere** — animated gold particles floating in the background
- 💬 **Conversation memory** — Batman remembers the full thread and builds on it
- 📊 **Session sidebar** — live message counter, session timer, knowledge source indicators
- 💡 **Prompt chips** — one-tap starter questions on the welcome screen
- 🔥 **Burn Protocol** — clears chat with a glitch animation
- 📱 **Fully responsive** — works on mobile and desktop

---

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/YOUR_USERNAME/batman-oracle.git
cd batman-oracle
```

### 2. Get your API keys

**Groq (Required — AI brain + voice input)**
- Go to [console.groq.com](https://console.groq.com)
- Create a free account
- Generate an API key
- Free tier is generous — more than enough for personal use

**ElevenLabs (Optional — cinematic voice output)**
- Go to [elevenlabs.io](https://elevenlabs.io)
- Create a free account
- Copy your API key from the profile settings
- Without this, it falls back to a browser TTS voice

### 3. Add your keys

Open `app.js` and find line 7:

```js
let GROQ_KEY = localStorage.getItem("gotham_groq") || "YOUR_GROQ_KEY_HERE";
let ELEVEN_KEY = localStorage.getItem("gotham_eleven") || "YOUR_ELEVENLABS_KEY_HERE";
```

Replace the placeholder strings with your actual keys.

**Or** — just open the app in your browser, click the ⚙️ settings icon, and paste your keys there. They get saved to your browser's localStorage automatically.

### 4. Run it

No build step. No npm install. Just open `index.html` in your browser.

```bash
# If you want a local server (recommended for mic access)
npx serve .
# or
python3 -m http.server 8080
```

Then open `http://localhost:8080`

> **Note:** Microphone access requires either `localhost` or `https`. Opening the file directly (`file://`) may block mic permissions in some browsers.

---

## 🗂️ Project Structure

```
batman-oracle/
├── index.html       # Full UI layout — sidebar, chat, controls
├── style.css        # Cinematic dark theme — all styling
├── app.js           # AI logic, prompt, voice, conversation memory
├── bat-logo.png     # Batman logo (bring your own)
└── nirvana.mp3      # Background music (bring your own)
```

---

## 🧠 How the Prompt Works

The hardest part of this project wasn't the UI. It was making the AI *not* behave like a quote machine.

The prompt is engineered around 6 extracted speech patterns from the real reels:

| Pattern | Trigger | Example |
|---|---|---|
| **"Good."** opener | They express fear or doubt | *"My dreams scare me"* → *"Good. If they don't scare you, they aren't big enough."* |
| **The Statistic** | They're failing or suffering | *"80% of this is losing. Most people quit inside that 80%."* |
| **Nobody Cares** | They want sympathy | *"Nobody cares if you're tired. Nobody cares if you're hurt."* |
| **The Redirect** | They ask how to fix a feeling | *"You don't fight the feeling. You move anyway."* |
| **The Proof** | They doubt their worth | *"Because you're still dreaming it."* |
| **One-Line Closer** | End of a thread | *"You will, if you don't stop."* |

The conversation rhythm: short cold opener → deeper on follow-up → devastating closer. The best line comes last, not first.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| AI Model | Groq LLaMA 3.3 70B |
| Voice Input | Groq Whisper Large v3 |
| Voice Output | ElevenLabs Multilingual v2 |
| Fallback TTS | StreamElements Brian |
| Frontend | Vanilla HTML / CSS / JS |
| Fonts | Cinzel, Oswald, Special Elite |
| Markdown | marked.js |

---

## 💡 Inspiration

This project started after watching the *Batman Told Me This* reel series — short motivational Q&As in Batman's voice. I wanted to be able to have that conversation live, not just watch it.

I'm primarily an embedded systems developer — C, hardware, microcontrollers. This was my first real step into AI integration and frontend development. It's not perfect. It's not finished. But it works, and it taught me a lot.

This is a small step toward understanding how AI and hardware can eventually come together — which is where I want to go next.

---

## 📌 Known Limitations

- Requires internet connection (Groq + ElevenLabs are cloud APIs)
- Mic input needs `localhost` or `https` — won't work on bare `file://`
- No persistent chat history across sessions yet
- `bat-logo.png` and `nirvana.mp3` not included — add your own

---

## 🤝 Contributing

This is a personal learning project but PRs and ideas are welcome. If you improve the prompt, the UI, or add offline support via Ollama — open a PR.

---

## 📄 License

MIT — use it, fork it, build on it. Just don't sell it as your own.

---

<div align="center">

*"It's not who I am underneath — what I do defines me."*

**Built with curiosity. Shipped in a weekend.**

</div>
