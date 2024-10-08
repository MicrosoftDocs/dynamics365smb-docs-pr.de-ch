---
title: Übersicht über Aufgaben zum Verwalten von Zahlungen an Kreditoren
description: 'Gliederungen ihm eine Arbeit, um Zahlungen an Kreditoren oder zu den Gläubigern, einschließlich Buchungszahlungszeilen und das Anzeigen einer Übersicht über den fälligen Saldo zu verwalten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '254, 256, 1190, 1191, 1227, 1228, 1229'
ms.date: 07/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="make-payments"></a>Zahlungen vornehmen

Sie bezahlen Kreditoren oder Debitoren oder entschädigen Ihre Mitarbeiter, indem Sie die jeweiligen Zahlungszeilen auf der Seite **Zahlungs-Erf.-Journal** buchen. Das Zahlungserfassungsjournal ist ein Fibu-Erfassungsjournal, das zum Anwenden von Zahlungen optimiert wird und viele leistungsstarke Aktionen bietet. Beispielsweise die Aktion **Lieferantenzahlungen vorschlagen**, die fällige Lieferantenzahlungen findet, und der Bericht **Lieferant – Zusammenfassung Alterung**, der eine Übersicht über fällige Lieferantenzahlungen anzeigt.  

Sie können den Zahlungsprozess über die Listen, Karten und Posten für Debitoren, Kreditoren und Mitarbeiter starten. Jede der Seiten hat eine Schaltfläche, die den Zahlungsstrom startet und die Ihnen dabei hilft, das Zahlungsausgangs Erf.-Journal auszufüllen.  

Im Zahlungsausgangs-Erfassungsjournal können Sie Computerschecks drucken sowie ausgestellte Schecks erfassen. Wenn Sie **Computer Scheck** im Feld **Bankkontozahlungsart** wählen, müssen Sie Zeilen drucken, die die Schecks darstellen, bevor Sie die Erfassungsjournalzeilen buchen können.

Nachdem Sie Zahlungen gebucht haben, können Sie sie in eine Bankdatei exportieren, die Sie zur Verarbeitung in Ihre Bank hochladen können.

Nachdem die Zahlungen in Ihrer Bank getätigt wurden, müssen Sie diese in den entsprechenden offenen Kreditorenposten ausgleichen. Sie können sie manuell oder über den Import in eine Bankkontoauszugsdatei und die automatische Anwendung der Zahlungen anwenden. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben..

| Bis | Informationen |
| --- | --- |
|Verwenden Sie die Seite **Zahlungsausgangs Erf.-Journal**, das auf dem Fibu Erf.-Journal basiert, um Zahlungen an Kreditoren oder für Mitarbeiter zu buchen.|[Arbeiten mit Fibu Erfassungsjournalen](ui-work-general-journals.md)|
|Buchen Sie Zahlungen an Kreditoren oder Mitarbeiter und Erstattungen an Debitoren und wenden Sie optional die Zahlungen für die verwandten unbezahlten Rechnungen/Gutschriften an, um sie als bezahlt abzuschliessen.|[Zahlungsbelege und Erstattungen](payables-how-post-payments-refunds.md)|
| Verwenden Sie die Funktion auf der Seite **Zahlung Erf.-Journal** um Kriterien, wie Fälligkeitsdatum, Rabatteignung und Ihrer Liquidität vorzuschlagen. |[Zahlungsvorschlag](payables-how-suggest-vendor-payments.md) |
| Stellen Sie Schecks für Zahlungen entweder als Ausdruck oder als Computer Schecks aus. Annullieren Sie Schecks vor oder nach dem Buchen. |[Zahlung per Scheck machen](payables-how-work-checks.md) |
|Erstellen von elektronischen Zahlungen entsprechend dem Banküberweisungsstandard EU SEPA.|[Zahlungen mit der AMC Banking 365 Fundamentals-Erweiterung oder per SEPA-Überweisung vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Bezahlen Sie einen Kreditor bar oder mit Scheck und buchen Sie die Zahlung, wenn Sie die Rechnung buchen. |[Einkaufsrechnungen sofort ausgleichen](finance-how-to-settle-purchase-invoices-promptly.md) |
| Um sicherzustellen, dass Ihre Bank nur Schecks und Beträge freigibt, können Sie ihr eine Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält. |[Positive Pay-Datei exportieren](finance-how-positive-pay.md) |

## <a name="see-also"></a>Siehe auch

[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
