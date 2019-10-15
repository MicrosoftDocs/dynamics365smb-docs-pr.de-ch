---
title: 'Vorgehensweise: Ändern von Planungsvorschlägen in einer grafischen Ansich| Microsoft Docst'
description: Eine typische Planungsaktivität besteht darin, Planungsvorschlagszeilen zu ändern oder hinzuzufügen, um die vorgeschlagenen Beschaffungsaufträge zu ändern, bevor Sie diese kommissionieren, indem Sie die Funktion **Ereignismeldung durchführen** ausführen. Eine Alternative zur Durchführung im Planungsvorschlag ist die Verwendung einer grafischen Ansicht.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3aea6aa1aab6b5006bdc548b99bfa037e995de32
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313386"
---
# <a name="modify-planning-suggestions-in-a-graphical-view"></a>Ändern von Planungsvorschlägen in einer grafischen Ansicht
Eine typische Planungsaktivität besteht darin, Planungsvorschlagszeilen zu ändern oder hinzuzufügen, um die vorgeschlagenen Beschaffungsaufträge zu ändern, bevor Sie diese kommissionieren, indem Sie die Funktion **Ereignismeldung durchführen** ausführen. Eine Alternative zur Durchführung im Planungsvorschlag ist die Verwendung einer grafischen Ansicht.

Auf der Seite **Artikelverfügbarkeit nach Zeitachse** können Sie gewisse Beschaffungsaufträge und Planungsvorschläge ändern, indem Sie Elemente entlang der X-Achse ziehen, um die Menge zu ändern oder entlang der Y-Achse, um das Fälligkeitsdatum zu ändern.  

 Auf der Seite **Artikelverfügbarkeit nach Zeitachse** und auf der Seite **Planungsvorschlag** können Sie folgende Änderungen vornehmen:  

-   Ändern eines vorgeschlagenen Lieferauftrags, der nur als Planungszeile vorhanden ist.  
-   Ändern eines vorhandenen Beschaffungsauftrags, den das Planungssystem für eine Änderung vorschlägt.  
-   Erstellen und Ändern eines neuen vorgeschlagenen Beschaffungsauftrags.  

Weitere Informationen zu den gezeigten Planungszeilentypen finden Sie im Feld Beschreibung im Inforegister **Ereignisänderungen**.  

Wenn Sie **Änderungen speichern** auf der Seite **Artikelverfügbarkeit nach Zeitachse** auswählen, werden die Änderungen, die Sie durchgeführt haben, in den Planungs- oder Bestellvorschlag kopiert. Sie können sie jetzt mithilfe des **Carry Out Action Msg. Plan.** implementieren  

Der folgende Ablauf zeigt, wie Vorratsvorschläge mit Drag & Drop geändert werden können. Alternativ können Sie die Felder **Fälligkeitsdatum** und **Menge** im Inforegister **Ereignisänderungen** ändern und die Änderungen im Inforegister **Zeitachse** auf der Seite **Planung** sofort grafisch anzeigen.  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a>So ändern Sie vorgeschlagene Beschaffungsaufträge in der grafischen Ansicht  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Artikel Verfügbarkeit auf Zeitachse** ein, und wählen dann den zugehörigen Link aus.  

    Die Seite **Artikelverfügbarkeit nach Zeitachse** wird geöffnet, mit Artikelnummer, Lagerplatz und Variante des Artikels in der ausgewählten Planungszeile, die in den Feldern des Inforegisters **Optionen** vorab ausgefüllt wurde. Das Inforegister **Zeitachse** zeigt die grafische Darstellung des voraussichtlichen Lagerbestands des Artikels, einschliesslich Planungsvorschläge.  

2.  Stellen Sie sicher, dass das Feld **Planungsvorschläge einschliessen** ausgewählt ist.  
3.  Suchen Sie den vorgeschlagenen Beschaffungsauftrag, der bearbeitet werden soll. Sie erkennen änderbare Elemente an dem grünen Kreis und dem Diskettensymbol. Weitere Informationen über die verschiedenen Symbole, finden Sie unter [Symbole und Bildsymbole im Inforegister „Zeitachse“](production-how-to-modify-planning-suggestions-in-a-graphical-view.md#symbols-and-icons-on-the-timeline-fasttab).  
4.  Positionieren Sie den Mauszeiger über dem grünen Kreis, bis er grösser wird und der Mauszeiger seine Form zum Verschiebungssymbol (vier Pfeile) ändert.  
5.  Drücken Sie die Maustaste und halten Sie sie gedrückt, während Sie den Zeiger nach oben oder unten ziehen, um die Menge zu ändern. Drücken Sie die Maustaste und halten Sie sie gedrückt, während Sie den Zeiger nach links oder rechts ziehen, um das Fälligkeitsdatum zu ändern.  
6.  Ausser dem Bewegen von Elementen mit Drag & Drop können Sie auch Planungsvorschläge ändern, indem Sie einige Rechtsklick-Funktionen verwenden. Klicken Sie mit der rechten Maustaste auf den grünen Kreis eines vorgeschlagenen Vorratselements, und wählen Sie eine der folgenden Funktionen aus.  

    |Funktion|Beschreibung|  
    |--------------|---------------------------------------|  
    |**Neuen Vorrat erstellen**|Erstellt an der Stelle, auf die Sie rechtsklicken, ein neues Element, das einen neuen vorgeschlagenen Beschaffungsauftrag darstellt. Dies wird zu einer neuen Zeile im Planungsvorschlag, wenn Sie **Änderungen speichern** auswählen.<br /><br /> **HINWEIS:** Wenn die Felder **Standortfilter** oder **Varianten-Filter** im Inforegister **Optionen** leer sind oder mehr als einen Filterwert enthalten, wird der neue Vorrat erstellt und später im Planungs- oder Bestellvorschlag mit den folgenden Codes gespeichert:<br /><br /> * Wenn das Feld "Filter" leer ist, wird der neue Vorrat ohne Lagerort oder Variantencode erstellt.<br /><br /> * «»Wenn mehr als ein Filterwert definiert ist, wird der neue Vorrat für den ersten Filterwert gemäss der Sortiermethode erstellt.<br /><br /> Wenn Sie eine andere Variante oder einen anderen Lagerortcode verwenden möchten, müssen Sie diese in der neuen Planungszeile manuell ändern.|  
    |**Vorrat automatisch anpassen**|Optimiert einen neuen Vorrat, den Sie im Diagramm erstellt haben, indem Sie sicherstellen, dass sich vor dem nächsten Vorrat ein Lagerbestand von null ergibt.|  
    |**Vorrat löschen**|Löscht das Element im Inforegister **Zeitachse** und löscht die Planungszeile, wenn Sie **Änderungen speichern** auswählen. Das Symbol wird als Diskette mit einem roten Kreuz angezeigt, wenn der Vorrat gelöscht wurde.<br /><br /> **HINWEIS:** Sie können nur einen Vorrat mit dem Ereignismeldungstyp **Neu** löschen. Nachdem Sie **Änderungen speichern** ausgewählt haben, müssen Sie die betreffende Planungszeile im Planungs- oder Bestellvorschlag manuell löschen.|  

7.  Wählen Sie auf der Registerkarte Aktionen in der Gruppe Allgemein die Option **Neu laden** aus, wenn Sie alle Änderungen zurücksetzen möchten, die Sie durchgeführt haben, nachdem Sie zuletzt die Seite **Artikel-Verfügbarkeit nach Zeitachse** geöffnet oder **Neu laden** ausgewählt haben.  
8. Wenn die Elemente an der gewünschten Stelle im Diagramm positioniert sind, aktivieren Sie **Änderungen speichern**, um Mengen- und Datumsänderungen in die Planungs- oder Bestellvorschlagszeilen zu kopieren, die die grafischen Elemente darstellen.  

Um die Beschaffungsplanänderungen zu übernehmen, müssen Sie den resultierenden Ereignismeldungen aus dem Planungs- oder Bestellvorschlag folgen. Weitere Informationen finden Sie unter Carry Out Action Msg.Plan..

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a>Symbole und Bildsymbole im Inforegister "Zeitachse"
 |Symbol/Bildsymbol|Beschreibung|  
 |------------------|---------------------------------------|  
 |Schwarzes Kreuz|Aufträge (Vorrat und Bedarf).<br /><br /> -   Kann nicht geändert werden.<br />-   Sichtbar, wenn das Feld **Voraussichtlichen Lagerbestand anzeigen** ausgewählt wird (orangefarbenes Diagramm).|  
 |Roter Kreis|Vorhandene Beschaffungsaufträge, die nicht in den Planungsvorschlägen enthalten sind.<br /><br /> -   Kann nicht geändert werden.<br />-   Sichtbar, wenn das Feld **Voraussichtlichen Lagerbestand anzeigen** ausgewählt wird (orangefarbenes Diagramm).|  
 |Gelber Stern|Nachfrageprognose.<br /><br /> -   Kann nicht geändert werden.<br />-   Sichtbar, wenn das Feld **Planungsname** einen Wert enthält.<br /><br /> Wenn die Felder **Voraussichtlichen Lagerbestand anzeigen** und **Planungsvorschläge einschliessen** ausgewählt werden, hat jeder gelbe Stern ein verknüpftes Äquivalent im entgegengesetzten Diagramm. Dieses stellt dar, wie ein vorgeschlagener Vorrat den voraussichtlichen Bedarf erfüllt.|  
 |Grüner Kreis mit einem Diskettensymbol mit einem roten Kreuz|Vorgeschlagener Beschaffungsauftrag mit Ereignismeldung *Abbrechen*.<br /><br /> -   Kann nicht geändert werden.<br />-   Sichtbar, wenn das Feld **Planungsvorschläge einschliessen** ausgewählt wird (grünes Diagramm).|  
 |Grüner Kreis mit einem Diskettensymbol mit einem Stern|Vorgeschlagene Beschaffungsaufträge mit Ereignismeldung *Neu*.<br /><br /> -   Kann geändert werden.<br />-   Sichtbar, wenn das Feld **Planungsvorschläge einschliessen** ausgewählt wird (grünes Diagramm).|  
 |Grüner Kreis mit einem Diskettensymbol mit einem oder zwei Pfeilen|Vorgeschlagene Beschaffungsaufträge mit Ereignismeldung *Neu berechnen*, *Menge ändern* oder *Neu berechnen & Menge ändern*<br /><br /> -   Kann geändert werden.<br />-   Sichtbar, wenn das Feld **Planungsvorschläge einschliessen** ausgewählt wird (grünes Diagramm).<br /><br /> Die Pfeile geben die Richtung des Planungsvorschlags an. Beispielsweise spiegelt ein Linkspfeil zusammen mit einem Nach-oben-Pfeil eine *Neu berechnen Menge ändern*-Ereignismeldung wider, die aus einer rückwärts ausgeführten Neuplanung und einer Mengenerhöhung besteht.|  

Wenn Sie das Dropdownmenü für das Inforegister **Zeitachse** zugreifen, sehen, die folgenden Funktionen, abhängig von dem, was Sie gewählt haben  

 |Funktion|Beschreibung|  
 |--------------|---------------------------------------|  
 |**Neuen Vorrat erstellen**|Erstellt an der Stelle, auf die Sie rechtsklicken, ein neues Element, das einen neuen vorgeschlagenen Beschaffungsauftrag darstellt. Dies wird zu einer neuen Zeile im Planungsvorschlag, wenn Sie **Änderungen speichern** auf der Registerkarte **Vorgang** auswählen.<br /><br /> Alle Filterwerte, die in den Feldern **Standortfilter** oder **Variantenfilter** im Inforegister **Optionen** definiert werden, werden auf den neuen Beschaffungsauftrag angewendet. **Hinweis:**  Wenn die Filterfelder leer sind oder mehr als einen Filterwert enthalten, wird der neue Beschaffungsauftrag erstellt, indem die folgenden Codes verwendet werden: <ul><li>Wenn das Feld "Filter" leer ist, wird der neue Vorrat ohne Lagerort oder Variantencode erstellt.</li><li>Wenn mehr als ein Filterwert definiert ist, wird der neue Vorrat erstellt, indem der erste Filterwert gemäss der Sortierreihenfolge verwendet wird.</li></ul> Wenn Sie einen anderen Varianten- oder Lagerortcode in dem neuen Beschaffungsauftrag verwenden möchten, müssen Sie ihn in der neuen Planungszeile manuell ändern.|  
 |**Vorrat automatisch anpassen**|Optimiert einen neuen Vorrat, den Sie in dem Plan erstellt haben, indem Sie sicherstellen, dass vor dem nächsten Vorrat ein Lagerbestand von null erstellt wird.|  
 |**Vorrat löschen**|Löscht das Element im Inforegister **Zeitachse** und löscht die Planungszeile, wenn Sie **Änderungen speichern** auf der Registerkarte **Vorgang** auswählen. Das Symbol wird als Diskette mit einem roten Kreuz angezeigt, wenn der Vorrat gelöscht wurde. **HINWEIS:**  Sie können nur einen Vorrat mit dem Ereignismeldungstyp *Neu* löschen. Nachdem Sie **Änderungen speichern** auf der Registerkarte **Vorgang** ausgewählt haben, müssen Sie die betreffende Planungszeile im Planungs- oder Bestellvorschlag manuell löschen.|  
 |**Beleg anzeigen**|Öffnet die Bestellung, Planungszeile oder Planung, die das Element darstellt.|  
 |**Verkleinern (Ctrl++)**|Vergrössert die Skala der x-Achse, sodass weniger Tage angezeigt werden. **Hinweis:** Sie erreichen dies auch, indem Sie CTRL drücken und das Mausrad bewegen.|  
 |**Vergrössern (Ctrl+-)**|Verkleinert die Skala der x-Achse, sodass mehr Tage angezeigt werden. **Hinweis:** Sie erreichen dies auch, indem Sie CTRL drücken und das Mausrad bewegen.|  
 |**Zoom zurücksetzen (Ctrl+0)**|Setzt die Skala der x-Achse wieder auf den ursprünglichen Zustand vor dem Zoomen zurück.|  

Zusätzlich zu den Tastaturaktionen, die zuvor erwähnt wurden, können Sie im Inforegister **Zeitachse** auch die folgenden Tastaturaktionen verwenden.  

 |Tastaturaktion|Beschreibung|  
 |---------------------|---------------------------------------|  
 |Ctrl+ Mausrad bewegen|Ändert die Skala der x-Achse.|  
 |Wählen Sie ein Element aus, und drücken Sie dann SHIFT+PFEILTASTE.|Verschiebt das Element in Richtung der Pfeilspitze.|  
 |Register|Springt zum nächsten Element.|  
 |SHIFT+TAB|Springt zum vorherigen Element.|  
 |Drücken Sie beim Verschieben eines Elements die ESC-Taste.|Bricht die Verschiebung ab. **Hinweis:** Funktioniert nicht, wenn Sie die Maustaste freigegeben haben.|

## <a name="see-also"></a>Siehe auch  
[Planung](production-planning.md)   
[Produktion einrichten](production-configure-production-processes.md)  
[Bearbeitungen](production-manage-manufacturing.md)    
[Lagerbesttand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
