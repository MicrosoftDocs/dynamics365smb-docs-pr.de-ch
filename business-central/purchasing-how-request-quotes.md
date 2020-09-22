---
title: Erstellen Sie eine Einkaufsofferte, um ein Angebot von Ihrem Lieferanten anzufordern | Microsoft Docs
description: Beschreibt, wie Verkaufsofferten oder eine Anforderung erstellt wird, um Ihre Offerte zu erfassen, um unter bestimmten Bedingungen einem Debitoren zu verkaufen.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: bc7bb92185d979871298a3312019e3116fecdab5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782940"
---
# <a name="request-quotes"></a>Offertenanforderungen
Eine Einkaufsofferte kann als erster Entwurf für eine Bestellung verwendet werden. Die Bestellung kann dann in eine Rechnung oder einen Auftrag umgewandelt werden.


## <a name="to-create-a-purchase-quote"></a>So erstellen Sie eine Einkaufsofferte
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Einkaufsanfragen** ein, und wählen Sie dann den entsprechenden Link.
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
