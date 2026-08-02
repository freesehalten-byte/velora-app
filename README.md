# Velora

Dieses Repository ist als gemeinsamer Arbeitsbereich fuer die Entwicklung von
Velora vorbereitet. Es kann auch auf einem Smartphone ueber einen GitHub
Codespace geoeffnet werden.

## Auf dem Handy starten

1. Die Repository-Seite in Chrome oder Safari oeffnen und bei GitHub anmelden.
2. **Code** > **Codespaces** > **Create codespace on work** waehlen.
3. Im Editor unten links pruefen, dass der eigene Branch ausgecheckt ist.
4. Aenderungen committen, pushen und anschliessend einen Pull Request nach
   `work` erstellen.

Die einmalige Einrichtung fuer zwei Personen sowie der sichere gemeinsame
Arbeitsablauf sind in [MOBILE_WORKFLOW.md](MOBILE_WORKFLOW.md) beschrieben.

## Koennen wir gleichzeitig zusammenarbeiten?

Ja. Fuer normale Aufgaben arbeitet ihr sicherer in zwei eigenen Codespaces und
Branches. Wenn ihr dagegen gleichzeitig dieselbe Datei sehen und bearbeiten
wollt, startet eine Person im Codespace eine **Live Share**-Sitzung und schickt
der anderen Person den Einladungslink. Die genauen Handy-Schritte stehen im
Abschnitt [Live zusammenarbeiten](MOBILE_WORKFLOW.md#4-live-zusammenarbeiten).

## Gemeinsam mit einem KI-Assistenten arbeiten

Ihr koennt auch von unterschiedlichen Orten aus Aufgaben beschreiben und die
Umsetzung durch einen KI-Assistenten vorbereiten lassen. GitHub bleibt dabei die
gemeinsame, verbindliche Projektquelle: Aufgabe als Issue erfassen, auf einem
eigenen Branch umsetzen lassen und den Pull Request durch die andere Person
pruefen lassen. Der genaue Ablauf steht in
[AI_WORKFLOW.md](AI_WORKFLOW.md).

> **Wichtig:** Momentan enthaelt das Repository nur die fertige APK und ein ZIP
> mit derselben APK, aber keinen bearbeitbaren App-Quellcode. Um die App wirklich
> weiterzuentwickeln, muss das Android-Projekt (zum Beispiel mit `app/`,
> `gradle/` und den Gradle-Dateien) in dieses Repository uebernommen werden.
