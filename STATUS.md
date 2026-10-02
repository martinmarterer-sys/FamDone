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
- Grundidee der Web-App definiert
- Zielgruppe festgelegt:
  - Mama
  - Papa
  - Mina
  - Karl
- Zweck der Anwendung beschrieben
- Rollenmodell festgelegt:
  - Admin-Zugang für die Eltern
  - normaler Zugang für alle Familienmitglieder
- Grundfunktionen beschrieben:
  - Aufgaben erstellen
  - Verantwortliche zuweisen
  - einmalige Aufgaben mit Datum
  - wiederkehrende Aufgaben
  - Aufgaben abhaken
  - Datum und Uhrzeit der Erledigung speichern
- Grunddesign festgelegt:
  - Minecraft-inspiriert
  - eigenständiger Stil ohne originale Minecraft-Assets
- Technische Grundregeln definiert
- `README.md` erstellt
- `REGELN.md` erstellt
- `STATUS.md` erstellt

### Noch nicht umgesetzt

- eigentliche Web-App
- Benutzeroberfläche
- Admin-Bereich
- Aufgabenverwaltung
- Wiederholungslogik
- Speicherung der Daten
- Bestätigungslogik
- responsive Darstellung
- Tests auf Desktop, Tablet und Smartphone

---

## 2. Woran aktuell gearbeitet wird

Aktuell befindet sich FamDone noch in der **Planungs- und Strukturierungsphase**.

Der Schwerpunkt liegt momentan auf:

- klaren Anforderungen
- dauerhaften Entwicklungsregeln
- Definition der Funktionen
- Festlegung der technischen Rahmenbedingungen
- Vorbereitung für die eigentliche Umsetzung der Web-App

Der eigentliche Programmcode der Anwendung wurde noch nicht erstellt.

---

## 3. Getroffene Entscheidungen

### Technische Entscheidungen

- FamDone wird als **Web-App** umgesetzt.
- Die Anwendung soll grundsätzlich aus **einer einzigen HTML-Datei** bestehen.
- HTML, CSS und JavaScript werden in dieser Datei eingebettet.
- Es werden keine externen Bibliotheken oder Frameworks verwendet.
- Es werden keine zusätzlichen CSS- oder JavaScript-Dateien benötigt.
- Die Anwendung soll direkt im Browser funktionieren.
- Die Daten werden zunächst lokal im Browser gespeichert.
- Für die Speicherung soll bevorzugt `localStorage` verwendet werden.
- Ein Backend oder eine externe Datenbank wird vorerst nicht verwendet.

### Sprachliche Entscheidungen

- Die gesamte Oberfläche ist auf **Deutsch**.
- Die Texte sollen einfach und familienfreundlich formuliert sein.
- Die Bedienung soll auch für Kinder verständlich sein.

### Nutzer und Rollen

- Es gibt vier Familienmitglieder:
  - Mama
  - Papa
  - Mina
  - Karl
- Es gibt einen Admin-Modus.
- Der Admin-Bereich wird durch ein Passwort geschützt.
- Das Admin-Passwort ist nur für die Eltern gedacht.
- Normale Nutzer benötigen kein Passwort.
- Normale Nutzer dürfen Aufgaben ansehen und abhaken.

### Aufgabenlogik

Aufgaben können:

- einmalig sein
- täglich wiederholt werden
- wöchentlich wiederholt werden
- monatlich wiederholt werden

Jede Aufgabe soll mindestens enthalten:

- Titel
- verantwortliche Person oder Personen
- Status
- optional ein Datum
- optional eine Wiederholung

Beim Abhaken werden automatisch gespeichert:

- Datum
- Uhrzeit

Wenn mehrere Personen eine Aufgabe bestätigen müssen, soll sichtbar sein:

- wer bereits bestätigt hat
- wer noch bestätigen muss

Eine solche Aufgabe gilt erst als vollständig erledigt, wenn alle notwendigen Bestätigungen erfolgt sind.

### Designentscheidung

- Der Look soll sich an Minecraft orientieren.
- Das Design bleibt jedoch eigenständig.
- Keine originalen Minecraft-Grafiken, Logos, Texturen oder anderen geschützten Inhalte werden übernommen.
- Der Stil soll blockartig, spielerisch und gut lesbar sein.
- Die Benutzerfreundlichkeit hat Vorrang vor Dekoration.

---

## 4. Offene Punkte

Folgende Punkte müssen im weiteren Projektverlauf noch konkret entschieden oder umgesetzt werden:

- genaue Struktur der Startseite
- genaue Darstellung der Familienmitglieder
- Darstellung offener und erledigter Aufgaben
- Aufbau des Admin-Bereichs
- Auswahl und Änderung des Admin-Passworts
- genaue Wiederholungslogik
- Umgang mit überfälligen Aufgaben
- Möglichkeit, Aufgaben nachträglich zu bearbeiten
- Verhalten beim Löschen einer Aufgabe
- genaue Darstellung der Bestätigungen
- Sortierung und Filterung der Aufgaben
- Speicherung von erledigten Aufgaben
- Möglichkeit eines Verlaufs oder Archivs
- Verhalten bei einem neuen Tag
- Verhalten bei wöchentlichen und monatlichen Wiederholungen
- Datensicherung oder Exportmöglichkeit
- eventuell spätere Erweiterung um echtes Login und Backend

---

## 5. Als Nächstes

Der nächste sinnvolle Schritt ist die Erstellung einer ersten funktionsfähigen Version der Web-App.

### Geplante Reihenfolge

1. Grundlayout der Web-App erstellen
2. Minecraft-inspiriertes Design umsetzen
3. Familienübersicht einbauen
4. Aufgabenliste anzeigen
5. Admin-Modus erstellen
6. Aufgaben anlegen können
7. Verantwortliche auswählen können
8. einmalige und wiederkehrende Aufgaben unterstützen
9. Aufgaben abhaken können
10. Datum und Uhrzeit automatisch speichern
11. Bestätigungslogik umsetzen
12. Daten mit `localStorage` speichern
13. Darstellung für Smartphone und Tablet optimieren
14. Funktionen testen
15. Fehler beheben
16. `README.md`, `REGELN.md` und `STATUS.md` aktualisieren

---

## 6. Ziel der nächsten Version

Die erste funktionsfähige Version von FamDone soll mindestens Folgendes ermöglichen:

- Start der Anwendung direkt im Browser
- Anzeige aller Familienmitglieder
- Anzeige offener Aufgaben
- Erstellen neuer Aufgaben im Admin-Modus
- Zuweisen von Verantwortlichen
- Festlegen von einmaligen oder wiederkehrenden Aufgaben
- Abhaken von Aufgaben
- automatische Speicherung von Datum und Uhrzeit
- lokale Speicherung der Daten
- verständliche Anzeige des aktuellen Erledigungsstatus

---

## 7. Statusübersicht

**Projektphase:** Planung / Vorbereitung  
**Web-App programmiert:** Nein  
**README vorhanden:** Ja  
**Dauerregeln vorhanden:** Ja  
**Statusdatei vorhanden:** Ja  
**Grundfunktionen definiert:** Ja  
**Designrichtung definiert:** Ja  
**Technische Basis entschieden:** Ja  
**Nächster Schritt:** Erste funktionsfähige HTML-Version von FamDone erstellen
