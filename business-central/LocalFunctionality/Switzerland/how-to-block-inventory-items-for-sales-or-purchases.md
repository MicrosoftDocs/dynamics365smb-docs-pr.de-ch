---
title: "Sperren von Lagerartikeln für Verkäufe oder Einkäufe"
description: "In Business Central kann ein Artikel als für Verkäufe, Einkäufe oder alle Verwendungszwecke gesperrt gekennzeichnet werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/02/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f11991333f4d9ebaf890b23841d9d90f929fdf98
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="block-inventory-items-for-sales-or-purchases"></a>Sperren von Lagerartikeln für Verkäufe oder Einkäufe
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kann ein Artikel als für Verkäufe, Einkäufe oder alle Verwendungszwecke gesperrt gekennzeichnet werden.  

In der folgenden Tabelle wird veranschaulicht, was beim Sperren von Artikeln passiert.  

|Artikel gekennzeichnet als|Ergebnis|  
|--------------------|------------|  
|**Verkauf gesperrt**|Der Artikel kann nicht in einem Verkaufsbeleg oder einem Erf.-Journal für Verkaufsartikel verwendet werden.|  
|**Einkauf gesperrt**|Der Artikel kann nicht in einem Einkaufsbeleg, einem Erf.-Journal für Einkaufsartikel oder in Einkaufsplanungsprozessen verwendet werden.|  
|**Gesperrt**|Der Artikel kann für keine Artikeltransaktion verwendet werden. Weitere Informationen zum Sperren eines Artikels für alle Zwecke erhalten Sie unter "Artikelkarte".|  

## <a name="to-block-inventory-items-for-sales"></a>So sperren Sie Lagerartikel für den Verkauf  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Artikel, den Sie sperren möchten, und wählen Sie dann die Aktion **Bearbeiten** aus.  
3.  Aktivieren Sie auf dem Inforegister **Preise und Verkauf** das Kontrollkästchen **Verkauf gesperrt**, um den ausgewählten Artikel für Verkaufstransaktionen zu sperren.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="to-block-inventory-items-for-purchase"></a>So sperren Sie Lagerartikel für den Einkauf  

1.  Wählen Sie ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Artikel, den Sie sperren möchten, und wählen Sie dann die Aktion **Bearbeiten** aus.  
3.  Aktivieren Sie auf dem Inforegister **Beschaffung** das Kontrollkästchen **Einkauf gesperrt**, um den ausgewählten Artikel für Einkaufstransaktionen zu sperren.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

Für folgende Aktionen erhalten Sie eine Fehlermeldung:  

- Eingeben von Verkaufs- und Einkaufszeilen in Verkaufs- bzw. Einkaufsbelege für gesperrte Artikel. Weitere Informationen erhalten Sie in den Tabellen "Verkaufszeile" und "Einkaufszeile".  
- Erstellen von Artikel-Erf.-Journalen für gesperrte Artikel. Weitere Informationen erhalten Sie im Fenster "Artikel Erf.-Journal".  
- Buchen von Artikeltransaktionen für gesperrte Artikel.  

## <a name="see-also"></a>Siehe auch  
 [Lagerverwaltung (Schweiz)](swiss-inventory-management.md)   
 [Kopieren von vorhandenen Elementen in neue Elemente](how-to-copy-existing-items-to-new-items.md)   
 [Deaktivieren des Artikelpreistrackings](how-to-deactivate-item-cost-tracking.md)

