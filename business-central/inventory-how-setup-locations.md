---
title: Einrichten einer Lagerortkarte und definieren von Umlagerungsrouten| Microsoft Docs
description: "Sie stellen eine Lagerortkarte für jedes Bundesland, den von Lagerartikel speichern, beispielsweise, ein Lager oder eine Vertriebsstelle und Einrichtungsrouten, um Artikel zwischen Lagerorten umlagern erstellen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 45943ef97eee9d6bf24fd679e5dbbab96f5177f8
ms.contentlocale: de-ch
ms.lasthandoff: 04/18/2018

---
# <a name="set-up-locations"></a><span data-ttu-id="9c9ed-103">Einrichten von Lagerorten</span><span class="sxs-lookup"><span data-stu-id="9c9ed-103">Set Up Locations</span></span>
<span data-ttu-id="9c9ed-104">Wenn Sie Artikel a mehr als einem Ort oder Lagerort kaufen, lagern oder verkaufen, müssen Sie jeden Lagerplatz mit einer Lagerortkarte einrichten und Umlagerungsrouten definieren.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="9c9ed-105">Sie können dann Belegzeilen für einen bestimmten Lagerplatz erstellen, Verfügbarkeit nach Lagerplatz anzeigen und Lagerbestand zwischen Lagerplätzen umlagern.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="9c9ed-106">Weitere Informationen finden Sie unter [Lagerbestand verwalten](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="9c9ed-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="9c9ed-107">So erstellen Sie eine Lagerortkarte</span><span class="sxs-lookup"><span data-stu-id="9c9ed-107">To create a location card</span></span>
1. <span data-ttu-id="9c9ed-108">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplätze** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="9c9ed-109">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="9c9ed-110">Füllen Sie im Fenster **Lagerortkarte** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-110">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="9c9ed-111">Wiederholen Sie die Schritte 2 und 3 für jeden Lagerplatz, an dem Sie Lagerbestand aufbewahren möchten.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="9c9ed-112">Viele Felder auf der Lagerortkarte beziehen sich auf Auftragsabwicklung von Artikel in eingehenden und ausgehenden Lagerprozessen.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="9c9ed-113">Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="9c9ed-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="9c9ed-114">So erstellen Sie eine Umlagerungsroute</span><span class="sxs-lookup"><span data-stu-id="9c9ed-114">To create a transfer route</span></span>
1. <span data-ttu-id="9c9ed-115">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplätze** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="9c9ed-116">Alternativ wählen Sie von jedem beliebigen Fenster **Standortkarten** die Aktion **Umlagerungsrouten** aus.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-116">Alternatively, from any **Location Card** window, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="9c9ed-117">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="9c9ed-118">Füllen Sie im Fenster **Lagerortkarte** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-118">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="9c9ed-119">Sie können jetzt die Lagerartikel zwischen zwei Lagerplätzen umlagern.</span><span class="sxs-lookup"><span data-stu-id="9c9ed-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="9c9ed-120">Weitere Informationen finden Sie unter [Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="9c9ed-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="9c9ed-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c9ed-121">See Also</span></span>
[<span data-ttu-id="9c9ed-122">Verwalten des Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="9c9ed-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="9c9ed-123">[Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="9c9ed-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="9c9ed-124">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9c9ed-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="9c9ed-125">Sie können auswählen, welche Funktionen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="9c9ed-125">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="9c9ed-126">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="9c9ed-126">General Business Functionality</span></span>](ui-across-business-areas.md)

