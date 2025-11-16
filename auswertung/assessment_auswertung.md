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

**Geschätzte Zeit**: 15 Minuten

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
    "question": """Welche Aussagen zur Informationsvisualisierung sind korrekt?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Visualisierungen sind eine Erfindung des digitalen Zeitalters",
            "correct": False,
            "feedback": """× Falsch: Visualisierungen sind keine Erfindung des digitalen Zeitalters - Balken- und Liniendiagramme waren bereits im 18. Jahrhundert gebräuchlich."""
        },
        {
            "answer": "Informationsvisualisierung dient dazu, große Mengen abstrakter Daten visuell erfassbar zu machen",
            "correct": True,
            "feedback": """✓ Richtig: Nach Rehbein dient Informationsvisualisierung dazu, große Mengen abstrakter Daten so visuell aufzuarbeiten, dass sie für Menschen erfassbar werden."""
        },
        {
            "answer": "Visualisierungen sind immer neutrale und objektive Darstellungen von Daten",
            "correct": False,
            "feedback": """× Falsch: Nach Burkhardt/Loist und Drucker sind Visualisierungen immer mit Interpretation durch die Personen verbunden, die diese erstellen."""
        },
        {
            "answer": "Alles, was quantifiziert werden kann, ist auch visualisierbar",
            "correct": True,
            "feedback": """✓ Richtig: Alles, was quantifiziert und in einen numerischen Wert gebracht werden kann, ist auch in einer Visualisierung darstellbar."""
        }
    ]
}]

display_quiz(multiple_choice1, colors=colors.jupyterquiz)
```

## Aufgabe 2

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

# Create a quiz instance
quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Beispiele den entsprechenden Funktionen von Visualisierungen zu:",
    descriptions=[
        "Eine Timeline visualisiert chronologische Entwicklungen für Konferenzteilnehmer",
        "Verschiedene Grafiken werden erstellt, um eine Hypothese zu Genderverteilungen zu überprüfen",
        "Ein Datensatz wird untersucht, um unbekannte Muster zu entdecken"
    ],
    options=[
        "Präsentation",
        "Konfirmative Analyse", 
        "Explorative Analyse"
    ],
    correct_mapping={
        "Eine Timeline visualisiert chronologische Entwicklungen für Konferenzteilnehmer": "Präsentation",
        "Verschiedene Grafiken werden erstellt, um eine Hypothese zu Genderverteilungen zu überprüfen": "Konfirmative Analyse",
        "Ein Datensatz wird untersucht, um unbekannte Muster zu entdecken": "Explorative Analyse"
    }
)
```


## Aufgabe 3

Bewerten Sie folgende Aussagen zu Visualisierungen und Interpretation:

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false1 = [{
    "question": """Daten haben eine inhärente visuelle Form, die nur eine Darstellungsweise ermöglicht""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt! Nach Drucker haben Daten keine inhärente visuelle Form - verschiedene Darstellungsweisen sind möglich."""
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
    "question": """Visualisierungen müssen kritisch gelesen und interpretiert werden""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! Visualisierungen müssen kritisch hinterfragt werden: Wer hat sie auf welcher Grundlage zu welchem Zweck erstellt?"""
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
    "question": """Die Wahl der Visualisierung ist mit subjektiven Entscheidungen verbunden""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! Welche Art der Visualisierung gewählt wird, ist mit subjektiven Entscheidungen der Erstellenden verbunden."""
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
    "question": """Verschiedene Daten eignen sich gleich gut für alle Visualisierungsformen""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt! Je nach Art der Daten eignen sich manche Formen der Visualisierung besser als andere."""
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

## Aufgabe 4

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

multiple_choice4 = [{
    "question": """Welche Aussagen zu Manovichs Ansätzen sind korrekt?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Manovich definiert Informationsvisualisierung als \"mapping between data and a visual representation\"",
            "correct": True,
            "feedback": """✓ Richtig: Das entspricht Manovichs Definition von Informationsvisualisierung."""
        },
        {
            "answer": "Klassische Visualisierungen folgen dem Prinzip der Komplexitätssteigerung",
            "correct": False,
            "feedback": """× Falsch: Klassische Visualisierungen folgen dem Prinzip der "Reduktion" - nur ein kleiner Teil der Merkmale wird bei der Visualisierung berücksichtigt."""
        },
        {
            "answer": "\"Visualisierung ohne Reduktion\" versucht, mehr Merkmale der Objekte zu erhalten",
            "correct": True,
            "feedback": """✓ Richtig: Bei einer "Visualisierung ohne Reduktion" sollen wesentlich mehr Merkmale der Objekte erhalten bleiben."""
        },
        {
            "answer": "Bei der \"Visualisierung ohne Reduktion\" werden Datenpunkte stark aggregiert",
            "correct": False,
            "feedback": """× Falsch: Statt Datenpunkte zu aggregieren wird versucht, große Datenmengen in ihrer Gesamtheit darzustellen."""
        }
    ]
}]

display_quiz(multiple_choice4, colors=colors.jupyterquiz)
```

## Aufgabe 5

Ordnen sie folgende Aussagen in Bezug auf Manovichs Schlüsselprinzipien klassischer Informationsvisualisierung ein:

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false5_1 = [{
    "question": """Das erste Prinzip ist die Reduktion von Objektmerkmalen""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! Erstes Prinzip: "Reduktion" - nur ein kleiner Teil der Merkmale wird bei der Visualisierung berücksichtigt."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false5_1, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false5_2 = [{
    "question": """Räumliche Variablen wie Position und Größe werden zur Datenrepräsentation verwendet""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! Zweites Prinzip: räumliche Variablen wie Position, Größe oder Form werden verwendet."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false5_2, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false5_3 = [{
    "question": """Komplexe Strukturen sollen durch Interaktion einfacher Elemente verstanden werden""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt! Ziel der Reduktion ist es, komplexe Strukturen durch die Interaktion einfacher Elemente besser verstehbar zu machen."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false5_3, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false5_4 = [{
    "question": """Klassische Visualisierungen bevorzugen zeitliche statt räumliche Variablen""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt! Klassische Visualisierungen bevorzugen räumliche, nicht zeitliche Variablen."""
        },
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false5_4, colors=colors.jupyterquiz)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false5_5 = [{
    "question": """Reduktion führt zu weniger verständlichen Darstellungen""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt! Reduktion dient der besseren Verständlichkeit, kann aber auch zu Informationsverlust führen."""
        },
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt"""
        }
    ]
}]

display_quiz(true_false5_5, colors=colors.jupyterquiz)
```

## Aufgabe 6

**Szenario:** Sie sollen für die Fallstudie zu studentischen Filmen (1985–1999) Visualisierungen zu folgenden Teilfragestellungen entwickeln:
- Zeitliche Verteilung der Filmproduktion
- Gattungsverteilung (Spiel-, Dokumentar-, Animationsfilm)
- Häufigste Schlagworte und deren zeitliche Entwicklung

Entwickeln Sie eine Visualisierungsstrategie:
1. Auswahl geeigneter Visualisierungsformen
2. Begründung der Methodenwahl
3. Erwartete Erkenntnisse und Grenzen

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('Assessment_E-6')
```

````{admonition} Musterlösung
:class: solution, dropdown

**1. Auswahl geeigneter Visualisierungsformen:**
- Zeitliche Verteilung: Liniendiagramm oder Säulendiagramm nach Jahren
- Gattungsverteilung: Kreisdiagramm oder Säulendiagramme
- Schlagworte: Tag Cloud oder Säulendiagramm mit zeitlicher Achse

**2. Begründung der Methodenwahl:**
- Zeitreihen für chronologische Entwicklungen
- Proportionale Darstellungen für Verteilungen
- Kombinierte Ansätze für mehrere Variablen

**3. Erwartete Erkenntnisse und Grenzen:**
- Mögliche Erkenntnisse: Produktionsspitzen, dominante Gattungen, thematische Trends
- Grenzen: Qualität der Metadaten, Interpretation der Kategorisierungen, fehlende Kontextualisierung
````

## Aufgabe 7

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

single_choice7 = [{
    "question": """Welche Aussage zur "Visualisierung ohne Reduktion" ist korrekt?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Sie eliminiert alle Reduktionsprozesse vollständig",
            "correct": False,
            "feedback": """× Falsch: Trotz des Versuchs, eine „Visualisierung ohne Reduktion" zu erstellen, können nie alle Merkmale eines Objekts in eine grafische Darstellung einfließen."""
        },
        {
            "answer": "Sie versucht mehr Merkmale zu erhalten, kann aber nie alle Merkmale darstellen",
            "correct": True,
            "feedback": """✓ Richtig: Es muss auch bei diesen Formen hinterfragt werden, welche Elemente in eine Daten-Visualisierung aufgenommen und welche nicht berücksichtigt werden."""
        },
        {
            "answer": "Sie ist nur bei digitalen Objekten anwendbar",
            "correct": False,
            "feedback": """× Falsch: Sie ist besonders gut bei digitalen Objekten anwendbar, aber nicht ausschließlich."""
        },
        {
            "answer": "Sie ersetzt die klassischen Visualisierungsformen komplett",
            "correct": False,
            "feedback": """× Falsch: Es ist ein ergänzender, nicht ersetzender Ansatz."""
        }
    ]
}]

display_quiz(single_choice7, colors=colors.jupyterquiz)
```

## Aufgabe 8

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

# Create a quiz instance
quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="""Ordnen Sie die Tools ihren typischen Anwendungsbereichen zu:""",
    descriptions=[
        "Komplexe Netzwerk-Visualisierungen",
        "Einfache Diagramme und Tabellenkalkulation",
        "Umfangreiche Datenauswertungen, Visualisierungen und komplexe Dashboards",
        "Schnelle, webbasierte Visualisierungen verschiedener Datentypen"
    ],
    options=[
        "Gephi",
        "Excel",
        "Tableau",
        "RAWGraph"
    ],
    correct_mapping={
        "Komplexe Netzwerk-Visualisierungen": "Gephi",
        "Einfache Diagramme und Tabellenkalkulation": "Excel",
        "Umfangreiche Datenauswertungen, Visualisierungen und komplexe Dashboards": "Tableau",
        "Schnelle, webbasierte Visualisierungen verschiedener Datentypen": "RAWGraph"
    }
)
```

