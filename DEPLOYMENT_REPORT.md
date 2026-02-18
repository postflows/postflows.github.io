# PostFlows Website — Deployment Report

## URL

- **Site:** https://postflows.github.io  
- **Repo:** https://github.com/postflows/postflows.github.io  

GitHub Pages deploys automatically from the `main` branch. If the site does not load immediately, wait 1–2 minutes and refresh. If it still fails, check **Settings → Pages**: Source should be **Deploy from a branch**, Branch **main** / **(root)**.

---

## Changes made to index.html

1. **Meta & SEO**
   - `meta name="description"` — Open-source scripts for DaVinci Resolve by PostFlows
   - `meta property="og:title"` — PostFlows — DaVinci Resolve Scripts
   - `meta property="og:description"` — Automation tools for serious editors.
   - `meta property="og:url"` — https://postflows.github.io
   - `link rel="canonical"` — https://postflows.github.io

2. **Favicon**
   - SVG favicon (PostFlows logo: dark square with four white/translucent squares) as data URI in `<head>`.

3. **Fonts**
   - Added **Inter** to Google Fonts link as fallback if Geist is unavailable.
   - `body` font-family: `'Geist', 'Inter', sans-serif`.

4. **Links**
   - Nav “GitHub” → https://github.com/postflows (unchanged).
   - Hero panel: each script opens either its detail page (TextPlus Manager, Clip Marker Tool) or the corresponding GitHub repo in a new tab.
   - Scripts grid: same behavior — detail page or repo.
   - Detail pages: “View on GitHub” / “Source on GitHub” → correct repo (resolve-textplus-manager, resolve-clip-marker-tool).
   - Download buttons left as `href="#"` (to be replaced with release/raw links later).

5. **Clip Marker Tool detail page**
   - Added full detail block `#detail-marker` so “Clip Marker Tool” opens an in-site page with description, installation steps, and link to https://github.com/postflows/resolve-clip-marker-tool.

6. **Dynamic title**
   - On detail page: `document.title` set to “TextPlus Manager — PostFlows” or “Clip Marker Tool — PostFlows”.
   - On “← All scripts”: title reset to “PostFlows — DaVinci Resolve Scripts”.

7. **Responsive**
   - `@media (max-width: 900px)`: single-column layout, reduced padding, hero panel above text, footer stacked.

---

## Resources section — links still placeholder (#)

These remain `href="#"` and can be filled later:

| Block        | Item                      | Note                    |
|-------------|---------------------------|-------------------------|
| Official Docs | Fusion Scripting Guide   | Need BMD/Fusion doc URL |
| Other Scripts | DaVinci Script Collection | Community list         |
| Other Scripts | Resolve Toolbox          | Commercial bundle       |
| Other Scripts | WSL DaVinci Scripts      | Open-source collection  |
| Utility tools | Resolve Script Loader    | Helper utility          |
| Utility tools | API Introspection Helper | Dump API reference      |
| Utility tools | Resolve Script Boilerplate | Template link        |
| Utility tools | Scripting Cheat Sheet    | Snippets doc            |
| Nav          | Docs                     | Future docs section     |
| Footer       | MIT License               | Can link to repo LICENSE |
| Footer       | Contact                   | Contact page or mailto  |

---

## Recommendations (next steps)

1. **Screenshots**  
   Add real script UI screenshots to `assets/screenshots/` and use them in card previews instead of mock windows.

2. **Download buttons**  
   Replace `href="#"` with:
   - GitHub “Releases” page (e.g. `https://github.com/postflows/resolve-textplus-manager/releases`), or  
   - Raw file URL (e.g. `https://github.com/.../raw/main/textplus-manager.lua`) for direct download.

3. **Resources**  
   Fill the placeholder links above when you have definitive URLs.

4. **Optional**  
   - “Copy install path” button on detail pages (macOS/Windows paths).  
   - Filter buttons (All / Lua / Python / etc.) wired to filter the script cards.
