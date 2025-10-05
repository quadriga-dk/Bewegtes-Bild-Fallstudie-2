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

````{admonition} Hinweis
:class: hinweis
Diese Übungsaufgaben dienen Ihrer Selbsteinschätzung und helfen Ihnen, das im Kapitel Gelernte zu reflektieren.

Sie können die Fragen in beliebiger Reihenfolge bearbeiten und die Beantwortung auch mehrfach versuchen. 

**So funktioniert es:**
- Wählen Sie bei jeder Frage die Antwort(en) aus, die Sie für richtig halten
- Lesen Sie das Feedback zu den einzelnen Antwortoptionen sorgfältig durch
- Die Erklärungen helfen Ihnen, Ihr Verständnis zu vertiefen – auch bei korrekten Antworten 

Es erfolgt keine Bewertung oder Speicherung Ihrer Ergebnisse. Nutzen Sie dieses Assessment, um Wissenslücken zu identifizieren und gegebenenfalls die entsprechenden Abschnitte des Kapitels nochmals zu bearbeiten. 

**Geschätzte Zeit**: XX

Viel Erfolg!
````
### Aufgabe 1

```{code-cell} ipython3
:tags: [remove-input]
display_quiz("../assets/assessment/recherche/recherche_quiz.json", colors = colors.jupyterquiz)
```

### Aufgabe 2

**Szenario:** Sie möchten eine eigene Fallstudie zu studentischen Animationsfilmen der 1990er Jahre durchführen. Beschreiben Sie systematisch Ihr Vorgehen bei der Materialrecherche im OPAC der Filmuniversität.

Ihre Antwort sollte folgende Schritte umfassen:  
1. Datenbankauswahl 
2. Zeitraumeingrenzung
3. Gattungsfilterung
4. Erste Ergebnisbewertung 
5. Verfeinerte Suchstrategien

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('Assessment-1')
```

````{admonition} Musterlösung
:class: solution, dropdown

**1. Datenbankauswahl:**
- Auswahl „Erweiterte Suche" auf der OPAC-Startseite
- Auswahl "Archivkatalog" im Dropdown-Menü „Datenbank"

**2. Zeitraumeingrenzung:**
- Eingabe "1990->1999" im Jahr-Feld
- Beachtung der korrekten Pfeil-Syntax

**3. Gattungsfilterung:**
- Suche nach "Animationsfilm" im Schlagwort-Feld
- Berücksichtigung der Bibliothekssystematik: "Animationsfilm/F"

**4. Erste Ergebnisbewertung:**
- Interpretation der Trefferanzahl
- Mehrfachkatalogisierung reflektieren (Anzahl der Such-Treffer muss nicht der Anzahl der vorhandenen Titel entsprechen)
- Einschätzung der Materialmenge für die Fragestellung: sind genug Titel im Archiv vorhanden

**5. Verfeinerte Suchstrategien:**
- Nutzung weiterer Suchfelder (Stichworte, Titel)
- Kombination verschiedener Suchparameter
````

### Aufgabe 3

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

multiple_choice1 = [{
    "question": """Welche Aussagen zur OPAC-Recherche sind korrekt? (Mehrere Antworten möglich)""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Die Trefferanzahl entspricht immer der exakten Anzahl vorhandener Filme",
            "correct": False,
            "feedback": """× Falsch: Die Trefferanzahl umfasst bibliographische Einträge, nicht unbedingt einzelne Filme. Mehrfachkatalogisierung ist möglich."""
        },
        {
            "answer": "Schlagworte folgen einem kontrollierten Vokabular der Bibliothek",
            "correct": True,
            "feedback": """✓ Richtig: Schlagworte wie "Dokumentarfilm/B" folgen der festgelegten Systematik der Bibliothek."""
        },
        {
            "answer": "Zeiträume werden mit einfachen Bindestrichen \"–\" eingegeben",
            "correct": False,
            "feedback": """× Falsch: Zeiträume werden mit Pfeil-Syntax eingegeben: "1985->1999"."""
        },
        {
            "answer": "Stichworte werden frei vergeben und folgen keiner vorgegebenen Liste",
            "correct": True,
            "feedback": """✓ Richtig: Im Unterschied zu Schlagworten werden Stichworte frei vergeben."""
        },
        {
            "answer": "Einzelne Filme können mehrfach katalogisiert sein",
            "correct": True,
            "feedback": """✓ Richtig: Filme können als Teil von Kompilationen oder auf verschiedenen Datenträgern mehrfach verzeichnet sein."""
        },
        {
            "answer": "Die Vollanzeige enthält nur technische Informationen",
            "correct": False,
            "feedback": """× Falsch: Die Vollanzeige enthält umfassende Informationen: Personen, Gewerke, Projektart, Inhaltsangabe etc."""
        }
    ]
}]

display_quiz(multiple_choice1, colors=colors.jupyterquiz)
```

### Aufgabe 4

Analysieren Sie anhand des Beispiels von Lotte Reiniger (Dang/Junginger, 2024) die Problematik der vermeintlichen "Neutralität" von Metadaten. Gehen Sie dabei auf folgende Aspekte ein:

1. Subjektivität in der Datenerfassung
2. Rolle kontrollierter Vokabulare
3. Historische Kontextualisierung

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('Assessment_C-3')
```

````{admonition} Musterlösung
:class: solution, dropdown

**1. Subjektivität in der Datenerfassung:**
- Verständnis, dass Metadaten Wertvorstellungen widerspiegeln 
- Beispiel: Unterschiedliche Berufsbezeichnungen für dieselbe Person
- Auswirkungen auf sozialen Status und Wahrnehmung

**2. Rolle kontrollierter Vokabulare:**
- Einfluss vorgegebener Begriffslisten auf Beschreibungen
- Ausschluss bestimmter Bezeichnungen durch Systemvorgaben
- Unterschiede zwischen strukturierten Feldern und Freitexten

**3. Historische Kontextualisierung:**
- Metadaten als historische Quellen verstehen
- Erfassung dessen, was zu bestimmten Zeiten als relevant galt
- Notwendigkeit der Kontextualisierung und Reflexion der Entstehungsbedingungen
````

### Aufgabe 5

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="""Welche Schritte sind für die Bildung eines thematischen Teilkorpus zum Thema "Grenze" notwendig? Bringen Sie die Schritte in die richtige Reihenfolge:""",
    descriptions=[
        "Erstellung von Visualisierungen zur zeitlichen Verteilung",
        "Suche nach Stichworten 'Grenze', 'Mauer', 'Grenzübertritt'", 
        "Sichtung ausgewählter Filme zur Vertiefung",
        "Definition der Suchbegriffe und Synonyme",
        "Eingrenzung des Grundkorpus (1985–1999)",
        "Export der Metadaten"
    ],
    options=[
        "1", 
        "2", 
        "3", 
        "4", 
        "5", 
        "6"
    ],
    correct_mapping={
        "Eingrenzung des Grundkorpus (1985–1999)": "1",
        "Definition der Suchbegriffe und Synonyme": "2", 
        "Suche nach Stichworten 'Grenze', 'Mauer', 'Grenzübertritt'": "3",
        "Export der Metadaten": "4",
        "Erstellung von Visualisierungen zur zeitlichen Verteilung": "5",
        "Sichtung ausgewählter Filme zur Vertiefung": "6"
    }
)
```

### Aufgabe 6

Vergleichen Sie die Herangehensweise dieser Fallstudie („Studentische Filme der Filmuniversität zur Wendezeit") mit einer hypothetischen Studie zu "Studentischen Filmen während der COVID-19-Pandemie (2020–2022)". Analysieren Sie:

1. Ähnlichkeiten in der Methodik
2. Unterschiede in den Herausforderungen
3. Anpassungen der Forschungsfragen

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('Assessment_C-5')
```

````{admonition} Musterlösung
:class: solution, dropdown

**1. Ähnlichkeiten in der Methodik:**
- Grundlegende Schritte der Materialrecherche 
- Bedeutung von Metadaten und deren kritische Reflexion
- Notwendigkeit der Operationalisierung
- Kombination quantitativer und qualitativer Ansätze

**2. Unterschiede in den Herausforderungen:**
- Verfügbarkeit digitaler vs. analoger Materialien
- Unterschiedliche rechtliche Rahmenbedingungen
- Temporale Nähe vs. historische Distanz
- Veränderte Lehrpläne und Produktionsbedingungen

**3. Anpassungen der Forschungsfragen:**
- Spezifische historische Kontexte (gesellschaftliche Umbrüche vs. Pandemie)
- Unterschiedliche thematische Schwerpunkte
````


