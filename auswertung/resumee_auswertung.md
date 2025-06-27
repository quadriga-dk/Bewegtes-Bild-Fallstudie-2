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

# Resümee Datenauswertung und Datenvisualisierung
Als Lernziel soll in diesem Kapitel die Fähigkeit vermittelt werden, einen Datensatz mithilfe von Visualisierungen und weiteren digitalen Tools hinsichtlich einer Fragestellung auszuwerten. Grundlage für die Auswertung ist der bereinigte Datensatz zum Filmkorpus unserer Fallstudie. Dabei werden folgende Teilbereiche behandelt:

```{admonition} Teilbereiche des Kapitels
:class: keypoint

* **Grundlagen** der Visualisierung
* **Visualisierungen** zur Fallstudie

```
Im Abschnitt zu [Grundlagen der Visualisierung](./visualisierung.md) klären wir zunächst den Begriff der Informationsvisualisierung und gehen auf deren lange Tradition ein. Ziel von Visualisierungen ist es, eine große Menge an abstrakten Daten für Menschen erfassbar zu machen. Gleichzeitig können durch Visualisierungen, Muster und Strukturen sichtbar werden, die ohne diese verborgen blieben. Wir führen verschiedene Beispiele für den Einsatz von Visualisierungen in der Filmwissenschaft und Filmgeschichtsschreibung an und gehen auf die verwendeten Tools ein.


# Neues Wissen testen
Zum Abschluss dieser Lerneinheit können Sie nun Ihr neu erworbenes Wissen auf die Probe stellen. Bei den folgenden Multiple Choice Fragen sind gegebenenfalls auch mehrere richtige Antworten möglich. 

```{code-cell} ipython3
:tags: [remove-input]
display_quiz("../assets/assessment/auswertung/auswertung_quiz.json", colors = colors.jupyterquiz)
```