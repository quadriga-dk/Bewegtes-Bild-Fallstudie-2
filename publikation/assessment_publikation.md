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

**Geschätzte Zeit**: 20 Minuten

Viel Erfolg!
````

## Aufgabe 1

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="""Bringen Sie die Schritte des Forschungsdatenlebenszyklus in die richtige Reihenfolge:""",
    descriptions=[
        "1", 
        "2", 
        "3", 
        "4", 
        "5", 
        "6",
        "7"      
    ],
    options=[
        "Planung", 
        "Erhebung", 
        "Aufbereitung", 
        "Analyse", 
        "Datenpublikation", 
        "Archivierung",
        "Nachnutzung"
    ],
    correct_mapping={
        "1": "Planung",
        "2": "Erhebung", 
        "3": "Aufbereitung",
        "4": "Analyse",
        "5": "Datenpublikation",
        "6": "Archivierung",
        "7": "Nachnutzung"
    }
)
```

## Aufgabe 2

Bewerten Sie folgende Aussagen zu Forschungsdaten:

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false1 = [{
    "question": """Forschungsdaten liegen immer digital vor.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt: Forschungsdaten müssen nicht immer digital vorliegen (z.B. Texte), sie können auch im Projekt in eine digitale Form überführt werden."""
        },
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt: Nicht alle Forschungsdaten liegen ursprünglich digital vor."""
        }
    ]
}]

display_quiz(true_false1, colors=colors.jupyterquiz)

true_false2 = [{
    "question": """Forschungsdaten können aus sehr heterogenen Materialien bestehen.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt: In der Regel hat man es mit heterogenen Material zu tun, wie schriftliche und bildliche Quellen oder Materialsammlungen."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt: Forschungsdaten umfassen verschiedenste Materialtypen und Quellen."""
        }
    ]
}]

display_quiz(true_false2, colors=colors.jupyterquiz)

true_false3 = [{
    "question": """Es existiert eine einheitliche Definition von Forschungsdaten.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt: Der Begriff Forschungsdaten lässt sich gerade in den Geisteswissenschaften nur schwer fassen, eine einheitliche Definition liegt nicht vor."""
        },
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt: Die Definition von Forschungsdaten ist nicht einheitlich und kann von Fach zu Fach variieren."""
        }
    ]
}]

display_quiz(true_false3, colors=colors.jupyterquiz)

true_false4 = [{
    "question": """Forschungsdaten müssen in ihren Disziplinen und Kontexten betrachtet werden.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt: Was als Forschungsdaten verstanden wird hängt von den Kontexten und Disziplinen ab in denen sie entstehen, es werden verschiedene Perspektiven eingenommen."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt: Die Interpretation von Forschungsdaten erfordert immer die Berücksichtigung des disziplinären Kontexts."""
        }
    ]
}]

display_quiz(true_false4, colors=colors.jupyterquiz)
```

## Aufgabe 3

```{code-cell} ipython3
:tags: [remove-input]
multiple_choice3 = [{
    "question": """Welche Aussagen zu Repositorien sind korrekt?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Zenodo ist ein transdisziplinäres Repositorium",
            "correct": True,
            "feedback": """✓ Richtig: Zenodo ist ein transdisziplinäres Repositorium und stellt verschiedene Arten von Forschungsoutput zur Verfügung."""
        },
        {
            "answer": "media/rep/ ist ein kuratiertes, fachspezifisches Repositorium",
            "correct": True,
            "feedback": """✓ Richtig: media/rep/ ist ein kuratiertes Repositorium, das Inhalte aus dem Bereich der kulturwissenschaftlich orientierten Medien- und Filmwissenschaft zur Verfügung stellt und vor der Veröffentlichung prüft."""
        },
        {
            "answer": "re3data.org ist selbst ein Repositorium für Datensätze",
            "correct": False,
            "feedback": """× Falsch: re3data.org ist ein "Registry of Research Data Repositories" – es verzeichnet Repositorien, ist aber selbst keines."""
        },
        {
            "answer": "Repositorien werden nur von kommerziellen Anbietern betrieben",
            "correct": False,
            "feedback": """× Falsch: Repositorien werden häufig durch gemeinnützige Organisationen oder Fachgemeinschaften getragen."""
        }
    ]
}]

display_quiz(multiple_choice3, colors=colors.jupyterquiz)
```

## Aufgabe 4

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

# Create a quiz instance
quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die Beschreibungen den entsprechenden Publikationsformen zu:",
    descriptions=[
        "Wissenschaftlicher Artikel mit Verweis auf extern gespeicherte Daten",
        "Datensatz mit kompakter Beschreibung in einem Repositorium",
        "Ausführliche Beschreibung und Analyse des Datensatz-Potentials"
    ],
    options=[
        "Data Paper",
        "Artikel mit Datenverweis",
        "Reine Datenpublikation",
        "Metadaten-Publikation"
    ],
    correct_mapping={
        "Wissenschaftlicher Artikel mit Verweis auf extern gespeicherte Daten": "Artikel mit Datenverweis",
        "Datensatz mit kompakter Beschreibung in einem Repositorium": "Reine Datenpublikation",
        "Ausführliche Beschreibung und Analyse des Datensatz-Potentials": "Data Paper"
    }
)
```

## Aufgabe 5

Bewerten Sie folgende Aussagen zu Data Papers:

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false1 = [{
    "question": """Data Papers sind primär auf Forschungsergebnisse fokussiert.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt. Im Zentrum von Data Papers stehen nicht Forschungsergebnisse, sondern die Erschließung, Durchdringung und Reflexion eines Datensatzes."""
        },
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt: Data Papers fokussieren sich auf die Dokumentation und Analyse des Datensatzes selbst."""
        }
    ]
}]

display_quiz(true_false1, colors=colors.jupyterquiz)

true_false2 = [{
    "question": """Der Aufbau von Data Papers wird häufig von einem Journal vorgegeben.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt: Der Aufbau eines Data Papers kann variieren und wird häufig vom publizierenden Journal vorgegeben."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt. Die Struktur wird typischerweise durch die Vorgaben des jeweiligen Journals bestimmt."""
        }
    ]
}]

display_quiz(true_false2, colors=colors.jupyterquiz)

true_false3 = [{
    "question": """Data Papers sollten das Datenmodell ausführlich reflektieren.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt: In einem Data Paper wird das Datenmodell eines Datensatzes ausführlich beschrieben und reflektiert."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt: Die Reflexion des Datenmodells ist ein wesentlicher Bestandteil eines Data Papers."""
        }
    ]
}]

display_quiz(true_false3, colors=colors.jupyterquiz)

true_false4 = [{
    "question": """Eine Diskussion der Nachnutzbarkeit ist überflüssig.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt: Auch die Möglichkeiten der Nachnutzung und der Erweiterung des Datensatzes sollten diskutiert und damit eine Grundlage für weitere Einsatzmöglichkeiten gelegt werden."""
        },
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt: Die Diskussion der Nachnutzbarkeit ist ein wichtiger Bestandteil von Data Papers."""
        }
    ]
}]

display_quiz(true_false4, colors=colors.jupyterquiz)
```


## Aufgabe 6

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

multiple_choice10 = [{
    "question": """Welche Informationen gelten nach DSGVO als personenbezogene Daten?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Name einer Person",
            "correct": True,
            "feedback": """✓ Richtig: Namen ermöglichen eine direkte Identifizierung von Personen."""
        },
        {
            "answer": "Institutions- oder Organisationszugehörigkeiten",
            "correct": True,
            "feedback": """✓ Richtig: Zugehörigkeiten sind Ausdruck der kulturellen oder sozialen Identität einer Person."""
        },
        {
            "answer": "Berufsangaben und Bildungsabschlüsse",
            "correct": True,
            "feedback": """✓ Richtig: Berufs- und Bildungsangaben sind Merkmale der wirtschaftlichen, kulturellen oder sozialen Identität einer Person."""
        },
        {
            "answer": "Anonymisierte statistische Werte",
            "correct": False,
            "feedback": """× Falsch: Anonymisierte Daten ohne Personenbezug fallen nicht unter die DSGVO."""
        }
    ]
}]

display_quiz(multiple_choice10, colors=colors.jupyterquiz)
```

## Aufgabe 7

Bewerten Sie folgende Aussagen zu Ausnahmen bei der Verarbeitung personenbezogener Daten:

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

true_false1 = [{
    "question": """Die Verarbeitung personenbezogener Daten ist grundsätzlich verboten.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt: Die Verarbeitung personenbezogener Daten ist zunächst grundsätzlich verboten; für Ausnahmen müssen bestimmte Bedingungen erfüllt sein."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt: Die Verarbeitung von personenbezogenen Daten ist prinzipiell nicht erlaubt, es müssen bestimmte Bedingungen erfüllt sein."""
        }
    ]
}]

display_quiz(true_false1, colors=colors.jupyterquiz)

true_false2 = [{
    "question": """Eine Einwilligung der betroffenen Personen ermöglicht die Datenverarbeitung.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt: Die Einwilligung der Betroffenen ist eine wichtige Ausnahme bei der Datenverarbeitung; sie kann jederzeit widerrufen werden."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt: Die Einwilligung ist eine der wichtigsten rechtlichen Grundlagen für die Datenverarbeitung."""
        }
    ]
}]

display_quiz(true_false2, colors=colors.jupyterquiz)

true_false3 = [{
    "question": """Die Pseudonymisierung reicht für eine Veröffentlichung aus.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": False,
            "feedback": """× Nicht korrekt: Eine Pseudonymisierung reicht nicht aus, der Personenbezug kann wiederhergestellt werden."""
        },
        {
            "answer": "Falsch",
            "correct": True,
            "feedback": """✓ Korrekt: Pseudonymisierung bietet keinen ausreichenden Schutz für eine Veröffentlichung."""
        }
    ]
}]

display_quiz(true_false3, colors=colors.jupyterquiz)

true_false4 = [{
    "question": """Wissenschaftliches Interesse kann eine Ausnahme darstellen.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt: Ein überwiegend wissenschaftliches Interesse kann eine Ausnahme darstellen (mit Auflagen)."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt: Wissenschaftliches Interesse ist eine der möglichen Rechtsgrundlagen für die Datenverarbeitung."""
        }
    ]
}]

display_quiz(true_false4, colors=colors.jupyterquiz)

true_false5 = [{
    "question": """Bei der Anonymisierung müssen alle Identifikatoren entfernt werden.""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Richtig",
            "correct": True,
            "feedback": """✓ Korrekt: Bei der Anonymisierung müssen alle Bezüge zu den Personen entfernt werden."""
        },
        {
            "answer": "Falsch",
            "correct": False,
            "feedback": """× Nicht korrekt: Alle Bezüge zu Personen müssen bei einer Anonymisierung entfernt werden."""
        }
    ]
}]

display_quiz(true_false5, colors=colors.jupyterquiz)
```

## Aufgabe 8

**Szenario:** In der Fallstudie zu studentischen Filmen konnten die originalen Daten nicht publiziert werden. Analysieren Sie die Problematik:
1. Identifizierung der Problemfelder
2. Bewertung der rechtlichen Situation

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('Assessment-8')
```

````{admonition} Musterlösung
:class: solution, dropdown

**1. Problemfelder:**
- Personenbezogene Daten: Namen und Funktionen der Mitwirkenden sind enthalten.
- Unveröffentlichte Werke: Größtenteils studentische Übungen, nicht professionelle Produktionen.
- Fehlende Einwilligung: Nicht gesichert, dass Personen der Veröffentlichung zugestimmt haben.
- Anonymisierung problematisch: Namen und Funktionen sind für die Forschung relevant.

**2. Rechtliche Situation:**
- Datenschutz-Grundverordnung (DSGVO)-Problematik: Personenbezogene Daten können ohne Einwilligung nicht veröffentlicht werden.
- Es liegt kein überwiegend wissenschaftliches Interesse vor, das die Verarbeitung und Veröffentlichung erlauben würde.
- Unterschied zu professionellen Produktionen: Personenangaben sind nicht bereits öffentlich.
- Urheberrechtliche Aspekte: Recht auf korrekte Namens- und Funktionsnennung.

````

## Aufgabe 9

**Szenario:** Sie haben einen Datensatz zu internationalen Filmfestivals erstellt, der öffentlich verfügbare Informationen unter CC-Lizenzen enthält und keine personenbezogenen Daten aufweist. Entwickeln Sie eine Publikationsstrategie:
1. Auswahl des geeigneten Repositoriums
2. Wahl der Publikationsform
3. Berücksichtigung der FAIR-Prinzipien


```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('Assessment-9')
```

````{admonition} Musterlösung
:class: solution, dropdown

**1. Repositorium-Auswahl:**
- Fachspezifisch (media/rep/) vs. transdisziplinär (Zenodo)
- Kuratierung vs. freie Publikation
- Langzeitarchivierung und Nachhaltigkeit 
- Sichtbarkeit und Auffindbarkeit

**2. Publikationsform:**
- Reine Datenpublikation für erste Veröffentlichung
- Data Paper für ausführliche Beschreibung
- Artikel mit Datenverweis für Forschungsergebnisse
- Kombination verschiedener Formen

**3. FAIR-Prinzipien:**
- Findable: Aussagekräftige Metadaten, Schlagworte, DOI
- Accessible: Offene Lizenz (CC BY), standardisierte Dateiformate
- Interoperable: CSV/XML-Format, dokumentierte Datenstruktur
- Reusable: Umfassende Dokumentation, Codebook, README-Datei

````

## Aufgabe 10

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

multiple_choice10 = [{
    "question": """Welche Aussagen zum Urheberrecht bei Forschungsdaten sind korrekt?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Forschungsdaten können unter bestimmten Voraussetzungen urheberrechtlich geschützt sein.",
            "correct": True,
            "feedback": """✓ Richtig: Schutz durch das Urheberrecht besteht bei einer eigenen geistigen Schöpfung."""
        },
        {
            "answer": "Eine gewisse Schöpfungshöhe muss für den Schutz durch das Urheberrecht erreicht werden.",
            "correct": True,
            "feedback": """✓ Richtig: Eine gewisse Schöpfungshöhe muss erreicht werden, also eine eigene geistige Leistung erkennbar sein, die über das Alltägliche und rein Handwerkliche hinausgeht."""
        },
        {
            "answer": "Messdaten und Daten aus Experimenten unterliegen grundsätzlich dem Urheberrecht.",
            "correct": False,
            "feedback": """x Falsch: Daten aus Experimenten und Messdaten unterliegen nicht dem Urheberrecht."""
        },
        {
            "answer": "Qualitative Forschungsdaten sind oft urheberrechtlich geschützt.",
            "correct": True,
            "feedback": """✓ Richtig: Qualitative Daten wie Interviews weisen oft eine eigene geistige Schöpfung auf."""
        }
    ]
}]

display_quiz(multiple_choice10, colors=colors.jupyterquiz)
```

## Aufgabe 11

**Szenario:** Sie möchten Filme als Forschungsdaten publizieren. Analysieren Sie die urheberrechtlichen Herausforderungen:

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('Assessment-11')
```

````{admonition} Musterlösung
:class: solution, dropdown

**1. Komplexität von Filmwerken:**
-	Mehrere Urheber:innen: Regisseur:in, Drehbuchautor:in, Kameraperson, Editor:in, Komponist:in
- Verschiedene Werkarten werden kombiniert
-	Unterscheidung zwischen Urheber:innen und Leistungsschutzberechtigten
-	Schutzfrist: urheberrechtlicher Schutz gilt bis 70 Jahre nach dem Tod der/des am längsten lebenden Urhebers:in
-	Unklare Abgrenzung schöpferischer Tätigkeiten
-	Verwertungsrechte vs. Urheberpersönlichkeitsrechte


**2. Umgangsstrategien:**
-	Nutzung gemeinfreier Werke (nach Ablauf der Schutzfristen)
-	Lizenzierung: Einholung entsprechender Nutzungsrechte
-	Ausnahmeregeln: Zitatrecht, Wissenschaftsschranken
-	Creative Commons Lizenzen bei entsprechenden Rechten
-	Rechtliche Beratung vor der Publikation

````