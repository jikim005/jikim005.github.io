# jiyoon-kim.com

Personal academic website of Jiyoon Kim — plain static HTML/CSS, hosted on GitHub Pages.

## Pages

- `index.html` — Home (bio)
- `research.html` — Research (work in progress with abstracts and PDFs)
- `teaching.html` — Teaching (courses, philosophy, evaluations)
- `cv.html` — CV (embedded PDF + download)

## Updating the CV

Replace `assets/pdf/CV_JiyoonKim.pdf` with the new file (same name), commit, and push.

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deployment

Hosted on GitHub Pages from the `main` branch. The `CNAME` file points the site at `www.jiyoon-kim.com`; DNS is managed at the domain registrar (A records for apex → GitHub Pages IPs, CNAME for www → `<username>.github.io`).
