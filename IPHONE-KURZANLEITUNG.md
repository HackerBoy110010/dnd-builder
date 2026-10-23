# D&D Charakter-Builder auf dem iPhone einrichten

Für eine einzelne Person ist das hier der beste Weg: **kein Apple Developer Account, kein Mac, keine 99 € pro Jahr.** Die App läuft danach wie eine normale App auf dem Home-Bildschirm, offline, mit allen Daten auf dem Gerät.

Dauer: etwa 10 Minuten.

---

## Schritt 1 – Dateien online bringen (einmalig, von einem beliebigen Computer)

Die App liegt als Web-App vor. Sie braucht eine **https://**-Adresse. Kostenlos geht das so:

### Variante A: Netlify Drop (am schnellsten)

1. Auf **app.netlify.com/drop** gehen, kostenlos anmelden.
2. Den Ordner **`iphone-paket`** (den gesamten Ordner, nicht nur den Inhalt) per Drag & Drop auf die Fläche ziehen.
3. Kurz warten – danach zeigt Netlify eine Adresse an, z. B. `https://xyz123.netlify.app`.
4. Diese Adresse notieren. Unter **Site settings → Change site name** kann man sie lesbarer machen, z. B. `dnd-builder`.

### Variante B: GitHub Pages (kostenlos, kein Karten- oder Vertragskram)

1. Neues Repository auf github.com anlegen (z. B. `dnd-builder`).
2. **Add file → Upload files** und den **Inhalt** des Ordners `iphone-paket` hochladen (also `index.html`, `assets/`, `icons/`, `manifest.webmanifest`, `sw.js`).
3. **Settings → Pages → Source: main / root → Save**.
4. Nach etwa einer Minute ist die Seite unter `https://<nutzer>.github.io/dnd-builder/` erreichbar.

Beide Wege liefern automatisch HTTPS – das ist für die Installation auf dem Home-Bildschirm nötig.

---

## Schritt 2 – Auf dem iPhone installieren

1. **Safari** öffnen (wichtig: Safari, nicht Chrome – nur Safari kann Apps zum Home-Bildschirm hinzufügen).
2. Die Adresse aus Schritt 1 aufrufen.
3. Unten auf das **Teilen-Symbol** (Quadrat mit Pfeil nach oben) tippen.
4. Im Menü nach unten scrollen und **„Zum Home-Bildschirm“** wählen.
5. Oben rechts auf **„Hinzufügen“** tippen.

Fertig. Auf dem Home-Bildschirm erscheint jetzt das App-Symbol „D&D Charakter-Builder“. Beim Start läuft sie **ohne Browser-Leisten im Vollbild**, genau wie eine installierte App.

---

## Schritt 3 – Daten aus der Android-Gruppe übernehmen (optional)

Die iPhone-Version speichert ihre Daten **lokal auf dem iPhone**. Sie ist also unabhängig von deiner Android-App – es gibt keine automatische Synchronisation. So bekommst du trotzdem alle Charaktere und Kampagnen rüber:

**Auf deinem Android-Gerät:**
1. In der App auf **Einstellungen → Backup jetzt speichern**.
2. Die erzeugte Datei (`dnd-backup-….json`) an das iPhone schicken, z. B. per WhatsApp, E-Mail, Google Drive oder AirDrop.

**Auf dem iPhone:**
1. Die App öffnen: **Einstellungen → Backup laden → Backup-Datei auswählen**.
2. Die Datei auswählen. Danach sind alle Charaktere und Kampagnen vorhanden.

Einzelne Charaktere kannst du alternativ als JSON exportieren (im Charakterbogen auf „PDF und JSON“) und im Zielgerät importieren.

> Hinweis: Änderungen auf dem iPhone landen nicht automatisch zurück auf deinem Android-Gerät. Für den Austausch einfach wieder ein Backup exportieren.

---

## Was auf dem iPhone genauso funktioniert

- Charaktere erstellen und bearbeiten, 2014 und 2024
- Unterrassen, Story-Graph, Backstory-Buch mit Kapiteln und eigenem Wortziel
- Kampagnenbuch mit Lore, NPCs, Sessions, Karten und Mindmap
- PDF-Export und JSON-Export
- Design-System mit Hell/Dunkel, Paletten, Atmosphären, Symbolstilen
- Deutsch und Englisch
- Volle Offline-Nutzung nach dem ersten Öffnen

## Was auf dem iPhone anders ist

| Funktion | iPhone |
|---|---|
| **Exakter Ordner für Exporte** | Nicht verfügbar (nur Android). Exporte werden über den iOS-Teilen-Dialog gespeichert – z. B. in „Dateien“, iCloud Drive oder per AirDrop. |
| **Automatische Sicherung** | Es gibt ein Auto-Backup in den App-Daten. Zusätzlich lohnt es sich, ab und zu manuell unter **Einstellungen → Backup** eine Datei zu exportieren. |
| **Installation** | Über Safari „Zum Home-Bildschirm“. Kein App Store nötig. |

---

## Falls die App mal nicht lädt

1. App schließen und neu öffnen.
2. Internet kurz einschalten – danach funktioniert sie wieder offline.
3. In **Einstellungen → Safari → Erweiterte → Website-Daten** die Daten der Seite löschen, dann neu laden.
4. Als letzten Ausweg: App vom Home-Bildschirm löschen und neu hinzufügen. **Vorher** ein Backup exportieren, sonst sind die lokalen Daten weg.

---

## Neue Version einspielen

Wenn es eine neue App-Version gibt:

1. Die neuen Dateien an dieselbe Adresse hochladen (bei Netlify Drop erneut hochladen, bei GitHub Pages die Dateien ersetzen).
2. Auf dem iPhone die App einmal mit Internet öffnen – sie aktualisiert sich beim nächsten Start selbst.
