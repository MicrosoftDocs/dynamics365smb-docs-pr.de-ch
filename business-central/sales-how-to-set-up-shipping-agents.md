---
title: 'Vorgehensweise: Versandagenten | Microsoft Docs'
description: Sie können einen Code für jeden Spediteur anlegen und Informationen dazu eingeben.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e1f6af964dad89a8a311f315f8885aaa94b92427
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "930512"
---
# <a name="set-up-shipping-agents"></a>Zusteller einrichten
Sie können einen Code für jeden Spediteur anlegen und Informationen dazu eingeben.  

Wenn Sie eine Internetadresse des Spediteurs eingeben und der Spediteur die Paketverfolgung im Internet anbietet, können Sie die Funktion zur automatischen Paketverfolgung nutzen. Weitere Informationen finden Sie unter [Pakete nachverfolgen](sales-how-track-packages.md)

Wenn Sie Spediteure in Ihren Verkaufsaufträgen eingeben, können Sie auch die Transportarten bestimmen, die jeder Spediteur anbietet.  
Für jeden Spediteur können Sie eine unbegrenzte Anzahl von Transportarten anlegen und Sie können für jede Transportart eine Transportzeit festlegen.  

Wenn Sie einer Verkaufsauftragszeile eine Spediteurtransportart zugeordnet haben, wird die Transportzeit für diese Zeile in den Lieferterminzusagen berücksichtigt. Weitere Informationen finden Sie unter [Berechnen von Lieferterminzusagen](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>So richten Sie einen Spediteur ein  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Versandagent** ein, und wählen dann den zugehörigen Link aus.  
2.  Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Wählen Sie die Aktion **Spediteurtransportarten**.
4. In **Spediteurtransportarten** füllen Sie die Felder wie notwendig aus.

> [!NOTE]  
>  Wenn Sie den Spediteur in der Auftragszeile löschen, wird auch der Spediteur Transportartcode gelöscht. Der Inhalt der Felder, die zum Teil auf der Spediteurtransportart basierten, wird neu berechnet.  

## <a name="see-also"></a>Siehe auch
[Um Pakete zu verfolgen](sales-how-track-packages.md)    
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
