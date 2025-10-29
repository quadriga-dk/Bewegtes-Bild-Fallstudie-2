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

# 🏆Selbsttest: Wissen und Praxis

````{admonition} Hinweis
:class: hinweis

Diese Übungsaufgaben dienen Ihrer Selbsteinschätzung und helfen Ihnen, das im Kapitel Gelernte zu reflektieren.

Sie können die Fragen in beliebiger Reihenfolge beantworten und die Beantwortung auch mehrfach versuchen. 

**So funktioniert es:**
- Wählen Sie bei jeder Frage die Antwort(en), die Sie für richtig halten
- Lesen Sie das Feedback zu den einzelnen Antwortoptionen sorgfältig durch
- Die Erklärungen helfen Ihnen, Ihr Verständnis zu vertiefen – auch bei korrekten Antworten 

Es erfolgt keine Bewertung oder Speicherung Ihrer Ergebnisse. Nutzen Sie dieses Assessment, um Wissenslücken zu identifizieren und gegebenenfalls die entsprechenden Abschnitte des Kapitels noch einmal zu bearbeiten.

**Geschätzte Zeit**: 15 Minuten

Viel Erfolg!
````

### Aufgabe 1

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

multiple_choice9 = [{
    "question": """Welche der folgenden Aussagen zu Digital Humanities sind korrekt?""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "Digital Humanities beschränken sich ausschließlich auf die Analyse von Texten",
            "correct": False,
            "feedback": """× Falsch: Digital Humanities umfassen nicht nur Texte, sondern auch audiovisuelle Medien, Bilder, Ton, geografische Informationen und sogar neue Technologien selbst als Gegenstand (vgl. Thaller, 2017)."""
        },
        {
            "answer": "Digital Humanities umfassen die Anwendung von Informationstechniken auf geisteswissenschaftliche Gegenstände",
            "correct": True,
            "feedback": """✓ Richtig: Dies entspricht Thallers Definition der Digital Humanities als "Summe aller Versuche, die Informationstechniken auf den Gegenstandsbereich der Geisteswissenschaften anzuwenden"."""
        },
        {
            "answer": "Digital Humanities erfordern immer eine einheitliche, allgemein akzeptierte Definition",
            "correct": False,
            "feedback": """× Falsch: Sowohl Thaller als auch König betonen, dass es keine einheitliche Definition von Digital Humanities gibt."""
        },
        {
            "answer": "Digital Humanities beinhalten die Selbstreflexion digitaler Forschungsprozesse",
            "correct": True,
            "feedback": """✓ Richtig: König hebt die Selbstreflexion digitaler Forschungs- und Publikationsprozesse als wichtigen Bestandteil hervor."""
        },
        {
            "answer": "Digital Humanities entstanden erst in den 2020er Jahren",
            "correct": False,
            "feedback": """× Falsch: Quantitative Ansätze in der Filmwissenschaft gibt es bereits seit den 1970er Jahren (Barry Salt), und Digital Humanities haben sich über Jahrzehnte hinweg entwickelt."""
        }
    ]
}]

display_quiz(multiple_choice9, colors=colors.jupyterquiz)
```

### Aufgabe 2 

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

# Create a quiz instance
quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die folgenden Tools/Datenbanken den entsprechenden Arbeitsbereichen der Digital Humanities in der Filmwissenschaft zu:",
    descriptions=[
        "Statistische Filmanalyse",
        "Digitale Filmanalyse/Annotation", 
        "Automatisierte Analyse großer Filmkorpora",
        "Digitale Archive und Datenbanken",
        "Feministische Filmgeschichtsschreibung",
        "Farbanalyse im Film"
    ],
    options=[
        "Cinemetrics", 
        "ELAN", 
        "Distant Viewing Toolkit", 
        "Media History Digital Library (MHDL)", 
        "Women Film Pioneers Explorer", 
        "VIAN"
    ],
    correct_mapping={
        "Statistische Filmanalyse": "Cinemetrics",
        "Digitale Filmanalyse/Annotation": "ELAN", 
        "Automatisierte Analyse großer Filmkorpora": "Distant Viewing Toolkit",
        "Digitale Archive und Datenbanken": "Media History Digital Library (MHDL)",
        "Feministische Filmgeschichtsschreibung": "Women Film Pioneers Explorer",
        "Farbanalyse im Film": "VIAN"
    }
)

```

### Aufgabe 3

**Szenario:** Sie arbeiten an einem Forschungsprojekt zu deutschen Stummfilmen der 1920er Jahre und möchten untersuchen, wie sich Montagestile in diesem Zeitraum entwickelt haben. Sie haben Zugang zu 50 digitalisierten Filmen.

Beschreiben Sie:
1. Welche digitalen Tools Sie einsetzen würden
2. Welche Art von Daten Sie erheben müssten

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('Assessment_3')
```

````{admonition} Musterlösung
:class: solution, dropdown

**1. Digitale Tools:**

**Für das Forschungsprojekt können beispielsweise folgende Tools eingesetzt werden**


**Statistische Filmanalyse:**
- **Cinemetrics** (nach Yuri Tsivian): Manuelles Tool zur Erfassung von Einstellungswechseln in einem Film; das Ergebnis wird auf die Cinemetrics-Website hochgeladen und die Average Shot Length (ASL) automatisch berechnet
- *Begründung:* Etablierte Methode seit Barry Salt, ermöglicht Vergleich verschiedener Montagestile

**Automatisierte Analyse:**
- **Distant Viewing Toolkit** (Arnold/Tilton): Automatisierte Erkennung von Einstellungswechseln mittels 'computer vision'
- *Begründung:* Verarbeitung großer Filmkorpora möglich, reduziert manuellen Aufwand

**Detaillierte Annotation:**
- **ELAN, VIAN oder Advene**: Tools für präzise, teilweise semiautomatische Filmannotation
- *Begründung:* Ermöglicht detaillierte Erfassung spezifischer Montagetechniken und deren Kontextualisierung

**Erweiterte Ansätze:**
- Kombination manueller und automatisierter Verfahren

**2. Art der Daten:**

**Grundlegende Schnittdaten:**
- Anzahl der Einstellungen pro Film: Basis für ASL-Berechnung
- Länge der einzelnen Einstellungen: Ermöglicht Analyse von Rhythmus und Tempo
- Gesamtfilmlänge: Notwendig für ASL-Berechnung (Filmlänge ÷ Anzahl Einstellungen)

**Kontextuelle Daten:**
- Entstehungsjahr: Zentral für die Untersuchung zeitlicher Entwicklungen
- Beteiligte Personen (Regie, Buch, Schauspiel etc.): Für stilistische Zuordnungen
- Filmgenre: Verschiedene Genres können unterschiedliche Montagestile aufweisen
````