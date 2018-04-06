---
title: 'Designdetails: Planungs-Zuordnungstabelle | Microsoft Docs'
description: "Dieses Thema gibt Einblicke dazu, was sich ändert, wenn Sie einen Artikel für die Planung ändern."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3e412c6fe82b3ee5640329c523b19d68f849f93a
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-planning-assignment-table"></a><span data-ttu-id="0f074-103">Designdetails: Planungs-Zuordnungstabelle</span><span class="sxs-lookup"><span data-stu-id="0f074-103">Design Details: Planning Assignment Table</span></span>
<span data-ttu-id="0f074-104">Alle Artikel sollten eingeplant werden, es gibt jedoch keinen Grund, einen Plan für einen Artikel zu berechnen, es sei denn, es gab eine Änderung im Bedarfs- oder Vorratsmuster seit der letzten Berechnung des Plans.</span><span class="sxs-lookup"><span data-stu-id="0f074-104">All items should be planned for, however, there is no reason to calculate a plan for an item unless there has been a change in the demand or supply pattern since the last time a plan was calculated.</span></span>  
  
<span data-ttu-id="0f074-105">Wenn der Benutzer einen neuen Verkaufsauftrag eingegeben oder einen vorhandenen geändert hat, gibt es Gründe zur Neuberechnung des Plans.</span><span class="sxs-lookup"><span data-stu-id="0f074-105">If the user has entered a new sales order or changed an existing one, there is reason to recalculate the plan.</span></span> <span data-ttu-id="0f074-106">Andere Ursachen beinhalten eine Änderung in der Planung oder im gewünschten Sicherheitsbestand.</span><span class="sxs-lookup"><span data-stu-id="0f074-106">Other reasons include a change in forecast or the desired safety stock quantity.</span></span> <span data-ttu-id="0f074-107">Das Ändern einer Stückliste durch Hinzufügen oder Entfernen einer Komponente führt wahrscheinlich zur Anzeige einer Änderung, jedoch nur für den Komponentenartikel.</span><span class="sxs-lookup"><span data-stu-id="0f074-107">Changing a bill of material by adding or removing a component would most likely indicate a change, but for the component item only.</span></span>  
  
<span data-ttu-id="0f074-108">Für mehrere Lagerorte findet die Zuweisung auf Artikelebene pro Lagerortkombination statt.</span><span class="sxs-lookup"><span data-stu-id="0f074-108">For multiple locations, the assignment takes place at the level of item per location combination.</span></span> <span data-ttu-id="0f074-109">Wenn beispielsweise ein Auftrag an nur einem Lagerplatz erstellt wurde, ordnet die Anwendung den Artikel an diesem bestimmten Lagerort für die Planung zu.</span><span class="sxs-lookup"><span data-stu-id="0f074-109">If, for example, a sales order has been created at only one location, the program will assign the item at that specific location for planning.</span></span>  
  
<span data-ttu-id="0f074-110">Der Grund für die Auswahl von Artikeln für die Planung hat mit der Systemleistung zu tun.</span><span class="sxs-lookup"><span data-stu-id="0f074-110">The reason for selecting items for planning is a matter of system performance.</span></span> <span data-ttu-id="0f074-111">Wenn keine Änderung des Bedarf-Vorrat-Musters eines Artikels eingetreten ist, schlägt das Planungssystem keine Aktionen vor.</span><span class="sxs-lookup"><span data-stu-id="0f074-111">If no change in an item’s demand-supply pattern has occurred, the planning system will not suggest any actions to be taken.</span></span> <span data-ttu-id="0f074-112">Ohne die Planungs-Zuweisung müsste das System die Berechnungen für alle Artikel ausführen, um herauszufinden, was zu planen ist, wodurch die Systemressourcen belastet würden.</span><span class="sxs-lookup"><span data-stu-id="0f074-112">Without the planning assignment, the system would have to perform the calculations for all items in order to find out what to plan for, and that would drain system resources.</span></span>  
  
<span data-ttu-id="0f074-113">Die Tabelle **Planning Assignment** überwacht Bedarf und Vorrat und ordnet die entsprechenden Artikel für die Planung zu.</span><span class="sxs-lookup"><span data-stu-id="0f074-113">The **Planning Assignment** table monitors demand and supply events and assigns the appropriate items for planning.</span></span> <span data-ttu-id="0f074-114">Die folgenden Ereignisse werden überwacht:</span><span class="sxs-lookup"><span data-stu-id="0f074-114">The following events are monitored:</span></span>  
  
* <span data-ttu-id="0f074-115">Ein neuer Verkaufsauftrag, eine Planung, eine Komponente, eine Bestellung, ein Fertigungsauftrag, ein Montageauftrag oder ein Umlagerungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="0f074-115">A new sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="0f074-116">Änderung von Artikel, Menge, Lagerort, Variante oder Datum auf einem Verkaufsauftrag, Plan, einer Komponente, einem Einkaufsauftrag, einem Produktionsauftrag, einem Montageauftrag oder einem Umlagerungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="0f074-116">Change of item, quantity, location, variant, or date on a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="0f074-117">Stornierung eines Verkaufsauftrags, einer Planung, einer Komponente, einer Bestellung, eines Fertigungsauftrags, eines Montageauftrags oder eines Umlagerungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="0f074-117">Cancellation of a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="0f074-118">Verbrauch von Artikeln ausserhalb der Planung.</span><span class="sxs-lookup"><span data-stu-id="0f074-118">Consumption of items other than planned.</span></span>  
* <span data-ttu-id="0f074-119">Istmeldungen von Artikeln ausserhalb der Planung.</span><span class="sxs-lookup"><span data-stu-id="0f074-119">Output of items other than planned.</span></span>  
* <span data-ttu-id="0f074-120">Ungeplante Bestandänderungen.</span><span class="sxs-lookup"><span data-stu-id="0f074-120">Unplanned changes in inventory.</span></span>  
  
<span data-ttu-id="0f074-121">Für diese direkten Vorrat-Bedarf-Verschiebungen wahrt das Auftragstracking- und Aktionsmeldungssystem die Planungs-Zuordnungstabelle und gibt einen Planungsgrund als Aktionsmeldung aus.</span><span class="sxs-lookup"><span data-stu-id="0f074-121">For these direct supply-demand displacements, the order tracking and action messaging system maintains the Planning Assignment table and states a planning reason as an action message.</span></span>  
  
<span data-ttu-id="0f074-122">Die folgenden Änderungen in den Stammdaten können ebenfalls eine Planungsunausgeglichenheit verursachen:</span><span class="sxs-lookup"><span data-stu-id="0f074-122">The following changes in master data can also cause a planning imbalance:</span></span>  
  
* <span data-ttu-id="0f074-123">Änderung des Status zu Zertifiziert im Fertigungsstücklistenkopf (für alle Artikel mit diesem Kopf).</span><span class="sxs-lookup"><span data-stu-id="0f074-123">Change of status to Certified in the production BOM header (for all items using that header).</span></span>  
* <span data-ttu-id="0f074-124">Gelöschte Zeile (untergeordneter Artikel).</span><span class="sxs-lookup"><span data-stu-id="0f074-124">Deleted line (child item).</span></span>  
* <span data-ttu-id="0f074-125">Änderung des Status zu Zertifiziert im Arbeitsplankopf (für alle Artikel mit diesem Arbeitsplan).</span><span class="sxs-lookup"><span data-stu-id="0f074-125">Change of status to Certified in the routing header (for all items using that routing).</span></span>  
* <span data-ttu-id="0f074-126">Änderungen in den folgenden Artikelkartenfeldern.</span><span class="sxs-lookup"><span data-stu-id="0f074-126">Changes in the following item card fields.</span></span>  
* <span data-ttu-id="0f074-127">Sicherheitsbestand oder Sicherh.-Zuschl. Beschaff.-Zt.</span><span class="sxs-lookup"><span data-stu-id="0f074-127">Safety Stock Quantity or Safety Lead Time.</span></span>  
* <span data-ttu-id="0f074-128">Beschaffungszeit.</span><span class="sxs-lookup"><span data-stu-id="0f074-128">Lead Time Calculation.</span></span>  
* <span data-ttu-id="0f074-129">Minimalbestand.</span><span class="sxs-lookup"><span data-stu-id="0f074-129">Reorder Point.</span></span>  
* <span data-ttu-id="0f074-130">Fert.-Stücklistennr (und alle untergeordneten Elemente der alten Stücklistenreferenz).</span><span class="sxs-lookup"><span data-stu-id="0f074-130">Production BOM No. (and all children of old BOM reference).</span></span>  
* <span data-ttu-id="0f074-131">Arbeitsplannr.</span><span class="sxs-lookup"><span data-stu-id="0f074-131">Routing No.</span></span>  
* <span data-ttu-id="0f074-132">Wiederbeschaffungsverfahren.</span><span class="sxs-lookup"><span data-stu-id="0f074-132">Reordering Policy.</span></span>  
  
<span data-ttu-id="0f074-133">In diesen Fällen verwaltet eine neue Funktion, Planungszuweisungs-Verwaltung, die Tabelle und zeigt den Planungsgrund als Nettoänderung an.</span><span class="sxs-lookup"><span data-stu-id="0f074-133">In these cases, a new function, Planning Assignment Management, maintains the table and states the planning reason as Net Change.</span></span>  
  
<span data-ttu-id="0f074-134">Die folgenden Änderungen verursachen keine Planungszuweisung:</span><span class="sxs-lookup"><span data-stu-id="0f074-134">The following changes do not cause a planning assignment:</span></span>  
  
* <span data-ttu-id="0f074-135">Kalender</span><span class="sxs-lookup"><span data-stu-id="0f074-135">Calendars</span></span>  
* <span data-ttu-id="0f074-136">Andere Planungsparameter auf einer Artikelkarte sind:</span><span class="sxs-lookup"><span data-stu-id="0f074-136">Other planning parameters on the item card</span></span>  
  
<span data-ttu-id="0f074-137">Wenn sie eine Prod.-Programmplanung oder einen Nettobedarf berechnen, gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="0f074-137">When calculating an MPS or an MRP, the following restrictions apply:</span></span>  
  
* <span data-ttu-id="0f074-138">Prod.-Programmplanung: Die Planungssystemprüfungen, ob der Artikel eine Absatzplanung oder einen Verkaufsauftrag führt.</span><span class="sxs-lookup"><span data-stu-id="0f074-138">MPS: The planning system checks that the item carries a production forecast or a sales order.</span></span> <span data-ttu-id="0f074-139">Wenn nicht, ist der Artikel nicht im Plan enthalten.</span><span class="sxs-lookup"><span data-stu-id="0f074-139">If not, the item is not included in the plan.</span></span>  
* <span data-ttu-id="0f074-140">Nettobedarf: Wenn das Planungssystem erkennt, dass der Artikel durch eine Prod.-Programmplanungs-Planungszeile oder einen Prod.-Programmplanungs-Beschaffungsauftrag aufgefüllt wird, wird der Artikel aus der Planung genommen.</span><span class="sxs-lookup"><span data-stu-id="0f074-140">MRP: If the planning system detects that the item is being replenished by an MPS planning line or MPS supply order, the item will be left out of the planning.</span></span> <span data-ttu-id="0f074-141">Jedoch ist jeder Bedarf aus den entsprechenden Komponenten enthalten.</span><span class="sxs-lookup"><span data-stu-id="0f074-141">However, any demand from relevant components is included.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f074-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f074-142">See Also</span></span>  
<span data-ttu-id="0f074-143">[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="0f074-143">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="0f074-144">[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="0f074-144">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
<span data-ttu-id="0f074-145">[Designdetails: Umlagerungen in Planung](design-details-transfers-in-planning.md) </span><span class="sxs-lookup"><span data-stu-id="0f074-145">[Design Details: Transfers in Planning](design-details-transfers-in-planning.md) </span></span>  
[<span data-ttu-id="0f074-146">Designdetails: Planungsparameter</span><span class="sxs-lookup"><span data-stu-id="0f074-146">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  

