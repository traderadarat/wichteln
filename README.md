# Wichteln

Kleine Web-App fürs Familien-Wichteln, die selbstständig läuft.

## So funktioniert es

1. Der Organisator schickt einmal den Familien-Link (mit Familien-Code nach `#k-`) in die Familiengruppe.
2. Jede Person trägt sich selbst ein: Name, Wünsche, wen sie nicht ziehen soll, und eine selbst gewählte 4-stellige PIN.
3. Beim Anmeldeschluss lost die App automatisch aus: Niemand zieht sich selbst, Ausschlüsse werden eingehalten, möglichst beschenkt sich niemand gegenseitig.
4. Danach sieht jede Person mit Name und PIN, wen sie beschenkt, samt deren aktuellen Wünschen. Die eigenen Wünsche lassen sich auch nach der Auslosung noch ändern.

## Aufbau

- `index.html`: die Seite (dieses Repository, GitHub Pages)
- Die Anmeldungen speichert eine Google-Apps-Script-Web-App im Google-Konto des Organisators, in einer privaten Google-Tabelle. Der Code dafür liegt bewusst nicht in diesem öffentlichen Repository.
- Ohne gültigen Familien-Code liefert die Schnittstelle keine Daten.

## Datenschutz

- Gespeichert werden nur Name, Wünsche, „zieht nicht“ und die PIN (als SHA-256-Hash mit Salt, nicht im Klartext).
- Keine Telefonnummern, keine E-Mail-Adressen, keine Konten, keine Cookies, keine Werbung, kein Tracking.
- Der Browser merkt sich im `localStorage` nur den Familien-Code und den eigenen Namen.
- Schriften liegen lokal im Ordner `fonts/`, es gibt keine Verbindung zu Google Fonts.
- GitHub Pages und Google protokollieren laut eigener Dokumentation die IP-Adressen der Aufrufe.
- Am eingestellten Löschdatum werden alle Anmeldungen und die Auslosung automatisch gelöscht.
- `noindex`: Suchmaschinen sollen die Seite nicht aufnehmen.

## Dateien

- `index.html`: Seite mit HTML, CSS und JavaScript in einer Datei
- `fonts/`: Atkinson Hyperlegible und Bricolage Grotesque, SIL Open Font License 1.1 (Lizenztexte liegen daneben)
- `vorschau.jpg`: Vorschaubild für WhatsApp-Links

Stand: 16.11.2026
