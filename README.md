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

