# REGELN.md – Dauerregeln für die Entwicklung von FamDone

Diese Regeln gelten dauerhaft für alle zukünftigen Änderungen, Erweiterungen und Code-Vorschläge für die Web-App **FamDone**, sofern nicht ausdrücklich etwas anderes angegeben wird.

## 1. Sprache und Bedienung

- Die komplette Benutzeroberfläche ist auf **Deutsch**.
- Texte, Buttons, Hinweise, Fehlermeldungen und Bestätigungen werden in einfacher und verständlicher Sprache formuliert.
- Die Bedienung soll auch für Kinder schnell verständlich sein.
- Technische Begriffe werden in der sichtbaren Oberfläche möglichst vermieden.

## 2. Technisches Zielformat

- Die Anwendung besteht grundsätzlich aus **einer einzigen HTML-Datei**.
- HTML, CSS und JavaScript werden vollständig in dieser Datei eingebettet.
- Es werden **keine zusätzlichen JavaScript- oder CSS-Dateien** angelegt.
- Es werden **keine externen Bibliotheken, Frameworks oder CDNs** verwendet.
- Es werden insbesondere keine Frameworks wie React, Vue, Angular, Bootstrap oder Tailwind eingesetzt.
- Die Anwendung soll direkt durch Öffnen der HTML-Datei im Browser funktionieren.

## 3. Datenspeicherung

- Solange nichts anderes festgelegt wird, werden Daten lokal im Browser gespeichert.
- Für die Speicherung wird bevorzugt `localStorage` verwendet.
- Aufgaben, Verantwortlichkeiten, Wiederholungen und Erledigungsinformationen sollen nach einem Neuladen der Seite erhalten bleiben.
- Es werden keine Daten ohne ausdrückliche Anweisung an externe Server oder Dienste übertragen.
- Es werden keine echten personenbezogenen oder sensiblen Daten im Quellcode hinterlegt.

## 4. Benutzer und Rollen

- Standardmäßig gibt es die Familienmitglieder:
  - Mama
  - Papa
  - Mina
  - Karl
- Es gibt zwei Rollen:
  - **Admin**
  - **Normaler Nutzer**
- Nur im Admin-Bereich dürfen Aufgaben erstellt, bearbeitet, gelöscht oder Verantwortliche geändert werden.
- Normale Nutzer dürfen Aufgaben ansehen und als erledigt markieren.
- Änderungen an Rollen oder Familienmitgliedern erfolgen nur auf ausdrückliche Anweisung.

## 5. Admin-Bereich

- Der Admin-Bereich wird durch ein Passwort geschützt.
- Das Passwort soll nicht offen sichtbar in der Benutzeroberfläche angezeigt werden.
- Bei einer reinen Ein-Datei-Lösung darf nicht behauptet werden, dass dieser Passwortschutz technisch vollständig sicher ist.
- Die Lösung ist für den privaten Familiengebrauch gedacht und nicht für sicherheitskritische Anwendungen.
- Eine spätere echte Benutzeranmeldung mit Backend kann als Erweiterung vorgesehen werden, darf aber nicht ohne ausdrücklichen Auftrag eingebaut werden.

## 6. Aufgaben

- Aufgaben können einmalig oder wiederkehrend sein.
- Unterstützte Wiederholungen sollen mindestens sein:
  - einmalig
  - täglich
  - wöchentlich
  - monatlich
- Jede Aufgabe erhält mindestens:
  - Titel
  - Verantwortliche Person oder Personen
  - Status
- Bei einmaligen Aufgaben kann ein Datum vergeben werden.
- Bei wiederkehrenden Aufgaben wird die Wiederholung eindeutig angezeigt.
- Aufgaben sollen nach Erledigung abgehakt werden können.
- Datum und Uhrzeit der Erledigung werden automatisch gespeichert.
- Erledigte Aufgaben müssen klar von offenen Aufgaben unterscheidbar sein.

## 7. Bestätigung und Transparenz

- Der Erledigungsstatus einer Aufgabe muss jederzeit eindeutig erkennbar sein.
- Wenn mehrere Personen eine Aufgabe bestätigen müssen, muss sichtbar sein, wer bereits bestätigt hat und wer noch fehlt.
- Eine Aufgabe gilt erst dann als vollständig erledigt, wenn alle dafür vorgesehenen Bestätigungen erfolgt sind.
- Bereits gespeicherte Erledigungsinformationen dürfen nicht unbeabsichtigt überschrieben werden.

## 8. Design

- Das Design soll **Minecraft-inspiriert** wirken.
- Verwendet werden dürfen beispielsweise:
  - blockartige Flächen
  - pixelartige Formen
  - kantige Buttons
  - erdige oder natürliche Farbtöne
  - spielerische Statusanzeigen
- Es werden keine originalen Minecraft-Grafiken, Logos, Texturen, Sounds oder andere geschützte Assets übernommen.
- Das Design soll eigenständig bleiben und nur an den Stil erinnern.
- Lesbarkeit und Bedienbarkeit haben Vorrang vor Dekoration.

## 9. Responsive Darstellung

- Die Web-App muss auf Desktop, Tablet und Smartphone nutzbar sein.
- Die Oberfläche soll sich automatisch an unterschiedliche Bildschirmgrößen anpassen.
- Buttons und Checkboxen müssen auf Touch-Geräten ausreichend groß sein.
- Wichtige Informationen dürfen auf kleinen Bildschirmen nicht abgeschnitten werden.
- Horizontales Scrollen soll möglichst vermieden werden.

## 10. Benutzerfreundlichkeit

- Häufige Aktionen sollen mit möglichst wenigen Klicks erreichbar sein.
- Vor dem Löschen einer Aufgabe wird eine Bestätigung verlangt.
- Fehlermeldungen sollen verständlich erklären, was zu tun ist.
- Nach erfolgreichen Aktionen soll eine kurze sichtbare Rückmeldung erscheinen.
- Leere Bereiche sollen verständliche Hinweise zeigen, zum Beispiel „Keine offenen Aufgaben“.

## 11. Barrierearme Umsetzung

- Texte müssen einen ausreichenden Kontrast zum Hintergrund haben.
- Buttons und Eingabefelder erhalten klare Beschriftungen.
- Formulare sollen auch mit Tastatur bedienbar sein.
- HTML-Elemente werden möglichst semantisch korrekt verwendet.
- Symbole dürfen wichtige Informationen nicht ausschließlich ohne Text vermitteln.

## 12. Code-Qualität

- Der Code soll übersichtlich, sauber gegliedert und verständlich kommentiert sein.
- HTML, CSS und JavaScript werden innerhalb der einen HTML-Datei klar voneinander getrennt.
- Funktionen sollen möglichst kleine, eindeutige Aufgaben haben.
- Wiederholter Code wird vermieden.
- Bestehende funktionierende Funktionen dürfen bei Erweiterungen nicht unnötig verändert werden.
- Vor jeder größeren Änderung ist zu prüfen, ob bestehende Funktionen dadurch beeinflusst werden.

## 13. Keine unnötige Komplexität

- Es wird immer die einfachste Lösung gewählt, die die gewünschte Funktion zuverlässig erfüllt.
- Keine zusätzlichen Technologien oder Abhängigkeiten ohne klaren Nutzen.
- Kein Backend, keine Datenbank, kein Hosting-Dienst und keine API ohne ausdrücklichen Auftrag.
- Funktionen, die noch nicht benötigt werden, werden nicht vorsorglich eingebaut.

## 14. Bestehende Funktionen schützen

Bei jeder Erweiterung gilt:

1. Bestehende Funktionen zuerst verstehen.
2. Nur die wirklich notwendigen Bereiche ändern.
3. Bestehende Datenstrukturen möglichst beibehalten.
4. Nach Änderungen prüfen, ob bisherige Funktionen weiterhin funktionieren.
5. Keine funktionierenden Bereiche ohne ausdrücklichen Grund komplett neu schreiben.

## 15. Änderungen durch ChatGPT

Wenn ChatGPT Änderungen am Projekt vornimmt:

- Anforderungen aus der aktuellen Aufgabe haben Vorrang.
- Diese Datei `REGELN.md` ist als dauerhafte Entwicklungsrichtlinie zu berücksichtigen.
- Bestehende Anforderungen aus `README.md` bleiben gültig.
- Bei Widersprüchen gilt folgende Priorität:
  1. aktuelle ausdrückliche Anweisung
  2. `REGELN.md`
  3. `README.md`
- Änderungen sollen vollständig umgesetzt und nicht nur beschrieben werden.
- Bei Unsicherheiten soll die einfachste, familienfreundlichste und wartungsärmste Lösung gewählt werden.

## 16. Nicht ohne ausdrücklichen Auftrag ändern

Folgende Grundentscheidungen dürfen nicht selbstständig verändert werden:

- Name der App: **FamDone**
- Sprache der Oberfläche: **Deutsch**
- Grundformat: **eine HTML-Datei**
- keine externen Bibliotheken
- Minecraft-inspirierter, aber eigenständiger Stil
- Admin- und Normalmodus
- Nutzung für die Familie
- lokale Datenspeicherung als Standard
