---
title: 'Vorgehensweise: Schliessen von offenen Lagerposten aus einem festen Ausgleich im Artikel Erf.-Journal | Microsoft Docs'
description: "Sie können das Feld **Ausgegl. von Posten** im Fenster **Artikel Erf.-Journal** verwenden, um einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion zu erstellen. Beispielsweise um die ausgehende Transaktion zu korrigieren oder ihre Rückgabe zu verarbeiten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1553b5f85cd9f00f9de15b59bcf258fba412967b
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Schliessen von offenen Lagerposten aus einem festen Ausgleich im Artikel Erf.-Journal
Sie können das Feld **Ausgegl. von Posten** im Fenster **Artikel Erf.-Journal** verwenden, um einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion zu erstellen. Beispielsweise um die ausgehende Transaktion zu korrigieren oder ihre Rückgabe zu verarbeiten. Weitere Informationen finden Sie unter Ausgegl. von Posten.  

> [!IMPORTANT]  
>  Feste Ausgleiche, die auf diese Weise vorgenommen werden, gelten nur für die Kosten, nicht für die Menge. Entsprechend schliesst der gebuchte positive Lagerposten nicht den angewendeten ausgehenden Posten und bleibt selbst offen. Dies gilt auch, wenn Sie einen festen Ausgleich für einen positiven Posten mit einem negativen Posten buchen, der nicht durch einen positiven regulären Posten geschlossen wurde. Dann bleiben die positiven und negativen Posten offen.  
>   
>  Dies bedeutet auch, dass Sie eine Lagerbuchungsperiode nicht schliessen können, wenn ein solcher Posten vorhanden ist.  

Der folgende Ablauf zeigt, wie solche Posten durch Ausführen von zwei korrigierenden Buchungen im Artikel Erfassungsjournal geschlossen werden.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>So schliessen Sie offene Lagerposten, die aus einem festen Ausgleich im Artikel Erfassungsjournal entstanden sind  

1.  Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Zugang mit der entsprechenden Menge zu buchen. Dadurch wird der ursprüngliche negative Posten mit einem festen Ausgleich geschlossen.  
2.  Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Abgang zu buchen. Dadurch wird der ursprüngliche korrigierende positive Posten mit einem festen Ausgleich geschlossen.  

## <a name="see-also"></a>Siehe auch  
[Entfernen und erneutes Ausgleichen von Lagerposten](finance-how-to-remove-and-reapply-item-entries.md)  
 [Verarbeiten von Verkaufsrücklieferung und Stornierungen](sales-how-process-sales-returns-cancellations.md)   
 [Einrichten der Lagerwertberechnung und der Kostenrechnung](finance-set-up-inventory-valuation-and-costing.md)   
 [Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)   
 [Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)

