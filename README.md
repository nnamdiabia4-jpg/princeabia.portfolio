# Prince Abia Portfolio

A static, single-page portfolio site. No framework and no build step: everything runs from `index.html`.

## Folder structure

```
prince-abia-portfolio/
├── index.html          All markup, CSS and JavaScript (home page + case studies)
├── covers/             Images, GIFs and logo marks used across the site
├── vendor/
│   └── matter.min.js   Matter.js 0.19.0 (physics for the Contact section chips)
├── package.json        Local dev server script
├── package-lock.json
├── vercel.json         Vercel settings (clean URLs, long caching for images)
└── .gitignore
```

## Run locally

Requires Node.js 18 or newer.

```bash
npm install
npm run dev
```

Then open http://localhost:3000.

You can also just double-click `index.html`, but a local server is closer to how the site behaves once deployed.

## Deploy to Vercel

**From the dashboard:** push this folder to a GitHub repository, then in Vercel choose *Add New → Project*, import the repo and keep these settings:

- Framework Preset: **Other**
- Build Command: leave empty (or `npm run build`)
- Output Directory: leave empty (the project root)

**From the command line:**

```bash
npm i -g vercel
vercel        # preview deployment
vercel --prod # production deployment
```

## Editing content

- Case studies are stored in the `CASES` object near the bottom of `index.html` (one entry each for `pursar`, `bare`, `ace` and `vela`).
- To add an image, drop it into `covers/` and reference it as `covers/your-file.jpg`.

## External services

- Fonts (Inter, Instrument Serif) load from Google Fonts. The serif used for the Contact heading is embedded in `index.html`.
- Case-study buttons link to Behance. The email link opens Gmail compose.
