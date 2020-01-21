---
title: Analysieren von Actuals vs. Budget | Microsoft Docs
description: Beschreibt, wie die tatsächlichen Beträge mit den budgetierten Beträgen analysiert werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 6773f03a436d1a65eace851abb1e886bdccee55f
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953865"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="35d02-103">Tatsächlichen Beträge mit den budgetierten Beträgen analysieren</span><span class="sxs-lookup"><span data-stu-id="35d02-103">Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="35d02-104">Als Teil des Zusammentragen, Analysieren und Teilen der Firmendaten sehen Sie aktuelle Beträge verglichen mit den budgetierten Beträgen für alle Konten sowie für mehrere Perioden.</span><span class="sxs-lookup"><span data-stu-id="35d02-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="35d02-105">Um budgetierte Beträge zu analysieren, müssen Sie zunächst Sachkonto-Budgets erstellen.</span><span class="sxs-lookup"><span data-stu-id="35d02-105">To analyze budgeted amounts, you must first create G(L budgets.</span></span> <span data-ttu-id="35d02-106">Weitere Informationen finden Sie unter [Sachkonto-Budgets erstellen](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="35d02-106">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="to-view-a-gl-budget"></a><span data-ttu-id="35d02-107">Einsehen eines Sachkonto-Budgets</span><span class="sxs-lookup"><span data-stu-id="35d02-107">To view a G/L budget</span></span>
<span data-ttu-id="35d02-108">In einem Budget mit Dimensionen können Sie die Posten filtern und somit bestimmte Budgets einsehen.</span><span class="sxs-lookup"><span data-stu-id="35d02-108">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="35d02-109">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Sachkontenbudgets** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="35d02-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="35d02-110">Öffnen Sie auf der Seite **G/L Budgets** das Budget, das Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="35d02-110">On the **G/L Budgets** page, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="35d02-111">Auf der Seite oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="35d02-111">At the top of the page, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="35d02-112">Wenn Sie **Periode** entweder im Feld **Als Zeile anzeigen** oder im Feld **Als Spalte anzeigen** ausgewählt haben, müssen Sie das Feld **Anzeigen nach** ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="35d02-112">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="35d02-113">Wenn Sie  **Periode** weder im Feld **Zeilenansicht** noch im Feld **Spaltenansicht** ausgewählt haben, dann geben Sie die entsprechende Periode im Feld **Datenfilter** ein.</span><span class="sxs-lookup"><span data-stu-id="35d02-113">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="35d02-114">In der Berechnung werden nur Finnanzbudgetposten mit den Filtercodes berücksichtigt, die Sie im Inforegister **Filter** eingeben.</span><span class="sxs-lookup"><span data-stu-id="35d02-114">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="35d02-115">Budgetposten mit anderen Filtercodes oder ohne Filtercodes werden nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="35d02-115">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="35d02-116">Solange der Filter auf der Seite verbleibt, zeigt das Budget nur die Budgetposten mit diesen Filtercodes an.</span><span class="sxs-lookup"><span data-stu-id="35d02-116">As long as the filter remains on the page, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="35d02-117">Ist eine Änderung des Budgets erforderlich, können Sie die einzelnen Budgetposten bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="35d02-117">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="35d02-118">Wählen Sie einen Betrag aus, um die zugrunde liegenden Finanzbudgetposten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="35d02-118">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="35d02-119">Aktuelle und budgetierte Beträge für alle Konten anzeigen:</span><span class="sxs-lookup"><span data-stu-id="35d02-119">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="35d02-120">Sie können Finanzbudgets anzeigen und sie mit tatsächlichen Werten in verschiedenen Bereichen von [!INCLUDE[d365fin](includes/d365fin_md.md)] vergleichen.</span><span class="sxs-lookup"><span data-stu-id="35d02-120">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="35d02-121">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="35d02-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="35d02-122">Auf der Seite **Kontenplan** wählen Sie die **Saldo/Budget** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="35d02-122">On the **Chart of Accounts** page, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="35d02-123">Auf der Seite oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="35d02-123">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="35d02-124">Um die Spezifikation eines angezeigten Betrags anzuzeigen, aktivieren Sie das Feld.</span><span class="sxs-lookup"><span data-stu-id="35d02-124">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="35d02-125">Die Filter, die Sie im Kopf auf der Seite setzen, werden sowohl auf die Fibuposten als auch auf die Budgetposten angewendet.</span><span class="sxs-lookup"><span data-stu-id="35d02-125">The filters you set on the page header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="35d02-126">Die Spalten auf der linken Seite enthalten den Kontenplan.</span><span class="sxs-lookup"><span data-stu-id="35d02-126">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="35d02-127">Von den fünf Spalten auf der rechten Seite enthalten die ersten vier aktuelle und budgetierte Soll- und Habenbeträge für jedes Konto.</span><span class="sxs-lookup"><span data-stu-id="35d02-127">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="35d02-128">Die fünfte Spalte zeigt die Relation zwischen den aktuellen und den budgetierten Beträgen des Sachkontos.</span><span class="sxs-lookup"><span data-stu-id="35d02-128">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="35d02-129">Wählen Sie auf der Seite **Saldo/Budget** mithilfe des Felds **Anzeigen nach** die gewünschte Periodenlänge aus.</span><span class="sxs-lookup"><span data-stu-id="35d02-129">Use the **View by** field on the **G/L Balance/Budget** page to select the period length.</span></span> <span data-ttu-id="35d02-130">Wählen Sie mithilfe des Felds **Anzeigen als** aus, wie die Beträge berechnet werden sollen (**Bewegung** oder **Saldo bis Datum**).</span><span class="sxs-lookup"><span data-stu-id="35d02-130">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="35d02-131">Klicken Sie auf der Registerkarte Aktionen auf **Vorperiode** oder F**olgeperiode**, um die Periode zu ändern.</span><span class="sxs-lookup"><span data-stu-id="35d02-131">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="35d02-132">Aktuelle und budgetierte Beträge für mehrere Perioden anzeigen:</span><span class="sxs-lookup"><span data-stu-id="35d02-132">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="35d02-133">Anstatt die aktuellen und budgetierten Beträge für alle Konten für eine einzige Periode einzusehen, können Sie eine Anzahl von Perioden für ein einziges Konto einsehen.</span><span class="sxs-lookup"><span data-stu-id="35d02-133">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="35d02-134">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="35d02-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="35d02-135">Auf der Seite **Kontenplan** wählen Sie das entsprechende Fibukonto aus, und wählen Sie die **Fibukontensaldo/Budget** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="35d02-135">On the **Chart of Accounts** page, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="35d02-136">Auf der Seite oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="35d02-136">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="35d02-137">Um die Spezifikation eines angezeigten Betrags anzuzeigen, aktivieren Sie das Feld.</span><span class="sxs-lookup"><span data-stu-id="35d02-137">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-related-training-at-microsoft-learnlearnmodulesbudgets-exchange-rates-dynamics-365-business-centralindex"></a><span data-ttu-id="35d02-138">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="35d02-138">See Related Training at [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="35d02-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35d02-139">See Also</span></span>
[<span data-ttu-id="35d02-140">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="35d02-140">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="35d02-141">Arbeiten mit Kontenschema</span><span class="sxs-lookup"><span data-stu-id="35d02-141">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
[<span data-ttu-id="35d02-142">Finanzen</span><span class="sxs-lookup"><span data-stu-id="35d02-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="35d02-143">Finanzen einrichten</span><span class="sxs-lookup"><span data-stu-id="35d02-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="35d02-144">Die Fibuposten und der Kontenplan</span><span class="sxs-lookup"><span data-stu-id="35d02-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="35d02-145">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="35d02-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
