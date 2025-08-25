# Visualisierungen zur Fallstudie
Für die vorliegende Fallstudie haben wir Visualisierungen erstellt, die die Bearbeitung der im Kapitel [Operationalisierung der Fragestellung](/recherche/operationalisierung) erarbeiteten Teilfragestellungen erleichtern und ermöglichen:

```{admonition} Teilfragestellungen
:class: keypoint

- Wie viele Filme sind zu welchen Zeitpunkten entstanden?
- Welchen Gattungen (Spielfilm, Dokumentarfilm, Animationsfilm) können diese Filme zugeordnet werden?
- Welchen Projektarten (Übung, Diplomfilm etc.) werden die Filme zugeordnet?
- Welche Gewerke sind an den Filmen beteiligt? Welche werden als verantwortlich aufgeführt?
- Welche Schlagworte und Stichworte treten auf? Gibt es Worthäufungen zu bestimmten Zeitpunkten?
```

Wie bereits an mehreren Stellen der OER angesprochen wurde, können wir aus rechtlichen Gründen den Originaldatensatz unserer Fallstudie nicht publizieren. Auf diese Problematik wird im Kapitel zu [Problemfelder bei der Datenpublikation](/publikation/problemfelder) noch genauer eingegangen. Für die Darstellung verschiedener Möglichkeiten der Datenvisualisierung können wir daher auch nicht den Originaldatensatz verwenden, sondern greifen auf einen [synthetisch erstellen Auswertungsdatensatz](/bereinigung/openRefine/0_datenbereinigung.md#datenbasis-und-synthetische-datensatze) zurück.

Im Rahmen der Fallstudie verwenden wir <a href="https://www.microsoft.com/de-de/microsoft-365/excel?market=de" class="external-link" target="_blank">Mircosoft Excel</a> als Tool zur Visualisierung und Auswertung. Dabei handelt es sich zwar nicht um ein frei zugängliches, sondern kommerzielles Produkt, jedoch haben zahlreiche Nutzer:innen das *Microsoft-Office-Paket* mit *Excel* auf ihren Computern installiert. Alternativ können auch Open-Source Office-Pakete wie z.B. <a href="https://de.libreoffice.org" class="external-link" target="_blank">LibreOffice</a>verwendet werden. Diese beinhalten ebenfalls für Datenvisualisierungen geeignete Tools und Funktionalitäten.

```{admonition} Achtung
:class: caution
In den folgenden Beschreibungen und für die Screenshots wird *Microsoft Excel* in der Version *2019* unter *Windows* verwendet. In der *Excel*-Version für *macOS* gibt es Abweichungen in der Menüführung und einige Funktionen sind nur eingeschränkt oder gar nicht verfügbar. Insbesondere gilt:

- Der **Legacy-Textimport-Assistent** (Import aus *Text/CSV* mit Überspringen von Zeilen) ist auf dem *Mac* nicht verfügbar. Stattdessen muss der Import über *Daten* > *Aus Text/CSV* erfolgen; eine manuelle Nachbearbeitung der ersten Zeilen ist erforderlich.
- **Power Query** wird unter *macOS* nur in den neueren Versionen von *Excel* (365/2021) unterstützt und ist dort in seinen Funktionen eingeschränkt. In *Excel 2019* für *Mac* steht *Power Query* nicht zur Verfügung.
- In **PivotCharts** sind bestimmte Optionen wie das Ausblenden von Feldschaltflächen oder erweiterte Sortieroptionen nicht verfügbar. Die Ergebnisse können jedoch durch Anpassungen in den *PivotTables* oder manuelles Bearbeiten erreicht werden.
- Die Benutzeroberfläche von **PivotTables** und **PivotCharts** weicht leicht von der Windows-Version ab (z. B. andere Position der Feldlisten).

Die grundlegenden Visualisierungen lassen sich dennoch nachvollziehen, erfordern aber Umwege. Für volle Funktionalität und Kompatibilität wird die Arbeit mit Excel unter **Windows** empfohlen.
```

```{admonition} Achtung
:class: caution
Eine native Desktop-Version von *Excel* für *Linux* existiert nicht. Die Nutzung ist nur möglich über:
- **Excel Online (Webversion)** – kostenlos nutzbar, aber eingeschränkter Funktionsumfang (kein *Power Pivot*, reduzierte Datenimport-Optionen).
- **Virtualisierung oder Emulation** (z. B. *Windows* in einer *VM* oder *Wine/Crossover*) – dadurch ist die vollständige Windows-Version verwendbar, aber mit zusätzlichem Aufwand.
Für volle Funktionalität und Kompatibilität wird die Arbeit mit Excel unter **Windows** empfohlen.
```

Im Folgenden stellen wir nun exemplarisch einige mögliche Vorgehensweisen für die Visualisierung und Auswertung unseres synthetischen Datensatzes dar. Ausgangspunkt sind dabei die vorher erarbeiteten Teilfragestellungen. Die verwendeten Screenshots stammen dabei aus der Excel-Arbeitsoberfläche.

## Import des Datensatzes in Excel
Der synthetische Datensatz liegt, wie ursprünglich der originale bereinigte Datensatz, als *tsv*-Datei vor. In diesem Format wurden die Daten nach der Bereinigung aus *OpenRefine* exportiert. Dieser Datensatz muss nun für die Visualisierungen und Auswertungen in Excel importiert werden.

Ausgangspunkt für den Import in Excel ist die Datei **Synthetischer_Datensatz_Auswertung_OER.tsv**. Sie können den Datensatz [hier](../assets/daten/Synthetischer_Datensatz_Auswertung_OER.tsv) (rechte Maustaste und *Ziel speichern unter* auswählen) herunterladen. Die tsv-Datei weist vor dem eigentlichen Datensatz eine Zeile mit dem Hinweis auf, dass es sich um einen synthetischen Datensatz für Unterrichtszwecke handelt, der keine personenbezogene Daten enthält. Diese erste Zeile muss vom Import ausgeschlossen werden. Nur dann werden die Daten mit den richtigen Spaltennamen korrekt in die Excel-Datei übernommen. Hierfür sind folgende Excel-Einstellungen notwendig.

Öffnen Sie Excel mit einer leeren Arbeitsmappe. Gehen Sie im Reiter *Datei* auf *Optionen*. ({numref}`excel_datei_optionen`)

```{figure} ../assets/auswertung/excel_datei_optionen.png
---
align: center
width: 40%
name: excel_datei_optionen
alt: Darstellung der Navigation über Datei zu Optionen Excel. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Navigation über *Datei* zu *Optionen*
```

Im sich öffnenden Optionen-Fenster gehen Sie zum Punkt *Daten*. Wählen Sie dort unter *Legacy-Datenimport-Assistenten anzeigen* das Kästchen *Aus Text (Legacy)* an. Bestätigen Sie die Auswahl mit *OK*. ({numref}`excel_optionen`)

```{figure} ../assets/auswertung/excel_optionen.png
---
align: center
width: 80%
name: excel_optionen
alt: Darstellung der Einstellungen in Optionen für den Datenimport in Excel. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Einstellungen in Optionen für den Datenimport in Excel
```

Gehen Sie nun auf den Reiter *Daten* und dort auf *Daten abrufen*. Unter *Legacy-Assistenten* klicken Sie auf *Aus Text (Legacy)*. ({numref}`excel_legacy`)

```{figure} ../assets/auswertung/excel_legacy_assistent_text.png
---
align: center
width: 80%
name: excel_legacy
alt: Darstellung der Schritte zum Starten des Text-Legacy-Assistenten. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Starten des Text-Legacy-Assistenten
```

Im Datei-Import Fenster navigieren Sie zum Speicherort der Datei *Synthetischer_Datensatz_Auswertung_OER.tsv* auf Ihrem Computer. Achten Sie darauf, dass rechts unten *Alle Dateien* ausgewählt ist, da ansonsten die tsv-Datei nicht angezeigt wird. Bestätigen sie die Auswahl mit *Importieren*. ({numref}`excel_dateiimport`)

```{figure} ../assets/auswertung/excel_textdatei_importieren.png
---
align: center
width: 80%
name: excel_dateiimport
alt: Darstellung der Auswahl der Import-Datei. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Auswahl der Import-Datei
```

Im ersten Schritt des Textkonvertierungs-Assistenten ist unter Datentyp der Punkt *Getrennt* (also mit Tabulatoren getrennt) bereits korrekt ausgewählt und kann so übernommen werden. *Import beginnen in Zeile* stellen Sie von *1* auf *2* ein, da beim Import ja die erste Zeile mit dem Hinweis auf die Übungsdatei übersprungen werden soll. Für *Dateiursprung* wählen Sie *65001 : Unicode (UTF-8)* aus – dies ist die Zeichen-Codierung, die beim Export aus *OpenRefine* verwendet wurde. Rufen Sie den zweiten Schritt durch Klick auf *Weiter* auf. ({numref}`excel_assistent_1`)

```{figure} ../assets/auswertung/excel_texkonvertierungsassistent_1.png
---
align: center
width: 80%
name: excel_assistent_1
alt: Darstellung des Textkonvertierungs-Assistenten – Schritt 1. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Textkonvertierungs-Assistent – Schritt 1
```

Im zweiten Schritt des Assistenten wird *Tabstopp* als *Trennzeichen* korrekt erkannt und kann mit *Weiter* übernommen werden. ({numref}`excel_assistent_2`)

```{figure} ../assets/auswertung/excel_texkonvertierungsassistent_2.png
---
align: center
width: 80%
name: excel_assistent_2
alt: Darstellung des Textkonvertierungs-Assistenten – Schritt 2. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Textkonvertierungs-Assistent – Schritt 2
```

Auch im dritten Schritt des Assistenten kann die Einstellung *Datenformat der Spalten* -> *Standard* beibehalten werden. Schließen Sie den Textkonvertierungs-Assistenten mit *Fertig stellen* ab. ({numref}`excel_assistent_3`)

```{figure} ../assets/auswertung/excel_texkonvertierungsassistent_3.png
---
align: center
width: 80%
name: excel_assistent_3
alt: Darstellung des Textkonvertierungs-Assistenten – Schritt 3. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Textkonvertierungs-Assistent – Schritt 3
```

Sie können nun den Ort in der Excel-Arbeitsmappe auswählen, an dem der Import durchgeführt werden soll. Auch hier können sie die Vorgabe *Bestehendes Arbeitsblatt* übernehmen und die Daten mit einem Klick auf *OK* aus der tsv-Datei in Excel importieren. ({numref}`excel_import_ort`)

```{figure} ../assets/auswertung/excel_import_ort.png
---
align: center
width: 80%
name: excel_import_ort
alt: Darstellung Ort des Datenimports festlegen. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Ort des Datenimports festlegen
```

Der Import der Daten der aus der Datei *Synthetischer_Datensatz_Auswertung_OER.tsv* in eine Excel-Arbeitsmappe ist nun abgeschlossen. Die Spaltenüberschriften und die Inhalte der Spalten wurden korrekt übernommen. ({numref}`excel_import_ende`)

```{figure} ../assets/auswertung/excel_import_ende.png
---
align: center
width: 100%
name: excel_import_ende
alt: Darstellung Abgeschlossener Datenimport in Excel. Ein Teil der Daten-Tabelle ist sichtbar.
---
Abgeschlossener Datenimport in Excel
```

Speichern Sie die importierten Daten als Excel-Datei durch einen Klick auf den Reiter *Datei* und anschließend *Speicher unter* ab. Wählen Sie hierfür den Speicherort auf Ihrem Computer aus und vergeben Sie einen Namen für die Datei, z.B. *Datensatz_Auswertung_OER.xlsx*. Diese Excel-Datei bildet den Ausgangspunkt für die nun folgenden Visualisierungen und Auswertungen.


## Titel pro Jahr
Wie ist es nun möglich, aus dem Datensatz eine grafische Darstellung der Anzahl der Titel pro Jahr im Untersuchungszeitraum unserer Fallstudie zu erstellen? In Excel kann hierfür die *PivotChart* Funktion verwendet werden. Öffnen sie dazu Datensatz als Excel-Datei. Im Reiter *Einfügen* klicken Sie nun auf *PivotChart* und wählen *PivotChart und PivotTable* aus. ({numref}`excel_pivot_chart`)

```{figure} ../assets/auswertung/excel_einfuegen_pivot_chart.png
---
align: left
width: 100%
align: center
name: excel_pivot_chart
alt: Darstellung der Excel Arbeitsoberfläche. Der Reiter Einfügen und die Auswahlmöglichkeiten PivotChart und Tabelle sind durch rote Kreise markiert.
---
Auswahl *PivotChart und PivotTable* im Reiter *Einfügen*.
```

Es öffnet sich ein Fenster *PivotTable erstellen*. Die Einstellungen können sie unverändert übernehmen und mit *OK* bestätigen. ({numref}`excel_pivot_tabelle`)

```{figure} ../assets/auswertung/excel_pivot_einfuegen_erstellen.PNG
---
align: left
width: 100%
align: center
name: excel_pivot_tabelle
alt: Darstellung des Fensters PivotTable erstellen. Die Schaltfläche OK ist mit einem roten Kreis gekennzeichnet.
---
Das Fenster *PivotTable erstellen*.
```

Es öffnet sich eine Excel-Arbeitsoberfläche. Auf der linken Seite wird eine leere Pivot-Tabelle angezeigt, in der Mitte ein leeres PivotChart und auf der rechten Seite sind PivotChart-Eingabefelder sichtbar, die noch nicht ausgefüllt sind. ({numref}`excel_pivot_screen`)

```{figure} ../assets/auswertung/excel_pivot_erstellen_screen.png
---
align: left
width: 100%
align: center
name: excel_pivot_screen
alt: Darstellung der Excel Arbeitsoberfläche mit Pivot-Elementen
---
Die Excel Arbeitsoberfläche mit Pivot-Elementen.
```

Nun wählen Sie unter *PivotChart-Felder* im rechten Bereich die Spalten *Titel* und *Jahr_1* an. Für *Jahr_1* müssen sie evtl. mit dem Balken nach unten scrollen. ({numref}`excel_pivot_felder`)

```{figure} ../assets/auswertung/titel_Jahr_excel_pivot_chart_felder.png
---
align: left
width: 100%
align: center
name: excel_pivot_felder
alt: Darstellung der im Bereich PivotChart-Felder angewählten Möglichkeiten Titel und Jahr_1
---
*Titel* und *Jahr_1* anwählen.
```

Auf der Excel-Arbeitsoberfläche werden eine erste Pivot-Tabelle und ein Pivot-Chart angezeigt, die jedoch noch keine sinnvollen Ergebnisse aufweisen. Hierfür müssen Sie die die Eingaben in den Feldern rechts unten verändern, also vertauschen. Klicken sie dafür auf den Eintrag und ziehen sie ihn in das jeweilige Eingabefeld. Das Feld *Achse (Rubriken)* beinhaltet dann den Eintrag *Jahr_1*, das Feld Werte den Eintrag *Anzahl von Titel*. ({numref}`titel_jahr_tausch`)

```{figure} ../assets/auswertung/titel_jahr_excel_pivot_chart_felder_tausch.png
---
align: left
width: 100%
align: center
name: titel_jahr_tausch
alt: Darstellung der im Bereich PivotChart-Felder ausgetauschten Einträge Jahr_1 und Titel.
---
Austausch der Feldinhalte
```

Durch den Austausch der Einträge ergibt sich ein Pivot-Chart, das bereits die gewünschte Visualisierung beinhaltet: In einem Säulendiagramm wird die Anzahl der Titel pro Jahr im Datensatz angezeigt, vom Jahr 1985 bis 1999. Allerdings enthält diese Darstellung noch Elemente, die für eine weitere Verwendung der Visualisierung bearbeitet werden müssen. ({numref}`titel_jahr_roh`)

```{figure} ../assets/auswertung/titel_jahr_grafik_roh.png
---
align: left
width: 100%
align: center
name: titel_jahr_roh
alt: Darstellung des Pivot-Chart, die Elemente die noch bearbeitet werden müssen sind rot umkreist.
---
Visualisierung vor der Bearbeitung
```

Die Legende auf der rechten Seite, die mit Ergebnis beschriftet ist, ist für diese Grafik nicht unbedingt notwendig. Ein Klick auf das Element ermöglicht das Löschen, indem im Kontextmenü der entsprechende *Löschen*-Befehl angewählt wird. Klicken Sie nun auf das Textfeld mit dem Inhalt *Ergebnis* in der Mitte des Charts, Sie können den Text nun mit einem neuen ersetzen, z.B. *Anzahl der Titel pro Jahr*.

Abschließend sollen noch die die Schaltflächen *Anzahl von Titel* links oben und *Jahr_1* links unten entfernt werden. Klicken sie hierfür im Reiter *Analysieren* auf *Feldschaltflächen* und wählen Sie *alle ausblenden* an. ({numref}`titel_jahr_ausblenden`)

```{figure} ../assets/auswertung/titel_jahr_feldschaltflaechen_ausblenden.png
---
align: left
width: 100%
align: center
name: titel_jahr_ausblenden
alt: Darstellung des Auswahlmenüs zum Ausblenden der Feldschaltflächen.
---
Ausblenden der Feldschaltflächen
```

Als Ergebnis erhalten Sie ein Säulendiagramm, dass die Anzahl der Titel pro Jahr in unserem untersuchten Datensatz darstellt. Durch Copy & Paste können Sie das Diagramm in andere Programme einfügen. ({numref}`titel_jahr_saule`)

```{figure} ../assets/auswertung/titel_jahr_grafik_säule.png
---
align: left
width: 100%
align: center
name: titel_jahr_saule
alt: Darstellung des Säulendiagramms zur Anzahl der Titel pro Jahr
---
Säulendiagramm zur Anzahl der Titel pro Jahr
```

Für die Auswertung haben wir zwar einen synthetischen Datensatz verwendet, die Proportionen des Originaldatensatzes sind aber weitgehend erhalten geblieben. Auffällig an der Grafik ist, dass die Anzahl der Titel 1988 sprunghaft ansteigt und sich im Vergleich zu 1987 fast verdoppelt. Danach ist wieder ein leichter Rückgang zu erkennen. Die Anzahl bleibt aber in den Wendejahren bis 1990 noch hoch und pendelt sich dann in den folgenden Jahren bei zwischen 60 und 80 Titel pro Jahr ein. Während der Wendezeit hat sich die Zahl der Filmtitel in unserem Datensatz also deutlich erhöht. Im Jahr 1995 ist nochmals ein Anstieg der Titelanzahl zu erkennen, der Grund hierfür müsste noch erforscht werden.

Mit Excel ist es einfach möglich, die Darstellung als Säulendiagramm in ein Liniendiagramm zu verwandeln. Klicken Sie hierfür mit einem Rechtsklick in das PivotChart in Excel und wählen sie im Kontextmenü *Diagrammtyp ändern* aus. ({numref}`titel_jahr_aendern_1`)

```{figure} ../assets/auswertung/titel_jahr_diagrammtyp_ändern_1.png
---
align: left
width: 100%
align: center
name: titel_jahr_aendern_1
alt: Darstellung Kontextmenüs, mit dem der Diagrammtyp geändert werden kann. Die notwendige Auswahl ist rot umkreist.
---
Kontextmenü zum Ändern des Diagrammtyps
```

Im erscheinenden Feld wählen Sie als Diagrammtyp *Linie* an und klicken auf *OK*. ({numref}`titel_jahr_aendern_2`)

```{figure} ../assets/auswertung/titel_jahr_diagrammtyp_ändern_2.png
---
align: left
width: 80%
align: center
name: titel_jahr_aendern_2
alt: Darstellung Auswahlmenüs, mit dem der Diagrammtyp geändert werden kann. Die notwendige Auswahl ist rot umkreist.
---
Auswahlmenü zum Ändern des Diagrammtyps
```

Als Ausgabe ergibt sich ein Liniendiagramm mit den gleichen Werten aus unserem analysierten Datensatz. ({numref}`titel_jahr_linie`)

```{figure} ../assets/auswertung/titel_jahr_grafik_linie.png
---
align: left
width: 100%
align: center
name: titel_jahr_linie
alt: Darstellung Liniendiagramm Anzahl der Titel pro Jahr
---
Liniendiagramm Anzahl der Titel pro Jahr
```

Im Liniendiagramm ist der sprunghafte Anstieg der Anzahl der Filmtitel im Jahr 1988 und zur Wendezeit noch deutlicher zu erkennen, ebenfalls die darauf folgende Reduktion der Titelanzahl in den weiteren Jahren. 

## Anzahl der Gattungen pro Jahr
Im nächsten Schritt soll nun eine visuelle Darstellung der Anzahl der Gattungen pro Jahr erstellt werden, die auf den Angaben in unserem synthetischen Datensatz beruht. Um die Übersichtlichkeit zu gewährleisten bietet es sich an, sich auf die Hauptgattungen Spielfilm, Dokumentarfilm und Animationsfilm zu konzentrieren und Mischformen oder andersartige Bezeichnungen außen vor zu lassen.

Das Vorgehen ist zunächst gleich wie bei der Darstellung der Titel pro Jahr. Gehen Sie in der Excel-Datei zum Arbeitsblatt, das die aus der [tsv-Datei importierten Daten](#import-des-datensatzes-in-excel) enthält. Wählen Sie im Reiter *Einfügen* den Punkt *PivotChart und PivotTable* aus. In den *PivotChart-Feldern* auf der rechten Seite der Oberfläche wählen sie dieses Mal jedoch nicht *Titel* und *Jahr_1*, sondern *Gattung* und *Jahr_1* aus. (siehe {numref}`excel_pivot_chart` bis {numref}`excel_pivot_felder`). Die angewählten Spalten werden wieder automatisch den PivotChart-Feldern *Achse (Rubriken)* und *Werte* zugeordnet. ({numref}`gattung_jahr_felder1`)

```{figure} ../assets/auswertung/gattung_jahr_felder_auswahl_1.png
---
align: center
width: 50%
name: gattung_jahr_felder1
alt: Darstellung der Auswahl PivotChart-Felder *Gattung* und "Jahr_1*. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl PivotChart-Felder *Gattung* und *Jahr_1*
```

Aus diesen automatisch ausgewählten Einträge in die Felder ergibt sich jedoch keine sinnvolle visuelle Darstellung der Daten in der Excel-Arbeitsoberfläche. Die Eingaben müssen angepasst und durch Anklicken und Ziehen in die richtigen Felder gebracht werden: Im Feld *Achse (Rubriken)* steht nun *Jahr_1*, im Feld *Werte* die *Anzahl von Gattungen* und im Feld *Legende (Reihe)* ist der Wert *Gattung* eingetragen. *Gattung* wird durch Anklicken in der oberen Liste und Ziehen in das Feld *Legende (Reihe)* gebracht. ({numref}`gattung_jahr_felder2`)

```{figure} ../assets/auswertung/gattung_jahr_felder_auswahl_2.png
---
align: center
width: 50%
name: gattung_jahr_felder2
alt: Darstellung der Auswahl PivotChart-Felder *Legende (Reihe)*, *Achse (Rubriken)* und *Werte*. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl PivotChart-Felder *Legende (Reihe)*, *Achse (Rubriken)* und *Werte*
```

Durch diese Einstellungen ergibt sich bereits eine visuelle Darstellung der in unserem synthetischen Datensatz enthaltenen Gattungen, verteilt über die Jahre des Untersuchungszeitraums unserer Fallstudie. Wir wollen uns jedoch auf die drei Gattungen Spielfilm, Dokumentarfilm und Animationsfilm beschränken und Mischformen nicht in der Grafik darstellen. Hierzu klicken sie auf die Feldschaltfläche *Gattung* in der Grafik auf der Excel-Benutzeroberfläche. Es öffnet sich ein Kontextmenü. Wählen Sie dort nur die Einträge Spielfilm, Dokumentarfilm und Animationsfilm aus und lassen Sie die anderen Möglichkeiten leer. Ein Klick auf *OK* beendet die Eingabe. ({numref}`gattung_jahr_ohne`)

```{figure} ../assets/auswertung/gattung_jahr_ohne_auswahl.png
---
align: center
width: 100%
name: gattung_jahr_ohne
alt: Darstellung der Auswahl der Gattungen die dargestellt werden sollen. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl der Gattungen die dargestellt werden sollen
```

Passen Sie nun wie im Abschnitt zur Darstellung der [Titel pro Jahr](/auswertung/datenvisualisierung.md#titel-pro-jahr) beschrieben den Titel des Diagramms an und blenden Sie die Feldschaltflächen aus (vgl. {numref}`titel_jahr_roh` und {numref}`titel_jahr_ausblenden`). Als Ergebnis erhalten sie ein Säulendiagramm, das die Verteilung der Gattungen Spielfilm, Dokumentarfilm und Animationsfilm über die Jahre unseres Untersuchungszeitraums darstellt. ({numref}`gattung_jahr_säule`)

```{figure} ../assets/auswertung/gattung_jahr_säule.png
---
align: center
width: 100%
name: gattung_jahr_säule
alt: Darstellung Säulendiagramm Gattungen pro Jahr.
---
Säulendiagramm Gattungen pro Jahr
```

In diese Darstellung kann zusätzlich noch eine Datentabelle eingeblendet werden. Hierfür klicken Sie auf das grüne Pluszeichen neben dem Diagramm in der Excel-Arbeitsoberfläche. Wählen Sie dann im Kontextmenü den Punkt *Datentabelle* an. ({numref}`gattung_jahr_säule_daten_auswahl`)

```{figure} ../assets/auswertung/gattung_jahr_säule_datentabelle.png
---
align: center
width: 100%
name: gattung_jahr_säule_daten_auswahl
alt: Darstellung der Auswahl der Anzeige Datentabelle. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl der Anzeige Datentabelle
```

Im Diagram werden nun in einer Tabelle die konkreten Zahlen zu Spielfilmen, Dokumentarfilmen und Animationsfilmen pro Jahr aus unserem syntehtischen Datensatz angezeigt. ({numref}`gattung_jahr_säule_daten`)

```{figure} ../assets/auswertung/gattung_jahr_säule_datentabelle_end.png
---
align: center
width: 100%
name: gattung_jahr_säule_daten
alt: Darstellung Gattungen pro Jahr mit Datentabelle
---
Säulendiagramm Gattungen pro Jahr mit Datentabelle
```

Was ergibt sich nun aus dieser visuellen Darstellung der Daten zu den Gattungen pro Jahr als Säulendiagramm? Auffallend ist, dass der Anteil an Dokumentarfilmen bereits ab dem Jahr 1985 sehr hoch ist im Vergleich zu den Spielfilmen und Animationsfilmen. Rund um die Jahre der Wende 1987, 1988 und 1989 ist im Diagramm nochmals eine deutliche Zunahme der dokumentarischen Arbeiten erkennbar. Dies kann darauf hindeuten, dass es den Studierenden (und evtl. auch den Lehrenden) wichtig war, die Ereignisse dieser Umbruchsjahre zu dokumentieren und kritisch zu begleiten. In den 1990er Jahren wiederum nimmt die Zahl der Dokumentarfilme ab, während mehr Spielfilme und Animationsfilme produziert wurden. Ob dies auf die veränderten politischen Bedingungen und sich wandelnde Strukturen im Studium zurückzuführen ist, müsste näher beleuchtet werden.

Insgesamt sind die Daten zu den Gattungen und damit auch ihre visuellen Darstellung jedoch mit Vorsicht zu betrachten. Wie im Kapitel zur Analyse der [Datenquelle](/bereinigung/datenquelle.md) dargelegt wurde, sind nicht alle Filmtitel mit Angaben zu ihrer jeweiligen Gattung versehen. Viele Titel sind hinsichtlich ihrer Zugehörigkeit zu Spielfilm, Dokumentarfilm oder Animationsfilm nicht klassifiziert. Hier ist also eine genauere Recherche im Archiv unumgänglich. Dennoch können wir die visuelle Auswertung der Daten mit in diese Recherche nehmen - z.B. indem wir überprüfen, wieviele Dokmentarfilme in den Jahren 1987 bis 1989 im Filmarchiv der Filmuniversität vorhanden sind. Diese Recherche kann dann mit den bereits vorhandenen Daten und deren visuellen Darstellung abgeglichen werden.

## Projektarten pro Jahr
Die visuelle Darstellung der Projektarten pro Jahr wird als Übung realisiert. Sie können dabei Ihr im letzten Kapitel erworbenes Wissen anwenden.

`````{admonition} Übung
:class: exercise
Erstellen sie auf der Grundlage des synthetischen Auswertungsdatensatz mit Excel eine visuelle Darstellung der Projektarten pro Jahr. Beschränken sie dabei die Darstellung auf die Projektarten *Abschlußfilm*, *Diplomfilm*, *Hauptprüfungsfilm* und  *Vordiplomfilm*.

````{admonition} Lösung
    :class: solution, dropdown

Eine mögliche Lösung ist folgendes Vorgehen. Wählen Sie im Reiter *Einfügen* die Option *PivotChart und PivotTable* aus. Bestätigen Sie die Eingabe im Fenster *PivotTable erstellen* mit *OK*. Sie gelangen zur Excel-Arbeitsoberfläche, in der Sie *PivotChart-Felder* auf der rechten Seite auswählen können. (vgl. {numref}`excel_pivot_chart` bis {numref}`excel_pivot_screen`).

Klicken Sie nun in den *PivotChart-Feldern* die Spalten *Projektart_1* und *Jahr_1* an. ({numref}`projektart_auswahl`)

```{figure} ../assets/auswertung/projektart_jahr_felder_auswahl.png
---
align: center
width: 50%
name: projektart_auswahl
alt: Darstellung der Auswahl Projektart_1 und Jahr_1. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl *Projektart_1* und *Jahr_1*
```

Ordnen Sie nun in den Feldern die jeweiligen Einträge zu:
* Achse (Rubriken) -> *Jahr_1*
* Werte -> *Anzahl von Projektart_1*
* Legende (Reihe) -> Projektart_1

*Projektart_1* tragen Sie ein, indem Sie den Eintrag in Feld oberhalb anklicken und in das entsprechende Eingabefeld Legende (Reihe) ziehen. ({numref}`projektart_auswahl_2`)

```{figure} ../assets/auswertung/projektart_jahr_felder_auswahl_2.png
---
align: center
width: 50%
name: projektart_auswahl_2
alt: Darstellung der Einträge in den Feldern. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Einträge in den Feldern
```

In der Excel-Arbeitsoberfläche sehen Sie nun das Säulendiagramm mit allen Projektarten. Grenzen Sie die angezeigten Projektarten ein, indem Sie auf die Feldschaltfläche *Projektart_1* in der Grafik klicken. Wählen Sie im Kontextmenü die Projektarten *Abschlußfilm*, *Diplomfilm*, *Hauptprüfungsfilm* und  *Vordiplomfilm* aus und bestätigen Sie die Eingabe mit *OK*. ({numref}`projektart_eingrenzung`)

```{figure} ../assets/auswertung/projektart_jahr_eingrenzung.png
---
align: center
width: 100%
name: projektart_eingrenzung
alt: Darstellung der Eingrenzung der angezeigten Projektarten. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Eingrenzung der angezeigten Projektarten
```

Klicken Sie auf das grüne Kreuz und fügen Sie einen Diagrammtitel hinzu. Abschließend wählen Sie im Menü *Analysieren* den Punkt den Punkt *Feldschaltflächen -> alle ausblenden* aus. (vgl. {numref}`titel_jahr_ausblenden`) Sie haben nun ein Säulendiagramm mit den Projektarten *Abschlußfilm*, *Diplomfilm*, *Hauptprüfungsfilm* und  *Vordiplomfilm* pro Jahr erstellt. Dieses können Sie per Copy & Paste in andere Programme einbinden.

````
`````

Für die Darstellung der Projektarten *Abschlußfilm*, *Diplomfilm*, *Hauptprüfungsfilm* und  *Vordiplomfilm* pro Jahr ergibt sich folgendes Säulendiagramm ({numref}`projektart_end`):

```{figure} ../assets/auswertung/projektart_jahr_end.png
---
align: center
width: 100%
name: projektart_end
alt: Darstellung Säulendiagramm Projektarten pro Jahr.
---
Säulendiagramm Projektarten pro Jahr
```

Es zeigt sich, dass in den Jahren 1987 bis 1989 deutlich mehr Diplomfilme als in den Jahren zuvor entstanden sind. Die Jahre 1985, 1986 und 1990 weisen sehr viele Hauptprüfungsfilme auf, diese Kategorie verschwindet nach Anfang der 1990er Jahre. Ab 1994 steigt die Zahl der Diplomfilme deutlich an.

Auch hier muss bei der Interpretation der visualisierten Daten vorsichtig vorgegangen werden. Wie schon bei den Gattungen werden auch die Projektarten nicht immer in den Angaben zu den Titeln erfasst (vgl. das Kapitel zur [Datenquelle](/bereinigung/datenquelle.md)). Die Zahlen können also von den real entstandenen Prüfungsarbeiten abweichen. Dennoch würde es sich anbieten, die sich verändernde Anzahl von Projektarten mit in der Zeit geltenden Studien- und Prüfungsordnungen abzugleichen. Die Veränderungen könnten auf eine neue Organisation des Studiums hindeuten. 

Wir haben eine weitere Visualisierung zu Projekarten mit der Bezeichnung *Übung* angefertigt. ({numref}`projektart_uebung`)

```{figure} ../assets/auswertung/projektart_übungen_jahr.png
---
align: center
width: 100%
name: projektart_uebung
alt: Darstellung Säulendiagramm Projektarten "Übung" pro Jahr.
---
Säulendiagramm Projektarten "Übung" pro Jahr
```
Hier fällt auf, dass die Anzahl der *Kameraübungen* und *TV-Übungen* in den Jahren 1988 und 1989 deutlich ansteigt, 1988 auch die Anzahl der Lichtübungen. Ein Grund hierfür könnte sein, dass innerhalb dieser Übungsformen aktuelle Ereignisse der Wendezeit besonders unkompliziert dokumentiert werden konnten. Auch Anfang der 1990er Jahre ist die Anzahl der Kameraübungen relativ hoch, wird aber noch von den Lichtübungen übertroffen. Diese Veränderungen könnten wiederum auf neue Unterrichtsstrukturen hindeuten. In beiden Fällen ist eine fundierte Recherche im Filmarchiv notwendig, um mögliche Ursachen für den Anstieg der Zahlen zu erforschen. Die Visualisierungen aus dem Datensatz können als Ausgangspunkt für diese Recherchen dienen.


## Anzahl der verantwortlichen Gewerke
Im nächsten Schritt soll der Datensatz hinsichtlich der Angaben zu den verantwortlichen Gewerken ausgewertet werden. Die Daten hierzu sind auf vier Spalten verteilt (verantw._Gewerk 1 bis 4). Für eine Visualisierung der Anzahl der Gewerke müssen die Inhalte der Spalten zunächst in eine Spalte zusammengeführt werden. Wählen Sie dafür im Reiter Daten die Option *Aus Tabelle/Bereich* an. ({numref}`excel_tabelle_bereich`)

```{figure} ../assets/auswertung/Excel_Daten_Tabelle_Bereich.png
---
align: center
width: 100%
name: excel_tabelle_bereich
alt: Auswahl im Reiter Daten: Aus Tabelle/Bereich. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl im Reiter Daten: *Aus Tabelle/Bereich*
```

Es öffnet sich der *Power Query-Editor* in Excel. Klicken Sie dort auf *Spalten auswählen*. ({numref}`excel_spalten_auswahl`)

```{figure} ../assets/auswertung/excel_spalten_auswaehlen.png
---
align: center
width: 100%
name: excel_spalten_auswahl
alt: Darstellung Option Spalten auswählen. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Option *Spalten auswählen*
```

Es öffnet sich ein Fenster zur Auswahl der Spalten. Wählen Sie zunächst zu Beginn der Liste alle Spalten ab und klicken sie anschließend auf *verantw._Gewerk_1 bis 4*. Beenden Sie die Eingabe mit *OK*. ({numref}`excel_spalten_gewerk`)

```{figure} ../assets/auswertung/excel_auswahl_gewerk.PNG
---
align: center
width: 50%
name: excel_spalten_gewerk
alt: Darstellung Auswahl der Spalten. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl der Spalten
```

Wählen Sie in der Arbeitsoberfläche alle Spalten aus, indem Sie auf den Spaltentitel klicken und dabei die *Strg-Taste* gedrückt halten. Die Spalten sind nun farbig hervorgehoben. Ein Rechtsklick auf einen der Spaltentitel öffnet ein Menü, in dem Sie *Nur ausgewählte Spalten entpivotieren* anwählen. ({numref}`excel_entpivotieren`)


```{figure} ../assets/auswertung/excel_spalten_entpivotieren.png
---
align: center
width: 100%
name: excel_entpivotieren
alt: Darstellung Markierte Spalten entpivotieren. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Markierte Spalten entpivotieren
```

Es entstehen zwei Spalten. *Attribut* enthält die Angaben zum *verantw._Gewerk 1 bis 4*, in *Wert* wurden die Inhalte der Spalten jeweils unteinandern aufgeführt übernommen. Wählen Sie nun *Schließen und Laden* an. Der *Power Query-Editor* wird geschlossen und die Inhalte der Spalten in ein neues Excel-Arbeitsblatt eingefügt. ({numref}`excel_query_ende`)

```{figure} ../assets/auswertung/excel_power_query_schließen.png
---
align: center
width: 50%
name: excel_query_ende
alt: Darstellung Markierte Spalten entpiovotieren. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Neue Spalten und Schließen des *Power Query-Editors*
```

Im neuen Excel-Arbeitsblatt benennen Sie die zwei Spalten um, damit sie für eine mögliche spätere Verwendung besser unterschieden werden können, z.B. in *Attribut_verant_Gewerk* und *Wert_verantw_Gewerk*. Ausgehend von dieser Excel-Tabelle können sie mit dem bereits bekannten Vorgehen mit der Visualisierung der Daten zu den verantwortlichen Gewerken beginnen.

Markieren Sie die beiden Spalten und Wählen Sie im Reiter *Einfügen* die Option *PivotChart und PivotTabelle* aus. Bestätigen Sie die Eingabe im folgenden Feld und wählen Sie in den *PivotChart-Feldern* beide Spalten an. (vgl. {numref}`excel_pivot_chart` bis {numref}`excel_pivot_felder`). Auf das Feld *Achse (Rubriken)* ziehen Sie den Eintrag *Wert_verantw_Gewerk*, auf *Werte* den Eintrag *Anzahl von Attribut_verantw_Gewerk*. ({numref}`excel_felder_gewerke`)


```{figure} ../assets/auswertung/excel_chart_felder_gewerke.png
---
align: center
width: 50%
name: excel_felder_gewerke
alt: Darstellung Einträge in die PivotChart-Felder. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Einträge in die PivotChart-Felder
```

Die Grafik zeigt nun die Anzahl der verantwortlichen Gewerke für alle entsprechenden Einträge im Datensatz an. Blenden Sie ggf. die Legende zur Grafik durch einen Klick auf das grüne Kreuz und das Setzen eines Hakens bei *Legende* ein. ({numref}`excel_legende`)


```{figure} ../assets/auswertung/excel_legende_einblenden.png
---
align: center
width: 40%
name: excel_legende
alt: Darstellung der Einblendung der Legende zur Grafik.  Einzelne Eingaben sind mit rot gekennzeichnet.
---
Einblendung der Legende zur Grafik
```

Für eine bessere Übersichtlichkeit der Visualisierung sollte diese noch angepasst werden. ({numref}`gewerke_roh`)

```{figure} ../assets/auswertung/Gewerke_verantwortlich_roh.png
---
align: center
width: 100%
name: gewerke_roh
alt: Darstellung der Grafik Erste Visualisierung der Anzahl der verantwortlichen Gewerke
---
Erste Visualisierung der Anzahl der verantwortlichen Gewerke
```

Dies geschieht über die Feldschaltfläche *Wert_verantw_Gewerk* im Chart. Beschränken Sie z.B. die Auswahl der in der Grafik dargestellten Gewerke auf diejenigen, die am häufigsten aufgeführt werden oder die für die Fragestellung interessant sind. Die Werte können Sie der Pivot-Tabelle entnehmen, die gleichezitig mit dem Pivot-Chart erzeugt wurde. Dies kann z.B. eine Beschränkung auf Animation, Buch, Kamera, Kameraübung und Regie sein. Für eine weitere Auswertung können sie die Auswahl der angezeigten Gewerke variieren. ({numref}`gewerke_auswahl`)


```{figure} ../assets/auswertung/gewerke_auswahl.png
---
align: center
width: 100%
name: gewerke_auswahl
alt: Darstellung Auswahl der Gewerke für die Visualisierung und Weitere Sortieroptionen. Einzelne Eingaben sind mit rot gekennzeichnet.
---
Auswahl der Gewerke für die Visualisierung und *Weitere Sortieroptionen*
```

Zusätzlich ist es möglich, die Reihenfolge der Gewerke in der Grafik zu verändern. Wählen Sie hierfür ebenfalls bei der Feldschaltfläche *Wert_verantw_Gewerk* den Punkt *weitere Sortieroptionen* aus. Im sich öffnenden Fenster zu *Sortieroptionen* entscheiden Sie sich bei *Absteigend (Z bis A) nach:* für die Option *Anzahl von Attribut_verantw_Gewerk*. ({numref}`gewerke_sortieren`)

```{figure} ../assets/auswertung/gewerke_sortieren.png
---
align: center
width: 50%
name: gewerke_sortieren
alt: Darstellung Auswahl aus Sortieroptionen. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl aus Sortieroptionen
```
 
In der Grafik werden nun die verantwortlichen Gewerke absteigend nach der Anzahl ihrer Nennung im Datensatz dargestellt. Versehen Sie die Grafik nun mit einer Beschriftung und blenden Sie die Feldschaltflächen aus. (vgl. {numref}`titel_jahr_roh` und {numref}`titel_jahr_ausblenden`) Per *Copy & Paste* können Sie die Grafik in andere Anwendungen einfügen. ({numref}`gewerke_verantwortlich`)

```{figure} ../assets/auswertung/Gewerke_verantwortlich.png
---
align: center
width: 100%
name: gewerke_verantwortlich
alt: Darstellung Grafik Anzahl der verantwortlichen Gewerke
---
Anzahl der verantwortlichen Gewerke
```

Eine Dominanz der Regie ist hier deutlich ersichtlich, gefolgt von der Kamera. Diese Unterschiede lassen sich durch einen anderen Diagrammtyp noch besser erfassen.

`````{admonition} Übung
:class: exercise
Wandeln Sie das Säulendiagramm zu *Anzahl der verantwortlichen Gewerke* in ein Kreisdiagramm um.

````{admonition} Lösung
    :class: solution, dropdown

Öffnen Sie mit einem Rechtsklick in die Grafik das Kontextmenü. Wählen Sie dort die Option *Diagrammtyp ändern* aus. ({numref}`gewerke_diagrammtyp_1`)

```{figure} ../assets/auswertung/gewerke_diagrammtyp_1.png
---
align: center
width: 100%
name: gewerke_diagrammtyp_1
alt: Darstellung *Diagrammtyp ändern*. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl *Diagrammtyp ändern*
```

Im sich öffnenden Fenster wählen Sie den Diagrammtyp *Kreis* aus. ({numref}`gewerke_diagrammtyp_2`)

```{figure} ../assets/auswertung/gewerke_diagrammtyp_2.png
---
align: center
width: 80%
name: gewerke_diagrammtyp_2
alt: Darstellung Auswahl Diagrammtyp Kreis. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl Diagrammtyp Kreis
```

Das Säulendiagramm wird in ein Kreisdiagramm umgewandelt.

````
`````

Im Kreisdiagramm wird die Dominanz der Regie im Rahmen der verantwortlichen Gewerke noch deutlicher. ({numref}`gewerke_verantwortlich_kreis`)

```{figure} ../assets/auswertung/Gewerke_verantwortlich_kreis.png
---
align: center
width: 100%
name: gewerke_verantwortlich_kreis
alt: Darstellung der Anzahl der verantwortlichen Gewerke als Kreisdiagramm
---
Anzahl der verantwortlichen Gewerke als Kreisdiagramm
```

Wie auch bei den bisherigen Visualisierungen und Auswertungen zum Datensatz muss bedacht werden, dass nicht für alle Titel die jeweils verantwortlichen Gewerke bei der Datenerfassung in die filmografischen Angaben aufgenommen wurden. Weiterführende Recherchen im Filmarchiv und in weiteren Archiven mit Informationen zu Entstehungskontexten der Filme sind also notwendig. Die Domianz der Regie in der Anzahl der für die Filme verantwortlichen Gewerke ist nicht weiter verwunderlich, wird die Regie – dem Auteur-Gedanken folgend – doch meist als die für den gesamten künstlerischen Prozess verantwortliche Instanz angesehen. Die Zuordnung verantwortlicher Gewerke zu studentischen Produktionen kann aber auch mit Lehrplänen und Studienordnungen zusammenhängen. Diese sollten in eine genauere Analyse der Zahlen zu den verantwortlichen Gewerken einbezogen werden.

## Anzahl der Schlagworte pro Jahr
Die Visuallsierung und Auswertung der Anzahl der Schlagworte pro Jahr folgt einem ähnlichen Vorgehen wie im letzten Abschnitt zu den verantwortlichen Gewerken. Die Schlagworte sind auf sechs Spalten verteilt (*Schlagwort_1* bis *Schlagwort_6*), die zur weiteren Verabeitung in eine Spalte überführt werden müssen. Für die Visualisierung ist zusätzlich noch die Spalte *Jahr_1* notwendig.

Ausgangspunkt ist der in die Excel-Tabelle importierte [Auswertungs-Datensatz](#import-des-datensatzes-in-excel). Wählen Sie dort im Reiter *Daten* die Option *Aus Tabelle/Bereich* aus. Der *Power Query-Editor* öffnet sich. Gehen Sie im Reiter *Start* auf *Spalten auswählen* und setzten Sie im sich öffnenden Fenster bei den Spalten *Jahr_1* und den Spalten *Schlagwort_1* bis *Schlagwort_6* einen Haken. Beenden Sie die Spaltenauswahl mit *OK*. (Vgl. {numref}`excel_tabelle_bereich` bis {numref}`excel_spalten_gewerk`)

Wählen Sie nun die Spalten *Schlagwort_1* bis *Schlagwort_6* aus, indem Sie in den Spaltentitel klicken und die *Strg-Taste* gedrückt halten. Achten Sie darauf, die Spalte *Jahr_1* nicht mit auszuwählen. Ein Rechtsklick auf einen der markierten Spaltentitel öffnet ein Menü, dort entscheiden Sie sich für die Option *Nur ausgewählte Spalten entpivotieren*. ({numref}`excel_spalten_schlagworte`)

```{figure} ../assets/auswertung/excel_spalten_schlagwort.png
---
align: center
width: 100%
name: excel_spalten_schlagworte
alt: Darstellung Auswahl der Schlagwort-Spalten und Option *Entpiovtieren*. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl der Schlagwort-Spalten und Option *Entpivotieren*
```

Mit einem Klick auf *Schließen & Laden* beenden Sie den *Power Query-Editor*, die neu erstellten Spalten werden zusammen mit der Spalte *Jahr_1* in ein neues Excel-Arbeitsblatt übernommen. (Vgl. {numref}`excel_query_ende`) Benennen Sie die Spalten *Attribut* und *Wert* um, damit diese für eine mögliche spätere Verwendung besser zuordenbar sind, z.B. in *Attribut_Schlagwort* und *Wert_Schlagwort*. Ausgehend von diesem Excel-Arbeitsblatt können Sie mit der Visualisierung der Daten beginnen. Das Vorgehen folgt dabei Schritten, die bereits in den letzten Abschnitten dargestellt wurden.

Klicken Sie auf den ersten Eintrag der Spalte *Jahr_1* und wählen Sie im Reiter *Einfügen* die Option *PivotChart und PivotTabelle* aus. Bestätigen Sie die Eingabe im folgenden Feld und wählen Sie in den *PivotChart-Feldern* die Spalten *Jahr_1* und *Wert_Schlagwort* an. (Vgl. {numref}`excel_pivot_chart` bis {numref}`excel_pivot_felder`) Auf das Feld *Achse (Rubriken)* ziehen Sie den Eintrag *Jahr_1*, auf *Werte* den Eintrag *Anzahl von Wert_Schlagwort* und auf das Feld *Legende (Reihe)* den Eintrag *Wert_Schlagwort*. ({numref}`excel_felder_schlagwort`)

```{figure} ../assets/auswertung/excel_chart_felder_schlagwort.png
---
align: center
width: 50%
name: excel_felder_schlagwort
alt: Darstellung Einträge in die PivotChart-Felder. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Einträge in die PivotChart-Felder
```

Wie bereits bei der Auswertung der verantwortlichen Gewerke ergibt sich hier aufgrund der hohen Anzahl an Schlagworten eine recht unübersichtliche Darstellung. ({numref}`schlagworte_jahr_roh`) Die Grafik sollte also weiter bearbeitet werden.

```{figure} ../assets/auswertung/schlagworte_jahr_roh.png
---
align: center
width: 100%
name: schlagworte_jahr_roh
alt: Darstellung der Visualisierung der Anzahl der Schlagworte pro Jahr
---
Erste Visualisierung der Anzahl der Schlagworte pro Jahr
```

Wie im Kapitel zur Analyse der [Datenquelle](../bereinigung/datenquelle.md#schlagwort-stichworter-zusammenfassung) dargelegt, werden bei der Erfassung der filmografischen Angaben für den Bibliothekskatalog die Gattungen als Schlagworte aufgenommen. Die Anzahl der [Gattungen pro Jahr](#anzahl-der-gattungen-pro-jahr) im Datensatz wurde bereits visualisiert und ausgewertet, die Schlagworte *Spielfilm*, *Dokumentarfilm* und *Animationsfilm* können also bei dieser Auswertung ausgeschlossen werden. Des Weiteren bietet es sich an, sich auf Schlagworte zu konzentrieren, die besonders häufig vorkommen und solche, die für die Forschungsfrage relevant erscheinen. Wählen Sie daher bei der Feldschaltfläche *Wert Schlagwort* in der Grafik zunächst alle Inhalte ab und dann die Schlagworte *Arbeit, Frauen, Porträtfilm* und *Wende* an. (Vgl. {numref}`gewerke_auswahl`) Blenden sie zusätzlich eine Datentabelle ein. (Vgl. {numref}`gattung_jahr_säule_daten_auswahl`) Dadurch ergibt sich bereits eine übersichtlichere Grafik. ({numref}`schlagworte_jahr_auswahl`)

```{figure} ../assets/auswertung/schlagworte_jahr_auswahl.png
---
align: center
width: 100%
name: schlagworte_jahr_auswahl
alt: Darstellung der Anzahl ausgewählter Schlagworte pro Jahr
---
Anzahl ausgewählter Schlagworte pro Jahr
```

Es zeigt sich, dass das Schlagwort *Arbeit* insbesondere 1987, aber auch 1988 und 1989 besonders häufig auftritt und danach fast verschwindet. Dies könnte mit sich verändernden politischen Bedingungen zu tun haben. Zu Zeiten der DDR hatte das Thema Arbeit einen hohen Stellenwert, was sich auch in der Anzahl der Schlagworte bzw. der Themenwahl, die sich in den Schlagworten spiegelt, zum Ausdruck kommen kann. Während der Wendezeit können sich die Themen und damit die Schlagworte zu den studentischen Filmen verändert haben. Für eine genauere Analyse sind jedoch Archiv-Recherchen notwendig, da die Häufung des Schlagwortes *Arbeit* auch mit speziellen Film-Übungen in den ensprechenden Jahren verbunden sein kann.

Um noch tiefer in eine Auswertung einsteigen zu können, soll nun die Darstellung der Jahre noch reduziert werden. Wählen Sie dazu im Dropdown-Menü *Jahr_1* in der Grafik die Jahren *1987 bis 1992* an. (Vgl. {numref}`gewerke_auswahl`)

```{figure} ../assets/auswertung/schlagworte_jahr_auswahl_2.png
---
align: center
width: 100%
name: schlagworte_jahr_auswahl_2
alt: Anzahl ausgewählter Schlagworte pro ausgewählte Jahre
---
Anzahl ausgewählter Schlagworte pro ausgewählte Jahre
```

Aus der Grafik ist ersichtlich, dass das Schlagwort *Wende* – wie zu erwarten war – erst im Jahr 1989 auftritt, im Jahr 1990 seinen Höhepunkt erreicht und ab 1991 wieder abflacht. Hier wäre es interessant, diese Auswertung mit in eine genauerer Recherche im Archiv zu nehmen und sich z.B. gezielt die studentischen Filme anzusehen, die mit dem Schlagwort *Wende* versehen sind. Auch wäre es sinnvoll, im Archiv dem auffallend häufigen Auftreten des Schlagworts *Porträtfilm* in den Jahren 1987 bis 1989 nachzugehen. 

Für eine weitere Auswertung sollte mit der Visualisierung weiterer, unterschiedlicher Schlagwortkombinationen fortgefahren werden. Wiederum ist anzumerken, dass nicht alle Filme mit Schlagworten versehen wurden, die Auswertung der Anzahl der Schlagworte also mit Bedacht vonstatten gehen sollte.

## Darstellung der Schlagworte mit Voyant Tools
Abschließend soll nun darauf eingegangen werden, wie mit *Voyant Tools* Visualisierungen der Schlagworte erstellt werden, die für eine weitere Auswertung hilfreich sein können, z.B. mit den bereits vorgestellten Möglichkeiten mit Excel. *Voyant Tools* ist webbassiert und wurde für die Auswertung größerer Textkoropra entwickelt. An dieser Stelle können wir nur einige grundlegende Funktionen von *Voyant Tools* vorstellen: Wir werden eine *Wortwolke* mit den Schlagworten aus unserem Datenset erzeugen, aus der die Häufigkeit der einzelnen Worte durch die Größe der Darstellung hervorgeht.

Öffnen Sie hierfür das im letzten Abschnitt zur Visualisierung der [Anzahl der Schlagworte pro Jahr](#anzahl-der-schlagworte-pro-jahr) erstellte Excel-Arbeitsblatt, markieren Sie die Spalte *Wert_Schlagwort* und kopieren Sie die Inhalte mit der Tastenkombination *Strg + C* in die Zwischenablage. ({numref}`voyant_schlagworte_excel_copy`)

```{figure} ../assets/auswertung/voyant_schlagwort_copy_excel.PNG
---
align: center
width: 100%
name: voyant_schlagworte_excel_copy
alt: Darstellung Kopieren der Spalte *Wert_Schlagwort* in die Zwischenablage
---
Kopieren der Spalte *Wert_Schlagwort* in die Zwischenablage
```

Gehen Sie nun zur Webseite von <a href="https://voyant-tools.org/?lang=de" class="external-link" target="_blank">Voyant Tools</a>. Fügen Sie in das Feld *Text hinzufügen* den Inhalt der Zwischenablage ein (Tastenkombination *Strg + V*) und klicken sie anschließend auf *Anzeigen*. ({numref}`voyant_eingabe_text`)

```{figure} ../assets/auswertung/voyant_eingabe_text.png
---
align: center
width: 100%
name: voyant_eingabe_text
alt: Darstellung Einfügen der Schlagworte aus der Zwischenablage. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Einfügen der Schlagworte aus der Zwischenablage
```

Die Arbeitsoberfläche von *Voyant Tools* zur Auswertung des eingelesenen Textes wird geföffnet. Setzen Sie in ihrem Browser ein Lesezeichen zu dieser Seite. Ihr Textkorpus – in diesem Fall die Schlagworte aus unserem Datensatz – wird hier gespeichert und kann später unter dieser URL weiter ausgewertet werden. Für jedes Auswertungs-Projekt wird eine einzigartige URL erzeugt.

Die Arbeitsoberfläche von *Voyant Tools* enthält mehrere Fenster, in denen Auswertungen zum eingelesenen Korpus vorgenommen werden können. Wir werden uns auf das Fenster links oben konzentrieren, in dem *Cirrus* aktviert ist. Es enthält bereits eine Wortwolke aus den eingelesenen Schlagworten. Die am häufigsten vorkommenden Worte werden größer dargesellt. 

In der Wortwolke treten *Spielfilm, Dokumentarfilm* und *Animationsfilm* als häufige Worte besonders hervor. ({numref}`voyant_eingabe_start`) Im Kapitel zur Analyse der [Datenquelle](../bereinigung/datenquelle.md#schlagwort-stichworter-zusammenfassung) haben wir bereits darauf hingeweisen, dass diese Gattungen ebenfalls in den Schlagworten erfasst werden. Für eine weitere Auswertung möchten wir die Gattungsbezeichnungen von der Visualisierung ausnehmen. Zeigen Sie hierfür mit der Maus in die Zeile, in der *Cirrus* über der Wortwolke aufgeführt wird. Bei den erscheinenden Eingabemöglichkeiten klicken Sie auf den Button neben dem Fragezeichen, für den *Optionen für dieses Tool definieren* angezeigt wird.

```{figure} ../assets/auswertung/voyant_start_eingabe.png
---
align: center
width: 100%
name: voyant_eingabe_start
alt: Darstellung Eingabeoptionen in Voyant Tools definieren. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Eingabeoptionen in Voyant Tools definieren
```

Im sich öffnenden Optionen-Eingabefenster wählen Sie in der Zeile *Stopwords* den Punkt *Liste bearbeiten*. ({numref}`voyant_eingabe_option`)

```{figure} ../assets/auswertung/voyant_eingabe_optionen.png
---
align: center
width: 50%
name: voyant_eingabe_option
alt: Darstellung Eingabeoption Liste bearbeiten. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Eingabeoption *Liste bearbeiten*
```

Es öffnet sich eine vordefinierte Liste mit *Stopwords*, die Worte enthält, die nicht in eine Auswertung eines Textkorpus mit *Voyant Tools* einfließen sollen. Dies sind Worte wie Artikel oder ausgeschriebene Zahlen, die häufig in Texten vorkommen, aber z.B. für Visualisierung hinderlich sind. Dieser Liste fügen Sie *Dokumentarfilm*, *Spielfilm* und *Animationsfilm* hinzu. Beenden Sie die Eingabe mit *Speichern*. ({numref}`voyant_eingabe_stopword`) Sie gelangen zurück zum Optionen Eingabefenster, wählen sie dort *Bestätigen* aus.

```{figure} ../assets/auswertung/voyant_eingabe_stopword.png
---
align: center
width: 50%
name: voyant_eingabe_stopword
alt: Darstellung Eingabe zusätzlicher Stopwords. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Eingabe zusätzlicher Stopwords
```

Im linken oberen Fenster ist eine neue Wortwolke entstanden, die die Schlagworte *Spielfilm*, *Dokumentarfilm* und *Animationsfilm* nicht mehr enthält. An der Größe der Darstellung der Worte ist erkennbar, dass die Schlagworte *Adaption, Porträtfilm, Wende, Arbeit* und *Frauen* besonders häufig im Textkorpus der Schlagworte vorkommen. ({numref}`voyant_wortwolke_regler`) Wenn Sie mit dem Mauszeiger über die entsprechenden Schlagworte fahren, wird die Anzahl der Nennungen im Korpus angezeigt, die der Anzahl der Einträge in unserem synthetischen Datensatz entspricht.

```{figure} ../assets/auswertung/voyant_wortwolke_regler.png
---
align: center
width: 100%
name: voyant_wortwolke_regler
alt: Darstellung Wortwolke zu Schlagworten mit Regler für die Anzahl der Begriffe. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Wortwolke zu Schlagworten mit Regler für die Anzahl der Begriffe
```

Links unter der Wortwolke finden Sie einen Regler, mit dem die Anzahl der in die Visualisierung in Form einer Wortwolke einbezogenen Begriffe verändert werden kann. Experimentieren Sie mit der Anzahl der Begriffe. Stellen Sie ihn z.B. auf das Maximum ein. ({numref}`voyant_wortwolke_regler_max`)

```{figure} ../assets/auswertung/voyant_wortwolke_regler_max.png
---
align: center
width: 100%
name: voyant_wortwolke_regler_max
alt: Darstellung Wortwolke zu Schlagworten mit maximaler Anzahl der Begriffe. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Wortwolke zu Schlagworten mit maximaler Anzahl der Begriffe
```

Auch in dieser Darstellung werden die bereits genannten Begriffe besonders groß dargestellt, es treten aber auch weitere Schlagworte wie *Satire* (mit 10 Nennungen), *Komödie* (ebenfalls 10 Nennungen) oder *Krankheit* (5 Nennungen) hervor. Mit diesen und weiteren in der Wortwolke erkennbaren Schlagworten kann in weiteren Visualisierungen mit Excel experimentiert werden, wie sie im vorigen Abschnitt erläutert wurden.

In der Kopfzeile über der Wortwolke gibt es die Möglichkeit, die Wortwolke als png- oder svg-Datei zu exportieren. Die Exportfunktion erscheint, wenn Sie mit der Maus in die Kopfzeile deuten.

*Voyant Tools* bietet zahlreiche weitere Auswertungsmöglichkeiten, auf die wir hier nicht genauer eingehen können. Experimentieren Sie mit den verschiedenen Tools. Sie könnten z.B. für die Auswertung von Inhaltsbeschreibungen zu den studentischen Filmen aus dem Archiv hilfreich sein, oder auch von Rezensionen zu den Filmen.

## Fazit
In diesem Kapitel haben wir Möglichkeiten der Visualisierung und Auswertung unseres (synthetischen) Datensatzes aufgezeigt, die für die Beantwortung der in der Fallstudie entwickelten Fragestellungen nützlich sein können. Für die Visualisierungen haben wir *Microsoft Excel* und abschließend *Voyant Tools* verwendet, die leicht zugänglich sind. 

Es hat sich gezeigt, dass durch Visualisierungen eine explorative Auswertung des Datensatzes möglich ist. Es wurde u.a. deutlich, dass Ende der 1980er Jahre die Anzahl der Titel im Datensatz ansteigt, verstärkt dokumentarische Formen entstanden sind und die Anzahl bestimmter Projektarten größer wird. Diese Auswertungen und Visualisierungen können eine gute Grundlage für weitere Recherchen im Filmarchiv der Filmuniversität und weiteren Archiven bilden.

Dabei muss im Blick behalten werden, dass im Datensatz nicht alle Angaben vollständig enthalten sind. So werden Gattungen oder Projektakrten nicht immer in die filmografischen Angaben im Archivkatalog aufgenommen. Die erstellten Visualisierungen und die Datengrundlage, auf der sie basieren, müssen also immer kritisch hinterfragt werden. Dennoch bieten sie gute und hilfreiche Ausgangspunkte für die weitere Arbeit an den Fragestellungen.
