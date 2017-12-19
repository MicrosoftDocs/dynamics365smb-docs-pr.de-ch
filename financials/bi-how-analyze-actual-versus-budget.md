---
title: Analysieren von Actuals vs. Budget | Microsoft Docs
description: "Beschreibt, wie die tatsächlichen Beträge mit den budgetierten Beträgen analysiert werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 12/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: cfe0eed4090ef458e774da8d0bc03910247570d7
ms.openlocfilehash: e76d590476b1236bf1d82a7f5e4f502ffdd9d02d
ms.contentlocale: de-ch
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="26bd1-103">Beschreibt, wie die tatsächlichen Beträge mit den budgetierten Beträgen analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="26bd1-103">How to: Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="26bd1-104">Als Teil des Zusammentragen, Analysieren und Teilen der Firmendaten sehen Sie aktuelle Beträge verglichen mit den budgetierten Beträgen für alle Konten sowie für mehrere Perioden.</span><span class="sxs-lookup"><span data-stu-id="26bd1-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="26bd1-105">Um budgetierte Beträge zu analysieren, müssen Sie zunächst Sachkonto-Budgets erstellen.</span><span class="sxs-lookup"><span data-stu-id="26bd1-105">To analyze budgeted amounts, you must first create G(L budgets.</span></span> <span data-ttu-id="26bd1-106">Weitere Informationen finden Sie unter [Gewusst wie: Sachkonto-Budgets erstellen](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="26bd1-106">For more information, see [How to: Create G/L Budgets](finance-how-create-budgets.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="26bd1-107">Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="26bd1-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="26bd1-108">Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.</span><span class="sxs-lookup"><span data-stu-id="26bd1-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-view-a-gl-budget"></a><span data-ttu-id="26bd1-109">Einsehen eines Sachkonto-Budgets</span><span class="sxs-lookup"><span data-stu-id="26bd1-109">To view a G/L budget</span></span>
<span data-ttu-id="26bd1-110">In einem Budget mit Dimensionen können Sie die Posten filtern und somit bestimmte Budgets einsehen.</span><span class="sxs-lookup"><span data-stu-id="26bd1-110">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="26bd1-111">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen] Symbol (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **G/L-Blatt Budgets** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="26bd1-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="26bd1-112">Öffnen Sie im Fenster **G/L Budgets** das Budget, das Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="26bd1-112">In the **G/L Budgets** window, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="26bd1-113">Im Fenster oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="26bd1-113">At the top of the window, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="26bd1-114">Wenn Sie **Periode** entweder im Feld **Als Zeile anzeigen** oder im Feld **Als Spalte anzeigen** ausgewählt haben, müssen Sie das Feld **Anzeigen nach** ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="26bd1-114">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="26bd1-115">Wenn Sie  **Periode** weder im Feld **Zeilenansicht** noch im Feld **Spaltenansicht** ausgewählt haben, dann geben Sie die entsprechende Periode im Feld **Datenfilter** ein.</span><span class="sxs-lookup"><span data-stu-id="26bd1-115">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="26bd1-116">In der Berechnung werden nur Finnanzbudgetposten mit den Filtercodes berücksichtigt, die Sie im Inforegister **Filter** eingeben.</span><span class="sxs-lookup"><span data-stu-id="26bd1-116">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="26bd1-117">Budgetposten mit anderen Filtercodes oder ohne Filtercodes werden nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="26bd1-117">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="26bd1-118">Solange der Filter im Fenster verbleibt, zeigt das Budget nur die Budgetposten mit diesen Filtercodes an.</span><span class="sxs-lookup"><span data-stu-id="26bd1-118">As long as the filter remains on the window, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="26bd1-119">Ist eine Änderung des Budgets erforderlich, können Sie die einzelnen Budgetposten bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="26bd1-119">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="26bd1-120">Wählen Sie einen Betrag aus, um die zugrunde liegenden Finanzbudgetposten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="26bd1-120">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="26bd1-121">Aktuelle und budgetierte Beträge für alle Konten anzeigen:</span><span class="sxs-lookup"><span data-stu-id="26bd1-121">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="26bd1-122">Sie können Finanzbudgets anzeigen und sie mit tatsächlichen Werten in verschiedenen Bereichen von [!INCLUDE[d365fin](includes/d365fin_md.md)] vergleichen.</span><span class="sxs-lookup"><span data-stu-id="26bd1-122">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="26bd1-123">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben **Kontenplan** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="26bd1-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="26bd1-124">Im Fenster **Kontenplan** wählen Sie die **Saldo/Budget** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="26bd1-124">In the **Chart of Accounts** window, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="26bd1-125">Im Fenster oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="26bd1-125">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="26bd1-126">Um die Spezifikation eines angezeigten Betrags anzuzeigen, aktivieren Sie das Feld.</span><span class="sxs-lookup"><span data-stu-id="26bd1-126">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="26bd1-127">Die Filter, die Sie im Kopf des Fensters setzen, werden sowohl auf die Sachposten als auch auf die Budgetposten angewendet.</span><span class="sxs-lookup"><span data-stu-id="26bd1-127">The filters you set in the window header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="26bd1-128">Die Spalten auf der linken Seite enthalten den Kontenplan.</span><span class="sxs-lookup"><span data-stu-id="26bd1-128">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="26bd1-129">Von den fünf Spalten auf der rechten Seite enthalten die ersten vier aktuelle und budgetierte Soll- und Habenbeträge für jedes Konto.</span><span class="sxs-lookup"><span data-stu-id="26bd1-129">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="26bd1-130">Die fünfte Spalte zeigt die Relation zwischen den aktuellen und den budgetierten Beträgen des Sachkontos.</span><span class="sxs-lookup"><span data-stu-id="26bd1-130">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="26bd1-131">Wählen Sie im Fenster **Saldo/Budget** mithilfe des Felds **Anzeigen nach** die gewünschte Periodenlänge aus.</span><span class="sxs-lookup"><span data-stu-id="26bd1-131">Use the **View by** field in the **G/L Balance/Budget** window to select the period length.</span></span> <span data-ttu-id="26bd1-132">Wählen Sie mithilfe des Felds **Anzeigen als** aus, wie die Beträge berechnet werden sollen (**Bewegung** oder **Saldo bis Datum**).</span><span class="sxs-lookup"><span data-stu-id="26bd1-132">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="26bd1-133">Klicken Sie auf der Registerkarte Aktionen auf **Vorperiode** oder F**olgeperiode**, um die Periode zu ändern.</span><span class="sxs-lookup"><span data-stu-id="26bd1-133">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="26bd1-134">Aktuelle und budgetierte Beträge für mehrere Perioden anzeigen:</span><span class="sxs-lookup"><span data-stu-id="26bd1-134">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="26bd1-135">Anstatt die aktuellen und budgetierten Beträge für alle Konten für eine einzige Periode einzusehen, können Sie eine Anzahl von Perioden für ein einziges Konto einsehen.</span><span class="sxs-lookup"><span data-stu-id="26bd1-135">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="26bd1-136">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben **Kontenplan** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="26bd1-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="26bd1-137">Im Fenster **Kontenplan** wählen Sie das entsprechende Sachkonto aus, und wählen Sie die **Sachkontensaldo/Budget** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="26bd1-137">In the **Chart of Accounts** window, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="26bd1-138">Im Fenster oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="26bd1-138">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="26bd1-139">Um die Spezifikation eines angezeigten Betrags anzuzeigen, aktivieren Sie das Feld.</span><span class="sxs-lookup"><span data-stu-id="26bd1-139">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="26bd1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26bd1-140">See Also</span></span>
[<span data-ttu-id="26bd1-141">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="26bd1-141">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="26bd1-142">Vorgehensweise: Arbeiten mit Kontenschemata</span><span class="sxs-lookup"><span data-stu-id="26bd1-142">How to: Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
[<span data-ttu-id="26bd1-143">Finanzen</span><span class="sxs-lookup"><span data-stu-id="26bd1-143">Finance</span></span>](finance.md)  
[<span data-ttu-id="26bd1-144">Finance einrichten</span><span class="sxs-lookup"><span data-stu-id="26bd1-144">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="26bd1-145">Die Finanzbuchhaltung und der Kontenplan</span><span class="sxs-lookup"><span data-stu-id="26bd1-145">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="26bd1-146">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26bd1-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

