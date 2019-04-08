---
title: 'Vorgehensweise: Titel-Beziehungen zwischen Bedarf und Vorrat | Microsoft Docs'
description: Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: de71e4c305b775df8c10306ecc474bc6944d0787
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "819824"
---
# <a name="track-relations-between-demand-and-supply"></a><span data-ttu-id="fd37b-103">Nachverfolgen von Beziehungen zwischen Bedarf und Vorrat</span><span class="sxs-lookup"><span data-stu-id="fd37b-103">Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="fd37b-104">Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist</span><span class="sxs-lookup"><span data-stu-id="fd37b-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="fd37b-105">Die Planungsvorschläge beinhalten zusätzliche Planungsinformationen wie  Nachverfolgung zu nicht auftragsbezogenen Entitäten und  Warnungen, um den Planer bei der Erstellung eines optimalen Beschaffungsplans zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fd37b-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="fd37b-106">Weitere Informationen finden Sie unter [Planungselement ohne Bedarfsverursacher](production-how-track-demand-supply.md#untracked-planning-elements).</span><span class="sxs-lookup"><span data-stu-id="fd37b-106">For more information, see [Untracked Planning Elements](production-how-track-demand-supply.md#untracked-planning-elements).</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="fd37b-107">Um verknüpfte Artikel zu verfolgen</span><span class="sxs-lookup"><span data-stu-id="fd37b-107">To track linked items</span></span>
<span data-ttu-id="fd37b-108">Das Tracking zeigt, wie Verkaufsaufträge, Fertigungsaufträge und Bestellungen über Reservierungen mit einem Fertigungsauftrag verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="fd37b-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="fd37b-109">Nachfolgend wird erläutert, wie Artikel für einen fest geplanten Fertigungsauftrag verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="fd37b-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="fd37b-110">Die Schritte sind für alle anderen Auftragsarten und der Planungsvorschlagszeilen ähnlich.</span><span class="sxs-lookup"><span data-stu-id="fd37b-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="fd37b-111">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Fest geplante Produktionsauftrag** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="fd37b-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="fd37b-112">Öffnen Sie den relevanten fest geplanten Fertigungsauftrag in der Liste.</span><span class="sxs-lookup"><span data-stu-id="fd37b-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="fd37b-113">Wählen Sie im Inforegister **Zeilen** in Aktionen **Funktion** aus, und wählen Sie dann **Auftragstracking**.</span><span class="sxs-lookup"><span data-stu-id="fd37b-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="fd37b-114">In den Zeilen im Fenster **Auftragstracking**werden die Belege angezeigt, die sich auf die aktuelle Fertigungsauftragszeile beziehen.</span><span class="sxs-lookup"><span data-stu-id="fd37b-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="fd37b-115">Planungselemente ohne Bedarfsverursacher</span><span class="sxs-lookup"><span data-stu-id="fd37b-115">Untracked Planning Elements</span></span>
<span data-ttu-id="fd37b-116">Die Seite**Planungselemente ohne Bedarfsverursacher** öffnet sich, wenn Sie das Feld **Mge. ohne Bedarfsverursacher** auf der Seite **Auftragsplanung** auswählen.</span><span class="sxs-lookup"><span data-stu-id="fd37b-116">The **Untracked Planning Elements** page opens when you choose the **Untracked Qty.** field on the **order Planning** page.</span></span> <span data-ttu-id="fd37b-117">Er dient beiden Zwecken:</span><span class="sxs-lookup"><span data-stu-id="fd37b-117">It serves two purposes:</span></span>

1. <span data-ttu-id="fd37b-118">Sie enthält Informationen zu Mengen ohne Bedarfsverursacher, die angezeigt werden, wenn der Benutzer auf der Seite "Bedarfsverursacher" Mengen ohne Bedarfsverursacher aufruft.</span><span class="sxs-lookup"><span data-stu-id="fd37b-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking page to see untracked quantities.</span></span>
2. <span data-ttu-id="fd37b-119">Sie enthält Warnmeldungen, die angezeigt werden, wenn der Benutzer auf der Seite **Planungsvorschlag** auf ein **Warnungs**-Symbol klickt.</span><span class="sxs-lookup"><span data-stu-id="fd37b-119">To hold warning messages displayed when the user chooses the **Warning** icon on the **Planning Worksheet** page.</span></span>

<span data-ttu-id="fd37b-120">Die Seite enthält Posten, die eine Überschussmenge ohne Bedarfsverursacher im Bedarfsverursachernetzwerk ausweisen.</span><span class="sxs-lookup"><span data-stu-id="fd37b-120">The page contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="fd37b-121">Diese Posten werden während der Planung erzeugt und zeigen die Herkunft der Überschussmenge ohne Bedarfsverursacher in den Bedarfsverursacherzeilen.</span><span class="sxs-lookup"><span data-stu-id="fd37b-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="fd37b-122">Die folgende Herkunft ist für den Überschuss ohne Bedarfsverursacher möglich:</span><span class="sxs-lookup"><span data-stu-id="fd37b-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="fd37b-123">Absatzplanung</span><span class="sxs-lookup"><span data-stu-id="fd37b-123">Production forecast</span></span>
- <span data-ttu-id="fd37b-124">Rahmenbestellungen</span><span class="sxs-lookup"><span data-stu-id="fd37b-124">Blanket orders</span></span>
- <span data-ttu-id="fd37b-125">Sicherheitsbestand</span><span class="sxs-lookup"><span data-stu-id="fd37b-125">Safety stock quantity</span></span>
- <span data-ttu-id="fd37b-126">Minimalbestand</span><span class="sxs-lookup"><span data-stu-id="fd37b-126">Reorder point</span></span>
- <span data-ttu-id="fd37b-127">Maximalbestand</span><span class="sxs-lookup"><span data-stu-id="fd37b-127">Maximum inventory</span></span>
- <span data-ttu-id="fd37b-128">Bestellmenge</span><span class="sxs-lookup"><span data-stu-id="fd37b-128">Reorder quantity</span></span>
- <span data-ttu-id="fd37b-129">Maximale Losgrösse</span><span class="sxs-lookup"><span data-stu-id="fd37b-129">Maximum order quantity</span></span>
- <span data-ttu-id="fd37b-130">Minimale Losgrösse</span><span class="sxs-lookup"><span data-stu-id="fd37b-130">Minimum order quantity</span></span>
- <span data-ttu-id="fd37b-131">Losgrössenrundungsfaktor</span><span class="sxs-lookup"><span data-stu-id="fd37b-131">Order multiple</span></span>
- <span data-ttu-id="fd37b-132">Toleranz (% der Losgrösse)</span><span class="sxs-lookup"><span data-stu-id="fd37b-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="fd37b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd37b-133">See Also</span></span>  
<span data-ttu-id="fd37b-134">[Planung](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="fd37b-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="fd37b-135">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="fd37b-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="fd37b-136">[Bearbeitungen](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="fd37b-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="fd37b-137">Lagerbesttand</span><span class="sxs-lookup"><span data-stu-id="fd37b-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="fd37b-138">Einkauf</span><span class="sxs-lookup"><span data-stu-id="fd37b-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="fd37b-139">Designdetails: Reservierung, Tracking und Aktionsmeldungen</span><span class="sxs-lookup"><span data-stu-id="fd37b-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="fd37b-140">[Designdetails: Vorratsplanung](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="fd37b-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="fd37b-141">Bewährte Einrichtungsmethoden: Beschaffungsplanung</span><span class="sxs-lookup"><span data-stu-id="fd37b-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="fd37b-142">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fd37b-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
