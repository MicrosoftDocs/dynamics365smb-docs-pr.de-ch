---
title: Erfassen von Aufwendungen oder Umsatz direkt in der Finanzbuchhaltung| Microsoft Docs
description: "Für Geschäftsaktivitäten, die nicht in einem Beleg festgehlaten sind, wie kleinere Aufwendungen oder Zahlungseingänge, können Sie die entsprechenden Transaktionen erstellen, indem Sie die Erf.-Journalzeilen im Fibu Erf.-Journal buchen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 43065620f34a7ef02e5247e78acf306500f82d90
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="a4027-103">Vorgehensweise: Transaktionen direkt in den Fibuposten buchen</span><span class="sxs-lookup"><span data-stu-id="a4027-103">How to: Post Transactions Directly to the General Ledger</span></span>
<span data-ttu-id="a4027-104">Die meisten Finanztransaktionen werden in den Fibuposten von Geschäftsbelegen wie Einkaufsrechnungen und Verkaufsaufträge gebucht.</span><span class="sxs-lookup"><span data-stu-id="a4027-104">Most financial transactions are posted to the general ledger through dedicated business documents, such as purchase invoices and sales orders.</span></span> <span data-ttu-id="a4027-105">Für Geschäftsaktivitäten, die nicht in einem Beleg in[!INCLUDE[d365fin](includes/d365fin_md.md)] festgehlaten sind, wie kleinere Aufwendungen oder Zahlungseingänge, können Sie die entsprechenden Transaktionen erstellen, indem Sie die Buch.-Blattzeilen im **Fibu Buch.-Blatt** buchen.</span><span class="sxs-lookup"><span data-stu-id="a4027-105">For business activities that are not represented by a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as smaller expenses or cash receipts, you can create the related transactions by posting journal lines in the **General Journal** window.</span></span>

<span data-ttu-id="a4027-106">Eine typische Verwendung des Fibu-Erf.-Journal gehört die Buchung der Kosten der Mitarbeiter während Geschäftsaktivitäten zur späteren Rückvergütung.</span><span class="sxs-lookup"><span data-stu-id="a4027-106">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="a4027-107">Weitere Informationen finden Sie unter [Vorgehensweise: Erstatten Sie die Ausgaben der Mitarbeiter zurück](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="a4027-107">For more information, see [How to: Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="a4027-108">Fibu Buch.-Erfassungsjournale dienen zum Buchen auf Fibukonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Mitarbeiterkonten.</span><span class="sxs-lookup"><span data-stu-id="a4027-108">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="a4027-109">Bei der Buchung mit einem Fibu Erf.-Journal werden immer Posten für Fibukonten erstellt.</span><span class="sxs-lookup"><span data-stu-id="a4027-109">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="a4027-110">Dies gilt auch, wenn beispielsweise eine Erfassungsjournalzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="a4027-110">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="a4027-111">Sie können Ihre Version eines Fibu Erf.-Journals anpassen, indem Sie einen Erf.-Journalnamen oder eine Vorlage einrichten.</span><span class="sxs-lookup"><span data-stu-id="a4027-111">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="a4027-112">Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="a4027-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="a4027-113">Anders als für Posten, die mit Belegen gebucht werden, die einen Gutschriftsvorgang benötigen, können Sie Posten ordnungsgemäß annullieren, die mit dem Erf.-Journal gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="a4027-113">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="a4027-114">Weitere Informationen finden Sie unter [Gewusst wie: Buchungen rückgängig machen](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="a4027-114">For more information, see [How to: Reverse Postings](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="a4027-115">Transaktionen direkt in den Fibuposten buchen</span><span class="sxs-lookup"><span data-stu-id="a4027-115">To post a transaction directly to a general ledger account</span></span>
1. <span data-ttu-id="a4027-116">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a4027-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="a4027-117">Öffnet das entsprechende Fibu Erf.-Journal</span><span class="sxs-lookup"><span data-stu-id="a4027-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="a4027-118">Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="a4027-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="a4027-119">Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="a4027-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="a4027-120">Wiederholen Sie Schritt 3 für jede separate Transaktion, die Sie buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="a4027-120">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="a4027-121">Wenn Sie Zeilen mit mehreren Transaktion über eine Gegenkontozeile, beispielsweise für das Bankkonto eingeben möchten, wählen Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel im **Fibu Buch.-Blattnamen** aus.</span><span class="sxs-lookup"><span data-stu-id="a4027-121">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="a4027-122">Dann werden das Feld **Betrag** auf der Gegenkontozeile automatisch mit dem Wert ausgefüllt, der erforderlich ist, um Transaktionen auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="a4027-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="a4027-123">Wählen Sie die **Buchen** Aktion aus, um die Transaktionen in den angegebenen Sachkonten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="a4027-123">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4027-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4027-124">See Also</span></span>
<span data-ttu-id="a4027-125">[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)A</span><span class="sxs-lookup"><span data-stu-id="a4027-125">[Working with General Journals](ui-work-general-journals.md)</span></span>  
[<span data-ttu-id="a4027-126">Vorgehensweise: Geschäftsverwandte Ausgaben der Beschäftigten aufzeichnen und zurückzahlen</span><span class="sxs-lookup"><span data-stu-id="a4027-126">How to: Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="a4027-127">So geht's: Buchungen stornieren</span><span class="sxs-lookup"><span data-stu-id="a4027-127">How to: Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="a4027-128">Finanzen</span><span class="sxs-lookup"><span data-stu-id="a4027-128">Finance</span></span>](finance.md)  
<span data-ttu-id="a4027-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a4027-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
