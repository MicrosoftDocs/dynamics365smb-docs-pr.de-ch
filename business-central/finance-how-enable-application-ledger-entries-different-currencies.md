---
title: "Ausgleichen von Posten in unterschiedlichen Währungen| Microsoft Docs"
description: "Wenn Sie an einen Debitor in einer Währung verkaufen, die Zahlung jedoch in einer anderen Währung erfolgt, kann die Rechnung mit der Zahlung ausgeglichen werden."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f8216885adb734dde214570c65b5f6036caa37d2
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="aaf18-103">Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="aaf18-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="aaf18-104">Falls Sie Einkäufe von einem Kreditor in einer Währung tätigen und die Zahlung in einer anderen Währung leisten, können Sie die Zahlung mit dem Einkauf ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="aaf18-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="aaf18-105">Wenn Sie entsprechend an einen Debitor in einer Währung verkaufen und die Zahlung in einer anderen Währung erhalten, können Sie die Zahlung mit der Verkaufsrechnung ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="aaf18-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="aaf18-106">Im Folgenden wird beschrieben, wie dies für Kreditorenposten im Fenster **Kreditoren & Einkauf Einrichtung** eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="aaf18-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="aaf18-107">Die Einrichtung für Debitorenposten im Fenster **Debitoren & Verkauf Einrichtung** ist ähnlich.</span><span class="sxs-lookup"><span data-stu-id="aaf18-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="aaf18-108">So aktivieren Sie den Ausgleich von Kreditorenposten in unterschiedlichen Währungen</span><span class="sxs-lookup"><span data-stu-id="aaf18-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="aaf18-109">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Käufe und Verkäufe einrichten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="aaf18-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="aaf18-110">Wählen Sie im Feld **Währungsausgleich** eine der folgenden Optionen.</span><span class="sxs-lookup"><span data-stu-id="aaf18-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="aaf18-111">Option</span><span class="sxs-lookup"><span data-stu-id="aaf18-111">Option</span></span> | <span data-ttu-id="aaf18-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aaf18-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="aaf18-113">Keine</span><span class="sxs-lookup"><span data-stu-id="aaf18-113">None</span></span> |<span data-ttu-id="aaf18-114">Ausgleich zwischen Währungen ist nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="aaf18-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="aaf18-115">EWU</span><span class="sxs-lookup"><span data-stu-id="aaf18-115">EMU</span></span> |<span data-ttu-id="aaf18-116">Ausgleich zwischen EWU-Währungen ist zugelassen.</span><span class="sxs-lookup"><span data-stu-id="aaf18-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="aaf18-117">Alle</span><span class="sxs-lookup"><span data-stu-id="aaf18-117">All</span></span> |<span data-ttu-id="aaf18-118">Ausgleich zwischen allen Währungen ist zugelassen.</span><span class="sxs-lookup"><span data-stu-id="aaf18-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="aaf18-119">So richten Sie Sachkonten für Rundungsdifferenzen beim Währungsausgleich ein</span><span class="sxs-lookup"><span data-stu-id="aaf18-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="aaf18-120">Wenn Sie Posten in unterschiedlichen Währungen ausgleichen, müssen Sie die Sachkonten einrichten, auf die Sie die Rundungsdifferenzen buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="aaf18-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="aaf18-121">Sie müssen die Sachkonten einrichten, bevor Sie die Aufgabe abschliessen.</span><span class="sxs-lookup"><span data-stu-id="aaf18-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="aaf18-122">Weitere Informationen finden Sie unter [Die Fibuposten und der Kontenplan verstehen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="aaf18-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="aaf18-123">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitorenbuchungsruppen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="aaf18-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="aaf18-124">Geben Sie in die Felder **Währungsausgl. Rund.-Sollkto.** und **Währungsausgl. Rund.-Habenkto.** die entsprechenden Sachkonten ein, um Rundungsdifferenzen zu buchen.</span><span class="sxs-lookup"><span data-stu-id="aaf18-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="aaf18-125">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkäufer-Buchungsgruppen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="aaf18-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="aaf18-126">Geben Sie in die Felder **Währungsausgl. Rund.-Sollkto.** und **Währungsausgl. Rund.-Habenkto.** die entsprechenden Sachkonten ein, um Rundungsdifferenzen zu buchen.</span><span class="sxs-lookup"><span data-stu-id="aaf18-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aaf18-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aaf18-127">See Also</span></span>
[<span data-ttu-id="aaf18-128">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="aaf18-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="aaf18-129">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="aaf18-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="aaf18-130">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aaf18-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

