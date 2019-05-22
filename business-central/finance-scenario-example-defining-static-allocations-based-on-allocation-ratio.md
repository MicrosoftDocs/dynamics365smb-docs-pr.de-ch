---
title: Definieren von statischen Umlagen basierend auf dem Verteilungsverhältnis | Microsoft Docs
description: Die statische Umlagemethode basiert auf einem definierten Wert, zum Beispiel die verwendeten Quadratmeter oder ein eingerichtetes Verteilungsverhältnis, wie 5:2:4.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: bd17923913355f883d14beb24136e97a839116e3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243402"
---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a><span data-ttu-id="2caa9-103">Szenario-Beispiel: Definieren von statischen Umlagen basierend auf dem Verteilungsverhältnis</span><span class="sxs-lookup"><span data-stu-id="2caa9-103">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>
<span data-ttu-id="2caa9-104">Die statische Umlagemethode basiert auf einem definierten Wert, zum Beispiel die verwendeten Quadratmeter oder ein eingerichtetes Verteilungsverhältnis, wie 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="2caa9-104">Static allocation method is based on a definite value, such as square meters used, or an established allocation ratio such as 5:2:4.</span></span>  

<span data-ttu-id="2caa9-105">In diesem Thema wird beschrieben, wie drei neue Verteilungsziel-Kostenträger für die Kostenstelle der Verteilungsquelle PROD mithilfe des eingerichteten Verteilungsverhältnisses 5:2:4 definiert wird.</span><span class="sxs-lookup"><span data-stu-id="2caa9-105">This topic describes how to define three new allocation target cost objects for the allocation source PROD cost center using the established allocation ratio 5:2:4.</span></span> <span data-ttu-id="2caa9-106">Die drei Zielkostenträger sind ZUBEHÖR, FARBE und EINRICHTUNG.</span><span class="sxs-lookup"><span data-stu-id="2caa9-106">The three target cost objects are ACCESSO, PAINT, and FITTINGS.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2caa9-107">Das Beispiel verwendet die Demodaten in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="2caa9-107">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><span data-ttu-id="2caa9-108">So definieren die die Kostenstelle der Verteilungsquelle PROD auf dem Inforegister "Allgemein"</span><span class="sxs-lookup"><span data-stu-id="2caa9-108">To define the allocation source PROD cost center on the General FastTab</span></span>  

1.  <span data-ttu-id="2caa9-109">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kostenumlage** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="2caa9-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Allocation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2caa9-110">Wählen Sie auf der Seite **Kostenumlage** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2caa9-110">On the **Cost Allocation** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="2caa9-111">Drücken Sie im Feld **ID** die EINGABETASTE, oder geben Sie eine ID ein.</span><span class="sxs-lookup"><span data-stu-id="2caa9-111">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="2caa9-112">Geben Sie in dem Feld **Menge** **1** ein.</span><span class="sxs-lookup"><span data-stu-id="2caa9-112">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="2caa9-113">In den Feldern **Gültigkeit ab** und **Gültig bis** geben Sie passende Datumsangaben ein.</span><span class="sxs-lookup"><span data-stu-id="2caa9-113">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="2caa9-114">Geben Sie im Feld **Kostenstellencode** **PROD** ein.</span><span class="sxs-lookup"><span data-stu-id="2caa9-114">In the **Cost Center Code** field, enter **PROD**.</span></span>  
7.  <span data-ttu-id="2caa9-115">Geben Sie im Feld **Für Kostenart gutschreiben** die Kostenart **9903** ein.</span><span class="sxs-lookup"><span data-stu-id="2caa9-115">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><span data-ttu-id="2caa9-116">So definieren Sie die Verteilungsziel-Kostenträger auf dem Inforegister "Zeilen"</span><span class="sxs-lookup"><span data-stu-id="2caa9-116">To define the allocation target cost objects on the Lines FastTab</span></span>  

1.  <span data-ttu-id="2caa9-117">Geben Sie in der ersten Rechnungszeile in dem Feld **Zielkostenart** die Zahl **9903** ein.</span><span class="sxs-lookup"><span data-stu-id="2caa9-117">On the first line, in the **Target Cost Type** field, enter **9903**.</span></span>  
2.  <span data-ttu-id="2caa9-118">Wählen Sie in der ersten Rechnungszeile in dem Feld **Zielkosteobjekt** die Option **ACCESSO** aus.</span><span class="sxs-lookup"><span data-stu-id="2caa9-118">On the first line, in the **Target Cost Object** field, select **ACCESSO**.</span></span>  
3.  <span data-ttu-id="2caa9-119">Wählen Sie in der ersten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2caa9-119">On the first line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
4.  <span data-ttu-id="2caa9-120">Wählen Sie in der ersten Zeile im Feld **Basis** die Option **Statisch** aus, um die Methode der statischen Umlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2caa9-120">On the first line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
5.  <span data-ttu-id="2caa9-121">Geben Sie in der ersten Zeile im Feld **Aktie** das Verteilungsverhältnis **5**ein.</span><span class="sxs-lookup"><span data-stu-id="2caa9-121">On the first line, in the **Share** field, enter the allocation ratio **5**.</span></span>  
6.  <span data-ttu-id="2caa9-122">Geben Sie in der zweiten Rechnungszeile in dem Feld **Zielkostenart** die Zahl **9903** ein.</span><span class="sxs-lookup"><span data-stu-id="2caa9-122">On the second line, in the **Target Cost Type** field, enter **9903**.</span></span>  
7.  <span data-ttu-id="2caa9-123">Wählen Sie in der zweiten Rechnungszeile in dem Feld **Zielkosteobjekt** **PAINT.**</span><span class="sxs-lookup"><span data-stu-id="2caa9-123">On the second line, in the **Target Cost Object** field, select **PAINT**.</span></span>  
8.  <span data-ttu-id="2caa9-124">Wählen Sie in der zweiten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2caa9-124">On the second line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
9. <span data-ttu-id="2caa9-125">Wählen Sie in der zweiten Zeile im Feld **Basis** die Option **Statisch** aus, um die Methode der statischen Umlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2caa9-125">On the second line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
10. <span data-ttu-id="2caa9-126">Geben Sie in der zweiten Zeile im Feld **Aktie** das Verteilungsverhältnis **2**ein.</span><span class="sxs-lookup"><span data-stu-id="2caa9-126">On the second line, in the **Share** field, enter the allocation ratio **2**.</span></span>  
11. <span data-ttu-id="2caa9-127">Geben Sie in der dritten Rechnungszeile in dem Feld **Zielkostenart** die Zahl **9903** ein.</span><span class="sxs-lookup"><span data-stu-id="2caa9-127">On the third line, in the **Target Cost Type** field, enter **9903**.</span></span>  
12. <span data-ttu-id="2caa9-128">Wählen Sie in der dritten Rechnungszeile in dem Feld **Zielkosteobjekt** die Option **ACCESSO** aus.</span><span class="sxs-lookup"><span data-stu-id="2caa9-128">On the third line, in the **Target Cost Object** field, select **FITTINGS**.</span></span>  
13. <span data-ttu-id="2caa9-129">Wählen Sie in der dritten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2caa9-129">On the third line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
14. <span data-ttu-id="2caa9-130">Wählen Sie in der dritten Zeile im Feld **Basis** die Option **Statisch** aus, um die Methode der statischen Umlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2caa9-130">On the third line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
15. <span data-ttu-id="2caa9-131">Geben Sie in der dritten Zeile im Feld **Aktie** das Verteilungsverhältnis **4**ein.</span><span class="sxs-lookup"><span data-stu-id="2caa9-131">On the third line, in the **Share** field, enter the allocation ratio **4**.</span></span>  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2caa9-132">berechnet automatisch das Feld  unter Verwendung eines **Prozentsatzes**, der von allen drei Zuteilungsverhältnissen abhängt, die im Feld **Aktie** für alle drei Zeilen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2caa9-132">automatically calculates the **Percent** field using a percentage rate that is dependent on all three allocation ratios that are entered in the **Share** field for all three lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2caa9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2caa9-133">See Also</span></span>  
[<span data-ttu-id="2caa9-134">Definieren und Zuweisen von Kosten</span><span class="sxs-lookup"><span data-stu-id="2caa9-134">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)   
