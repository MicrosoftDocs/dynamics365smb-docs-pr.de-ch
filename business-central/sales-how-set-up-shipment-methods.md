---
title: 'Vorgehensweise: Einrichten von Lieferbedingungen | Microsoft Docs'
description: Sie können eine Code für jede einzelne angebotene Versandmethode einrichten, wie auch die Informationen dazu angeben und die Informationen dazu eingeben.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: be65cd62cec984cd2571b6e88998dc169741f376
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312090"
---
# <a name="set-up-shipment-methods"></a>Liefermethoden einrichten
Versandmethoden nennt man auch Incoterms; sie hängen oft ab vom Artikel, den Debitoren und den Kreditoren. Wenn der Debitor beispielsweise auf einer Insel lebt, kann er entscheiden, die Artikel immer auf dem Luftweg oder immer auf dem Seeweg geliefert zu bekommen. Einige Debitoren fordern möglicherweise eine Lieferung am nächsten Tag. Einige möchten die Bestellung vielleicht abholen. Sie können auf den Debitoren- und Kreditorenkarten angeben, welche Lieferart gewünscht ist.

In der Tabelle **Lieferbedingung** richten Sie die Beschreibung und den Code für jede Lieferbedingung ein. Sie können z. B. den Code „FOB“ einrichten und im Feld **Beschreibung** können Sie "Frei an Bord" eingeben. Sie können dann den Code im Feld **Versandmethodencode** an anderer Stelle in der Anwendung eingeben, z. B. auf der Debitorenkarte. Wenn Sie dann neue Aufträge, Bestellungen, Rechnungen oder Gutschriften erstellen oder buchen, wird das System die Beschreibung einfügen, die zu dem Code gehört. Sie können die Standardbeträge auf dem Beleg je nach Anforderung ändern.

## <a name="to-set-up-a-shipment-code"></a>So richten Sie einen Versandcode ein
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Versandmethode** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie auf der Seite **Versandmethode** die Aktion **Neu** aus.
3. Geben Sie in der neuen Zeile einen Code und eine Beschreibung für die Lieferbedingung an.

## <a name="see-also"></a>Siehe auch
[Incoterms](https://iccwbo.org/resources-for-business/incoterms-rules)  
[Zusteller einrichten](sales-how-to-set-up-shipping-agents.md)  
[Pakete verfolgen](sales-how-track-packages.md)    
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
