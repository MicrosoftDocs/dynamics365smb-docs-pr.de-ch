---
title: "Gschäftsrelevante Ausgaben der Beschäftigten aufzeichnen und zurückzahlen | Microsoft Docs"
description: "Buchen Sie die Kosten der Mitarbeiter mit dem Fibu-Erf.-Journal zu dem Konto und buchen Sie später die Zahlung an das Bankkonto des Mitarbeiters, dem die geschäftsverwandten Ausgaben zurückzuerstatten sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 75e2615dfd7af8ec6269affb0a61f75adf1c6d97
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="record-and-reimburse-employees-expenses"></a>Geschäftsverwandte Ausgaben der Beschäftigten aufzeichnen und zurückzahlen
[!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt Transaktionen für Mitarbeiter auf ähnliche Weise wie für Kreditoren. Entsprechend bestehen Mitarbeiterbuchungsgruppen, um sicherzustellen, dass Mitarbeiterposten auf den entsprechenden Konten in der Fibu gebucht werden.

> [!NOTE]  
> Mitarbeitertransaktionen können nur in der lokalen Währung gebucht werden. Vergütungszahlungen für Mitarbeiter unterstützen keine Skonti und Zahlungstoleranzen.

Wenn die Mitarbeiter ihr eigenes Geld für die Geschäftsaktivitäten ausgeben, können Sie die Kosten auf das Konto des Mitarbeiters buchen. Dann können Sie die Kosten den Mitarbeiter zurückerstatten, indem Sie eine Zahlung auf das  Bankkonto des Mitarbeiters leisten, ähnlich wie Sie Kreditoren bezahlen.

## <a name="to-record-an-employees-expense"></a>Um die Ausgaben eines Mitarbeiters tz erfassen
Sie buchen die Ausgaben der Mitarbeiter im Fenster **Fibu-Erf.-Journal**.
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Allgemeine Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.
2. Öffnet das entsprechende Fibu Erf.-Journal Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)
3. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Wiederholen Sie Schritt 3 für alle Ausgaben, die der Beschäftigte hatte.

    > [!TIP]  
    > Wenn Sie Zeilen mit mehreren Transaktion über eine Gegenkontozeile, beispielsweise für das Bankkonto des Mitarbeiters eingeben möchten, wählen Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel im **Fibu-Erf.-Journalnamen** aus. Dann werden das Feld **Betrag** auf der Gegenkontozeile automatisch mit dem Wert ausgefüllt, der erforderlich ist, um Transaktionen auszugleichen.
5. Wählen Sie die **Buchen** Aktion aus, um die Ausgaben des Kontos des Mitarbeiters zu erfassen.

## <a name="to-reimburse-an-employee"></a>Rückerstattung für Mitarbeiter
Sie zahlen die Kosten dem Mitarbeiter zurück, indem Sie Zahlungen zu dem Bankkonto im Fenster **Zahlungsausgangs-Erf.-Journal** buchen.
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Zahlungs-Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.
2. Öffnet das entsprechende Zahlungsausgangs-Erf.-Journal Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)
3. Füllen Sie die Felder je nach Bedarf aus. Weitere Informationen finden Sie unter [Zahlungen durchführen](payables-make-payments.md).
4. Wählen Sie alternativ die **Mitarbeiter-Zahlung vorschlagen** Aktion aus, um automatisch Erfassungsjournalzeilen für offene Mitarbeitervergütungen einzufügen.
5. Wählen Sie die Aktion **Buchen**, um die Rückerstattung zu erfassen.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Um Vergütungen mit Mitarbeiterposten ausgleichen
Sie gleichen Mitarbeiterzahlungen in den entsprechenden offenen Mitarbeiterposten gleich aus, wie Sie dies für Kreditorenzahlungen tun, zum Beispiel im Fenster **Zahlungsabstimmungs-Erf.-Journal** in den entsprechenden Bankkontoauszugsposten. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md). Alternativ können Sie im Fenster **Mitarbeiter-Posten** den Eintrag manuell eingeben. Weitere Informationen finden Sie unter [Manuelle Abstimmung von Zahlungen](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Siehe auch
[Buchen von Transaktionen direkt im Fibuposten](finance-how-post-transactions-directly.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)A  
[Buchungen stornieren](finance-how-reverse-journal-posting.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

