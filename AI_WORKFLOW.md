# Zu zweit aus der Ferne mit einem KI-Assistenten arbeiten

Ja, ihr koennt an verschiedenen Orten sein und beide mit einem KI-Assistenten am
gleichen GitHub-Projekt arbeiten. Wichtig ist, GitHub als gemeinsame Quelle zu
verwenden. Zwei getrennte Chats teilen ihren Verlauf und ihre Erinnerungen nicht
automatisch miteinander.

## Voraussetzungen

- Beide Personen haben mit ihrem eigenen GitHub-Konto Zugriff auf das
  Repository.
- Der verwendete KI-Arbeitsbereich hat Zugriff auf das Repository und darf
  Branches pushen sowie Pull Requests vorbereiten.
- Der bearbeitbare App-Quellcode liegt im Repository. Mit der vorhandenen APK
  allein kann der Assistent die App nicht verlaesslich weiterentwickeln.

Ob ein Assistent wirklich zu GitHub pushen kann, haengt von der Verbindung und
den vergebenen GitHub-Rechten ab. Ohne eingerichtetes GitHub-Repository oder
Anmeldung kann er nur lokale Commits beziehungsweise einen Patch vorbereiten.

## Empfohlener Ablauf pro Aufgabe

### 1. Aufgabe auf GitHub festhalten

Unter **Issues > New issue > Aufgabe fuer den KI-Assistenten** ein Issue
erstellen. Ziel, gewuenschtes Verhalten und Abnahmekriterien moeglichst konkret
eintragen. Screenshots koennen direkt an das Issue angehaengt werden.

### 2. Dem Assistenten einen eindeutigen Auftrag geben

Eine Person startet einen neuen Arbeitsauftrag und schreibt beispielsweise:

```text
Bearbeite Issue #12 im Repository velora-app.
Erstelle dafuer einen eigenen Branch, teste die Aenderung,
committe sie und bereite einen Pull Request nach work vor.
Veraendere nichts ausserhalb dieser Aufgabe.
```

Falls der Assistent das Issue nicht selbst lesen kann, den gesamten Issue-Text
in den Chat kopieren. Keine Passwoerter, Zugriffstoken, Signing-Keys oder andere
Geheimnisse in einen Chat oder ein Issue schreiben.

### 3. Nicht dieselbe Aufgabe doppelt starten

Im Issue kurz kommentieren, wer die Umsetzung gestartet hat. Die zweite Person
kann waehrenddessen ein anderes Issue bearbeiten, sollte aber nicht parallel
denselben Branch durch einen zweiten Assistenten veraendern lassen.

### 4. Pull Request gemeinsam pruefen

Der Assistent soll seine Arbeit nicht direkt ungeprueft in `work` zusammenfuehren.
Die andere Person prueft im Pull Request mindestens:

- Sind die Abnahmekriterien des Issues erfuellt?
- Wurden nur passende Dateien veraendert?
- Sind Tests erfolgreich und nachvollziehbar dokumentiert?
- Sind keine Geheimnisse oder grossen Build-Dateien enthalten?

Erst danach wird der Pull Request zusammengefuehrt und das Issue geschlossen.

## Was zwischen zwei Chats geteilt wird

Geteilt werden nur Informationen, die im Repository gespeichert oder auf GitHub
festgehalten wurden, zum Beispiel Issues, Commits, Branches und Pull Requests.
Der persoenliche Chatverlauf des Bruders ist in einem anderen Chat nicht
automatisch sichtbar. Deshalb gehoeren Entscheidungen und offene Punkte in das
jeweilige GitHub-Issue oder in den Pull Request.

## Einfache Aufgabenverteilung

- **Person A:** Issue anlegen und Abnahmekriterien festlegen.
- **KI-Assistent:** Code aendern, Tests ausfuehren, committen und Pull Request
  vorbereiten.
- **Person B:** Pull Request auf dem Handy pruefen und freigeben.
- Bei der naechsten Aufgabe koennen die Rollen getauscht werden.

So koennt ihr beide von ueberall arbeiten, ohne denselben Chat oder denselben
Codespace gleichzeitig offen halten zu muessen.
