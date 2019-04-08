---
title: 'So geht es: Fertigungsauftragsüberschriften herstellen | Microsoft Docs'
description: Sie können Fertigungsaufträge manuell erstellen, und der erste Schritt in diesem Ablauf ist das Erstellen des Fertigungsauftragskopfs.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 13d699dbeb8fe2c3979a7b6bd330b14f077d2d3c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "818996"
---
# <a name="create-production-order-headers"></a><span data-ttu-id="9667f-103">Fertigungsauftragsköpfe erstellen</span><span class="sxs-lookup"><span data-stu-id="9667f-103">Create Production Order Headers</span></span>
<span data-ttu-id="9667f-104">Sie können Fertigungsaufträge manuell erstellen, und der erste Schritt in diesem Ablauf ist das Erstellen des Fertigungsauftragskopfs.</span><span class="sxs-lookup"><span data-stu-id="9667f-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="9667f-105">Fertigungsaufträge werden üblicherweise bei einem dieser Planungsfunktion erstellt, um einen bekannten Bedarf zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="9667f-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="9667f-106">Weitere Informationen finden Sie unter [Planung](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="9667f-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="9667f-107">Im weiteren Prozess wird ein fest geplanter Fertigungsauftrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="9667f-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="9667f-108">Sie können auch Fertigungsaufträge mit einem anderen Status erstellen.</span><span class="sxs-lookup"><span data-stu-id="9667f-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="9667f-109">Fertigungsauftragsköpfe erstellen</span><span class="sxs-lookup"><span data-stu-id="9667f-109">To create a production order header</span></span>  
1.  <span data-ttu-id="9667f-110">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Fest geplante Produktionsaufträge** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="9667f-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9667f-111">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="9667f-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="9667f-112">Geben Sie im Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="9667f-112">In the **No.**</span></span> <span data-ttu-id="9667f-113">die nächste Nummer aus der Serie ein.</span><span class="sxs-lookup"><span data-stu-id="9667f-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="9667f-114">Wählen Sie im Feld **Herkunftsart.** die Herkunft des Fertigungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="9667f-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="9667f-115">Hier können Sie auswählen, eine Fertigungsfamilie zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="9667f-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="9667f-116">Weitere Informationen finden Sie unter [Mit Stücklisten arbeiten](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="9667f-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="9667f-117">Wählen Sie im Feld **Herkunftsnr.** die Artikelnummer, Fertigungsfamilie oder den Verkaufskopf aus, für die/den der Fertigungsauftrag erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9667f-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="9667f-118">Füllen Sie die Felder **Menge** und **Fälligkeitsdatum** entsprechend Ihren Anforderungen aus.</span><span class="sxs-lookup"><span data-stu-id="9667f-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="9667f-119">Wenn Sie Produktionsanforderungen, wie Komponenten oder Arbeitsgänge ändern, können Sie schnell  einen Fertigungsauftrag neu planen.</span><span class="sxs-lookup"><span data-stu-id="9667f-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="9667f-120">Weitere Informationen finden Sie unter [Direktes Aktualisieren oder ersetzen von Produktionsaufträgen](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="9667f-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="9667f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9667f-121">See Also</span></span>  
<span data-ttu-id="9667f-122">[Bearbeitungen](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="9667f-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="9667f-123">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="9667f-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="9667f-124">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="9667f-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="9667f-125">Lagerbesttand</span><span class="sxs-lookup"><span data-stu-id="9667f-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9667f-126">Einkauf</span><span class="sxs-lookup"><span data-stu-id="9667f-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9667f-127">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9667f-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
