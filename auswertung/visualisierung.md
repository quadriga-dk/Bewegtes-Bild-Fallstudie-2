# Grundlagen Visualisierung
Die im Datensatz unserer Fallstudie enthaltenen **Metadaten bzw. filmografischen Angaben** zu den studentischen Filmen sollen in den folgenden Abschnitten genauer analysiert werden. Eine Möglichkeit der Auswertung stellt die Visualisierung der Metadaten mit digitalen Tools dar. Durch diese Visualisierungen sollen Muster und Besonderheiten im Datensatz erkennbar werden.

Grundlage für die Auswertung sind die im Abschnitt zur [Operationalisierung der Fragestellung](/recherche/operationalisierung) erarbeiteten Teilfragestellungen, wie z.B. die Anzahl der Filmtitel zu bestimmten Zeitpunkten des Untersuchungszeitraums, die auftretenden Gattungsformen oder die Art der Projekte. Zunächst werden jedoch einige generelle Aspekte der Datenvisualisierung geklärt, um deren Möglichkeiten und Grenzen besser verständlich zu machen. Daran anschließend folgen im nächsten Abschnitt exemplarische Beispiele für Visualisierungen.

## Was ist Informationsvisualisierung?
Informations- bzw. Datenvisualisierung ist nicht auf wissenschaftliche Erkenntnisgewinnung beschränkt, sondern tritt auch im Alltag für die Darstellung komplexer Sachverhalte in visueller Form auf. Zum Beispiel kann die Darstellung der Organisationsstruktur einer Institution als Organigramm als Informationsvisualisierung verstanden werden.

Visualisierungen sind keine Erfindung des digitalen Zeitalters, sondern haben eine lange Tradition. Formen von Balken- und Liniendiagrammen waren bereits im 18. Jahrhundert gebräuchlich. {cite}`e-Drucker_2021` Alles, was quantifiziert und in einen numerischen Wert gebracht werden kann, ist auch in einer Visualisierung darstellbar, z.B. als Graph oder Diagramm. Hierfür genügen auch 'analoge' Hilfsmittel wie Papier und Stift, digitale Tools vereinfachen und erweitern lediglich die Darstellungsmöglichkeiten. 

Informationsvisualisierung wird häufig funktional definiert: Sie dient dazu, große Mengen abstrakter Daten so visuell so aufzuarbeiten, dass sie für Menschen erfassbar werden. {cite}`e-Rehbein_2017` Durch passende Visualisierungen von Daten ist es möglich, vorher verborgene Muster, Strukturen oder Auffälligkeiten zu erkennen.

Rehbein unterscheidet dabei drei verschiedene Funktionen von Informationsvisualisierungen im Forschungsprozess:

```{admonition} Funktionen von Visualisierungen im Forschungsprozess
:class: keypoint
* Präsentation: durch Visualisierungen werden wissenschaftliche Erkenntnisse anschaulich kommuniziert
* konfirmative Analyse: Visualisierungen dienen dazu, eine zuvor formulierte Hypothese durch verschiedene Sichtweisen auf die Daten zu verifizieren oder zu falsifizieren.
* explorative Analyse: mithilfe von Visualisierungen wird in den Daten nach latent vorhandenen Strukturen, Mustern, Trends und Auffälligkeiten gesucht, die zur Formulierung einer Forschungshypothese beitragen können
```

Im Rahmen unserer Fallstudie werden wir uns v.a. mit der explorativen Analyse beschäftigen.

## Informationsvisualisierung und Interpretation
Visualisierungen kommen zum Einsatz, wenn eine große Anzahl von Daten für Menschen erfassbar und lesbar gemacht werden soll. Sie ermöglichen es, komplexe Zusammenhänge in Datensätzen verständlich darzustellen. {cite}`e-Burkhardt_Loist_2024` Für Marcus Burkhardt und Skadi Loist ist diese auf den ersten Blick einfache Verständlichkeit von Visualisierungen dabei sowohl Versprechen als auch Gefahr. Karten, Graphen und Diagramme wirken unmittelbar zugänglich und scheinen eindeutige Aussagen zu liefern, gleichzeitig können sie aber auch suggestiv, irreführend und täuschend sein.

Visualisierungen sind nicht nur neutrale, leicht verständliche Darstellungen von Daten, sondern sind immer mit Interpretation durch die Personen, die diese erstellen, verbunden. Auf diesen Zusammenhang von Visualisierung und Interpretation weist auch Johanna Drucker hin. {cite}`e-Drucker_2021` Drucker argumentiert, dass Daten keine inhärente visuelle Form haben, die nur eine Darstellungsweise der Daten möglich macht. Vielmehr können Daten unterschiedlich visualisiert werden, wobei sich je nach Art der Daten manche Formen der Visualisierung besser eignen als andere.

Welche Art der Visualisierung gewählt wird, ist mit subjektiven Entscheidungen der Erstellenden verbunden. Visualisierungen müssen daher auch kritisch gelesen und interpretiert werden. Wer hat sie auf welcher Grundlage mit welchen Intentionen zu welchem Zweck produziert? Die Herausforderung besteht für Drucker darin, eine Form der Visualisierung zu finden, die der Forschungsaufgabe angemessen ist und neue Erkenntnisse vermitteln kann.

## Neue Formen der Visualisierung
Für die Suche nach neuen Erkenntnissen kann es notwendig sein, über bestehende Formen der Visualisierungen hinauszugehen und innovative Ansätze zu erproben. Im Rahmen seiner Arbeit zu _Cultural Analytics_ schlägt Lev Manovich innovative Herangehensweisen in Bezug auf graphische Darstellungen von Daten vor. Zunächst definiert Manovich _Informationsvisualisierung_ kompakt nochmals folgendermaßen:

> We can define _information visualization_ as a _mapping between data and a visual representation_. {cite}`e-Manovich_2020`

Informationsvisualisierungen folgen dabei nach Manovich bisher zwei Schlüsselprinzipien. Das erste dieser Prinzipien ist die _Reduktion_. Um Objekte und Beziehungen zwischen ihnen in Form von Punkten, Linien oder Kurven darstellen zu können, wird nur ein kleiner Teil der Merkmale der Objekte berücksichtigt, was zu einer Reduktion führt. Komplexe Strukturen sollen durch die Interaktion einfacher Elemente verstanden werden. Als zweites Prinzip führt Manovich an, dass bevorzugt _räumliche Variablen_ wie Position, Größe oder Form verwendet werden, um Unterschiede in Daten zu repräsentieren und Muster und Beziehungen erkennbar zu machen.

### Visualisierung ohne Reduktion
Im Rahmen sich verändernder technischer Möglichkeiten schlägt Manovich einen neuen Ansatz vor, den er _Visualisierung ohne Reduktion_ nennt. Dabei sollen wesentlich mehr Merkmale der Objekte erhalten bleiben. Die Komplexität und Individualität der Originaldaten soll bewahrt werden – im Gegensatz zur Reduktion der klassischen Formen der Informationsvisualisierung. Statt Datenpunkte zu aggregieren, wird versucht, große Datenmengen in ihrer Gesamtheit darzustellen, wobei jeder einzelne Datenpunkt sichtbar bleibt. Dies ist möglich, da die Objekte häufig bereits in digitaler Form vorliegen und für Visualisierungen mit digitalen Tools verarbeitet werden können. Z.B. können Worthäufungen in einem Text als _tag cloud_ dargestellt oder Abbildungen gemäß ihrer Farbwerte angeordnet werden. Beispiele hierfür finden sich auf der Projektseite von Manovichs <a href="https://lab.culturalanalytics.info/p/projects.html" class="external-link" target="_blank">Cultural Analytics Lab</a>.

### Beispiel Dsiga Vertov
Auch für Filme hat Manovich die Visualisierung ohne Reduktion anhand der Werke Dsiga Vertovs erprobt, also versucht, möglichst viele Bild-, Inhalts- und Strukturinformationen in der Visualisierung zu erhalten. {cite}`e-Manovich_2013` Adelheid Heftberger adaptierte seine Ansätze für ihre Arbeiten zu Vertov. {cite}`e-Heftberger_2016`; {cite}`e-heftberger_2018` Sie schlägt vor, Visualisierungen als exploratives Tool auf der Makro- und Mikroebene zu nutzen. Indem Bildfolgen mit einer Abbildung aus jeder Einstellung eines Vertov-Films erzeugt werden, können auftretende Muster in der Montage oder bei Einstellungslängen erkannt werden. Für die Darstellung von Einstellungslängen können z.B. jeweils ein Bild aus der Einstellung mit Balkendiagrammen zu den Längen kombiniert werden. Beispiele für solche Visualisierungen liefert das <a href="https://www.flickr.com/photos/culturevis/albums/72157632441192048/" class="external-link" target="_blank">zusätzliche Material</a> zu Manovichs Vertov-Artikel.

Dabei sollte im Blick behalten werden, dass trotz des Versuchs, eine _Visualisierung ohne Reduktion_ zu erstellen, nie alle Merkmale eines Objekts in eine grafische Darstellung einfließen können. Es muss also auch für diese Formen der Visualisierungen hinterfragt werden, welche Elemente in eine Daten-Visualisierung aufgenommen und welche außen vor gelassen werden.

## Visualisierungen in der Filmwissenschaft und in der Filmgeschichtsschreibung
Die Verwendung etablierter und leicht zu bedienender digitaler Visualisierungstools kann ebenfalls fruchtbar sein. Als Beispiele für solche Tools nennen Marcus Burkhardt und Skadi Loist <a href="https://www.rawgraphs.io/" class="external-link" target="_blank">RAWGraphs</a> oder <a href="https://www.tableau.com/de-de" class="external-link" target="_blank">Tableau</a> und gehen in ihrem Artikel näher auf <a href="https://gephi.org/" class="external-link" target="_blank">Gephi</a> ein. {cite}`e-Burkhardt_Loist_2024` Mit Gephi können komplexe Netzwerke visualisiert werden. Skadi Loist untersuchte z.B. mit solchen Netzwerk-Visualisierungen die Zirkulation von Filmen zwischen internationalen Festivals und wie Festivals durch diese Zirkulation miteinander verbunden sind. ({numref}`visualisierung_network_festival`) {cite}`e-Loist_2020`; {cite}`e-Loist_Samoilova_2023` Betrachtet wurde u.a., welche Festivals im Zentrum dieser Zirkulation stehen und welche eher an der Peripherie zu verorten sind.

```{figure} ../assets/auswertung/Visualisierung_FestivalNetwork_Samoilova_Loist.png
---
align: left
width: 100%
name: visualisierung_network_festival
alt: Abbildung Visualisierung "Core and periphery of the festival network"
---
Visualisierung "Core and periphery of the festival network" (Evgenia Samoilova, Skadi Loist, <a href="https://creativecommons.org/licenses/by/4.0/l" class="external-link" target="_blank">CC BY 4.0</a>, Quelle: <a href="https://figshare.com/articles/figure/Core_and_periphery_of_the_festival_network/25585602/1?file=45586989" class="external-link" target="_blank">https://figshare.com/articles/figure/Core_and_periphery_of_the_festival_network/25585602/1?file=45586989</a>)
```

Im Kapitel [Filmwissenschaft und Digital Humanities ](/einleitung/filmwissenschaft) wird erwähnt, dass auf der Grundlage der Einträge in der <a href="https://cinemetrics.uchicago.edu/" class="external-link" target="_blank">Cinemetrics-Datenbank</a> Visualisierungen erstellt werden können, die Plattform <a href="https://search.projectarclight.org/" class="external-link" target="_blank">Arclight</a> liefert Visualisierungen von Abfragen der <a href="https://mediahist.org/" class="external-link" target="_blank">Media History Digital Library (MHDL)</a>. Diese Visualisierungen sind für die Erforschung filmgeschichtlicher Fragestellungen nützlich.

Ein Beispiel für ein Visualisierungsprojekt zur feministischen Filmgeschichtsschreibung ist der <a href="https://www.informatik.uni-marburg.de/women-film-pioneers-explorer/" class="external-link" target="_blank">Women Film Pioneers Explorer</a>, der die Forschung über Frauen im frühen Film einem größeren Publikum zugänglich machen soll und von Sarah-Mai Dang im Rahmen eines Seminars und ihres Forschungsprojekts entwickelt wurde. {cite}`e-Dang_2023` Der _Women Film Pioneers Explorer_ basiert auf den Daten des ebenfalls im Kapitel [Filmwissenschaft und Digital Humanities ](/einleitung/filmwissenschaft) bereits kurz vorgestellten <a href="https://wfpp.columbia.edu/" class="external-link" target="_blank">Women Film Pioneers Project (WFPP)</a>. Das WFPP stellt Informationen zu Karrieren von über 300 Frauen im frühen Film zur Verfügung, die durch interaktive Visualisierungen erschlossen werden. Durch die Visualisierung eröffnen sich neue Perspektiven und bestehende Annahmen über Frauen im frühen Film können überprüft werden. So lassen sich z.B. mithilfe des _Explorers_ Cluster bilden, die die Berufsbezeichnungen wiedergeben. ({numref}`wfpp_1`)

```{figure} ../assets/auswertung/Women_Film_Pioneer_Explorer_Professions.JPG
---
align: left
width: 100%
name: wfpp_1
alt: Screenshot aus dem Women Film Pionieers Explorer zur Clusterbildung für Berufsbezeichnungen
---
Screenshot Visualisierung "Cluster Professions" Women Film Pioneers Explorer (<a href="https://www.informatik.uni-marburg.de/women-film-pioneers-explorer/Cluster.html" class="external-link" target="_blank">https://www.informatik.uni-marburg.de/women-film-pioneers-explorer/Cluster.html</a>)
```

Durch Klick auf die einzelnen Berufsbezeichnungen können weitere Untergruppen und auch die Einträge zu den Karrieren einzelner Frauen aufgerufen werden. Eine weitere Visualisierung hat die Form einer Landkarte, die die weltweiten Arbeitsorte von Frauen im frühen Film anzeigt. ({numref}`wfpp_2`) Linien machen ihre beruflichen Verbindungen in verschiedene Länder sichtbar. So wird deutlich, dass viele Frauen bereits damals international im Filmgeschäft tätig waren. 

```{figure} ../assets/auswertung/Women_Film_Pioneer_Explorer_Map.JPG
---
align: left
width: 100%
name: wfpp_2
alt: Screenshot aus dem Women Film Pionieers Explorer zur internationalen Verbindungslinien
---
Screenshot Visualisierung "Map" Women Film Pioneers Explorer (<a href="https://www.informatik.uni-marburg.de/women-film-pioneers-explorer/Map.html" class="external-link" target="_blank">https://www.informatik.uni-marburg.de/women-film-pioneers-explorer/Map.html</a>)
```

Sarah-Mai Dang weist darauf hin, dass durch diese Art der interaktiven Visualisierung nicht nur Informationen repräsentiert, sondern auch neue Informationen generiert und neue Fragen aufgeworfen werden. {cite}`e-Dang_2023` Solche Fragen können etwa sein, welche Frau wann wo mit wem an welchen Filmprojekten gearbeitet hat.

Nachdem nun einige Grundlagen der Datenvisualisierung dargelegt wurden, werden im folgenden Kapitel verschiedene Beispiele für Visualisierungen und Auswertungen zu unserer Fallstudie behandelt.


## Literatur
```{bibliography}
:filter: docname in docnames
:keyprefix: e-
```