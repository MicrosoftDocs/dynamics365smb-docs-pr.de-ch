---
title: 'Vorgehensweise: Versandagenten | Microsoft Docs'
description: Sie können einen Code für jeden Spediteur anlegen und Informationen dazu eingeben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fbd27caed8be1e7231f98964890fafed66c7bbbb
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748232"
---
# <a name="set-up-shipping-agents"></a><span data-ttu-id="19745-103">Zusteller einrichten</span><span class="sxs-lookup"><span data-stu-id="19745-103">Set Up Shipping Agents</span></span>
<span data-ttu-id="19745-104">Sie können einen Code für jeden Spediteur anlegen und Informationen dazu eingeben.</span><span class="sxs-lookup"><span data-stu-id="19745-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="19745-105">Wenn Sie eine Internetadresse des Spediteurs eingeben und der Spediteur die Paketverfolgung im Internet anbietet, können Sie die Funktion zur automatischen Paketverfolgung nutzen.</span><span class="sxs-lookup"><span data-stu-id="19745-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="19745-106">Weitere Informationen finden Sie unter [Pakete nachverfolgen](sales-how-track-packages.md)</span><span class="sxs-lookup"><span data-stu-id="19745-106">For more information, see [Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="19745-107">Wenn Sie Spediteure in Ihren Verkaufsaufträgen eingeben, können Sie auch die Transportarten bestimmen, die jeder Spediteur anbietet.</span><span class="sxs-lookup"><span data-stu-id="19745-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="19745-108">Für jeden Spediteur können Sie eine unbegrenzte Anzahl von Transportarten anlegen und Sie können für jede Transportart eine Transportzeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="19745-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="19745-109">Wenn Sie einer Verkaufsauftragszeile eine Spediteurtransportart zugeordnet haben, wird die Transportzeit für diese Zeile in den Lieferterminzusagen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="19745-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="19745-110">Weitere Informationen finden Sie unter [Berechnen von Lieferterminzusagen](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="19745-110">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="19745-111">So richten Sie einen Spediteur ein</span><span class="sxs-lookup"><span data-stu-id="19745-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="19745-112">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Zusteller** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="19745-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="19745-113">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="19745-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="19745-114">.</span><span class="sxs-lookup"><span data-stu-id="19745-114">.</span></span>  
3.  <span data-ttu-id="19745-115">Wählen Sie die Aktion **Spediteurtransportarten**.</span><span class="sxs-lookup"><span data-stu-id="19745-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="19745-116">In **Spediteurtransportarten** füllen Sie die Felder wie notwendig aus.</span><span class="sxs-lookup"><span data-stu-id="19745-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="19745-117">Wenn Sie den Spediteur in der Auftragszeile löschen, wird auch der Spediteur Transportartcode gelöscht.</span><span class="sxs-lookup"><span data-stu-id="19745-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="19745-118">Der Inhalt der Felder, die zum Teil auf der Spediteurtransportart basierten, wird neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="19745-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="19745-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19745-119">See Also</span></span>
[<span data-ttu-id="19745-120">Lieferbedingungen einrichten</span><span class="sxs-lookup"><span data-stu-id="19745-120">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)  
<span data-ttu-id="19745-121">[Pakete verfolgen](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="19745-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="19745-122">Logistik</span><span class="sxs-lookup"><span data-stu-id="19745-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="19745-123">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="19745-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="19745-124">[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="19745-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="19745-125">[Montageverwaltung](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="19745-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="19745-126">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="19745-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="19745-127">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="19745-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
