# jiyoon-kim.com

Personal academic website of Jiyoon Kim — plain static HTML/CSS, hosted on GitHub Pages.

## Pages

- `index.html` — Home (bio)
- `research.html` — Research (work in progress with abstracts and PDFs)
- `teaching.html` — Teaching (courses, philosophy, evaluations)
- `cv.html` — CV (embedded PDF + download)

## How to update the site

Any change follows the same three steps — edit, commit, push:

```bash
cd ~/jiyoon-kim-website
# 1. make your edits (see common tasks below)
# 2. save them into git's history
git add -A
git commit -m "Describe what you changed"
# 3. publish — the live site updates ~30 seconds after this
git push
```

To preview before publishing, run `python3 -m http.server 8000` in this
folder and open http://localhost:8000 — check your edits, then push.

### Common tasks

- **New CV**: replace `assets/pdf/CV_JiyoonKim.pdf` with the new file,
  keeping the exact same filename. Then commit and push.
- **Edit text** (bio, abstracts, courses): open the page's `.html` file in any
  text editor, find the text, and change it. The files are plain text.
- **Add a paper**: in `research.html`, copy an existing
  `<div class="paper"> … </div>` block and edit the title, note, PDF link
  (drop the PDF in `assets/pdf/` first), and abstract.
- **Change colors**: edit `--accent` and `--heading` at the top of
  `css/style.css`.

Or open Claude Code in this folder and just describe the change.

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deployment

Hosted on GitHub Pages from the `main` branch. The `CNAME` file points the site at `www.jiyoon-kim.com`; DNS is managed at the domain registrar (A records for apex → GitHub Pages IPs, CNAME for www → `<username>.github.io`).
