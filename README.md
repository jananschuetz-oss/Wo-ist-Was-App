# Abgelegt — als installierbare App über GitHub Pages

Diese vier Dateien ergeben zusammen eine installierbare Web-App (PWA).
Alle Einträge (inkl. Fotos) bleiben ausschließlich lokal im Browser des
jeweiligen Geräts gespeichert — GitHub liefert nur den Code aus, sieht
und speichert keine deiner Daten.

## Dateien in diesem Ordner

- `index.html` — die App selbst
- `manifest.json` — App-Name, Icon, Startmodus
- `sw.js` — Service Worker (Offline-Zugriff)
- `icons/` — App-Icons in drei Größen

## Einrichtung (einmalig)

1. Lege in deinem GitHub-Account ein **neues Repository** an (z. B. `abgelegt`).
   Öffentlich oder privat — für GitHub Pages im kostenlosen Plan muss es
   **öffentlich** sein, sonst ist die Seite nicht über eine normale URL erreichbar.
2. Lade **alle Dateien aus diesem Ordner** (inkl. des `icons`-Unterordners,
   mit der Ordnerstruktur erhalten) in das Repository hoch — z. B. per
   Drag & Drop im Browser auf der GitHub-Seite des Repos, oder per
   `git add . && git commit -m "Abgelegt App" && git push`.
3. Im Repository: **Settings → Pages**.
4. Unter „Build and deployment" → „Source" die Option **„Deploy from a branch"**
   wählen, als Branch **`main`** und als Ordner **`/ (root)`**.
5. Speichern. Nach ein bis zwei Minuten ist die App erreichbar unter:

   `https://DEIN-BENUTZERNAME.github.io/DEIN-REPO-NAME/`

## Auf dem Handy installieren

- **Android/Chrome:** Seite öffnen → Chrome zeigt entweder automatisch ein
  „Installieren"-Angebot, oder du tippst in der App selbst auf den Button
  „App installieren", sobald er erscheint.
- **iPhone/Safari:** Seite öffnen → Teilen-Symbol → „Zum Home-Bildschirm".

Danach öffnet sich die App über ihr eigenes Icon, im Vollbild, ohne
Adressleiste — und funktioniert auch offline, weil der Service Worker
die App-Hülle zwischenspeichert.

## Falls du die App später änderst

Wenn du am Code etwas anpassen lässt und neu hochlädst: In `sw.js` die
Zahl in `abgelegt-cache-v1` um eins erhöhen (z. B. `v2`), damit Geräte,
die die App schon installiert haben, die neue Version laden statt die
zwischengespeicherte alte.
