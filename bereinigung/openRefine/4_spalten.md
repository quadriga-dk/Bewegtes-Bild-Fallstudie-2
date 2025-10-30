# Bereinigung der Spalten

Durch die Sichtung des eingelesenen Datensatzes konnten Sie sich einen Überblick über den Inhalt der einzelnen Zeilen und Spalten verschaffen. Nicht alle Inhalte werden den Anforderungen eines konsistenten und strukturierten Datensatzes entsprechen. Bei solchen Einträgen setzt die Bereinigung eines Datensatzes an.

```{admonition} Achtung
:class: caution
Gehen Sie bei der Bereinigung eines Datensatzes mit Vorsicht und Bedacht vor. Spalteninhalte, die zunächst als für die Beantwortung der Forschungsfrage nicht notwendig erschienen und gelöscht wurden, können sich später im Forschungsprozess als relevant und nützlich erweisen.

Auch die Vereinheitlichung von Schreibweisen (z.B. von Institutionen, Berufsbezeichnungen etc.) kann sich als problematisch erweisen, etwa wenn sich Schreibweisen oder Bezeichnungen im Laufe der Zeit verändert haben und sich dies später als relevant für die Forschungsfrage herausstellt.

Schritte in der Datenbereinigung sind immer mit Interpretationsprozessen verbunden, die gut überlegt und reflektiert werden müssen. Denken Sie daher daran, regelmäßig Zwischenversionen Ihres OpenRefine-Projekts zu [exportieren und abzuspeichern](3_sichtung.md#export-eines-openrefine-projekts). 
```


## Löschen von Spalten

Ein häufiges Problem in unbereinigten Datensätzen sind Spalten, die etwa
- immer den selben Eintrag,
- keine oder wenige Einträge,
- oder Einträge aus Eingabefehlern

enthalten. Letzteres ist für die Spalte *Column 8* des Übungsdatensatzes der Fall.

In der Anwendung des *Text Facet* zeigt sich, dass diese Spalte nur zwei Einträge aufweist, die für Filme wenig Sinn ergeben:

````{margin} 
```{admonition} Hinweis
:class: hinweis
Die leeren Einträge werden innerhalb des *Facets* als *(blank)* angezeigt, auch wenn sie als *null* importiert wurden. 
```
````

```{figure} ../../assets/bereinigung/openRefine/spalten/textfacet_column8.png
---
align: center
width: 50%
name: textfacet_column8
alt: Text Facet der Spalte Column 8 des Übungsdatensatzes
---
*Text Facet* der Spalte *Column 8* des Übungsdatensatzes
```

Diese Spalte soll nun gelöscht werden. 
Öffnen Sie dazu das Dropdown-Menü der Spalte, wählen Sie *Edit column* aus und anschließend *Remove column*.

```{figure} ../../assets/bereinigung/openRefine/spalten/remove_column.png
---
align: center
width: 50%
name: remove_column
alt: Der Menüpunkt zur Löschung einer Spalte
---
Der Menüpunkt zur Löschung einer Spalte
```

Neben dem Spalten-Dropdown-Menü gibt es noch eine eigene Oberfläche zum Löschen und Umordnen von Spalten.
Dieses *Re-order / Remove columns* Menü wird über das Dropdown-Menü der Spalte *All* und den Reiter *Edit columns* geöffnet. 

```{figure} ../../assets/bereinigung/openRefine/spalten/reorder_columns_1.png
---
align: center
width: 50%
name: reorder_columns_1
alt: Die Schritte zum Öffnen des Menüs Re-oder / remove columns
---
Die Schritte zum Öffnen des Menüs *Re-oder / remove columns*
```
Hier können die Spalten per *Drag-and-Drop* umgeordnet und mittels der Ablage auf der rechten Seite gelöscht werden. 

```{figure} ../../assets/bereinigung/openRefine/spalten/reorder_columns_2.png
---
align: center
width: 75%
name: reorder_columns_2
alt: Das Menü Re-oder / Remove columns
---
Das Menü *Re-oder / Remove columns*
```

## Undo / Redo für reproduzierbare Arbeitsschritte

Ganz egal wie Sie die Spalte entfernen – Sie haben damit die erste Änderung am Datensatz vorgenommen.
Jede dieser Änderungen wird in einer Liste festgehalten und mit dem Projekt gespeichert, sodass sich auch zukünftig jeder Arbeitsschritt nachvollziehen lässt. Sie finden diese *Undo / Redo* Liste auf der linken Seite des Hauptfensters. 

```{figure} ../../assets/bereinigung/openRefine/spalten/undoRedo_1.png
---
align: center
width: 50%
name: undoRedo_1
alt: Die Undo / Redo Liste
---
Die *Undo / Redo* Liste
```

````{margin} 
```{admonition} Hinweis
:class: hinweis
*JSON* (JavaScript Object Notation) ist ein Datenformat, das dem einfachen Austausch von Daten zwischen verschiedenen Anwendungen dient. Es kann von vielen Programmiersprachen gelesen werden. Weitere Informationen zu JSON finden sich im <a href="https://de.wikipedia.org/wiki/JSON" class="external-link" target="_blank">Wikipedia-Artikel zu JSON</a> und auf der <a href="https://www.json.org/json-de.html" class="external-link" target="_blank">JSON-Projektseite</a>.
```
````

Mit Klick auf einen vorherigen Schritt in der Liste kann zu einem früheren Arbeitsstand zurückgekehrt werden. In OpenRefine ist damit kein Wiederholen von *STRG Z* und *STRG Y* nötig wie man es aus anderen Programmen kennt.

Außerdem lassen sich über das Feld *Extract* die aufgelisteten  Arbeitsschritte im *JSON* Format extrahieren:

```{figure} ../../assets/bereinigung/openRefine/spalten/undoRedo_extractButton.png
---
align: center
width: 50%
name: undoRedo_extractButton
alt: Der Button zum Extrahieren der Arbeitsschritte
---
Der Button zum Extrahieren der Arbeitsschritte
```

In dem sich öffnenden *Extract*-Fenstern können durch setzen eines Hakens einzelne Schritte ausgewählt werden, die Teil des *JSON*-Exports auf der rechten Seite werden sollen. Standardmäßig werden alle Schritte ausgewählt. Durch einen Klick auf *Export* können Sie die *JSON*-Datei herunterladen. Alternativ können Sie den Inhalt im rechten Feld auch in die Zwischenablage kopieren, um ihn nach einem späteren oder früheren *Undo/Redo* Schritt anzuwenden oder in ein anderes OpenRefine-Projekt einzufügen.

```{figure} ../../assets/bereinigung/openRefine/spalten/undoRedo_extract.png
---
align: center
width: 75%
name: undoRedo_export
alt: Das Fenster zum Extrahieren der Arbeitsschritte
---
Das Fenster zum Extrahieren der Arbeitsschritte
```

Der Button *Apply* öffnet das hierfür notwendige Menü. 

```{figure} ../../assets/bereinigung/openRefine/spalten/undoRedo_applyButton.png
---
align: center
width: 50%
name: undoRedo_apply
alt: Der Button zum Anwenden der Arbeitsschritte
---
Der Button zum Anwenden der Arbeitsschritte
```

Es kann entweder eine *JSON*-Datei über den *Choose File*-Button ausgewählt oder es können *JSON*-Inhalte aus der Zwischenablage in dem Textfeld abgelegt werden. Mit Klick auf den *Run operations*-Button werden die Änderungen angewendet.

```{figure} ../../assets/bereinigung/openRefine/spalten/undoRedo_apply.png
---
align: center
width: 75%
name: undoRedo_apply_run
alt: Das Fenster zur Anwendung von Arbeitsschritten 
---
Das Fenster zur Anwendung von Arbeitsschritten 
```

Neben der Übertragung von Arbeitsschritten auf andere Projekte ist diese Funktion besonders praktisch, um nachträglich an einem vorherigen Arbeitsstands des Projekts eine Änderung vorzunehmen und anschließend die später erfolgten Schritte erneut anzuwenden. 

## Übung Löschen einer zusätzlichen Spalte

`````{admonition} Übung
:class: exercise
Im Datensatz befindet sich eine weitere Spalte, die gelöscht werden kann. Finden Sie die Spalte mittels eines *Facets* und löschen Sie die Spalte. 


````{admonition}  Lösung
:class: solution, dropdown
Die Spalte *Bib._Nummer* enthält für jeden Film die Bibliotheksnummer der Bibliothek der Filmuniversität Babelsberg KONRAD WOLF. Zwar weichen einige Einträge ab, allerdings sind diese vermutlich durch Eingabefehler entstanden. 

```{figure} ../../assets/bereinigung/openRefine/sichtung/textfacet_bibNummer.png
---
align: center
width: 75%
name: textfacet_bibNummer
alt: Das Text Facet der Spalte Bib._Nummer
---
Das *Text Facet* der Spalte *Bib._Nummer*
```

Für die Beantwortung der Forschungsfrage sind die Einträge nicht relevant und die Spalte kann somit gelöscht werden. Wählen Sie hierfür im Dropdown-Menü *Edit column* und *Remove this column* aus (siehe {numref}`remove_column`).
````
`````

## Aufteilung von Spalten

Im [Kapitel zur Datenquelle](../datenquelle.md) wurde auf die Entstehung des Filmarchiv-Datensatzes als Teil eines Online-Bibliothekskatalogs eingegangen. Infolge der Eingaberoutinen bei der Erfassung der Daten zu den Archiv-Filmen und aufgrund technischer Gegebenheiten des Bibliothekssystems werden in einzelnen Eingabefeldern oft mehrere Informationen gleichzeitig aufgenommen. Dies hat zur Folge, dass auch in dem uns von der Bibliothek zur Verfügung gestellten Auszug aus der Datenbank häufig mehrere Einträge in einer Zelle aufgeführt sind und so in *OpenRefine* importiert wurden.

Grundsätzlich sollte jedoch im Sinne der Auswertung des Datensatzes mit digitalen Tools jede Zelle nur einen Eintrag enthalten. Die Einträge in einzelnen Zellen einer Spalte müssen also aufgeteilt und in zusätzlich erzeugte neue Spalten überführt werden.

Beim Übungsdatensatz tritt dieses Problem bei den drei Spalten *Verlag*, *Schlagwort* und *Stichwort* auf. *OpenRefine* bietet glücklicherweise eine einfache Lösung, da die einzelnen Einträge innerhalb der Zellen durch Trennzeichen wie in einer Liste voneinander abgegrenzt sind, etwa "*Kollektiv Bild und Ton Potsdam ; Atelier für Dokumentar-Film Babelsberg*" in der Spalte *Verlag*. Entlang des Semikolons lassen sich hier die Einträge voneinander unterscheiden. 

Für das Aufteilen der Mehrfach-Einträge in einer Spalte gehen Sie nun folgendermaßen vor. Öffnen Sie das Dropdown-Menü der aufzuteilenden Spalte und wähle sie im Reiter *Edit column* die erste Option *Split into several columns* aus. 

```{figure} ../../assets/bereinigung/openRefine/spalten/split_column_1.png
---
align: center
width: 75%
name: split_columns_1
alt: Das Öffnen des Menüs zum Aufteilen von Spalten
---
Das Öffnen des Menüs zum Aufteilen von Spalten
```

Im anschließenden Fenster kann das Trennzeichen ausgewählt werden. Für die Spalte *Verlag* ist ` ; ` das passende Trennzeichen, also das Semikolon mit einem vorangestellten und folgenden Leerzeichen. Zwar würde auch `;`, also nur das Semikolon ohne die Leerzeichen, zu einem ähnlichen Ergebnis führen, allerdings blieben dabei die Leerzeichen am Anfang bzw. am Ende der getrennten Einträge enthalten. Ggf. ist es sinnvoll die Option *Remove this column* zu deaktivieren, um die ursprüngliche Spalte nach der Aufteilung zu erhalten. Die Option *Guess cell type* wählt für jeden Eintrag den passenden Dateityp aus, so werden Zahlen etwa automatisch als numerischer Dateityp interpretiert (siehe [Numeric Facet](./3_sichtung.md#numeric-facet)).

```{figure} ../../assets/bereinigung/openRefine/spalten/split_column_2.png
---
align: center
width: 75%
name: split_columns_2
alt: Das Menü zum Aufteilen von Spalten
---
Das Menü zum Aufteilen von Spalten
```
Klicken Sie auf *OK*, nachdem sie die richtigen Einstellungen vorgenommen haben. Nun sollten zwei neue Spalten *Verlag 1* und *Verlag 2* erstellt werden. 

```{figure} ../../assets/bereinigung/openRefine/spalten/split_column_3.png
---
align: center
width: 50%
name: split_columns_3
alt: Die neuen Spalten mit den getrennten Einträgen
---
Die neuen Spalten mit den getrennten Einträgen
```

Die Anzahl an neuen Spalten ergibt sich aus der maximalen Anzahl an getrennten Einträgen. Es genügt also, wenn nur für einen einzigen Film zwei Verlage genannt sind, um zwei Spalten zu erzeugen.

## Umbenennung von Spalten
Leider verwendet *OpenRefine* in der automatischen Nummerierung der neuen Spalten ein Leerzeichen zwischen dem ursprünglichen Spaltennamen und der Zahl. Da Leerzeichen bei der Weiterverarbeitung des Datensatzes durch zusätzliche Programme, z.B. zur Visualisierung des Datensatzes, zu Fehlern führen können, sollten Sie die neuen Spalten umbenennen und die Leerzeichen durch einen Unterstrich ersetzen. Wählen Sie *Rename column* über das Dropdown-Menü der Spalte und den Reiter *Edit columns* aus.

```{figure} ../../assets/bereinigung/openRefine/spalten/rename.png
---
align: center
width: 75%
name: rename
alt: Das Öffnen des Menüs zum Umbenennen von Spalten
---
Das Öffnen des Menüs zum Umbenennen von Spalten
```
Sollten sich sich entschieden haben, die ursprüngliche Spalte *Verlag* nicht zu löschen, ist es sinnvoll diese ebenfalls umzubenennen, z.B. in *Verlag_OG*. So kann gekennzeichnet werden, dass es sich um die "originale Spalte" aus dem Datensatz handelt. Anschließend können Sie die Spalte mittels des oben beschriebenen *Re-order / Remove columns* Menüs ans Ende des Datensatzes verschieben (siehe {numref}`reorder_columns_1` und {numref}`reorder_columns_2`). 

## Übung

````{admonition} Übung
:class: exercise
Teilen Sie die Einträge in der Spalte *Schlagwort* auf mehrere Spalten auf. Jede Zelle der aufgeteilten Spalte soll nur noch einen Eintrag enthalten. Benennen Sie die neuen Spalten so um, dass sie bei der Verarbeitung mit weiteren Programmen keine Probleme verursachen.


```{admonition}  Lösungen
:class: solution, dropdown

Bestimmen Sie zunächst das Trennzeichen, das die einzelnen Einträge in den Spalten voneinander abgrenzt. Das Trennzeichen für die Spalte *Schlagwort* ist `;`.

Wählen Sie nun in der aufzuteilenden Spalte aus dem Dropdown-Menü im Reiter *Edit column* die erste Option *Split into several columns* aus (siehe {numref}`split_columns_1`). Geben Sie im Eingabefeld *Separator* bei der Spalte *Schlagwort* ` ; ` ein. Vergessen Sie dabei nicht die Leerzeichen vor und nach dem Trennzeichen, um die Leerzeichen der Ursprungsspalte nicht in die Einträge der neuen Spalte zu übernehmen (siehe {numref}`split_columns_2`).

Die neu entstandenen Spalten enthalten Leerzeichen in ihrer Benennung, die zu Problemen bei der Verarbeitung des Datensatzes in anderen Programmen führen können. Wählen Sie *Rename this column* über das Dropdown-Menü der umzubenennenden Spalte und dort den Reiter *Edit columns* aus und ersetzen Sie die Leerzeichen im Spaltennamen durch Unterstriche (siehe {numref}`rename`).

Vielleicht ist Ihnen bereits aufgefallen, dass sich die Spalte *Stichwort* nicht auf die selbe Weise aufteilen lässt, da sie neben dem Semikolon auch andere Trennzeichen enthält. Im nächsten Kapitel erfahren Sie, wie Sie auch diesem Problem begegnen können. 

```
````