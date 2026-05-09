# granat-site-indigo

Granat partner-facing site — **periwinkle indigo variant** (working name "CD", TMA-aligned, from the May 2026 Claude design pipeline).

Palette: deep indigo-purple `#1A1043` ground · granat-red `#C5403F` CTAs · periwinkle `#8FA3E8` accents — matched to the existing Granat Telegram MiniApp. Multi-section narrative (12 sections + combined single-page) with embedded voice-to-choir demo (Section 7).

## Run locally

```
npm install
cp .env.example .env       # set GRANAT_API_KEY
npm run dev                # or: npm start
```

Default port: 3000.

## Deploy

Same pattern as `granat-future-site` — Timeweb App Platform, Express static server with voice-API proxy. See `DEPLOY.md`.

## Companion repo

`granat-site-wine` — wine-brown variant of the same content. Both repos are deployable independently to separate domains so stakeholders can A/B compare visual direction before publishing decision.

## Structure

```
public/
  index.html               # combined mobile-friendly single-page (12 sections embedded)
  Hero.html                # standalone Section 1
  Challenge.html           # Section 2
  Philosophy.html          # Section 5
  Architecture.html        # Section 6
  How It Works.html        # Section 7 (voice demo)
  Roadmap.html             # Section 8
  Social.html              # Section 9
  Economy.html             # Section 10
  Invitation.html          # Section 11
  CTA.html                 # Section 12
  Team.html                # Section 4
  Granat - standalone source.html   # readable canonical source
  Hero.standalone.src.html
  guide.mp3                # voice-demo guide audio
  assets/                  # imagery (hero pomegranate)
  favicon.*                # favicons + apple-touch-icon + PWA icons
server.js                  # Express static + voice proxy + rate limiting
```
