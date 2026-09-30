# Pomo Worlds

A pomodoro timer with five worlds to focus in. Each world has its own look, music, sounds and a little companion who keeps you company while you work.

**Live site:** add your link here after deploying (for example `https://pomo-worlds.vercel.app`).

## The worlds

| World | Look | Companion | Break animation |
|---|---|---|---|
| **Cozy Café** | Soft clay 3D, pastel colours, a drink that empties as you focus | A study buddy (tomato, cat, bunny or bear) who walks beside you | The buddy sips its drink and dances |
| **Minimal** | Japandi calm: warm paper, thin serif type and an ink-brush circle | A little ink face | A breathing circle guides your breath while petals fall |
| **80s** | Synthwave: a neon sunset over an endless moving grid | A neon robot | A neon car cruises the horizon under shooting stars |
| **Retro** | 8-bit quest: an HP bar that drains and a heart for every round | A pixel tomato hero | The hero sleeps by a campfire |
| **Dark academia** | A brass pocket watch, candlelight and old books | An owl on the desk | Tea by the candle while the owl dozes |

Every world has four colour palettes.

## Music

Each world has six tracks, all generated live in the browser:

- **Cozy Café:** Music box, Lo-fi beats, Ukulele sunshine, Rainy window, Café hum, Marimba morning
- **Minimal:** Zen piano, Soft rain, Singing bowls, Forest stream, Koto garden, Brown noise
- **80s:** Neon drone, Night drive, Outrun, Neon rain, Arcade lounge, Cassette tape
- **Retro:** Chiptune loop, Overworld, Dungeon, Boss battle, Village inn, Pixel rain
- **Dark academia:** Fireside, Harpsichord study, Library rain, Candlelit strings, Grandfather clock, Cello nocturne

## Features

- Focus, short break and long break, with a long break after every four focus rounds
- Each mode remembers its own paused time; skipping a focus round does not count it as finished
- Custom round lengths, a volume slider, a completion chime and button click sounds
- A popup and a themed confetti burst when a focus round ends
- The companion speaks up when you start, at halfway, with one minute left and when a round ends
- A 3D carousel to choose your world, with a zoom-in transition into it
- 3D tilt and parallax on desktop, and a phone-friendly layout
- Your world, palette, music, buddy, round lengths and today's round count are remembered in your browser

## How to use

1. Pick a world on the welcome screen and press **Enter**, or click the portal in the middle.
2. Press **Start**. Use the tabs to switch between Focus, Short break and Long break.
3. Use the dock in the top-right corner:
   - **Music:** turn music on or off and choose a track
   - **Sounds:** volume, completion chime and button sounds
   - **Timer:** round lengths
   - **Look:** colour palette (and study buddy in Cozy Café)
4. Press **← Worlds** in the top-left corner to choose another world.

### Keyboard

| Key | Action |
|---|---|
| Space | Start or pause the timer |
| ← → | Browse worlds on the welcome screen |
| Esc | Close a panel or popup |

## Running it locally

The whole site is one file, `index.html`. Double-click it to open it in your browser. There is nothing to install or build.

## Deploying

Any static host works, because the site is a single HTML file.

**Vercel (command line)**

```bash
npm install -g vercel
vercel          # first deploy and login
vercel --prod   # publish to your live link
```

**Vercel (from GitHub):** go to [vercel.com/new](https://vercel.com/new), import this repository and click **Deploy**. No settings are needed.

**Netlify:** drag the project folder onto [app.netlify.com/drop](https://app.netlify.com/drop).

**GitHub Pages:** in this repository go to **Settings → Pages**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.

## How it's built

- Plain HTML, CSS and JavaScript in a single file, with no frameworks or build step
- All graphics are drawn with SVG and CSS
- All music and sound effects are generated with the Web Audio API, so there are no audio files; the completion chime is also rendered to a short audio clip so it plays reliably in every browser
- The timer runs on a background worker so it stays accurate in hidden tabs
- Fonts load from Google Fonts: Fredoka, Nunito, Cormorant Garamond, Karla, Orbitron, Audiowide, Press Start 2P, EB Garamond, Cinzel and Bricolage Grotesque
- Respects the "reduce motion" setting on your device

## Browser support

Works in current versions of Chrome, Edge, Safari and Firefox, on desktop and mobile. Browsers only allow sound after you tap or click something, so music starts when you enter a world.
