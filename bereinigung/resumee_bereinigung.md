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

# Resümee
Das Lernziel dieses Kapitels ist, die Aufbereitung der Daten eines Korpus von Filmen mit passenden Tools zu vermitteln. Der Zweck und die Schritte einer Datenbereinigung werden anhand des Korpus der Fallstudie aufgezeigt. Hierfür haben wir diesen Themenbereich in einzelne Teilbereiche aufgeteilt:

```{admonition} Teilbereiche des Kapitels
:class: keypoint

* Definition und Bestimmung eines **Datenmodells**
* Analyse einer **Datenquelle**
* **Datenbereinigung** mit der Software OpenRefine

```

Im Zentrum der Datenaufbereitung stehen die Metadaten zu den Filmen unseres Korpus, wobei unter Metadaten hier die filmografischen Angaben zu verstehen sind. Die Daten zu unserem Korpus haben wir in Form eines Auszuges aus der Datenbank des OPAC der Bibliothek der Filmuniversität erhalten.

Im Abschnitt zum [Datenmodell](./modell.md) wird zunächst geklärt, was unter diesem Begriff zu verstehen ist. In einem Datenmodell wird festgelegt, welche Merkmale des Datenobjekts aufgeführt werden und in welchem Format dies geschehen soll. In unserem Fall ist das Datenobjekt der jeweilige Film aus dem Bestand des Filmarchivs. Für eine Arbeit mit den Daten muss das zugrundeliegende Datenmodell analysiert werden.

Diese Analyse erfolgt in unserer Fallstudie im Abschnitt zur [Datenquelle](./datenquelle.md). Dort gehen wir dem Datenmodell nach, das dem Auszug der Daten zu unserem Filmkorpus aus dem OPAC zugrunde liegt. Dies geschieht u.a., indem wir den Eingabeprozess der filmografischen Angaben in die Datenbank des OPAC nachvollziehen und einzelne Eingabefelder besprechen. Dadurch wird die Struktur des Datenbankauszugs den wir von der Bibliothek erhalten haben besser verständlich und deutlich, welche Bereinigungsschritte notwendig sind.

Den Prozess der [Datenbereinigung](./openRefine/0_datenbereinigung.md) stellen wir abschließend zu diesem Kapitel dar. Die Software *OpenRefine* wird vorgestellt und kurz begründet, warum wir uns für dieses Programm entschieden haben. Die Arbeit mit dieser Software stellen wir anhand einiger exemplarischer Schritte bei der Bereinigung unseres Datensatzes vor, die in dieser Form auch bei vielen anderen Datensätzen angewendet werden können.

Am Ende steht schließlich ein konsistenter, einheitlich strukturierter Datensatz, der für die weitere Auswertung der filmografischen Daten mit digitalen Tools verwendet werden kann. 


# Neues Wissen testen
Zum Abschluss dieser Lerneinheit können Sie nun Ihr neu erworbenes Wissen auf die Probe stellen. Bei den folgenden Multiple Choice Fragen sind gegebenenfalls auch mehrere richtige Antworten möglich. 

```{code-cell} ipython3
:tags: [remove-input]
display_quiz("../assets/assessment/bereinigung/bereinigung_quiz.json", colors = colors.jupyterquiz)
```