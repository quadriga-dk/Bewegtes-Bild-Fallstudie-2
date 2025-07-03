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

Im Folgenden stellen wir nun exemplarisch einige mögliche Vorgehensweisen für die Visualisierung und Auswertung unseres synthetischen Datensatzes dar. Ausgangspunkt sind dabei die vorher erarbeiteten Teilfragestellungen. Die verwendeten Screenshots stammen dabei aus der Excel-Arbeitsoberfläche.

## Import des Datensatzes in Excel
Der synthetische Datensatz liegt, wie ursprünglich der originale bereinigte Datensatz, als *tsv*-Datei vor. In diesem Format wurden die Daten nach der Bereinigung aus *OpenRefine* exportiert. Dieser Datensatz muss nun für die Visualisierungen und Auswertungen in Excel importiert werden.

Ausgangspunkt für den Import in Excel ist die Datei **Synthetischer_Datensatz_Auswertung_OER.tsv**. Sie können den Datensatz [hier](../assets/daten/Synthetischer_Datensatz_Auswertung_OER.tsv) (rechte Maustaste und *Ziel speichern unter* auswählen) herunterladen. Die tsv-Datei weist vor dem eigentlichen Datensatz eine Zeile mit dem Hinweis auf, dass es sich um einen synthetischen Datensatz für Unterrichtszwecke handelt, der keine personenbezogene Daten enthält. Diese erste Zeile muss vom Import ausgeschlossen werden. Nur dann werden die Daten mit den korrekten Spaltennamen richtig in die Datei übernommen. Hierfür sind folgende Excel-Einstellungen notwendig.

Öffnen Sie Excel mit einer leeren Arbeitsmappe. Gehen Sie im Reiter *Datei* auf *Optionen* und im sich öffnenden Optionen-Fenster auf den Punkt *Daten*. Wählen Sie dort unter *Legacy-Datenimport-Assistenten anzeigen* das Kästchen *Aus Text (Legacy)* an. Bestätigen Sie die Auswahl mit *OK*. ({numref}`excel_optionen`)

```{figure} ../assets/auswertung/excel_optionen.png
---
align: center
width: 100%
name: excel_optionen
alt: Darstellung der Einstellungen in Optionen für den Datenimport in Excel. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Einstellungen in Optionen für den Datenimport in Excel
```

Gehen Sie nun auf den Reiter *Daten* und dort auf *Daten abrufen*. Unter *Legacy-Assistenten* klicken Sie auf *Aus Text (Legacy)*. ({numref}`excel_legacy`)

```{figure} ../assets/auswertung/excel_legacy_assistent_text.png
---
align: center
width: 100%
name: excel_legacy
alt: Darstellung der Schritte zum Starten des Text-Legacy-Assistenten. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Starten des Text-Legacy-Assistenten
```

Im Datei-Import Fenster navigieren Sie zum Speicherort der Datei *Synthetischer_Datensatz_Auswertung_OER.tsv* auf Ihrem Computer. Achten Sie darauf, dass rechts unten *Alle Dateien* ausgewählt ist, da ansonsten die tsv-Datei nicht angezeigt wird. Bestätigen sie die Auswahl mit *Importieren*. ({numref}`excel_dateiimport`)

```{figure} ../assets/auswertung/excel_textdatei_importieren.png
---
align: center
width: 100%
name: excel_dateiimport
alt: Darstellung der Auswahl der Import-Datei. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Auswahl der Import-Datei
```

Im ersten Schritt des Textkonvertierungs-Assistenten ist unter Datentyp der Punkt *Getrennt* (also mit Tabulatoren getrennt) bereits korrekt ausgewählt und kann so übernommen werden. *Import beginnen in Zeile* stellen Sie von *1* auf *2* ein, da beim Import ja die erste Zeile mit dem Hinweis auf die Übungsdatei übersprungen werden soll. Für *Dateiursprung* wählen Sie *65001 : Unicode (UTF-8)* aus - dies ist die Zeichen-Codierung, die beim Export aus *OpenRefine* verwendet wurde. Rufen Sie den zweiten Schritt durch Klick auf *Weiter* auf. ({numref}`excel_assistent_1`)

```{figure} ../assets/auswertung/excel_texkonvertierungsassistent_1.png
---
align: center
width: 100%
name: excel_assistent_1
alt: Darstellung des Textkonvertierungs-Assistenten - Schritt 1. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Textkonvertierungs-Assistent - Schritt 1
```

Im zweiten Schritt des Assistenten wird *Tabstopp* als *Trennzeichen* korrekt erkannt und kann mit *Weiter* übernommen werden. ({numref}`excel_assistent_2`)

```{figure} ../assets/auswertung/excel_texkonvertierungsassistent_2.png
---
align: center
width: 100%
name: excel_assistent_2
alt: Darstellung des Textkonvertierungs-Assistenten - Schritt 2. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Textkonvertierungs-Assistent - Schritt 2
```

Auch im dritten Schritt des Assistenten kann die Einstellung *Datenformat der Spalten* -> *Standard* beibehalten werden. Schließen Sie den Textkonvertierungs-Assistenten mit *Fertig stellen* ab. ({numref}`excel_assistent_3`)

```{figure} ../assets/auswertung/excel_texkonvertierungsassistent_3.png
---
align: center
width: 100%
name: excel_assistent_3
alt: Darstellung des Textkonvertierungs-Assistenten - Schritt 3. Die Auswahlfelder sind mit roten Kreisen gekennzeichnet.
---
Textkonvertierungs-Assistent - Schritt 3
```

Sie können nun den Ort in der Excel-Arbeitsmappe auswählen, an dem der Import durchgeführt werden soll. Auch hier können sie die Vorgabe *Bestehendes Arbeitsblatt* übernehmen und die Daten mit einem Klick auf *OK* aus der tsv-Datei in Excel importieren. ({numref}`excel_import_ort`)

```{figure} ../assets/auswertung/excel_import_ort.png
---
align: center
width: 100%
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
alt: Darstellung der Excel Arbeitsoberfläche. der Reiter Einfügen und die Auswahlmöglichkeiten PivotChart und Tabelle sind durch rote Kreise markiert.
---
Auswahl *PivotChart und PivotTabelle" im Reiter *Einfügen*.
```

Es öffnet sich ein Fenster *PivotTabelle erstellen*. Die Einstellungen können sie unverändert übernehmen und mit OK bestätigen. ({numref}`excel_pivot_tabelle`)

```{figure} ../assets/auswertung/excel_pivot_einfuegen_erstellen.PNG
---
align: left
width: 100%
align: center
name: excel_pivot_tabelle
alt: Darstellung des Fensters PivotTabelle erstellen. Die Schaltfläche OK ist mit einem roten Kreis gekennzeichnet.
---
Das Fenster *Fensters PivotTabelle erstellen*.
```

Es öffnet sich eine Excel-Arbeitsoberfläche. Auf der linken Seite wird eine leere PivotTabelle angezeigt, in der Mitte ein leeres PivotChart und auf der rechten Seite sind PivotChart-Eingabefelder sichtbar, die noch nicht ausgefüllt sind. ({numref}`excel_pivot_screen`)

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
width: 100%
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

Das Vorgehen ist zunächst gleich wie bei der Darstellung der Titel pro Jahr. Wählen Sie im Reiter *Einfügen* den Punkt *PivotChart und PivotTable* aus. In den *PivotChart-Feldern* auf der rechten Seite der Oberfläche wählen sie dieses Mal jedoch nicht *Titel* und *Jahr_1*, sondern *Gattung* und *Jahr_1* aus. (siehe {numref}`excel_pivot_chart` bis {numref}`excel_pivot_felder`). Die angewählten Spalten werden wieder automatisch den PivotChart-Feldern *Achse (Rubriken)* und *Werte* zugeordnet. ({numref}`gattung_jahr_felder1`)

```{figure} ../assets/auswertung/gattung_jahr_felder_auswahl_1.png
---
align: center
width: 100%
name: gattung_jahr_felder1
alt: Darstellung der Auswahl PivotChart-Felder *Gattung* und "Jahr_1*. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Auswahl PivotChart-Felder *Gattung* und "Jahr_1*
```

Aus diesen automatisch ausgewählten Einträge in die Felder ergibt sich jedoch keine sinnvolle visuelle Darstellung der Daten in der Excel-Arbeitsoberfläche. Die Eingaben müssen angepasst und durch Anklicken und Ziehen in die richtigen Felder gebracht werden: Im Feld *Achse (Rubriken)* steht nun *Jahr_1*, im Feld *Werte* die *Anzahl von Gattungen* und im Feld *Legende (Reihe)* ist der Wert *Gattung* eingetragen. *Gattung* wird durch Anklicken in der oberen Liste und Ziehen in das Feld *Legende (Reihe)* gebracht. ({numref}`gattung_jahr_felder2`)

```{figure} ../assets/auswertung/gattung_jahr_felder_auswahl_2.png
---
align: center
width: 100%
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

In diese Darstellung kann zusätzlich noch eine Datentabelle eingeblendet werden. Hierfür klicken Sie auf das grüne Pluszeichen neben dem Diagramm in der Excel-Arbeitsoberfläche. Wählen Sie dann im Kontextmenü den Punkt *Datentabelle* zusätzlich an. ({numref}`gattung_jahr_säule_daten_auswahl`)

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

Insgesamt sind die Daten zu den Gattungen und damit auch ihre visuellen Darstellung jedoch mit Vorsicht zu betrachten. Wie im Kapitel zur Analyse der [Datenquelle](/bereinigung/datenquelle.md) dargelegt wurde, sind nicht alle Filmtitel mit Angaben zu ihrer jeweiligen Gattung versehen. Viele Titel sind hinsichtlich ihrer Zugehörigkeit zu Spielfilm, Dokumentarfilm oder Animationsfilm nicht klassifiziert. Hier ist also eine genauere Recherche im Archiv unumgänglich. Dennoch können wir die visuelle Auswertung der Daten mit in diese Recherche nehmen - z.B. indem wir überprüfen, wieviele Dokmentarfilme in den Jahren 1987 bis 1999 im Filmarchiv der Filmuniversität vorhanden sind. Diese Recherche kann dann mit den bereits vorhandenen Daten und deren visuellen Darstellung abgeglichen werden.

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
width: 100%
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
width: 100%
name: projektart_auswahl_2
alt: Darstellung der Einträge in den Feldern. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Einträge in den Feldern
```

In der Excel-Arbeitsoberfläche sehen Sie nun das Säulendiagramm mit allen Projektarten. Grenzen Sie die angezeigten Projektarten ein, indem Sie auf das grüne Kreuz neben dem Diagramm klicken. Wählen Sie im Kontextmenü die Projektarten *Abschlußfilm*, *Diplomfilm*, *Hauptprüfungsfilm* und  *Vordiplomfilm* aus und bestätigen Sie die Eingabe mit *OK*. ({numref}`projektart_eingrenzung`)

```{figure} ../assets/auswertung/projektart_jahr_eingrenzung.png
---
align: center
width: 100%
name: projektart_eingrenzung
alt: Darstellung der Eingrezung der angezeigten Projektarten. Einzelne Eingaben sind mit roten Kreisen gekennzeichnet.
---
Eingrezung der angezeigten Projektarten
```

Fügen Sie einen Diagrammtitel hinzu. Abschließend wählen Sie im Menü *Analysieren* den Punkt den Punkt *Feldschaltflächen -> alle ausblenden* aus. (vgl. {numref}`titel_jahr_ausblenden`) Sie haben nun ein Säulendiagramm mit den Projektarten *Abschlußfilm*, *Diplomfilm*, *Hauptprüfungsfilm* und  *Vordiplomfilm* pro Jahr erstellt. Dieses können Sie per Copy & Paste in andere Programme einbinden.

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
