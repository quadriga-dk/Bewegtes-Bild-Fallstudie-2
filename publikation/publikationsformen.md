# Formen der Datenpublikation
Um die eigene Forschung sichtbar und nachvollziehbar zu machen und um die erhobenen Daten in anderen Forschungsprojekten nachzunutzen, sollten Datensätze publiziert werden. Für die Form solcher Publikationen hat sich bisher noch kein allgemeingültiger Standard entwickelt. Sophie Einwächter führt aus, dass in der Medienwissenschaft wie auch in anderen Geisteswissenschaften bisher Erfahrungen mit Datenpublikationen fehlen und sich diese zudem erst als anerkannte wissenschaftliche Publikationsform etablieren müssen. {cite}`g-Einwächter_2022`

Als Orte für die langfristige Datenspeicherung bieten sich die im letzten Kapitel dargestellten Repositorien an, die zudem die Kriterien der Zugänglichkeit und Auffindbarkeit erfüllen. Grob lassen sich dabei drei verschiedene Formen der Datenpublikation unterscheiden:

```{admonition} Formen der Datenpublikation
:class: keypoint
* In einem wissenschaftlichen Beitrag werden Forschungsergebnisse veröffentlicht und dabei auf Daten verwiesen, die in einem Repositorium abgelegt sind.
* Daten werden mit einer kompakten Beschreibung in einem Repositorium publiziert.
* In einem Data Paper werden in einem Repositorium gespeicherte Daten ausführlich beschrieben und deren Potenzial analysiert.
```

Diesen drei Formen werden im Folgenden betrachtet.

## Artikel mit Verweis auf Daten im Repositorium
Wissenschaftliche Artikel, die Forschungsergebnisse darstellen und deren Qualität durch den Prozess eines Peer-Reviews sichergestellt wird, sind als Publikationsform etabliert. In einem solchen Beitrag können Daten bezüglich einer Forschungsfrage ausgewertet und die Datenanalyse in die Argumentation eingebaut werden. Im Artikel wird auf Daten verwiesen, die an einem öffentlich zugänglichen Speicherort wie einem Repositorium abgerufen werden können. Teilweise schreiben es die Regularien eines Publikationsmediums vor, dass zugehörige Daten für den Review-Prozess verfügbar sein und anschließend auch veröffentlicht werden müssen.

Beispiele für diese Art der Publikationsform werden im Abschnitt zu [Filmwissenschaft und Digital Humanities](../einleitung/filmwissenschaft.md#weitere-entwicklungen-in-der-digitalen-forschung-zur-filmgeschichtsschreibung) vorgestellt. In einer Special Issue des <a href="https://culturalanalytics.org/issue/10778" class="external-link" target="_blank">Journal of Cultural Analytics</a>, das sich mit dem Themenbereich _Digital Film Historiography: Challenges of/and Interdisciplinarity_ beschäftigt und von Malte Hagener und Diana Roig-Sanz herausgegeben wurde, sind Beiträge versammelt, die sich mit digitaler Filmgeschichtsschreibung aus verschiedenen Perspektiven beschäftigen. Die zugehörigen Datensätze wurden in einem Repositorium veröffentlicht. Die vorgestellten Forschungsergebnisse können also mit den Datensätzen nachvollzogen und diese ggf. in anderen, weiterführenden Forschungsprojekten verwendet werden.

```{figure} ../assets/publikation/Repositorium_Journal_of_Cultural_Analytics.png
---
align: left
width: 100%
name: repo_journal
alt: Screenshot einer Liste mit Datensätzen zu Beiträgen im Journal of Cultural Analytics
---
Screenshot einer <a href="https://dataverse.harvard.edu/dataverse/culturalanalytics?q=&fq2=publicationDate%3A%222024%22&fq0=subtreePaths%3A%22%2F2839294%22&fq1=dvObjectType%3A%28dataverses+OR+datasets%29&types=dataverses%3Adatasets&sort=dateSort&order=" class="external-link" target="_blank">Liste mit Datensätzen</a> zu Beiträgen im Journal of Cultural Analytics 
```

## Daten in einem Repositorium
Datensätze können in einem Repositorium nicht nur im Kontext eines veröffentlichten Artikels abgelegt werden, sondern auch als eigenständige Datenveröffentlichung. In beiden Fällen sollten bestimmte Kriterien erfüllt werden. Neben dem Titel sollten die Autor:innen des Datensatzes, das Veröffentlichungsdatum und die Version ersichtlich sein – Datensätze können auch weiterentwickelt und aktualisierte Versionen zur Verfügung gestellt werden. Wichtig ist ein kompakter Beschreibungstext, aus dem hervorgeht, in welchem Kontext die Daten entstanden sind, wie sie erhoben wurden und was in einzelnen Dateien des Datensatzes enthalten ist. Deutlich erkennbar sollte sein, unter welcher Lizenz der Datensatz veröffentlicht wurde (z.B. <a href="https://creativecommons.org/licenses/by/4.0/" class="external-link" target="_blank">CC BY 4.0</a>), unter welchen Bedingungen er also weiter genutzt werden kann. Oft werden auch Stichworte und Themen angegeben, was der einfacheren Auffindbarkeit dient.

Es folgen die einzelnen Dateien des Datensatzes, versehen mit entsprechenden beschreibenden Metadaten. Für diese Dateien sollten bevorzugt Dateiformate verwendet werden, die programmunabhängig sind, wie z.B. Textdateien im csv-, tsv- oder xml-Format, wie sie im Abschnitt zu [Datenformaten](../bereinigung/openRefine/2_import.md#datenformate) im Kapitel zur Datenbereinigung beschrieben wurden. Diese haben den Vorteil, dass sie in zahlreiche digitale Tools zur Weiterverarbeitung und Auswertung der Daten eingelesen werden können. Oft werden aber auch Excel-Tabellen dort abgelegt. Es bietet sich an, Dateien hinzuzufügen, die den Inhalt und die Struktur der in den Dateien enthaltenen Daten beschreiben (z.B. in Form eines "Codebooks", das einzelne Variablen und Spaltennamen aufschlüsselt). Für eine genauere Einordnung des gesamten Datensatzes erweist sich eine readme-Datei als nützlich, also eine einfache Textdatei mit den zentralen Informationen zum Datensatz, die zusammen mit den Daten heruntergeladen wird.

Die einzelnen Dateien eines Datensatzes können meist entweder einzeln angewählt und heruntergeladen werden oder als gesamter Datensatz mit allen Dateien.

```{figure} ../assets/publikation/Repositorium_Eintrag_National_Film_History.png
---
align: left
width: 100%
name: repo_eintrag
alt: Screenshot eines Eintrags zu einem Datensatz eines Beitrags im Journal of Cultural Analytics
---
Screenshot eines <a href="https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/C80HD1" class="external-link" target="_blank">Eintrags zu einem Beitrag</a> im Journal of Cultural Analytics 
```

## Data Papers
Data Papers unterscheiden sich von Artikeln mit publizierten Daten dadurch, dass ihr Fokus nicht auf Forschungsergebnissen liegt, sondern auf der Datenaufbereitung, der genauen Beschreibung des veröffentlichten Datensatzes und dessen Potenziale für die Forschung. Data Papers werden in speziellen Journals oder in Rubriken von fachspezifischen Journals veröffentlicht. Für die Film- und Medienwissenschaft wurde z.B. eine Rubrik für Data Papers im <a href="https://necsus-ejms.org/" class="external-link" target="_blank">NECSUS_European Journal of Media Studies</a> eingerichtet.


```{figure} ../assets/publikation/NECSUS_Data_Papers_markiert.png
---
align: left
width: 100%
name: NECSUS
alt: Screenshot der der Rubrik "Data Papers" im NECSUS_European Journal of Media Studies
---
Screenshot der der Rubrik <a href="https://necsus-ejms.org/portfolio/spring-2023_ports/#toggle-id-7" class="external-link" target="_blank">"Data Papers"</a> im NECSUS_European Journal of Media Studies
```

Der Aufbau eines Data Papers kann variieren und wird häufig vom publizierenden Journal vorgegeben. Meist fokussiert sich ein Data Paper zunächst auf die Beschreibung des Datensatzes und dessen Struktur: Welche Dateien sind enthalten und wie ist die Beziehung zwischen den Dateien? Handelt es sich z.B. um einen Auszug aus einer Datenbank mit verschiedenen Tabellen, die untereinander mit eindeutigen Identifikatoren in Beziehung gesetzt werden können?

Daran anschließend wird das Datenmodell beschrieben. Bei komplexen Datenmodellen werden auch grafische Darstellungen der Modelle eingefügt. Darauf aufbauend werden die Datenerhebung und die Datenquellen dargelegt. Wer hat die Daten in welchem Kontext erhoben? Wurden die Daten automatisch oder manuell erfasst? Welche Quellen wurden verwendet, z.B. Angaben aus Zeitungen, Handelsregistern, Förderinstitutionen oder Festivals-Archiven? Und falls mehrere Quellen ausgewertet wurden: Wie wurden diese zusammengeführt? Wie sah der Prozess der Standardisierung aus?

Im Diskussionsteil wird das Datenmodell ausführlich reflektiert (z.B. ob die Variablen und Feldnamen sinnvoll gewählt sind oder an welchen Stellen Lücken im Datensatz erkennbar sind), ebenso wie die Datenquellen (z.B. die Methoden der Datenerhebung, wo sind die Grenzen der Quellen, was kann mit ihnen erforscht werden). Auch die Möglichkeiten der Nachnutzung und der Erweiterung des Datensatzes sollten diskutiert werden.

Auf die Diskussion folgt eine Zusammenfassung der Ergebnisse des Papers, die auch einen Ausblick auf weitere Einsatzmöglichkeiten des Datensatzes enthalten kann. Ein Data Paper sollte einen Datensatz verständlich erschließen, ihn durchdringen und kritisch reflektieren und damit eine optimale Grundlage für eine mögliche Nachnutzung legen.







## Literatur
```{bibliography}
:filter: docname in docnames
:labelprefix: G
:keyprefix: g-
```
