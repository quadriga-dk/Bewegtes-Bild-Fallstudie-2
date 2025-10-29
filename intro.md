# Studentische Filme an der Filmuniversität Babelsberg zur Wendezeit (1985-1999)

```{figure} assets/intro/Wordcloud.png
---
align: left
width: 100%
name: wordcloud
alt: Wordcloud zur Fallstudie
---

```

````{margin}
```{admonition} Fragen oder Feedback 
:class: frage-feedback

<a href="https://github.com/quadriga-dk/Bewegtes-Bild-Fallstudie-2/issues/new?assignees=&labels=question&projects=&template=frage.yml" class="external-link" target="_blank">
    Stellen Sie eine Frage
</a> <br>
<a href="https://github.com/quadriga-dk/Bewegtes-Bild-Fallstudie-2/issues/new?assignees=&labels=feedback&projects=&template=feedback.yml" class="external-link" target="_blank">
    Geben Sie uns Feedback
</a>

Mit Ihren Rückmeldungen können wir unser interaktives Lehrbuch gezielt an Ihre Bedürfnisse anpassen.

```
````
`````{margin}
````{admonition} Zitierhinweis
:class: citation-information
```{literalinclude} /CITATION.bib
:language: bibtex
```
Schick, T., Winter, M., Loist, S. & Gieseke, L. (2025). _Studentische Filme an der Filmuniversität Babelsberg zur Wendezeit (1985–1999)_.   

````
`````

Im Rahmen der Digital Humanities werden in verschiedenen Bereichen der Geisteswissenschaften in den letzten Jahren verstärkt digitale Werkzeuge und digitale Methoden eingesetzt. Auch die Filmwissenschaft beschäftigt sich mit den Möglichkeiten und Grenzen digitaler Ansätze. So widmet die Zeitschrift _montage/av_ im Jahr 2020 eine Ausgabe dem Thema <a href="https://montage-av.de/29-1-2020/" class="external-link" target="_blank">Digitale Praktiken</a> in der Filmforschung, im gleichen Jahr erscheint in _Digital Humanities Quarterly (DHQ)_ ein Themenschwerpunkt zu <a href="https://digitalhumanities.org/dhq/vol/14/4/index.html" class="external-link" target="_blank">Digital Humanities & Film Studies</a>. Für die Filmgeschichtsschreibung zeigt der Sammelband _Doing Digital Film History_ {cite}`f-Dang_van_der_Heijden_Olesen_2024` verschiedene Perspektiven digitaler Herangehensweisen auf.

Die vorliegende _Open Educational Resource (OER)_[^1] wurde in Form eines <a href="https://jupyterbook.org/" class="external-link" target="_blank">Jupyter Books</a> auf der Grundlage einer Fallstudie entwickelt. Sie befasst sich mit einer filmwissenschaftlichen Fragestellung und erkundet, wie für deren Bearbeitung digitale Verfahren sinnvoll eingesetzt werden können. Im Mittelpunkt der exemplarischen Untersuchung steht das Filmarchiv der Hochschule für Film und Fernsehen (HFF) "Konrad Wolf", also der heutigen Filmuniversität Babelsberg KONRAD WOLF. Ausgangspunkt für die Fallstudie bildet folgende Frage: **Welche Veränderungen lassen sich in den studentischen Filmen der Jahre 1985 bis 1999 erkennen, die auf die deutsche Einheit verweisen?**

Die OER führt anhand eines konkreten Beispiels in einige grundlegende Aspekte des digitalen Arbeitens in der Filmwissenschaft ein. Dabei nimmt die Fallstudie vor allem Metadaten und filmografische Angaben zu den studentischen Produktionen im Filmarchiv in den Blick. Nach einem Abschnitt zum Themenbereich _Digital Humanities und Filmwissenschaft_ werden die einzelnen Schritte der Fallstudie dargestellt und nachvollziehbar gemacht: Von der Konkretisierung der Fragestellung über die Korpusbildung, Datenerhebung und Datenbereinigung bis hin zur Erstellung von Visualisierungen auf der Grundlage des Datensatzes und der Datenpublikation.

## Zielgruppe

Diese _Open Educational Resource (OER)_ richtet sich in Form eines _Selbstlernkurses_ an Wissenschaftler:innen, die sich für die Bearbeitung filmwissenschaftlicher Fragestellungen mithilfe digitaler Methoden und Tools interessieren. Die Fallstudie wurde in erster Linie für Forschende der Film- und Medienwissenschaft entwickelt. Sie bietet aber auch wertvolle Einblicke für Vertreter:innen anderer geisteswissenschaftlicher Disziplinen wie z.B. der Geschichts- oder Informationswissenschaft, die sich in ihren Forschungsprojekten mit Bewegtbildmaterial beschäftigen möchten. Besondere Vorkenntnisse sind nicht erforderlich. Die OER kann dabei sowohl für das eigene Lernen als auch in der Lehre eingesetzt werden.

## Struktur der Fallstudie

Die Darstellung der Fallstudie in dieser Open Educational Resource ist in mehrere Schritte unterteilt.

```{figure} assets/intro/Grafik_Schritte.png
---
align: left
width: 100%
name: grafik
alt: Grafische Darstellung der einzelnen Schritte der Fallstudie
---
Schritte der Fallstudie
```

In einem [einleitenden Kapitel](einleitung/toc) wird auf das Themenfeld "Digital Humanities und Filmwissenschaft" eingegangen. Die daran anschließende Fallstudie ist folgendermaßen gegliedert:

* im **1. Schritt** wird wird durch eine Materialrecherche zur Forschungsfrage eingegrenzt, welche Filme untersucht werden sollen, also ein Filmkorpus für die Fallstudie gebildet. Es wird definiert, was unter filmografischen Angaben (wie z.B. Titel, Regie, Entstehungsjahr etc.) bzw. Metadaten zu verstehen ist und anschließend erläutert, auf welche Weisen die Fragestellung operationalisiert werden kann (siehe Kapitel [Vorarbeiten und Recherche](recherche/toc)).

* im **2. Schritt** wird die Rolle von Datenmodellen und einer guten Datenstruktur genauer beleuchtet. Die Datenquelle für die Metadaten des zu untersuchenden Filmkorpus wird analysiert und die Bereinigung eines Datensatzes mit dem Open Source Tool zur Datenbereinigung <a href="https://openrefine.org/" class="external-link" target="_blank">OpenRefine</a> anhand exemplarischer Schritte dargelegt (siehe Kapitel [Datenerhebung und Datenbereinigung](bereinigung/toc)). Da der Originaldatensatz personenbezogene Daten in den filmografischen Angaben enthält, die nicht für eine offene Publikation geeignet sind, wird für die Erläuterung der Bereinigungsschritte ein synthetischer Datensatz mit fiktiven Einträgen verwendet.

* im **3. Schritt** findet eine exemplarische Auswertung des synthetischen Datensatzes mithilfe von Visualisierungen statt. Zudem werden die im Datensatz enthaltenen Schlagwörter nach Mustern untersucht, die Aufschluss über behandelte Themen und Motive geben können (siehe Kapitel [Datenauswertung und Datenvisualisierung](auswertung/toc)).

* im **4.Schritt** steht der Weg zur Publikation der Daten im Mittelpunkt. Es wird auf den Stand des Forschungsdatenmanagement in der Filmwissenschaft und mögliche Problemfelder bei der Datenpublikation eingegangen (siehe Kapitel [Datenpublikation](publikation/toc)).

In einem [abschließenden Kapitel](zusammenfassung/reflexion) werden die Ergebnisse der Fallstudie zusammengefasst und reflektiert, gefolgt von einem Ausblick auf weitere mögliche Auswertungen des zum Korpus erstellten Datensatzes.



## Literatur
```{bibliography}
:filter: docname in docnames
:keyprefix: f-
```

[^1]: Weitere Informationen zum Konzept von Open Educational Resources finden sich auf <a href="https://open-educational-resources.de/" class="external-link" target="_blank">OERinfo</a>
