# Forschungsarbeit: IT-Projektmanagement und KI

Dieses Projekt enthaelt die LaTeX-Vorlage fuer die Forschungsarbeit von Robin Ladwig und Patrick Koch.

## Thema

Die Entwicklung des IT-Projektmanagements von klassischen linearen Ansaetzen zu agilen Vorgehensmodellen - Der Einfluss kuenstlicher Intelligenz auf gegenwaertige und zukuenftige Projektpraktiken

## Projektstruktur

- `Arbeit.tex`: Hauptdatei. Diese Datei in VS Code oeffnen und kompilieren.
- `latex/`: Einzelne Kapitel und Einstellungen der Arbeit.
- `latex/preamble/commands.tex`: Stammdaten wie Titel, Autor, Studiengang, Pruefer und Matrikelnummern.
- `references.bib` und `seminar-lit.bib`: Literaturdatenbanken fuer Quellen.
- `bilder/`: Abbildungen fuer die Arbeit.
- `Input/`: Aufgabenstellung, Skripte und sonstige Modulunterlagen.
- `Arbeit.pdf`: erzeugte PDF-Datei.

## Wichtige Stellen zum Ausfuellen

Die persoenlichen Daten stehen in:

`latex/preamble/commands.tex`

Dort muessen spaeter noch ergaenzt werden:

- Matrikelnummer Robin
- Matrikelnummer Patrick
- Abgabedatum
- falls noetig weitere formale Angaben

## Arbeiten in VS Code

Empfohlene Installation:

- Visual Studio Code
- Extension: LaTeX Workshop
- MiKTeX
- Strawberry Perl, damit `latexmk` funktioniert

Zum Erzeugen der PDF:

1. Den gesamten Projektordner in VS Code oeffnen.
2. `Arbeit.tex` oeffnen.
3. Mit `Ctrl + Alt + B` kompilieren.
4. Mit `Ctrl + Alt + V` die PDF-Vorschau oeffnen.

Wenn eine Fehlermeldung kommt, in VS Code unter `View > Output > LaTeX Workshop` nachsehen.

## Typischer Arbeitsablauf

1. Nur in den Kapiteldateien unter `latex/` schreiben.
2. Nach groesseren Aenderungen `Ctrl + Alt + B` ausfuehren.
3. PDF kontrollieren.
4. Quellen zuerst in `.bib` eintragen.
5. Quellen dann im Text mit `\cite{...}` zitieren.

## Kapiteldateien

- `latex/00-Zusammenfassung.tex`
- `latex/01-Einleitung.tex`
- `latex/02-Kapitel2.tex`
- `latex/03-Kapitel3.tex`
- `latex/04-Forschungsdesign.tex`
- `latex/05-KI-Projektpraktiken.tex`
- `latex/06-Diskussion.tex`
- `latex/08-ZusammenfassungUndAusblick.tex`
- `latex/anhang.tex`

Die Gliederung ist aktuell als Arbeitsstruktur angelegt. Inhalte, Forschungsfrage, Methode, Auswertung und Literatur muessen noch ausgearbeitet werden.

## Hinweise fuer Zusammenarbeit

- Nicht gleichzeitig dieselbe Datei bearbeiten, wenn ihr OneDrive/SharePoint nutzt.
- Nach jeder groesseren Aenderung kurz kompilieren.
- Fehlermeldungen nicht ignorieren, weil spaetere Fehler oft Folgefehler sind.
- Keine Formatierung manuell mit Leerzeichen bauen. Ueberschriften, Listen, Tabellen und Abbildungen immer mit LaTeX-Befehlen setzen.

## GitHub-Anleitung fuer Robin

Diese Schritte sind fuer die Zusammenarbeit mit GitHub gedacht. Wichtig ist: Erst aktuelle Version holen, dann arbeiten, dann eigene Aenderungen hochladen.

### Einmalige Einrichtung

Robin braucht lokal:

- Git
- Visual Studio Code
- MiKTeX
- Strawberry Perl
- VS-Code-Extension: LaTeX Workshop

Das Repository wird einmalig von GitHub heruntergeladen:

```powershell
git clone https://github.com/DEIN_USERNAME/Forschungsprojekt_Semster_5_Projektmanagement_KI.git
```

Danach den heruntergeladenen Ordner in VS Code oeffnen.

### Vor jedem Arbeiten: aktuelle Version holen

Bevor Robin etwas bearbeitet, soll er im VS-Code-Terminal in den Projektordner gehen und ausfuehren:

```powershell
git checkout robin
git pull origin robin
```

Wenn Robin Aenderungen von `main` in seinen Branch holen soll:

```powershell
git checkout robin
git pull origin main
```

Danach erst Dateien bearbeiten.

### Beim Arbeiten

Robin sollte moeglichst nur die Dateien bearbeiten, die ihm zugeteilt wurden, zum Beispiel:

- `latex/02-Kapitel2.tex`
- `latex/03-Kapitel3.tex`
- einzelne Quellen in `references.bib`

Nicht gleichzeitig mit Patrick dieselbe Kapiteldatei bearbeiten. Dadurch entstehen weniger Git-Konflikte.

Nach groesseren Aenderungen:

```powershell
Ctrl + Alt + B
```

Damit prueft Robin, ob die LaTeX-Datei noch kompiliert.

### Eigene Aenderungen speichern und hochladen

Wenn Robin fertig ist oder einen Zwischenstand sichern moechte:

```powershell
git status
git add .
git commit -m "Bearbeite Kapitel 2"
git push origin robin
```

Die Commit-Nachricht soll kurz beschreiben, was geaendert wurde, zum Beispiel:

```powershell
git commit -m "Ergaenze Vergleich Wasserfall und Scrum"
```

### Wenn Git meldet, dass zuerst gepullt werden muss

Dann hat jemand anderes in der Zwischenzeit etwas hochgeladen. Robin soll dann ausfuehren:

```powershell
git pull origin robin
```

Falls dabei ein Konflikt entsteht, nicht einfach blind loeschen. Dann Patrick Bescheid sagen und gemeinsam die betroffene Datei pruefen.

### Was Robin nicht committen sollte

Diese Dateien entstehen automatisch beim Kompilieren und gehoeren normalerweise nicht in Git:

- `Arbeit.pdf`
- `.aux`
- `.log`
- `.bbl`
- `.blg`
- `.fdb_latexmk`
- `.synctex.gz`

Sie werden durch `.gitignore` bereits ausgeschlossen. Wenn `git status` nur solche Dateien zeigt, muss Robin sie nicht hochladen.

### Kurzer Standardablauf

Der normale Ablauf ist:

```powershell
git checkout robin
git pull origin robin

# Dateien bearbeiten
# PDF mit Ctrl + Alt + B pruefen

git status
git add .
git commit -m "Kurze Beschreibung der Aenderung"
git push origin robin
```
