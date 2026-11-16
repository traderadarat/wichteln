# Wichteln

Kleine Web-App fürs Familien-Wichteln über WhatsApp.

## So funktioniert es

1. **Organisator** öffnet die Seite, trägt die Teilnehmer ein (optional Telefonnummer und Wünsche), legt Budget, Datum, Notiz und Ausschlüsse fest (z. B. Paare ziehen sich nicht).
2. **Lose ziehen:** Die Seite lost zufällig aus. Niemand zieht sich selbst, Ausschlüsse werden eingehalten, auf Wunsch beschenkt sich niemand gegenseitig.
3. **Verschicken:** Für jede Person entsteht ein persönlicher Link (WhatsApp-Knopf oder Kopieren). Wer den Link öffnet, sieht einen Umschlag mit Siegel und nach dem Antippen, wen er oder sie beschenkt.

Der Organisator sieht die Zuteilung nicht und kann selbst mitspielen. Unter „Erweitert“ gibt es eine Gesamtliste für den Fall, dass der Organisator nicht mitspielt.

## Persönlich machen

- Überschrift: Feld „Name der Runde“ auf der Seite ausfüllen. Sie steht dann oben und in jedem Link.
- Voreinstellungen (Budget, Datum, Startüberschrift) im `CONFIG`-Block ganz oben im Script von `index.html`.

## Datenschutz

- **Kein Server, keine Anmeldung.** Die Zuteilung steckt verschleiert im persönlichen Link (nach dem `#`). Dieser Teil der Adresse wird vom Browser nicht an den Webserver geschickt.
- **Eingaben des Organisators** (Namen, Telefonnummern, Wünsche) bleiben im `localStorage` seines Browsers. Sie stehen nicht im Code und nicht im Repository.
- **Schriften lokal** im Ordner `fonts/`. Es gibt keine Verbindung zu Google Fonts oder anderen Drittservern.
- **GitHub Pages** protokolliert laut eigener Dokumentation die IP-Adressen der Besucher.
- **noindex:** Suchmaschinen sollen die Seite nicht aufnehmen.
- Die Verschleierung ist kein echter Tresor. Wer es darauf anlegt, kann einen Link entschlüsseln. Für ein Familienspiel reicht es.

## Dateien

- `index.html`: die ganze App (HTML, CSS, JavaScript in einer Datei)
- `fonts/`: Schriften Atkinson Hyperlegible und Bricolage Grotesque, beide unter der SIL Open Font License 1.1 (Lizenztexte liegen daneben)
- `vorschau.jpg`: Vorschaubild für WhatsApp-Links

Erstellt am 16.11.2026.
