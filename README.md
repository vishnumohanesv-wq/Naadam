# NAADAM · നാദം

**Live South Indian radio, songs and a focus timer in one file.**

Naadam plays live Malayalam, Tamil, Kannada, Telugu, Hindi and English radio, searches songs, saves your favourites, and works like an app on your phone. Everything is in a single file, `naadam-pro.html`. There is nothing to install or build.

---

## Quick start

1. **Rename** `naadam-pro.html` to `index.html`.
2. **Host it** (free, about 2 minutes):
   - **Netlify Drop:** open `app.netlify.com/drop` and drag `index.html` onto the page. You get an HTTPS link right away.
   - **GitHub Pages:** create a repository, upload `index.html`, then go to *Settings → Pages* and deploy from the `main` branch.
3. **Open the link in Chrome** on your phone.
4. **Install it:** Android Chrome → ⋮ menu → *Add to Home screen* (or *Install app*). iPhone Safari → Share → *Add to Home Screen*.

> **Do not open the file straight from WhatsApp or file storage.** Those viewers are limited. Install does not work there, and some features are restricted. Always open it from a web link.

---

## What you get

### Radio
- **Six languages of radio:** Malayalam, Tamil, Kannada, Telugu, Hindi and English. Switch with the language chips at the top.
- **A live station directory.** Stations come from the free [Radio Browser](https://www.radio-browser.info) directory, so stream links stay up to date. Each language loads up to about 500 stations.
- **A hand-picked list of well-known stations** (Club FM, Radio Mango, Red FM, Radio Mirchi, Radio City, All India Radio city stations, community radios, devotional stations and more). Each name is matched to a working link in the live directory. If no working link is found, that station stays hidden, so you never see a dead entry.
- **Filters:** categories (FM & Hits, All India Radio, Retro & Melodies, Devotional/News, Focus & Work), 📍 city chips (Kochi, Chennai and so on) and # tag chips (news, devotional, retro and so on).
- **Sort** by Popular, A–Z or Best quality. Each row shows the bitrate, for example `128k`.
- **Search everywhere:** if your search finds nothing, one button searches the whole Radio Browser directory.
- **Favourites, your own stations, recently played, and a Surprise me button.**
- **Focus & Work:** calm ambient stations plus a work and break timer.

### Songs
- **Song search:** search any Malayalam, Tamil, Kannada, Telugu, Hindi or English song, artist or album.
- **Browse by artist** (about 30 each for Malayalam and Tamil), by mood (Love, Sad, Dance, Workout, Rain, Wedding, Lo-fi, Mass & BGM and more), or by devotional theme.
- **Play all and Shuffle,** plus an era filter (2020s, 2010s, 2000s, 90s and older). Each song shows its release year.
- **Liked songs** and **recent searches** are saved on your device.
- Songs play as **30-second previews**. The arrow icon on each song opens the full song in YouTube Music.

### Focus & Work timer
- Pick 25/5, 50/10 or 90/20 minutes of work and break.
- It plays calm radio, shows a countdown pill, and plays a soft chime when each phase ends.
- Start it from **Home → Browse → Focus Timer**, from the **Library**, by pressing **F**, or by voice ("start focus 25").

### Voice assistant
Tap the mic button and speak. Examples:
- “Play Yesudas songs”
- “Pause”, “Volume up”
- “Tamil radio”
- “Sleep timer 30”
- “Change language to Hindi”
- “Start focus 25”

Voice works in the browsers that support speech recognition (Chrome on Android and desktop).

### Two views
- **Mobile view:** a phone layout with a bottom navigation bar.
- **System view:** a laptop layout with a side menu.
- The app picks one automatically. You can switch any time with the 📱 / 🖥️ button in the top bar.

### Easy to use
- **Back button:** a ‹ arrow appears whenever you are not on Home. The phone's own back gesture works too. It closes the player or a menu first, then goes back one screen at a time. On the first screen it asks you to press back again to exit.
- **Compact layout and Lite effects:** these turn on automatically on phones so the app is small and smooth. Change them in **Library** or in the Help card (press **?**).
- **Six colour palettes:** Sunset, Kerala, Ocean, Mint, Violet and Rose, in dark or light mode. Open the 🎨 button, or go to **Library → Colours**.
- **Six interface languages:** English, മലയാളം, தமிழ், ಕನ್ನಡ, తెలుగు and हिन्दी.
- **Sleep timer,** with a smooth fade-out.
- **Lock-screen and Bluetooth controls:** the station name and play, pause, next and previous show on your phone's lock screen and in the car.
- **Data saver mode** for slow connections.
- **Backup and restore:** download your favourites, liked songs, custom stations and history as a file, and restore them on another phone.
- **Command palette:** press **Ctrl + K** (or ⌘ + K) to find any action.

### Keyboard shortcuts

| Key | Action |
|---|---|
| `Space` or `K` | Play / pause |
| `N` / `P` | Next / previous |
| `↑` / `↓` | Volume |
| `M` | Mute |
| `/` | Search |
| `Ctrl` + `K` | Command palette |
| `F` | Focus timer |
| `?` | Shortcuts and help |

---

## Your data and privacy

- No account and no sign-in.
- Favourites, liked songs, history, custom stations and settings stay **in your browser** on your device.
- The app contacts only these services:
  - **Radio Browser** for the station directory
  - **iTunes Search** for song search and previews
  - **Google Fonts**, plus the **Tailwind CSS** and **hls.js** libraries, loaded from their public servers
- Use **Library → Backup** to save your data before clearing your browser or changing phones.

---

## Troubleshooting

| Problem | What to do |
|---|---|
| A station will not play | Streams go offline sometimes. The app tries to reconnect, then moves to the next station. Pick another, or add a working link with **+ Add station**. |
| The layout looks too big, small or cut off | Press **?** → **Reset layout**. You can also switch Mobile / System view with the 📱 / 🖥️ button. |
| The app feels slow on your phone | Turn on **Lite effects** and **Compact** layout in **Library** or in the Help card. |
| "Install app" does not appear | Open the page from a normal web link in Chrome. It does not work from WhatsApp or from a file on your phone. |
| Voice does not work | Allow microphone access and use Chrome. |
| Something looks wrong | Press **?**, tap **Copy info**, and send it to whoever maintains the app. It shows your screen size, view mode and error count. |

---

## Known limits

- **No offline mode.** The app needs an internet connection. A single file cannot include the background worker offline mode requires.
- **Songs are 30-second previews.** Full songs open in YouTube Music.
- **Stations are only as good as the live directory.** A station appears only if the directory has a working link for it. The built-in stream links for the first ten Malayalam stations were best guesses, and the app swaps in current links from the directory whenever it finds a match.
- **No built-in equalizer** in this version.

---

## For developers

- **Single file:** HTML, CSS and JavaScript, using Tailwind CSS (CDN) and hls.js (CDN). There is no build step.
- **Add a station name to the list:** find the `CUR` catalogue in the script, for example:
  ```js
  R('Radio Example 99.9', 'fm', 'hits,kochi', /radio example/i, { q: 'radio example' })
  ```
  The pattern (`/radio example/i`) is matched against live directory names. `q` is the search word used if the bulk list does not contain it.
- **Focus & Work stations** are listed under `FOCUS` and use fixed stream links.
- **Change colours:** the palette variables are near the end of the stylesheet (`html[data-pal=...]`).
- **Saved settings** use browser storage keys that start with `nd_`.

---

## Credits

- Station directory: [Radio Browser](https://www.radio-browser.info)
- Song previews: [iTunes Search API](https://developer.apple.com/library/archive/documentation/AudioVideo/Conceptual/iTuneSearchAPI/)
- Streaming playback: [hls.js](https://github.com/video-dev/hls.js)
- Styling: [Tailwind CSS](https://tailwindcss.com)
- Ambient focus radio: [SomaFM](https://somafm.com)
- Fonts: [Google Fonts](https://fonts.google.com)

*All station names, logos and streams belong to their owners.*
