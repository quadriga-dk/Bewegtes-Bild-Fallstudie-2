---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
```{code-cell} ipython3
:tags: [remove-cell]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors
```

# 🏆Selbsttest: Wissen und Praxis

````{admonition} Wie nutze ich den Selbsttest?
:class: hinweis, dropdown
Diese Übungsaufgaben dienen Ihrer Selbsteinschätzung und helfen Ihnen, das im Kapitel Gelernte zu reflektieren.

Sie können die Fragen in beliebiger Reihenfolge bearbeiten und die Beantwortung auch mehrfach versuchen. 

**So funktioniert es:**
- Wählen Sie bei jeder Frage die Antwort(en) aus, die Sie für richtig halten
- Lesen Sie das Feedback zu den einzelnen Antwortoptionen sorgfältig durch
- Die Erklärungen helfen Ihnen, Ihr Verständnis zu vertiefen – auch bei korrekten Antworten 

Es erfolgt keine Bewertung oder Speicherung Ihrer Ergebnisse. Nutzen Sie dieses Assessment, um Wissenslücken zu identifizieren und gegebenenfalls die entsprechenden Abschnitte des Kapitels nochmals zu bearbeiten. 

**Geschätzte Zeit**: 20 Minuten

Viel Erfolg!
````


## Aufgabe 1

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

multiple_choice1 = [{
    "question": """Nach Stachowiak und Jannidis (2017) - welche Aspekte charakterisieren ein Modell?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Ein Modell ist immer eine Abbildung, es repräsentiert etwas",
            "correct": True,
            "feedback": """✓ Richtig: Erster Aspekt - Modelle sind immer Abbildungen, sie repräsentieren etwas."""
        },
        {
            "answer": "Ein Modell ist nicht das Original, es weist nur ausgewählte Merkmale auf",
            "correct": True,
            "feedback": """✓ Richtig: Zweiter Aspekt - Modelle sind reduzierte Darstellungen mit ausgewählten Merkmalen."""
        },
        {
            "answer": "Ein Modell hat einen oder mehrere Verwendungszwecke",
            "correct": True,
            "feedback": """✓ Richtig: Dritter Aspekt - Modelle werden für spezifische Zwecke erstellt."""
        },
        {
            "answer": "Ein Modell ist immer eine exakte Kopie des Originals",
            "correct": False,
            "feedback": """× Falsch: Modelle sind explizit keine Kopien, sondern Abstraktionen."""
        }
    ]
}]

display_quiz(multiple_choice1, colors=colors.jupyterquiz)
```

## Aufgabe 2

Bewerten Sie folgende Aussagen zu Datenmodellen:

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false1 = [{
    "question": """Datenmodelle sind objektiv und wertfrei""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt! Nach Drucker enthalten Datenmodelle bestimmte Weltanschauungen, Werte und Werturteile."""
        },
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false1, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false2 = [{
    "question": """Jede Erzeugung von Daten beinhaltet eine Modellierung""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! Drucker betont, dass jede Erzeugung von Daten eine Modellierung beinhaltet."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false2, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false3 = [{
    "question": """Datenmodelle können Weltanschauungen und Werturteile enthalten""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! Modelle sind nicht neutral, sondern spiegeln bestimmte Perspektiven wider."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false3, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false4 = [{
    "question": """Ein Datenmodell legt fest, welche Merkmale des Objekts als charakteristisch gelten""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! Modelle definieren, was als notwendig für die Charakterisierung eines Datenobjekts erachtet wird."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false4, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false5 = [{
    "question": """Existierende Daten sind immer gegeben und nicht gemacht""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt! Daten sind „gemacht“ und nicht „gegeben“ - sie unterliegen bestimmten Konstruktionsprozessen."""
        },
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false5, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false6 = [{
    "question": """Datenmodelle sollten vor ihrer Nutzung analysiert und verstanden werden""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! Drucker empfiehlt die Analyse des Modells vor der Nutzung; nur bei einem Verständnis des zugrundeliegenden Modells ist eine sinnvolle Arbeit mit Daten möglich."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false6, colors=colors.jupyterquiz)
```


## Aufgabe 3

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

multiple_choice3 = [{
    "question": """Welche Aussagen zum OPAC der Filmuniversität sind korrekt?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Das System wurde ursprünglich für Bücher und Zeitschriften konzipiert",
            "correct": True,
            "feedback": """✓ Richtig: Der Online-Katalog wurde ursprünglich für Medien in Schriftform wie Bücher oder Zeitschriften konzipiert, andere Medienarten wurden integriert."""
        },
        {
            "answer": "Die Reihenfolge der Gewerke folgt einer bibliotheksinternen Systematik",
            "correct": True,
            "feedback": """✓ Richtig: Die Reihung der Gewerke in den OPAC-Einträgen zu den Filmtiteln folgt einer bibliotheksintern festgelegten Abfolge."""
        },
        {
            "answer": "Pro Film können maximal 25 Personen erfasst werden",
            "correct": True,
            "feedback": """✓ Richtig: Im Eingabeformular des OPAC können bis zu 25 Personen je Film erfasst werden."""
        },
        {
            "answer": "Die Eingabe der filmografischen Daten orientiert sich an der komplexen Norm EN 15907",
            "correct": False,
            "feedback": """× Falsch: Die Eingabe orientiert sich an der Norm EN 15744 (Mindestsatz von Metadaten für Kinofilme), nicht an der komplexen EN 15907."""
        }
    ]
}]

display_quiz(multiple_choice3, colors=colors.jupyterquiz)
```

## Aufgabe 4

**Szenario:** Sie erhalten einen OPAC-Datenauszug mit folgenden Beispieleinträgen:

```
ID: 12458
Titel: Stilles Land
Jahr: 1992
sonstige Person: Dresen, Andreas [Regie] ; Höfer, Andreas [Kamera] ; Stieler, Laila [Drehbuch]
Umfang/Format: 35mm, 2690m, 98 Min, 24fps, Farbe, Mono
Schlagwort: Spielfilm ; Drama/A
Stichwörter: Wende, Provinz, Theater, Kleinstadt
```

Analysieren Sie diese Datenstruktur:
1. Identifizieren Sie Probleme für die maschinelle Auswertung
2. Bewerten Sie die Datenqualität des Auszugs

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('Assessment_4')
```

````{admonition} Musterlösung
:class: solution, dropdown

**1. Probleme für die maschinelle Auswertung:**
- In einem Feld sind mehrere Werte vorhanden (sonstige Person, Umfang/Format, Schlagwort, Stichwörter)
- Verschiedene Trennzeichen (Semikolon, Komma)
- Komma wird auch als Zeichen in Einträgen verwendet (z.B. Personenangabe Nachname, Vorname)
- Gemischte Informationstypen in einem Feld (Format, Länge, Dauer, etc. in Umfang/Format)
- Strukturierte und unstrukturierte Informationen sind vermischt
- Leerzeichen um die Trennzeichen sind inkonsistent

**2. Beurteilung der Datenqualität:**
- Eine ID ist vorhanden, dies ist wichtig für die eindeutige Identifikation eines Eintrages
- Eine Jahreszahl für eine zeitliche Einordnung ist vorhanden
- Die Gewerke sind klar zugeordnet
- Die Schlagworte folgen einem kontrollierten Vokabular, dadurch wird eine einheitliche Beschreibung vereinfacht
- Die Stichwörter sind frei vergeben; dies kann zu Inkonsistenzen führen aber auch individuelle Beschreibungen ermöglichen
- Technische Angaben zum Filmwerk sind vorhanden
````

## Aufgabe 5

**Szenario:** In einem Datensatz finden Sie folgende problematische Jahresangaben:

```
[1995]
ca. 1997
1990/91
1993-1995
1999
```

Entwickeln Sie eine systematische Bereinigungsstrategie mit *OpenRefine*:
1. Identifizierung der Probleme 
2. Notwendige Bereinigungsschritte 
3. Verwendung geeigneter *OpenRefine*-Funktionen

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('Assessment_-5')
```

````{admonition} Musterlösung
:class: solution, dropdown

**1. Probleme identifizieren:**
- Eckige Klammern bei Jahren
- "ca." Zusätze für Schätzungen
- Verschiedene Trennzeichen für Jahresbereiche (/, -)
- Abgekürzte Jahreszahlen (91 statt 1991)

**2. Bereinigungsschritte:**
- Übersicht über die Art der verschiedenen Jahresangaben
- Entfernung der Zusätze (eckige Klammern)
- Normalisierung der Trennzeichen (z.B. ; statt / oder -)
- Ergänzung abgekürzter Jahreszahlen
- Neue Spalte für Schätzungsangaben erstellen
- Aufteilung in separate Jahresspalten

**3. OpenRefine-Funktionen:**
- Text Facet für Übersicht
- Cluster für ähnliche Einträge
- GREL-Funktionen für Bereinigungen (replace- und contains-Methode)
- „Add column based on this column" für neue Spalte für Schätzungen
- „Split into several columns" für Aufteilung in mehrere Spalten
````

## Aufgabe 6

Bewerten Sie folgende Aussagen zu OpenRefine:

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false1 = [{
    "question": """OpenRefine läuft als lokaler Webserver ohne Internetverbindung""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! OpenRefine läuft lokal, es benötigt dabei keine aktive Internetverbindung."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false1, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false2 = [{
    "question": """Firefox ist der empfohlene Browser für OpenRefine""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt! Für OpenRefine werden WebKit-basierte Browser empfohlen (Chrome, Safari, Edge), Firefox kann Probleme verursachen."""
        },
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false2, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false3 = [{
    "question": """Alle Arbeitsschritte werden automatisch in einer Undo/Redo-Liste dokumentiert""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! Jede Änderung wird in der Undo/Redo-Liste festgehalten, einzelne Schritte können einfach rückgängig gemacht oder an anderer Stelle wiederholt werden."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false3, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false4 = [{
    "question": """Text Facets zeigen nur eindeutige Werte ohne Häufigkeitsangabe""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt! Text Facets zeigen Werte mit ihrer Häufigkeit in grauer Schrift an."""
        },
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false4, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false5 = [{
    "question": """GREL ist eine an JavaScript angelehnte Programmiersprache""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! GREL ist eine an JavaScript angelehnte Programmiersprache, die einfach zu erlernen ist und meist nur wenige Zeilen Code umfasst."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false5, colors=colors.jupyterquiz)
```


## Aufgabe 7

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

multiple_choice7 = [{
    "question": """Welche Aussagen zu Datenformaten sind korrekt?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "CSV steht für \"Comma Separated Values\"",
            "correct": True,
            "feedback": """✓ Richtig: CSV ist die Standardabkürzung für komma-getrennte Werte."""
        },
        {
            "answer": "Das Pipe-Zeichen | ist problematisch als Trennzeichen",
            "correct": False,
            "feedback": """× Falsch: Pipe ist ein gutes Trennzeichen, da es selten in Texten vorkommt."""
        },
        {
            "answer": "Kommas in Filmtiteln können beim CSV-Import-Probleme verursachen",
            "correct": True,
            "feedback": """✓ Richtig: Kommas in Titeln würden fälschlicherweise als Trennzeichen interpretiert."""
        },
        {
            "answer": "UTF-8 ist die empfohlene Zeichenkodierung",
            "correct": True,
            "feedback": """✓ Richtig: UTF-8 wird als Webstandard empfohlen."""
        }
    ]
}]

display_quiz(multiple_choice7, colors=colors.jupyterquiz)
```

## Aufgabe 8

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

single_choice8 = [{
    "question": """Welche Aussage zu Facets ist NICHT korrekt?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Text Facets zeigen alle Einträge einer Spalte mit ihrer Häufigkeit",
            "correct": False,
            "feedback": """× Dies ist korrekt: Text Facets bündeln identische Einträge und zeigen deren Anzahl."""
        },
        {
            "answer": "Numeric Facets funktionieren nur mit Zahlen",
            "correct": False,
            "feedback": """× Dies ist korrekt: Numeric Facets sind nur auf Zahlen ausgelegt."""
        },
        {
            "answer": "Mehrere Facets können gleichzeitig aktiv sein",
            "correct": False,
            "feedback": """× Dies ist korrekt: Verschiedene Facets können kombiniert werden."""
        },
        {
            "answer": "Text Facets sind standardmäßig numerisch sortiert",
            "correct": True,
            "feedback": """✓ Richtig - dies ist NICHT korrekt: Text Facets sind standardmäßig alphabetisch, nicht numerisch sortiert."""
        }
    ]
}]

display_quiz(single_choice8, colors=colors.jupyterquiz)
```

## Aufgabe 9

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

multiple_choice9 = [{
    "question": """Welche Aussagen zu GREL sind korrekt?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "GREL steht für \"General Refine Expression Language\"",
            "correct": True,
            "feedback": """✓ Richtig: "General Refine Expression Language" ist der vollständige Name der Sprache."""
        },
        {
            "answer": "GREL-Code wird spaltenübergreifend ausgeführt",
            "correct": False,
            "feedback": """× Falsch: Der Code wird auf jeden einzelnen Eintrag in der Spalte identisch angewendet, nicht über mehrere Spalten hinweg."""
        },
        {
            "answer": "Das Wort \"value\" repräsentiert einzelne Einträge",
            "correct": True,
            "feedback": """✓ Richtig: "value" repräsentiert die einzelnen Einträge in der Spalte."""
        },
        {
            "answer": "Mehrere Methoden können hintereinander gereiht werden",
            "correct": True,
            "feedback": """✓ Richtig: Mehrere Methoden können hintereinander gereiht und nacheinander ausgeführt werden. Beispiel: "value.replace().replace()"."""
        }
    ]
}]

display_quiz(multiple_choice9, colors=colors.jupyterquiz)
```

## Aufgabe 10

Bewerten Sie folgende Aussagen zu GREL-Methoden:

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false1 = [{
    "question": """replace("old", "new") ersetzt einen Textteil durch einen anderen""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! replace() ersetzt Textteile: value.replace("/", " ; ")"""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false1, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false2 = [{
    "question": """contains(„text") gibt immer einen Textwert zurück""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt! contains() gibt Boolean-Werte zurück, also true oder false: value.contains(„ca.") → true/false"""
        },
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false2, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false3 = [{
    "question": """match(/pattern/) arbeitet mit Regular Expressions""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! match() arbeitet mit Regex-Mustern: value.match(/(Go).*/)"""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false3, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false4 = [{
    "question": """toLowercase() wandelt Text in Kleinbuchstaben um""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! toLowercase() erzeugt Kleinschreibung: "value.toLowercase()" """
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false4, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false5 = [{
    "question": """Regular Expressions werden in GREL mit Schrägstrichen /.../ markiert""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! In GREL werden statt Anführungszeichen Schrägstriche für Regex verwendet."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false5, colors=colors.jupyterquiz)
```
