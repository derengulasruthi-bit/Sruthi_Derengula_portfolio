# Sruthi Derengula – Portfolio Website

Personal portfolio for Sruthi Derengula — Data Analyst, Business Analyst & Technology Educator.
It is a fast, static website (plain HTML, CSS and JavaScript, no build step) with the original
dark premium design: animated gradient blobs, word-by-word hero reveal, floating skill badges,
scrolling skills marquee, animated counters, 3D card tilt, project case-study pop-ups,
certificate lightbox and a downloadable résumé.

**Live URL:** https://portfolio-deployment-e6bcf9.netlify.app

## What's inside

```
site/                         ← everything that gets published
  index.html                  page markup (all sections)
  css/styles.css              design, animations, responsive rules
  js/main.js                  animations, case studies, lightbox, mobile menu
  assets/images/              profile photos, certificates, project images
  assets/Derengula_Sruthi_Resume.pdf
  favicon.svg, 404.html, robots.txt, _headers
  downloads/sruthi-portfolio-website.zip   deployment-ready copy of the site
netlify.toml                  tells Netlify to publish the site/ folder
```

Technologies: HTML5, CSS3 (grid, custom properties, keyframe animations), vanilla JavaScript
(IntersectionObserver), Google Fonts (Sora, Inter), Netlify static hosting.

## Run it locally

No install is needed. Either open `site/index.html` in a browser, or serve the folder:

```bash
npx serve site        # or: python3 -m http.server --directory site 8000
```

## Publish it on Netlify (step by step)

**Option 1 — Drag and drop (easiest, about 2 minutes)**
1. Download `sruthi-portfolio-website.zip` and unzip it on your computer.
2. Sign in (or sign up free) at https://app.netlify.com.
3. Open https://app.netlify.com/drop.
4. Drag the unzipped folder (the one that contains `index.html`) onto the page.
5. Netlify uploads it and shows a public URL such as `https://random-name.netlify.app`.
6. Optional: **Site configuration → Change site name** to get e.g. `https://sruthi-derengula.netlify.app`.

**Option 2 — This connected project**
This repository is already connected to Netlify. Every change published to the `main`
branch redeploys the site automatically at https://portfolio-deployment-e6bcf9.netlify.app.

**Custom domain (optional):** Domain management → Add a domain → follow the DNS steps.
HTTPS is set up automatically.

## Updating content

- **Text:** edit `site/index.html`.
- **Photos / certificates:** replace the file in `site/assets/images/` and keep the same name.
- **Case-study images:** paths are in the `IMG` object near the top of `site/js/main.js`.
- **Résumé:** replace `site/assets/Derengula_Sruthi_Resume.pdf` (same file name).
- If you deploy under a different web address, update the `og:image` URL in `index.html`
  so link previews on LinkedIn/WhatsApp show your photo.
