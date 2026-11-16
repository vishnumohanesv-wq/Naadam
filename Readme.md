# NAADAM (നാദം)

> **"Feel Every Beat. Hear Every Language."**  
> A lightweight, zero-dependency Progressive Web App (PWA) built for South Indian and multi-language live radio, song previews, and multilingual voice assistance.

---

## 🌟 Overview

**NAADAM** is a self-contained, single-file web application designed for effortless playback of South Indian (Malayalam, Tamil, Kannada, Telugu) as well as Hindi and English live radio stations and music previews. Built with a glassmorphism UI inspired by classic brass and emerald aesthetics, it runs entirely client-side with zero ads, offline state persistence, and native OS media integration.

---

## ✨ Key Features

- **Multilingual UI & Regional Hubs:** Full interface localization and dedicated station hubs for **Malayalam (മലയാളം)**, **Tamil (தமிழ்)**, **Kannada (ಕನ್ನಡ)**, **Telugu (తెలుగు)**, **Hindi (हिन्दी)**, and **English**.
- **Live Radio & All India Radio (AIR):** Instant access to regional FM hits, retro melodies, devotional channels, and AIR stations powered by the Radio-Browser directory with built-in fallback streams.
- **Song Discovery & Previews:** Search tracks, artists, and albums via the iTunes Search API with 30-second audio previews and one-tap links to open full tracks in YouTube Music.
- **NAADAM Voice Assistant:** Tap-to-talk multilingual voice control supporting regional languages for playback, volume adjustment, sleep timers, language switching, and station searches.
- **Immersive Now Playing Sheet:** Features a spinning vinyl disc animation, decorative audio visualizer, queue management ("Up Next"), and quick song title bookmarking while listening to live radio.
- **Library & Local JSON Backup:** Save favourite stations, liked songs, and listening history locally in `localStorage`, complete with one-click JSON export and restore.
- **Custom Stream Support:** Add your own radio stream URLs (`.mp3`, `.aac`, `.m3u8`) and share station links directly via URL hashes.
- **Data Saver & Sleep Timer:** Reduce bandwidth by limiting directory payloads and remote artwork, or set an automatic playback shutoff timer (15 to 90 minutes).
- **Adaptive Themes & PWA Ready:** Seamless Dark and Light modes, responsive desktop sidebar / mobile bottom navigation, `MediaSession` lock-screen controls, and installable PWA manifest.

---

## 🛠️ Technology Stack

- **Core:** Semantic HTML5, Vanilla ES6+ JavaScript (Single-File Architecture)
- **Styling:** Tailwind CSS (CDN), Custom CSS Variables, Google Fonts (`Cinzel`, `Playfair Display`, `Inter`, and Noto Sans Indic scripts)
- **Audio & Streaming:** HTML5 `<audio>` + [HLS.js](https://github.com/video-dev/hls.js/) for `.m3u8` adaptive streaming
- **External APIs:**
  - [Radio-Browser API](https://www.radio-browser.info/) — Live global & regional radio directory
  - [iTunes Search API](https://developer.apple.com/library/archive/documentation/AudioVideo/Conceptual/iTuneSearchAPI/) — Track metadata and 30-second audio previews
  - Web Speech API (`SpeechRecognition` & `SpeechSynthesis`) — On-device voice commands and spoken feedback
  - Media Session API — Hardware media keys and lock-screen player controls

---

## 🚀 Getting Started

Because NAADAM is built as a single-file monolith (`Naadam (1).html`), there are no build tools, bundlers, or `node_modules` required.

### Running Locally
1. Download `Naadam (1).html` (optionally rename it to `index.html`).
2. Serve it over a local HTTP server (recommended so HTTPS/HTTP stream playback, Service Worker registration, and Web Speech API permissions work properly):
   ```bash
   # Using Python
   python3 -m http.server 8080

   # Or using Node.js
   npx serve .
   ```
3. Open `http://localhost:8080` in any modern web browser.

### Installing as an App (PWA)
1. Open the hosted app in Chrome, Edge, or Safari.
2. Navigate to the **Library** tab and click **Install app**, or use your browser's **"Add to Home Screen"** / **"Install"** option.

---

## 🎙️ Voice Assistant Commands

Tap the center **Microphone** button in the navigation bar and try speaking (or typing) commands in English or supported Indian languages:

| Action | Example Commands |
| :--- | :--- |
| **Play Songs / Artists** | *"Play Yesudas songs"*, *"Search A R Rahman"* |
| **Switch Radio Hub** | *"Tamil radio"*, *"Play Malayalam FM"* |
| **Playback Control** | *"Pause"*, *"Stop"*, *"Next"*, *"Previous"* |
| **Volume Control** | *"Volume up"*, *"Volume down"*, *"Volume 60"*, *"Mute"* |
| **Sleep Timer** | *"Sleep timer 30 minutes"*, *"Sleep timer off"* |
| **Favourites & Language** | *"Add to favourites"*, *"Change language to Hindi"* |

---

## 📁 Project Structure

```text
├── index.html   # Complete single-file application (HTML, CSS, JS, Manifest)
└── sw.js        # Optional Service Worker for offline asset caching
```

---

## 📄 License

This project is open-source and available for personal and educational use.
