# granat-site-indigo

> Granat partner-facing site — periwinkle-indigo variant, aligned to the Telegram MiniApp. Part of the Granat platform; maintained by Cone Red Engineering.

A multi-section narrative site (12 sections plus a combined single page) with an embedded voice-to-choir demo, in the periwinkle-indigo visual direction (working name "CD", from the May 2026 design pipeline). Its companion `granat-site-wine` carries the same content in a wine-brown palette; the two deploy independently so stakeholders can A/B the visual direction.

Palette: deep indigo-purple `#1A1043` ground · granat-red `#C5403F` CTAs · periwinkle `#8FA3E8` accents — matched to the existing Granat Telegram MiniApp.

## Stack

- Node.js + Express (static server with voice-API proxy)
- `express-rate-limit`, `multer`
- Static multi-section site in `public/`

## Getting started

```bash
npm install
cp .env.example .env        # set GRANAT_API_KEY
npm run dev                 # http://localhost:3000
```

## Configuration

| Variable | Purpose |
|---|---|
| `GRANAT_API_KEY` | Upstream voice-API key (injected server-side for the Section 7 demo) |
| `GRANAT_API_BASE` | Upstream voice-API base URL |

## Deployment

Timeweb App Platform — Express static server with the voice-API proxy pattern. See `DEPLOY.md`.

## Repository layout

```
public/
  index.html        combined single-page (12 sections embedded)
  Hero.html         Section 1            How It Works.html  Section 7 (voice demo)
  Challenge.html    Section 2            Roadmap.html       Section 8
  Team.html         Section 4            Social.html        Section 9
  Philosophy.html   Section 5            Economy.html       Section 10
  Architecture.html Section 6            Invitation.html    Section 11
                                         CTA.html           Section 12
  guide.mp3         voice-demo guide audio
  assets/           imagery
  favicon.*         favicons + PWA icons
server.js           Express static + voice proxy + rate limiting
```

## License

Proprietary. © 2026 Granat Music Artistic Talent Contracting L.L.C S.O.C. All rights reserved. See [LICENSE](./LICENSE).
