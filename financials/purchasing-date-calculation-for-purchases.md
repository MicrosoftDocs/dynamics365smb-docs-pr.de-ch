---
title: "Terminberechnung für Einkäufe  | Microsoft Docs"
description: "Das Programm berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist. Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7e569474e3d222a56500665fa73408f47480f338
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="date-calculation-for-purchases"></a>Terminberechnung für Einkäufe
[!INCLUDE[d365fin](includes/d365fin_md.md)] berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist. Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind.  

Wenn Sie ein gewünschtes Wareneingangsdatum in einem Einkaufsbestellkopf angeben, ist das berechnete Auftragsdatum das Datum, an dem die Bestellung erfolgen muss, um die Artikel an dem Datum zu erhalten, das Sie angefordert haben. Dann wird das Datum, an dem die Artikel für die Kommissionierung zur Verfügung stehen, im Feld **Erwartetes Eingangsdatum** berechnet und eingegeben.  

Wenn Sie kein gewünschtes Wareneingangsdatum angeben, wird das Bestelldatum in der Zeile als Ausgangspunkt zur Berechnung des Datums verwendet, an dem die Artikel eingehen sollen, und des Datums, an dem die Artikel für die Kommissionierung zur Verfügung stehen.  

## <a name="calculating-with-a-requested-receipt-date"></a>Berechnung mit einem gewünschten Wareneingangsdatum  
Falls es ein gewünschtes Wareneingangsdatum in der Einkaufsbestellungszeile gibt, wird dieses Datum als Ausgangspunkt für die folgenden Berechnungen verwendet.  

- Gewünschtes Wareneingangsdatum – Beschaffungszeit = Bestelldatum  
- Gewünschtes Wareneingangsdatum + Eingeh. Lagerdurchlaufzeit + Beschaffungszeit = Erwartetes Wareneingangsdatum  

Wenn Sie ein gewünschtes Wareneingangsdatum im Bestellkopf angegeben haben, wird dieses Datum in das entsprechende Feld in allen Zeilen kopiert. Sie können dieses Datum in den einzelnen Zeilen ändern oder entfernen.  

## <a name="calculating-without-a-requested-delivery-date"></a>Berechnung ohne ein gewünschtes Wareneingangsdatum  
Wenn Sie eine Bestellzeile ohne ein gewünschtes Lieferdatum eingeben, füllt die Anwendung das Feld **Bestelldatum** in der Zeile mit dem **Bestelldatum** im Bestellkopf. Hierbei handelt es sich entweder um das Datum, das Sie eingegeben haben, oder um das Arbeitsdatum. Die folgenden Datumsangaben werden dann in der Einkaufsbestellungszeile berechnet, mit dem Bestelldatum als Ausgangspunkt.  

- Bestelldatum + Beschaffungszeit = Geplantes Wareneingangsdatum  
- Geplantes Wareneingangsdatum + Eingeh. Lagerdurchlaufzeit + Beschaffungszeit = Erwartetes Wareneingangsdatum  

Falls Sie das Bestelldatum in der Zeile ändern (z. B. weil die Artikel bei dem Kreditor erst zu einem späteren Datum verfügbar sind), werden die entsprechenden Datumsangaben in der Zeile automatisch neu berechnet.  

Wenn Sie das Bestelldatum im Kopf ändern, wird das Datum in allen Zeilen in das Feld  kopiert, und alle zugehörigen **Datumsfelder** werden neu berechnet.  

## <a name="see-also"></a>Siehe auch  
 [Terminberechnung für Verkäufe](sales-date-calculation-for-sales.md)   
 [So wird's gemacht: Lieferterminzusagen berechnen](sales-how-to-calculate-order-promising-dates.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

