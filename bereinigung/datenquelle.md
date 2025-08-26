# Datenquelle
Ausgangspunkt für die Fallstudie sind existierende Daten in Form eines Auszugs aus der Datenbank des Bibliothekskatalogs (OPAC) der Filmuniversität Babelsberg. In diesem Auszug sind **alle im Katalog vorhandenen Angaben zu studentischen Filmen aus den Jahren 1985 bis 1999** enthalten. Johanna Drucker weist darauf hin, dass bei der Arbeit mit existierenden Daten danach gefragt werden sollte, wie vollständig diese Daten sind und wer diese wie erstellt hat. {cite}`d-Drucker_2021` Solche Datensätze enthalten nach Drucker selten Angaben darüber, wie sie entstanden sind – weder in einer möglichen zusätzlichen Dokumentation noch in den Metadaten. Daher sollte das den Daten zugrunde liegende Modell analysiert werden. Zielführende Fragen sind für einen Rückschluss auf das Modell z.B.: Welche Feldnamen wurden für die Charakterisierung einzelner Informationen verwendet? Welche Systeme zur Kategorisierung sind erkennbar? Wo fehlen Angaben?

## Analyse des Datenmodells

Sarah-Mai Dang bringt nochmals auf den Punkt, was mit Datenmodellierung gemeint ist: 

> „Unter Datenmodellierung ist, allgemein gesprochen, ein formales Verfahren zu verstehen, das darauf abzielt, Daten für Menschen und/oder Computer verständlich, also les- und nutzbar aufzubereiten.“ {cite}`d-Dang_2022`

Wie diese Aufarbeitung geschieht und welche Vorannahmen, technischen Voraussetzungen oder pragmatische Vorgehensweisen darin einfließen und diese prägen, gilt es zu verstehen und bei der Arbeit mit dem Datensatz zu beachten. In der bereits im Abschnitt zu Metadaten angesprochenen Studie zu heterogenen Metadaten am Beispiel von Lotte Reiniger kommen Pauline Junginger und Sarah-Mai Dang daher in ihrem Fazit zu dem Schluss:
> „Unsere Analyse macht deutlich, dass für die korrekte Einordnung der Daten nicht nur filmhistorisches Wissen, sondern auch Kenntnisse über die jeweiligen Datenbankstrukturen und Wissenspraktiken notwendig sind.“ {cite}`d-Dang_Junginger_2024`

Die Wissenspraktiken an dieser Stelle näher zu beleuchten, würde zu weit führen. Wir betrachten jedoch kurz die Datenbankstrukturen.

Als ein System, das für Bibliotheken entwickelt wurde, ist der Online-Katalog und dessen Datenbank für die Erfassung von Medien in Schriftform wie Bücher oder Zeitschriften konzipiert worden. Andere Medienarten wie DVDs oder, wie im Fall des Filmarchivs der Filmuniversität, Filme wurden in dieses System integriert bzw. es wurde für diese modifiziert. Es ist also nicht genuin für die Verarbeitung und Speicherung filmarchivarischer Metadaten vorgesehen.

## Metadaten für die Identifikation von Filmen
Um die Identifikation von Filmen zu erleichtern und Metadaten zu filmischen Werken möglichst einheitlich zu erheben, wurde eine internationale Norm in Form eines sehr komplexen Datenmodells erarbeitet, die Norm <a href="http://filmstandards.org/fsc/index.php/EN_15907" class="external-link" target="_blank">EN 15907</a>. Mit diesem Modell können nicht nur einzelne filmische Werke, sondern auch verschiedene Fassungen oder Manifestationen wie unterschiedliche Filmkopien, DVD-Ausgaben o.ä. und Beziehungen zu anderen Werken erfasst werden. Durch die einheitliche Norm soll der Austausch dieser sehr detaillierten Daten zu Filmen erleichtert werden, z.B. zwischen Filmarchiven. Gleichzeitig bringt die Komplexität des Datenmodells einen hohen Aufwand bei der Eingabe der Metadaten mit sich. Ein kompakter Überblick zu diesem Themenfeld findet sich in Margret Schilds Beitrag zu Metadaten-Management in Filmarchiven. {cite}`d-Schild_2017`

Schild geht auch darauf ein, dass zusätzlich zu der Norm EN 15907 noch die Norm <a href="http://filmstandards.org/fsc/index.php/EN_15744" class="external-link" target="_blank">EN 15744</a> eingeführt wurde, in der Minimalstandards zur eindeutigen Identifikation von Filmwerken definiert werden. Sie legt ein Datenset mit 15 Elementen fest, die z.B. den Titel, die Besetzung, an der Produktion beteiligte Personen, das Format, die Länge des Materials in Metern, die Dauer und das Genre beinhalten. An diesem Minimalstandard orientiert sich auch die Erfassung von Metadaten zu den Filmen im Filmarchiv der Filmuniversität im OPAC.

## Metadaten im OPAC der Filmuniversität
Um die Struktur der Daten im OPAC und den Ablauf der Erfassung dieser Daten zu einem Film im Archiv der Filmuniversität besser zu verstehen, haben wir für die Fallstudie ein Gespräch mit der zuständigen Person in der Bibliothek geführt. Die folgenden Ausführungen beziehen sich u.a. auf dieses Gespräch. An dieser Stelle können nicht alle Felder, in denen Metadaten zu den Filmen aufgeführt sind, besprochen werden. Der Fokus liegt v.a. auf denen, die häufig auftreten und die für die Bearbeitung der im [letzten Kapitel](/recherche/operationalisierung.md) erarbeiteten (Teil)fragestellungen potenziell relevant sind. Es soll ein Verständnis vermittelt werden, wie diese Metadaten in den OPAC und damit in unseren Datensatz aufgenommen wurden. Dadurch wollen wir eine Grundlage für deren kritische Auswertung legen.

### Erfassung der Daten
Bei den studentischen Filmen im Archiv handelt es sich zum großen Teil um Titel, die nur dort und in keinen anderen Archiv vorhanden sind. Es können also für die Katalogisierung meist keine Informationen aus externen Quellen übernommen werden, wie z.B. aus Datenbanken im Internet oder DVD-Covers. Die Daten für die Einträge in den OPAC werden durch eine Sichtung des Films selbst abgenommen. Während der Sichtung werden diese in ein Formblatt eingetragen und anschließend in den OPAC übertragen. Neben den "verantwortlichen Personen", die dem jeweiligen Gewerk – also filmischen Arbeitsbereich – zugeordnet sind, werden Informationen wie Titel, Regie, Produktionsjahr oder Format in diesem Formblatt erfasst. Wichtig ist hierbei, dass die Reihenfolge der Gewerke nicht der Reihenfolge im Abspann des Films entspricht, sondern einer bibliotheksintern festgelegten einheitlichen Abfolge für alle Filme. Diese erscheint später auch in der Anzeige des OPACs: Regie, Kamera, Produktion, Drehbuch, Dramaturgie, Montage / Schnitt, Ton (Sound), Mischung, Musik, Szenografie, Herstellungsleitung, Darsteller, thematisierte Person, fachliche Beratung. Die Prozesse bei der Eingabe der Daten beeinflussen hier die spezifische Art ihrer Anordnung in der Ausgabe im OPAC und in unserem Datensatz.

Im Folgenden werden die Eingabefelder in der Reihenfolge besprochen, wie sie in der Anzeige der Weboberfläche des OPACs der Filmuniversität auftreten. Für eine bessere Übersichtlichkeit haben wir die Felder in Gruppen zusammengefasst.

```{admonition} Achtung
:class: caution
Bei der Arbeit an unserer Fallstudie haben wir festgestellt, dass der Datensatz zu unserem Korpus studentischer Filme aus dem Filmarchiv personenbezogene Daten enthält. Für diese ist leider nicht gesichert, dass eine Einwilligung der Personen zur Veröffentlichung der Angaben vorliegt. Wir können somit diesen Datensatz nicht publizieren. Im Kapitel zu [Problemfeldern](/publikation/problemfelder) bei der Datenpublikation gehen wir noch genauer auf dieses Thema ein. Für die Veranschaulichung der weiteren Arbeitsschritte verwenden wir einen synthetischen Datensatz, der sich an den Inhalten des Originaldatensatzes orientiert und der im Kapitel zur [Datenbereinigung](/bereinigung/openRefine/0_datenbereinigung) besprochen wird. Für ein besseres Verständnis der Struktur des OPAC-Datensatzes bietet es sich dennoch an, im Folgenden die einzelnen Komponenten genauer zu betrachten. 
```

### Sonstige Person
Die an einer Produktion beteiligten Personen werden nacheinander in das Feld "sonstige Person" aufgenommen. Die Reihung der Gewerke folgt der oben aufgeführten Abfolge. Im Eingabeformular des OPAC können bis zu 25 Personen je Film erfasst werden. Jede Person wird für jeden Film nur einmal erfasst, ist sie an mehreren Gewerken beteiligt, sind diese nacheinander in der eckigen Klammer aufgeführt, die auf den Namen folgt. ({numref}`opac_person`)

```{figure} ../assets/bereinigung/quelle/OPAC_Person.png
---
align: left
width: 100%
name: opac_person
alt: Darstellung des Ausschnitts einer Vollanzeige eines Einzeltitels im Katalog der Bibliothek der Filmuniversität. Einzelne Felder sind mit einer roten Umrandung hervorgehoben.
---
Feld "sonstige Person" in der Vollansicht eines Eintrags des Bibliothekskatalogs
```

### Titel, Zusatz, Personenangaben
In einem weiteren Feld wird der Titel des Films genannt. Im Feld Zusatz sind die Projektarten der studentischen Filme aufgeführt, z.B. "Übung", "Diplomfilm", "Hauptprüfungsfilm" oder "F1", "F2", "F3" – was ebenfalls spezifische Filmübungen aus dem Lehrplan der Hochschule sind. Gegebenenfalls werden die Übungen zusätzlich den Studiengängen zugeordnet, die hauptverantwortlich oder beteiligt waren. ({numref}`opac_titel`) Bei "Personenangaben" werden Einträge aus den Feldern "sonstige Personen" wiederholt, in der Regel die erste Zeile in Form der Regie und des entsprechenden Namens, gelegentlich finden sich mehrere Namensnennungen und Gewerke im selben Feld.

```{figure} ../assets/bereinigung/quelle/OPAC_Titel_Zusatz_Personenangaben.png
---
align: left
width: 100%
name: opac_titel
alt: Darstellung des Ausschnitts einer Vollanzeige eines Einzeltitels im Katalog der Bibliothek der Filmuniversität. Einzelne Felder sind mit einer roten Umrandung hervorgehoben.
---
Felder "Titel", "Zusatz" und "Personenangaben" in der Vollansicht eines Eintrags des Bibliothekskatalogs
```

### Umfang/Format, Allgemeine Anmerkung
Das Feld "Umfang/Format" enthält Informationen zum Format des Films (16mm, 35mm, Betacam SP etc.), zur Länge in Metern, zur Dauer in Minuten, zu den Bildern pro Sekunde, ob der Film in Farbe oder Schwarzweiß vorliegt und zum Tonformat. Diese Angaben wurden in einer Zeile untergebracht, da sie für die Vorführung des Films relevant sind und schnell an einem Ort erkennbar sein sollten. Für eine weitere Auswertung des Datensatzes sind dies Informationen, die einzeln zur Verfügung stehen müssen und daher aus einem Feld in mehrere aufgeteilt werden sollen.

"Allgemeine Anmerkung" enthält die Kennzeichnung, dass es sich um einen Film im Filmarchiv handelt. Zusätzlich werden Angaben zum Copyright erfasst, in der gleichen Reihenfolge wie im Abspann aufgeführt. ({numref}`opac_umfang`)

```{figure} ../assets/bereinigung/quelle/OPAC_Umfang_Format_Allg_Angaben.jpg
---
align: left
width: 100%
name: opac_umfang
alt: Darstellung des Ausschnitts einer Vollanzeige eines Einzeltitels im Katalog der Bibliothek der Filmuniversität. Einzelne Felder sind mit einer roten Umrandung hervorgehoben.
---
Felder "Umfang/Format" und "Allgemeine Anmerkung" in der Vollansicht eines Eintrags des Bibliothekskatalogs
```
### Schlagwort, Stichwörter, Zusammenfassung
Die Einträge der Schlagworte im entsprechenden Feld folgen der <a href="https://www.filmuniversitaet.de/fileadmin/user_upload/pdfs/bibliothek/schlagsys.pdf" class="external-link" target="_blank">Systematik</a> der Universitätsbibliothek. Es handelt sich um ein kontrolliertes Vokabular, da nur Begriffe vergeben werden können, die in der Liste aufgeführt sind. Anhand des Schlagworts wird auch die Gattung des Films charakterisiert – also Dokumentarfilm, Spielfilm oder Animationsfilm –, falls die Gattung bei der Eingabe erfasst wurde. Später sollen die Angaben zur Gattung ausgewertet werden. Im Datensatz müssen diese also wiederum als eigene, getrennte Zellen vorhanden sein.

Im Gegensatz zum Schlagwort werden Stichwörter frei vergeben und folgen keinem festgelegten Vokabular. Durch Stichwörter werden der Inhalt, die Themen oder Motive eines Films charakterisiert. Aufgrund der freien Vergabe ist hier wieder der historische Kontext der Archivierung und die potenziell subjektive Bewertung zu berücksichtigen.

Das Feld Zusammenfassung enthält eine kurze Inhaltsangabe des Films, gelegentlich auch Ausschnitte aus Rezensionen. Diese Inhaltszusammenfassungen stammen aus verschiedenen Quellen: Teilweise wurden sie aus Texten der Öffentlichkeitsarbeit übernommen, teilweise aus Angaben der Produktionsabteilung. Wo keine Texte vorlagen, wurden diese auch von den Personen verfasst, die die Daten der Filme eingegeben haben. Im Feld sind bis zu drei einzelne Einträge mit Texten zum Inhalt möglich. ({numref}`opac_schlagwort`)

```{figure} ../assets/bereinigung/quelle/OPAC_Schlagwort_Stichwort_Zusammenfassung.png
---
align: left
width: 100%
name: opac_schlagwort
alt: Darstellung des Ausschnitts einer Vollanzeige eines Einzeltitels im Katalog der Bibliothek der Filmuniversität. Einzelne Felder sind mit einer roten Umrandung hervorgehoben.
---
Felder "Schlagwort", "Stichwörter" und "Zusammenfassung" in der Vollansicht eines Eintrags des Bibliothekskatalogs
```

### Fazit und weiteres Vorgehen
Die Analyse des Datenmodells und der Eigenschaften einzelner Felder verbesserte unseren Überblick über die Struktur der Daten im OPAC und damit auch über die Datenstruktur im uns vorliegenden Auszug aus der OPAC-Datenbank. Dabei wird nochmals die Problematik deutlich, dass Daten nicht einfach "gegeben", sondern immer "gemacht" sind. Welche Metadaten zu einem Film erfasst werden und welche nicht, welche Felder wie mit welchen Merkmalen befüllt werden, unterliegt Entscheidungen, die auch die weitere Auswertung der Daten beeinflussen. Dabei stellt sich immer wieder die Frage: Was kann auf dieser Grundlage wie und mit welcher Zuverlässigkeit für eine genauere Analyse des Korpus verwendet werden?

Die genauere Betrachtung des Datenmodells hat ebenfalls ergeben, dass die Daten im erhaltenen Auszug noch nicht in einer Form vorliegen, wie sie für eine weitere Arbeit mit den Metadaten zu den Filmen notwendig ist. Sie müssen noch "bereinigt", also in eine gute und eindeutige Struktur gebracht werden. Im nächsten Schritt werden wir nun die Datenbereinigung angehen.


## Literatur
```{bibliography}
:filter: docname in docnames
:labelprefix: D
:keyprefix: d-
```
