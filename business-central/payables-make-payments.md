---
title: Überblick der Aufgaben zum Verwalten von Zahlungen an Debitoren | Microsoft Docs
description: Gliederungen ihm eine Arbeit, um Zahlungen an Kreditoren oder zu den Gläubigern, einschliesslich Buchungszahlungszeilen und das Anzeigen einer Übersicht über den fälligen Saldo zu verwalten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 4ece210d5dd8f7748b6c7031bb0fedf571b61c9c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253185"
---
# <a name="making-payments"></a>Zahlungen vornehmen

Wenn Sie Zahlungen an Kreditoren oder Debitoren leisten oder Ihre Mitarbeiter entschädigen, buchen Sie die jeweiligen Zahlungszeilen auf der **Zahlungsausgangs Erf.-Journal**-Seite. Das Erf.-Journal ist ein Fibu Erf.-Journal, das zum Anwenden von Zahlungen optimiert wird und enthält mehrere leistungsstarke Funktionen wie die **Zahlungsvorschlag** Funktion einfügen, welche Kreditorenzahlungen, die fällig sind und den **Kreditor - Saldo nach Perioden** Bericht findet, der einen Überblick über die fälligen Kreditorenzahlungen anzeigt.  

Sie können den Vorgang des Leistens der Zahlung aus Listen, den Karten und der Posten für Debitoren, Kreditoren und Mitarbeiter starten. Jede der Seiten hat eine Schaltfläche, die den Zahlungsstrom startet und die Ihnen dabei hilft, das Zahlungsausgangs Erf.-Journal auszufüllen.  

Im Zahlungsausgangs-Erfassungsjournal können Sie Computerschecks drucken sowie ausgestellte Schecks erfassen. Wenn Sie **Computer Scheck** im Feld **Bankkontozahlungsart** wählen, dann müssen alle Posten für Schecks gedruckt werden, damit die Erfassungsjournalzeilen gebucht werden können.

Wenn Zahlungen gebucht werden, exportieren Sie sie in eine Bankdatei für den Upload zu Ihrer Bank zur Verarbeitung.

Nachdem die Zahlungen in Ihrer Bank getätigt wurden, müssen Sie diese in den entsprechenden offenen Kreditorenposten ausgleichen. Sie können dies manuell oder über den Import in eine Bankkontoauszugsdatei und das Automatische Ausgleichen der Zahlungen durchführen. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

| Bis | Informationen |
| --- | --- |
|Verwenden Sie die Seite **Zahlungsausgangs Erf.-Journal**, das auf dem Fibu Erf.-Journal basiert, um Zahlungen an Kreditoren oder für Mitarbeiter zu buchen.|[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)A|
|Buchen Sie Zahlungen an Kreditoren oder Mitarbeiter und Erstattungen an Debitoren und wenden Sie optional die Zahlungen für die verwandten unbezahlten Rechnungen/Gutschriften an, um sie als bezahlt abzuschliessen.|[Zahlungsbelege und Erstattungen](payables-how-post-payments-refunds.md)|
| Verwenden Sie die Funktion auf der Seite **Zahlung Erf.-Journal** um Kriterien, wie Fälligkeitsdatum, Skontoeignung und Ihrer Liquidität vorzuschlagen. |[Zahlungsvorschlag](payables-how-suggest-vendor-payments.md) |
| Stellen Sie Schecks für Zahlungen entweder als Ausdruck oder als Computer Schecks aus. Annullieren Sie Schecks vor oder nach dem Buchen. |[Zahlung per Scheck machen](payables-how-work-checks.md) |
|Erstellen von elektronischen Zahlungen entsprechend dem Banküberweisungsstandard EU SEPA.|[Nehmen Sie Zahlungen mit dem Bank-Datenkonvertierungs-Service- oder einer SEPA-Banküberweisung vor](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Bezahlen Sie einen Kreditor bar oder mit Scheck und buchen Sie die Zahlung, wenn Sie die Rechnung buchen. |[Einkaufsrechnungen sofort ausgleichen](finance-how-to-settle-purchase-invoices-promptly.md) |
| Um sicherzustellen, dass Ihre Bank nur Schecks und Beträge freigibt, können Sie ihr eine Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält. |[Um eine Positive Pay-Datei zu exportieren](finance-how-positive-pay.md) |

## <a name="see-also"></a>Siehe auch
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
