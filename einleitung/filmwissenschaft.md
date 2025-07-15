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

# Filmwissenschaft und Digital Humanities
Im folgenden Kapitel werden einige Grundzüge der Digital Humanities und deren Rolle in der Filmwissenschaft vorgestellt. Dadurch sollen Grundlagen für das Verständnis der Fallstudie gelegt werden, auf die sich die vorliegende _Open Educational Resource_ bezieht. Dabei werden folgende Lernziele verfolgt:

```{admonition} Grundzüge der Digital Humanities und deren Rolle in der Filmwissenschaft
:class: lernziele
1. Die Lernenden sind mit Definitionsansätzen und Arbeitsbereichen der Digital Humanities vertraut.
```

## Digital Humanities
Immer mehr Quellen aus den geisteswissenschaftlichen Disziplinen liegen mittlerweile in digitaler Form vor. Gedruckte Zeitungsartikel, Bücher oder Fotomaterial werden digitalisiert, Informationen zu kulturellen Artefakten in Online-Datenbanken zugänglich gemacht und kulturelle, politische oder geschichtliche Themen in wissenschaftlichen Blogs und speziellen Portalen im Internet aufbereitet. Durch diese **Retrodigitalisierung** analoger Materialien und die wachsende Anzahl genuin digitaler Quellen ergeben sich neue Chancen, aber auch Herausforderungen für die Geisteswissenschaften. Für die Geschichtsforschung stellt Peter Haber angesichts der "Digitalität von immer mehr zeithistorischen Quellen" die Frage in den Raum, ob nicht mehr wie früher ein Mangel, sondern mittlerweile vielmehr ein Überfluss an verfügbaren Informationen und Quellen herrsche. {cite}`Haber_2012`

### Definitionsansätze

Angesichts der rasant voranschreitenden Digitalisierung, die auch geisteswissenschaftliche Arbeitsfelder betrifft, sind neue Herangehensweisen und Methoden notwendig, die dieser immer weiter wachsenden Anzahl an potentiell zur Verfügung stehenden Daten und Quellen Rechnung trägt. Immer häufiger ist die Rede von **"Digital Humanities"** - auch wenn es nach wie vor schwer fällt, diesen Begriff zu definieren. Manfred Thaller versteht die Digital Humanities zunächst "als die Summe aller Versuche, die Informationstechniken auf den Gegenstandsbereich der Geisteswissenschaften anzuwenden." {cite}`Thaller_2017` Es tut sich für ihn somit ein recht breites Feld an möglichen Untersuchungsgegenständen auf: Angefangen bei Texten über nicht-textuelle Medien wie Tonaufnahmen, Noten, Bilder oder Filme und geografischen Informationen bis hin zu den neuen Technologien selbst als Gegenstand. Aus den jeweiligen Quellen müssen Daten extrahiert und in eine gut strukturierte Form gebracht werden, damit sie mit digitalen Methoden und Werkzeugen ausgewertet werden können.

Auch Mareike König betont, dass eine einheitliche Definition von Digital Humanities nicht existiert. Ihr Definitionsversuch lautet, "dass die Digital Humanities die Entwicklung, Anwendung und Erforschung von digitalen Techniken, Methoden und Medien zur Beantwortung geisteswissenschaftlicher Fragestellungen umfassen." {cite}`König_2021` Wichtiger Bestandteil der Digital Humanities ist für sie die Selbstreflexion digitaler Forschungs- und Publikationsprozesse sowie eine entsprechende Theoriebildung.

### Nutzen digitaler Verfahren

Welche Chancen bieten die Digital Humanities? Ein Vorteil von digitalen Herangehensweisen ist, dass nicht nur immer größere Mengen an digitalen Quellen zur Verfügung stehen, sondern diese auch auf eine Art und Weise ausgewertet werden können, die bisher nicht möglich war. In sehr großen Textmengen kann etwa nach wiederkehrenden Mustern, Wortgruppen oder Motiven gesucht werden, die der menschlichen Wahrnehmung sonst verborgen bleiben - allein schon deshalb, weil niemand diese Menge an Texten selbst lesen, geschweige denn aufbereiten könnte. Durch diese digitale Art der Auswertung können sich neue Fragestellungen ergeben, sowie bisherige Annahmen aufgrund dieser quantitativen Untersuchungen überprüft und neu beleuchtet werden. Im Idealfall ergänzen sich neuere quantitative und klassische qualitative geisteswissenschaftliche Herangehensweisen und können so zu neuen Erkenntnissen führen. Nicht zuletzt werden die digitalisierten Quellen und erarbeiteten Forschungsdaten in Repositorien und Datenbanken öffentlich zugänglich gemacht und leisten somit einen Beitrag auf dem Weg zur Nachnutzbarkeit in Open Science.


## Filmwissenschaft
Auch in der Filmwissenschaft werden Ansätze der Digital Humanities immer wichtiger. Dabei sind datengetriebene, quantitative Vorgehensweisen schon länger in Gebrauch. Bereits in den 1970er-Jahren setzte sich Barry Salt dafür ein, statistische Methoden für die Analyse von Filmen anzuwenden {cite}`Salt_1974` und baute seine Überlegungen in den folgenden Jahren weiter aus {cite}`Salt_2009`. Eine wichtige Größe für die statistische Filmanalyse ist für Salt die "Average shot lenght" (ASL), also die durchschnittliche Länge der Einstellungen eines Films, die sich aus der Länge des Films geteilt durch die Anzahl der Einstellungen errechnet. Davon ausgehend kann z.B. auf die Häufigkeit von Schnitten und damit auf verschiedene Montagestile rückgeschlossen werden. Neben der ASL wurden auch Einstellungsgrößen und Kamerabewegungen in Einstellungen quantitativ erfasst und statistisch ausgewertet.

### Datenbanken und digitale Tools

Die Erhebung dieser Werte erfolgte zu Beginn meist noch rein manuell ohne Einbeziehung computergestützter Mittel. Yuri Tsivian {cite}`Tsivian_2009` nahm Salts Ansatz auf und führte ihn in Form von "Cinemetrics" weiter. Er entwickelte ein einfaches digitales Tool, mit dem die Einstellungswechsel bei der Sichtung eines Films manuell erfasst werden können. Die so erhaltenen Werte, also die Zahl der Einstellungen in einem Film und die Länge der Einstellungen werden im Anschluss in eine Datenbank im Internet hochgeladen, wo eine statistische Auswertung dieser Daten erfolgt. Dies geschieht über die <a href="https://cinemetrics.uchicago.edu/" class="external-link" target="_blank">Cinemetrics Website</a>, auf der neben der ASL unter anderem die Dauer der längsten und kürzesten Einstellung, die Anzahl der Einstellungen oder die Gesamtlänge des Films aufgeführt werden. Ebenso können auf der Grundlage dieser Daten verschiedene Visualisierungen erstellt werden (vgl. {numref}`cinemetrics_visualisierung`). Diese Datenbank ist frei zugänglich, alle können also sowohl Daten zur Verfügung stellen als auch mit den vorhandenen Daten arbeiten.

```{figure} ../assets/einleitung/Cinementrics_Visualisierung.JPG
---
align: left
width: 100%
name: cinemetrics_visualisierung
alt: Screenshot Darstellung der Visualisierung eines Eintags aus der Cinemetrcis-Datenbank.
---
Screenshot der Visualisierung eines Eintrags aus der Cinemetrcis-Datenbank
```

Viele Datenbanken mit filmografischen Angaben, wie z.B. Titel, Entstehungsjahr, beteiligte Personen, Produktionsländer oder Festivalpremieren sind frei zugänglich. Beispiele hierfür sind etwa <a href="https://www.imdb.com/" class="external-link" target="_blank">IMDb</a>, <a href="https://www.ofdb.de/"  class="external-link" target="_blank">OFDb</a> oder <a href="https://www.filmportal.de/" class="external-link" target="_blank">filmportal.de</a>. Diese Datenbanken liefern Daten und Metadaten zu Filmen, die unter verschiedenen Perspektiven ausgewertet werden können. {cite}`Stelmach_2024` Für Analysen im Rahmen der Production Studies sind etwa Zusammensetzungen der Filmcrew, Produktionsbudgets oder Förderungen interessant, Webseiten mit Ratings, Rezensionen, digitalisierte Presseartikel oder Kinoprogramme ermöglichen die Auswertung der Rezeption von Filmen.

Zu beachten ist hierbei, dass bei der Publikation von Daten aus solchen frei zugänglichen Datenbanken im Rahmen eigener Forschungsprojekte bestimmte rechtliche Rahmenbedingungen eingehalten werden müssen. Auf dieses Thema wird im Kapitel zu [Problemfeldern](/publikation/problemfelder) bei der Datenpublikation noch näher eingegangen.

### Formen der Visualisierung

Die große Anzahl an Film- und Metadaten erfordert neue Formen der kritischen Einordnung und Auswertung der Informationen. Eine mögliche Form der Datenerschließung ist die Visualisierung. Im Rahmen seines Ansatzes der **"Cultural Analytics"** hat sich Lev Manovich intensiv mit Möglichkeiten und Techniken der Visualisierung von (kulturellen) Informationen auseinandergesetzt und stellt als einen Ansatz die "Visualisierung ohne Reduktion" heraus, bei der möglichst alle vorhandenen Informationen in der Visualisierung erhalten bleiben. {cite}`Manovich_2020` Diesen Ansatz greift Adelheid Heftberger in ihrer Arbeit zu Dsiga Vertovs Filmen auf und entwickelt ihn weiter. {cite}`Heftberger_2016` 

```{figure} ../assets/einleitung/Heftberger_Materiality_and_Montage_Vertov.jpg
---
align: left
width: 100%
name: vertov_visualisierung
alt: Close-ups von Gesischtern in "The Eleventh Year" (Dziga Vertov, 1928)
---
Close-ups von Gesichtern in "The Eleventh Year" (Dziga Vertov, 1928) (Quelle: {cite}`heftberger_2018`, <a href="https://creativecommons.org/licenses/by/4.0/legalcode"  class="external-link" target="_blank">CC BY 4.0</a>)
```

Sie bestimmt die Länge der Einstellungen von Vertovs Filmen und erstellt mit Einzelbildern aus den Einstellungen Visualisierungen, aus denen Muster im Schnitt oder auch die Wiederkehr einzelner Einstellungen ersichtlich werden. {cite}`heftberger_2018` Komplexe Montagefolgen können so besser erfasst und ausgewertet werden.

### Filmanalytische Tools

````{margin} 
```{admonition} Hinweis
:class: hinweis
Eine ausführliche Vorstellung filmanalytischer Tools findet sich bei <a href="https://quadriga-dk.github.io/Bewegtes-Bild-Fallstudie-1/intro.html" target="_blank">Fallstudie I - Bewegtes Bild</a>. 
```
````

Digitale Tools können auch filmanalytische Prozesse unterstützen. Sie erleichtern die Erstellung von Annotationen zu einzelnen Filmen, also die Anreicherung von Filmen mit zusätzlichen Informationen zu dessen verschiedenen medialen Ebenen, wie etwa Tongestaltung, Bild oder Musikeinsatz. Es entstehen digitale Filmprotokolle, durch die Eigenschaften eines Films erfassbar und analysierbar werden sollen. Diese Annotationen können wiederum unter Einbeziehung digitaler Tools ausgewertet und mit Annotationen zu anderen Filmen in Beziehung gesetzt werden.

Annotiert werden Elemente wie Montage, Kamera, Bildkomposition, auftretende Figuren, Dialoge oder Motive. {cite}`Bakels_Grotkopp_Scherer_Stratil_2020` Beispiele für solche Tools sind etwa <a href="https://archive.mpi.nl/tla/elan" class="external-link" target="_blank">ELAN</a>, das ursprünglich für linguistische Analysen konzipiert wurde, <a href="https://www.vian.app/" class="external-link" target="_blank">VIAN</a>, das den Fokus v.a. auf die Analyse von Farbe im Film legt und <a href="https://advene.org/" class="external-link" target="_blank">Advene</a>, bei dem Annotationselemente aufeinander bezogen werden können. Solche Tools zur digitalen Filmanalyse werden fortlaufend weiterentwickelt: Einzelne Annotationskomponenten wie z.B. die Erkennung der Länge von Einstellungen oder der Texte von Dialogen können immer besser automatisiert erfasst werden. Andere Elemente, wie Kamerabewegungen oder Einstellungsgrößen, müssen meist noch manuell eingegeben oder stark nachgebessert werden. Manuelle und automatische Annotationen werden miteinander verzahnt, die Annotationsergebnisse sollen maschinenlesbar und weiterverarbeitbar sein. Mit ihnen ist z.B. die Erstellung von Visualisierungen möglich, die Muster audiovisueller Kompositionen sichtbar und besser auswertbar machen.

### Distant Viewing

Neben der Annotation einzelner Filme wird mit Unterstützung digitaler Werkzeuge die (teil-)automatisierte Analyse einer großen Menge von Filmen möglich. Franceso Moretti entwickelte den literaturwissenschaftlichen Ansatz des "distant reading" {cite}`Moretti_2016`, bei dem digitalisierte Texte nach bestimmten Mustern, Motiven oder Wortgruppen durchsucht werden. In Form des "distant viewing" übertragen Taylor Arnold und Lauren Tilton diesen Ansatz auf die Analyse (audio-)visueller Werke. {cite}`Arnold_Tilton_2023` Sie setzen sich in diesem Kontext mit den Möglichkeiten und Grenzen von 'computer vision' auf der Grundlage von Algorithmen sowohl theoretisch als auch praktisch auseinander. Für die praktische Anwendung des Distant-Viewing-Ansatzes haben sie das <a href="https://github.com/distant-viewing/dvt" class="external-link" target="_blank">Distant Viewing Toolkit</a> entwickelt, das auf der Programmiersprache Python basiert. Mit diesem Toolkit ist es möglich, automatisiert Annotationen zu erstellen, z.B. welche Figuren oder Objekte im Bild sichtbar sind oder wie lange die einzelnen Einstellungen dauern. Auf der Grundlage dieser Annotationen können wiederum Muster erkannt, Gemeinsamkeiten und Unterschiede in einem Korpus von Filmen herausgearbeitet werden. Arnold und Tilton haben dies exemplarisch an der Untersuchung zweier US-amerikanischer TV-Sitcoms aus den 1960er Jahren und in Zusammenarbeit mit Tim van der Heijden für Amateurvideos aufgezeigt. {cite}`Arnold_Tilton_Berke_2019`; {cite}`Heijden_Arnold_Tilton_2024`

### Forschungsdaten

Beim "distant viewing", aber auch bei allen anderen digitalen, computergestützten Ansätzen in der Filmwissenschaft, entstehen Forschungsdaten (siehe hierzu auch das Kapitel [Datenpublikation](../publikation/forschungsdaten)). Diese Daten sollen langfristig gespeichert und für andere Wissenschaftler:innen zugänglich gemacht werden. Die hierfür notwendige Infrastruktur befindet sich noch im Aufbau. Wichtig ist hierbei neben der langfristigen Speicherung auch die Auffindbarkeit und die Zugänglichkeit der Daten. {cite}`Hagener_Kammerer_2020` Zudem muss die Entstehung der Daten nachvollziehbar und deren Qualität einschätzbar sein. Nur so können diese potentiell von anderen Wissenschaftler:innen in anderen Forschungskontexten nachgenutzt werden.

Bei der Datenpublikation müssen zudem rechtliche Aspekte berücksichtigt werden. Insbesondere bei Filmwerken ist in diesem Kontext die Beachtung von Urheberrechten relevant, aber auch Fragen des Datenschutzes, wie z.B. Vorschriften zum Umgang mit personenbezogenen Daten, sind zu bedenken. Personenbezogene Daten können etwa in filmografischen Angaben eine Rolle spielen. Das komplexe Themenfeld der rechtlichen Rahmenbedingungen wird im Kapitel zu [Problemfeldern](/publikation/problemfelder) bei der Datenpublikation genauer behandelt.

Als Speicherort für Forschungsdaten stehen verschiedene Repositorien zur Verfügung. Für die Film- und Medienwissenschaft hat sich etwa <a href="https://mediarep.org/communities/7e880a5a-5bcd-49b7-9b0e-ce4851b8d7bf" class="external-link" target="_blank">media/rep/</a> etabliert. <a href="https://zenodo.org/" class="external-link" target="_blank">Zenodo</a> bietet ebenfalls die Möglichkeit, Forschungsdaten zu publizieren und bei <a href="https://www.re3data.org/" class="external-link" target="_blank">re3data</a> kann nach Repositorien recherchiert werden.

## Filmgeschichtsschreibung
Neben Repositorien stellen Datenbanken mit digitalisierten Materialien, wie Text- und Bildmaterial, zu Filmen und zur Filmgeschichte wichtige Quellen für die computergestützte filmwissenschaftliche Forschung dar. Solche Datenbanken sind über Web-Portale meist frei zugänglich und bieten verschiedene Recherchemöglichkeiten. Ein wichtiges Beispiel und Vorbild für Projekte ähnlicher Art ist die <a href="https://mediahist.org/" class="external-link" target="_blank">Media History Digital Library (MHDL)</a>, die mittlerweile fast drei Millionen gescannte Seiten umfasst. Die MHDL enthält dabei vor allem US-amerikanische Zeitschriften und Bücher, der Bestand reicht bis in die 1960er Jahre. Nach US-amerikanischem Recht sind viele Publikationen, die bis zu diesem Zeitraum erschienen sind, nicht mehr durch das Copyright geschützt und können öffentlich zugänglich gemacht werden. {cite}`Hagener_Kammerer_2020` 

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

Ein weiteres Auswertungstool ist <a href="https://search.projectarclight.org/" class="external-link" target="_blank">Arclight</a>, das Visualisierungen zu Ergebnissen von Suchanfragen an die MHDL generiert (vgl. {numref}`arclight_caligari`). In dem Sammelband _The Arclight guidebook to media history and the digital humanities_ werden verschiedene medienhistorische Forschungsprojekte vorgestellt, die unter anderem mit der MHDL und Arclight realisiert wurden, aber auch weitere Tools und Methoden der Digital Humanities anwenden. {cite}`Acland_Hoyt_2016` 

```{figure} ../assets/einleitung/Arclight_Caligari.JPG
---
align: left
width: 100%
name: arclight_caligari
alt: Darstellung der Visualisierung einer Suche mit Arclight.
---
Screenshot Visualisierung mit Arclight
```

### Feministische Filmgeschichtsschreibung

Auch für die feministische Filmgeschichtsschreibung werden digitale Ansätze und Ressourcen immer wichtiger und eröffnen neue Möglichkeiten. So weist Sarah-Mai Dang darauf hin, dass digitale Archive einen relativ einfachen Zugang zu Materialien ermöglichen. Dadurch können individuelle Lebensgeschichten leichter sichtbar gemacht und das bisher vernachlässigte filmische Schaffen von Frauen genauer beleuchtet werden. {cite}`Dang_2018` In der Filmgeschichtsschreibung wurde die Rolle von Frauen in allen Bereichen der Filmindustrie und des Filmschaffens lange nicht beachtet - insbesondere auch bei Forschungen zum frühen Film. Um dies zu ändern, wird z.B. seit 2013 das Webportal <a href="https://wfpp.columbia.edu/" class="external-link" target="_blank">Women Film Pioneers Project (WFPP)</a> betrieben, in dem Materialien zur Arbeit von Frauen auf allen Ebenen der Filmproduktion in der Stummfilmzeit frei zugänglich sind. Im Rahmen eines Forschungsprojektes hat sich Sarah-Mai Dang damit beschäftigt, wie Datenvisualisierungen zur feministischen Filmgeschichtsschreibung beitragen können. {cite}`Dang_2024` Unter ihrer Leitung wurde der <a href="https://www.informatik.uni-marburg.de/women-film-pioneers-explorer/" class="external-link" target="_blank">Women Film Pioneers Explorer</a> entwicklet, der Informationen aus dem WFPP visualisiert und damit leichter erschließbar macht. {cite}`Dang_2023`

```{figure} ../assets/einleitung/Women_Film_Pioneer_Explorer_Screenshot_Professions.PNG
---
align: left
width: 100%
name: pioneer_explorer
alt: Screenshot aus dem Women Film Pionieers Explorer - Dendrogram Professions
---
Screenshot Visualisierung "Dendrogram" Women Film Pioneers Explorer (<a href="https://www.informatik.uni-marburg.de/women-film-pioneers-explorer/Dendrogram.html" class="external-link" target="_blank">https://www.informatik.uni-marburg.de/women-film-pioneers-explorer/Dendrogram.html</a>)
```

Sarah-Mai Dang führt weiterhin aus, dass durch digitale Datenbanken und Plattformen wie etwa die MHDL oder <a href="https://echo.commarts.wisc.edu/" class="external-link" target="_blank">ECHO (Early Cinema History Online)</a> eine Fülle an Material in digitaler Form vorliegt und daher gezielt durchsucht werden kann. {cite}`Dang_2018` Daraus ergibt sich die Möglichkeit, neue Fragen zur Filmgeschichte stellen und neue Perspektiven für die Filmwissenschaft einzunehmen. Durch Datenbanken könnten laut Dang zudem bisher übersehene Quellen und Zusammenhänge sichtbar gemacht werden, existierende Forschung bestätigt, aber auch hinterfragt und ausdifferenziert werden. Nicht zuletzt plädiert sie dafür, dass das Erstellen von Datensätzen und Datenbanken als akademische Tätigkeit anerkannt werden muss.

### Weitere Entwicklungen in der digitalen Forschung zur Filmgeschichtsschreibung

Digitale Ansätze sind für die Filmgeschichtsschreibung also durchaus gewinnbringend. In einem einführenden Beitrag zum Sonderheft _Digital Film Historiography: Challenges of/and Interdisciplinarity_ des <a href="https://culturalanalytics.org/issue/10778" class="external-link" target="_blank">Journal of Cultural Analytics</a> weisen die Herausgeber:innen Malte Hagener und Diana Roig-Sanz jedoch darauf hin, dass sich digitale Methoden in der Filmwissenschaft und Filmgeschichtsschreibung nur langsam etablieren und führen dies u.a. auf die Komplexität des multimodalen Objekts Film zurück. Einerseits erschwert die Datengröße der digitalen Formen die Arbeit, andererseits sind Fragen des Copyrights in Bezug auf Film besonders komplex. Zudem seien viele Quellen noch nicht digitalisiert und noch nicht online verfügbar. Strukturierte Datensätze müssen erst noch erstellt und Standards etabliert werden. Es gilt, neue digitale Methoden zu entwickeln und mit bestehenden Ansätzen zu kombinieren. Hierfür ist nicht zuletzt wie in allen Bereichen der Digital Humanities ein interdisziplinäres Arbeiten notwendig. Dass der Einsatz digitaler Tools und Vorgehensweisen für die filmwissenschaftliche und filmgeschichtliche Forschung fruchtbar sein können, zeigen die einzelnen Beiträge der Ausgabe. Deren Themen reichen von der Erfassung der Daten von deutschen Filmschaffenden im Filmexil 1933 bis 1945 {cite}`Klages_2024` über die Auswertung visueller Muster in sowjetischen Wochenschauen {cite}`Oiva_Ohm_Mukhina_Solà_Schich_2024` bis hin zu einer Annäherung an nationale Filmgeschichte mithilfe der Netzwerkanalyse. {cite}`Hagener_Blaschke_2024`

In dem von Sarah-Mai Dang, Tim van der Heijden und Christian Gosvig Olesen herausgegebenen Sammelband _Doing Digital Film History: Concepts, Tools, Practices_ werden weitere aktuelle Tendenzen in der digitalen Filmgeschichtsforschung vorgestellt. {cite}`Dang_van_der_Heijden_Olesen_2024` Der Band diskutiert in verschiedenen Beiträgen, wie digitale Technologien unser Verständnis von Film und Filmgeschichte verändern. Dabei wird eine interdisziplinäre Herangehensweise verfolgt und auf die Verbindung quantitativer und qualitativer Vorgehensweisen eingegangen. Auch hier wird ein breites Themenfeld filmgeschichtlicher Forschung mit digitalen Herangehensweisen abgedeckt, wobei der Band in vier größere Bereiche untereilt ist: Search - Data - Analysis - Visualization. Neben Forschungsdatenmanagement in der Filmwissenschaft {cite}`Dang_2024b` wird auch kritisch auf die Problematik der Datenbereinigung eingegangen {cite}`Schneider_Zimmermann_2025`, es werden Erfahrungen in der Lehre zu Digital Humanities und digitalen Tools in der Filmwissenschaft reflektiert {cite}`Diecke_Hagener_2024`, Analysetools wie das Distant Viewing Toolkit dargestellt {cite}`Heijden_Arnold_Tilton_2024` und die Möglichkeiten von Visualisierungen in der Medienwissenschaft ausgelotet. {cite}`Burkhardt_Loist_2024`



## Neues Wissen anwenden
Zum Abschluss dieser Lerneinheit können sie nun ihr neu erworbenes Wissen auf die Probe stellen. Bei den folgenden Multiple Choice Fragen sind gegebenenfalls auch mehrere richtige Antworten möglich. 

```{code-cell} ipython3
:tags: [remove-input]
display_quiz("../assets/assessment/einleitung/filmwissenschaft_dh_quiz.json", colors = colors.jupyterquiz)
```


## Literatur
```{bibliography}
:filter: docname in docnames
```
