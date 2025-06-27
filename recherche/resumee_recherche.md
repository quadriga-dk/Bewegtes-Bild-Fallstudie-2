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

# Resümee Vorarbeiten und Recherche
Im Zentrum dieses Kapitels stehen zwei Lernziele. Zum einen werden Kenntnisse vermittelt, wie eine filmwissenschaftliche Fragestellung konzipiert wird, die mit digitalen Tools bearbeitet werden kann. Zum anderen wird der Prozess zur Bildung eines zur Fragestellung passenden Korpus aufgezeigt. Hierfür behandeln wir im Kapitel verschiedene Teilbereiche:

```{admonition} Teilbereiche des Kapitels
:class: keypoint

* **Materialrecherche** zur Fragestellung
* **Metadaten** und die mit ihnen verbundenen Problemfelder
* **Operationalisierung**  und Konkretisierung der Fragestellung

```

Ausgangspunkt unserer Fallstudie ist die Frage, welche Veränderungen sich in den studentischen Filmen der damaligen Hochschule für Film und Fernsehen (HFF) Konrad Wolf in den Jahren 1985 bis 1999 erkennen lassen, die auf die deutsche Einheit verweisen.

Am Beginn des Kapitels wird das Vorgehen bei der [Materialrecherche](./material.md) zur Ausgangsfragestellung dargestellt. Wir führen die Schritte einer Recherche im Online-Bibliothekskatalog (OPAC) der Universitätsbibliothek exemplarisch vor, in dem die studentischen Filme des Archivs der Filmuniversität verzeichnet sind. Mithilfe geeigneter Suchfunktionen des OPAC erarbeiten wir einen ersten Überblick über die im Archiv vorhandenen und zur Fragestellung passenden Filme. Bei der ersten Sichtung einer Stichprobe aus diesen Filmen fallen uns verschiedene Themen und Motive auf, die bei der weiteren Eingrenzung der Fragestellung hilfreich sein können.

Im folgenden Abschnitt zu [Daten und Metadaten](./metadaten.md) werden eine Definition und verschiedene Arten von Metadaten vorgestellt. Die Rolle von Klassifikationssystemen im Kontext der Erstellung von Metadaten wird näher beleuchtet. Bei der Arbeit mit Metadaten ist es wichtig zu reflektieren, dass diese nicht als 'neutral' gesehen werden können, sondern eng mit Wertvorstellungen und Weltsichten verbunden sind. Metadaten müssen daher immer auch kontextualisiert werden, der Prozess ihrer Entstehung spielt eine wichtige Rolle um sie zu verstehen und zu beurteilen.

Abschließend erfolgt die [Operationalisierung der Fragestellung](./operationalisierung.md). Bei der Operationalisierung geht es darum zu bestimmen, welche Daten für die Beantwortung einer Fragestellung hilfreich sind und erhoben werden müssen. Anhand unserer Ausgangsfrage zeigen wir verschiedene Perspektiven auf, die eingenommen werden können, wobei der Fokus auf den möglichen quantifizierbaren Aspekten und den potentiell notwendigen Daten liegt. Darauf aufbauend legen wir dar, wie aus der Ausgangsfrage einzelne Teilfragestellungen entwickelt werden, die für unsere Fallstudie relevant sind.

Insgesamt demonstrieren wir in diesem Kapitel am Beispiel unserer konkreten Fallstudie die allgemeinen Schritte für die Entwicklung von Fragestellungen und für die Ausdifferenzierung passender Korpora.


# Neues Wissen testen
Zum Abschluss dieser Lerneinheit können Sie nun Ihr neu erworbenes Wissen auf die Probe stellen. Bei den folgenden Multiple Choice Fragen sind gegebenenfalls auch mehrere richtige Antworten möglich. 

```{code-cell} ipython3
:tags: [remove-input]
display_quiz("../assets/assessment/recherche/recherche_quiz.json", colors = colors.jupyterquiz)
```