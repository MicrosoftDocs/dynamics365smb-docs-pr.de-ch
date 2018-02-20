---
title: "Einrichten von Status für Serviceaufträge und Reparaturen | Microsoft Docs"
description: "Sie müssen neun Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8ffd5d6893b2b6c8ce7b7377c586f4f5414279b5
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="80f96-103">Einrichten von Status für Serviceaufträge und Reparaturen</span><span class="sxs-lookup"><span data-stu-id="80f96-103">Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="80f96-104">Sie müssen Reparaturstatusoptionen einrichten, die den Fortschritt von Reparatur- und Wartungsarbeiten in Serviceaufträgen widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="80f96-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="80f96-105">Sie müssen mindestens neun Reparaturstatusoptionen eingerichtet werden, die die Situation oder Aktionen von Servicearbeiten an Serviceartikeln kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="80f96-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="80f96-106">Sie können die Prioritätsstufe für die Optionen des Serviceauftragsstatus festlegen.</span><span class="sxs-lookup"><span data-stu-id="80f96-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="80f96-107">Die vier Prioritäten lauten: "Hoch" und "Sehr Hoch", "Sehr Gering" und "Gering".</span><span class="sxs-lookup"><span data-stu-id="80f96-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  
  
<span data-ttu-id="80f96-108">Wenn Sie den Reparaturstatus eines Serviceartikels in einem Serviceauftrag ändern, wird der Serviceauftragsstatus aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="80f96-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="80f96-109">Der Reparaturstatus jedes Serviceartikels ist mit dem Serviceauftragsstatus verknüpft.</span><span class="sxs-lookup"><span data-stu-id="80f96-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="80f96-110">Sind die Serviceartikel mit zwei oder mehr Serviceauftragsstatusoptionen verknüpft, wird der Serviceauftragsstatus mit der höchsten Priorität ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="80f96-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="80f96-111">So richten Sie einen Reparaturstatus ein</span><span class="sxs-lookup"><span data-stu-id="80f96-111">To set up a repair status</span></span>  
1. <span data-ttu-id="80f96-112">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Reparaturstatus** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="80f96-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Repair Status**, and then choose the related link.</span></span> <span data-ttu-id="80f96-113">2.</span><span class="sxs-lookup"><span data-stu-id="80f96-113">2.</span></span> <span data-ttu-id="80f96-114">Erstellen Sie einen neuen Reparaturstatus.</span><span class="sxs-lookup"><span data-stu-id="80f96-114">Create a new repair status.</span></span>  
3. <span data-ttu-id="80f96-115">Füllen Sie die Felder **Code** und **Beschreibung** aus.</span><span class="sxs-lookup"><span data-stu-id="80f96-115">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="80f96-116">Wählen Sie im **Serviceauftragsstatus** Feld den Auftragsstatus aus, mit dem der Reparaturstatus verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="80f96-116">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="80f96-117">Das Feld **Priorität** zeigt die Priorität des von Ihnen ausgewählten Serviceauftragsstatus.</span><span class="sxs-lookup"><span data-stu-id="80f96-117">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="80f96-118">Wählen Sie einen Reparaturstatus aus.</span><span class="sxs-lookup"><span data-stu-id="80f96-118">Choose a repair status.</span></span> <span data-ttu-id="80f96-119">Sie können nur einen auswählen.</span><span class="sxs-lookup"><span data-stu-id="80f96-119">You can choose only one.</span></span>  
6. <span data-ttu-id="80f96-120">Um Serviceverträge, einschliesslich Serviceartikel, mit diesem Reparaturstatus buchen zu können, wählen Sie das Feld **Buchen zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="80f96-120">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="80f96-121">Um die Serviceauftragsstatusoption in Serviceaufträgen, die Serviceartikel mit diesem Reparaturstatus enthalten, manuell auf **Offen** ändern zu können, wählen Sie das Kontrollkästchen **Status Offen zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="80f96-121">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="80f96-122">Wählen Sie die Kontrollkästchen **Status in Bearbeitung zulassen**, **Status Erledigt zulassen**und **Status Warten zulassen** auf die gleiche Weise aus.</span><span class="sxs-lookup"><span data-stu-id="80f96-122">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="80f96-123">So richten Sie Servicestatusprioritäten ein</span><span class="sxs-lookup"><span data-stu-id="80f96-123">To set up service status priorities</span></span>  
1. <span data-ttu-id="80f96-124">Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceauftragsstatus** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="80f96-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="80f96-125">Wählen Sie den Serviceauftragsstatus aus, für den Sie eine Priorität festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="80f96-125">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="80f96-126">Wählen Sie im Feld **Priorität**die Priorität aus, die Sie diesem Serviceauftragsstatus zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="80f96-126">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="80f96-127">Wiederholen Sie diesen Schritt für jeden Status.</span><span class="sxs-lookup"><span data-stu-id="80f96-127">Repeat this step for each status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="80f96-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80f96-128">See Also</span></span>  
[<span data-ttu-id="80f96-129">Serviceauftragsstatus und Reparaturstatus</span><span class="sxs-lookup"><span data-stu-id="80f96-129">Understanding Service Order Status and Repair Status</span></span>]()  
[<span data-ttu-id="80f96-130">Einrichten der Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="80f96-130">Setting Up Service Management</span></span>](service-setup-service.md)  

