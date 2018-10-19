---
title: "so fassen Sie Wareneingänge zusammen | Microsoft Docs"
description: "Wenn Sie mehrere Einkaufslieferungen gleichzeitig fakturieren möchten, können Sie die Funktion Sammelgutschrift verwenden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c6a6707c9968bca856fda51984283277b27e8e84
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="26d42-103">Zusammenfassen von Lieferungen in einer einzelnen Rechnung</span><span class="sxs-lookup"><span data-stu-id="26d42-103">Combine Receipts on a Single Invoice</span></span>
<span data-ttu-id="26d42-104">Wenn Sie mehrere Einkaufslieferungen gleichzeitig fakturieren möchten, können Sie die Funktion **Sammelgutschrift** verwenden.</span><span class="sxs-lookup"><span data-stu-id="26d42-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="26d42-105">Bevor Sie eine zusammengefassten Einkaufslieferung erstellen können, müssen Sie mehrere Einkaufslieferungen für den gleichen Debitor in der gleichen Währung gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="26d42-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="26d42-106">Anders ausgedrückt: Sie müssen mindestens zwei Einkaufsbestellungen ausgefüllt und als geliefert (aber nicht fakturiert) gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="26d42-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="26d42-107">Wenn Einkaufslieferungen in einer Rechnung zusammengefasst und gebucht werden, wird für die fakturierten Zeilen eine gebuchte Einkaufsrechnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="26d42-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="26d42-108">Das Feld **Fakturierte Menge** auf der Ursprungseinkaufsbestellung oder der Rahmenbestellung wird ausgehend von der fakturierten Menge aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="26d42-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="26d42-109">Der ursprüngliche Beleg wird jedoch nicht gelöscht, auch wenn er vollständig geliefert und fakturiert wurde, und Sie müssen daher den Einkaufsbeleg löschen.</span><span class="sxs-lookup"><span data-stu-id="26d42-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

## <a name="to-combine-receipts"></a><span data-ttu-id="26d42-110">So fassen Sie Wareneingänge zusammen</span><span class="sxs-lookup"><span data-stu-id="26d42-110">To combine receipts</span></span>  
1. <span data-ttu-id="26d42-111">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufrechnung** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="26d42-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="26d42-112">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="26d42-112">Choose the **New** action.</span></span> <span data-ttu-id="26d42-113">Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="26d42-113">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="26d42-114">Klicken Sie im Inforegister **Zeilen** und wählen die  Aktionen **Wareneingangszeilen holen**.</span><span class="sxs-lookup"><span data-stu-id="26d42-114">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="26d42-115">Wählen Sie die Wareneingangszeilen aus, die in der Rechnung enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="26d42-115">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="26d42-116">Wenn Sie eine falsche Wareneingangszeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Einkaufsrechnung löschen und die Funktion **Wareneingangszeilen holen** erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="26d42-116">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="26d42-117">Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="26d42-117">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="26d42-118">Offene Einkaufsreklamationen nach kombinierter Lieferungsbuchung entfernen</span><span class="sxs-lookup"><span data-stu-id="26d42-118">To remove open purchase orders after combined receipt posting</span></span>  
1. <span data-ttu-id="26d42-119">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verrechnete Verkaufsaufträge löschen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="26d42-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="26d42-120">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="26d42-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="26d42-121">.</span><span class="sxs-lookup"><span data-stu-id="26d42-121">.</span></span>
3. <span data-ttu-id="26d42-122">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="26d42-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="26d42-123">Alternativ löschen Sie die jeweiligen Aufträge manuell.</span><span class="sxs-lookup"><span data-stu-id="26d42-123">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="26d42-124">Wiederholen Sie die Schritte 1 bis 3 für alle betroffenen anderen Belege, wie z. B. Rahmenbestellungen.</span><span class="sxs-lookup"><span data-stu-id="26d42-124">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="26d42-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26d42-125">See Also</span></span>  
[<span data-ttu-id="26d42-126">Einkauf</span><span class="sxs-lookup"><span data-stu-id="26d42-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="26d42-127">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26d42-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

