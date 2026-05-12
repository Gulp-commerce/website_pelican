# pelicanpicks.com

Static marketing site for Pelican Picks. Built with **Vite** + **Tailwind CSS v4**, deployed to **GitHub Pages**.

## Pages

- `index.html` — one-pager landing
- `kontakt.html` — contact
- `impressum.html` — Impressum (DE)
- `datenschutz.html` — Datenschutzerklärung (DE)

## Develop

```bash
npm install
npm run dev      # local dev server with HMR
npm run build    # production build into dist/
npm run preview  # preview built site
```

## Deploy

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds with Vite
and deploys `dist/` to GitHub Pages. The custom domain (`pelicanpicks.com`) is
preserved via `public/CNAME`.

**One-time setup in the GitHub repo settings:**
Settings → Pages → Build and deployment → Source: **GitHub Actions**.

## Structure

```
.
├── index.html, kontakt.html, impressum.html, datenschutz.html
├── src/
│   ├── main.js          (mobile menu toggle, footer year)
│   └── style.css        (Tailwind + theme tokens)
├── public/              (static assets copied as-is)
│   ├── logo.png
│   ├── favicon.svg
│   ├── robots.txt
│   └── CNAME
├── vite.config.js       (multi-page entries)
└── .github/workflows/deploy.yml
```

The previous Publii-generated state is archived in the `publii-final` git tag.
