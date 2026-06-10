# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Jiyoon Kim's personal academic website (jiyoon-kim.com), ported from Squarespace to plain static HTML/CSS hosted on GitHub Pages. No build step, no framework, no JavaScript dependencies.

## Structure

- Four pages: `index.html` (Home), `research.html`, `teaching.html`, `cv.html`. Each page duplicates the same header/nav and footer markup inline — when editing nav or footer links, update all four files.
- `css/style.css` — single stylesheet; colors/fonts/layout via CSS variables in `:root`.
- `assets/pdf/` — CV, paper PDFs, teaching evaluations. To update the CV, replace `assets/pdf/CV_JiyoonKim.pdf` (filename is referenced from `index.html` and `cv.html`).
- `assets/img/profile.jpg` — homepage portrait (resized to ≤1000px with `sips`).
- `CNAME` — custom domain for GitHub Pages; do not delete.

## Conventions

- Research entries on `research.html` follow a fixed pattern: `.paper` div with title, status note (journal status / coauthor), then a `.paper-actions` row holding an empty `<details><summary>Abstract</summary></details>` toggle chip plus an optional `.chip` PDF link, followed by the abstract in `<p class="abstract">`. The abstract is shown via the CSS rule `.paper:has(details[open]) .abstract` — the `<details>` element stays empty on purpose. New papers should copy this pattern.
- The header nav (including the `.nav-social` inline-SVG icon links) is duplicated across all four pages; keep them in sync.
- Typographic entities (`&ldquo;`, `&rsquo;`, `&mdash;`) are used in body text rather than raw unicode quotes.
- Content mirrors the owner's former Squarespace site; keep wording changes minimal unless asked.

## Preview and deploy

- Local preview: `python3 -m http.server 8000` from the repo root, then open http://localhost:8000.
- Deployed via GitHub Pages from the `main` branch root. Pushing to `main` publishes the site.
