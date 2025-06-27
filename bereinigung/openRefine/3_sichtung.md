# Sichtung des Datensatzes
## Layout OpenRefine

Als ersten Schritt in der Bereinigung eines Datensatzes lohnt es sich, diesen im Detail mit den Funktionen von *OpenRefine* zu sichten. So erhalten Sie eine genaue Vorstellung bezüglich des Inhalts jeder Spalte und möglicher Probleme und können diese anschließend zielorientiert angehen. 

Nachdem die Importeinstellungen vorgenommen wurden, kann das Projekt über den Button *Create Project* erstellt werden:

```{figure} ../../assets/bereinigung/openRefine/sichtung/import_final.png
---
align: left
width: 100%
name: create_project_button
alt: Create Project
---
*Create Project*
```
Nun öffnet sich das Hauptfenster von *OpenRefine*, in dem Sie während der Bereinigung eines Datensatzes die meiste Zeit verbringen werden. 

```{figure} ../../assets/bereinigung/openRefine/sichtung/main_window.png
---
align: left
width: 100%
name: main_window
alt: Hauptfenster
---
Hauptfenster
```
Ihnen mag auffallen, dass nicht alle Zeilen gleichzeitig angezeigt werden. Die Anzeige sehr großer Datensätze kann *OpenRefine* deutlich verlangsamen, allerdings sollte das beim Übungsdatensatz nicht als Problem auftreten. Mittels dieser Menü-Elemente kann die maximale Anzahl an Zeilen festgelegt und zwischen ihnen navigiert werden:

```{figure} ../../assets/bereinigung/openRefine/sichtung/row_navigation.png
---
align: left
width: 100%
name: row_navigation
alt: Menü-Elemente zur Zeilen-Navigation
---
Menü-Elemente zur Zeilen-Navigation
```
````{margin} 
```{admonition} Hinweis
:class: hinweis
Datensätze können im *Row* und *Record* Format dargestellt werden. Die meisten Datensätze liegen im Row-Format vor, wie auch der Übungsdatensatz. Im Record-Format  können mehrere Zeilen zu einem Tabellensatz, einem *Record*, zusammengefasst werden. In der *OpenRefine* Dokumentation finden sie mehr Informationen zum Unterschied der Darstellung in <a href="https://openrefine.org/docs/manual/exploring#rows-vs-records" class="external-link" target="_blank">Rows und Records</a> und zur Umwandlung von <a href="https://openrefine.org/docs/manual/cellediting#fill-down-and-blank-down" class="external-link" target="_blank">Rows in Records</a>.
```
````
Innerhalb der Spalte *All* werden die Zeilen nummeriert und können für ein besseres Auffinden mit einer Flagge oder einem Stern markiert werden. Weder diese Markierungen noch die Nummerierung sind Teil das Datensatzes und werden beim Export des bearbeiteten Datensatzes nicht mit eingeschlossen. 

### Export eines OpenRefine Projekts
Während Ihrer Arbeit an dem Datensatz möchten Sie ggf. einen Zwischenschritt des *OpenRefine*-Projekts speichern.

```{admonition} Achtung
:class: caution
Denken Sie daran, regelmäßig Zwischenstände Ihres Projekts als eigene *OpenRefine*-Projektdateien abzuspeichern. Diese sollten sie so benennen, dass der Arbeitsstand aus dem Dateinamen ersichtlich ist (z.B. durch Einbindung des Bearbeitungsdatums, einer Versionsnummer, eines Kürzels der bearbeitenden Person etc.).

In *OpenRefine* können zwar Bearbeitungsschritte relativ einfach rückgängig gemacht werden, dennoch kann es ggf. nützlich sein, auf eine älteren Version der Datenbereinigung zurückgreifen zu können. Insbesondere vor größeren Bearbeitungsschritten wie z.B. dem Löschen ganzer Spalten oder Zeilen ist das Speichern einer Zwischenversion des Projekts sinnvoll.
```

 Klicken Sie dazu auf das *Export* Dropdown-Menü in der oberen rechten Ecke der Benutzeroberfläche und wählen Sie den ersten Punkt *OpenRefine project archive to file*:

```{figure} ../../assets/bereinigung/openRefine/sichtung/export_tar.png
---
align: left
width: 50%
name: export_tar
alt: Projekt-Export
---
Export eines *OpenRefine* Projekts
```
Wählen Sie einen Speicherort und einen Dateinamen aus. Es empfiehlt sich für die Benennung der Export-Datei den vorgeschlagenen aktuellen Namen des Projekts beizubehalten und falls notwendig durch weitere Informationen zu ergänzen. Das Projekt wird im *TAR* Format gespeichert. Anschließend kehren Sie durch einen Klick auf den *Open* Button zum Startmenü von *OpenRefine* zurück. Hier können Sie das Projekt vom gewählten Speicherort aus re-importieren:

```{figure} ../../assets/bereinigung/openRefine/sichtung/reimport_1.png
---
align: left
width: 100%
name: reimport
alt: Re-Import eines Projekts
---
Re-Import eines Projekts
```

Im sich nun wieder öffnenden Hauptfenster benennen Sie nun mit einem Klick auf den aktuellen Namen das Projekt um. Geben Sie hierfür einen neuen oder modifizierten Projektnamen ein, z.B. mit angepasster Datumsangabe:

```{figure} ../../assets/bereinigung/openRefine/sichtung/reimport_2.png
---
align: left
width: 100%
name: reimport_2
alt: Umbenennung eines Projekts
---
Umbenennung eines Projekts
```

## Sichtung mittels Facets
Zurück zum Datensatz selbst. In einem ersten Schritt ist es sinnvoll, den Inhalt jeder Spalte des Datensatzes zu überprüfen. 

### Text Facets
Zu diesem Zweck kann ein sogenanntes **Text Facet** verwendet werden, um die Inhalte einer Spalte gebündelt auf der linken Seite des Hauptfensters anzuzeigen. Sie erstellen ein *Text Facet*, indem sie das Dropdown-Menü einer Spalte öffnen, dort *Facet* und anschließend *Text Facet* auswählen:

```{figure} ../../assets/bereinigung/openRefine/sichtung/textfacet_1.png
---
align: center
width: 50%
name: textfacet_1
alt: Erstellung eines Text Facet
---
Erstellung eines *Text Facet*
```
Auf der linken Seite des Hauptfenster erscheint das erstellte *Text Facet*:

```{figure} ../../assets/bereinigung/openRefine/sichtung/textfacet_titel.png
---
align: center
width: 50%
name: textfacet_title
alt: Ein *Text Facet* für die Spalte *Titel*
---
Ein *Text Facet* für die Spalte *Titel*
```

Am unteren Rand kann das Fenster verlängert werden. 
Im Falle der Spalte *Titel* werden *1176 choices* angezeigt, also genauso viele Einträge wie Zeilen. Jede Zeile enthält somit die Informationen für einen Titel.

 Ein *Text Facet* für die Spalte *Jahr* zeigt weniger *choices* an:

```{figure} ../../assets/bereinigung/openRefine/sichtung/textfacet_jahr.png
---
align: center
width: 50%
name: textfacet_jahr
alt: Ein *Text Facet* für die Spalte *Jahr*
---
Ein *Text Facet* für die Spalte *Jahr*
```
Da sich mehrere Filme dasselbe Produktionsjahr teilen, gibt es in dieser Spalte deutlich weniger unterschiedliche Einträge. Standardmäßig ist das *Text Facet* alphabetisch sortiert. Diese Sortierung lässt sich auch auf *count* umstellen, also auf die Häufung pro Eintrag:

```{figure} ../../assets/bereinigung/openRefine/sichtung/textfacet_jahr_count.png
---
align: center
width: 50%
name: textfacet_jahr_count
alt: Die Sortierung nach *count*
---
Die Sortierung nach *count*
```

Neben jedem Eintrag wird in grau dessen Häufung angezeigt. Mit Klick auf einen der Einträge, etwa das häufigste Jahr *1989*, wird der Datensatz gefiltert, sodass nur noch Filme aus diesem Jahr angezeigt und bearbeitet werden. 

```{figure} ../../assets/bereinigung/openRefine/sichtung/textfacet_filter.png
---
align: left
width: 100%
name: textfacet_filter
alt: Filterung des Datensatzes nach dem Jahr 1989
---
Filterung des Datensatzes nach dem Jahr *1989*
```
Mit einem Klick auf den Button *invert* kann diese Auswahl auch umgekehrt werden, sodass nur noch Filme ausgewählt sind, die **nicht** dem Jahr 1989 zugeordnet wurden. 

```{figure} ../../assets/bereinigung/openRefine/sichtung/textfacet_filter_invert.png
---
align: center
width: 50%
name: textfacet_filter_inverse
alt: Invertierung des Text Filter
---
Invertierung des *Text Filter*
```
Ein Klick auf den Button *reset* hebt die Filterung auf. 

Bei der Erkundung eines Datensatzes haben *Text Facets* damit v.a. zwei Funktionen:
- Sichtung des Inhalts von Spalten eines Datensatzes und von dort auftretenden Werthäufungen
- Filterung des Datensatzes nach einzelnen Spalteninhalten, um nur eine Auswahl des Datensatzes zu betrachten und zu bearbeiten

### Numeric Facet
````{margin} 
```{admonition} Hinweis
:class: hinweis
Mehr zu den übrigen *Facets* finden Sie auf
<a href="https://openrefine.org/docs/manual/facets" class="external-link" target="_blank">dieser Seite der *OpenRefine* Dokumentation</a>.
```
````

Über das *Facet* Dropdown-Menü können auch andere Arten von *Facets* ausgewählt werden. 
Das *Numeric Facet* ist praktisch, um den Datensatz hinsichtlich eines Zahlenraums zu filtern, etwa nach dem Zeitraum der Jahre *1989* bis *1994*:

```{figure} ../../assets/bereinigung/openRefine/sichtung/numericfacet.png
---
align: center
width: 50%
name: numeric_facet
alt: Numeric Facet zur Auswahl des Zeitraums 1989 bis 1994
---
*Numeric Facet* zur Auswahl des Zeitraums *1989* bis *1994*
```
Anders als das *Text Facet*, das auf Text und Zahlen angewandt werden kann, funktioniert das *Numeric Facet* nur für Zahlen. 

### Text filter
Mit einem *Text Filter* können Sie Spalten nach einem Text durchsuchen und den Datensatz nach den Ergebnissen filtern. Der *Text Filter* findet sich im Dropdown-Menü der Spalten unter den *Facets*:

```{figure} ../../assets/bereinigung/openRefine/sichtung/textfilter_1.png
---
align: center
width: 25%
name: textfilter_1
alt: Auswahl des Text Filter
---
Auswahl des *Text Filter*
```
Nun kann der Datensatz mittels eines Textfelds durchsucht werden. Im folgenden Beispiel wird der *Text Filter* auf die Spalte *verantw.__Person* angewandt und Filme von *Olga Mielke* ausgewählt. 

```{figure} ../../assets/bereinigung/openRefine/sichtung/textfilter_2.png
---
align: center
width: 100%
name: textfilter_2
alt: Anwendung des Textfilter
---
Anwendung des *Text Filter*
```

Wie bei den *Facets* ist es möglich, den *Text Filter* zu invertieren, sodass nur noch Filme ohne *Olga Mielke* ausgewählt werden. 
Zudem gibt es innerhalb des *Text Filter* die zwei Optionen *case sensitive* und *regular expression*. In einer *case sensitive* Suche wird die Groß- bzw. Kleinschreibung des Suchbegriffs berücksichtigt, somit würde etwa ein Film von *olga mielke* nicht mehr ausgewählt werden. Zusätzlich können Sie auch nach Mustern innerhalb der Einträge mittels *regular expressions* oder *Regex* suchen. Im [Abschnitt zur Standardisierung der Titel](5.2_titel.md) wird der Umgang mit Regex genauer erklärt.