# LaTeX-Cheatsheet fuer die Hausarbeit

Dieses Cheatsheet zeigt die wichtigsten LaTeX-Befehle fuer diese Forschungsarbeit.

## Text schreiben

Normale Abschnitte werden einfach als Text geschrieben.

Ein neuer Absatz entsteht durch eine Leerzeile im Quelltext.

```tex
Dies ist der erste Absatz.

Dies ist der zweite Absatz.
```

## Ueberschriften

```tex
\section{Einleitung}
\subsection{Problemstellung}
\subsubsection{Zielsetzung}
```

Nicht selbst nummerieren. LaTeX erstellt Nummerierung und Inhaltsverzeichnis automatisch.

## Hervorhebungen

```tex
\textbf{fetter Text}
\textit{kursiver Text}
\underline{unterstrichener Text}
```

Sparsam verwenden. Wissenschaftliche Arbeiten sollten ruhig formatiert sein.

## Listen

Aufzaehlung ohne Nummern:

```tex
\begin{itemize}
    \item Klassisches Projektmanagement
    \item Agile Vorgehensmodelle
    \item Kuenstliche Intelligenz
\end{itemize}
```

Nummerierte Liste:

```tex
\begin{enumerate}
    \item Planung
    \item Durchfuehrung
    \item Auswertung
\end{enumerate}
```

## Quellen zitieren

Ein normaler Verweis:

```tex
\cite{autor2024}
```

Ein Satz mit Quelle:

```tex
Agile Methoden reagieren flexibler auf veraenderte Anforderungen \cite{autor2024}.
```

Der Eintrag `autor2024` muss in einer `.bib`-Datei stehen, zum Beispiel in `references.bib`.

Beispiel fuer einen BibTeX-Eintrag:

```bibtex
@book{autor2024,
  author    = {Max Autor},
  title     = {Projektmanagement in der IT},
  year      = {2024},
  publisher = {Beispiel Verlag}
}
```

## Abbildungen einfuegen

Bilddateien gehoeren in den Ordner `bilder/`.

```tex
\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.8\textwidth]{bilder/dateiname.png}
    \caption{Beschreibung der Abbildung}
    \label{fig:beispiel}
\end{figure}
```

Im Text auf die Abbildung verweisen:

```tex
Wie in Abbildung \ref{fig:beispiel} dargestellt, ...
```

Wichtig: Das Label sollte eindeutig sein, zum Beispiel `fig:wasserfallmodell`.

## Tabellen

Einfache Tabelle:

```tex
\begin{table}[htbp]
    \centering
    \caption{Vergleich klassischer und agiler Vorgehensmodelle}
    \label{tab:vergleich}
    \begin{tabular}{lll}
        \hline
        Kriterium & Klassisch & Agil \\
        \hline
        Planung & umfangreich vorab & iterativ \\
        Anforderungen & stabil angenommen & veraenderbar \\
        Steuerung & phasenorientiert & inkrementell \\
        \hline
    \end{tabular}
\end{table}
```

Im Text darauf verweisen:

```tex
Tabelle \ref{tab:vergleich} zeigt die zentralen Unterschiede.
```

## Fussnoten

```tex
Dies ist ein Begriff mit Erklaerung.\footnote{Hier steht die Fussnote.}
```

Fussnoten nur nutzen, wenn die Information den Lesefluss stoeren wuerde.

## Querverweise

Labels koennen fuer Kapitel, Abbildungen und Tabellen genutzt werden.

```tex
\section{Forschungsdesign}
\label{sec:forschungsdesign}

Wie in Kapitel \ref{sec:forschungsdesign} beschrieben, ...
```

Nach neuen Labels manchmal zweimal kompilieren, damit Verweise korrekt angezeigt werden.

## Sonderzeichen

Einige Zeichen haben in LaTeX eine besondere Bedeutung und muessen maskiert werden:

```tex
\%   Prozentzeichen
\&   kaufmaennisches Und
\_   Unterstrich
\#   Raute
```

Beispiel:

```tex
Scrum \& Kanban werden haeufig kombiniert.
```

## Gedankenstrich und Bindestrich

```tex
IT-Projektmanagement      % normaler Bindestrich
klassisch -- agil         % Gedankenstrich
```

## Anfuehrungszeichen

In deutschen Texten am besten:

```tex
\glqq klassisches Projektmanagement\grqq
```

## Abkuerzungen

Beim ersten Auftreten ausschreiben:

```tex
Kuenstliche Intelligenz (KI)
```

Danach kann `KI` verwendet werden.

## Kommentare im Quelltext

Alles nach `%` wird von LaTeX ignoriert.

```tex
% TODO: Quelle ergaenzen
Dieser Satz erscheint in der PDF.
```

## Haeufige Fehler

- Eine geschweifte Klammer `{` oder `}` fehlt.
- Eine Umgebung wurde nicht beendet, zum Beispiel `\begin{figure}` ohne `\end{figure}`.
- Eine Bilddatei liegt nicht im richtigen Ordner.
- Ein `\cite{...}` verweist auf einen nicht vorhandenen BibTeX-Key.
- Sonderzeichen wie `%`, `&` oder `_` wurden nicht maskiert.

## Praktische Regel

Wenn nach einer Aenderung ein Fehler auftritt, zuerst die zuletzt bearbeitete Stelle pruefen. Meistens liegt der Fehler direkt dort oder wenige Zeilen davor.

