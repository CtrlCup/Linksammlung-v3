# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Linksammlung v3** is a personal link management application – a static website with a frosted-glass (Milchglas) design, two switchable link lists, responsive layout, and Docker deployment.

## Tech Stack

- **Static HTML** – single `site/index.html`, no build step
- **Tailwind CSS** via CDN (`cdn.tailwindcss.com`)
- **Vanilla JavaScript** – config-driven rendering
- **nginx:alpine** – served via Docker

## Project Structure

```
site/
├── index.html        # Entire app (HTML + inline JS)
├── config.json       # All configuration (title, links, assets, toggle labels)
└── assets/
    ├── icons/        # Tile icons, favicon
    ├── wallpaper/    # Background images
    └── fonts/        # Custom fonts
docker-compose.yml    # Docker deployment
nginx.conf            # nginx configuration
```

## Development Commands

```bash
docker compose up -d          # Start server → http://localhost:8080
docker compose down           # Stop server
docker compose restart web    # Restart after nginx.conf changes
```

No build step required. Edit `site/config.json` to change links and settings, then reload the browser.

## Configuration

All content is driven by `site/config.json`:
- `title` – page title
- `favicon` – path to favicon image
- `wallpaper` – path to background image (falls back to CSS gradient)
- `toggleLabels` – labels for the left/right toggle
- `lists.left` / `lists.right` – link arrays with `text`, `url`, `description`, `icon`

## Assets

Place files in `site/assets/`:
- Icons: `site/assets/icons/`
- Wallpapers: `site/assets/wallpaper/`
- Fonts: `site/assets/fonts/`
