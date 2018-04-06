---
title: "Designdetails: Unter dem Überlaufmenge bleiben | Microsoft Docs"
description: "Wenn die Funktionen Auffüllen auf Maximalbestand Feste Bestellmenge verwendet werden, konzentriert sich das Planungssystem nur auf den voraussichtlichen Lagerbestand in dem vorgegebenen Zeitrahmen. Dies bedeutet, dass das Planungssystem möglicherweise überflüssigen Vorrat vorschlägt, wenn negativer Bedarfs- oder positive Vorratsänderungen ausserhalb gegebenen Zeitrahmens auftreten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2fc2ef2528a1edc85c0a7694c1afc5bec7a0065a
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-staying-under-the-overflow-level"></a><span data-ttu-id="84a34-104">Designdetails: Unter dem Überlauflevel bleiben</span><span class="sxs-lookup"><span data-stu-id="84a34-104">Design Details: Staying under the Overflow Level</span></span>
<span data-ttu-id="84a34-105">Wenn die Funktionen Auffüllen auf Maximalbestand Feste Bestellmenge verwendet werden, konzentriert sich das Planungssystem nur auf den voraussichtlichen Lagerbestand in dem vorgegebenen Zeitrahmen.</span><span class="sxs-lookup"><span data-stu-id="84a34-105">When using the Maximum Qty. and Fixed Reorder Qty. policies, the planning system focuses on the projected inventory in the given time-bucket only.</span></span> <span data-ttu-id="84a34-106">Dies bedeutet, dass das Planungssystem möglicherweise überflüssigen Vorrat vorschlägt, wenn negativer Bedarfs- oder positive Vorratsänderungen ausserhalb gegebenen Zeitrahmens auftreten.</span><span class="sxs-lookup"><span data-stu-id="84a34-106">This means that the planning system may suggest superfluous supply when negative demand or positive supply changes occur outside of the given time bucket.</span></span> <span data-ttu-id="84a34-107">Wenn aus diesem Grund ein überflüssiger Vorrat vorgeschlagen wird, berechnet das Planungssystem die zu reduzierende oder zu löschende Vorratsmenge, um überflüssigen Vorrat zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="84a34-107">If, for this reason, a superfluous supply is suggested, the planning system calculates which quantity the supply should be decreased to (or deleted) to avoid the superfluous supply.</span></span> <span data-ttu-id="84a34-108">Diese Menge wird als "Überlaufmenge" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="84a34-108">This quantity is called the “overflow level.”</span></span> <span data-ttu-id="84a34-109">Diese Menge wird als "Überlauflevel" bezeichnet. Der Überlauf wird als Planungszeile mit einer **Menge ändern** oder **Abbrechen** Operation und der folgenden Warnmeldung mitgeteilt:</span><span class="sxs-lookup"><span data-stu-id="84a34-109">The overflow is communicated as a planning line with a **Change Qty. (Decrease)** or **Cancel** action and the following warning message:</span></span>  

<span data-ttu-id="84a34-110">*Achtung: Der voraussichtliche Lagerbestand [xx] ist höher als das Überlauflevel [xx] am Fälligkeitsdatum [xx].*</span><span class="sxs-lookup"><span data-stu-id="84a34-110">*Attention: The projected inventory [xx] is higher than the overflow level [xx] on the Due Date [xx].*</span></span>  

<span data-ttu-id="84a34-111">![Lagerüberlaufmenge](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span><span class="sxs-lookup"><span data-stu-id="84a34-111">![Inventory overflow level](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span></span>  

##  <a name="calculating-the-overflow-level"></a><span data-ttu-id="84a34-112">Berechnung des Überlauflevels</span><span class="sxs-lookup"><span data-stu-id="84a34-112">Calculating the Overflow Level</span></span>  
<span data-ttu-id="84a34-113">Das Überlauflevel wird auf verschiedene Arten abhängig vom Planungssetup berechnet.</span><span class="sxs-lookup"><span data-stu-id="84a34-113">The overflow level is calculated in different ways depending on planning setup.</span></span>  

### <a name="maximum-qty-reordering-policy"></a><span data-ttu-id="84a34-114">Auffüllen auf Maximalbestand. Wiederbeschaffungsverfahren</span><span class="sxs-lookup"><span data-stu-id="84a34-114">Maximum Qty. reordering policy</span></span>  
<span data-ttu-id="84a34-115">Überlauflevel = Maximalbestand</span><span class="sxs-lookup"><span data-stu-id="84a34-115">Overflow level = Maximum Inventory</span></span>  

> [!NOTE]  
>  <span data-ttu-id="84a34-116">Wenn eine Auftragsmindestmenge existiert, wird sie wie folgt hinzugefügt: Überlauflevel-= Maximalbestand-+ Auftragsmindestmenge.</span><span class="sxs-lookup"><span data-stu-id="84a34-116">If a minimum order quantity exists, then it will be added as follows: Overflow level = Maximum Inventory + Minimum Order Quantity.</span></span>  

### <a name="fixed-reorder-qty-reordering-policy"></a><span data-ttu-id="84a34-117">Nachbestellungsrichtlinie Feste Bestellmenge</span><span class="sxs-lookup"><span data-stu-id="84a34-117">Fixed Reorder Qty. reordering policy</span></span>  
<span data-ttu-id="84a34-118">Überlauflevel = Bestellmenge + Minimalbestand</span><span class="sxs-lookup"><span data-stu-id="84a34-118">Overflow level = Reorder Quantity + Reorder Point</span></span>  

> [!NOTE]  
>  <span data-ttu-id="84a34-119">Wenn die Mindestauftragsgrösse höher als der Minimalbestand ist, dann werden folgende Ersetzungen vorgenommen: Überlauflevel-= Bestellmenge + Mindestauftragsgrösse</span><span class="sxs-lookup"><span data-stu-id="84a34-119">If the minimum order quantity is higher than the reorder point, then it will replace as follows: Overflow Level = Reorder Quantity + Minimum Order Quantity</span></span>  

### <a name="order-multiple"></a><span data-ttu-id="84a34-120">Losgrössenrundungsfaktor</span><span class="sxs-lookup"><span data-stu-id="84a34-120">Order Multiple</span></span>  
<span data-ttu-id="84a34-121">Wenn ein Auftragsvielfaches vorhanden ist, reguliert dieses den Überlauflevel für die Wiederbeschaffungsverfahren Höchstmenge und Feste Nachbestellmenge.</span><span class="sxs-lookup"><span data-stu-id="84a34-121">If an order multiple exists, then it will adjust the overflow level for both Maximum Qty. and Fixed Reorder Qty. reordering policies.</span></span>  

##  <a name="creating-the-planning-line-with-overflow-warning"></a><span data-ttu-id="84a34-122">Erstellen der Planungszeile mit Überlaufwarnmeldung</span><span class="sxs-lookup"><span data-stu-id="84a34-122">Creating the Planning Line with Overflow Warning</span></span>  
<span data-ttu-id="84a34-123">Wenn eine vorhandene Lieferung dazu führt, dass der voraussichtliche Lagerbestand höher ist, als das Überlauflevel am Ende eines Zeitrahmens höher, wird eine Planungszeile erstellt.</span><span class="sxs-lookup"><span data-stu-id="84a34-123">When an existing supply causes the projected inventory to be higher than the overflow level at the end of a time bucket, a planning line is created.</span></span> <span data-ttu-id="84a34-124">Um vor einem möglichen überflüssigen Vorrat zu warnen, hat die Planungszeile eine Warnmeldung, das Feld **Ereignismeldung akzeptieren** ist nicht aktiviert, und die Ereignismeldung ist entweder "Abbrechen" oder "Menge ändern".</span><span class="sxs-lookup"><span data-stu-id="84a34-124">To warn about the potential superfluous supply, the planning line has a warning message, the **Accept Action Message** field is not selected, and the action message is either Cancel or Change Qty.</span></span>  

### <a name="calculating-the-planning-line-quantity"></a><span data-ttu-id="84a34-125">Berechnen der Planungszeilenmenge</span><span class="sxs-lookup"><span data-stu-id="84a34-125">Calculating the Planning Line Quantity</span></span>  
<span data-ttu-id="84a34-126">Planungszeilen-Menge = Netzstrom-Menge - (voraussichtlicher Lagerbestand - Überlauflevel)</span><span class="sxs-lookup"><span data-stu-id="84a34-126">Planning Line Quantity = Current Supply Quantity – (Projected Inventory – Overflow Level)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="84a34-127">Wie bei allen Hinweiszeilen werden alle Max./Min.-Auftragsmengen oder Auftragsvielfache ignoriert.</span><span class="sxs-lookup"><span data-stu-id="84a34-127">As with all warning lines, any maximum/minimum order quantity or order multiple will be ignored.</span></span>  

### <a name="defining-the-action-message-type"></a><span data-ttu-id="84a34-128">Definieren des Aktionsmeldungstyps</span><span class="sxs-lookup"><span data-stu-id="84a34-128">Defining the Action Message Type</span></span>  

-   <span data-ttu-id="84a34-129">Wenn die Planungszeilenmenge höher als 0 ist, ist die Aktionsmeldung „Menge ändern“.</span><span class="sxs-lookup"><span data-stu-id="84a34-129">If the planning line quantity is higher than 0, then the action message is Change Qty.</span></span>  
-   <span data-ttu-id="84a34-130">Wenn die Planungszeilenmenge gleich oder niedriger als 0 ist, ist die Aktionsmeldung „Stornieren“.</span><span class="sxs-lookup"><span data-stu-id="84a34-130">If the planning line quantity is equal to or lower than 0, then the action message is Cancel</span></span>  

### <a name="composing-the-warning-message"></a><span data-ttu-id="84a34-131">Verfassen der Warnmeldung</span><span class="sxs-lookup"><span data-stu-id="84a34-131">Composing the Warning Message</span></span>  
<span data-ttu-id="84a34-132">Im Falle eines Überlaufs zeigt das Fenster  **Planungselement ohne Nachverfolgung** eine Warnmeldung mit den folgenden Informationen an:</span><span class="sxs-lookup"><span data-stu-id="84a34-132">In case of overflow, the **Untracked Planning Elements** window displays a warning message with the following information:</span></span>  

-   <span data-ttu-id="84a34-133">Der voraussichtliche Lagerbestand, der die Warnung ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="84a34-133">The projected inventory level that triggered the warning</span></span>  
-   <span data-ttu-id="84a34-134">Der berechnete Überlauflevel</span><span class="sxs-lookup"><span data-stu-id="84a34-134">The calculated overflow level</span></span>  
-   <span data-ttu-id="84a34-135">Das Fälligkeitsdatum des Vorratsereignisses.</span><span class="sxs-lookup"><span data-stu-id="84a34-135">The due date of the supply event.</span></span>  

<span data-ttu-id="84a34-136">Beispiel: "Der voraussichtliche Lagerbestand 120 übersteigt das Überlauflevel 60 am 28.01.11"</span><span class="sxs-lookup"><span data-stu-id="84a34-136">Example: “The projected inventory 120 is higher than the overflow level 60 on 28-01-11”</span></span>  

## <a name="scenario"></a><span data-ttu-id="84a34-137">Szenario</span><span class="sxs-lookup"><span data-stu-id="84a34-137">Scenario</span></span>  
<span data-ttu-id="84a34-138">In diesem Szenario ändert ein Kunde einen Verkaufsauftrag von 70 zu 40 Stück zwischen zwei Planungen.</span><span class="sxs-lookup"><span data-stu-id="84a34-138">In this scenario, a customer changes a sales order from 70 to 40 pieces between two planning runs.</span></span> <span data-ttu-id="84a34-139">Die Überlauffunktion reduziert den Einkauf, der für die anfängliche Verkaufsmenge vorgeschlagen worden war.</span><span class="sxs-lookup"><span data-stu-id="84a34-139">The overflow feature sets in to reduce the purchase that was suggested for the initial sales quantity.</span></span>  

### <a name="item-setup"></a><span data-ttu-id="84a34-140">Artikeleinrichtung</span><span class="sxs-lookup"><span data-stu-id="84a34-140">Item setup</span></span>  

|<span data-ttu-id="84a34-141">Wiederbeschaffungsverfahren</span><span class="sxs-lookup"><span data-stu-id="84a34-141">Reordering Policy</span></span>|<span data-ttu-id="84a34-142">Auffüllen auf Maximalbestand</span><span class="sxs-lookup"><span data-stu-id="84a34-142">Maximum Qty.</span></span>|  
|-----------------------|------------------|  
|<span data-ttu-id="84a34-143">Maximale Losgrösse</span><span class="sxs-lookup"><span data-stu-id="84a34-143">Maximum Order Quantity</span></span>|<span data-ttu-id="84a34-144">100</span><span class="sxs-lookup"><span data-stu-id="84a34-144">100</span></span>|  
|<span data-ttu-id="84a34-145">Minimalbestand</span><span class="sxs-lookup"><span data-stu-id="84a34-145">Reorder Point</span></span>|<span data-ttu-id="84a34-146">50</span><span class="sxs-lookup"><span data-stu-id="84a34-146">50</span></span>|  
|<span data-ttu-id="84a34-147">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="84a34-147">Inventory</span></span>|<span data-ttu-id="84a34-148">80</span><span class="sxs-lookup"><span data-stu-id="84a34-148">80</span></span>|  

### <a name="situation-before-sales-decrease"></a><span data-ttu-id="84a34-149">Situation vor Vertriebsabgang</span><span class="sxs-lookup"><span data-stu-id="84a34-149">Situation before sales decrease</span></span>  

|<span data-ttu-id="84a34-150">Ereignis</span><span class="sxs-lookup"><span data-stu-id="84a34-150">Event</span></span>|<span data-ttu-id="84a34-151">"Menge ändern"</span><span class="sxs-lookup"><span data-stu-id="84a34-151">Change Qty.</span></span>|<span data-ttu-id="84a34-152">Voraussichtlicher Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="84a34-152">Projected Inventory</span></span>|  
|-----------|-----------------|-------------------------|  
|<span data-ttu-id="84a34-153">Tag eins</span><span class="sxs-lookup"><span data-stu-id="84a34-153">Day one</span></span>|<span data-ttu-id="84a34-154">keine</span><span class="sxs-lookup"><span data-stu-id="84a34-154">None</span></span>|<span data-ttu-id="84a34-155">80</span><span class="sxs-lookup"><span data-stu-id="84a34-155">80</span></span>|  
|<span data-ttu-id="84a34-156">Verkauf</span><span class="sxs-lookup"><span data-stu-id="84a34-156">Sale</span></span>|<span data-ttu-id="84a34-157">-70</span><span class="sxs-lookup"><span data-stu-id="84a34-157">-70</span></span>|<span data-ttu-id="84a34-158">10</span><span class="sxs-lookup"><span data-stu-id="84a34-158">10</span></span>|  
|<span data-ttu-id="84a34-159">Ende des Zeitrahmens</span><span class="sxs-lookup"><span data-stu-id="84a34-159">End of time bucket</span></span>|<span data-ttu-id="84a34-160">keine</span><span class="sxs-lookup"><span data-stu-id="84a34-160">None</span></span>|<span data-ttu-id="84a34-161">10</span><span class="sxs-lookup"><span data-stu-id="84a34-161">10</span></span>|  
|<span data-ttu-id="84a34-162">Neue Bestellung vorschlagen</span><span class="sxs-lookup"><span data-stu-id="84a34-162">Suggest new purchase order</span></span>|<span data-ttu-id="84a34-163">+90</span><span class="sxs-lookup"><span data-stu-id="84a34-163">+90</span></span>|<span data-ttu-id="84a34-164">100</span><span class="sxs-lookup"><span data-stu-id="84a34-164">100</span></span>|  

### <a name="situation-after-sales-decrease"></a><span data-ttu-id="84a34-165">Situation nach Vertriebsabgang</span><span class="sxs-lookup"><span data-stu-id="84a34-165">Situation after sales decrease</span></span>  

|<span data-ttu-id="84a34-166">Ändern</span><span class="sxs-lookup"><span data-stu-id="84a34-166">Change</span></span>|<span data-ttu-id="84a34-167">"Menge ändern"</span><span class="sxs-lookup"><span data-stu-id="84a34-167">Change Qty.</span></span>|<span data-ttu-id="84a34-168">Voraussichtlicher Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="84a34-168">Projected Inventory</span></span>|  
|------------|-----------------|-------------------------|  
|<span data-ttu-id="84a34-169">Tag eins</span><span class="sxs-lookup"><span data-stu-id="84a34-169">Day one</span></span>|<span data-ttu-id="84a34-170">keine</span><span class="sxs-lookup"><span data-stu-id="84a34-170">None</span></span>|<span data-ttu-id="84a34-171">80</span><span class="sxs-lookup"><span data-stu-id="84a34-171">80</span></span>|  
|<span data-ttu-id="84a34-172">Verkauf</span><span class="sxs-lookup"><span data-stu-id="84a34-172">Sale</span></span>|<span data-ttu-id="84a34-173">-40</span><span class="sxs-lookup"><span data-stu-id="84a34-173">-40</span></span>|<span data-ttu-id="84a34-174">40</span><span class="sxs-lookup"><span data-stu-id="84a34-174">40</span></span>|  
|<span data-ttu-id="84a34-175">Einkauf</span><span class="sxs-lookup"><span data-stu-id="84a34-175">Purchase</span></span>|<span data-ttu-id="84a34-176">+90</span><span class="sxs-lookup"><span data-stu-id="84a34-176">+90</span></span>|<span data-ttu-id="84a34-177">130</span><span class="sxs-lookup"><span data-stu-id="84a34-177">130</span></span>|  
|<span data-ttu-id="84a34-178">Ende des Zeitrahmens</span><span class="sxs-lookup"><span data-stu-id="84a34-178">End of time bucket</span></span>|<span data-ttu-id="84a34-179">keine</span><span class="sxs-lookup"><span data-stu-id="84a34-179">None</span></span>|<span data-ttu-id="84a34-180">130</span><span class="sxs-lookup"><span data-stu-id="84a34-180">130</span></span>|  
|<span data-ttu-id="84a34-181">Vorschlagen, den Einkauf zu vermindern</span><span class="sxs-lookup"><span data-stu-id="84a34-181">Suggest to decrease purchase</span></span><br /><br /> <span data-ttu-id="84a34-182">Auftrag von 90 bis 60</span><span class="sxs-lookup"><span data-stu-id="84a34-182">order from 90 to 60</span></span>|<span data-ttu-id="84a34-183">-30</span><span class="sxs-lookup"><span data-stu-id="84a34-183">-30</span></span>|<span data-ttu-id="84a34-184">100</span><span class="sxs-lookup"><span data-stu-id="84a34-184">100</span></span>|  

### <a name="resulting-planning-lines"></a><span data-ttu-id="84a34-185">Planzeilen erstellen</span><span class="sxs-lookup"><span data-stu-id="84a34-185">Resulting Planning Lines</span></span>  
 <span data-ttu-id="84a34-186">Eine Planungszeile (Warnen) wird erstellt, um den Einkauf mit 30 von 90 auf 60 zu verringern, um den voraussichtlichen Lagerstatus auf 100 entsprechend dem Überlauflevel festzuhalten.</span><span class="sxs-lookup"><span data-stu-id="84a34-186">One planning line (warning) is created to reduce the purchase with 30 from 90 to 60 to keep the projected inventory on 100 according to the overflow level.</span></span>  

<span data-ttu-id="84a34-187">![Planung entsprechend Überlaufmenge](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span><span class="sxs-lookup"><span data-stu-id="84a34-187">![Plan according to overflow level](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="84a34-188">Ohne die Sammelfunktion werden keine Warnmeldungen erstellt, wenn der voraussichtliche Lagerbestand über Maximalbestand ist.</span><span class="sxs-lookup"><span data-stu-id="84a34-188">Without the Overflow feature, no warning is created if the projected inventory level is above maximum inventory.</span></span> <span data-ttu-id="84a34-189">Dies kann einen überflüssigen Vorrat von 30 verursachen.</span><span class="sxs-lookup"><span data-stu-id="84a34-189">This could cause a superfluous supply of 30.</span></span>  

## <a name="see-also"></a><span data-ttu-id="84a34-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84a34-190">See Also</span></span>  
<span data-ttu-id="84a34-191">[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="84a34-191">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="84a34-192">[Designdetails: Planungsparameter](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="84a34-192">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="84a34-193">[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="84a34-193">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="84a34-194">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="84a34-194">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

