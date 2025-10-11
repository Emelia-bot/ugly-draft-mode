```markdown
# Ugly Draft Mode — Just Start Creating

A single-file, offline-friendly writing sandbox designed to make messy first drafts feel **safe** and easy.  
No backend, no frameworks—just one `index.html` with HTML/CSS/JS.

> Live anywhere. Open, type, save drafts locally. That’s it.

---

## ✨ Features
- Playful typography (Comic Sans / Comic Neue style with fallbacks)
- Mobile-first responsive layout
- Timer + live word count
- Local draft save / load / delete (via `localStorage`)
- Rotating encouragement messages
- “Nobody’s Watching” safety badge

---

## 🗂 Project Structure
```

.
├─ index.html      # the entire app
└─ README.md       # this file

```

---

## ▶️ Quick Start (Local)
1. Download or copy **`index.html`** to your computer.
2. Double-click to open it in your browser.
3. Start typing. Drafts save to your browser’s `localStorage`.

> macOS TextEdit tip: Format → *Make Plain Text* before saving as `index.html`.

---

## 🚀 Deploy

### Option A — GitHub Pages (free)
1. Push this repo to GitHub with `index.html` at the **root** (same folder as README).
2. In your repo: **Settings → Pages**  
   - **Source:** “Deploy from a branch”  
   - **Branch:** `main` (root) → **Save**  
3. Wait a minute. Your site appears at:
```

https://<your-username>.github.io/<repo-name>

```

> If you don’t see it, refresh after ~60 seconds or check Actions tab for build logs.

### Option B — Netlify Drop (fastest, no account needed)
1. Put `index.html` in a folder (e.g., `ugly-draft-mode/`).
2. Go to **https://app.netlify.com/drop**
3. Drag the **folder** onto the drop zone.
4. You’ll get a live URL like `https://silly-name-12345.netlify.app`.

**Fix Netlify 404s**
- Ensure `index.html` is at the **root** of what you dropped (not nested in `/index/`).
- Filename must be exactly `index.html`.
- If you plan to navigate to sub-paths, add a `_redirects` file with:
```

/*    /index.html   200

````

### Option C — Vercel
1. Go to **https://vercel.com** → Sign up.
2. “Add New” → “Project” → Import your repo (or drag the folder).
3. Deploy. You’ll get `https://<project>.vercel.app`.

---

## 📱 Mobile QA (5-Minute Checklist)
- **Fonts**: Same playful font on iOS & Android (no unexpected serif).
- **Layout**: No horizontal scroll at 320–375px; text stays inside containers.
- **Tap targets**: Buttons ≥ 44×44px; padding ≥ 16px around edges.
- **Typing**: Keyboard doesn’t hide the editor; word count updates live.
- **Drafts**: Save → back to home → draft shows in list → reopen OK → delete works.

---

## 🛠️ Customization Notes

**Fonts (most reliable):**  
Add a hosted font (e.g., Comic Neue) in `<head>` if you want 100% consistency across devices:
```html
<link href="https://fonts.googleapis.com/css2?family=Comic+Neue:wght@400;700&display=swap" rel="stylesheet">
<style>
body { font-family: "Comic Neue", "Comic Sans MS", "Comic Sans", "Chalkboard SE", cursive, sans-serif; }
</style>
````

**Mobile safety CSS:**
If long words “bleed” on small screens, add:

```css
html, body { max-width: 100%; overflow-x: hidden; -webkit-text-size-adjust: 100%; }
textarea, .editor-container { word-wrap: break-word; overflow-wrap: anywhere; }
img, video { max-width: 100%; height: auto; }
```

**Keyboard overlap (optional):**

```css
textarea { padding-bottom: 24vh; } /* room for mobile keyboard */
```

---

## 🔐 Privacy

All drafts are stored locally in your browser via `localStorage`. No servers, no tracking.
Clearing site data or switching devices will affect access to saved drafts.

---

## 🧭 Roadmap (optional)

* Voice Capture mode (mic → transcript → export)
* Export (Markdown / TXT / Copy All)
* Theme settings (dark / high contrast)
* Backup/restore to a file

---

## 🆘 Troubleshooting

**GitHub Pages not showing?**

* Ensure `index.html` is at the repo root (not in a subfolder).
* Settings → Pages → source is set to `main` (root).
* Wait ~1–2 minutes; then hard-refresh.

**Netlify “Page not found”**

* `index.html` must be at the root of the deployed folder.
* If using sub-paths, add `_redirects` with `/* /index.html 200`.

**Different font on mobile**

* Add the Google Fonts link above and set `font-family` to it first in the stack.

---

## 📝 License

Personal/portfolio use permitted. Add your preferred license if commercializing.

```

add README for Ugly Draft Mode project
