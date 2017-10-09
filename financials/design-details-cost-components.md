---
title: 'Designdetails: Kostenkomponenten | Microsoft Docs'
description: "Kostenkomponenten sind unterschiedliche Arten von Kosten, die den Wert eines Lagerzugangs erhöhen oder vermindern."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0a134142bfcb11692ed6157e873fcfa2900b9222
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-cost-components"></a><span data-ttu-id="f0b3b-103">Designdetails: Kostenkomponenten</span><span class="sxs-lookup"><span data-stu-id="f0b3b-103">Design Details: Cost Components</span></span>
<span data-ttu-id="f0b3b-104">Kostenkomponenten sind unterschiedliche Arten von Kosten, die den Wert eines Lagerzugangs erhöhen oder vermindern.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-104">Cost components are different types of costs that make up the value of an inventory increase or decrease.</span></span>  

 <span data-ttu-id="f0b3b-105">Die folgende Tabelle zeigt die verschiedenen Kostenkomponenten und alle untergeordneten Kostenkomponenten an, aus denen sie bestehen.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-105">The following table shows the different cost components and any subordinate cost components that they consist of.</span></span>  

|<span data-ttu-id="f0b3b-106">Kostenkomponenten</span><span class="sxs-lookup"><span data-stu-id="f0b3b-106">Cost Component</span></span>|<span data-ttu-id="f0b3b-107">Unterstellte Kostenkomponente</span><span class="sxs-lookup"><span data-stu-id="f0b3b-107">Subordinate Cost Component</span></span>|<span data-ttu-id="f0b3b-108">Description</span><span class="sxs-lookup"><span data-stu-id="f0b3b-108">Description</span></span>|  
|--------------------|--------------------------------|---------------------------------------|  
|<span data-ttu-id="f0b3b-109">Direkte Kosten</span><span class="sxs-lookup"><span data-stu-id="f0b3b-109">Direct cost</span></span>|<span data-ttu-id="f0b3b-110">Einstandspreis (Preis des direkten Kaufs)</span><span class="sxs-lookup"><span data-stu-id="f0b3b-110">Unit cost (direct purchase price)</span></span>|<span data-ttu-id="f0b3b-111">Kosten, die direkt auf das Kostenobjekt zurückzuführen sind.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-111">Cost that can be traced to a cost object.</span></span>|  
|<span data-ttu-id="f0b3b-112">Direkte Kosten</span><span class="sxs-lookup"><span data-stu-id="f0b3b-112">Direct cost</span></span>|<span data-ttu-id="f0b3b-113">Fracht Kosten (Artikelgebühren)</span><span class="sxs-lookup"><span data-stu-id="f0b3b-113">Freight cost (item charge)</span></span>|<span data-ttu-id="f0b3b-114">Kosten, die direkt auf das Kostenobjekt zurückzuführen sind.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-114">Cost that can be traced to a cost object.</span></span>|  
|<span data-ttu-id="f0b3b-115">Direkte Kosten</span><span class="sxs-lookup"><span data-stu-id="f0b3b-115">Direct cost</span></span>|<span data-ttu-id="f0b3b-116">Versicherungskosten (Artikelgebühren)</span><span class="sxs-lookup"><span data-stu-id="f0b3b-116">Insurance cost (item charge)</span></span>|<span data-ttu-id="f0b3b-117">Kosten, die direkt auf das Kostenobjekt zurückzuführen sind.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-117">Cost that can be traced to a cost object.</span></span>|  
|<span data-ttu-id="f0b3b-118">Indirekte Kosten</span><span class="sxs-lookup"><span data-stu-id="f0b3b-118">Indirect cost</span></span>||<span data-ttu-id="f0b3b-119">Kosten, die nicht auf ein Kostenobjekt zurückzuführen sind.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-119">Cost that cannot be traced to a cost object.</span></span>|  
|<span data-ttu-id="f0b3b-120">Abweichung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-120">Variance</span></span>|<span data-ttu-id="f0b3b-121">Einkaufsabweichung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-121">Purchase variance</span></span>|<span data-ttu-id="f0b3b-122">Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-122">The difference between actual and standard costs, which is only posted for items using the **Standard** costing method.</span></span>|  
|<span data-ttu-id="f0b3b-123">Abweichung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-123">Variance</span></span>|<span data-ttu-id="f0b3b-124">Materialabweichung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-124">Material variance</span></span>|<span data-ttu-id="f0b3b-125">Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-125">The difference between actual and standard costs, which is only posted for items using the **Standard** costing method.</span></span>|  
|<span data-ttu-id="f0b3b-126">Abweichung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-126">Variance</span></span>|<span data-ttu-id="f0b3b-127">Kapazitätsabweichung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-127">Capacity variance</span></span>|<span data-ttu-id="f0b3b-128">Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-128">The difference between actual and standard costs, which is only posted for items using the **Standard** costing method.</span></span>|  
|<span data-ttu-id="f0b3b-129">Abweichung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-129">Variance</span></span>|<span data-ttu-id="f0b3b-130">Fremdarbeitskostenabweichung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-130">Subcontracted variance</span></span>|<span data-ttu-id="f0b3b-131">Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-131">The difference between actual and standard costs, which is only posted for items using the **Standard** costing method.</span></span>|  
|<span data-ttu-id="f0b3b-132">Abweichung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-132">Variance</span></span>|<span data-ttu-id="f0b3b-133">Abweichung Kapazitätsgemeinkosten</span><span class="sxs-lookup"><span data-stu-id="f0b3b-133">Capacity overhead variance</span></span>|<span data-ttu-id="f0b3b-134">Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-134">The difference between actual and standard costs, which is only posted for items using the **Standard** costing method.</span></span>|  
|<span data-ttu-id="f0b3b-135">Abweichung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-135">Variance</span></span>|<span data-ttu-id="f0b3b-136">Prod.-Gemeinkostenabw.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-136">Manufacturing overhead variance</span></span>|<span data-ttu-id="f0b3b-137">Der Unterschied zwischen tatsächlichen Kosten und dem Einstandspreis (fest), der nur für Artikel mit der Lagerabgangsmethode **Standard** gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-137">The difference between actual and standard costs, which is only posted for items using the **Standard** costing method.</span></span>|  
|<span data-ttu-id="f0b3b-138">Neubewertung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-138">Revaluation</span></span>||<span data-ttu-id="f0b3b-139">Eine Abschreibung oder ein Wertzuwachs für den aktuellen Lagerwert.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-139">A depreciation or appreciation of the current inventory value.</span></span>|  
|<span data-ttu-id="f0b3b-140">Rundung</span><span class="sxs-lookup"><span data-stu-id="f0b3b-140">Rounding</span></span>||<span data-ttu-id="f0b3b-141">Restbeträge, die durch die Berechnung von Bestandsminderungen entstehen.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-141">Residuals caused by the way in which valuation of inventory decreases are calculated.</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="f0b3b-142">Fracht- und Versicherungskosten sind Artikel-Gebühren, die jederzeit zu den Kosten des Artikels addiert werden können.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-142">Freight and insurance costs are item charges that can be added to an item’s cost at any time.</span></span> <span data-ttu-id="f0b3b-143">Wenn Sie die Stapelverarbeitung **Artikeleintrag Kosten anpassen** ausführen, wird der Wert aller zugehörigen Lagerabgänge entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-143">When you run the **Adjust Cost - Item Entries** batch job, the value of any related inventory decreases are updated accordingly.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f0b3b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0b3b-144">See Also</span></span>  
 <span data-ttu-id="f0b3b-145">[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="f0b3b-145">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
 <span data-ttu-id="f0b3b-146">[Designdetails: Abweichungen](design-details-variance.md) [Verwalten der Lagerkosten](finance-manage-inventory-costs.md)</span><span class="sxs-lookup"><span data-stu-id="f0b3b-146">[Design Details: Variance](design-details-variance.md) [Managing Inventory Costs](finance-manage-inventory-costs.md)</span></span>  
 [<span data-ttu-id="f0b3b-147">Finanzen</span><span class="sxs-lookup"><span data-stu-id="f0b3b-147">Finance</span></span>](finance.md)  
 <span data-ttu-id="f0b3b-148">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f0b3b-148">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
