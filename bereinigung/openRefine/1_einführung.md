# Einführung und Installation OpenRefine
```{figure} ../../assets/bereinigung/openRefine/einführung/OpenRefine_logo_(2018-present).svg
---
align: left
width: 100%
name: openRefine_logo_(2018-present)
alt: OpenRefine Logo (2018-heute)
---
OpenRefine Logo (2018-heute), übernommen von <a href="https://commons.wikimedia.org/wiki/File:OpenRefine_logo_%282018-present%29.svg" class="external-link" target="_blank">*wikimedia.org*</a>.
**"A power tool for working with messy data."**
```

*OpenRefine* ist eine OpenSource Software für die Bereinigung, Formatierung und Anreicherung von Datensätzen. Sie präsentiert die Datensätze in einer grafischen Benutzeroberfläche, die in ihrer tabellarischen Ansicht an Excel erinnert. In *OpenRefine* stehen jedoch zahlreiche Bearbeitungsfunktionen zur Verfügung, die weit über die Möglichkeiten von Excel hinausgehen und sonst nur durch die Anwendung verschiedener Programmiersprachen umgesetzt werden können. Zudem ist OpenRefine in der Lage, eine Vielzahl von Datei- und Datenformaten (z.B. csv, txt, xls) für die Verarbeitung einzulesen und später zu exportieren.[^1]

Zwischen 2010 und 2012 wurde *OpenRefine* als *GoogleRefine* von *Google* entwickelt. Nach dem Ende der Unterstützung durch Google wurde *OpenRefine* als freie Software veröffentlicht und weiterentwickelt, teilweise finden sich noch Artikel und Tutorials unter dem Namen *GoogleRefine*. 
Im Folgenden wird wiederholt auf die <a href="https://openrefine.org/docs" class="external-link" target="_blank">*OpenRefine* Dokumentation</a> verlinkt – in dieser werden Sie bei Fragen bezüglich des Programms schnell fündig.
Sie können sich zudem im <a href="https://forum.openrefine.org/c/community" class="external-link" target="_blank">offiziellen *OpenRefine* Forum</a> mit anderen Nutzenden austauschen oder dort die Lösung eines Problems finden. Die Entwicklung von *OpenRefine* sowie Fragen zu fehlenden Funktionen, Bugs als auch Workarounds werden außerdem in den <a href="https://github.com/OpenRefine/OpenRefine/issues" class="external-link" target="_blank">Issues des *OpenRefine* Github Repositorium</a>  diskutiert. 


```{admonition} OpenRefine Versionen
:class: keypoint
Für diese OER wurde die zum Zeitpunkt derer Erstellung aktuelle *OpenRefine* Version **3.9.3** vom **17.04.2025** verwendet. Ältere und neuere Versionen weisen ggf. Unterschiede bei der Arbeitsoberfläche und bei den Funktionalitäten auf. Sie finden sämtliche Versionen von *OpenRefine* <a href="https://github.com/OpenRefine/OpenRefine/releases" class="external-link" target="_blank">im GitHub Repositorium des Projekts</a>. 
```
## Installation

*OpenRefine* kann von der <a href="https://openrefine.org/download" class="external-link" target="_blank">Website des Projekts</a> heruntergeladen werden. Die Software wird lokal installiert, aber ähnlich wie die Office Produkte von *Google* über einen Browser ausgeführt. Als lokaler Webserver benötigt das Programm dabei keine aktive Internetverbindung. Unterstützt werden WebKit basierte Browser wie etwa

- Google Chrome
- Chromium
- Opera
- Microsoft Edge
- und Safari.

Bei anderen Browsern, wie z.B. *Firefox*, kann es zu Fehlern in der grafischen Darstellung kommen.

```{admonition} Fehler aufgrund des Browsers
:class: keypoint
Auch bei den offiziell unterstützen Browsern kann es zu Fehlermeldungen oder Bugs kommen, etwa aufgrund von Updates. In solchen Fällen muss ein anderer der unterstützten Browser verwendet werden. 
```

Nach der Installation kann *OpenRefine* gestartet werden. Es öffnet sich ein Terminal-Fenster (bzw. ein Anwendungsindikator im macOS Dock), das für die eigentliche Arbeit mit dem Programm nicht relevant ist, jedoch geöffnet bleiben muss. Die Benutzeroberfläche von *OpenRefine* wird über die Server-Adresse <a href="http://127.0.0.1:3333/" class="external-link" target="_blank">http://127.0.0.1:3333/</a> in einem Tab des Browsers geöffnet, beim Start des Programms geschieht dies in der Regel automatisch. 

Zum Beenden von *OpenRefine* schließen Sie zunächst alle Tabs des Browsers in denen das Programm ausgeführt wird. Anschließen klicken Sie bei Windows auf das geöffnete Terminal-Fenster und schließen dieses mit der Tasenkombibation `Strg` + `C`. Unter macOS schließen Sie *OpenRefine*, indem Sie es im Dock auswählen und mit `cmd` + `Q` beenden. Durch diese Art des Beendens des Programms wird gewährleistet, dass alle Änderungen die mit *OpenRefine* durchgeführt wurden auch sicher abgespeichert werden.

Zusätzliche Informationen zur Installationen und den Systemvoraussetzungen finden Sie auf <a href="https://openrefine.org/docs/manual/installing" class="external-link" target="_blank">dieser Seite der OpenRefine Dokumentation</a>.

## Grenzen von OpenRefine

````{margin} 
```{admonition} Hinweis
:class: hinweis
Eine Einführung zu _Python_  findet sich unter <a href="https://programming-24.mooc.fi" class="external-link" target="_blank"> "Python Programming MOOC 2024"</a>.
```
````

Neben OpenRefine wurde bei der Bereinigung des originalen Datensatzes auch die Programmiersprache *Python* genutzt, um die grundlegende Struktur des Datensatzes zu ändern. Zwar sind diese Änderungen größtenteils auch innerhalb von OpenRefine realisierbar, dies wäre jedoch mit einem erheblich höheren, manuellen Aufwand und entsprechend hoher Fehleranfälligkeit verbunden. So ist es etwa in OpenRefine nicht möglich, auf der Grundlage von Spalten-übergreifenden Regeln neue Spalten zu erstellen oder Einträge zu verschieben. Die Stärke von *OpenRefine* liegt weniger in solchem <a href="https://en.wikipedia.org/wiki/Data_wrangling" class="external-link" target="_blank">*Data wrangling*</a>, als vielmehr in der genauen Bereinigung der Einträge selbst. 



Eine Einführung in die Programmierung mit *Python* ist im Rahmen dieser OER nicht zielführend. Für einen Einstieg in *Python* und die Arbeit mit Datensätzen ist der Kurs <a href="https://programming-24.mooc.fi" class="external-link" target="_blank"> *Python Programming MOOC 2024*</a> der Universität Helsinki zu empfehlen.

[^1]: Eine Auflistung der mit *OpenRefine* einlesbaren Datenformate und Quellen findet sich in Abschnitt [Vorbereitung und Import des Datensatzes](2_import.md) und in der <a href="https://openrefine.org/docs/manual/starting" class="external-link" target="_blank">*OpenRefine* Dokumentation</a>. 