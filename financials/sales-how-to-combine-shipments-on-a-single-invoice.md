---
title: 'Vorgehensweise: Zusammenfassen von Lieferungen in einer einzelnen Rechnung | Microsoft Docs'
description: "Wenn Sie mehr als eine Lieferung gleichzeitig fakturieren möchten, können Sie die Funktion zum Erstellen von Sammelrechnungen verwenden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e6be50119da5c617ce6dbf603903266f9ced821e
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="9393e-103">Vorgehensweise: Zusammenfassen von Lieferungen in einer einzelnen Rechnung</span><span class="sxs-lookup"><span data-stu-id="9393e-103">How to: Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="9393e-104">Wenn Sie mehr als eine Lieferung gleichzeitig fakturieren möchten, können Sie die Funktion zum Erstellen von Sammelrechnungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9393e-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

 <span data-ttu-id="9393e-105">Bevor Sie eine Sammelrechnung erstellen können, müssen Sie mehr als eine Verkaufslieferung für den gleichen Debitor in der gleichen Währung gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="9393e-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="9393e-106">Anders ausgedrückt, Sie müssen zwei oder mehr Verkaufsaufträge erstellt und als geliefert (aber nicht fakturiert) gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="9393e-106">In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced.</span></span> <span data-ttu-id="9393e-107">Um Lieferungen zu kombinieren, muss das Kontrollkästchen **Sammelrechnung** im Inforegister **Lieferung** der Karte **Debitor** aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="9393e-107">To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.</span></span>  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="9393e-108">So kombinieren Sie Lieferungen manuell auf einer einzigen Rechnung:</span><span class="sxs-lookup"><span data-stu-id="9393e-108">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="9393e-109">Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsrechnung** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="9393e-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9393e-110">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="9393e-110">Choose the **New** action.</span></span> <span data-ttu-id="9393e-111">Weitere Informationen finden Sie unter [Gewusst wie: Rechnungsverkäufe](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="9393e-111">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="9393e-112">Wählen Sie im Feld **Verk. an Deb.-Nr.**</span><span class="sxs-lookup"><span data-stu-id="9393e-112">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="9393e-113">Feld, geben Sie den Debitor ein, der die Rechnung für die gelieferten Artikel erhält.</span><span class="sxs-lookup"><span data-stu-id="9393e-113">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="9393e-114">Klicken Sie im Inforegister **Zeilen** und wählen die  Aktionen **Warenverandszeilen holen**.</span><span class="sxs-lookup"><span data-stu-id="9393e-114">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="9393e-115">Wählen Sie die Lieferzeile aus, die in die Rechnung aufgenommen werden soll:</span><span class="sxs-lookup"><span data-stu-id="9393e-115">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="9393e-116">Um alle Zeilen einzufügen, wählen Sie alle Zeilen aus, und wählen Sie die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="9393e-116">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="9393e-117">Um spezifische Zeilen einzufügen, wählen Sie die Zeilen aus, und wählen Sie die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="9393e-117">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="9393e-118">Sie können die Ctrl-Taste verwenden, um mehrere nicht unmittelbar aufeinander folgende Zeilen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9393e-118">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="9393e-119">Wenn Sie eine falsche Lieferzeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Rechnung löschen und die Funktion **Lieferzeilen holen** erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="9393e-119">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="9393e-120">Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="9393e-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="9393e-121">So kombinieren Sie Lieferungen automatisch in einer einzigen Rechnung:</span><span class="sxs-lookup"><span data-stu-id="9393e-121">To automatically combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="9393e-122">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Versand kombinieren** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="9393e-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="9393e-123">Das Anforderungsfenster "Batchauftrag" wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9393e-123">The batch job request window opens.</span></span>  
2. <span data-ttu-id="9393e-124">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="9393e-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="9393e-125">Wählen Sie das Kontrollkästchen **Rechnungen buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="9393e-125">Select the **Post Invoices** check box.</span></span>  
4.  <span data-ttu-id="9393e-126">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9393e-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9393e-127">Die Rechnungen müssen manuell gebucht werden, wenn das Kontrollkästchen **Rechnungen buchen** für die Stapelverarbeitung nicht aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="9393e-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="9393e-128">Offene Verkaufsaufträge nach kombinierter Lieferungsbuchung entfernen</span><span class="sxs-lookup"><span data-stu-id="9393e-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="9393e-129">Wenn Lieferungen in einer Rechnung zusammengefasst und gebucht werden, wird für die fakturierten Zeilen eine gebuchte Verkaufsrechnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="9393e-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="9393e-130">Das Feld **Fakturierte Menge** auf dem Ursprungsrahmenauftrag oder dem Auftrag wird ausgehend von der fakturierten Menge aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9393e-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="9393e-131">Werden Lieferungen auf diese Weise fakturiert, bleiben die Aufträge, aus denen die Lieferungen gebucht werden, weiterhin bestehen, auch wenn sie vollständig geliefert und fakturiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9393e-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="9393e-132">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Erledigte Aufträge löschen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="9393e-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="9393e-133">Wählen Sie im Feld **Kontonummer**</span><span class="sxs-lookup"><span data-stu-id="9393e-133">Specify in the **No.**</span></span> <span data-ttu-id="9393e-134">Filterfeld an, welche Verkaufsaufträge zu löschen sind.</span><span class="sxs-lookup"><span data-stu-id="9393e-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="9393e-135">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9393e-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="9393e-136">Sie können die einzelnen Verkaufsaufträge auch manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="9393e-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="9393e-137">Wiederholen Sie die Schritte 1 bis 3 für alle betroffenen anderen Belege, wie z. B. leere Verkaufsaufträge.</span><span class="sxs-lookup"><span data-stu-id="9393e-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="9393e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9393e-138">See Also</span></span>  
[<span data-ttu-id="9393e-139">Verkauf</span><span class="sxs-lookup"><span data-stu-id="9393e-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="9393e-140">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9393e-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

