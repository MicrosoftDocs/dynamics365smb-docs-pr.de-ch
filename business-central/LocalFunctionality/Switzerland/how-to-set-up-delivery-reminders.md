---
title: Einrichten von Lieferbenachrichtigungen
description: In Business Central können Sie Lieferbenachrichtigungen nutzen, um Verkäufer über verspätete Lieferungen zu mahnen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/23/2020
ms.author: sgroespe
ms.openlocfilehash: 3fe1a3dca9a5ab1d561ff0ad9c1b4f2ab45dc990
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676637"
---
# <a name="set-up-delivery-reminders"></a>Gewusst wie: Einrichten von Lieferbenachrichtigungen

In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] können Sie Lieferbenachrichtigungen nutzen, um Verkäufer über verspätete Lieferungen zu mahnen. Um Lieferanmahnungen für Kreditoren zu erstellen, müssen Sie die Stammdaten für die Erstellung von Lieferanmahnungen sowie die Nummernserien für die Lieferanmahnungen auf der Seite **Kreditoren & Einkauf einrichten** einrichten.  

## <a name="to-set-up-delivery-reminders"></a>So richten Sie Lieferbenachrichtigungen ein  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Tell me-Funktion"), geben Sie **Einrichten von Einkäufen und Verbindlichkeiten** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Legen Sie im Inforegister **Allgemein** im Feld **Standard Lief.-Mahn. Datumsfeld** eine der folgenden Optionen gemäss der Beschreibung in der folgenden Tabelle fest.  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**Gewünschtes Wareneingangsdatum**|So legen Sie fest, dass der Datumswert im Feld **Gewünschtes Wareneingangsdatum** auf der Bestellzeile als Standarddatum für das Erstellen von Lieferbenachrichtigungen verwendet wird.|  
    |**Zugesagtes Wareneingangsdatum**|So legen Sie fest, dass der Datumswert im Feld **Zugesagtes Wareneingangsdatum** auf der Bestellzeile als Standarddatum für das Erstellen von Lieferbenachrichtigungen verwendet wird.|  
    |**Erwartetes Wareneingangsdatum**|So legen Sie fest, dass der Datumswert im Feld **Erwartetes Wareneingangsdatum** auf der Bestellzeile als Standarddatum für das Erstellen von Lieferbenachrichtigungen verwendet wird.|  

3. Füllen Sie im Inforegister **Nummerierung** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Lieferbenachrichtigungsnummern**|Der Nummernseriencode für Lieferbenachrichtigungen.|  
    |**Reg. Lieferbenachrichtigungsnummern**|Der Nummernseriencode für ausgegebene Lieferanmahnungen.|  

4. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch

[Lieferanmahnungen](delivery-reminders.md)  
[Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md)  
[So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md)  
[So erstellen Sie Lieferanmahnungen manuell](how-to-create-delivery-reminders-manually.md)
