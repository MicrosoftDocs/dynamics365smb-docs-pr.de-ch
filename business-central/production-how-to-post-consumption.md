---
title: Den Verbrauch über Stapelverarbeitung buchen
description: Wenn die Spülmethode Manuell ist, müssen Sie die Komponenten manuell buchen, indem Sie ein Verbrauchsjournal verwenden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0b3ee6ca54e21605b4e9cf340b04656694c9801e
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935200"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="d1d7c-103">Produktionsverbrauch mit Stapelverarbeitung buchen</span><span class="sxs-lookup"><span data-stu-id="d1d7c-103">Batch Post Production Consumption</span></span>

<span data-ttu-id="d1d7c-104">Wenn die Buchungsmethode **Manuell** ist, müssen Sie den Verbrauch manuell mit einem Verbrauchsprotokoll buchen.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>  

>[!NOTE]
> <span data-ttu-id="d1d7c-105">Wenn Sie auf der Lagerortkarte im Feld **Kommissionierung erforderlich** ein Häkchen gesetzt haben, um anzugeben, dass für den Lagerort die Bearbeitung der Kommissionierung erforderlich ist, müssen Sie diese Stapelvearbeitung nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-105">If you have placed a check mark in the **Require Pick** field on the location card to indicate that the location requires inventory pick processing, then you do not need to use this batch job.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d1d7c-106">übernimmt den Verbrauch, wenn Sie die Lagerkommissionierung buchen.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-106">will handle consumption when you post the inventory pick.</span></span> <span data-ttu-id="d1d7c-107">Weitere Informationen finden Sie unter [Herausnehmen für die Produktion in grundlegenden Lagerort-Konfigurationen](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).</span><span class="sxs-lookup"><span data-stu-id="d1d7c-107">For more information, see [Pick for Production in Basic Warehouse Configurations](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).</span></span>  

<span data-ttu-id="d1d7c-108">Sie können [!INCLUDE[prod_short](includes/prod_short.md)] so einstellen, um automatisch (*flush*) Komponenten zu buchen, wenn Sie beginnen oder Fertigungsaufträge beenden.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-108">You can also set up [!INCLUDE[prod_short](includes/prod_short.md)] to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="d1d7c-109">Weitere Informationen finden Sie unter [Komponenten entsprechend dem Arbeitsgangs-Ausstoss leeren](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="d1d7c-109">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="d1d7c-110">Die Laufzeit für eine oder mehrere Verbrauchszeile buchen</span><span class="sxs-lookup"><span data-stu-id="d1d7c-110">To post consumption for one or more production order lines</span></span>

1. <span data-ttu-id="d1d7c-111">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **FA-Verbrauchs Erf.-Journal** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d1d7c-112">Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Verbrauchsdaten aus.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-112">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="d1d7c-113">Verwenden Sie die Aktion **Verbrauch berechnen**, um Erfassungsjournalzeilen von Fertigungsaufträgen basierend auf der Berechnung der Verbrauchsmenge auf der Ist-Menge (der Menge der fertig gestellten Artikel, die Sie ausgewertet haben) oder der Soll-Menge (der Menge von Artikeln, die Sie fertigen möchten) basiert.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-113">Use the **Calc. Consumption** action to generate journal lines from production orders based on the actual output (the quantity of finished goods that you have reported) or on the expected output (the quantity of finished goods that you expect to produce).</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1d7c-114">Wenn Sie die Standortkarte so konfiguriert haben, dass eine Lagerentnahme erforderlich ist, können nur Mengen eingegeben werden, die bereits über eine Lageraktivität im Feld **Menge** auf der Seite **Verbrauchsjournal** kommissioniert wurden, keine berechnete Menge.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-114">If you configured the location card to require warehouse pick processing, then only quantities that are already picked through a warehouse activity can be entered in the **Quantity** field in the **Consumption Journal** page, not any calculated quantity.</span></span> <span data-ttu-id="d1d7c-115">Weitere Informationen unter [Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="d1d7c-115">For more information, see [Pick for Production or Assembly in Advanced Warehouse Configurations](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span></span>

3. <span data-ttu-id="d1d7c-116">Um den Verbrauch zu buchen, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-116">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="d1d7c-117">Die damit verbundenen Bestände werden reduziert.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-117">The related inventories are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1d7c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1d7c-118">See Also</span></span>

[<span data-ttu-id="d1d7c-119">Produktion</span><span class="sxs-lookup"><span data-stu-id="d1d7c-119">Manufacturing</span></span>](production-manage-manufacturing.md)  
[<span data-ttu-id="d1d7c-120">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="d1d7c-120">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="d1d7c-121">Planung</span><span class="sxs-lookup"><span data-stu-id="d1d7c-121">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="d1d7c-122">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="d1d7c-122">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d1d7c-123">Einkauf</span><span class="sxs-lookup"><span data-stu-id="d1d7c-123">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="d1d7c-124">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d1d7c-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]
