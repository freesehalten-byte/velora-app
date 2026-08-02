# Gemeinsam vom Handy am Projekt arbeiten

## 1. Einmalig durch den Repository-Besitzer

1. Auf GitHub das Repository oeffnen.
2. Unter **Settings > Collaborators > Add people** den GitHub-Benutzernamen des
   Bruders einladen. Er muss die Einladung annehmen.
3. Unter **Settings > Codespaces** Codespaces fuer das Repository erlauben.
4. Optional, aber empfohlen: Unter **Settings > Branches** eine Branch-Protection
   fuer `work` anlegen. Dabei mindestens **Require a pull request before
   merging** aktivieren. So ueberschreibt niemand versehentlich die Arbeit des
   anderen.

Diese Einstellungen koennen nicht durch Dateien im Repository vergeben werden;
sie muessen vom Besitzer auf GitHub vorgenommen werden.

## 2. Codespace auf dem Smartphone oeffnen

1. Chrome oder Safari im Querformat verwenden und bei GitHub anmelden.
2. Auf der Repository-Seite **Code > Codespaces** antippen.
3. **Create codespace on work** waehlen. Die Konfiguration in
   `.devcontainer/devcontainer.json` richtet den Browser-Editor ein.
4. Fuer mehr Platz im Editor kann die Browser-Funktion **Desktopwebsite**
   aktiviert werden. Eine Bluetooth-Tastatur ist hilfreich, aber nicht noetig.

Jede Person sollte einen eigenen Codespace und einen eigenen Branch benutzen.
Ein Codespace ist eine persoenliche Entwicklungsumgebung, kein gemeinsam
gesteuerter Bildschirm.

## 3. Pro Aufgabe einen Branch verwenden

Im Terminal des Codespaces:

```bash
git switch work
git pull
git switch -c name/kurze-beschreibung
```

Beispiele sind `alex/login-fehler` oder `sam/neue-farbe`. Danach Dateien im
Browser-Editor bearbeiten und die Aenderungen sichern:

```bash
git status
git add .
git commit -m "Beschreibe die Aenderung kurz"
git push -u origin HEAD
```

GitHub zeigt danach einen Link zum Erstellen eines Pull Requests. Als Zielbranch
`work` auswaehlen. Die andere Person prueft den Pull Request und fuehrt ihn
zusammen. Vor der naechsten Aufgabe wieder mit einem aktuellen `work` beginnen.

## 4. Live zusammenarbeiten

Ja, ihr koennt auch gleichzeitig im selben Codespace arbeiten. Dafuer ist die
Erweiterung **Live Share** bereits in der Codespace-Konfiguration eingetragen.

### Eine Sitzung starten

1. Eine Person oeffnet ihren Codespace und wartet, bis er vollstaendig gestartet
   ist.
2. In der linken Seitenleiste **Live Share** oeffnen oder in der Befehlspalette
   `Live Share: Start Collaboration Session` auswaehlen.
3. Bei der ersten Nutzung mit dem GitHub-Konto anmelden.
4. Den erzeugten Einladungslink privat an den Bruder schicken. Den Link nicht
   oeffentlich posten: Wer Zugriff auf den Link erhaelt, kann der Sitzung
   beitreten.
5. Der Bruder oeffnet den Link auf seinem Handy, meldet sich bei GitHub an und
   bestaetigt den Beitritt im Browser-Editor.

Beide sehen nun die gleichen Projektdateien und koennen Cursor und Aenderungen
live verfolgen. Der Besitzer der Sitzung kann die Freigabe jederzeit ueber
**Live Share: Stop Collaboration Session** beenden.

### Wichtig bei einer Live-Sitzung

- Nur der Gastgeber commitet und pusht die gemeinsam erstellten Aenderungen.
  Dadurch entstehen keine doppelten oder widerspruechlichen Commits.
- Terminalzugriff nur freigeben, wenn er wirklich gebraucht wird. Niemals
  Passwoerter, Tokens oder andere Geheimnisse im geteilten Terminal anzeigen.
- Live Share ersetzt Git nicht: Nach der Sitzung weiterhin committen, pushen und
  einen Pull Request erstellen.
- Falls Live Share im mobilen Browser nicht sauber bedienbar ist, nutzt zwei
  eigene Codespaces und das Branch-Verfahren aus Abschnitt 3. Das funktioniert
  auch ohne gleichzeitige Bearbeitung.

## 5. Was noch fuer echte App-Entwicklung fehlt

Die vorhandenen Dateien `Velora (1).apk` und `velora.zip` sind Ausgabedateien.
Eine APK kann installiert, aber nicht sinnvoll wie ein Android-Projekt
weiterbearbeitet werden. Der urspruengliche Quellcode muss aus Android Studio,
Flutter, React Native oder dem verwendeten App-Builder exportiert und committed
werden.

Vor dem Hochladen pruefen:

- keine Passwoerter, API-Schluessel, Signing-Keys oder `.env`-Dateien committen;
- den zum Framework passenden `.gitignore` verwenden;
- Build-Ausgaben wie `build/` nicht committen;
- grosse fertige APKs besser als **GitHub Release** bereitstellen.

Sobald der Quellcode vorhanden ist, sollte die Codespace-Konfiguration an das
tatsaechliche Framework angepasst und ein automatischer Build-Test ergaenzt
werden.

## 6. Codespace stoppen und Kosten vermeiden

Nach der Arbeit auf GitHub **Codespaces** oeffnen, beim eigenen Codespace das
Drei-Punkte-Menue waehlen und **Stop codespace** antippen. Nicht mehr benoetigte
Codespaces koennen dort geloescht werden. Vorher immer committen und pushen,
damit keine Arbeit verloren geht.
