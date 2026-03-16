# Linksammlung v3

Eine persönliche Linksammlung als statische Webseite mit Milchglas-Design.

## Features

- Zwei umschaltbare Linklisten (z.B. Privat / Arbeit)
- Milchglas-Design (Glassmorphism) mit Hover-Animationen
- Responsives Layout (1 / 2 / 3 Spalten)
- Konfiguration über eine einzige JSON-Datei
- Docker-Deployment mit nginx

## Starten

```bash
docker compose up -d
```

Öffne [http://localhost:8080](http://localhost:8080).

## Konfiguration

Bearbeite `site/config.json`:

```json
{
  "title": "Meine Linksammlung",
  "favicon": "assets/icons/favicon.png",
  "wallpaper": "assets/wallpaper/bg.jpg",
  "toggleLabels": { "left": "Privat", "right": "Arbeit" },
  "lists": {
    "left": [
      { "text": "GitHub", "url": "https://github.com", "description": "Code & Repos", "icon": "" }
    ],
    "right": [
      { "text": "Jira", "url": "https://jira.example.com", "description": "Tickets", "icon": "" }
    ]
  }
}
```

## Assets

- Hintergrundbild: `site/assets/wallpaper/`
- Icons: `site/assets/icons/`
- Fonts: `site/assets/fonts/`

Nach Änderungen Seite im Browser neu laden.

## Lizenz

Privat
