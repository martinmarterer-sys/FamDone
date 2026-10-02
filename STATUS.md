# STATUS.md – Projektstatus FamDone

Diese Datei dokumentiert den aktuellen Stand des Projekts **FamDone**.  
Sie soll regelmäßig aktualisiert werden und festhalten:

- was bereits fertig ist
- woran aktuell gearbeitet wird
- welche Entscheidungen getroffen wurden
- was als Nächstes umgesetzt werden soll

---

## 1. Aktueller Stand

### Bereits fertig

- Projektname festgelegt: **FamDone**
- Grundidee und Zweck der Web-App definiert
- Zielgruppe festgelegt:
  - Mama
  - Papa
  - Mina
  - Karl
- Rollenmodell umgesetzt:
  - Admin-Zugang für die Eltern
  - normaler Zugang für alle Familienmitglieder
- Erste funktionsfähige Web-App als `index.html` erstellt
- Web-App über GitHub Pages veröffentlicht
- komplette Benutzeroberfläche auf Deutsch umgesetzt
- Minecraft-inspirierter, eigenständiger Stil umgesetzt
- responsive Grunddarstellung für Desktop, Tablet und Smartphone umgesetzt
- Admin-Bereich mit Passwortschutz umgesetzt
- Aufgaben können erstellt werden
- Aufgaben können bearbeitet werden
- Aufgaben können gelöscht werden
- Verantwortliche können ausgewählt werden
- einmalige Aufgaben werden unterstützt
- tägliche Wiederholungen werden unterstützt
- wöchentliche Wiederholungen werden unterstützt
- monatliche Wiederholungen werden unterstützt
- Aufgaben können von den zugeordneten Familienmitgliedern bestätigt werden
- bei mehreren Verantwortlichen wird angezeigt, wer bereits bestätigt hat und wer noch fehlt
- eine Aufgabe gilt erst als erledigt, wenn alle notwendigen Bestätigungen erfolgt sind
- Datum und Uhrzeit einer Bestätigung werden gespeichert und angezeigt
- Daten werden lokal im Browser über `localStorage` gespeichert
- Filter nach Familienmitglied und Aufgabenstatus sind vorhanden
- `README.md` erstellt
- `REGELN.md` erstellt
- `STATUS.md` erstellt
- `IDEEN.md` erstellt

### Behobener Fehler in dieser Version

Beim ersten Test der Web-App trat folgender Fehler auf:

- Nach dem Anlegen einer Aufgabe wurde die Aufgabe scheinbar nicht gespeichert bzw. nicht korrekt angezeigt.
- Nach der Eingabe einer Aufgabe brach die Darstellung teilweise ab, sodass der Admin-Bereich anschließend nicht mehr normal genutzt werden konnte.

**Ursache:**  
Die Funktion `isTaskActive` wurde an drei Stellen direkt an `Array.filter()` übergeben. `filter()` übergibt neben der Aufgabe zusätzlich den Array-Index. Dieser Index wurde von `isTaskActive` fälschlich als Datumswert verwendet. Sobald mindestens eine Aufgabe vorhanden war, konnte dadurch ein JavaScript-Fehler entstehen und die weitere Darstellung abbrechen.

**Korrektur:**  
Die drei Filteraufrufe verwenden jetzt jeweils eine eigene Callback-Funktion und übergeben ausschließlich die Aufgabe an `isTaskActive`. Dadurch bleibt der vorgesehene Datums-Standardwert erhalten.

---

## 2. Woran aktuell gearbeitet wird

FamDone befindet sich jetzt in der **ersten Test- und Fehlerbehebungsphase**.

Der Schwerpunkt liegt aktuell auf:

- praktischem Testen der bereits vorhandenen Funktionen
- Beheben einzelner Fehler nach dem Kursprinzip „eine Sache verbessern“
- Sicherstellen, dass Aufgaben zuverlässig angelegt und gespeichert werden
- Sicherstellen, dass der Admin-Bereich nach dem Speichern weiterhin nutzbar bleibt
- Prüfen, ob gespeicherte Daten nach einem Neuladen erhalten bleiben

---

## 3. Getroffene Entscheidungen

### Technische Entscheidungen

- FamDone bleibt eine **Web-App in einer einzigen HTML-Datei**.
- HTML, CSS und JavaScript bleiben vollständig in `index.html` eingebettet.
- Es werden keine externen Bibliotheken, Frameworks oder CDNs verwendet.
- Es werden keine zusätzlichen CSS- oder JavaScript-Dateien benötigt.
- Die Daten werden lokal im Browser gespeichert.
- Für die Speicherung wird `localStorage` verwendet.
- Ein Backend oder eine externe Datenbank wird vorerst nicht eingesetzt.
- Bestehende funktionierende Bereiche werden bei Fehlerkorrekturen möglichst nicht verändert.

### Sprachliche Entscheidungen

- Die gesamte Oberfläche bleibt auf **Deutsch**.
- Texte sollen einfach, familienfreundlich und auch für Kinder verständlich sein.

### Nutzer und Rollen

- Familienmitglieder:
  - Mama
  - Papa
  - Mina
  - Karl
- Es gibt einen Admin-Modus.
- Der Admin-Bereich wird durch ein Passwort geschützt.
- Das Admin-Passwort ist nur für die Eltern gedacht.
- Normale Nutzer benötigen kein Passwort.
- Normale Nutzer dürfen Aufgaben ansehen und bestätigen.

### Aufgabenlogik

Aufgaben können:

- einmalig sein
- täglich wiederholt werden
- wöchentlich wiederholt werden
- monatlich wiederholt werden

Jede Aufgabe enthält mindestens:

- Titel
- verantwortliche Person oder Personen
- Status
- optional ein Datum
- optional eine Wiederholung

Beim Bestätigen werden automatisch gespeichert:

- Datum
- Uhrzeit

Wenn mehrere Personen eine Aufgabe bestätigen müssen, wird sichtbar:

- wer bereits bestätigt hat
- wer noch bestätigen muss

Eine Aufgabe gilt erst als vollständig erledigt, wenn alle vorgesehenen Bestätigungen erfolgt sind.

### Designentscheidung

- Der Look bleibt Minecraft-inspiriert.
- Das Design bleibt eigenständig.
- Es werden keine originalen Minecraft-Grafiken, Logos, Texturen oder Sounds verwendet.
- Lesbarkeit und Bedienbarkeit haben Vorrang vor Dekoration.

---

## 4. Aktuell zu prüfen

Nach Einspielen der korrigierten `index.html` sollen gezielt folgende Punkte getestet werden:

1. Admin-Bereich öffnen.
2. Neue Aufgabe anlegen.
3. Prüfen, ob die Aufgabe sofort in der Übersicht erscheint.
4. Prüfen, ob der Admin-Bereich nach dem Speichern weiterhin sichtbar und nutzbar bleibt.
5. Direkt eine zweite Aufgabe anlegen.
6. Seite neu laden.
7. Prüfen, ob beide Aufgaben noch vorhanden sind.
8. Eine Aufgabe bearbeiten.
9. Eine Aufgabe löschen.
10. Eine Aufgabe bestätigen und prüfen, ob Datum und Uhrzeit angezeigt werden.

---

## 5. Noch offene Punkte

Folgende Punkte sollen im weiteren Projektverlauf noch getestet, entschieden oder später umgesetzt werden:

- vollständiger Test der täglichen Wiederholung über einen Tageswechsel
- vollständiger Test der wöchentlichen Wiederholung über einen Wochenwechsel
- vollständiger Test der monatlichen Wiederholung über einen Monatswechsel
- Verhalten bei zukünftigen einmaligen Aufgaben
- Verhalten bei überfälligen Aufgaben
- langfristiger Verlauf oder Archiv für erledigte Aufgaben
- Datensicherung oder Exportmöglichkeit
- später eventuell Nutzung auf mehreren Geräten mit gemeinsamem Datenstand
- später eventuell echtes Login und Backend
- weitere Ideen aus `IDEEN.md`

---

## 6. Als Nächstes

Der nächste Schritt ist **nicht sofort eine neue Funktion**, sondern zuerst der erneute Test der korrigierten Version.

Wenn der Fehler behoben ist:

1. korrigierte `index.html` in GitHub übernehmen
2. `STATUS.md` in GitHub aktualisieren
3. Änderungen committen
4. GitHub Pages kurz aktualisieren lassen
5. Web-App neu laden
6. Aufgabenanlage erneut testen
7. bei einem weiteren Problem wieder genau einen Fehler oder Verbesserungswunsch bearbeiten

---

## 7. Statusübersicht

**Projektphase:** Erste Test- und Fehlerbehebungsphase  
**Web-App programmiert:** Ja  
**Über GitHub Pages veröffentlicht:** Ja  
**README vorhanden:** Ja  
**Dauerregeln vorhanden:** Ja  
**Statusdatei vorhanden:** Ja  
**Ideensammlung vorhanden:** Ja  
**Admin-Bereich vorhanden:** Ja  
**Aufgabenverwaltung vorhanden:** Ja  
**Lokale Datenspeicherung vorhanden:** Ja  
**Aktuell behobener Fehler:** Aufgabenanlage verursachte JavaScript-Abbruch durch falsche Verwendung von `isTaskActive` als `filter()`-Callback  
**Nächster Schritt:** Korrigierte Version in GitHub übernehmen und Aufgabenanlage erneut testen
