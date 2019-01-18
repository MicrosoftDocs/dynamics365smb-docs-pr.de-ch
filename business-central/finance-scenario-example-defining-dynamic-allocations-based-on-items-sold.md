---
title: 'Szenario-Beispiel: Definieren von dynamischen Zuteilungen auf der Basis der verkauften Artikel | Microsoft Docs'
description: "Dieses Thema zeigt ein Beispiel für das Definieren von Zuordnungen mithilfe der Methode der dynamischen Verteilung."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 3103583c9781c283479c5f66e90f0e875faf46cc
ms.contentlocale: de-ch
ms.lasthandoff: 11/26/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="c493d-103">Szenario-Beispiel: Definieren von dynamischen Zuteilungen auf der Basis der verkauften Artikel</span><span class="sxs-lookup"><span data-stu-id="c493d-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="c493d-104">Dieses Thema zeigt ein Beispiel für das Definieren von Zuordnungen mithilfe der Methode der dynamischen Verteilung.</span><span class="sxs-lookup"><span data-stu-id="c493d-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="c493d-105">In dem Beispiel ändern Sie die dynamische Verteilung der Kosten für die VERKAUF-Kostenstelle, sodass der neue Kostenträger COMPUTERAUSSTATTUNG unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c493d-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="c493d-106">COMPUTERAUSSTATTUNG-Pakete haben Artikelnummern im Bereich von 8904-W bis 8924-W.</span><span class="sxs-lookup"><span data-stu-id="c493d-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="c493d-107">Sie verwenden die Verkaufszahlen des Vorjahres, um den Anteil zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c493d-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="c493d-108">Die Verteilung wird auf die helfende Kostenart 9903 gebucht.</span><span class="sxs-lookup"><span data-stu-id="c493d-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c493d-109">Das Beispiel verwendet die Demodaten in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="c493d-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="c493d-110">So definieren Sie dynamische Zuteilungen auf der Basis der im Vorjahr verkauften Artikel</span><span class="sxs-lookup"><span data-stu-id="c493d-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="c493d-111">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kostenumlage** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="c493d-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c493d-112">Wählen Sie auf der Seite **Kostenumlage** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="c493d-112">On the **Cost Allocation** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="c493d-113">Drücken Sie im Feld **ID** die EINGABETASTE, oder geben Sie eine ID ein.</span><span class="sxs-lookup"><span data-stu-id="c493d-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="c493d-114">Geben Sie in dem Feld **Menge** **1** ein.</span><span class="sxs-lookup"><span data-stu-id="c493d-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="c493d-115">In den Feldern **Gültigkeit ab** und **Gültig bis** geben Sie passende Datumsangaben ein.</span><span class="sxs-lookup"><span data-stu-id="c493d-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="c493d-116">Geben Sie im Feld **Kostenstellencode** **VERKAUF** ein.</span><span class="sxs-lookup"><span data-stu-id="c493d-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="c493d-117">Geben Sie im Feld **Für Kostenart gutschreiben** die Kostenart **9903** ein.</span><span class="sxs-lookup"><span data-stu-id="c493d-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="c493d-118">Geben Sie im Feld **Für Kostenart gutschreiben** die Kostenart **9903** ein.</span><span class="sxs-lookup"><span data-stu-id="c493d-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="c493d-119">Wählen Sie im Feld **Zielkostenobjekt** die Option **Neu** aus, um einen neuen Kostenträger COMPUTERAUSSTATTUNG zu erstellen, und füllen Sie ggf. Felder aus.</span><span class="sxs-lookup"><span data-stu-id="c493d-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="c493d-120">Wählen Sie **COMPUTERAUSSTATTUNG** aus.</span><span class="sxs-lookup"><span data-stu-id="c493d-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="c493d-121">Lassen Sie das Feld **Zielkostenstelle** leer.</span><span class="sxs-lookup"><span data-stu-id="c493d-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="c493d-122">Wählen Sie in der dritten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c493d-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="c493d-123">Wählen Sie im Feld **Basis** die Verteilungsgrundlage **Verkaufte Artikel (Betrag)** aus.</span><span class="sxs-lookup"><span data-stu-id="c493d-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="c493d-124">Geben Sie im Feld **Nummernfilter** den Wert **8904-W..8924-W** ein.</span><span class="sxs-lookup"><span data-stu-id="c493d-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="c493d-125">In dem Feld **Datumsfiltercode** geben Sie **Vorjahr** ein.</span><span class="sxs-lookup"><span data-stu-id="c493d-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="c493d-126">Damit der Vorschlag berechnet wird, klicken Sie auf Aktionen **Umlageschlüssel berechnen**.</span><span class="sxs-lookup"><span data-stu-id="c493d-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="c493d-127">verwendet die Verkaufszahlen der Vorjahre, um einen Anteil von 1596,50 MW mit 100 Prozent für die COMPUTERAUSSTATTUNG-Pakete zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c493d-127">uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="c493d-128">Das bedeutet, dass alle Artikel, die letztes Jahr verkauft wurden, dem Kostenträger COMPUTERAUSSTATTUNG zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c493d-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c493d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c493d-129">See Also</span></span>  
[<span data-ttu-id="c493d-130">Definieren und Zuweisen von Kosten</span><span class="sxs-lookup"><span data-stu-id="c493d-130">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="c493d-131">[Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="c493d-131">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="c493d-132">Informationen zur Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="c493d-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

