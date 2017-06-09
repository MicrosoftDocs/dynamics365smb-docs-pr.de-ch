---
title: Power BI Berichte in der Listenansicht in Dynamics 365 for Financials nutzen | Microsoft Docs
description: "Sie können Power BI Berichte hinzufügen, die zusätzliche Einblick in Daten in Listen in Financials geben."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 02/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 3c58c71a9ebc3df4e55202f50e856a715d64854f
ms.contentlocale: de-ch
ms.lasthandoff: 05/04/2017


---
# <a name="using-power-bi-reports-in-your-list-views-in-dynamics-365-for-financials"></a>Power BI Berichte in der Listenansicht in Dynamics 365 for Financials nutzen
[!INCLUDE[d365fin](includes/d365fin_md.md)] enthält einen Infoboxregler in mehreren Schlüssellistenseiten, die zusätzliche Einblick in die Daten in dieser Liste bereitstellen. Während Sie sich zwischen den Zeilen in der Liste bewegen, wird der Bericht für den Eintrag gefiltert und aktualisiert. Sie können benutzerdefinierte Berichte erstellen, aber es gibt einige Regeln, die Sie beim Erstellen der Berichte befolgen müssen, um sicherzustellen, dass das gewünschte Verhalten geliefert wird.  

**Hinweis**: Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Power BI haben. Zudem müssen Sie [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) herunterladen. Weitere Informationen finden Sie unter[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power BI Datenquelle] (across-how-use-financials-data-source-powerbi.md)  

## <a name="report-data-set"></a>Bericht Dataset
Wenn Sie den Bericht in Power BI Desktop erstellen, definieren Sie die Datenquelle oder den Webdienst, der die Daten enthält, die in der Liste verknüpft sind, den Sie im Bericht zuordnen möchten. Wenn Sie beispielsweise einen Bericht für die Verkaufsliste erstellen möchten, stellen Sie sicher, dass das Dataset Informationen zu den entsprechenden Verkäufen enthält.  

Um Daten in Berichten zu filtern, basierend auf dem ausgewählten Datensatz der Listenseite, muss der primäre Schlüssel als Berichtsfilter verwendet werden. Die Primärschlüssel müssen Teil des Datasets sein, um die Berichte korrekt zu filtern. In den meisten Fällen ist der Primärschlüssel für eine Liste **Nr.** Feld  

## <a name="defining-the-report-filter"></a>Definiert den Berichts-Filter
Der Bericht wird benötigt, um einen grundlegenden Berichtsfilter (kein Seiten- oder visueller Filter und kein erweiterter Filter), um Filter in der Power BI  ein Sichtfilter und keinen gewechselten Filter) haben z in der Energie BI Infosteuerung korrekt anzuzeigen. Der Filter, der zum Power BI Bericht von jeder Listenseite übergeben wird, basiert auf dem Primärschlüssel, wie im vorherigen Abschnitt erläutert.  

Um einen Filter für den Bericht zu definieren, wählen Sie den Primärschlüssel aus der Liste der verfügbaren Felder und ziehen dann das Feld in den Abschnitt **Berichts-Filter**.  

![Den Berichtfilter für den Verkaufsrechnungs-Tätigkeitsbericht festlegen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="report-size-and-color"></a>Meldet Größe und Farbe
Die Größe des Berichts muss auf 325 Pixel auf 310 Pixel festgelegt werden. Dies ist für die Skalierung des Berichts im verfügbaren Platz erforderlich, der von der Power BI Infosteuerung zugelassen wird. Um die Grösse des Berichts zu definieren, den Fokus ausserhalb des Berichts im Berichtslayoutbereich zu platzieren und um das Farbenrollensymbol zu wählen.

![Den Berichtfilter für die Breite und die Höhe des Verkaufsrechnungs-Tätigkeitsbericht festlegen](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

Sie können die Breite und die Tiefe des Berichts ändern, indem Sie im Feld **Benutzerdefiniert** **Art** auswählen.

Wenn Sie möchten, dass der Hintergrund des Bericht sich mit der Hintergrundfarbe der Power BI Infofaktenbox vermischt, definieren Sie eine benutzerdefinierte Hintergrundfarbe*E5E5E5*. Diese Angabe ist optional.  

## <a name="reports-with-multiple-pages"></a>Berichte mit mehrere Seiten
Mit Power BI können Sie einen Bericht mit einer oder mehreren Seiten erstellen. Die grafischen Elemente, die Sie in den  [!INCLUDE[d365fin](includes/d365fin_md.md)] Listenseiten einsehen möchten, müssen auf der ersten Seite des Berichts in Power BI sein.  

**Hinweis:** Die Power BI Fakten-Infobox kann nur die ersten Seite des Berichts anzeigen; wenn Sie andere Seiten anzeigen möchten, müssen Sie die Registerkarten im unteren Bereich des Berichts erweitern, um zu anderen Seiten zu navigieren.  

## <a name="saving-your-report"></a>Ihren Bericht speichern

Wenn Sie Ihren Bericht speichern, ist es üblich, dass der Name des Berichts den Namen der Liste enthält, die Sie im Bericht anzeigen möchten. Beispielsweise muss das Wort *Kreditor* im Namen des Berichts erscheinen, die Sie auf der Kreditorenliste zur Verfügung stellen möchten.  

Dies ist keine Anforderung; es macht aber den Prozess zur Auswahl der Berichte schneller. Wenn die Berichts-Auswahlseite in einer Listenseite geöffnet ist, werden sie in einen Filter basierend auf dem Seitennamen bereitgestellt, um die Anzahl der angezeigten Bericht zu begrenzen.  Sie können den Filter entfernen, um eine vollständige Liste von Berichten zu erhalten, die in Power BI verfügbar sind.  

## <a name="troubleshooting"></a>Problembehebung
Dieser Abschnitt bietet eine Problemumgehung für die typischsten Probleme, die auftreten können, wenn Sie den Power BI Bericht erstellen.  

**Benutzer sieht keinen Bericht auf der ausgewählten Berichtseite** Wenn Sie keinen Bericht auswählen können, ist eine mögliche Lösung, den Namen des Berichts zu prüfen, um sicherzustellen, dass es den Namen der Seite enthält. Sie können den Filter entfernen, um eine vollständige Liste von Berichten zu erhalten, die in Power BI verfügbar sind.  

**Bericht wird geladen ist aber leer, nicht gefiltert oder falsch gefiltert** Prüfen Sie, dass der Berichtsfilter den korrekten Primärschlüssel enthält. In den meisten Fällen ist dies das **Nr.** Feld, aber in der Tabelle **Sachposten** z.B. verwenden Sie das **Lfd. Nr.** Feld.

**Bericht wird gebucht, aber er zeigt die Seite an, die Sie nicht erwartet haben** Überprüfen Sie, ob die Seite, die angezeigt werden sollen, die ersten Seite in Ihren Bericht ist.  

**Bericht erscheint mit unerwünschten grauen Rändern, ist zu klein oder zu umfangreich**

Vergewissern Sie sich, dass die Berichtsgröße auf 325 Pixel x 310 Pixel festgelegt wird. Speichern Sie den Bericht, und aktualisieren Sie anschliessend die Listenseite.  

## <a name="see-also"></a>Siehe auch
[Verwenden Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power BI Datenquelle] (across-how-use-financials-data-source-powerbi.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)    
[Einrichten von [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)    
[Finanzen](finance.md)  

