---
title: Erstellen Sie eine Einkaufsofferte, um ein Offerte von Ihrem Lieferanten anzufordern | Microsoft Docs
description: Beschreibt, wie Verkaufsofferten oder eine Anforderung erstellt wird, um Ihre Offerte zu erfassen, um unter bestimmten Bedingungen einem Kunden zu verkaufen.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3fe5eca9c26380248471facbd945838b1bf47a1d
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="request-quotes"></a>Offertenanforderungen
Eine Einkaufsofferte kann als erster Entwurf für eine Bestellung verwendet werden. Die Bestellung kann dann in eine Rechnung oder einen Auftrag umgewandelt werden.


## <a name="to-create-a-purchase-quote"></a>So erstellen Sie eine Einkaufsofferte
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Einkaufsofferten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Erstellen eines neuen Belegs, so wie Sie eine Bestellung erstellen. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>So konvertieren Sie eine Einkaufsofferte in eine Einkaufsbestellung
Wenn Sie die Offerte akzeptiert haben, können Sie diese mit einer Einkaufsrechnung oder einem Auftrag umwandeln, um den Einkauf zu verarbeiten.

1. Öffnen Sie eine Einkaufsofferte, die bereit ist zum umzuwandeln, und wählen Sie die **Bestellung erst.** Aktion aus.

Die Einkaufsofferte wird aus der Datenbank entfernt. Eine Einkaufsrechnung oder ein Einkaufsauftrag wird auf der Basis der Informationen in der Einkaufsofferte erstellt, in der Sie den Einkauf verarbeiten können. In der erstellten Einkaufsrechnung bzw. -bestellung gibt das Feld **Offertennr.** die Nummer der Einkaufsofferte an, aus der sie erstellt wurde.

## <a name="see-also"></a>Siehe auch
[Einkauf](purchasing-manage-purchasing.md)  
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

