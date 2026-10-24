# Anannya Gupta portfolio
Static site: HTML, CSS, vanilla JS. No build step, no dependencies. Fonts load from Google Fonts. Navigation uses `#hash` routes, so it works on any static host.

## Files
- `index.html` shell, title, meta tags
- `styles.css` colors and fonts in `:root` at the top, then all styles
- `script.js` all content (CONFIG, PROJECTS, SKILLS, LEARNING, EXP, CERTS) plus routing and the playground
- `assets/illustration/custom-illustration.svg` hero art (edit in any text editor or Figma/Inkscape)
- `assets/screenshots/` project screenshots (see its README)
- `assets/icons/`, `assets/images/` empty, for your own files

## Run locally
    python3 -m http.server 8000
then open http://localhost:8000

## Edit
- Name, email, GitHub, LinkedIn, resume: `CONFIG` at the top of `script.js`.
- Project text, role, tech, links: the project's entry in `PROJECTS`. `live` and `repo` buttons appear only when you fill them in. Add a date field only if you add rendering for it.
- New project: copy an entry in `PROJECTS`, give it a unique `id`, set `shots` to 0 until you have screenshots.
- Screenshots: save files in `assets/screenshots/` as `<project-id>-01.png`, `<project-id>-02.png`... (for example, `prontos-01.png`, `containercode-01.png`, `intelliapt-01.png`, or `anzentix-01.png`). Set that project's `shots` number in `script.js` to the count (optional `alts` array for alt text). See [assets/screenshots/README.md](assets/screenshots/README.md) for details.
- Colors/fonts: `:root` variables in `styles.css`; font link in `index.html`.
- Learning list, experience, certifications: `LEARNING`, `EXP`, `CERTS`.

## Deploy
- GitHub Pages: push to a repo, Settings > Pages > deploy from `main` / root.
- Netlify: drag the folder onto app.netlify.com/drop, or connect the repo (no build command, publish directory `.`).
- Vercel: `vercel` in the folder (framework: Other, no build command), or import the repo.

## Troubleshooting
- Blank page when opening `index.html` directly: use the local server above.
- Screenshot missing: check the filename matches `<id>-0N.png` and that `shots` is set.
- Fonts look different offline: they load from Google Fonts and fall back to system fonts.
- Changes not showing: hard refresh (Ctrl/Cmd+Shift+R).
