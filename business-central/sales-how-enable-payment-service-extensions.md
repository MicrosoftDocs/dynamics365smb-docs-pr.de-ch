---
title: Aktivieren Sie Debitoren-Zahlungen mit Zahlungsverkehr
description: 'Erleichtern Sie Ihren Debitoren das Bezahlen ihrer Rechnungen, indem Sie Kundenzahlungen über Zahlungsdienste aktivieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: online payment
ms.search.forms: '1060, 1061, 1062'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="enable-customer-payments-through-payment-services"></a>Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr

Als Alternative zum Einzug von Zahlungen per Banküberweisung oder Kreditkarte können Ihre Debitoren Sie über ihr Konto mit Zahlungsdiensten wie PayPal oder WorldPay bezahlen.  

Nachdem Sie einen Zahlungsverkehr in [!INCLUDE[prod_short](includes/prod_short.md)], wird ein Link zum Service auf Verkaufsbelegen verfügbar, den Sie per E-Mail an Ihren Geschäftspartner senden können. Debitoren können den Link verwenden, um zum Zahlungsverkehr zu wechseln und die Rechnung direkt über das Verkaufsbeleg zu bezahlen. Wenn Sie nicht den Link hinzufügen möchten, beispielsweise wenn ein Debitor in Bar bezahlt, können Sie den Zahlungsverkehr von der Rechnung entfernen, bevor Sie buchen.  

Die Erweiterungen PayPal Payments Standard und WorldPay Payments Standard sind in [!INCLUDE[prod_short](includes/prod_short.md)] installiert und können von Ihnen aktiviert werden.  

> [!CAUTION]
> Die Erweiterung WorldPay Payments Standard wird eingestellt. Der Code gilt ab dem 2. Veröffentlichungszyklus 2023 als veraltet. Die App bleibt für die nächsten drei Hauptversionen aktiv und wird dann entfernt.   

## <a name="to-enable-a-payment-service-in-"></a>Einen Zahlungsverkehr in [!INCLUDE[prod_short](includes/prod_short.md)] aktivieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Zahlungsverkehr** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Zahlungsverkehr** die Aktion **Neu** aus.  
3. Wählen Sie die Zahlungsverkehr aus und schliessen Sie dann die Seite.  
4. Wählen Sie auf der Seite **Zahlungsverkehr** die Aktion **Einrichten** aus.  
5. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Schliessen Sie die Seite.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Einen Zahlungsverkehr in einer Verkaufsrechnung auswählen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Verkaufsrechnung, die Sie zahlen möchten, indem Sie den Zahlungsverkehr verwenden.  
3. Geben Sie im Feld **Zahlungsverkehr** den Zahlungsservice ein.  

    > [!NOTE]  
    > Das Feld **Zahlungsverkehr** ist verfügbar, wenn Sie den Zahlungsservice aktiviert haben.  

## <a name="see-also"></a>Siehe auch

[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzenb](ui-extensions.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
