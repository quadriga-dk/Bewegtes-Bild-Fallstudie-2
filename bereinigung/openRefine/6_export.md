# Export des Datensatzes

Nach erfolgreicher Bereinigung soll der Datensatz natürlich auch exportiert werden um ihn auszuwerten. In *OpenRefine* stehen zahlreiche Exportformate mit einem Klick auf das *Export* Dropdown-Menü oben rechts im Hauptfenster zur Verfügung.

```{figure} ../../assets/bereinigung/openRefine/export/export_1.png
---
align: center
width: 50%
name: export_1
alt: Anzeige der verfügbaren Exportformate
---
Anzeige der verfügbaren Exportformate
```
Auf den Export eines *OpenRefine*-Projekts wurde bereits im Kapitel zur [Sichtung des Datensatzes](./3_sichtung.md#export-eines-openrefine-projekts) eingegangen. Informationen zu den weiteren Exportformaten finden Sie auf dieser Seite der <a href="https://openrefine.org/docs/manual/exporting#export-data" class="external-link" target="_blank">*OpenRefine* Dokumentation</a>.

Im Folgenden soll auf das Vorgehen beim Export des Datensatzes als Textdatei eingegangen werden – also genau jenes Format, in dem der Übungsdatensatz auch zu Beginn vorlag. Textdateien sind programm-unspezifisch und das Standardformat bei der Veröffentlichung von Datensätzen.

Wird im oben gezeigten Menü der Export als **CSV**, also als Textdatei mit *Comma-separated values*, ausgewählt, ergänzt *OpenRefine* automatisch Anführungszeichen am Anfang und am Ende von Einträgen, die ebenfalls ein Komma enthalten. Ggf. werden diese aber von anderen Programmen nicht korrekt interpretiert. Daher ist der Export als **TSV** (*Tab-seperated value*) oder mittels einem ungewöhnlichem Sonderzeichen wie dem *Pipe* `|` als Trennungszeichen die bessere Option. Wählen Sie für letzteres den Menüpunkt *Custom tabular...* aus.

```{figure} ../../assets/bereinigung/openRefine/export/export_2.png
---
align: center
width: 50%
name: export_2
alt: Der Menüpunkt custom tabular
---
Der Menüpunkt *custom tabular*
```

Wechseln Sie in dem sich nun öffnenden Fenster in den Reiter *Download*.
Wählen Sie als *Line-based text format* die Option *custom separator* aus und entscheiden Sie sich im Textfeld daneben für ein Trennungszeichen Ihrer Wahl. Falls Sie das *Pipe*-Zeichen `|` verwenden möchten: Unter Windows wird dieser senkrechte Strich mit der Tastenkombination `Alt Gr`+`<` erzeugt, in macOS mit `option`+`7`.

```{figure} ../../assets/bereinigung/openRefine/export/export_3.png
---
align: center
width: 100%
name: export_3
alt: Das Menücustom tabular
---
Das Menü *custom tabular*
```

Über den Button *Preview* können Sie eine Vorschau des Datensatzes ansehen, die sich in einem neuen Fenster öffnet. Sind sie zufrieden, kann der bereinigte Datensatz mit einem Klick auf den *Download* Button heruntergeladen und abgespeichert werden.

Damit ist die Bereinigung des Datensatzes erfolgreich abgeschlossen!

Sie können Ihre Ergebnisse mit [dieser Musterlösung des *OpenRefine*-Projekts](../../assets/daten/Synthetischer_Datensatz_Uebung_OER_final.tar) und [dieser TSV-Exportdatei](../../assets/daten/Synthetischer_Datensatz_Uebung_OER_final.tsv) (rechte Maustaste und *Ziel speichern unter* auswählen) vergleichen.

