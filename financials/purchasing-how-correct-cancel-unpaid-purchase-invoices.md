---
title: "Ändern oder Löschen einer unbezahlten Einkaufsrechnung| Microsoft Docs"
description: "Erklärt, wie automatisch eine Einkaufsgutschrift korrigiert, abgebrochen oder rückgängig gemacht wird und eine gebuchte Einkaufsrechnung erstellt wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: f7d9b5ef0192f0d66d50d4ba51f6e2c4d12a89f5
ms.contentlocale: de-ch
ms.lasthandoff: 04/16/2018

---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="1cc06-103">Ändern oder Löschen einer unbezahlten Einkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="1cc06-103">Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="1cc06-104">Sie können eine bezahlte Einkaufsrechnung korrigieren oder abbrechen.</span><span class="sxs-lookup"><span data-stu-id="1cc06-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="1cc06-105">Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn Sie den Kauf früh im Bestellvorgang ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="1cc06-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="1cc06-106">Wenn Sie bereits für Produkte auf der gebuchten Einkaufsrechnung bezahlt haben, können Sie diese aus der gebuchten Einkaufsrechnung selbst nicht korrigieren oder stornieren.</span><span class="sxs-lookup"><span data-stu-id="1cc06-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="1cc06-107">Stattdessen müssen Sie eine Einkaufsgutschrift manuell erstellen, um den Einkauf zu stornieren, optional verwaltet mit einer Einkaufsreklamation.</span><span class="sxs-lookup"><span data-stu-id="1cc06-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="1cc06-108">Weitere Informationen finden Sie unter [Einkaufsretouren verarbeiten oder Stornieren](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="1cc06-108">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="1cc06-109">Im Fenster **Geb. Einkaufsrechnung** können Sie die Schaltfläche **Korrigieren** oder **Stornieren** wählen.</span><span class="sxs-lookup"><span data-stu-id="1cc06-109">In the **Posted Purchase Invoice** window, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="1cc06-110">Wenn Sie eine gebuchte Einkaufsrechnung korrigieren oder stornieren, wird sie in allen Sach- und Inventurposten angewendet, die erstellt wurden, als die erste Einkaufsrechnung gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="1cc06-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="1cc06-111">Dadurch wird die gebuchte Einkaufsrechnung in Ihren Finanzdatensätzen storniert und verlässt die gebuchte Korrektureinkaufsgutschrift für Ihr Protokoll.</span><span class="sxs-lookup"><span data-stu-id="1cc06-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="1cc06-112">Nachfolgend wird die Verwendung von **Korrigieren** und **Stornieren** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1cc06-112">In the following the use of **Correct** and **Cancel** is described.</span></span>

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="1cc06-113">Gebuchte Einkaufsrechnung korrigieren</span><span class="sxs-lookup"><span data-stu-id="1cc06-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="1cc06-114">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="1cc06-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1cc06-115">Wählen Sie die gebuchte Einkaufsrechnung, die Sie korrigieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1cc06-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
   >   <span data-ttu-id="1cc06-116">Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Einkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.</span><span class="sxs-lookup"><span data-stu-id="1cc06-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="1cc06-117">Im Fenster **Gebuchte Einkaufsrechnung** wählen Sie **Korrekt** aus.</span><span class="sxs-lookup"><span data-stu-id="1cc06-117">In the **Posted Purchase Invoice** window, choose **Correct**.</span></span>

    <span data-ttu-id="1cc06-118">Eine neue Verkaufsrechnung mit den gleichen Informationen wird erstellt, auf dem Sie die Korrektur machen können.</span><span class="sxs-lookup"><span data-stu-id="1cc06-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="1cc06-119">Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="1cc06-119">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="1cc06-120">Das Feld **Storniert** am Anfang gebuchten Einkaufsrechnung wird auf **Ja** geändert.</span><span class="sxs-lookup"><span data-stu-id="1cc06-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="1cc06-121">Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu annullieren.</span><span class="sxs-lookup"><span data-stu-id="1cc06-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="1cc06-122">Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Einkaufsgutschrift anzuzeigen, die die gebuchte Einkaufsrechnung annulliert.</span><span class="sxs-lookup"><span data-stu-id="1cc06-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="1cc06-123">Gebuchte Einkaufsrechnung stornieren</span><span class="sxs-lookup"><span data-stu-id="1cc06-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="1cc06-124">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="1cc06-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1cc06-125">Wählen Sie die gebuchte Einkaufsrechnung, die Sie stornieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1cc06-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
   >   <span data-ttu-id="1cc06-126">Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Einkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.</span><span class="sxs-lookup"><span data-stu-id="1cc06-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="1cc06-127">Im Fenster **Gebuchte Einkaufsrechnung** wählen Sie **Stornieren** aus.</span><span class="sxs-lookup"><span data-stu-id="1cc06-127">In the **Posted Purchase Invoice** window, choose **Cancel**.</span></span>

    <span data-ttu-id="1cc06-128">Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu annullieren.</span><span class="sxs-lookup"><span data-stu-id="1cc06-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="1cc06-129">Das Feld **Storniert** am Anfang gebuchten Einkaufsrechnung wird auf **Ja** geändert.</span><span class="sxs-lookup"><span data-stu-id="1cc06-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="1cc06-130">Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Einkaufsgutschrift anzuzeigen, die die gebuchte Einkaufsrechnung annulliert.</span><span class="sxs-lookup"><span data-stu-id="1cc06-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cc06-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cc06-131">See Also</span></span>
[<span data-ttu-id="1cc06-132">Einkauf</span><span class="sxs-lookup"><span data-stu-id="1cc06-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="1cc06-133">Erfassen eines Einkaufs</span><span class="sxs-lookup"><span data-stu-id="1cc06-133">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="1cc06-134">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1cc06-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

