---
title: 'Vorgehensweise: Versandagenten | Microsoft Docs'
description: Sie können einen Code für jeden Spediteur anlegen und Informationen dazu eingeben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2ea5d9fce1c10cf3c07c833efbe19b208f0c5a7c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788889"
---
# <a name="set-up-shipping-agents"></a>Zusteller einrichten
Sie können einen Code für jeden Spediteur anlegen und Informationen dazu eingeben.  

Wenn Sie eine Internetadresse des Spediteurs eingeben und der Spediteur die Paketverfolgung im Internet anbietet, können Sie die Funktion zur automatischen Paketverfolgung nutzen. Weitere Informationen finden Sie unter [Pakete nachverfolgen](sales-how-track-packages.md)

Wenn Sie Spediteure in Ihren Verkaufsaufträgen eingeben, können Sie auch die Transportarten bestimmen, die jeder Spediteur anbietet.  
Für jeden Spediteur können Sie eine unbegrenzte Anzahl von Transportarten anlegen und Sie können für jede Transportart eine Transportzeit festlegen.  

Wenn Sie einer Verkaufsauftragszeile eine Spediteurtransportart zugeordnet haben, wird die Transportzeit für diese Zeile in den Lieferterminzusagen berücksichtigt. Weitere Informationen finden Sie unter [Berechnen von Lieferterminzusagen](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>So richten Sie einen Spediteur ein  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Zusteller** ein, und wählen Sie dann den zugehörigen Link.  
2.  Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Wählen Sie die Aktion **Spediteurtransportarten**.
4. In **Spediteurtransportarten** füllen Sie die Felder wie notwendig aus.

> [!NOTE]  
>  Wenn Sie den Spediteur in der Auftragszeile löschen, wird auch der Spediteur Transportartcode gelöscht. Der Inhalt der Felder, die zum Teil auf der Spediteurtransportart basierten, wird neu berechnet.  

## <a name="see-also"></a>Siehe auch
[Liefermethoden einrichten](sales-how-set-up-shipment-methods.md)  
[Pakete verfolgen](sales-how-track-packages.md)    
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
