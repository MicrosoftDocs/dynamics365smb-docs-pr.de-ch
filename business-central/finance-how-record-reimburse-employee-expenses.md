---
title: Geschäftsverwandte Ausgaben der Beschäftigten aufzeichnen und zurückzahlen
description: 'Buchen Sie die Ausgaben der Mitarbeiter mit dem Allgemeinen Journal auf das Konto des Mitarbeiters und buchen Sie dann eine Zahlung auf dessen Bankkonto, um die geschäftsbezogenen Ausgaben zu erstatten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: reimbursement
ms.search.form: '63, 234, 625, 5224, 5237, 5238, 5239, 5240'
ms.date: 03/13/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="record-and-reimburse-employees-expenses"></a>Geschäftsverwandte Ausgaben der Beschäftigten aufzeichnen und zurückzahlen

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt Transaktionen für Mitarbeiter auf ähnliche Weise wie für Kreditoren. Entsprechend bestehen Mitarbeiterbuchungsgruppen, um sicherzustellen, dass Mitarbeiterposten auf den entsprechenden Konten in der Fibu gebucht werden.

> [!NOTE]  
> Vergütungszahlungen für Mitarbeiter unterstützen keine Skonti und Zahlungstoleranzen.

Wenn die Mitarbeiter ihr eigenes Geld für die Geschäftsaktivitäten ausgeben, können Sie die Kosten auf das Konto des Mitarbeiters buchen. Dann können Sie die Kosten den Mitarbeiter zurückerstatten, indem Sie eine Zahlung auf das  Bankkonto des Mitarbeiters leisten, ähnlich wie Sie Kreditoren bezahlen.  

In diesem Artikel wird erläutert, wie Sie die Ausgaben in den Büchern erfassen und die Kosten dem Mitarbeiter zurückerstatten. Ihre Organisation verfügt möglicherweise über ein Portal oder eine App, über die Mitarbeiter ihre Spesenabrechnungen einreichen können.

[!INCLUDE [prod_short](includes/prod_short.md)] ist flexibel genug, um vielen verschiedenen Praktiken gerecht zu werden. Die genauen zu verwendenden Kontonummern hängen von der Konfiguration und den Prozessen Ihrer Organisation ab.  

Sie können allgemeine Erfassungsjournale für Mitarbeiterkonten verwenden, um Mitarbeiterausgaben und Rückerstattungstransaktionen in Fremdwährungen zu erfassen und anschliessend die Beträge einfach nachzuverfolgen und mit Belegen zu vergleichen. Lassen Sie Ihren Taschenrechner in Ihrer Schreibtischschublade – Business Central kann den Wechselkurs für Sie anpassen. Wenn Sie allgemeine Erfassungsjournale verwenden, um Transaktionen für Mitarbeiterkonten zu buchen, z. B. wenn Sie Ausgaben erstatten, können Sie im Feld **Währungscode** die Währung für die Transaktionen angeben. Durch die Angabe einer Währung können Sie dieselben Features nutzen wie beim Erfassen von Transaktionen in den Debitoren- und Kreditorenbüchern. Beispielsweise können Mitarbeitende eine Ausgabe in Euro erfassen, ihre Bezahlung jedoch in Dollar erhalten.

Um sicherzustellen, dass der Wechselkurs für die Beträge aktuell ist, können Sie die Mitarbeitersalden anpassen, wenn Sie den Batchauftrag für den Währungswechselkurs ausführen. Wenn Sie die Wechselkurstabelle verwenden, die Mitarbeitersalden jedoch in Ihrer lokalen Währung abrechnen möchten, können Sie die Mitarbeiterkonten von der Anpassung der Wechselkurse ausschliessen.

## <a name="to-record-an-employees-expense"></a>Um die Ausgaben eines Mitarbeiters tz erfassen

Sie buchen die Ausgaben der Mitarbeiter auf der Seite **Fibu Erf.-Journal**.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Allgemeine Erfassungen** ein, und wählen Sie dann den entsprechenden Link.  
2. Öffnet das entsprechende Fibu Erf.-Journal Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md).
3. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Wiederholen Sie Schritt 3 für alle Ausgaben, die der Beschäftigte hatte.

    > [!TIP]  
    > Wenn Sie Zeilen mit mehreren Transaktion über eine Gegenkontozeile, beispielsweise für das Bankkonto des Mitarbeiters eingeben möchten, wählen Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** auf der Seite für Ihren Stapel im **Fibu Erf.-Journalnamen** aus. Dann werden das Feld **Betrag** auf der Gegenkontozeile automatisch mit dem Wert ausgefüllt, der erforderlich ist, um Transaktionen auszugleichen.
5. Wählen Sie die **Buchen** Aktion aus, um die Ausgaben des Kontos des Mitarbeiters zu erfassen.

## <a name="to-reimburse-an-employee"></a>Rückerstattung für Mitarbeiter

Sie zahlen die Kosten dem Mitarbeiter zurück, indem Sie Zahlungen zu dem Bankkonto auf der Seite **Zahlungsausgangs Erf.-Journal** buchen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Zahlungsausgangs Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.
2. Öffnet das entsprechende Zahlungsausgangs-Erf.-Journal Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md).
3. Füllen Sie die Felder je nach Bedarf aus. Weitere Informationen finden Sie unter [Zahlungen durchführen](payables-make-payments.md).
4. Wählen Sie alternativ die **Mitarbeiter-Zahlung vorschlagen** Aktion aus, um automatisch Erfassungsjournalzeilen für offene Mitarbeitervergütungen einzufügen.
5. Wählen Sie die Aktion **Buchen**, um die Rückerstattung zu erfassen.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Um Vergütungen mit Mitarbeiterposten ausgleichen

Sie gleichen Mitarbeiterzahlungen in den entsprechenden offenen Mitarbeiterposten gleich aus, wie Sie dies für Kreditorenzahlungen tun, zum Beispiel auf der Seite **Zahlungsabstimmungserf.-Journal** in den entsprechenden Bankkontoauszugsposten. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md). Alternativ können Sie auf der Seite **Mitarbeiter-Posten** den Eintrag manuell eingeben. Weitere Informationen finden Sie im dazugehörigen Artikel [Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Weitere Informationen

[Buchen von Transaktionen direkt im Fibuposten](finance-how-post-transactions-directly.md)  
[Arbeiten mit Fibu Erfassungsjournalen](ui-work-general-journals.md)  
[Erf.-Journalbuchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
