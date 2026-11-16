# LED Album Art

Full-screen Spotify album art rendered as a simulated LED matrix. Built for iPad, works in any modern browser.

**Layouts:** Panel (square matrix with bezel) · Ambient (whole screen of LEDs, art bleeds into the edges) · Now Playing (art + scrolling pixel-font title/artist/progress; adapts to landscape & portrait)
**LED styles:** Round · Square · Diffused · Pixel
**Resolution:** 16 / 32 / 48 / 64 / 96
**Color:** Full · 12-bit · 6-bit · 8-color · Amber · Green · Ice · Pocket (4-shade green), with optional ordered dithering
**Transitions:** Dissolve · Wipe · Fade · Cut

Gestures: tap = show/hide controls · swipe ← → = layout · swipe ↑ ↓ = LED style.

## Setup

1. **Host it on GitHub Pages:** in the repo, go to Settings → Pages → Deploy from branch → `main` / root.
   Your URL will be `https://<user>.github.io/<repo>/`.
2. **Create a Spotify app:** go to https://developer.spotify.com/dashboard → Create app → tick **Web API**.
   Add the Redirect URI exactly as the app shows it in Settings (e.g. `https://<user>.github.io/<repo>/`, including the trailing slash).
3. Open the site on your iPad → tap → ⚙ → Source: Spotify → paste your **Client ID** → Connect.
4. Tap Share → **Add to Home Screen** for a full-screen app with no browser bar. The "Keep screen awake" option stops it from dimming.

No server or client secret is needed. It uses Spotify's PKCE flow, and tokens stay in your browser's local storage.
Note: if you add it to the Home Screen, connect Spotify from inside the Home Screen app. iOS keeps its storage separate from Safari's.
