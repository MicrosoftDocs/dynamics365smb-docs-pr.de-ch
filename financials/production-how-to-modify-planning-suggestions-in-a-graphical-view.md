---
title: "Vorgehensweise: Ändern von Planungsvorschlägen in einer grafischen Ansich| Microsoft Docst"
description: "Eine typische Planungsaktivität besteht darin, Planungsvorschlagszeilen zu ändern oder hinzuzufügen, um die vorgeschlagenen Beschaffungsaufträge zu ändern, bevor Sie diese kommissionieren, indem Sie die Funktion **Ereignismeldung durchführen** ausführen. Eine Alternative zur Durchführung im Planungsvorschlag ist die Verwendung einer grafischen Ansicht."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6cdd86fb96e89e99ea2378221d2991bd640f887e
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-modify-planning-suggestions-in-a-graphical-view"></a><span data-ttu-id="74cf6-104">Vorgehensweise: Ändern von Planungsvorschlägen in einer grafischen Ansicht</span><span class="sxs-lookup"><span data-stu-id="74cf6-104">How to: Modify Planning Suggestions in a Graphical View</span></span>
<span data-ttu-id="74cf6-105">Eine typische Planungsaktivität besteht darin, Planungsvorschlagszeilen zu ändern oder hinzuzufügen, um die vorgeschlagenen Beschaffungsaufträge zu ändern, bevor Sie diese kommissionieren, indem Sie die Funktion **Ereignismeldung durchführen** ausführen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-105">A typical planning activity is to change or add planning worksheet lines to modify the suggested supply orders before you commit them by running the **Carry out Action Message** function.</span></span> <span data-ttu-id="74cf6-106">Eine Alternative zur Durchführung im Planungsvorschlag ist die Verwendung einer grafischen Ansicht.</span><span class="sxs-lookup"><span data-stu-id="74cf6-106">An alternative to doing this in the planning worksheet is to use a graphical view.</span></span>

<span data-ttu-id="74cf6-107">Im Fenster **Artikelverfügbarkeit nach Zeitachse** können Sie gewisse Beschaffungsaufträge und Planungsvorschläge ändern, indem Sie Elemente entlang der X-Achse ziehen, um die Menge zu ändern oder entlang der Y-Achse, um das Fälligkeitsdatum zu ändern.</span><span class="sxs-lookup"><span data-stu-id="74cf6-107">In the **Item Availability by Timeline** window, you can modify certain supply orders and suggestions by dragging elements on the x-axis to change quantity or dragging elements on the y-axis to change due date.</span></span>  

 <span data-ttu-id="74cf6-108">Im Fenster **Artikelverfügbarkeit nach Zeitachse** und im Fenster **Planungsvorschlag** können Sie folgende Änderungen vornehmen:</span><span class="sxs-lookup"><span data-stu-id="74cf6-108">In the **Item Availability by Timeline** window and the **Planning Worksheet** window you can make the following changes:</span></span>  

-   <span data-ttu-id="74cf6-109">Ändern eines vorgeschlagenen Lieferauftrags, der nur als Planungszeile vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="74cf6-109">Modify a suggested supply order that only exists as a planning line.</span></span>  
-   <span data-ttu-id="74cf6-110">Ändern eines vorhandenen Beschaffungsauftrags, den das Planungssystem für eine Änderung vorschlägt.</span><span class="sxs-lookup"><span data-stu-id="74cf6-110">Modify an existing supply order that the planning system suggests to change.</span></span>  
-   <span data-ttu-id="74cf6-111">Erstellen und Ändern eines neuen vorgeschlagenen Beschaffungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="74cf6-111">Create a new suggested supply order and modify it.</span></span>  

<span data-ttu-id="74cf6-112">Weitere Informationen zu den gezeigten Planungszeilentypen finden Sie im Feld Beschreibung im Inforegister **Ereignisänderungen**.</span><span class="sxs-lookup"><span data-stu-id="74cf6-112">For more information about the planning line types that are shown, see the Description field on the **Event Changes** FastTab.</span></span>  

<span data-ttu-id="74cf6-113">Wenn Sie **Änderungen speichern** im Fenster **Artikelverfügbarkeit nach Zeitachse** auswählen, werden die Änderungen, die Sie durchgeführt haben, in den Planungs- oder Bestellvorschlag kopiert.</span><span class="sxs-lookup"><span data-stu-id="74cf6-113">When you choose **Save Changes** in the **Item Availability by Timeline** window, the modifications that you have made are copied to the planning or requisition worksheet.</span></span> <span data-ttu-id="74cf6-114">Sie können sie jetzt mithilfe des **Carry Out Action Msg. Plan.** implementieren</span><span class="sxs-lookup"><span data-stu-id="74cf6-114">You can now implement them using the **Carry Out Action Msg.-Plan.** function.</span></span>  

<span data-ttu-id="74cf6-115">Der folgende Ablauf zeigt, wie Vorratsvorschläge mit Drag & Drop geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="74cf6-115">The following procedure shows how to modify supply suggestions by drag and drop.</span></span> <span data-ttu-id="74cf6-116">Alternativ können Sie die Felder **Fälligkeitsdatum** und **Menge** im Inforegister **Ereignisänderungen** ändern und die Änderungen im Inforegister **Zeitachse** im Fenster **Planung** sofort grafisch anzeigen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-116">As an alternative, you can change the **Due Date** and **Quantity** fields on the **Event Changes** FastTab and immediately see the changes graphically on the **Timeline** FastTab in the **Planning Worksheet** window.</span></span>  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a><span data-ttu-id="74cf6-117">So ändern Sie vorgeschlagene Beschaffungsaufträge in der grafischen Ansicht</span><span class="sxs-lookup"><span data-stu-id="74cf6-117">To modify suggested supply orders in the graphical view</span></span>  
1.  <span data-ttu-id="74cf6-118">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Artikelverfügbarkeit nach Zeitachse** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="74cf6-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Availability by Timeline**, and then choose the related link.</span></span>  

    <span data-ttu-id="74cf6-119">Das Fenster **Artikelverfügbarkeit nach Zeitachse** wird geöffnet, mit Artikelnummer, Lagerplatz und Variante des Artikels in der ausgewählten Planungszeile, die in den Feldern des Inforegisters **Optionen** vorab ausgefüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="74cf6-119">The **Item Availability by Timeline** window opens with the item number, location, and variant of the item on the selected planning line prefilled in the **Options** FastTab.</span></span> <span data-ttu-id="74cf6-120">Das Inforegister **Zeitachse** zeigt die grafische Darstellung des voraussichtlichen Lagerbestands des Artikels, einschliesslich Planungsvorschläge.</span><span class="sxs-lookup"><span data-stu-id="74cf6-120">The **Timeline** FastTab shows a graphical representation of the item’s projected inventory, including planning suggestions.</span></span>  

2.  <span data-ttu-id="74cf6-121">Stellen Sie sicher, dass das Feld **Planungsvorschläge einschliessen** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="74cf6-121">Make sure that the **Include Planning Suggestions** field is selected.</span></span>  
3.  <span data-ttu-id="74cf6-122">Suchen Sie den vorgeschlagenen Beschaffungsauftrag, der bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="74cf6-122">Find the suggested supply order that you want to modify.</span></span> <span data-ttu-id="74cf6-123">Sie erkennen änderbare Elemente an dem grünen Kreis und dem Diskettensymbol.</span><span class="sxs-lookup"><span data-stu-id="74cf6-123">You can identify modifiable elements by the green circle and the disk icon.</span></span> <span data-ttu-id="74cf6-124">Weitere Informationen über die verschiedenen Symbole, finden Sie im Inforegister Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="74cf6-124">For more information about the different symbols, see the "Symbols and Icons on the Timeline FastTab" section.</span></span>  
4.  <span data-ttu-id="74cf6-125">Positionieren Sie den Mauszeiger über dem grünen Kreis, bis er grösser wird und der Mauszeiger seine Form zum Verschiebungssymbol (vier Pfeile) ändert.</span><span class="sxs-lookup"><span data-stu-id="74cf6-125">Place the pointer over the green circle until it enlarges and the pointer changes to Move shape (four arrows).</span></span>  
5.  <span data-ttu-id="74cf6-126">Drücken Sie die Maustaste und halten Sie sie gedrückt, während Sie den Zeiger nach oben oder unten ziehen, um die Menge zu ändern.</span><span class="sxs-lookup"><span data-stu-id="74cf6-126">Press and hold the mouse button while you drag the pointer up or down to modify the quantity.</span></span> <span data-ttu-id="74cf6-127">Drücken Sie die Maustaste und halten Sie sie gedrückt, während Sie den Zeiger nach links oder rechts ziehen, um das Fälligkeitsdatum zu ändern.</span><span class="sxs-lookup"><span data-stu-id="74cf6-127">Press and hold the mouse button while you drag the pointer left or right to modify the due date.</span></span>  
6.  <span data-ttu-id="74cf6-128">Außer dem Bewegen von Elementen mit Drag & Drop können Sie auch Planungsvorschläge ändern, indem Sie einige Rechtsklick-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="74cf6-128">In addition to moving elements by drag and drop, you can modify planning suggestions by using a number of drop-down menu functions.</span></span> <span data-ttu-id="74cf6-129">Klicken Sie mit der rechten Maustaste auf den grünen Kreis eines vorgeschlagenen Vorratselements, und wählen Sie eine der folgenden Funktionen aus.</span><span class="sxs-lookup"><span data-stu-id="74cf6-129">Access the drop-down menu for the green circle of a suggested supply element and select one the following functions</span></span>  

    |<span data-ttu-id="74cf6-130">Funktion</span><span class="sxs-lookup"><span data-stu-id="74cf6-130">Function</span></span>|<span data-ttu-id="74cf6-131">Description</span><span class="sxs-lookup"><span data-stu-id="74cf6-131">Description</span></span>|  
    |--------------|---------------------------------------|  
    |<span data-ttu-id="74cf6-132">**Neuen Vorrat erstellen**</span><span class="sxs-lookup"><span data-stu-id="74cf6-132">**Create New Supply**</span></span>|<span data-ttu-id="74cf6-133">Erstellt an der Stelle, auf die Sie rechtsklicken, ein neues Element, das einen neuen vorgeschlagenen Beschaffungsauftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="74cf6-133">Creates a new element point where you access the drop-down menu, which represents a new suggested supply order.</span></span> <span data-ttu-id="74cf6-134">Dies wird zu einer neuen Zeile im Planungsvorschlag, wenn Sie **Änderungen speichern** auswählen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-134">It becomes a new line in the planning worksheet when you choose **Save Changes**.</span></span><br /><br /> <span data-ttu-id="74cf6-135">**HINWEIS:** Wenn die Felder **Standortfilter** oder **Varianten-Filter** im Inforegister **Optionen** leer sind oder mehr als einen Filterwert enthalten, wird der neue Vorrat erstellt und später im Planungs- oder Bestellvorschlag mit den folgenden Codes gespeichert:</span><span class="sxs-lookup"><span data-stu-id="74cf6-135">**NOTE:** If the **Location Filter** or **Variant Filter** fields on the **Options** FastTab are empty or have more than one filter value, then the new supply is created and later saved to the planning or requisition worksheet with the following codes:</span></span><br /><br /> <span data-ttu-id="74cf6-136">* Wenn das Feld "Filter" leer ist, wird der neue Vorrat ohne Lagerort oder Variantencode erstellt.</span><span class="sxs-lookup"><span data-stu-id="74cf6-136">* If the filter field is empty, then the new supply is created without a location or variant code.</span></span><br /><br /> <span data-ttu-id="74cf6-137">* «»Wenn mehr als ein Filterwert definiert ist, wird der neue Vorrat für den ersten Filterwert gemäß der Sortiermethode erstellt.</span><span class="sxs-lookup"><span data-stu-id="74cf6-137">* If more than one filter value is defined, then the new supply is created for the first filter value according to the sorting method.</span></span><br /><br /> <span data-ttu-id="74cf6-138">Wenn Sie eine andere Variante oder einen anderen Lagerortcode verwenden möchten, müssen Sie diese in der neuen Planungszeile manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="74cf6-138">If you want another variant or location code, then you must manually change it on the new planning line.</span></span>|  
    |<span data-ttu-id="74cf6-139">**Vorrat automatisch anpassen**</span><span class="sxs-lookup"><span data-stu-id="74cf6-139">**Auto-Adjust Supply**</span></span>|<span data-ttu-id="74cf6-140">Optimiert einen neuen Vorrat, den Sie im Diagramm erstellt haben, indem Sie sicherstellen, dass sich vor dem nächsten Vorrat ein Lagerbestand von null ergibt.</span><span class="sxs-lookup"><span data-stu-id="74cf6-140">Optimizes a new supply that you have created in the graph by making sure that it results in zero inventory before the next supply.</span></span>|  
    |<span data-ttu-id="74cf6-141">**Vorrat löschen**</span><span class="sxs-lookup"><span data-stu-id="74cf6-141">**Delete Supply**</span></span>|<span data-ttu-id="74cf6-142">Löscht das Element im Inforegister **Zeitachse** und löscht die Planungszeile, wenn Sie **Änderungen speichern** auswählen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-142">Deletes the element in the **Timeline** FastTab and deletes the planning line when you choose **Save Changes**.</span></span> <span data-ttu-id="74cf6-143">Das Symbol wird als Diskette mit einem roten Kreuz angezeigt, wenn der Vorrat gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="74cf6-143">The icon changes to a disk that has a red cross when the supply has been deleted.</span></span><br /><br /> <span data-ttu-id="74cf6-144">**HINWEIS:**Sie können nur einen Vorrat mit dem Ereignismeldungstyp **Neu** löschen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-144">**NOTE:** You can only delete a supply of action message type **New**.</span></span> <span data-ttu-id="74cf6-145">Nachdem Sie **Änderungen speichern** ausgewählt haben, müssen Sie die betreffende Planungszeile im Planungs- oder Bestellvorschlag manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-145">After you choose **Save Changes**, you must manually delete the planning line in question in the planning or requisition worksheet.</span></span>|  

7.  <span data-ttu-id="74cf6-146">Wählen Sie auf der Registerkarte Aktionen in der Gruppe Allgemein die Option **Neu laden** aus, wenn Sie alle Änderungen zurücksetzen möchten, die Sie durchgeführt haben, nachdem Sie zuletzt das Fenster Artikel-**Verfügbarkeit nach Zeitachse**geöffnet oder **Neu laden** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="74cf6-146">Choose the **Reload** action if you want to reset all the changes that you have made after you last opened the **Item Availability by Timeline** window or selected **Reload**.</span></span>  
8. <span data-ttu-id="74cf6-147">Wenn die Elemente an der gewünschten Stelle im Diagramm positioniert sind, aktivieren Sie **Änderungen speichern**, um Mengen- und Datumsänderungen in die Planungs- oder Bestellvorschlagszeilen zu kopieren, die die grafischen Elemente darstellen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-147">When the elements are placed where you want them in the diagram, choose **Save Changes** to copy modified quantity and date changes to the planning or requisition lines that represent the graphical elements.</span></span>  

<span data-ttu-id="74cf6-148">Um die Beschaffungsplanänderungen zu übernehmen, müssen Sie den resultierenden Ereignismeldungen aus dem Planungs- oder Bestellvorschlag folgen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-148">To implement the supply plan changes, you must follow the resulting action messages from the planning or requisition worksheet.</span></span> <span data-ttu-id="74cf6-149">Weitere Informationen finden Sie unter Carry Out Action Msg.Plan..</span><span class="sxs-lookup"><span data-stu-id="74cf6-149">For more information, see Carry Out Action Msg.-Plan..</span></span>

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a><span data-ttu-id="74cf6-150">Symbole und Bildsymbole im Inforegister "Zeitachse"</span><span class="sxs-lookup"><span data-stu-id="74cf6-150">Symbols and Icons on the Timeline FastTab</span></span>
 |<span data-ttu-id="74cf6-151">Symbol/Bildsymbol</span><span class="sxs-lookup"><span data-stu-id="74cf6-151">Symbol/Icon</span></span>|<span data-ttu-id="74cf6-152">Description</span><span class="sxs-lookup"><span data-stu-id="74cf6-152">Description</span></span>|  
 |------------------|---------------------------------------|  
 |<span data-ttu-id="74cf6-153">Schwarzes Kreuz</span><span class="sxs-lookup"><span data-stu-id="74cf6-153">Black cross</span></span>|<span data-ttu-id="74cf6-154">Aufträge (Vorrat und Bedarf).</span><span class="sxs-lookup"><span data-stu-id="74cf6-154">Orders (both supply and demand).</span></span><br /><br /> <span data-ttu-id="74cf6-155">-   Kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="74cf6-155">-   Cannot be modified.</span></span><br /><span data-ttu-id="74cf6-156">-   Sichtbar, wenn das Feld **Voraussichtlichen Lagerbestand anzeigen** ausgewählt wird (orangefarbenes Diagramm).</span><span class="sxs-lookup"><span data-stu-id="74cf6-156">-   Visible when the **Show Projected Inventory** field is selected (orange graph).</span></span>|  
 |<span data-ttu-id="74cf6-157">Roter Kreis</span><span class="sxs-lookup"><span data-stu-id="74cf6-157">Red circle</span></span>|<span data-ttu-id="74cf6-158">Vorhandene Beschaffungsaufträge, die nicht in den Planungsvorschlägen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="74cf6-158">Existing supply orders that are not in planning suggestions.</span></span><br /><br /> <span data-ttu-id="74cf6-159">-   Kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="74cf6-159">-   Cannot be modified.</span></span><br /><span data-ttu-id="74cf6-160">-   Sichtbar, wenn das Feld **Voraussichtlichen Lagerbestand anzeigen** ausgewählt wird (orangefarbenes Diagramm).</span><span class="sxs-lookup"><span data-stu-id="74cf6-160">-   Visible when the **Show Projected Inventory** field is selected (orange graph).</span></span>|  
 |<span data-ttu-id="74cf6-161">Gelber Stern</span><span class="sxs-lookup"><span data-stu-id="74cf6-161">Yellow star</span></span>|<span data-ttu-id="74cf6-162">Nachfrageprognose.</span><span class="sxs-lookup"><span data-stu-id="74cf6-162">Forecast demand.</span></span><br /><br /> <span data-ttu-id="74cf6-163">-   Kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="74cf6-163">-   Cannot be modified.</span></span><br /><span data-ttu-id="74cf6-164">-   Sichtbar, wenn das Feld **Planungsname** einen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="74cf6-164">-   Visible when the **Forecast Name** field has a value.</span></span><br /><br /> <span data-ttu-id="74cf6-165">Wenn die Felder **Voraussichtlichen Lagerbestand anzeigen** und **Planungsvorschläge einschliessen** ausgewählt werden, hat jeder gelbe Stern ein verknüpftes Äquivalent im entgegengesetzten Diagramm.</span><span class="sxs-lookup"><span data-stu-id="74cf6-165">When both the **Show Projected Inventory** and the **Include Planning Suggestions** fields are selected, then each yellow star has a linked counterpart in the opposite graph.</span></span> <span data-ttu-id="74cf6-166">Dieses stellt dar, wie ein vorgeschlagener Vorrat den voraussichtlichen Bedarf erfüllt.</span><span class="sxs-lookup"><span data-stu-id="74cf6-166">This illustrates how a suggested supply fulfills the forecasted demand.</span></span>|  
 |<span data-ttu-id="74cf6-167">Grüner Kreis mit einem Diskettensymbol mit einem roten Kreuz</span><span class="sxs-lookup"><span data-stu-id="74cf6-167">Green circle with an icon shaped as a disk that has a red cross</span></span>|<span data-ttu-id="74cf6-168">Vorgeschlagener Beschaffungsauftrag mit Ereignismeldung *Abbrechen*.</span><span class="sxs-lookup"><span data-stu-id="74cf6-168">Suggested supply order with action message *Cancel*.</span></span><br /><br /> <span data-ttu-id="74cf6-169">-   Kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="74cf6-169">-   Cannot be modified.</span></span><br /><span data-ttu-id="74cf6-170">-   Sichtbar, wenn das Feld **Planungsvorschläge einschließen** ausgewählt wird (grünes Diagramm).</span><span class="sxs-lookup"><span data-stu-id="74cf6-170">-   Visible when the **Include Planning Suggestions** field is selected (green graph).</span></span>|  
 |<span data-ttu-id="74cf6-171">Grüner Kreis mit einem Diskettensymbol mit einem Stern</span><span class="sxs-lookup"><span data-stu-id="74cf6-171">Green circle with an icon shaped as a disk that has a star</span></span>|<span data-ttu-id="74cf6-172">Vorgeschlagene Beschaffungsaufträge mit Ereignismeldung *Neu*.</span><span class="sxs-lookup"><span data-stu-id="74cf6-172">Suggested supply orders with action message *New*.</span></span><br /><br /> <span data-ttu-id="74cf6-173">-   Kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="74cf6-173">-   Can be modified.</span></span><br /><span data-ttu-id="74cf6-174">-   Sichtbar, wenn das Feld **Planungsvorschläge einschließen** ausgewählt wird (grünes Diagramm).</span><span class="sxs-lookup"><span data-stu-id="74cf6-174">-   Visible when the **Include Planning Suggestions** field is selected (green graph).</span></span>|  
 |<span data-ttu-id="74cf6-175">Grüner Kreis mit einem Diskettensymbol mit einem oder zwei Pfeilen</span><span class="sxs-lookup"><span data-stu-id="74cf6-175">Green circle with an icon shaped as a disk that has one or two arrows</span></span>|<span data-ttu-id="74cf6-176">Vorgeschlagene Beschaffungsaufträge mit Ereignismeldung *Neu berechnen*, *Menge ändern* oder *Neu berechnen & Menge ändern*</span><span class="sxs-lookup"><span data-stu-id="74cf6-176">Suggested supply orders with action message *Reschedule*, *Change Qty.*, or *Resched. and Chg. Qty.*</span></span><br /><br /> <span data-ttu-id="74cf6-177">-   Kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="74cf6-177">-   Can be modified.</span></span><br /><span data-ttu-id="74cf6-178">-   Sichtbar, wenn das Feld **Planungsvorschläge einschließen** ausgewählt wird (grünes Diagramm).</span><span class="sxs-lookup"><span data-stu-id="74cf6-178">-   Visible when the **Include Planning Suggestions** field is selected (green graph).</span></span><br /><br /> <span data-ttu-id="74cf6-179">Die Pfeile geben die Richtung des Planungsvorschlags an.</span><span class="sxs-lookup"><span data-stu-id="74cf6-179">The arrows reflect the direction of the planning suggestion.</span></span> <span data-ttu-id="74cf6-180">Beispielsweise spiegelt ein Linkspfeil zusammen mit einem Nach-oben-Pfeil eine *Neu berechnen Menge ändern*-Ereignismeldung wider, die aus einer rückwärts ausgeführten Neuplanung und einer Mengenerhöhung besteht.</span><span class="sxs-lookup"><span data-stu-id="74cf6-180">For example, a left arrow together with an up arrow reflects a *Resched. and Chg. Qty.* action message that consists of a backward rescheduling and a quantity increase.</span></span>|  
 ||  

<span data-ttu-id="74cf6-181">Wenn Sie das Dropdownmenü für das Inforegister **Zeitachse** zugreifen, sehen, die folgenden Funktionen, abhängig von dem, was Sie gewählt haben</span><span class="sxs-lookup"><span data-stu-id="74cf6-181">When you access the drop-down menu for the **Timeline** FastTab, the following functions appear depending what you choose</span></span>  

 |<span data-ttu-id="74cf6-182">Funktion</span><span class="sxs-lookup"><span data-stu-id="74cf6-182">Function</span></span>|<span data-ttu-id="74cf6-183">Description</span><span class="sxs-lookup"><span data-stu-id="74cf6-183">Description</span></span>|  
 |--------------|---------------------------------------|  
 |<span data-ttu-id="74cf6-184">**Neuen Vorrat erstellen**</span><span class="sxs-lookup"><span data-stu-id="74cf6-184">**Create New Supply**</span></span>|<span data-ttu-id="74cf6-185">Erstellt an der Stelle, auf die Sie rechtsklicken, ein neues Element, das einen neuen vorgeschlagenen Beschaffungsauftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="74cf6-185">Creates a new element on the point where you access the drop-down menu, which represents a new suggested supply order.</span></span> <span data-ttu-id="74cf6-186">Dies wird zu einer neuen Zeile im Planungsvorschlag, wenn Sie **Änderungen speichern** auf der Registerkarte **Vorgang** auswählen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-186">It becomes a new line in the planning worksheet when you choose **Save Changes** on the **Process** tab.</span></span><br /><br /> <span data-ttu-id="74cf6-187">Alle Filterwerte, die in den Feldern **Standortfilter** oder **Variantenfilter** im Inforegister **Optionen** definiert werden, werden auf den neuen Beschaffungsauftrag angewendet.</span><span class="sxs-lookup"><span data-stu-id="74cf6-187">Any filter values that are defined in the **Location Filter** or **Variant Filter** fields on the **Options** FastTab will be applied to the new supply order.</span></span> <span data-ttu-id="74cf6-188">**Hinweis:**  Wenn die Filterfelder leer sind oder mehr als einen Filterwert enthalten, wird der neue Beschaffungsauftrag erstellt, indem die folgenden Codes verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="74cf6-188">**Note:**  If the filter fields are empty or have more than one filter value, then the new supply order is created by using the following codes:</span></span> <ul><li><span data-ttu-id="74cf6-189">Wenn das Feld "Filter" leer ist, wird der neue Vorrat ohne Lagerort oder Variantencode erstellt.</span><span class="sxs-lookup"><span data-stu-id="74cf6-189">If the filter field is empty, then the new supply is created without a location or variant code.</span></span></li><li><span data-ttu-id="74cf6-190">Wenn mehr als ein Filterwert definiert ist, wird der neue Vorrat erstellt, indem der erste Filterwert gemäss der Sortierreihenfolge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="74cf6-190">If more than one filter value is defined, then the new supply is created by using the first filter value according to the sorting order.</span></span></li></ul> <span data-ttu-id="74cf6-191">Wenn Sie einen anderen Varianten- oder Lagerortcode in dem neuen Beschaffungsauftrag verwenden möchten, müssen Sie ihn in der neuen Planungszeile manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="74cf6-191">If you want another variant or location code in the new supply order, then you must manually change it on the new planning line.</span></span>|  
 |<span data-ttu-id="74cf6-192">**Vorrat automatisch anpassen**</span><span class="sxs-lookup"><span data-stu-id="74cf6-192">**Auto-Adjust Supply**</span></span>|<span data-ttu-id="74cf6-193">Optimiert einen neuen Vorrat, den Sie in dem Plan erstellt haben, indem Sie sicherstellen, dass vor dem nächsten Vorrat ein Lagerbestand von null erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="74cf6-193">Optimizes a new supply that you have created in the graph by making sure that it creates zero inventory before the next supply.</span></span>|  
 |<span data-ttu-id="74cf6-194">**Vorrat löschen**</span><span class="sxs-lookup"><span data-stu-id="74cf6-194">**Delete Supply**</span></span>|<span data-ttu-id="74cf6-195">Löscht das Element im Inforegister **Zeitachse** und löscht die Planungszeile, wenn Sie **Änderungen speichern** auf der Registerkarte **Vorgang** auswählen. Das Symbol wird als Diskette mit einem roten Kreuz angezeigt, wenn der Vorrat gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="74cf6-195">Deletes the element in the **Timeline** FastTab and deletes the planning line when you choose **Save Changes** on the **Process** tab. The icon changes to a disk that has a red cross when the supply has been deleted.</span></span> <span data-ttu-id="74cf6-196">**HINWEIS:**  Sie können nur einen Vorrat mit dem Ereignismeldungstyp *Neu* löschen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-196">**Note:**  You can only delete a supply of action message type *New*.</span></span> <span data-ttu-id="74cf6-197">Nachdem Sie **Änderungen speichern** auf der Registerkarte **Vorgang** ausgewählt haben, müssen Sie die betreffende Planungszeile im Planungs- oder Bestellvorschlag manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-197">After you choose **Save Changes** on the **Process** tab, you must manually delete the planning line in question in the planning or requisition worksheet.</span></span>|  
 |<span data-ttu-id="74cf6-198">**Beleg anzeigen**</span><span class="sxs-lookup"><span data-stu-id="74cf6-198">**Show Document**</span></span>|<span data-ttu-id="74cf6-199">Öffnet die Bestellung, Planungszeile oder Planung, die das Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="74cf6-199">Opens the order, planning line, or forecast that the element represents.</span></span>|  
 |<span data-ttu-id="74cf6-200">**Verkleinern (Ctrl++)**</span><span class="sxs-lookup"><span data-stu-id="74cf6-200">**Zoom Out (Ctrl++)**</span></span>|<span data-ttu-id="74cf6-201">Vergrössert die Skala der x-Achse, sodass weniger Tage angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="74cf6-201">Makes the scale of the x-axis larger, so that fewer days are shown.</span></span> <span data-ttu-id="74cf6-202">**Hinweis:** Sie erreichen dies auch, indem Sie CTRL drücken und das Mausrad bewegen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-202">**Note:**  You can also do this by pressing Ctrl + scroll mouse wheel.</span></span>|  
 |<span data-ttu-id="74cf6-203">**Vergrössern (Ctrl+-)**</span><span class="sxs-lookup"><span data-stu-id="74cf6-203">**Zoom In (Ctrl+-)**</span></span>|<span data-ttu-id="74cf6-204">Verkleinert die Skala der x-Achse, sodass mehr Tage angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="74cf6-204">Makes the scale of the x-axis smaller, so that more days are shown.</span></span> <span data-ttu-id="74cf6-205">**Hinweis:** Sie erreichen dies auch, indem Sie STRG drücken + das Mausrad bewegen.</span><span class="sxs-lookup"><span data-stu-id="74cf6-205">**Note:**  You can also do this by pressing Ctrl + scroll mouse wheel.</span></span>|  
 |<span data-ttu-id="74cf6-206">**Zoom zurücksetzen (Ctrl+0)**</span><span class="sxs-lookup"><span data-stu-id="74cf6-206">**Reset Zoom (Ctrl+0)**</span></span>|<span data-ttu-id="74cf6-207">Setzt die Skala der x-Achse wieder auf den ursprünglichen Zustand vor dem Zoomen zurück.</span><span class="sxs-lookup"><span data-stu-id="74cf6-207">Reverts the scale of the x-axis to what was used before you zoomed.</span></span>|  

<span data-ttu-id="74cf6-208">Zusätzlich zu den Tastaturaktionen, die zuvor erwähnt wurden, können Sie im Inforegister **Zeitachse** auch die folgenden Tastaturaktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="74cf6-208">In addition to the keyboard actions that were mentioned earlier, you can also use the following keyboard actions in the **TimeLine** FastTab.</span></span>  

 |<span data-ttu-id="74cf6-209">Tastaturaktion</span><span class="sxs-lookup"><span data-stu-id="74cf6-209">Keyboard Action</span></span>|<span data-ttu-id="74cf6-210">Description</span><span class="sxs-lookup"><span data-stu-id="74cf6-210">Description</span></span>|  
 |---------------------|---------------------------------------|  
 |<span data-ttu-id="74cf6-211">Ctrl+ Mausrad bewegen</span><span class="sxs-lookup"><span data-stu-id="74cf6-211">Ctrl + scroll mouse wheel</span></span>|<span data-ttu-id="74cf6-212">Ändert die Skala der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="74cf6-212">Changes the scale of the x-axis.</span></span>|  
 |<span data-ttu-id="74cf6-213">Wählen Sie ein Element aus, und drücken Sie dann SHIFT+PFEILTASTE.</span><span class="sxs-lookup"><span data-stu-id="74cf6-213">Select an element, then press Shift+Arrow</span></span>|<span data-ttu-id="74cf6-214">Verschiebt das Element in Richtung der Pfeilspitze.</span><span class="sxs-lookup"><span data-stu-id="74cf6-214">Moves the element in the direction of the arrow stroke.</span></span>|  
 |<span data-ttu-id="74cf6-215">Register</span><span class="sxs-lookup"><span data-stu-id="74cf6-215">Tab</span></span>|<span data-ttu-id="74cf6-216">Springt zum nächsten Element.</span><span class="sxs-lookup"><span data-stu-id="74cf6-216">Moves to the next element.</span></span>|  
 |<span data-ttu-id="74cf6-217">SHIFT+TAB</span><span class="sxs-lookup"><span data-stu-id="74cf6-217">Shift+Tab</span></span>|<span data-ttu-id="74cf6-218">Springt zum vorherigen Element.</span><span class="sxs-lookup"><span data-stu-id="74cf6-218">Moves to the previous element.</span></span>|  
 |<span data-ttu-id="74cf6-219">Drücken Sie beim Verschieben eines Elements die ESC-Taste.</span><span class="sxs-lookup"><span data-stu-id="74cf6-219">While moving an element, press Esc.</span></span>|<span data-ttu-id="74cf6-220">Bricht die Verschiebung ab.</span><span class="sxs-lookup"><span data-stu-id="74cf6-220">Cancels the move.</span></span> <span data-ttu-id="74cf6-221">**Hinweis:** Funktioniert nicht, wenn Sie die Maustaste freigegeben haben.</span><span class="sxs-lookup"><span data-stu-id="74cf6-221">**Note:**  Does not work if you have released the mouse button.</span></span>|

## <a name="see-also"></a><span data-ttu-id="74cf6-222">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74cf6-222">See Also</span></span>  
<span data-ttu-id="74cf6-223">[Planung](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="74cf6-223">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="74cf6-224">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="74cf6-224">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="74cf6-225">[Bearbeitungen](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="74cf6-225">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="74cf6-226">Lagerbesttand</span><span class="sxs-lookup"><span data-stu-id="74cf6-226">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="74cf6-227">Einkauf</span><span class="sxs-lookup"><span data-stu-id="74cf6-227">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="74cf6-228">[Designdetails: Vorratsplanung](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="74cf6-228">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="74cf6-229">Bewährte Einrichtungsmethoden: Beschaffungsplanung</span><span class="sxs-lookup"><span data-stu-id="74cf6-229">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="74cf6-230">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="74cf6-230">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
