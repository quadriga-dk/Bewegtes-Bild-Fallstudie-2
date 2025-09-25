# Datenmodell
In den letzten Abschnitten wurde eine filmwissenschaftliche Fragestellung entwickelt und ein Filmkorpus eingegrenzt. Als Korpus wurden die studentischen Filme im Archiv der Filmuniversität Babelsberg KONRAD WOLF aus den Jahren 1985 bis 1999 identifiziert, für die nun **Metadaten in Form von filmografischen Angaben** erhoben werden sollen, die für die weitere Bearbeitung der Fragestellung erforderlich sind. Wie können diese Informationen in einer hierfür geeigneten Form erfasst werden?

## Datensätze aus dem Bibliothekskatalog

Bisher wurden die Datensätze zu einzelnen oder einer Gruppe von Filmen über den <a href="http://server8.bibl.filmuniversitaet.de/" class="external-link" target="_blank">Online-Bibliothekskatalog (OPAC)</a> der Filmuniversität mittels gezielter Suchanfragen abgerufen (vgl. Abschnitt [Materialrecherche](/recherche/material)). Im Rahmen dieser ersten Überblicks-Recherche zum vorhandenen Filmmaterial war es ausreichend, die filmografischen Daten per "Copy and Paste" aus der Trefferanzeige des Katalogs zu kopieren, z.B. in ein Textverarbeitungsprogramm oder ein Programm zur Tabellenkalkulation. Die Menge der recherchierten Filme blieb dabei übersichtlich, daher konnte auf diese Weise ein erster Vergleich und eine erste stichpunktartige Auswertung bezüglich potenzieller Gemeinsamkeiten stattfinden.

Für das gesamte Korpus der Filme wäre diese Vorgehensweise nicht durchzuführen: Bei der Überblicks-Recherche ergab sich auf die Suchanfrage nach studentischen Filmen aus den Jahren 1985 bis 1999 im Katalog eine Trefferanzahl von 1366 bibliografischen Einträgen. Welche alternativen Möglichkeiten zum manuellen Kopieren der Daten aus den OPAC in eine Datei gibt es nun? Um Informationen aus Webseiten zu extrahieren und zu speichern wird häufig das sogenannte "Web Scraping"[^1] angewendet, für das verschiedene Software-Tools zur Verfügung stehen. Web Scraping kann jedoch aus technischen Gründen nicht bei allen Web-Ressourcen eingesetzt werden.

## Auszug aus der Datenbank des Bibliothekskatalogs

Eine eigenständige automatisierte Verarbeitung der Daten aus der Oberfläche des OPACs war nicht möglich. Daher wurde der Systembibliothekar der Filmuniversität angefragt, ob er uns die OPAC-Daten zu den studentischen Filmen unseres Untersuchungszeitraums zur Verfügen stellen kann. Er erklärte sich bereit, für die Fallstudie einen Auszug aus der Datenbank des Bibliothekskatalogs zu erstellen, der alle Einträge aus dem OPAC für die Filme des Korpus enthält.

```{admonition} Achtung
:class: caution
Bei unserer weiteren Arbeit mit dem auf dem Auszug basierenden Datensatz zu den studentischen Filmen zur Wendezeit stellte sich heraus, dass dieser in den filmografischen Angaben personenbezogene Daten enthält. Da für diese Angaben nicht gesichert ist, dass die betroffenen Personen einer Veröffentlichung zugestimmt haben, können wir diesen Datensatz nun nicht publizieren. Auf die genauen Probleme die sich ergeben haben und die geltenden rechtlichen Rahmenbedingungen gehen wir im Kapitel zu [Problemfeldern](/publikation/problemfelder) bei der Datenpublikation noch ein. Für die Veranschaulichung der weiteren Arbeitsschritte verwenden wir einen synthetischen Datensatz, der im Kapitel zur [Datenbereinigung](/bereinigung/openRefine/0_datenbereinigung) besprochen wird.
```

Auch wenn der originale Datensatz im Rahmen unserer Fallstudie nicht veröffentlicht werden kann, stellen wir im Folgenden dennoch unsere weitere Vorgehensweise dar. Als Screenshots werden Einträge zu einem Werk genutzt, das später auf DVD veröffentlicht wurde – Andreas Dresens Film "Stilles Land" (1992). In diesem Fall kann davon ausgegangen werden, dass die Zustimmung der beteiligten Mitwirkenden für eine Veröffentlichung ihrer personenbezogenen Daten erteilt wurde.

Der Auszug aus der Datenbank des Bibliothekskatalogs liegt uns als tsv-Datei vor, also in Form einer Text-Datei, bei der die einzelnen Einträge zu den Filmtiteln durch Tabulatoren voneinander getrennt werden.[^2] Dabei sind die Informationen in einzelne Felder untergliedert, die innerhalb des OPACs unter "Vollanzeige des Titels" angezeigt werden. ({numref}`opac_vollanzeige_standard`)

```{figure} ../assets/bereinigung/modell/OPAC_Vollanzeige_Standard.png
---
align: left
width: 100%
name: opac_vollanzeige_standard
alt: Darstellung der Vollanzeige eines Einzeltitels im Katalog der Bibliothek der Filmuniversität. Der Anzeigeformat Standardformat ist mit einer roten Umrandung hervorgehoben.
---
Ausschnitt aus der Vollanzeige eines Einzeltitels im "Standardformat" im OPAC der Filmuniversität.
```

Wird in der Vollanzeige des Titels das Anzeigeformat "Feldnummern" angewählt, werden weitere Felder angezeigt, die im "Standardformat" nicht sichtbar waren, aber in der Auszugs-Datei enthalten sind. ({numref}`opac_vollanzeige_feldnummern`)

```{figure} ../assets/bereinigung/modell/OPAC_Vollanzeige_Feldnummern.png
---
align: left
width: 100%
name: opac_vollanzeige_feldnummern
alt: Darstellung der Vollanzeige eines Einzeltitels im Katalog der Bibliothek der Filmuniversität. Das Anzeigeformat Feldnummern ist mit einer roten Umrandung hervorgehoben.
---
Ausschnitt aus der Vollanzeige eines Einzeltitels im Anzeigeformat "Feldnummern" im OPAC der Filmuniversität.
```

In der Vollanzeige des Titels und in den verschiedenen Anzeigeformaten wird deutlich, dass die filmografischen Daten und damit die Metadaten zu den Titeln einer bestimmten Struktur, einem bestimmten Modell folgen. Auf die Funktion und auf den Aufbau solcher Datenmodelle geht Johanna Drucker ein. {cite}`c-Drucker_2021` Sie weist darauf hin, dass jede Erzeugung von Daten eine Modellierung beinhaltet. Durch ein Modell wird festgelegt, was als Merkmal des Datenobjekts – hier des jeweiligen Films – aufgeführt wird, d.h. was für die Charakterisierung als notwendig erachtet wird. Zudem muss entschieden werden, in welchem Format diese Informationen vorliegen sollen.

Mit Bezug auf Herbert Stachowiak führt Fotis Jannidis genauer aus, was mit dem Oberbegriff "Modell" gemeint ist. {cite}`c-Jannidis_2017` Er nennt drei Aspekte:

```{admonition} Aspekte eines Modells
:class: keypoint
- Ein Modell ist immer eine Abbildung, es repräsentiert etwas.
- Es ist nicht das Original, auch nicht dessen Kopie; es weist nicht alle Merkmale des Originals auf, sondern nur ausgewählte.
- Ein Modell hat einen oder mehrere Verwendungszwecke.
```

Dass eine Auswahl aus Merkmalen getroffen wird, impliziert auch, dass Modelle und damit Datenmodelle, wie schon im Abschnitt zu [Metadaten](/recherche/metadaten) ausgeführt, bestimmte Weltanschauungen, Werte und Werturteile enthalten. {cite}`c-Drucker_2021` 

## Analyse des Modells als Ausgangspunkt

Bevor existierende Daten – in dieser Fallstudie die Daten zu den Filmen aus dem OPAC der Filmuniversität – verwendet werden, sollte daher nach Drucker immer das zugrundeliegende Modell analysiert und verstanden werden. Welche Merkmale wurden aufgenommen? Fehlen evtl. bestimmte Merkmale? Wie sind Felder benannt und welche Klassifikationssysteme sind erkennbar?

Eine tiefgreifende Analyse des Datenmodells und der Struktur der OPAC-Daten kann an dieser Stelle nicht erfolgen. Auf Teile dieses Themenbereichs wird im folgenden Abschnitt zur Analyse der [Datenquelle](datenquelle) und im Abschnitt [Datenbereinigung](openRefine/0_datenbereinigung) nochmals eingegangen. Einen ausführlichen Überblick über die Prozesse bei der Erschließung von Metadaten zu Filmen für Kataloge liefert Anna Bohn. {cite}`c-Bohn_2018` 

Da es sich bei den OPAC-Daten um Daten aus einer existierenden Datenbank handelt, liegen diese in einer strukturierten Form vor. Aus der Vollanzeige des Titels im Bibliothekskatalog wird etwa deutlich, dass der Datensatz Informationen zu beteiligten Personen, Titel, Jahr und Format enthalten sollte. Zudem sind Schlagworte, Stichwörter und eine Inhaltsbeschreibung aufgeführt. Es zeigt sich jedoch auch, dass in einem Feld häufig mehrere Einträge aufgeführt werden. In dem jeweiligen Feld für "sonstige Personen" ist z.B. sowohl der Name der Person als auch deren Funktion(en) eingetragen (z.B. Regie, Drehbuch, Kamera, Darsteller:in etc.). Und das Feld "Umfang/Format" führt neben dem Filmformat (16mm, 35mm etc.) u.a. die Dauer in Minuten auf. ({numref}`opac_ausschnitt_vollanzeige`)

```{figure} ../assets/bereinigung/modell/OPAC_Ausschnitt_Vollanzeige.png
---
align: left
width: 100%
name: opac_ausschnitt_vollanzeige
alt: Darstellung des Ausschnitts einer Vollanzeige eines Einzeltitels im Katalog der Bibliothek der Filmuniversität. Das einzelne Felder sind mit einer roten Umrandung hervorgehoben.
---
Felder in der Vollansicht eines Eintrags des Bibliothekskatalogs
```

## Notwendige Datenbereinigung 

````{margin} 
```{admonition} Hinweis
:class: hinweis
Weitere Hinweise darauf, was eine effiziente Datenstruktur auszeichnet, finden sich bei <a href="https://quadriga-dk.github.io/Tabelle-Fallstudie-1/Markdown/20_Datenstruktur.html#" target="_blank">Fallstudie I - Tabelle</a>. 
```
````

Bereitet man die Daten zu den Filmen in Form einer Tabelle auf, enthält eine Zelle der Tabelle mehrere Informationen. Für eine Datenstruktur, die maschinell ausgewertet werden kann, darf jede Zelle lediglich einen eindeutigen Wert bzw. Eintrag aufweisen. Dies deutet darauf hin, dass der Datenauszug aus dem OPAC der Filmuniversität noch bearbeitet – also "bereinigt" werden muss, z.B. indem mehrere Werte in einer Zelle jeweils auf einzelne neue Zellen aufgeteilt werden. Für diese Bereinigung, aber auch für die weitere Arbeit mit dem Datensatz, ist es sinnvoll zu verstehen, nach welchen Kriterien die Erfassung der filmografischen Daten im Bibliothekskatalog stattgefunden hat, und warum diese Struktur gewählt wurde. Darauf wird im folgenden Abschnitt eingegangen.


## Literatur
```{bibliography}
:filter: docname in docnames
:keyprefix: c-
```


[^1]: Auf die genaue Funktionsweise von "Web Scraping" und die damit verbundenen rechtlichen und ethischen Fragen einzugehen, würde hier zu weit führen. Einen ersten Überblick liefert der <a href="https://de.wikipedia.org/wiki/Screen_Scraping" target="_blank">Wikipedia-Artikel</a> zum Thema.
[^2]: Die genauen Unterschiede zwischen verschiedenen Dateitypen, in denen Datensätze vorliegen (z.B. csv oder tsv), werden hier nicht weiter behandelt. Im Abschnitt zur [Datenbereinigung](openRefine/0_datenbereinigung) werden diese noch genauer dargestellt.


