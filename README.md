# THE ALGORITHM — Landing Page

Welcome experience for clients receiving access to the Market & Social Intelligence platform, built by THE LAB at Wanted.

---

## Before going live

Open `index.html` and update the top of the `<script>` block:

| Field | Location | What to change |
|---|---|---|
| `algorithmUrl` | `CONFIG.algorithmUrl` | Replace `'YOUR_URL_HERE'` with the actual platform URL |
| Client name | `CONFIG.client` | Replace `'Universidad Católica de San Pablo'` |
| Logo | `assets/images/wanted-blanco.png` | Drop in the correct white logo (PNG or SVG) |

---

## File structure

```
index.html              ← Single-file app, no build step
assets/
  images/
    wanted-blanco.png   ← White logo (gate + final screen)
    wanted-negro.png    ← Dark logo (reserved)
  audio/                ← Drop a .mp3/.ogg here if replacing procedural audio
README.md
.gitignore
```

---

## Deploy to Netlify

**Drag & drop (fastest):**
1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag the entire project folder onto the "Deploy manually" drop zone
3. Done — live in ~30 seconds

**Netlify CLI:**
```bash
npm install -g netlify-cli
netlify deploy --dir . --prod
```

**From GitHub (continuous deployment):**
1. Push this repo to GitHub
2. In Netlify: New site → Import from Git → select repo
3. Build command: *(leave empty)*
4. Publish directory: `.`
5. Deploy

---

## Local preview

Open `index.html` directly in Chrome — no server required.

For other browsers or to test the fullscreen API accurately:
```bash
npx serve .
# then open http://localhost:3000
```

---

## Customizing for a new client

All client-specific values live in `CONFIG` at the top of the script:

- `algorithmUrl` — CTA button destination
- `client` — name shown in the final welcome message
- `layers[]` — four analysis layer names and descriptions
- `counters[]` — the three animated stat counters on the final screen
