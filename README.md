# Imposter – PWA Starter

Diese Mappe ist bereit zum Hosten als Progressive Web App (PWA), funktioniert auf iOS & Android.

## Dateien
- `index.html` – Spiel + PWA-Integration
- `manifest.webmanifest` – PWA-Metadaten/Icons
- `service-worker.js` – Offline-Cache
- `icons/` – 192, 512 und 180 (apple-touch-icon)

## Lokales Testen
> Service Worker funktionieren nur über HTTPS **oder** auf `localhost`.
1. Starte einen lokalen Server im Projektordner:
   - Python: `python3 -m http.server 8000`
   - Node: `npx serve -p 8000` (falls `serve` installiert)
2. Öffne `http://localhost:8000` auf deinem Rechner.

## Auf dem iPhone installieren (empfohlen: HTTPS-Hosting)
1. Deploye den Ordner auf einen Hoster mit **HTTPS** (z. B. GitHub Pages, Netlify, Vercel).
2. Öffne die URL in **Safari** auf dem iPhone.
3. Tippe auf **Teilen** → **Zum Home-Bildschirm** → **Hinzufügen**.

## GitHub Pages (schnell & kostenlos)
1. Neues Repo anlegen und Inhalt pushen.
2. In den Repo-Einstellungen → **Pages** → Branch `main` oder `gh-pages` wählen.
3. Warte, bis die Seite gebaut ist – die URL ist dann `https://<username>.github.io/<repo>/`.
4. Öffne die URL in Safari und füge sie zum Home-Bildschirm hinzu.

## Updates veröffentlichen
- Passe den `CACHE`-Namen in `service-worker.js` (z. B. `imposter-v2`) an, damit Clients neue Assets laden.
- Lade die geänderten Dateien hoch – Nutzer erhalten beim nächsten Laden die neue Version.

## Hinweise zu iOS
- Add-to-Home ist manuell über das Teilen-Menü.
- Offline-Modus funktioniert durch den Service Worker (daher HTTPS/localhost notwendig).
- Hintergrund-Timer/Push sind eingeschränkt; für das Partyspiel reicht der Foreground-Timer.

Viel Spaß!
