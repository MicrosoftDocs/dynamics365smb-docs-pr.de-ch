---
title: Erstellen Sie einen Verkaufsauftrag, der mit einer Einkaufsbestellung für eine direkte Lieferung verknüpft ist | Microsoft Docs
description: Beschreibt, wie Sie einen Verkaufsauftrag erstellen, der mit einer Bestellung verknüpft ist, um sicherzustellen, dass die Artikel vom Kreditor direkt an den Debitor versendet werden
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7a87023445ea10aa19cc0cc4f60d76ce4cf3e365
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "929373"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="a68ad-103">Direktlieferungen machen</span><span class="sxs-lookup"><span data-stu-id="a68ad-103">Make Drop Shipments</span></span>
<span data-ttu-id="a68ad-104">Eine Direktlieferung ist die Lieferung von Artikeln, von einem Ihrer Kreditoren direkt an einen Ihrer Debitoren.</span><span class="sxs-lookup"><span data-stu-id="a68ad-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="a68ad-105">Wenn ein Verkaufsauftrag für Direktlieferung markiert wird und Sie eine Bestellung erstellen, in der der Debitor im Feld **Verk. an Deb.-Nr.**</span><span class="sxs-lookup"><span data-stu-id="a68ad-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="a68ad-106">angegeben wird, können Sie die beiden Belege verknüpfen und somit den Kreditor anweisen, direkt an den Kunden zu versenden.</span><span class="sxs-lookup"><span data-stu-id="a68ad-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="a68ad-107">So erstellen Sie einen Verkaufsauftrag für eine Direktlieferung</span><span class="sxs-lookup"><span data-stu-id="a68ad-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="a68ad-108">Um eine Direktlieferung vorzubereiten, erstellen Sie einen normalen Verkaufsauftrag für einen Artikel, ausser dass Sie in der Verkaufsauftragszeile angeben müssen, dass für den Verkauf Direktlieferung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a68ad-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="a68ad-109">Legen Sie einen Verkaufsauftrag für einen Artikel an.</span><span class="sxs-lookup"><span data-stu-id="a68ad-109">Create a sales order for an item.</span></span> <span data-ttu-id="a68ad-110">Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)</span><span class="sxs-lookup"><span data-stu-id="a68ad-110">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="a68ad-111">Aktivieren Sie in der Verkaufsauftragszeile für den Direktlieferungsartikel das Kontrollkästchen **Direktlieferung**.</span><span class="sxs-lookup"><span data-stu-id="a68ad-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="a68ad-112">Verwenden Sie die Funktion **Spalten auswählen**, wenn das Feld nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="a68ad-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="a68ad-113">Weitere Informationen finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="a68ad-113">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="a68ad-114">So erstellen Sie Bestellungen für Direktlieferungen:</span><span class="sxs-lookup"><span data-stu-id="a68ad-114">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="a68ad-115">Um eine Direktlieferung für den Artikel, der verkauft werden soll, vorzubereiten, erstellen Sie eine normale Bestellung, ausser dass Sie in der Bestellung angeben müssen, dass direkt an den Debitoren geliefert wird, nicht an Sie selbst.</span><span class="sxs-lookup"><span data-stu-id="a68ad-115">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="a68ad-116">Erstellen Sie eine Bestellung.</span><span class="sxs-lookup"><span data-stu-id="a68ad-116">Create a purchase order.</span></span> <span data-ttu-id="a68ad-117">Füllen Sie keines dieser Felder in den Zeilen aus.</span><span class="sxs-lookup"><span data-stu-id="a68ad-117">Do not fill any fields on the lines.</span></span> <span data-ttu-id="a68ad-118">Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="a68ad-118">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="a68ad-119">Wählen Sie im Feld **Verk. an Deb.-Nr.**</span><span class="sxs-lookup"><span data-stu-id="a68ad-119">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="a68ad-120">den Debitor aus, an die Sie verkaufen.</span><span class="sxs-lookup"><span data-stu-id="a68ad-120">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="a68ad-121">Wählen Sie die Aktion **Direktlieferungen** aus, und dann die Aktion **Auftrag holen**.</span><span class="sxs-lookup"><span data-stu-id="a68ad-121">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="a68ad-122">Auf der Seite **Verkaufsliste** wählen Sie den Auftrag, den Sie im Abschnitt [So erstellen Sie einen Verkaufsauftrag für Direktlieferung](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment) vorbereitet haben.</span><span class="sxs-lookup"><span data-stu-id="a68ad-122">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="a68ad-123">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a68ad-123">Choose the **OK** button.</span></span>

<span data-ttu-id="a68ad-124">Die Zeileninformation aus dem Auftrag werden in die Bestellzeile eingetragen.</span><span class="sxs-lookup"><span data-stu-id="a68ad-124">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="a68ad-125">Sie können nun den Kreditor anweisen, die Artikel an Ihren Kunden zu versenden, indem Sie ihm beispielsweise die Bestellung als PDF-Datei senden.</span><span class="sxs-lookup"><span data-stu-id="a68ad-125">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="a68ad-126">So zeigen Sie den verknüpften Auftrag aus der Bestellung an</span><span class="sxs-lookup"><span data-stu-id="a68ad-126">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="a68ad-127">Wählen Sie die Verkaufsauftragszeile der Direktlieferung aus, dann die Aktion **Bestellung**, die Aktion **Direktlieferung** und die Aktion **Bestellung**.</span><span class="sxs-lookup"><span data-stu-id="a68ad-127">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="a68ad-128">So buchen Sie eine Direktlieferung:</span><span class="sxs-lookup"><span data-stu-id="a68ad-128">To post a drop shipment</span></span>
<span data-ttu-id="a68ad-129">Wenn der Kreditor die Artikel geliefert hat, können Sie den Verkaufsauftrag als geliefert buchen.</span><span class="sxs-lookup"><span data-stu-id="a68ad-129">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="a68ad-130">Sie können auch die Bestellung buchen, aber nur mit der Option **Erhalten** bis der Verkaufsauftrag fakturiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a68ad-130">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="a68ad-131">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a68ad-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="a68ad-132">Öffnen Sie den Verkaufsauftrag, den Sie in [So erstellen Sie einen Verkaufsauftrag für Direktlieferung]() erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="a68ad-132">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="a68ad-133">Geben Sie im Feld **Zu liefernde Menge** an, wieviele der Bestellmengen geliefert werden sollen, die gesamte Menge oder eine Teilmenge.</span><span class="sxs-lookup"><span data-stu-id="a68ad-133">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="a68ad-134">Wählen Sie die Aktion **Buchen** oder **Buchen und Senden** aus.</span><span class="sxs-lookup"><span data-stu-id="a68ad-134">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="a68ad-135">Wählen Sie dann entweder die Option **Liefern**, um zu einem späteren Zeitpunkt zu fakturieren oder **Liefern und Fakturieren**, um sofort zu fakturieren.</span><span class="sxs-lookup"><span data-stu-id="a68ad-135">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="a68ad-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a68ad-136">See Also</span></span>
[<span data-ttu-id="a68ad-137">Spezialaufträge erstellen:</span><span class="sxs-lookup"><span data-stu-id="a68ad-137">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="a68ad-138">Einkauf von Artikeln für einen Verkauf</span><span class="sxs-lookup"><span data-stu-id="a68ad-138">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="a68ad-139">Produkte verkaufen</span><span class="sxs-lookup"><span data-stu-id="a68ad-139">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="a68ad-140">Erfassen eines Einkaufs</span><span class="sxs-lookup"><span data-stu-id="a68ad-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="a68ad-141">Verkauf</span><span class="sxs-lookup"><span data-stu-id="a68ad-141">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="a68ad-142">Lagerbesttand</span><span class="sxs-lookup"><span data-stu-id="a68ad-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="a68ad-143">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a68ad-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
