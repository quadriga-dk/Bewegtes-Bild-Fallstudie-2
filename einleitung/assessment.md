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

Sie können die Fragen in beliebiger Reihenfolge beantworten und auch mehrfach versuchen. 

**So funktioniert es:**
- Wählen Sie bei jeder Frage die Antwort(en), die Sie für richtig halten
- Lesen Sie das Feedback zu den einzelnen Antwortoptionen sorgfältig durch
- Die Erklärungen helfen Ihnen, Ihr Verständnis zu vertiefen – auch bei korrekten Antworten 

Es erfolgt keine Bewertung oder Speicherung Ihrer Ergebnisse. Nutzen Sie dieses Assessment, um Wissenslücken zu identifizieren und gegebenenfalls die entsprechenden Abschnitte des Kapitels noch einmal zu bearbeiten.

**Geschätzte Zeit**: XX

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
    "question": """Welche der folgenden Aussagen zu Digital Humanities sind korrekt? (Mehrere Antworten möglich)""",
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
**Tools/Datenbanken:**  
1. Cinemetrics
2. ELAN
3. Distant Viewing Toolkit
4. Media History Digital Library (MHDL)
5. Women Film Pioneers Explorer
6. VIAN

**Arbeitsbereiche:**  
A. Statistische Filmanalyse  
B. Digitale Filmanalyse/Annotation  
C. Automatisierte Analyse großer Filmkorpora  
D. Digitale Archive und Datenbanken  
E. Feministische Filmgeschichtsschreibung  
F. Farbanalyse im Film  


```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz
import sys
sys.path.append("..")
from quadriga import colors

multiple_choice10 = [{
    "question": """Ordnen Sie die folgenden Tools/Datenbanken den entsprechenden Arbeitsbereichen der Digital Humanities in der Filmwissenschaft zu:""",
    "type": "multiple_choice",
    "answers": [
        {
            "answer": "1-A, 2-B, 3-C, 4-D, 5-E, 6-F",
            "correct": True,
            "feedback": """✓ Ausgezeichnet! Sie haben alle Tools korrekt zugeordnet:
- Cinemetrics → Statistische Filmanalyse: Ermöglicht die Erfassung von Schnittdaten und berechnet statistische Werte wie die Average Shot Length (ASL)
- ELAN → Digitale Filmanalyse: Annotationstool, das ursprünglich für linguistische Analysen entwickelt und für Filmannotationen adaptiert wurde
- Distant Viewing Toolkit → Automatisierte Analyse: Ermöglicht die automatisierte Annotation und Analyse großer Mengen von Filmen
- MHDL → Digitale Archive: Wichtige digitale Ressource mit fast drei Millionen gescannten Seiten von Materialien zur Film- und Mediengeschichte
- Women Film Pioneers Explorer → Feministische Filmgeschichtsschreibung: Visualisiert Daten aus dem Women Film Pioneers Project
- VIAN → Farbanalyse: Entwickelt für die automatisierte Analyse von Farbe im Film"""
        },
        {
            "answer": "1-B, 2-A, 3-C, 4-D, 5-E, 6-F",
            "correct": False,
            "feedback": """× Nicht korrekt. Überprüfen Sie die Zuordnung von Cinemetrics und ELAN. Cinemetrics ist speziell für statistische Filmanalyse (ASL-Berechnung) konzipiert, während ELAN ein allgemeines Annotationstool ist."""
        },
        {
            "answer": "1-A, 2-C, 3-B, 4-D, 5-E, 6-F",
            "correct": False,
            "feedback": """× Nicht korrekt. Überprüfen Sie die Zuordnung von ELAN und Distant Viewing Toolkit. ELAN ist für detaillierte manuelle Annotation gedacht, während das Distant Viewing Toolkit automatisierte Analyse großer Korpora ermöglicht."""
        },
        {
            "answer": "1-A, 2-B, 3-F, 4-D, 5-E, 6-C",
            "correct": False,
            "feedback": """× Nicht korrekt. Überprüfen Sie die Zuordnung von Distant Viewing Toolkit und VIAN. Das Distant Viewing Toolkit ist für automatisierte Analyse großer Filmkorpora konzipiert, während VIAN speziell für Farbanalyse entwickelt wurde."""
        }
    ]
}]

display_quiz(multiple_choice10, colors=colors.jupyterquiz)
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