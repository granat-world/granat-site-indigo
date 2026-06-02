# granat-site-indigo — Reviewer Quickstart

> **⚠️ OUT OF SCOPE for Phase 1 independent code review.**
> This repository is a **Cone Red goodwill artefact**, delivered to the Customer as-is at the close of Phase 1. It is **not** one of the two in-scope repositories. Master review guide: [`granat-world/GRANAT/REVIEW_GUIDE.md`](https://github.com/granat-world/GRANAT/blob/develop/REVIEW_GUIDE.md).
>
> This quickstart is provided so that a curious reviewer can run the project locally if they want — not because review is expected.

---

## 1. What this repository is

A multi-section partner-facing narrative site (12 sections plus a combined single page) with an embedded voice-to-choir demo, in the **periwinkle-indigo** visual direction (working name "CD"), aligned to the existing Granat Telegram Mini App palette. Sibling of `granat-site-wine` (same content, different palette). Palette: deep indigo-purple `#1A1043` ground · granat-red `#C5403F` CTAs · periwinkle `#8FA3E8` accents.

## 2. Requirements

| Tool | Version |
|---|---|
| Node.js | ≥ 18 (LTS) |
| npm | ≥ 10 |
| Browser | any modern |

**Time to running:** ~1–2 minutes

## 3. Clone and run

```bash
git clone https://github.com/granat-world/granat-site-indigo.git
cd granat-site-indigo
cp .env.example .env
# Optional: set GRANAT_API_KEY in .env if you want the Section 7 voice
#          demo to call the upstream voice API live.
npm install
npm run dev
# Open http://localhost:3000
```

Same server pattern as the wine variant: Express serves static + proxies the voice API.

## 4. What to look at

- **`public/index.html`** — combined single-page (12 sections embedded)
- **`public/{Hero, Challenge, Team, Philosophy, Architecture, How It Works, Roadmap, Social, Economy, Invitation, CTA}.html`** — individual sections
- **`server.js`** — Express static + voice-API proxy + rate limiting

## 5. Stack overview

- Node.js + Express
- `express-rate-limit`
- `multer`
- Static multi-section site in `public/`

## 6. License

Proprietary. © 2026 Granat Music Artistic Talent Contracting L.L.C S.O.C. See `LICENSE`.

---

**For the actual Phase 1 review pack**, see [`granat-world/GRANAT/REVIEW_GUIDE.md`](https://github.com/granat-world/GRANAT/blob/develop/REVIEW_GUIDE.md) — the master guide covering the in-scope repositories (`GRANAT` + `reactjs-miniapp-granat`), their SBOMs, security audits, and the 14 048-line platform documentation pack.
