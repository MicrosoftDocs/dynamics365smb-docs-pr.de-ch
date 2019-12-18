---
title: Info zu Planungsfunktionen  | Microsoft Docs
description: Das Planungssystem berücksichtigt sämtliche Bedarfs- und Vorratsdaten, saldiert die Ergebnisse und erstellt Vorschläge zum Ausgleichen des Vorrats, damit der Bedarf erfüllt werden kann.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 03ac7e30e65912a5f09d617b87c09a7b15c4f9c5
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878109"
---
# <a name="about-planning-functionality"></a><span data-ttu-id="323da-103">Info zu Planungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="323da-103">About Planning Functionality</span></span>
<span data-ttu-id="323da-104">Das Planungssystem berücksichtigt sämtliche Bedarfs- und Vorratsdaten, saldiert die Ergebnisse und erstellt Vorschläge zum Ausgleichen des Vorrats, damit der Bedarf erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="323da-104">The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.</span></span>  

<span data-ttu-id="323da-105">Weitere Informationen finden Sie unter [Designdetails: Beschaffungsplanung](design-details-supply-planning.md)</span><span class="sxs-lookup"><span data-stu-id="323da-105">For detailed information, see [Design Details: Supply Planning](design-details-supply-planning.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="323da-106">Für alle Felder, die in diesem Thema genannt werden, Lesen Sie die QuickInfo, um die Funktion zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="323da-106">For all the fields that are mentioned in this topic, read the tooltip to understand their function.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><span data-ttu-id="323da-107">Bedarf und Vorrat</span><span class="sxs-lookup"><span data-stu-id="323da-107">Demand and Supply</span></span>  
<span data-ttu-id="323da-108">Planung besteht aus zwei Elementen: Bedarf und Vorrat.</span><span class="sxs-lookup"><span data-stu-id="323da-108">Planning has two elements: demand and supply.</span></span> <span data-ttu-id="323da-109">Dieses beiden Elemente müssen einander angepasst werden, damit sichergestellt ist, dass der Bedarf rechtzeitig und kostengünstig erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="323da-109">These must be held in balance to ensure that the demand is met in a timely and cost-efficient manner.</span></span>  

- <span data-ttu-id="323da-110">Bedarf ist der Oberbegriff für jede Art von Bruttobedarf: beispielsweise Verkaufsauftrag, Serviceauftrag, Komponentenbedarf aus einem Montage- oder Fertigungsauftrag, ausgehende Umlagerung, Rahmenbestellung oder Absatzplanung.</span><span class="sxs-lookup"><span data-stu-id="323da-110">Demand is the common term used for any kind of gross requirement such as a sales order, service order, component need from assembly or production orders, outbound transfer, blanket order or forecast.</span></span> <span data-ttu-id="323da-111">Darüber hinaus erlaubt die Anwendung einige technische Arten von Bedarf, - z. B. negative Fertigungsaufträge oder Einkaufsbestellungen, negative Lagerbestände und Einkaufsreklamationen.</span><span class="sxs-lookup"><span data-stu-id="323da-111">In addition to these, application allows some other technical types of demand - such as a negative production or purchase order, negative inventory, and purchase return.</span></span>  
- <span data-ttu-id="323da-112">Vorrat ist der Oberbegriff für jede Art von Beschaffung: beispielsweise Einkaufsbestellung, Montageauftrag, Fertigungsauftrag oder eingehende Umlagerung.</span><span class="sxs-lookup"><span data-stu-id="323da-112">Supply is the common word used for any kind of replenishment such as inventory, a purchase order, assembly order, production order, or inbound transfer.</span></span> <span data-ttu-id="323da-113">Entsprechend kann es negative Verkaufs- oder Serviceaufträge, negativen Komponentenbedarf oder negative Verkaufsreklamationen geben – alle diese Elemente entsprechen in gewisser Weise ebenfalls einem Vorrat.</span><span class="sxs-lookup"><span data-stu-id="323da-113">Correspondingly, there can be a negative sales or service order, negative component need or sales return – all of which in some way also represent supply.</span></span>  

<span data-ttu-id="323da-114">Ausserdem hat das Planungssystem die Aufgabe sicherzustellen, dass der Lagerbestand nicht unnötig wächst.</span><span class="sxs-lookup"><span data-stu-id="323da-114">Another goal of the planning system is to ensure that the inventory does not grow unnecessarily.</span></span> <span data-ttu-id="323da-115">Im Fall eines abnehmenden Bedarfs wird das Planungssystem vorschlagen, dass vorhandene Ersatzaufträge zurückgestellt, mengenmässig verringert oder storniert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="323da-115">In the case of decreasing demand, the planning system will suggest that you postpone, decrease in quantity, or cancel existing replenishment orders.</span></span>  

## <a name="planning-calculation"></a><span data-ttu-id="323da-116">Planungsberechnung</span><span class="sxs-lookup"><span data-stu-id="323da-116">Planning Calculation</span></span>  
<span data-ttu-id="323da-117">Das Planungssystem wird durch den erwarteten und den tatsächlichen Debitorenbedarf sowie die Wiederbeschaffungsparameter gesteuert.</span><span class="sxs-lookup"><span data-stu-id="323da-117">The planning system is driven by anticipated and actual customer demand, as well as inventory reordering parameters.</span></span> <span data-ttu-id="323da-118">Ein Ausführen der Planungsberechnung bewirkt, dass die Anwendung bestimmte Aktionen (Ereignismeldungen) vorschlägt, die sich auf mögliche Beschaffungen von Kreditoren, Umlagerungen zwischen Lagern oder die Fertigung beziehen.</span><span class="sxs-lookup"><span data-stu-id="323da-118">Running the planning calculation will result in application suggesting specific actions (Action Messages) to take concerning possible replenishment from vendors, transfers between warehouses, or production.</span></span> <span data-ttu-id="323da-119">Wenn es bereits Ersatzaufträge gibt, könnten die vorgeschlagenen Aktionen so aussehen, dass die Aufträge vergrössert oder schneller erteilt werden sollen, damit den Bedarfsänderungen Rechnung getragen wird.</span><span class="sxs-lookup"><span data-stu-id="323da-119">If replenishment orders already exist, the suggested actions could be to increase or expedite the orders to meet the changes in demand.</span></span>  

<span data-ttu-id="323da-120">Die Basis der Planungsroutine findet sich in der Brutto-Netto-Berechnung.</span><span class="sxs-lookup"><span data-stu-id="323da-120">The basis of the planning routine is in the gross-to-net calculation.</span></span> <span data-ttu-id="323da-121">Die Nettobedarfe steuern die voraussichtlichen Freigabemengen, die anhand der Arbeitspläne (Produktionsartikel) oder der Vorlaufzeiten der Artikelkarten (Einkaufsartikel) geplant werden.</span><span class="sxs-lookup"><span data-stu-id="323da-121">Net requirements drive planned order releases, which are scheduled based on the routing information (manufactured items) or the item card lead time (purchased items).</span></span> <span data-ttu-id="323da-122">Voraussichtliche Freigabemengen basieren auf der Planungsberechnung und werden durch die Parameter beeinflusst, die auf den einzelnen Artikelkarten festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="323da-122">Planned order release quantities are based on the planning calculation, and are affected by the parameters set on the individual item cards.</span></span>  

## <a name="planning-with-manual-transfer-orders"></a><span data-ttu-id="323da-123">Planung mit manuellen Umlagerungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="323da-123">Planning with Manual Transfer Orders</span></span>
<span data-ttu-id="323da-124">Wie aus dem Feld **Beschaffungsmethode** auf einer Lagerhaltungsdatenkarte zu ersehen ist, kann das Planungssystem für die Erstellung von Umlagerungsaufträgen zum standortübergreifenden Ausgleichen von Offerte und Nachfrage eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="323da-124">As you can see from the **Replenishment System** field on a SKU card, the planning system can be set up to create transfer orders to balance supply and demand across locations.</span></span>  

<span data-ttu-id="323da-125">Über solche automatischen Umlagerungsaufträge hinaus werden möglicherweise manchmal allgemeine Umlagerungen von Lagermengen an einen anderen Lagerort erforderlich, unabhängig von der vorhandenen Nachfrage.</span><span class="sxs-lookup"><span data-stu-id="323da-125">In addition to such automatic transfer orders, you may sometimes need to perform a general move of inventory quantities to another location, irrespective of existing demand.</span></span> <span data-ttu-id="323da-126">Zu diesem Zweck würde normalerweise manuell ein Umlagerungsauftrag für die umzulagernde Menge erstellt.</span><span class="sxs-lookup"><span data-stu-id="323da-126">For this purpose you would manually create a transfer order for the quantity to move.</span></span> <span data-ttu-id="323da-127">Um sicherzustellen, dass das Planungssystem diese manuellen Umlagerungsauftrag nicht verändert, müssen Sie das Feld **Planungsflexibilität** in der /den Umlagerungszeile(n) auf Keine festlegen.</span><span class="sxs-lookup"><span data-stu-id="323da-127">To ensure that the planning system does not try to manipulate this manual transfer order, you must set the **Planning Flexibility** on the transfer line(s) to None.</span></span>  

<span data-ttu-id="323da-128">Wenn hingegen das Planungssystem die Mengen und Daten für Umlagerungsaufträge an die vorhandene Nachfrage anpassen soll, müssen Sie das Feld **Planungsflexibilität**auf den Standardwert Unbeschränkt festlegen.</span><span class="sxs-lookup"><span data-stu-id="323da-128">Contrarily, if you do want the planning system to adjust the transfer order quantities and dates to existing demand, you must set the **Planning Flexibility** field to the default value, Unlimited.</span></span>

## <a name="planning-parameters"></a><span data-ttu-id="323da-129">Planungsparameter</span><span class="sxs-lookup"><span data-stu-id="323da-129">Planning Parameters</span></span>  
<span data-ttu-id="323da-130">Die Planungsparameter steuern die Beschaffung (wann, wie viel und wie) anhand der verschiedenen Einstellungen auf den Artikelkarten (oder Lagerhaltungsdaten) sowie der Produktionseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="323da-130">The planning parameters control when, how much, and how to replenish based on the various settings on the item card (or stockkeeping unit - SKU), and the manufacturing setup.</span></span>  

<span data-ttu-id="323da-131">Die folgenden Planungsparameter sind auf der Artikel- oder Lagerhaltungsdatenkarte vorhanden:</span><span class="sxs-lookup"><span data-stu-id="323da-131">The following planning parameters exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="323da-132">Toleranzperiode</span><span class="sxs-lookup"><span data-stu-id="323da-132">Dampener Period</span></span>  
-   <span data-ttu-id="323da-133">Toleranzmenge</span><span class="sxs-lookup"><span data-stu-id="323da-133">Dampener Quantity</span></span>  
-   <span data-ttu-id="323da-134">Wiederbeschaffungsverfahren</span><span class="sxs-lookup"><span data-stu-id="323da-134">Reordering Policy</span></span>  
-   <span data-ttu-id="323da-135">Minimalbestand</span><span class="sxs-lookup"><span data-stu-id="323da-135">Reorder Point</span></span>
-   <span data-ttu-id="323da-136">Maximalbestand</span><span class="sxs-lookup"><span data-stu-id="323da-136">Maximum Inventory</span></span>  
-   <span data-ttu-id="323da-137">Überlaufmenge</span><span class="sxs-lookup"><span data-stu-id="323da-137">Overflow Level</span></span>  
-   <span data-ttu-id="323da-138">Zeitrahmen</span><span class="sxs-lookup"><span data-stu-id="323da-138">Time Bucket</span></span>  
-   <span data-ttu-id="323da-139">Loskumulierungsperiode</span><span class="sxs-lookup"><span data-stu-id="323da-139">Lot Accumulation Period</span></span>  
-   <span data-ttu-id="323da-140">Neuplanungsperiode</span><span class="sxs-lookup"><span data-stu-id="323da-140">Rescheduling Period</span></span>  
-   <span data-ttu-id="323da-141">Bestellmenge</span><span class="sxs-lookup"><span data-stu-id="323da-141">Reorder Quantity</span></span>  
-   <span data-ttu-id="323da-142">Sicherh.-Zuschl. Beschaff.-Zt.</span><span class="sxs-lookup"><span data-stu-id="323da-142">Safety Lead Time</span></span>  
-   <span data-ttu-id="323da-143">Sicherheitsbestand</span><span class="sxs-lookup"><span data-stu-id="323da-143">Safety Stock Quantity</span></span>  
-   <span data-ttu-id="323da-144">Montagerichtlinie</span><span class="sxs-lookup"><span data-stu-id="323da-144">Assembly Policy</span></span>  
-   <span data-ttu-id="323da-145">Produktionsart</span><span class="sxs-lookup"><span data-stu-id="323da-145">Manufacturing Policy</span></span>  

<span data-ttu-id="323da-146">Die folgenden Auftragsmodifikationen sind auf der Artikel- oder Lagerhaltungsdatenkarte vorhanden:</span><span class="sxs-lookup"><span data-stu-id="323da-146">The following order modifiers exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="323da-147">Minimale Losgrösse</span><span class="sxs-lookup"><span data-stu-id="323da-147">Minimum Order Quantity</span></span>  
-   <span data-ttu-id="323da-148">Maximale Losgrösse</span><span class="sxs-lookup"><span data-stu-id="323da-148">Maximum Order Quantity</span></span>  
-   <span data-ttu-id="323da-149">Losgrössenrundungsfaktor</span><span class="sxs-lookup"><span data-stu-id="323da-149">Order Multiple</span></span>  

<span data-ttu-id="323da-150">Zu den globalen Planungseinrichtungsfeldern auf der Seite **Produktion Einrichtung** gehören:</span><span class="sxs-lookup"><span data-stu-id="323da-150">Global planning setup fields on the **Manufacturing Setup** page include:</span></span>  

-   <span data-ttu-id="323da-151">Dyn. Stückl.-Ebene berechnen</span><span class="sxs-lookup"><span data-stu-id="323da-151">Dynamic Low-Level Code</span></span>  
-   <span data-ttu-id="323da-152">Aktuelle Bedarfsplanung</span><span class="sxs-lookup"><span data-stu-id="323da-152">Current Demand Forecast</span></span>  
-   <span data-ttu-id="323da-153">Absatzpl. pro Lagerort verw.</span><span class="sxs-lookup"><span data-stu-id="323da-153">Use Forecast on Locations</span></span>  
-   <span data-ttu-id="323da-154">Vorg. Sich.-Zuschl. Besch.-Zt.</span><span class="sxs-lookup"><span data-stu-id="323da-154">Default Safety Lead Time</span></span>  
-   <span data-ttu-id="323da-155">Leere Überlaufmenge</span><span class="sxs-lookup"><span data-stu-id="323da-155">Blank Overflow Level</span></span>  
-   <span data-ttu-id="323da-156">Prod.-Prog.Pl./Nettobed. komb.</span><span class="sxs-lookup"><span data-stu-id="323da-156">Combined MPS/MRP Calculation</span></span>   
-   <span data-ttu-id="323da-157">Komponenten von Lagerort</span><span class="sxs-lookup"><span data-stu-id="323da-157">Components at Location</span></span>  
-   <span data-ttu-id="323da-158">Standardtoleranzperiode</span><span class="sxs-lookup"><span data-stu-id="323da-158">Default Dampener Period</span></span>  
-   <span data-ttu-id="323da-159">Toleranzmenge</span><span class="sxs-lookup"><span data-stu-id="323da-159">Default Dampener Quantity</span></span>  

<span data-ttu-id="323da-160">Weitere Informationen finden Sie unter [Designdetails: Planungsparameter](design-details-planning-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="323da-160">For more information, see [Design Details: Planning Parameters](design-details-planning-parameters.md)</span></span>  

## <a name="other-important-planning-fields"></a><span data-ttu-id="323da-161">Andere wichtige Planungs-Felder</span><span class="sxs-lookup"><span data-stu-id="323da-161">Other Important Planning Fields</span></span>
### <a name="planning-flexibility"></a><span data-ttu-id="323da-162">Planungsflexibilität</span><span class="sxs-lookup"><span data-stu-id="323da-162">Planning Flexibility</span></span>
<span data-ttu-id="323da-163">In den meisten Beschaffungsaufträgen wie Fertigungsaufträge, können Sie **Unbeschränkt** oder **Keine** im Feld **Planungsflexibilität** auf den Zeilen auswählen.</span><span class="sxs-lookup"><span data-stu-id="323da-163">On most supply orders, such as production orders, you can select **Unlimited** or **None** in the **Planning Flexibility** field on the lines.</span></span>

<span data-ttu-id="323da-164">Gibt an, ob die durch die Fertigungsauftragszeile dargestellte Lieferung bei der Berechnung von Ereignismeldungen vom Planungssystem berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="323da-164">This specifies whether the supply represented by the production order line is considered by the planning system when calculating action messages.</span></span>
<span data-ttu-id="323da-165">Enthält das Feld die Option **Unbeschränkt**, wird die Zeile beim Berechnen von Ereignismeldungen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="323da-165">If the field contains **Unlimited**, then the planning system includes the line when calculating action messages.</span></span> <span data-ttu-id="323da-166">Wenn das Feld die Option **Keine** enthält, ist die Zeile unveränderlich und wird bei der Berechnung von Aktionsmeldungen nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="323da-166">If the field contains **None**, then the line is firm and unchangeable, and the planning system does not include the line when calculating action messages.</span></span>

### <a name="warning"></a><span data-ttu-id="323da-167">Warnung</span><span class="sxs-lookup"><span data-stu-id="323da-167">Warning</span></span>
<span data-ttu-id="323da-168">Das Feld **Warnung** auf der **Planungsvorschlag** Seite informiert Sie über jede mögliche Planungszeile, die für eine ungewöhnliche Situation mit einen Text erstellt wird, den der Benutzer klicken kann, um weitere Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="323da-168">The **Warning** information field on the **Planning Worksheet** page informs you of any planning line created for an unusual situation with a text, which the user can choose to read additional information.</span></span> <span data-ttu-id="323da-169">Folgende Arten von Warnungen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="323da-169">The following warning types exist:</span></span>

- <span data-ttu-id="323da-170">Notfall</span><span class="sxs-lookup"><span data-stu-id="323da-170">Emergency</span></span>
- <span data-ttu-id="323da-171">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="323da-171">Exception</span></span>
- <span data-ttu-id="323da-172">Achtung</span><span class="sxs-lookup"><span data-stu-id="323da-172">Attention</span></span>
- <span data-ttu-id="323da-173">Notfall</span><span class="sxs-lookup"><span data-stu-id="323da-173">Emergency</span></span>

<span data-ttu-id="323da-174">Die Warnung für einen Notfall wird in zwei Situationen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="323da-174">The emergency warning is displayed in two situations:</span></span>

- <span data-ttu-id="323da-175">Der Lagerbestand ist am geplanten Startdatum negativ.</span><span class="sxs-lookup"><span data-stu-id="323da-175">The inventory is negative on the planning starting date.</span></span>
- <span data-ttu-id="323da-176">Es sind rückdatierte Beschaffungs- oder Bedarfsereignisse vorhanden.</span><span class="sxs-lookup"><span data-stu-id="323da-176">Back-dated supply or demand events exist.</span></span>

<span data-ttu-id="323da-177">Wenn der Lagerbestand eines Artikels am geplanten Startdatum negativ ist, wird vom Planungssystem ein Notfallbeschaffungsauftrag für den negativen Bestand vorgeschlagen, der am geplanten Startdatum eingeht.</span><span class="sxs-lookup"><span data-stu-id="323da-177">If an item’s inventory is negative on the planning starting date, the planning system suggests an emergency supply order for the negative quantity to arrive on the planning starting date.</span></span> <span data-ttu-id="323da-178">Im Warnungstext werden das Startdatum und die Menge der Notfallbestellung angegeben.</span><span class="sxs-lookup"><span data-stu-id="323da-178">The warning text states the starting date and the quantity of the emergency order.</span></span>

<span data-ttu-id="323da-179">Belegzeilen mit Fälligkeitsdaten vor dem geplanten Startdatum werden in einem Notfallbeschaffungsauftrag für den Artikel zusammengefasst, der am geplanten Startdatum eingehen soll.</span><span class="sxs-lookup"><span data-stu-id="323da-179">Any document lines with due dates before the planning starting date are consolidated into one emergency supply order for the item to arrive on the planning starting date.</span></span>

### <a name="exception"></a><span data-ttu-id="323da-180">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="323da-180">Exception</span></span>
<span data-ttu-id="323da-181">Die Ausnahmewarnung wird angezeigt, wenn der voraussichtlich verfügbare Lagerbestand den Sicherheitsbestand unterschreitet.</span><span class="sxs-lookup"><span data-stu-id="323da-181">The exception warning is displayed if the projected available inventory drops below the safety stock quantity.</span></span>

<span data-ttu-id="323da-182">Vom Planungssystem wird ein Beschaffungsauftrag vorgeschlagen, um den Bedarf am Fälligkeitsdatum zu decken.</span><span class="sxs-lookup"><span data-stu-id="323da-182">The planning system will suggest a supply order to meet the demand on its due date.</span></span> <span data-ttu-id="323da-183">In der Warnung werden der Sicherheitsbestand des Artikels und das Datum angegeben, an dem er unterschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="323da-183">The warning text states the item’s safety stock quantity and the date on which it is violated.</span></span>

<span data-ttu-id="323da-184">Das Unterschreiten des Sicherheitsbestands gilt als Ausnahme, da dieser Zustand nicht eintreten sollte, wenn der Minimalbestand korrekt festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="323da-184">Violating the safety stock level is considered an exception because it should not occur if the reorder point has been set correctly.</span></span>

> [!NOTE]
> <span data-ttu-id="323da-185">Der Vorrat in Planungszeilen mit Ausnahmewarnungen wird normalerweise nicht gemäss den Planungsparametern geändert.</span><span class="sxs-lookup"><span data-stu-id="323da-185">Supply on planning lines with Exception warnings is normally not modified according to planning parameters.</span></span> <span data-ttu-id="323da-186">Stattdessen wird vom Planungssystem nur eine Beschaffung vorgeschlagen, um die genaue Bedarfsmenge zu decken.</span><span class="sxs-lookup"><span data-stu-id="323da-186">Instead, the planning system only suggests a supply to cover the exact demand quantity.</span></span> <span data-ttu-id="323da-187">Sie können jedoch die Planung so festlegen, dass bestimmte Planungsparameter für Planungszeilen mit bestimmten Warnungen berücksichtigt werden können.</span><span class="sxs-lookup"><span data-stu-id="323da-187">However, you can set the planning run up to respect certain planning parameters for planning lines with certain warnings.</span></span> <span data-ttu-id="323da-188">Weitere Informationen finden Sie unter "Respekt-Planungsparameter für Ausnahme-Warnungen" in Plan kalkulieren.</span><span class="sxs-lookup"><span data-stu-id="323da-188">For more information, see “Respect Planning Parameters for Exception Warnings” in Calculate Plan - Plan.</span></span> <span data-ttu-id="323da-189">Wksh.</span><span class="sxs-lookup"><span data-stu-id="323da-189">Wksh.</span></span>

### <a name="attention"></a><span data-ttu-id="323da-190">Achtung</span><span class="sxs-lookup"><span data-stu-id="323da-190">Attention</span></span>
<span data-ttu-id="323da-191">Die Achtungswarnung wird in zwei Situationen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="323da-191">The attention warning is displayed in two situations:</span></span>

- <span data-ttu-id="323da-192">Das geplante Startdatum liegt vor dem Arbeitsdatum.</span><span class="sxs-lookup"><span data-stu-id="323da-192">The planning starting date is earlier than the work date.</span></span>
- <span data-ttu-id="323da-193">Die Planungszeile schlägt vor, eine freigegebene Bestellung oder einen freigegebenen Fertigungsauftrag zu ändern.</span><span class="sxs-lookup"><span data-stu-id="323da-193">The planning line suggests to change a released purchase or production order.</span></span>

> [!NOTE]
> <span data-ttu-id="323da-194">In Planzeilen mit Warnungen ist das Kontrollkästchen **Ereignismeldung akzeptieren** nicht aktiviert, da diese Zeilen vom Planer genauer untersucht werden sollen, bevor der Plan umgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="323da-194">In planning lines with warnings, the **Accept Action Message** field is not selected, because the planner is expected to further investigate these lines before carrying out the plan.</span></span>

## <a name="see-also"></a><span data-ttu-id="323da-195">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="323da-195">See Also</span></span>  
[<span data-ttu-id="323da-196">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="323da-196">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)  
<span data-ttu-id="323da-197">[Planung](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="323da-197">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="323da-198">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="323da-198">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="323da-199">[Bearbeitungen](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="323da-199">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="323da-200">Lagerbesttand</span><span class="sxs-lookup"><span data-stu-id="323da-200">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="323da-201">Einkauf</span><span class="sxs-lookup"><span data-stu-id="323da-201">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="323da-202">Bewährte Einrichtungsmethoden: Beschaffungsplanung</span><span class="sxs-lookup"><span data-stu-id="323da-202">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="323da-203">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="323da-203">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
