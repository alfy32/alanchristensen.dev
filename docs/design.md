# alanchristensen.dev — Site Design

**Date:** 2026-05-30
**Status:** Live

## Goal

A minimal personal homepage at [alanchristensen.dev](https://alanchristensen.dev). Puts the name and links forward — nothing more. Developer tools live at a separate site ([tools.alanchristensen.dev](https://tools.alanchristensen.dev), its own repo).

## Audience & Tone

- Anyone looking up Alan Christensen
- Clean, fast, readable — not flashy

---

## Architecture

**Stack:** Plain HTML, CSS, and vanilla JavaScript. No framework, no build step.

**File structure:**

```
alanchristensen.dev/
├── index.html   # Personal landing page
├── style.css    # Styles and dark mode
├── nav.js       # Site header (name link + dark mode toggle) injected via JS
└── CNAME        # GitHub Pages custom domain config
```

---

## Homepage (`index.html`)

- Name (large, top)
- One-line tagline
- Icon links to GitHub and LinkedIn
- A "Developer Tools →" card linking to `tools.alanchristensen.dev`

Nothing else.

---

## Visual Design

- **Font:** System font stack — no external fonts
- **Colors:** White background, dark text, single muted accent (blue/slate). Dark mode inverts bg/text.
- **Dark mode:** Toggle button in nav, persisted to `localStorage`
- **Layout:** Centered, max ~720px wide

---

## Hosting

| Concern | Solution | Cost |
|---------|----------|------|
| Hosting | GitHub Pages | Free |
| CI/CD | GitHub Pages auto-deploy on push to `main` | Free |
| Custom domain | Namecheap / Cloudflare Registrar | ~$10–15/yr |
| HTTPS | GitHub Pages provides it automatically | Free |

**Repo:** `github.com/alfy32/alanchristensen.dev`

**Deployment:** Push to `main` → GitHub Pages serves it.
