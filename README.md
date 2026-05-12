# Tabata Ticker Marketing Site

Marketing website for Tabata Ticker, a minimal iPhone and Apple Watch Tabata timer.

## Overview

Tabata Ticker runs the classic Tabata workout:

- 8 rounds
- 20 seconds work
- 10 seconds rest
- iPhone owns the timer
- Apple Watch mirrors the timer and sends start, pause, reset, and sound commands
- Sound cues run during the final 5 work seconds and final 3 rest seconds
- Apple Watch pairs cues with haptics

The page also includes a playable four-minute Tabata timer as a small easter egg, similar to the playable Minesweeper preview on the MenuMines site.

## Tech Stack

- Plain HTML with a small inline JavaScript timer
- [Tailwind CSS](https://tailwindcss.com) v4 built with the CLI
- [JetBrains Mono](https://www.jetbrains.com/lp/mono/) via Google Fonts
- Static files served directly by GitHub Pages

This matches the MenuMines site convention: `src/styles.css` is the Tailwind source, `dist/styles.css` is the generated output, and `dist/styles.css` is committed so GitHub Pages can serve the site without a build step.

## Local Development

Install dependencies:

```sh
npm install
```

Build CSS:

```sh
npm run build:css
```

Open the site:

```sh
open index.html
```

Rebuild CSS while editing:

```sh
npm run dev
```

## Deployment

Deploy this repo the same way as the MenuMines site:

1. Push the static site to the `main` branch.
2. In GitHub, enable GitHub Pages for the repository.
3. Set the Pages source to deploy from the `main` branch.
4. Keep `dist/styles.css` committed.

Until a custom domain is ready, the site is configured for:

```text
https://smeriwether.github.io/tabataticker-site/
```

When a domain is chosen:

- Add a `CNAME` file containing the domain.
- Update `index.html` canonical/Open Graph URLs.
- Update `robots.txt`.
- Update `sitemap.xml`.

## App Store Link

The current page intentionally shows the App Store call to action as "Coming Soon." When the App Store listing is live:

- Replace the disabled App Store blocks in `index.html` with real links.
- Add an `apple-itunes-app` smart-banner meta tag if desired.
- Update structured data availability if needed.

## Project Structure

```text
.
├── src/
│   └── styles.css       # Tailwind source and custom styles
├── dist/
│   └── styles.css       # Generated CSS, committed for GitHub Pages
├── index.html           # Main marketing page and playable timer
├── privacy.html         # Privacy policy
├── icon-1024.png        # App icon source copy
├── icon-180.png         # Apple touch icon
├── icon-128.png         # Smaller app icon
├── favicon-32.png
├── favicon-16.png
├── robots.txt
├── sitemap.xml
├── package.json
└── README.md
```
