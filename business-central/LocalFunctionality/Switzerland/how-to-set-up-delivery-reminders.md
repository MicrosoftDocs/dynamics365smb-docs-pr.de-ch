---
title: Einrichten von Lieferbenachrichtigungen
description: "In Business Central können Sie Lieferbenachrichtigungen nutzen, um Verkäufer über verspätete Lieferungen zu mahnen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a4ebb298b62bc194b478749d17f0684d14b70d09
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-delivery-reminders"></a>Gewusst wie: Einrichten von Lieferbenachrichtigungen
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] können Sie EinkaufsLieferbenachrichtigungen verwenden, um Kreditoren an überfällige Lieferungen zu erinnern. Zum Erstellen von Lieferbenachrichtigungen für Kreditoren müssen Sie Basisdaten für die Erstellung von Lieferbenachrichtigungen und Nummernserien für Lieferbenachrichtigungen im Fenster **Kreditoren & Einkauf Einrichtung** einrichten.  

## <a name="to-set-up-delivery-reminders"></a>So richten Sie Lieferbenachrichtigungen ein  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen"), und öffnen Sie **Kreditoren- und Debitoren-Einrichtung**. Wählen Sie dann den zugehörigen Link aus.  
2.  Legen Sie im Inforegister **Allgemein** im Feld **Standard Lief.-Mahn. Datumsfeld** eine der folgenden Optionen gemäss der Beschreibung in der folgenden Tabelle fest.  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**Gewünschtes Wareneingangsdatum**|So legen Sie fest, dass der Datumswert im Feld **Gewünschtes Wareneingangsdatum** auf der Bestellzeile als Standarddatum für das Erstellen von Lieferbenachrichtigungen verwendet wird.|  
    |**Zugesagtes Wareneingangsdatum**|So legen Sie fest, dass der Datumswert im Feld **Zugesagtes Wareneingangsdatum** auf der Bestellzeile als Standarddatum für das Erstellen von Lieferbenachrichtigungen verwendet wird.|  
    |**Erwartetes Wareneingangsdatum**|So legen Sie fest, dass der Datumswert im Feld **Erwartetes Wareneingangsdatum** auf der Bestellzeile als Standarddatum für das Erstellen von Lieferbenachrichtigungen verwendet wird.|  

3.  Füllen Sie im Inforegister **Nummerierung** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Lieferbenachrichtigungsnummern**|Der Nummernseriencode für Lieferbenachrichtigungen.|  
    |**Reg. Lieferbenachrichtigungsnummern**|Der Nummernseriencode für ausgestellte Lieferbenachrichtigungen.|  

4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
 [Lieferanmahnungen](delivery-reminders.md)   
 [Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md)   
 [So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [So erstellen Sie Lieferanmahnungen manuell](how-to-create-delivery-reminders-manually.md)

