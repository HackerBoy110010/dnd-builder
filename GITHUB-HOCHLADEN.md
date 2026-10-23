# Auf GitHub hochladen – Schritt für Schritt (ohne Git, nur mit der Maus)

Damit bekommt die App eine **https://**-Adresse und kann auf dem iPhone installiert werden.
Dauer: ca. 2 Minuten. Du brauchst kein Git und kein Terminal.

> Wichtig: Das Repository muss **öffentlich (Public)** sein. GitHub Pages ist kostenlos nur für öffentliche Repositories. Private Repositories brauchen einen kostenpflichtigen Plan.
> Es stehen keine persönlichen Daten darin – nur der Programmcode der App. Die Charaktere und Kampagnen entstehen später lokal auf den Geräten und liegen nicht auf GitHub.

---

## Schritt 1 – Repository anlegen

1. Auf **github.com** anmelden (kostenlosen Account erstellen, falls noch nicht vorhanden).
2. Oben rechts auf **„+“** → **„New repository“**.
3. Unter **Repository name** einen Namen eingeben, z. B. `dnd-builder`.
4. **Public** auswählen.
5. **Wichtig:** Kein Häkchen bei „Add a README file“ setzen. Alle anderen Felder leer lassen.
6. Auf **„Create repository“** klicken.

---

## Schritt 2 – Dateien hochladen

Du landest jetzt auf der Seite mit der Aufschrift „Quick setup“. Dort gibt es den Link **„uploading an existing file“** – darauf klicken.
(Alternativ: **„Add file“** → **„Upload files“**.)

Jetzt den **Inhalt** des Ordners `iphone-paket` auf die große Fläche ziehen:

- `index.html`
- `404.html`
- `README.md`
- `manifest.webmanifest`
- `sw.js`
- der Ordner **`assets`**
- der Ordner **`icons`**

Die Datei `.nojekyll` ist ein versteckte Datei. Wenn sie beim Ziehen nicht mitgeht, ist das **kein Problem** – sie ist nur ein Schutz gegen den GitHub-Vorverarbeiter; die App funktioniert auch ohne sie.

Danach:
1. Unten bei **„Commit changes“** einfach den grünen Button **„Commit changes“** klicken.
2. Kurz warten, bis die Dateien erscheinen.

Wenn GitHub Ordner nicht einzeln annimmt, stattdessen **„Add file“ → „Upload files“** nutzen und dort beide Ordner nacheinander hochladen. Wichtig ist nur, dass `index.html` **ganz oben** im Repository liegt und nicht in einem Unterordner.

---

## Schritt 3 – GitHub Pages einschalten

1. Im Repository oben auf **„Settings“** (Zahnrad) klicken.
2. Links im Menü auf **„Pages“**.
3. Unter **„Build and deployment“** bei **Source** die Option **„Deploy from a branch“** wählen.
4. Unter **Branch** `main` und daneben **`/ (root)`** auswählen.
5. Auf **„Save“** klicken.

Oben erscheint nach kurzer Zeit die Meldung:

**„Your site is live at `https://<dein-name>.github.io/<repository>/`“**

Beim ersten Mal kann es **1–2 Minuten** dauern, bis die Seite erreichbar ist. Wenn du die Adresse aufrufst und die App erscheint, hat alles geklappt.

---

## Schritt 4 – Auf dem iPhone installieren

1. **Safari** öffnen (nur Safari kann das).
2. Die Adresse aus Schritt 3 aufrufen, z. B. `https://dein-name.github.io/dnd-builder/`.
3. Unten auf das **Teilen-Symbol** tippen.
4. **„Zum Home-Bildschirm“** wählen → **„Hinzufügen“**.

Fertig. Die App liegt jetzt mit eigenem Symbol auf dem Home-Bildschirm und läuft im Vollbild.

---

## Später: neue Version hochladen

Wenn es ein Update gibt:

1. Die neuen Dateien im Repository über **„Add file“ → „Upload files“** ersetzen (gleiche Dateinamen verwenden).
2. Unten **„Commit changes“**.
3. Auf dem iPhone die App einmal **mit Internet** öffnen – sie aktualisiert sich beim nächsten Start von selbst.

---

## Falls etwas nicht klappt

| Problem | Lösung |
|---|---|
| Seite zeigt „404“ | Prüfen, ob Pages in den Settings wirklich auf `main` und `/ (root)` steht. Einmal neu laden; beim ersten Mal dauert es bis zu 2 Minuten. |
| Seite lädt, aber bleibt weiß | Prüfen, ob `index.html` **direkt im Hauptverzeichnis** liegt (nicht in einem Unterordner wie `iphone-paket`). |
| Weiß nach dem Öffnen der App auf dem iPhone | Einmal mit Internet öffnen, dann App schließen und neu starten. |
| Icons fehlen auf dem Home-Bildschirm | Prüfen, ob der Ordner `icons` mit hochgeladen wurde. Falls nicht: nachträglich über „Add file → Upload files“ ergänzen. |
| „Add to Home Screen“ wird nicht angeboten | Sicherstellen, dass **Safari** benutzt wird und die Adresse mit `https://` beginnt. |

---

## Hinweis zur Adresse

Die Adresse ist öffentlich aufrufbar, aber ohne den Link findet sie niemand (GitHub Pages wird nicht indexiert, wenn du es nicht verbreitest). Sie enthält keine deiner Spieldaten – diese liegen ausschließlich auf dem jeweiligen Gerät.
