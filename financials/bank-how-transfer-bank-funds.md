---
title: "Bank-Geldmittel überweisen| Microsoft Docs"
description: "Sie können Überweisungsbeträge von einem Bankkonto auf ein anders übertragen, einschließlich verschiedene Währungen, indem Sie die Transaktion im Fibu Erf.-Journal buchen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 20661cce60bc9007adb9767388bf5af6f9c3acb9
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-bank-funds"></a><span data-ttu-id="e069d-103">Gewusst wie: Bank-Geldmittel überweisen</span><span class="sxs-lookup"><span data-stu-id="e069d-103">How to: Transfer Bank Funds</span></span>
<span data-ttu-id="e069d-104">Manchmal ist es erforderlich, einen Betrag von einem Bankkonto auf ein anderes Bankkonto zu überweisen.</span><span class="sxs-lookup"><span data-stu-id="e069d-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="e069d-105">Dafür müssen Sie eine Transaktion im Fibu Erf.-Journal buchen.</span><span class="sxs-lookup"><span data-stu-id="e069d-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="e069d-106">Die Aufgabe variiert abhängig davon, ob die Bankkonten dieselbe Währung oder unterschiedlichen Währungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e069d-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="e069d-107">So buchen Sie Überweisungen zwischen Bankkonten mit demselben Währungscode:</span><span class="sxs-lookup"><span data-stu-id="e069d-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="e069d-108">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite ober Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e069d-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="e069d-109">Füllen Sie in einer Erf.-Journalzeile die Felder **Buchungsdatum** und **Belegnr.** aus.</span><span class="sxs-lookup"><span data-stu-id="e069d-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="e069d-110">Wählen Sie im Feld **Kontoart** die Option **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="e069d-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="e069d-111">Im Feld **Kontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="e069d-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="e069d-112">Geben Sie im Feld **Betrag** den Betrag ein, der überwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e069d-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="e069d-113">Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="e069d-113">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="e069d-114">Im Feld **Gegenkontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="e069d-114">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="e069d-115">Buchen Sie das Erf.-Journal.</span><span class="sxs-lookup"><span data-stu-id="e069d-115">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="e069d-116">Überweisungen zwischen Bankkonten mit verschiedenen Währungscodes buchen:</span><span class="sxs-lookup"><span data-stu-id="e069d-116">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="e069d-117">Um Beträge zwischen Bankkonten zu transferieren, die unterschiedliche Währungen verwenden, müssen Sie zwei Fibu Buch.-Blattzeilen buchen.</span><span class="sxs-lookup"><span data-stu-id="e069d-117">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="e069d-118">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite ober Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e069d-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="e069d-119">Erstellen Sie zwei Erf.-Journalzeilen und füllen Sie die Felder **Buchungsdatum** und **Belegnr.** aus.</span><span class="sxs-lookup"><span data-stu-id="e069d-119">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="e069d-120">Wählen Sie in der ersten Erfassungsjournalzeile des Feldes **Art** **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="e069d-120">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="e069d-121">Im Feld **Kontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="e069d-121">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="e069d-122">Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos ein.</span><span class="sxs-lookup"><span data-stu-id="e069d-122">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="e069d-123">Geben Sie die Habenbeträge mit einem Minuszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="e069d-123">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="e069d-124">Geben Sie die Sollbeträge ohne ein Minuszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="e069d-124">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="e069d-125">Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="e069d-125">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="e069d-126">Im Feld **Gegenkontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="e069d-126">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="e069d-127">Wählen Sie in der zweiten Erfassungsjournalzeile des Feldes **Art** **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="e069d-127">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="e069d-128">Im Feld **Kontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="e069d-128">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="e069d-129">Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos ein.</span><span class="sxs-lookup"><span data-stu-id="e069d-129">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="e069d-130">Geben Sie die Habenbeträge mit einem Minuszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="e069d-130">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="e069d-131">Geben Sie die Sollbeträge ohne ein Minuszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="e069d-131">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="e069d-132">Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="e069d-132">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="e069d-133">Im Feld **Gegenkontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="e069d-133">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="e069d-134">Wenn die im Buch.-Blatt verwendeten Wechselkurse von den Wechselkursen im Fenster **Währungswechselkurse** abweichen, geben Sie eine dritte Zeile für den Wechselkursgewinn oder -verlust ein.</span><span class="sxs-lookup"><span data-stu-id="e069d-134">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="e069d-135">Geben Sie **Fibukonto** im Feld **Kontoart** ein.</span><span class="sxs-lookup"><span data-stu-id="e069d-135">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="e069d-136">Geben Sie die Fibukontonummer für Wechselkursgewinn oder -verlust im Feld **Kontonr.** ein.</span><span class="sxs-lookup"><span data-stu-id="e069d-136">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="e069d-137">Geben Sie den Wechselkursgewinn oder - verlust im Feld **Amount** mit oder ohne Minuszeichen jeweils für Soll- und Habenbeträge ein.</span><span class="sxs-lookup"><span data-stu-id="e069d-137">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="e069d-138">Buchen Sie die Erf.-Journalzeile.</span><span class="sxs-lookup"><span data-stu-id="e069d-138">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="e069d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e069d-139">See Also</span></span>
[<span data-ttu-id="e069d-140">Verwalten von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="e069d-140">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="e069d-141">Einrichten von Banken</span><span class="sxs-lookup"><span data-stu-id="e069d-141">Setting Up Banking</span></span>](bank-setup-banking.md)  
<span data-ttu-id="e069d-142">[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)A</span><span class="sxs-lookup"><span data-stu-id="e069d-142">[Working with General Journals](ui-work-general-journals.md)</span></span>  
<span data-ttu-id="e069d-143">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e069d-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

