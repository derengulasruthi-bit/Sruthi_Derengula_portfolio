# AGENTS.md

## Architecture
Static, single-page portfolio. No framework, no bundler, no build step. Netlify publishes `site/`
directly (see `netlify.toml`). Headers are in `site/_headers` (not netlify.toml) so they also apply
when the folder is deployed via drag-and-drop.

## Key files
- `site/index.html` – all section markup (hero, stats, about, skills, projects, experience, education, contact).
- `site/css/styles.css` – the original design rules, followed by a clearly marked
  "Deployment compatibility & responsive refinements" block. Add fixes in that block; do not
  restyle the original rules (the owner wants the design preserved exactly).
- `site/js/main.js` – `IMG` (image paths) and `PROJ` (case-study content) objects drive the
  project modals; then hero word reveal, IntersectionObserver reveals (`.rv` → `.in`), card tilt,
  progress bar, cursor glow, counters (`data-count`), certificate lightbox, mobile menu.
- `site/assets/` – images and the résumé PDF.
- `site/downloads/sruthi-portfolio-website.zip` – deployment-ready copy for the owner. Rebuild it
  (from `site/` minus `downloads/`, plus a `netlify.toml` with `publish = "."` and the deploy
  instructions) whenever site files change.

## Non-obvious decisions
- The site came from one self-contained HTML file with base64-embedded images and résumé.
  These were split into real files for caching and performance. The original résumé button used a
  preview-only `window.claude` download API; it is now a normal `<a download>` link.
- The colour variables are named `--purple`/`--blue` but hold rose/peach values (#C9849A/#F2D3BE).
  This is intentional. Keep them.
- Card tilt only runs on mouse/fine-pointer devices so cards don't stay tilted after a tap.
- The `og:image` uses the absolute production URL.
