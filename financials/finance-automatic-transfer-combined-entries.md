---
title: "Automatische Übertragung und kombinierte Posten | Microsoft Docs"
description: "In der Kostenrechnung können Sie Sachposten in eine Kostenart transferieren, indem Sie eine zusammengefasste Buchung verwenden. Sie können angeben, ob eine Kostenart kombinierte Posten im Feld **Kombinierte Einträge** in der Kostenartdefinition erhalten soll. Die drei Optionen werden in der folgenden Tabelle beschrieben."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f4796d9796788d2fbbf5706688aec75a4ed9a6d8
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="automatic-transfer-and-combined-entries"></a>Automatische Übertragung und kombinierte Posten
In der Kostenrechnung können Sie Sachposten in eine Kostenart transferieren, indem Sie eine zusammengefasste Buchung verwenden. Sie können angeben, ob eine Kostenart kombinierte Posten im Feld **Kombinierte Einträge** in der Kostenartdefinition erhalten soll. Die drei Optionen werden in der folgenden Tabelle beschrieben.  

|Posten kombinieren|Beschreibung|  
|---------------------|-----------------|  
|keine|Jeder Sachposten wird einzeln in die entsprechende Kostenart umgelagert.|  
|Tag|Sachposten mit dem gleichen Buchungsdatum werden wie ein Posten in die entsprechende Kostenart umgelagert.|  
|Monat|Alle Sachposten im selben Kalendermonat werden wie ein Posten in die entsprechende Kostenart umgelagert.|  

> [!IMPORTANT]  
>  Wenn Sie das Kontrollkästchen **Automatische Übertragung aus Fibukonten** im Fenster **Kostenrechnungseinrichtung** aktiviert haben, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] die Kostenrechnung nach jeder Buchung in der Fibu aktualisiert. Kombinierte Posten sind nicht möglich.  

## <a name="see-also"></a>Siehe auch  
 [So übertragen Sie Fibuposten in Kostenposten](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Kriterien für die Übertragung von Sachposten in Kostenposten](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Ergebnisse der Übertragung](finance-results-of-the-transfer.md)   
 [Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

