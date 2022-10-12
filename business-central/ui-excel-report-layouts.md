---
title: Arbeiten mit Excel-Layouts
description: Erfahren Sie, wie Sie mit Excel erstellte Berichtslayouts erstellen und ändern.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/14/2022
ms.author: jswymer
ms.openlocfilehash: 45f321afeb411eee4cb9f9dd215cefc393f58458
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529583"
---
# <a name="working-with-excel-layouts"></a>Arbeiten mit Excel-Layouts

Excel-Berichtslayouts basieren auf Microsoft Excel-Arbeitsmappen (.xlsx-Dateien). Damit können Sie Berichte erstellen, indem Sie vertraute Excel-Funktionen zum Zusammenfassen, Analysieren und Präsentieren von Daten wie Formeln, PivotTables und PivotCharts verwenden.

![Zeigt ein Beispiel für ein Excel-Layout.](media/excel-layout-2.png)

In diesem Artikel werden einige der wichtigsten Dinge erläutert, die Sie wissen müssen, um mit Excel-Layouts zu beginnen.

## <a name="why-use-excel-layouts"></a>Gründe für die Verwendung von Excel-Layouts

Hier sind einige weitere Vorteile der Verwendung von Excel-Layouts:

- Interaktive Berichte mit Visualisierungen wie Slicern erstellen
- Rohdaten aus dem Berichtsdataset anzeigen, um besser zu verstehen, wie der Bericht funktioniert und woher die Daten zu visuellen Elementen stammen
- Integrierte Office-Funktionen verwenden, um gerenderte Berichte nachzubearbeiten, z. B.:
  - [Schutz der Arbeitsblätter](https://support.microsoft.com/en-us/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Anwenden von Vertraulichkeitsbezeichnungen](https://support.microsoft.com/en-us/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Hinzufügen von Kommentaren und Notizen](https://support.microsoft.com/en-us/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Prognose und Analyse](https://support.microsoft.com/en-us/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4) 
- Verwenden Sie installierte Add-Ins und App-Integrationen wie Power Automate-Flows oder OneDrive.

## <a name="get-started"></a>Erste Schritte

Es müssen im Wesentlichen zwei Aufgaben erledigt werden, um ein Excel-Layout in einem Bericht einzurichten:

1. Erstellen Sie die neue Excel-Layoutdatei.
2. Fügen Sie dem Bericht das neue Layout hinzu.

## <a name="task-1-create-the-excel-layout-file"></a>Aufgabe 1: Erstellen der Excel-Layoutdatei

Wie in diesem Abschnitt erläutert, gibt es drei Möglichkeiten, eine Excel-Layoutdatei für einen Bericht zu erstellen

### <a name="from-any-report"></a>[Aus einem beliebigen Bericht](#tab/any-report)

Sie können die folgenden Schritte verwenden, um ein Excel-Layout aus einem beliebigen Bericht zu erstellen, unabhängig vom aktuellen Layouttyp. Das Excel-Layout enthält das erforderliche **Daten**-Blatt und die notwendige Tabelle, ein **Metadaten melden**-Blatt und sonst nichts.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. In der **Berichtslayouts**-Liste wählen Sie ein beliebiges Layout für den Bericht wählen dann die **Bericht ausführen**-Aktion aus.
3. Wählen Sie auf der Berichtsanforderungsseite **Senden an** > **Microsoft Excel-Dokument (nur Daten)** > **OK** aus.

   In diesem Schritt wird eine Excel-Arbeitsmappe heruntergeladen, die das Berichtsdataset enthält.
4. Öffnen Sie die heruntergeladene Datei in Excel, nehmen Sie die Änderungen vor und speichern Sie die Datei.

### <a name="from-another-excel-layout-on-a-report"></a>[Aus einem anderen Excel-Layout in einem Bericht](#tab/other-layout)

Wenn für einen Bericht bereits ein Excel-Layout vorhanden ist, verwenden Sie das vorhandene Layout als Ausgangspunkt. Es gibt zwei Ansätze, um eine Kopie des Layouts zu erhalten. Sie können das vorhandene Layout aus der **Berichtslayouts**-Seite exportieren oder laden das Layout von der Anforderungsseite des Berichts herunterladen. Bei beiden Möglichkeiten wird eine Excel-Layoutdatei heruntergeladen, die alle Blätter der vorhandenen Datei enthält. Der Unterschied besteht darin, dass das Layout der Anforderungsseite tatsächliche Daten enthält. Die Daten sind nicht erforderlich, aber sie helfen bei der Gestaltung des Layouts.

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Ansatz 1: Exportieren des Layouts aus der **Berichtslayouts**-Seite

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Wählen Sie das Excel-Layout aus der Liste und dann die **Layout exportieren**-Aktion oben auf der Seite aus.
3. Öffnen Sie die Datei in Excel, nehmen Sie die Änderungen vor und speichern Sie die Datei.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Ansatz 2: Das Layout von der Anforderungsseite des Berichts herunterladen

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. In der **Berichtslayouts**-Liste wählen Sie ein beliebiges Layout für den Bericht wählen dann die **Bericht ausführen**-Aktion aus.
3. Wählen Sie auf der Berichtsanforderungsseite **Herunterladen** aus.
4. Öffnen Sie die Datei in Excel, nehmen Sie die Änderungen vor und speichern Sie die Datei.

### <a name="from-al-code"></a>[Aus AL-Code](#tab/from-code)

Diese Methode ist am weitesten fortgeschritten. Sie erfordert Kenntnisse des AL-Codes und richtet sich daher an Programmierer. Die Excel-Layouts sind in diesem Fall Teil eines Erweiterungspakets, das Sie installieren. Weitere Informationen finden Sie unter [Erstellen eines Excel-Layoutberichts](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) in der Hilfe für Entwickler und IT Pro.

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a>Aufgabe 2: Den Excel-Layout dem Bericht hinzufügen

Sobald Sie die Excel-Layoutdatei haben, besteht die nächste Aufgabe darin, sie als neues Layout für den Bericht hinzuzufügen.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Wählen Sie **Neues Layout** aus.
3. Legen Sie die **Berichts-ID** auf Bericht fest.
4. Geben Sie einen Namen in **Layout-Name** ein.
5. Legen Sie **Formatoptionen** auf **Excel** fest.
6. Wählen Sie **OK** > **Auswählen** fest, um den Datei-Explorer auf Ihrem Gerät zu öffnen. 
7. Suchen Sie die Excel-Datei und wählen Sie sie aus. Wählen Sie dann **Öffnen** aus.

   Die ausgewählte Datei wird in das Layout hochgeladen und Sie kehren zur **Berichtslayouts**-Seite zurück.
8. Wenn Sie sehen möchten, wie der Bericht mit dem neuen Layout aussieht, wählen Sie das Layout in der Liste und dann **Bericht ausführen** aus.


<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet can only include one table named **Data**.

**Data** table
  - The **Data** sheet must include a table that has the name **Data**.
  - The table must have at least one column and can only include columns that are also in report dataset.
  - The table must start in the first cell A1 of the **Data** sheet.

3. Report Metadata 
-->

## <a name="understanding-excel-layouts"></a>Grundlagen von Excel-Layouts

Es gibt einige Dinge, die Sie wissen oder berücksichtigen sollten, wenn Sie mit dem Erstellen oder Ändern von Excel-Layouts beginnen. Jedes Excel-Layout muss zwei Elemente enthalten: ein **Daten**-Blatt und eine **Daten**-Tabelle. Diese Elemente bilden die Grundlage des Layouts, indem Sie die Geschäftsdaten aus Business Central definieren, mit denen Sie arbeiten können. Sie können sich das **Daten**-Blatt als eine Art Vertrag zwischen dem Layout in den Geschäftsdaten vorstellen. Sie verwenden diese Daten als Quelle für Berechnungen und Visualisierungen, die Sie auf anderen Blättern präsentieren möchten.

Es gibt einige spezifische Anforderungen an die Struktur der Excel-Arbeitsmappe. Wenn die Anforderungen nicht erfüllt sind, werden Sie Probleme haben, das Layout zu verwenden. Das folgende Diagramm und die Tabelle skizzieren die Elemente eines Excel-Layouts und die Anforderungen.

[![Zeigt die unterschiedlichen Elemente eines Excel-Layouts.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Nr.|Element|Beschreibung|Notwendig|
|---|-------|----|---|
|1|**Daten**-Blatt|<ul><li>Muss den Namen **Daten** haben</li><li>Kann nur eine Tabelle enthalten, und die Tabelle muss den Namen **Daten** haben</li></ul>|![Ist notwendig](media/check.png) | 
|2|**Daten**-Tabelle|<ul><li>Muss den Namen **Daten** haben</li><li>Muss mindestens eine Spalte haben.</li><li>Kann nur Spalten einschliessen, die sich im Berichtsdatensatz befinden.</li><li>Muss in der ersten Zelle **A1** des **Daten**-Blatts beginnen</li></ul>|![Ist notwendig](media/check.png)|
|3|Präsentationsblätter|<ul><li>Werden verwendet, um Daten zu präsentieren.</li><li>Daten stammen aus dem **Daten**-Blatt. </li></ul>||
|4|**Metadaten melden**-Blatt|<ul><li>Wird automatisch eingefügt, wenn das Layout durch Exportieren eines anderen Berichts als Excel erstellt wurde</li><li>Enthält allgemeine Informationen zum Bericht</li><li>Kann gelöscht werden</li></ul>|

Zusammenfassung: Möglichkeiten des **Daten**-Blatts:

- Ändern Sie nicht die Namen von **Daten**-Blatt, **Daten**-Tabelle oder Spalten.
- Sie können Spalten löschen oder ausblenden.
- Fügen Sie keine Spalten hinzu, es sei denn, sie sind im Berichtsdatensatz enthalten.
- Sie können die Blätter in beliebiger Reihenfolge platzieren. Zum Beispiel kann das **Daten**-Blatt das erste oder letzte sein.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Ändern Sie das aktuelle Berichtslayout](ui-how-change-layout-currently-used-report.md)  
[Importieren und Exportieren eines benutzerdefinierten Berichts- oder Beleglayouts](ui-how-import-and-export-report-layout.md)  
[Arbeiten mit Berichten, Stapelverarbeitungen und XMLports](ui-work-report.md)  
[Bereiten Sie Finanzberichte mit Kontenschema und Kontengruppen vor](bi-how-work-account-schedule.md)  
[Business Intelligence](bi.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analysieren von Berichtsdaten mit Excel](report-analyze-excel.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]