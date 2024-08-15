---
title: Zahlungen und Rückerstattungen in Zahlungserfassungsjournalen erfassen
description: 'Lesen Sie auf der Seite Zahlungsausgangs Buch.-Blätter nach, wie Sie Zahlungen an Kreditoren und Rückerstattungen an Debitoren erfassen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 07/17/2024
ms.service: dynamics-365-business-central
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Zahlungen und Erstattungen im Zahlungserfassungsjournal erfassen

Auf der Seite  **Zahlungsjournale**  erfassen Sie Zahlungen, die Sie an Lieferanten leisten, und Rückerstattungen, die Sie an Kunden leisten. Wenn Sie eine Zahlungserfassungsjournal-Zeile buchen, wird der bezahlte Betrag auf dem angegebenen Bankkonto erfasst. Sie müssen dann die Schritte unternehmen, um die tatsächliche Geldüberweisung aus dem entsprechenden Bankkonto vorzunehmen.  

Zahlungserfassungsjournale sind Fibu-Erfassungsjournale, die zum Leisten von Zahlungen optimiert werden. Sie können Zeilen schnell hinzufügen, können von Kreditorenzahlungen [!INCLUDE[prod_short](includes/prod_short.md)] vorschlagen lassen, und Sie können die Zahlung zu gebuchten Belege anwenden. Obwohl Sie Zahlungen leisten, geben Sie einen positiven Betrag in das Feld **Beleg-Betrag** ein. Je nach Belegart für die Erf.-Journalzeile, wird dieser Betrag dann mit einem negativen Betrag in den zugrunde liegenden Transaktionen erstellt. Dieser Weg ist schneller, um Erfassungsjournalzeilen manuell hinzufügen. Wenn Sie es vorziehen, negative Beträge einzugeben, können Sie das Erf.-Journal personalisieren, um das Feld **Betrag** anzuzeigen, Weitere Informationen zum Personalisieren von Seiten finden Sie unter [Beginnen Sie mit der Personalisierung, indem Sie den Personalisierungsmodus verwenden](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).  

- Ausgleichen von Zahlungen mit Rechnungen oder Gutschriften

    Wenn Sie das Feld **Ausgleich mit Belegnr.** mit der Rechnung oder Gutschrift eingeben, die bezahlt oder erstattet werden muss, wird der entsprechende Beleg auf **Bezahlt** festgelegt, wenn Sie das Erfassungsjournal buchen. Diese Einstellung wird als Bündelung bezeichnet. Als Alternative zum Anwenden während der Zahlungsbuchung, können Sie die Seite **Kreditorenpostenausgleich** und **Debitorenpostenausgleich** verwenden, nachdem Sie die Zahlung gebucht haben. Weitere Informationen finden Sie zum Beispiel unter [Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten](payables-how-apply-purchase-transactions-manually.md).  

- Vorgeschlagener Zahlungen an Kreditoren oder für Mitarbeiter abrufen.

    Die Aktionen **Zahlungsvorschlag** und **Mitarbeiterzahlung vorschlagen** können Ihnen dabei helfen, Zahlungserfassungsjournal-Zeilen automatisch entsprechend der Priorisierung und den Fälligkeitsterminen automatisch auszufüllen. Weitere Informationen finden Sie unter [Zahlungsvorschlag](payables-how-suggest-vendor-payments.md). Mit dieser Funktion wird das Feld **Ausgleich mit Belegnr.** ausgefüllt.  

- Drucken von Schecks und Buchen von Zahlungen elektronisch der Bank übermitteln.

    Zusätzlich zur Erfassung für die Leistung der Zahlung können Sie auch die Seite **Zahlungsausgangs Erf.-Journal** verwenden, um die Zahlung für die weitere Verarbeitung von Ihrer Bank zu registrieren. Weitere Informationen finden Sie unter [Scheckzahlungen vornehmen](payables-how-work-checks.md) und [Elektronische Zahlungen vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a>So nehmen Sie Zahlungen im Zahlungsausgangs Erf.-Journal vor

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Zahlungsausgangs Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie den Erfassungsjournal-Batch, den Sie für Zahlungen verwenden.
3. Wenn Sie wissen, wer zu bezahlen ist, füllen Sie die Felder manuell aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Um die Zahlung auch auf die zugehörige Rechnung oder Gutschrift anzuwenden, wählen Sie auf der Seite  **Kreditoreneinträge anwenden**  das Feld  **Gilt für Belegnr.**, Auswählen die entsprechende Rechnung oder Gutschrift und wählen Sie dann die Schaltfläche  **OK** .

    Viele Felder, wie die Felder **Dokumentbetrag** und **Fälligkeitsdatum** enthalten nun Informationen aus dem ausgewählten Beleg.
5. Verwenden Sie alternativ die Aktion **Zahlungsvorschlag**. Alle Informationen und Beträge werden auch in die Erfassungsjournalzeilen eingegeben. Weitere Informationen finden Sie unter [Zahlungsvorschlag](payables-how-suggest-vendor-payments.md).
6. Nachdem Sie alle Zahlungserfassungsjournal-Zeilen ausgefüllt haben, wählen Sie die Aktion **Buchen** aus.

## <a name="to-issue-a-refund-check"></a>So stellen Sie einen Scheck zur Rückerstattung aus

1. Wählen Sie die ![Glühbirne , die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Tell me-Funktion"), geben Sie **Zahlungsjournale** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie im Feld **Belegart** die Option **Rückerstattung**.  
3. Geben Sie im Feld **Externe Belegnummer** eine Referenz für den Rückerstattungsscheck (z. B. die Retourenummer) ein.  
4. Wählen Sie im Feld **Kontoart** die Option **Kreditor** aus.  
5. Wählen Sie im Feld **Konto-Nr.** die Kontonummer des Debitors, auf den der Scheck für die Rückerstattung ausgestellt wird.  
6. Geben Sie im Feld **Betrag** den zu erstattenden Betrag ein.  
7. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.  
8. Geben Sie im Feld  **Kontonr.**  Auswählen das Bankkonto ein, von dem der Scheck ausgestellt wurde.  
9. Wählen Sie im Feld **Gilt für Beleg. Nr.** die Belege aus, die eine Rückerstattung erfordern.  
10. Nachdem Sie alle Zahlungserfassungsjournal-Zeilen ausgefüllt haben, wählen Sie die Aktion **Buchen/Drucken**, die Aktion **Buchen und Drucken** und dann **Ja** aus.  
  
## <a name="see-also"></a>Siehe auch

[Scheckzahlungen vornehmen](payables-how-work-checks.md)  
[Elektronische Zahlungen vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Um eine Positive Pay-Datei zu exportieren](finance-how-positive-pay.md)  
[Arbeiten mit Fibu Erfassungsjournalen](ui-work-general-journals.md)  
[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
