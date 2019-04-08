---
title: Ausgleichen von Zahlungen mit den entsprechenden Belegen und diese buchen| Microsoft Docs
description: Beschreibt, wie man Zahlungen speichert, die Sie an Kreditoren und Erstattungen leisten, die Sie den Debitoren erstellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 7b3065dd0528588fec4c05e4e9c391a3beb1cc9a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "819757"
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Rekordzahlungen und Erstattungen im Zahlungsausgangs Erf.-Journal

Auf der Seite **Zahlungsjournal** erfassen Sie Zahlungen and Kreditoren und Erstattungen an Debitoren. Wenn Sie eine Zlg Erf.-Journalzeile buchen, wird der zahlende Betrag angegebenen Systembankkonto erfasst. Sie müssen dann die Schritte unternehmen, um die tatsächliche Geldüberweisung aus dem entsprechenden Bankkonto vorzunehmen.  

Das Erf.-Journal ist ein Fibu Erf.-Journal, das zum Anwenden von Zahlungen optimiert wird. Sie können Zeilen schnell hinzufügen, können von Kreditorenzahlungen [!INCLUDE[d365fin](includes/d365fin_md.md)] vorschlagen lassen, und Sie können die Zahlung zu gebuchten Belege anwenden. Auch wenn Sie Zahlungen leisten, geben Sie einen positiven Betrag im Feld **Beleg-Betrag** Feld ein. Je nach Belegart für die Erf.-Journalzeile, wird dieser Betrag dann mit einem negativen Betrag in den zugrunde liegenden Transaktionen erstellt. Dieser Weg ist schneller, um Erfassungsjournalzeilen manuell hinzufügen. Wenn Sie es vorziehen, negative Beträge einzugeben, können Sie das Erf.-Journal personalisieren, um das Feld **Betrag** anzuzeigen,  

- Ausgleichen von Zahlungen mit Rechnungen oder Gutschriften

    Wenn Sie das Feld **Ausgleich mit Belegnr.** mit der Rechnung oder Gutschrift eingeben, die bezahlt oder erstattet werden muss, wird der entsprechende Beleg festgelegt, der bezahlt wird, wenn Sie das Erf.-Journal buchen. Dies wird als Bündelung bezeichnet. Als Alternative zum Anwenden während der Zahlungsbuchung, können Sie die Seite **Kreditorenpostenausgleich** und **Debitorenpostenausgleich** verwenden, nachdem Sie die Zahlungsbuchung erstellt haben. Weitere Informationen finden Sie zum Beispiel unter [Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten](payables-how-apply-purchase-transactions-manually.md).  

- Vorgeschlagener Zahlungen an Kreditoren oder für Mitarbeiter abrufen.

    Die Funktion **Zahlungsvorschlag** kann helfen **Erf.-Journalzeilen automatisch vorzuschlagen** und zwar entsprechend der Priorisierung automatisch auszufüllen. Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md). Mit dieser Funktion wird das Feld **Ausgleich mit Belegnr.** ausgefüllt.  

- Drucken von Schecks und Buchen von Zahlungen elektronisch der Bank übermitteln.

    Zusätzlich zur Erfassung für die Leistung der Zahlung können Sie auch die Seite **Zahlungsausgangs Erf.-Journal** verwenden, um die Zahlung für die weitere Verarbeitung von Ihrer Bank zu registrieren. Weitere Informationen finden Sie unter [Anwenden von Zahlungen](payables-how-work-checks.md) und [Debitoren-Zahlungen manuell ausgleichen](payables-how-export-payments-bank-file.md).  

## <a name="to-make-payments-in-the-payment-journal"></a>So nehmen Sie Zahlungen im Zahlungsausgangs Erf.-Journal vor

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Zahlungs-Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie den Erf.-Journalnamen, der mit den Zahlungen dediziert ist.
3. Wenn Sie wissen, wie die Zahlung oder Rückerstattung erfolgt, füllen Sie die Felder manuell. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Um die Zahlung mit der entsprechenden Rechnung oder Gutschrift auch anzuwenden, aktivieren Sie **Felder Ausgleich. No.** Feld auf der Seite **Kreditorenpostenausgleich** wählen Sie die relevante Rechnung oder die Gutschrift und dann die Schaltfläche **OK** aus.

    Viele Felder, wie die Felder **Dokumentbetrag** und **Fälligkeitsdatum** werden nun mit Informationen aus dem ausgewählten Belegs ausgefüllt.
5. Alternativ nutzen Sie die **Zahlungsvorschlagfunktion**. Alle Informationen und Beträge werden dann auch auf die Erfassungsjournalzeilen eingegeben. Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md).

    Nachrichten leiten Sie, um die erforderlichen Felder korrekt auszufüllen.
6.  Wenn die Projekt-Erfassungsjournalzeilen vollständig sind, wählen Sie die Aktion **Buchen** aus.

## <a name="see-also"></a>Siehe auch
[Zahlung per Scheck machen](payables-how-work-checks.md)  
[Elektronische Zahlungen machen ](payables-how-export-payments-bank-file.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Um eine Positive Pay-Datei zu exportieren](finance-how-positive-pay.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)A  
[Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
