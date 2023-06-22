---
title: 'Eine Einkaufsofferte erstellen, um ein Offerte anzufordern'
description: 'Beschreibt, wie Verkaufsofferten oder Anforderungen erstellt werden, um Ihre Offerten zu erfassen, um unter bestimmten Bedingungen Produkte an einen Debitoren zu verkaufen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: '49, 97, 9306, 9346'
ms.date: 08/08/2022
ms.author: edupont
---
# <a name="request-quotes" />Offertenanforderungen

Eine Einkaufsofferte kann als erster Entwurf für eine Bestellung verwendet werden. Die Bestellung kann dann in eine Rechnung umgewandelt werden.

## <a name="create-a-purchase-quote" />Erstellen Sie eine Einkaufsofferte

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Einkaufsofferten** ein und wählen Sie dann den entsprechenden Link.
2. Erstellen eines neuen Belegs, so wie Sie eine Bestellung erstellen. Erfahren Sie mehr unter [Einkäufe aufzeichnen](purchasing-how-record-purchases.md).

## <a name="convert-a-purchase-quote-to-a-purchase-order" />Konvertieren Sie eine Einkaufsofferte in eine Einkaufsbestellung

Wenn Sie die Offerte akzeptiert haben, können Sie diese mit einer Einkaufsrechnung umwandeln, um den Einkauf zu verarbeiten.

1. Öffnen Sie eine Einkaufsofferte, die Sie umwandeln möchten, und wählen Sie die **Bestellung erst.** Aktion aus.

Die Einkaufsofferte wird aus der Datenbank entfernt. Eine Verkaufsrechnung oder ein Verkaufsauftrag wird auf der Basis der Informationen in der Verkaufsofferte erstellt, in der Sie den Verkauf verarbeiten können und dann die Verkaufsrechnung buchen. In der erstellten Verkaufsrechnung gibt das Feld **Offertennr.** die Nummer des Verkaufsauftrags und der Rechnung, aus der sie erstellt wurde.

> [!NOTE]
> Es ist nicht möglich, eine Einkaufsofferte direkt in eine Einkaufsrechnung umzuwandeln, wie dies bei Verkaufsofferten möglich ist. Einzelheiten zum Erstellen einer Einkaufsrechnung finden Sie unter [Erfassen Sie Einkäufe mit Einkaufsrechnungen](purchasing-how-record-purchases.md).

## <a name="see-related-microsoft-trainingtrainingmodulescreate-purchase-documents-dynamics--business-central" />Siehe verwandte [Microsoft Schulungen](/training/modules/create-purchase-documents-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Einkauf](purchasing-manage-purchasing.md)  
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
