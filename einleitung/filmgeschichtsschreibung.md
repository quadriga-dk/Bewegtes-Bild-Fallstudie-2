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


# Filmgeschichtsschreibung
Neben Repositorien stellen Datenbanken mit digitalisierten Materialien, wie Text- und Bildmaterial, zu Filmen und zur Filmgeschichte wichtige Quellen für die computergestützte filmwissenschaftliche Forschung dar. Solche Datenbanken sind über Web-Portale meist frei zugänglich und bieten verschiedene Recherchemöglichkeiten. Ein wichtiges Beispiel und Vorbild für Projekte ähnlicher Art ist die <a href="https://mediahist.org/" class="external-link" target="_blank">Media History Digital Library (MHDL)</a>, die mittlerweile fast drei Millionen gescannte Seiten umfasst. Die MHDL enthält dabei vor allem US-amerikanische Zeitschriften und Bücher, der Bestand reicht bis in die 1960er Jahre. Nach US-amerikanischem Recht sind viele Publikationen, die bis zu diesem Zeitraum erschienen sind, nicht mehr durch das Copyright geschützt und können öffentlich zugänglich gemacht werden. {cite}`ac-Hagener_Kammerer_2020` 

```{figure} ../assets/einleitung/Lantern_Recherche_Caligari.JPG
---
align: left
width: 100%
name: lantern_caligari
alt: Darstellung eines Suchtreffers bei der Recherche in der MHDL mit Lantern.
---
Screenshot Suche in der MHDL mit Lantern
```

<a href="https://lantern.mediahist.org/" class="external-link" target="_blank">Lantern</a> stellt eine Weboberfläche zur Verfügung, mit der Volltextsuchen im Bestand möglich sind (vgl. {numref}`lantern_caligari`). Entsprechende Treffer werden mit den Metadaten zur Publikation aufgeführt, das Digitalisat der Publikation - also der gescannte, mit Texterkennung bearbeitete Originaltext - und damit der Kontext des Such-Treffers kann direkt aufgerufen werden.

Ein weiteres Auswertungstool ist <a href="https://search.projectarclight.org/" class="external-link" target="_blank">Arclight</a>, das Visualisierungen zu Ergebnissen von Suchanfragen an die MHDL generiert (vgl. {numref}`arclight_caligari`). In dem Sammelband _The Arclight guidebook to media history and the digital humanities_ werden verschiedene medienhistorische Forschungsprojekte vorgestellt, die unter anderem mit der MHDL und Arclight realisiert wurden, aber auch weitere Tools und Methoden der Digital Humanities anwenden. {cite}`ac-Acland_Hoyt_2016` 

```{figure} ../assets/einleitung/Arclight_Caligari.JPG
---
align: left
width: 100%
name: arclight_caligari
alt: Darstellung der Visualisierung einer Suche mit Arclight.
---
Screenshot Visualisierung mit Arclight
```

## Feministische Filmgeschichtsschreibung

Auch für die feministische Filmgeschichtsschreibung werden digitale Ansätze und Ressourcen immer wichtiger und eröffnen neue Möglichkeiten. So weist Sarah-Mai Dang darauf hin, dass digitale Archive einen relativ einfachen Zugang zu Materialien ermöglichen. Dadurch können individuelle Lebensgeschichten leichter sichtbar gemacht und das bisher vernachlässigte filmische Schaffen von Frauen genauer beleuchtet werden. {cite}`ac-Dang_2018` In der Filmgeschichtsschreibung wurde die Rolle von Frauen in allen Bereichen der Filmindustrie und des Filmschaffens lange nicht beachtet - insbesondere auch bei Forschungen zum frühen Film. Um dies zu ändern, wird z.B. seit 2013 das Webportal <a href="https://wfpp.columbia.edu/" class="external-link" target="_blank">Women Film Pioneers Project (WFPP)</a> betrieben, in dem Materialien zur Arbeit von Frauen auf allen Ebenen der Filmproduktion in der Stummfilmzeit frei zugänglich sind. Im Rahmen eines Forschungsprojektes hat sich Sarah-Mai Dang damit beschäftigt, wie Datenvisualisierungen zur feministischen Filmgeschichtsschreibung beitragen können. {cite}`ac-Dang_2024` Unter ihrer Leitung wurde der <a href="https://www.informatik.uni-marburg.de/women-film-pioneers-explorer/" class="external-link" target="_blank">Women Film Pioneers Explorer</a> entwicklet, der Informationen aus dem WFPP visualisiert und damit leichter erschließbar macht. {cite}`ac-Dang_2023`

```{figure} ../assets/einleitung/Women_Film_Pioneer_Explorer_Screenshot_Professions.PNG
---
align: left
width: 100%
name: pioneer_explorer
alt: Screenshot aus dem Women Film Pionieers Explorer - Dendrogram Professions
---
Screenshot Visualisierung "Dendrogram" Women Film Pioneers Explorer (<a href="https://www.informatik.uni-marburg.de/women-film-pioneers-explorer/Dendrogram.html" class="external-link" target="_blank">https://www.informatik.uni-marburg.de/women-film-pioneers-explorer/Dendrogram.html</a>)
```

Sarah-Mai Dang führt weiterhin aus, dass durch digitale Datenbanken und Plattformen wie etwa die MHDL oder <a href="https://echo.commarts.wisc.edu/" class="external-link" target="_blank">ECHO (Early Cinema History Online)</a> eine Fülle an Material in digitaler Form vorliegt und daher gezielt durchsucht werden kann. {cite}`ac-Dang_2018` Daraus ergibt sich die Möglichkeit, neue Fragen zur Filmgeschichte stellen und neue Perspektiven für die Filmwissenschaft einzunehmen. Durch Datenbanken könnten laut Dang zudem bisher übersehene Quellen und Zusammenhänge sichtbar gemacht werden, existierende Forschung bestätigt, aber auch hinterfragt und ausdifferenziert werden. Nicht zuletzt plädiert sie dafür, dass das Erstellen von Datensätzen und Datenbanken als akademische Tätigkeit anerkannt werden muss.

## Weitere Entwicklungen in der digitalen Forschung zur Filmgeschichtsschreibung

Digitale Ansätze sind für die Filmgeschichtsschreibung also durchaus gewinnbringend. In einem einführenden Beitrag zum Sonderheft _Digital Film Historiography: Challenges of/and Interdisciplinarity_ des <a href="https://culturalanalytics.org/issue/10778" class="external-link" target="_blank">Journal of Cultural Analytics</a> weisen die Herausgeber:innen Malte Hagener und Diana Roig-Sanz jedoch darauf hin, dass sich digitale Methoden in der Filmwissenschaft und Filmgeschichtsschreibung nur langsam etablieren und führen dies u.a. auf die Komplexität des multimodalen Objekts Film zurück. Einerseits erschwert die Datengröße der digitalen Formen die Arbeit, andererseits sind Fragen des Copyrights in Bezug auf Film besonders komplex. Zudem seien viele Quellen noch nicht digitalisiert und noch nicht online verfügbar. Strukturierte Datensätze müssen erst noch erstellt und Standards etabliert werden. Es gilt, neue digitale Methoden zu entwickeln und mit bestehenden Ansätzen zu kombinieren. Hierfür ist nicht zuletzt wie in allen Bereichen der Digital Humanities ein interdisziplinäres Arbeiten notwendig. Dass der Einsatz digitaler Tools und Vorgehensweisen für die filmwissenschaftliche und filmgeschichtliche Forschung fruchtbar sein können, zeigen die einzelnen Beiträge der Ausgabe. Deren Themen reichen von der Erfassung der Daten von deutschen Filmschaffenden im Filmexil 1933 bis 1945 {cite}`ac-Klages_2024` über die Auswertung visueller Muster in sowjetischen Wochenschauen {cite}`ac-Oiva_Ohm_Mukhina_Solà_Schich_2024` bis hin zu einer Annäherung an nationale Filmgeschichte mithilfe der Netzwerkanalyse. {cite}`ac-Hagener_Blaschke_2024`

In dem von Sarah-Mai Dang, Tim van der Heijden und Christian Gosvig Olesen herausgegebenen Sammelband _Doing Digital Film History: Concepts, Tools, Practices_ werden weitere aktuelle Tendenzen in der digitalen Filmgeschichtsforschung vorgestellt. {cite}`ac-Dang_van_der_Heijden_Olesen_2024` Der Band diskutiert in verschiedenen Beiträgen, wie digitale Technologien unser Verständnis von Film und Filmgeschichte verändern. Dabei wird eine interdisziplinäre Herangehensweise verfolgt und auf die Verbindung quantitativer und qualitativer Vorgehensweisen eingegangen. Auch hier wird ein breites Themenfeld filmgeschichtlicher Forschung mit digitalen Herangehensweisen abgedeckt, wobei der Band in vier größere Bereiche untereilt ist: Search - Data - Analysis - Visualization. Neben Forschungsdatenmanagement in der Filmwissenschaft {cite}`ac-Dang_2024b` wird auch kritisch auf die Problematik der Datenbereinigung eingegangen {cite}`ac-Schneider_Zimmermann_2025`, es werden Erfahrungen in der Lehre zu Digital Humanities und digitalen Tools in der Filmwissenschaft reflektiert {cite}`ac-Diecke_Hagener_2024`, Analysetools wie das Distant Viewing Toolkit dargestellt {cite}`ac-Heijden_Arnold_Tilton_2024` und die Möglichkeiten von Visualisierungen in der Medienwissenschaft ausgelotet. {cite}`ac-Burkhardt_Loist_2024`





Neues Wissen anwenden
Zum Abschluss dieser Lerneinheit können sie nun ihr neu erworbenes Wissen auf die Probe stellen. Bei den folgenden Multiple Choice Fragen sind gegebenenfalls auch mehrere richtige Antworten möglich. 

```{code-cell} ipython3
:tags: [remove-input]
display_quiz("../assets/assessment/einleitung/filmwissenschaft_dh_quiz.json", colors = colors.jupyterquiz)
```

## Literatur
```{bibliography}
:filter: docname in docnames
:keyprefix: ac-
```
