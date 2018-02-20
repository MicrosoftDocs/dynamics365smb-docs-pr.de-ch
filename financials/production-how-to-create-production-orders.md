---
title: "So geht es: Fertigungsauftragsüberschriften herstellen | Microsoft Docs"
description: "Sie können Fertigungsaufträge manuell erstellen, und der erste Schritt in diesem Ablauf ist das Erstellen des Fertigungsauftragskopfs."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3ffbe781830a492256be864bace38bbef3050596
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="create-production-order-headers"></a><span data-ttu-id="c2b62-103">Fertigungsauftragsköpfe erstellen</span><span class="sxs-lookup"><span data-stu-id="c2b62-103">Create Production Order Headers</span></span>
<span data-ttu-id="c2b62-104">Sie können Fertigungsaufträge manuell erstellen, und der erste Schritt in diesem Ablauf ist das Erstellen des Fertigungsauftragskopfs.</span><span class="sxs-lookup"><span data-stu-id="c2b62-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="c2b62-105">Fertigungsaufträge werden üblicherweise bei einem dieser Planungsfunktion erstellt, um einen bekannten Bedarf zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c2b62-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="c2b62-106">Weitere Informationen finden Sie unter [Planung](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="c2b62-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="c2b62-107">Im weiteren Prozess wird ein fest geplanter Fertigungsauftrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2b62-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="c2b62-108">Sie können auch Fertigungsaufträge mit einem anderen Status erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2b62-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="c2b62-109">Fertigungsauftragsköpfe erstellen</span><span class="sxs-lookup"><span data-stu-id="c2b62-109">To create a production order header</span></span>  
1.  <span data-ttu-id="c2b62-110">Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen ") aus und geben Sie **Feste Auftragsplanung** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="c2b62-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c2b62-111">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="c2b62-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="c2b62-112">Geben Sie im Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="c2b62-112">In the **No.**</span></span> <span data-ttu-id="c2b62-113">die nächste Nummer aus der Serie ein.</span><span class="sxs-lookup"><span data-stu-id="c2b62-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="c2b62-114">Wählen Sie im Feld **Herkunftsart.** die Herkunft des Fertigungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="c2b62-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="c2b62-115">Hier können Sie auswählen, eine Fertigungsfamilie zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="c2b62-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="c2b62-116">Weitere Informationen finden Sie unter [Mit Stücklisten arbeiten](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="c2b62-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="c2b62-117">Wählen Sie im Feld **Herkunftsnr.** die Artikelnummer, Fertigungsfamilie oder den Verkaufskopf aus, für die/den der Fertigungsauftrag erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2b62-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="c2b62-118">Füllen Sie die Felder **Menge** und **Fälligkeitsdatum** entsprechend Ihren Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="c2b62-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="c2b62-119">Wenn Sie Produktionsanforderungen, wie Komponenten oder Arbeitsgänge ändern, können Sie schnell  einen Fertigungsauftrag neu planen.</span><span class="sxs-lookup"><span data-stu-id="c2b62-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="c2b62-120">Weitere Informationen finden Sie unter [Direktes Aktualisieren oder ersetzen von Produktionsaufträgen](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="c2b62-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="c2b62-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2b62-121">See Also</span></span>  
<span data-ttu-id="c2b62-122">[Bearbeitungen](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="c2b62-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="c2b62-123">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="c2b62-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="c2b62-124">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="c2b62-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="c2b62-125">Lagerbesttand</span><span class="sxs-lookup"><span data-stu-id="c2b62-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c2b62-126">Einkauf</span><span class="sxs-lookup"><span data-stu-id="c2b62-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c2b62-127">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c2b62-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

