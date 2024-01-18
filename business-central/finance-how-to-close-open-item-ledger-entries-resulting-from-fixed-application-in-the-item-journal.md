---
title: 'Schliessen Sie Artikelbucheinträge, die aus einer festen Anwendung stammen'
description: 'Erfahren Sie, wie Sie einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion im Artikel-Erfassungsjournal erstellen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 40
ms.date: 12/12/2023
ms.author: bholtorf
---
# Offene Lagerposten aus einem festen Ausgleich im Artikel-Erf.-Journal schliessen

Sie können das Feld **Ausgegl. von Posten** auf der Seite **Artikel Erf.-Journal** verwenden, um einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion zu erstellen. Beispielsweise um die ausgehende Transaktion zu korrigieren oder ihre Rückgabe zu verarbeiten.  

> [!IMPORTANT]  
> Feste Ausgleiche, die auf diese Weise vorgenommen werden, gelten nur für die Kosten, nicht für die Menge. Entsprechend schliesst der gebuchte positive Lagerposten nicht den angewendeten ausgehenden Posten und bleibt selbst offen. Dies gilt auch, wenn Sie einen festen Ausgleich für einen positiven Posten mit einem negativen Posten buchen, der nicht durch einen positiven regulären Posten geschlossen wurde. Dann bleiben die positiven und negativen Posten offen.  
>
> Dies bedeutet auch, dass Sie eine Lagerbuchungsperiode nicht schliessen können, wenn ein solcher Posten vorhanden ist.  

Sie können Ausgleichsposten unter bestimmten Bedingungen ändern und erneut anwenden, indem Sie die Seite **Anwendungs-Arbeitsblatt** verwenden.  

Der folgende Ablauf zeigt, wie solche Posten durch Ausführen von zwei korrigierenden Buchungen im Artikel Erfassungsjournal geschlossen werden.  

## So schliessen Sie offene Lagerposten, die aus einem festen Ausgleich im Artikel Erfassungsjournal entstanden sind  

1. Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Zugang mit der entsprechenden Menge zu buchen. Dadurch wird der ursprüngliche negative Posten mit einem festen Ausgleich geschlossen.  

    Das Feld **Ausgegl.-von-Posten** gibt die Nummer des ausgehenden Lagerpostens an, dessen Einstandspreis dem eingehenden Lagerposten weitergeleitet wird, wenn Sie eine eingehende Transaktion des Typs **Zugang** oder **Einkauf** mit dem Artikel Erf.-Journal buchen.  
2. Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Abgang zu buchen. Dadurch wird der ursprüngliche korrigierende positive Posten mit einem festen Ausgleich geschlossen.  

    Das Feld **Ausgegl.-von-Posten** gibt an, ob die Menge in der Artikel Erf.-Journalzeile mit einem bereits gebuchten Beleg ausgeglichen werden soll. Geben Sie in diesem Fall die Postennummer des Lagerpostens ein, der mit der Artikel-Erf.-Journalzeile ausgeglichen werden soll.

## Siehe auch 

[Lagerposten entfernen und erneut ausgleichen](finance-how-to-remove-and-reapply-item-entries.md)  
[Verarbeiten von Verkaufsrücklieferung und Stornierungen](sales-how-process-sales-returns-cancellations.md)  
[Einrichten der Lagerwertberechnung und der Kostenrechnung](finance-set-up-inventory-valuation-and-costing.md)  
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]