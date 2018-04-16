---
title: "Vorgehensweise: Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen| Microsoft Docs"
description: Die fertig gestellte Menge stellt den Arbeitsfortschritt in Form der gefertigten Menge dar.
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
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: dea3fa173e1f3a73abac1b22ea111ab5cf5b3a22
ms.contentlocale: de-ch
ms.lasthandoff: 04/16/2018

---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="a80b4-103">Ausgabe über Stapelverarbeitung buchen und Bearbeitungszeiten prüfen</span><span class="sxs-lookup"><span data-stu-id="a80b4-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="a80b4-104">Die fertig gestellte Menge stellt den Arbeitsfortschritt in Form der gefertigten Menge dar.</span><span class="sxs-lookup"><span data-stu-id="a80b4-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="a80b4-105">Nur wenn Sie die fertig gestellte Menge für den letzten Arbeitsgang buchen, dann aktualisiert die Anwendung automatisch den Lagerbestand.</span><span class="sxs-lookup"><span data-stu-id="a80b4-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="a80b4-106">Die fertig gestellte Mengen für eine oder mehrere Fertigungsauftragszeilen buchen</span><span class="sxs-lookup"><span data-stu-id="a80b4-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="a80b4-107">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Ausgabe-Erfassungsjournal** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="a80b4-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a80b4-108">Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Ausgabedaten aus.</span><span class="sxs-lookup"><span data-stu-id="a80b4-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="a80b4-109">Wenn der Arbeitsgang beendet ist, wählen Sie das Feld **Beendet** aus.</span><span class="sxs-lookup"><span data-stu-id="a80b4-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="a80b4-110">Wenn der Lagerort, in den die Artikel eingelagert werden sollen, Lagerplätze verwendet, die Bearbeitung der Einlagerung jedoch nicht erforderlich ist,  weisen Sie der Erf.-Journalzeile einen Lagerplatzcode zu, um festzulegen, wo die Artikel im Lagerort eingelagert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a80b4-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="a80b4-111">Weitere Informationen finden Sie unter [Produktionseinlagerung oder Montageausgabe](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="a80b4-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="a80b4-112">Wählen Sie **Buchen** aus, um die Vorgänge zu buchen.</span><span class="sxs-lookup"><span data-stu-id="a80b4-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="a80b4-113">Die fertig gestellte Menge wird gebucht.</span><span class="sxs-lookup"><span data-stu-id="a80b4-113">The output quantity will be posted.</span></span> <span data-ttu-id="a80b4-114">Der Artikel ist jetzt versandbereit.</span><span class="sxs-lookup"><span data-stu-id="a80b4-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="a80b4-115">Die Laufzeit für eine oder mehrere Fertigungsauftragszeilen buchen</span><span class="sxs-lookup"><span data-stu-id="a80b4-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="a80b4-116">Die Bearbeitungszeit stellt den Arbeitsfortschritt in Form der benötigten Arbeitszeit dar.</span><span class="sxs-lookup"><span data-stu-id="a80b4-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="a80b4-117">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Ausgabe-Erfassungsjournal** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="a80b4-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a80b4-118">Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Ausgabedaten aus.</span><span class="sxs-lookup"><span data-stu-id="a80b4-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="a80b4-119">Wenn der Arbeitsgang beendet ist, wählen Sie das Feld **Beendet** aus.</span><span class="sxs-lookup"><span data-stu-id="a80b4-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="a80b4-120">Wählen Sie die **Buchen** Aktion aus, um die Zeit zu buchen, die je Arbeitsgang aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a80b4-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="a80b4-121">Kapazitätsposten werden für die benötigte Arbeitsplätzen oder Arbeitsplatzgruppen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a80b4-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="a80b4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a80b4-122">See Also</span></span>  
<span data-ttu-id="a80b4-123">[Bearbeitungen](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="a80b4-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="a80b4-124">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="a80b4-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="a80b4-125">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="a80b4-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="a80b4-126">Lagerbesttand</span><span class="sxs-lookup"><span data-stu-id="a80b4-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a80b4-127">Einkauf</span><span class="sxs-lookup"><span data-stu-id="a80b4-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a80b4-128">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a80b4-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

