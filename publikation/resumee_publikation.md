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
In diesem Kapitel soll als Lernziel die Fähigkeit vermittelt werden, einen Datensatz für eine Datenpublikation vorzubereiten und ein passendes Repositorium für die Veröffentlichung auszuwählen. Dabei werden im Kapitel folgenden Teilbereichen behandelt:

```{admonition} Teilbereiche des Kapitels
:class: keypoint

* **Forschungsdatenmanagement** in der Filmwissenschaft
* Formen der **Datenpublikation** 

```

Im Abschnitt [Forschungsdatenmanagement (FDM)](./forschungsdaten.md) werden zunächst kurz dessen Grundlagen erläutert. Wir stellen dar, was unter einem Forschungsdatenlebenszyklus zu verstehen ist und welche Vorteile ein Datenmanagementplan für ein Projekt bietet. Dabei wird deutlich, das der Begriff 'Forschungsdaten' sich nicht eindeutig definieren lässt und es immer auch vom Forschungskontext abhängig ist, was als relevante Forschungsdaten gesehen werden kann. Oft kann es sich dabei um sehr heterogenes Material handeln, z.B. Texte, Bilder, Annotationen oder Filmprotokolle. Bei unserer Fallstudie haben sich als Forschungsdaten filmografische Angaben zu studentischen Filmen ergeben. Für diesen Datensatz müssen wir uns im Rahmen des FDM Gedanken machen, wie wir ihn publizieren und archivieren wollen. Für die Publikation stehen Repositorien zur Verfügung, die verschiedene Charakteristika aufweisen.

Die verschiedenen [Formen der Datenpublikation](./publikationsformen.md) stellen wir im folgenden Abschnitt vor. Prinzipiell können drei Möglichkeiten unterschiedene werden. Begleitend zu einem wissenschaftlichen Artikel werden zugehörige Datensätze in einem Repositorium veröffentlicht. Im Artikel wird auf diese Daten verwiesen. Datensätze können auch unabhängig von anderen Publikationen in einem Repositorium veröffentlicht und zugänglich gemacht werden. Data Papers schließlich beschreiben und analysieren Datensätze in einem Repositorium genau und gehen oft auch auf die Nachnutzbarkeit der veröffentlichten Daten ein. In allen Fällen ist es wichtig, dass zu den Daten, die ein einem Repositorium zugänglich gemacht werden, möglichst genaue Beschreibungen zur Entstehung und Struktur der Daten vorliegen. Nur so ist es möglich, diese Daten auch für andere Projekte zu nutzen, da hierfür deren Kontext klar ersichtlich sein muss. 

Insgesamt vermitteln wir im Kapitel ein Verständnis für die Bedeutung eines guten Forschungsdatenmanagement und für die Vorteile einer durchdachten Datenpublikation.


# Neues Wissen testen
Zum Abschluss dieser Lerneinheit können Sie nun Ihr neu erworbenes Wissen auf die Probe stellen. Bei den folgenden Multiple Choice Fragen sind gegebenenfalls auch mehrere richtige Antworten möglich. 

```{code-cell} ipython3
:tags: [remove-input]
display_quiz("../assets/assessment/publikation/publikation_quiz.json", colors = colors.jupyterquiz)
```