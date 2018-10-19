---
title: "Bank-Geldmittel überweisen| Microsoft Docs"
description: "Sie können Überweisungsbeträge von einem Bankkonto auf ein anders übertragen, einschliesslich verschiedene Währungen, indem Sie die Transaktion im Fibu Erf.-Journal buchen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 758833e146c03cde3f892ec24d43143bcdce655c
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-bank-funds"></a>Bank-Geldmittel überweisen
Manchmal ist es erforderlich, einen Betrag von einem Bankkonto auf ein anderes Bankkonto zu überweisen. Dafür müssen Sie eine Transaktion im Fibu Erf.-Journal buchen. Die Aufgabe variiert abhängig davon, ob die Bankkonten dieselbe Währung oder unterschiedlichen Währungen verwenden.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>So buchen Sie Überweisungen zwischen Bankkonten mit demselben Währungscode:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Allgemeines Erfassungsjournal** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie in einer Erf.-Journalzeile die Felder **Buchungsdatum** und **Belegnr.** aus.
3. Wählen Sie im Feld **Kontoart** die Option **Bankkonto** aus.
4. Im Feld **Kontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.
5. Geben Sie im Feld **Betrag** den Betrag ein, der überwiesen werden soll.
6. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.
7. Im Feld **Gegenkontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.
8. Buchen Sie das Erf.-Journal.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Überweisungen zwischen Bankkonten mit verschiedenen Währungscodes buchen:
Um Beträge zwischen Bankkonten zu transferieren, die unterschiedliche Währungen verwenden, müssen Sie zwei Fibu Buch.-Blattzeilen buchen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Allgemeines Erfassungsjournal** ein, und wählen dann den zugehörigen Link aus.
2. Erstellen Sie zwei Erf.-Journalzeilen und füllen Sie die Felder **Buchungsdatum** und **Belegnr.** aus.
3. Wählen Sie in der ersten Erfassungsjournalzeile des Feldes **Art** **Bankkonto** aus.
4. Im Feld **Kontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.
5. Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos ein. Geben Sie die Habenbeträge mit einem Minuszeichen ein. Geben Sie die Sollbeträge ohne ein Minuszeichen ein.
6. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.
7. Im Feld **Gegenkontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.
8. Wählen Sie in der zweiten Erfassungsjournalzeile des Feldes **Art** **Bankkonto** aus.
9. Im Feld **Kontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.
10. Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos ein. Geben Sie die Habenbeträge mit einem Minuszeichen ein. Geben Sie die Sollbeträge ohne ein Minuszeichen ein.
11. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.  
12. Im Feld **Gegenkontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.

    > [!NOTE]  
    > Wenn die im Buch.-Blatt verwendeten Wechselkurse von den Wechselkursen im Fenster **Währungswechselkurse** abweichen, geben Sie eine dritte Zeile für den Wechselkursgewinn oder -verlust ein. Geben Sie **Fibukonto** im Feld **Kontoart** ein. Geben Sie die Fibukontonummer für Wechselkursgewinn oder -verlust im Feld **Kontonr.** ein. Geben Sie den Wechselkursgewinn oder - verlust im Feld **Amount** mit oder ohne Minuszeichen jeweils für Soll- und Habenbeträge ein.
13. Buchen Sie die Erf.-Journalzeile.

## <a name="see-also"></a>Siehe auch
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)A  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

