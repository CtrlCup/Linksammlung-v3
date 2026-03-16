# Linksammlung v3

Eine persönliche Linksammlung als statische Webseite mit Milchglas-Design.

## Features

- Zwei umschaltbare Linklisten (z.B. Privat / Arbeit)
- Milchglas-Design (Glassmorphism) mit Hover-Animationen
- Responsives Layout (1 / 2 / 3 Spalten)
- Konfiguration über eine einzige JSON-Datei
- Docker-Deployment mit nginx

## Einrichtung

1. Beispielkonfiguration kopieren:
   ```bash
   cp site/config.example.json site/config.json
   ```

2. `site/config.json` nach Bedarf anpassen

3. Assets in die entsprechenden Ordner legen:
   - Hintergrundbild: `site/assets/wallpaper/`
   - Icons: `site/assets/icons/`
   - Fonts: `site/assets/fonts/`

4. Starten:
   ```bash
   docker compose up -d
   ```

5. Öffne [http://localhost:8080](http://localhost:8080)

## Konfiguration

Alle Einstellungen erfolgen in `site/config.json` (wird nicht mit Git versioniert):

| Feld | Beschreibung |
|------|-------------|
| `title` | Seitentitel (Browser-Tab) |
| `favicon` | Pfad zum Favicon |
| `wallpaper` | Pfad zum Hintergrundbild |
| `font` | Pfad zu einer Custom Font (optional) |
| `defaultIcon` | Standard-Icon wenn kein Link-Icon gesetzt (optional) |
| `toggleLabels` | Beschriftung des Toggle-Sliders |
| `lists.left` / `lists.right` | Die beiden Linklisten |

Siehe `site/config.example.json` als Vorlage.

## Lizenz

Privat
