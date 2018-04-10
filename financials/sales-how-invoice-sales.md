---
title: Verkaufsangebote erstellen| Microsoft Docs
description: Beschreibt, wie Sie einen Verkaufsauftrag erstellen, einen Vertrag mit einem Kunden erfassen, Produkte unter bestimmten Bedingungen verkaufen oder kaufen.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 03/12/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ea9b4a6310df319df06d02c53b9d6156caaee24f
ms.openlocfilehash: ca826b8a2a736097eee259913bd40bd8888270dc
ms.contentlocale: de-ch
ms.lasthandoff: 03/28/2018

---
# <a name="invoice-sales"></a>Verkaufsrechnung
Sie erstellen eine Verkaufsrechnung oder eine Bestellung, um Ihre Vereinbarung mit dem Kunden zu erfassen, um bestimmte Produkte unter speziellen Liefer- und Zahlungsbedingungen zu verkaufen.  

Es gibt mehrere Szenarien, in dem Sie einen Verkaufsauftrag anstelle einer Verkaufsrechnung verwenden müssen:  

* Wenn Sie nur einen Teil einer Bestellmenge liefern müssen, da z. B. die gesamte Menge nicht verfügbar ist.  
* Wenn Sie Artikel verkaufen, die Ihr Kreditor direkt an den Debitor liefert, d. h. bei einer sogenannten Direktlieferung. Weitere Informationen finden Sie unter [Direktlieferungen erstellen](sales-how-drop-shipment.md)  

In allen anderen Aspekten ist das Vorgehen bei Verkaufsaufträgen gleich wie bei Verkaufsrechnungen. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)

Sie können mit dem Debitor verhandeln, indem Sie zuerst eine Verkaufsofferte erstellen, die Sie in eine Verkaufsrechnung umwandeln können, wenn Sie dem Verkauf zustimmen. Weitere Informationen finden Sie unter  [Angebot erstellen](sales-how-make-offers.md).

Wenn der Debitor entscheidet zu kaufen, senden Sie die Verkaufsrechnung, um die entsprechende Menge und die Wertposten zu erstellen. Wenn Sie die Verkaufsrechnung buchen, können Sie den Beleg als PDF-Dateianhang auch senden. Sie können den E-Mail-Text haben, der mit einer Zusammenfassung der Rechnung und der Zahlungsinformationen, wie ein Link zu Paypal, vorab ausgefüllt wurde. Weitere Informationen finden Sie unter [Senden von Dokumenten über E-Mail](ui-how-send-documents-email.md).

Im betrieblichen Umfeld, in dem der Debitor bezahlen muss, bevor Produkte, wie in der Einzelhandelsbranche, geliefert werden, müssen Sie den Zahlungseingang für die Produkte abwarten, bevor Sie die Produkte liefern. In den meisten Fällen verarbeiten Sie eingehende Zahlungen einige Wochen nach Lieferung, indem Sie die Zahlungen in ihre entsprechenden gebuchten, unbezahlten Verkaufsrechnungen übernehmen. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

Im betrieblichen Umfeld, wo der Debitor sofort bezahlt, beispielsweise in Paypal oder bar oder mit Kreditkarte, können Sie die gewünschte Methode im Feld **Zahlungsformcode** Feld der Verkaufsrechnung auswählen. Zahlung wird sofort auf der gebuchten Rechnung erfasst. Für Zahlungsservices müssen Sie das Feld **Zahlungsverkehr** ausfüllen. Weitere Informationen finden Sie unter [Aktivieren Sie Zahlungen durch Zahlungsverkehr](sales-how-enable-payment-service-extensions.md)

Sie können direkt gezahlte Rechnungen für nicht-registrierte Debitoren auch erstellen, indem Sie eine "eine Bargelddebitoren" Karte einrichten, auf der Sie auf der Verkaufsrechnung hinweisen. Weitere Informationen finden Sie unter [Einrichten von Bargeldkunden](finance-how-to-set-up-cash-customers.md).)  

Sie können eine gebuchte Verkaufsrechnung einfach korrigieren oder stornieren, bevor sie bezahlt wird. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn der Debitor eine Änderung früh im Bestellvorgang anfordert. Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Verkaufsrechnungen](sales-how-correct-cancel-sales-invoice.md). Wenn die gebuchte Verkaufsrechnung bezahlt ist, müssen Sie eine Verkaufsgutschrift erstellen, um den Verkauf zu stornieren. Weitere Informationen finden Sie unter [Retouren verarbeiten oder Stornieren](sales-how-process-sales-returns-cancellations.md).

Artikel können Lagerartikel und Dienstleistungen sein, gekennzeichnet als **Lager**- und **Service**-Typen auf der Artikelkarte. Der Verkaufsrechnungsprozess ist derselbe für beide Artikeltypen. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

Sie können die oberen Infoboxen des Verkaufsangebotes auf zwei Arten ausfüllen, abhängig davon, ob der Debitor bereits registriert ist. Siehe Schritt 2 und 3 im folgenden Verfahren.

## <a name="to-create-a-sales-invoice"></a>So erstellen Sie eine Verkaufsrechnung
1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsrechnung** ein und wählen den zugehörenden Link aus.  
2. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein.

   Andere Felder im Fenster **Verkaufsrechnung** werden nun mit den Standardinformationen vom ausgewählten Debitor ausgefüllt. Wenn der Debitor noch nicht erfasst wurde, dann führen Sie die folgenden Schritte durch:
3. Geben Sie im Feld **Debitor** den Namen eines neuen Debitors ein.
4. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**, um die Übertragung zu bestätigen.
5. Im Fenster **Vorlage für neuen Debitor wählen** wählen Sie eine Vorlage, auf der die neue Debitorenkarte basieren soll, und dann wählen Sie die Schaltfläche **OK**.
6. Eine neue Debitorenkarte wird geöffnet, vorausgefüllt mit Informationen auf der ausgewählten Debitorenvorlage. Füllen Sie die restlichen Felder aus. Weitere Informationen finden Sie unter [Neue Kunden registrieren](sales-how-register-new-customers.md).  
7. Wenn Sie die Debitorenkarte abgeschlossen haben, wählen Sie die Schaltfläche **OK**, um zum Fenster **Verkaufsrechnung** zurückzugehen.

   Felder im Verkaufsrechnungskopf werden mit den Informationen, die Sie festgelegt haben, in der neuen Debitorenkarte ausgefüllt.  
8. Füllen Sie im Fenster **Verkaufsrechnung** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Sie können nun die Verkaufsrechnungszeilen für Produkte füllen, die Sie an den Kunden oder für jede mögliche Transaktion mit dem Kunden verkaufen, den Sie im Fibuposten buchen möchten.   

Wenn Sie wiederkehrende Verkaufszeilen für den Debitor wie einen Monatsersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Schaltfläche **Wiederkehrende Verkaufszeilen holen** einfügen.  
9. Wählen Sie im Inforegister **Zeilen** im Feld **Art** aus, welche Art des Produkts, der Kosten oder der Transaktion Sie für den Debitor mit der Verkaufszeile buchen werden.
10. Geben Sie im Feld **Nr.** Feld, einen Datensatz auswählen, um entsprechend dem Wert im Feld **Art** zu buchen.

    Sie lassen das **Nr.** Feld leer in folgenden Fällen: - Wenn die Zeile für eine Bemerkung ist. Die Bemerkung im Feld **Beschreibung** enthalten ist.
        - Wenn die Zeile für einen Katalogartikel ist. Wählen Sie die Aktion **Nicht-Katalogartikel auswählen**. Weitere Informationen finden Sie unter [Arbeiten mit nicht im Bestand vorhandenen Artikeln](inventory-how-work-nonstock-items.md).

11. Geben Sie im Feld **Menge** ein, wie viele Einheiten des Produkts, der Kosten oder der Transaktion, in der Zeile des Debitors gespeichert werden soll.  

    > [!NOTE]  
>   Wenn Artikel vom Typ **Service** sind, oder das **Typ**-Feld **Ressource** enthält, ist die Menge eine Zeiteinheit wie Stunden, wie im Feld **Einheit des Messcodes** der Zeile angegeben.  

    Der Wert im Feld **Zeilenbetrag** Feld wird als *VK-Preis* x *Menge* berechnet.  

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Debitorenkarte ausgewählt haben.  
12. Wenn Sie Skonto gewähren möchten, geben Sie einen Prozentsatz im Feld **Zeilenrabatt %** ein. Der Wert im Feld **Zeilenbetrag** wird entsprechend aktualisiert.  

    Wenn Sie bestimmte Artikelpreise für den Debitor auf dem Inforegister **Verkaufspreise und Verkaufspreis-Zeilenrabatte** eingerichtet haben, werden der Preis und der Betrag auf der Rechnungszeile automatisch aktualisiert, wenn die vereinbarten Preiskriterien erfüllt sind. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)  
13. Wiederholen Sie die Schritte 9 bis 12 für jedes Produkt oder jede Gebühr, die Sie an den Kunden verkaufen möchten.  

    Die Summen unter den Zeilen werden berechnet, während Sie Zeilen erstellen oder ändern.  
14. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    Wenn Sie Rechnungsrabatte für den Debitor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Rechnungsrabatt in Prozent** eingetragen, sobald die Kriterien erfüllt sein, und der entsprechende Betrag wird im Feld **Rechnungsbetrag mit Rabatt ohne Mehrwertsteuer** eingefügt. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)  
15. Wenn die Verkaufsrechnungszeilen ausgeführt werden, wählen Sie die Aktion **Buchen und Senden** aus.  

Das Dialogfeld **Buchungs- und Sendebestätigung** zeigt die gewünschte Methode des Debitors das Empfangen von Belegen an. Sie können die Sendemethode ändern, indem Sie die Schaltfläche vom Feld **Beleg senden an** auswählen. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).

Der zugehörige Artikel und die Debitorenposten werden nun im System erstellt, und die Verkaufsrechnung wird als PDF-Dokument ausgegeben. Die Verkaufsrechnung wird in der Liste der gebuchten Verkaufsrechnungen entfernt und durch einen neuen Beleg in der Liste der gebuchten Verkaufsrechnungen ersetzt.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Massenrechnungsstellung von Microsoft Bookings in  Finance and Operations, Business edition](finance-bookings.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

