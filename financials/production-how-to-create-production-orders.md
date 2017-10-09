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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0c792dbb7d7261e8f8b89ca4f3d39d875142c4eb
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-production-order-headers"></a><span data-ttu-id="4beff-103">So wird's gemacht: Fertigungsauftragsköpfe erstellen</span><span class="sxs-lookup"><span data-stu-id="4beff-103">How to: Create Production Order Headers</span></span>
<span data-ttu-id="4beff-104">Sie können Fertigungsaufträge manuell erstellen, und der erste Schritt in diesem Ablauf ist das Erstellen des Fertigungsauftragskopfs.</span><span class="sxs-lookup"><span data-stu-id="4beff-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="4beff-105">Fertigungsaufträge werden üblicherweise bei einem dieser Planungsfunktion erstellt, um einen bekannten Bedarf zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="4beff-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="4beff-106">Weitere Informationen finden Sie unter [Planung](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="4beff-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="4beff-107">Im weiteren Prozess wird ein fest geplanter Fertigungsauftrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="4beff-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="4beff-108">Sie können auch Fertigungsaufträge mit einem anderen Status erstellen.</span><span class="sxs-lookup"><span data-stu-id="4beff-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="4beff-109">Fertigungsauftragsköpfe erstellen</span><span class="sxs-lookup"><span data-stu-id="4beff-109">To create a production order header</span></span>  
1.  <span data-ttu-id="4beff-110">Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen ") aus und geben Sie **Feste Auftragsplanung** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="4beff-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4beff-111">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4beff-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="4beff-112">Geben Sie im Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="4beff-112">In the **No.**</span></span> <span data-ttu-id="4beff-113">die nächste Nummer aus der Serie ein.</span><span class="sxs-lookup"><span data-stu-id="4beff-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="4beff-114">Wählen Sie im Feld **Herkunftsart.** die Herkunft des Fertigungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="4beff-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="4beff-115">Hier können Sie auswählen, eine Fertigungsfamilie zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="4beff-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="4beff-116">Weitere Informationen finden Sie unter [Vorgehensweise: Mit Stücklisten arbeiten](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="4beff-116">For more information, see [How to: Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="4beff-117">Wählen Sie im Feld **Herkunftsnr.** die Artikelnummer, Fertigungsfamilie oder den Verkaufskopf aus, für die/den der Fertigungsauftrag erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4beff-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="4beff-118">Füllen Sie die Felder **Menge** und **Fälligkeitsdatum** entsprechend Ihren Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="4beff-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="4beff-119">Wenn Sie Produktionsanforderungen, wie Komponenten oder Arbeitsgänge ändern, können Sie schnell  einen Fertigungsauftrag neu planen.</span><span class="sxs-lookup"><span data-stu-id="4beff-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="4beff-120">Weitere Informationen finden Sie unter [Vorgehensweise:Aktualisieren oder ersetzen von Produktionsaufträgen.](production-how-to-replan-refresh-production-orders.md)</span><span class="sxs-lookup"><span data-stu-id="4beff-120">For more information, see [How to: Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="4beff-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4beff-121">See Also</span></span>  
<span data-ttu-id="4beff-122">[Bearbeitungen](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="4beff-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="4beff-123">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="4beff-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="4beff-124">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="4beff-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="4beff-125">Lagerbesttand</span><span class="sxs-lookup"><span data-stu-id="4beff-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4beff-126">Einkauf</span><span class="sxs-lookup"><span data-stu-id="4beff-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4beff-127">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4beff-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

