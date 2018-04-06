---
title: Einrichten einer automatischen Archivierung von Belegen (Schweiz)
description: "Sie können die automatische Archivierung von Verkaufs- und Einkaufsbelegen einrichten – beispielsweise Angebote, Rahmenbestellungen und Aufträge – bevor Sie Belege löschen."
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
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 09fca5cba94bed83b862cd8bb9d4b5be895c509d
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-automatic-archiving-of-documents-in-switzerland"></a>Einrichten einer automatischen Archivierung von Belegen (Schweiz)
Sie können die automatische Archivierung von Verkaufs- und Einkaufsbelegen einrichten – beispielsweise Offerten, Rahmenbestellungen und Aufträge – bevor Sie Belege löschen.  

Nachfolgend wird beschrieben, wie die automatische Archivierung von Verkaufsbelegen eingerichtet wird. Diese Gewusst wie gilt allerdings auch für Einkaufsbelege.  

## <a name="to-set-up-automatic-archiving-of-documents"></a>So richten Sie die automatische Archivierung von Belegen ein  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Debit&oren && Verkauf Einr.** ein und wählen dann den zugehörigen Link aus.  
2.  Füllen Sie im Fenster **Debitoren & Verkauf Einr.** im Inforegister **Archivierung** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Offerte archivieren**|**Nie**, wenn Verkaufsbelege beim Löschen nie archiviert werden sollen.<br /><br /> –oder–<br /><br /> **Frage**, wenn der Benutzer angeben soll, ob er Verkaufsbelege beim Löschen archivieren möchte.<br /><br /> –oder–<br /><br /> **Immer**, wenn Verkaufsofferten automatisch beim Löschen archiviert werden sollen.|  
    |**Rahmenaufträge archivieren**|Wählen Sie diese Option aus, um Rahmenaufträge bei jedem Löschen automatisch zu archivieren.|  
    |**Aufträge und Reklamationen archivieren**|Wählen Sie diese Option aus, um Verkaufsaufträge bei jedem Löschen automatisch zu archivieren.|  
    |**Automatisches Aktivitätenprotokoll**|Wählen Sie diese Option aus, um automatisch einen Eintrag für den Kontakt im Aktivitätenprotokoll zu erstellen, wenn ein Verkaufsauftrag oder eine Teillieferung gebucht wird oder wenn eine Verkaufsofferte in einen Verkaufsauftrag umgewandelt wird. **Hinweis:** Dieses Feld ist auf der Seite **Kreditoren & Einkauf Einr.** nicht verfügbar.|  

3.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
 [Einkaufsbelege und Verkaufsbelege (Schweiz)](swiss-purchase-documents-and-sales-documents.md)   
 [Importieren von Postleitzahlen (Schweiz)](how-to-import-swiss-post-codes.md)   
 [Drucken einer Lagerkommissionierliste von einem Auftrag](how-to-print-an-inventory-picking-list-from-a-sales-order.md)   
 [So drucken Sie im Verlauf von Stapelbuchungen Verkaufsaufträge und Bestellungen](how-to-print-sales-and-purchase-orders-during-batch-posting.md)

