---
title: SEPA Lastschriftzahlungen | Microsoft Docs
description: "Wenn ein Basislastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ee07ca7ba498858fac794f1ee1f27f281de8ae02
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a>SEPA-Lastschrifteinzug-Zahlungseingänge buchen
Wenn ein Basislastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen. Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  

Sie können der Zahlungseingang direkt aus dem **Lastschriften** oder im **Direct Debit Collect. Posten** buchen. Sie können auch die Arbeit an einen anderen Benutzer übertragen, indem Sie die zugehörigen Erf.-Journalzeilen vorbereiten.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a>Buchen eines Basislastschrifteingangs im Basislastschriftfenster  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lastschriften** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie eine Zeile für die Basislastschrifterfassung, die in eine Bankdatei exportiert und von der Bank erfolgreich verarbeitet wurde. Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
3. Wählen Sie die Aktion **Zahlungseingang buchen** aus.  
4. Füllen Sie im Fenster **Lastschrift erstellen** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Basislastschriftnr.**|Geben Sie den Basislastschrifteinzug an, für den Sie den Zahlungseingang buchen wollen.|  
    |**Fibu Erf.-Journalvorlage**|Geben Sie an, welche Fibu Erf.-Journalvorlage zum Buchen des Zahlungseingangs verwendet werden soll, etwa die Vorlage für Bareingänge.|  
    |**Fibu Erf.-Journalname**|Geben Sie an, welcher Fibu Erf.-Journalname für die Buchung des Zahlungseingangs verwendet werden soll.|  
    |**Nur Erf.-Journal erstellen**|Markieren Sie dieses Kontrollkästchen, wenn Sie den Zahlungseingang nicht buchen wollen, wenn Sie die Schaltfläche **OK** wählen. Der Zahlungseingang wird in dem angegebenen Buch vorbereitet und erst gebucht, wenn jemand die fraglichen Erf.-Journal-Zeilen bucht.|  

5. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
 [Einziehen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
 [Verkauf](sales-manage-sales.md)

