---
title: Ressourcenverbrauch und Preise aufzeichnen und anpassen | Microsoft Docs
description: "Beschreibt, wie Sie den Ressourcenverbrauch oder den Verbrauch erfassen können, die einem Projekt zugeordnet sind, um Kosten, Preisen und Arbeitstypen zu verwalten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f86fed1b300df98ef120e2f91fdd0785670d04f1
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="22bad-103">Verwenden von Ressourcen für Projekte</span><span class="sxs-lookup"><span data-stu-id="22bad-103">Use Resources for Jobs</span></span>
<span data-ttu-id="22bad-104">Wenn Sie den Verbrauch von Ressourcen im Projekt Erf.-Journal buchen, können Sie die Einstands- und Verkaufspreise, die Arbeitstypen und die damit verknüpften Projekte verfolgen.</span><span class="sxs-lookup"><span data-stu-id="22bad-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="22bad-105">Weitere Informationen finden Sie unter [Nutzung von Projekten](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="22bad-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="22bad-106">Sie können auch den Verbrauch einer Ressource in einem Ressourcen Erf.-Journal buchen.</span><span class="sxs-lookup"><span data-stu-id="22bad-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="22bad-107">Posten, die in einem Ressourcen Erf.-Journal gebucht werden, haben keinen Einfluss auf die Fibu.</span><span class="sxs-lookup"><span data-stu-id="22bad-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="22bad-108">So weisen Sie Projekten Ressourcen zu</span><span class="sxs-lookup"><span data-stu-id="22bad-108">To assign resources to jobs</span></span>
<span data-ttu-id="22bad-109">Sie weisen Projekten Ressourcen zu, indem Sie Projektplanungszeilen für das Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="22bad-109">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="22bad-110">Weitere Informationen finden Sie unter  [Projekte erstellen](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="22bad-110">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="22bad-111">Um Ressourcenverbrauch für ein Projekt buchen</span><span class="sxs-lookup"><span data-stu-id="22bad-111">To record resource usage for a job</span></span>
1. <span data-ttu-id="22bad-112">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen Symbol") und geben **Projektbuch** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="22bad-113">Öffnen Sie das relevante Projekt-Erf.-Journal und füllen Sie die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-113">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="22bad-114">Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-114">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="22bad-115">Um Ressourcenpreise zu justieren:</span><span class="sxs-lookup"><span data-stu-id="22bad-115">To adjust resource prices</span></span>
<span data-ttu-id="22bad-116">Wenn Sie die Einstands- und Verkaufspreise für eine grosse Anzahl von Ressourcen ändern möchten, können Sie den Batchauftrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="22bad-116">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="22bad-117">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Ressourcenkosten/Preise anpassen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="22bad-118">Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-118">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="22bad-119">Diese Stapelverarbeitung erzeugt oder aktualisiert keine alternativen Einkaufs- oder Verkaufspreise für Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="22bad-119">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="22bad-120">Sie ändert lediglich den Inhalt des Feldes auf der Ressourcenkarte für das Feld **Feld korrigieren**, das Sie in der Stapelverarbeitung ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="22bad-120">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="22bad-121">Die Änderung tritt für die Ressourcen sofort in Kraft, überprüfen Sie daher Ihre Korrekturfaktoren, bevor Sie die Stapelverarbeitung ausführen.</span><span class="sxs-lookup"><span data-stu-id="22bad-121">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="22bad-122">Um Ressourcen-Preisänderungsvorschläge auf Basis bestehender alternativer Preise zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="22bad-122">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="22bad-123">Wenn Sie bereits alternative Ressourcenpreise für mehrere Ressourcen eingerichtet haben, können Sie den Batchauftrag verwenden, um alternative Ressourcenpreise einzurichten.</span><span class="sxs-lookup"><span data-stu-id="22bad-123">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="22bad-124">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Ressourcenkosten Änderungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="22bad-125">Wählen Sie die Aktion **Res. Preisänderung (Preis) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-125">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="22bad-126">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-126">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="22bad-127">Wenn die Stapelverarbeitung beendet ist, öffnen Sie das Fenster **Ressourcen-Preisänderungen**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22bad-127">When the batch job is finished, the **Resource Price Changes** window shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="22bad-128">So erstellen Sie Ressourcenpreisvorschläge auf Basis bestehender Standard-VK-Preise</span><span class="sxs-lookup"><span data-stu-id="22bad-128">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="22bad-129">Wenn Sie einen oder mehrere alternative Ressourcenpreise basierend auf den Standardpreisen auf den Ressourcenkarten festlegen möchten, dann können Sie den Batchauftrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="22bad-129">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="22bad-130">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Ressourcenkosten Änderungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="22bad-131">Wählen Sie die Aktion **Res. Preisänderung (Res) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-131">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="22bad-132">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-132">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="22bad-133">Wenn die Stapelverarbeitung beendet ist, öffnen Sie das Fenster **Ressourcen-Preisänderungen**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22bad-133">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="22bad-134">Um Ressourcenpreisvorschläge auf Basis alternierender Preise zu erhalten</span><span class="sxs-lookup"><span data-stu-id="22bad-134">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="22bad-135">Wenn Sie bereits alternative Ressourcenpreise für mehrere Ressourcen eingerichtet haben, können Sie den Batchauftrag verwenden, um alternative Ressourcenpreise einzurichten.</span><span class="sxs-lookup"><span data-stu-id="22bad-135">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="22bad-136">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Res.-VK-&Preisvorschlag (Preis)** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="22bad-137">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-137">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="22bad-138">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="22bad-138">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="22bad-139">Wenn die Stapelverarbeitung beendet ist, öffnen Sie das Fenster **Ressourcen-Preisänderungen**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="22bad-139">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="22bad-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22bad-140">See Also</span></span>
[<span data-ttu-id="22bad-141">Projektmanagement</span><span class="sxs-lookup"><span data-stu-id="22bad-141">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="22bad-142">Finanzen</span><span class="sxs-lookup"><span data-stu-id="22bad-142">Finance</span></span>](finance.md)  
<span data-ttu-id="22bad-143">[Einkauf](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="22bad-143">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="22bad-144">[Verkauf](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="22bad-144">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="22bad-145">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="22bad-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

