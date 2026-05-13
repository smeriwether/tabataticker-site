# Tabata Ticker Marketing Site

Marketing website for Tabata Ticker, a focused iPhone, iPad, and Apple Watch Tabata timer.

## Overview

Tabata Ticker runs the classic Tabata workout and supports saved custom presets:

- 8 rounds
- 20 seconds work
- 10 seconds rest
- Custom work time, rest time, and round count presets
- iPhone owns the timer
- Apple Watch mirrors the timer and sends start, pause, reset, and sound commands
- Sound cues run during the final 5 work seconds and final 3 rest seconds
- Apple Watch pairs cues with haptics
- Single $0.99 App Store purchase for iPhone, iPad, and Apple Watch

The page also includes real app screenshots in CSS-rendered iPhone and Apple Watch shells, plus a playable four-minute Tabata timer as a small easter egg, similar to the playable Minesweeper preview on the MenuMines site.

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

The site is configured for:

```text
https://tabataticker.merimerimeri.com/
```

Custom domain setup:

- DNS should include a `CNAME` record for `tabataticker` pointing to `smeriwether.github.io`.
- The repo-root `CNAME` file contains `tabataticker.merimerimeri.com`.
- GitHub Pages should be configured with `tabataticker.merimerimeri.com` as the custom domain.

## App Store Link

The live App Store listing is:

```text
https://apps.apple.com/us/app/tabata-ticker/id6768484593
```

The home page uses that URL for both App Store call-to-action links, the FAQ App Store link, the iOS smart-banner meta tag, and the structured data download URL.

## Project Structure

```text
.
├── src/
│   └── styles.css       # Tailwind source and custom styles
├── dist/
│   └── styles.css       # Generated CSS, committed for GitHub Pages
├── assets/
│   └── screenshots/     # Resized app screenshots used in device shells
├── index.html           # Main marketing page and playable timer
├── privacy.html         # Privacy policy
├── app-store-badge.svg  # Official App Store download badge
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
