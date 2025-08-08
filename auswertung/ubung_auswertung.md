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

## Übung zur Datenauswertung und Datenvisualisierung
```{code-cell} ipython3
:tags: [remove-input]
display_quiz("../assets/assessment/auswertung/auswertung_quiz.json", colors = colors.jupyterquiz)
```
