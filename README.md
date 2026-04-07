# HSOA Astro CMS Template

## Struktur

```
src/
  content/
    home.json              ← Alle Inhalte der Hauptseite
    leistungen/
      immobilienrecht.json ← Immobilienrecht-Unterseite
      [weitere].json       ← Weitere Leistungsseiten (im CMS erstellen)
  pages/
    index.astro            ← Hauptseite
    leistungen/[slug].astro ← Dynamische Leistungsseiten
  layouts/
    Layout.astro           ← HTML-Grundgerüst
public/
  admin/
    config.yml             ← Decap CMS Konfiguration
    index.html             ← CMS Interface
  images/                  ← Hier landen hochgeladene Bilder
```

## Setup

1. Diesen Ordner in dein lokales Repo kopieren (Dateien mergen, nicht ersetzen)
2. `npm run build` testen
3. Git push → Netlify baut automatisch

## Neue Leistungsseite erstellen

Im CMS unter **Leistungsseiten → Neu** → Slug = URL-Pfad (z.B. `apothekenrecht`)
→ Seite erscheint dann automatisch unter `/leistungen/apothekenrecht`

## Bilder einfügen

Alle Felder mit "Bild" in der Bezeichnung öffnen den Bild-Uploader im CMS.
Bilder werden in `public/images/` gespeichert.

## Placeholder-Bilder entfernen

Alle Bild-Felder sind optional (`required: false`). Wenn kein Bild gesetzt ist,
wird der Bild-Container einfach nicht gerendert.
