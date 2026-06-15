# InHerVoice Website — Maintenance Guide

Hosted on GitHub Pages from the `/docs` folder of this repo.
Live URL: `https://pallavi-ai-labs.github.io/in-her-voice/`

---

## File Structure

```
docs/
├── index.html              ← The entire website (single file)
├── WEBSITE.md              ← This file
└── assets/
    └── visuals/
        ├── 2026-05-08-silicon-to-ai-arc.png
        ├── 2026-05-18-hyperscaler-chips-intel-foundry.png
        ├── 2026-05-21-agent-eval-outcome-leaderboards.png
        ├── 2026-05-21-seattle-shield-consent-default.png
        └── 2026-05-11-deployCo-enterprise-deployment.png
```

Everything is in `index.html`. No build step. No framework. Edit HTML directly and push.

---

## How to Update the Writing Section

The Writing section is in `index.html` — search for `id="writing"`.

Each post is a card `<div>` with this structure:
```html
<div class="reveal ... card-hover bg-surface border ...">
  <img src="assets/visuals/YOUR-IMAGE.png" alt="..." class="writing-img ..." />
  <div class="p-6 flex flex-col flex-1">
    <span class="...">Tag</span>
    <span class="...">Month Year</span>
    <h3>Post title here</h3>
    <p>Two-line excerpt here...</p>
    <a href="LINKEDIN_POST_URL">Read on LinkedIn</a>
  </div>
</div>
```

To update a post:
1. Replace the `<img src="...">` with the new visual (copy PNG to `assets/visuals/`)
2. Update the tag, date, title, excerpt, and LinkedIn link
3. Save and deploy

---

## How to Add a New Project

The Projects section is in `index.html` — search for `id="projects"`.

Copy an existing project card `<div class="reveal card-hover ...">...</div>` and paste it inside the grid. Update:
- The emoji icon
- Title and tagline
- Description text
- Status badge (LIVE / LIVE DEMO / BUILDING)
- Tag badges (tech stack)
- Optional link (or remove the `<a>` tag if private)

---

## How to Update Placeholder Links

Search for `<!-- UPDATE:` in `index.html`. Currently flagged:

| Comment | What to replace | Where |
|---|---|---|
| `<!-- UPDATE: LinkedIn URL -->` | Pallavi's actual LinkedIn profile URL | Nav connect button, Writing CTA, Connect card |
| `<!-- UPDATE: Substack URL -->` | Pallavi's Substack publication URL | Substack strip `<a href="#">`, Connect card `<a href="#">` |

Replace `href="#"` or `href="https://www.linkedin.com/in/pallavi-sharma-ai/"` with the real URLs.

---

## How to Add New Images

1. Copy the PNG into `docs/assets/visuals/`
2. Reference it in `index.html` as `src="assets/visuals/your-filename.png"`
3. Always include a descriptive `alt="..."` attribute

---

## How to Deploy

GitHub Pages serves from the `/docs` folder automatically once enabled in repo Settings.

```bash
# From the repo root:
git add docs/
git commit -m "Update website: <what changed>"
git push
```

GitHub Pages auto-deploys within ~60 seconds of the push. No build step required.

### First-time setup (one time only)
1. Go to repo Settings → Pages
2. Source: Deploy from a branch
3. Branch: `main` (or your default branch), Folder: `/docs`
4. Save — the site goes live at `https://pallavi-ai-labs.github.io/in-her-voice/`

---

## Style Reference (for manual edits)

Colors are defined in the Tailwind config block at the top of `index.html`:
- `bg-bg` — `#080c14` (page background)
- `bg-surface` — `#111827` (cards)
- `bg-surface2` — `#1a2234` (secondary surfaces)
- `text-gold` — `#f59e0b` (amber accent)
- `text-blue` — `#60a5fa` (blue accent)
- `text-text` — `#f1f5f9` (primary text)
- `text-muted` — `#94a3b8` (secondary text)

Font: Inter (loaded from Google Fonts CDN — requires internet connection to render correctly).
