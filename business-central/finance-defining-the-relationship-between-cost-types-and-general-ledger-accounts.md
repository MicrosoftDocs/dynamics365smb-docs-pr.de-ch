---
title: Definieren der Beziehung zwischen Kostenarten und Fibukonten | Microsoft Docs
description: Lernen, wie die beiden Felder definiert werden, die die Beziehung zwischen Kostenart und Fibukonto festlegen
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: c5b4549e330bd9b3369b6fe5b18361f6662291c9
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "918044"
---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a><span data-ttu-id="3e64c-103">Definieren der Beziehung zwischen Kostenarten und Sachkonten</span><span class="sxs-lookup"><span data-stu-id="3e64c-103">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>
<span data-ttu-id="3e64c-104">Das Verbindung zwischen der Kostenart und dem Fibukonto wird in der Kostenart und im Fibukonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="3e64c-104">The relationship between the cost type and the general ledger account is created in the cost type and in the general ledger account.</span></span>  

* <span data-ttu-id="3e64c-105">Das Feld **Fibukontenbereich** in der Tabelle **Kostenart** bestimmt, welche Fibukonten zu einer Kostenart gehören.</span><span class="sxs-lookup"><span data-stu-id="3e64c-105">The **G/L Account Range** field in the **Cost Type** table establishes which general ledger accounts belong to a cost type.</span></span>  
* <span data-ttu-id="3e64c-106">Das **Kostenartennummer**</span><span class="sxs-lookup"><span data-stu-id="3e64c-106">The **Cost Type No.**</span></span> <span data-ttu-id="3e64c-107">Feld im Kontenplan bestimmt, zu welcher Kostenart ein Fibukonto gehört.</span><span class="sxs-lookup"><span data-stu-id="3e64c-107">field in the chart of accounts establishes which cost type a general ledger account belongs to.</span></span>  

<span data-ttu-id="3e64c-108">Diese beiden Felder werden automatisch ausgefüllt, wenn Sie die **Kostenarten aus Kontenplan abrufen**-Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e64c-108">These two fields are filled automatically when you use the **Get Cost Types from Chart of Accounts** function.</span></span>  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a><span data-ttu-id="3e64c-109">Beziehung zwischen Fibukonten und Kostenarten</span><span class="sxs-lookup"><span data-stu-id="3e64c-109">Relationship Between General Ledger Accounts and Cost Types</span></span>  
<span data-ttu-id="3e64c-110">Zwischen Fibukonten und Kostenarten besteht eine n:1-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="3e64c-110">There is an n:1 relationship between general ledger accounts and cost types.</span></span> <span data-ttu-id="3e64c-111">Mehrere Fibukonten können zu einer Kostenart gehören, aber jedes Fibukonto gehört nur zu einer Kostenart.</span><span class="sxs-lookup"><span data-stu-id="3e64c-111">Several general ledger accounts can belong to one cost type, but each general ledger account belongs to only one cost type.</span></span> <span data-ttu-id="3e64c-112">In der folgenden Tabelle werden die Details der Beziehung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3e64c-112">The following table describes the details in the relationship.</span></span>  

|<span data-ttu-id="3e64c-113">Verbindungen</span><span class="sxs-lookup"><span data-stu-id="3e64c-113">Relationship</span></span>|<span data-ttu-id="3e64c-114">**Fibukontobereich**</span><span class="sxs-lookup"><span data-stu-id="3e64c-114">**G/L Account Range**</span></span>|<span data-ttu-id="3e64c-115">**Kostenartnr.**</span><span class="sxs-lookup"><span data-stu-id="3e64c-115">**Cost Type No.**</span></span>|  
|------------------|------------------------------------------------|-------------------------------------------|  
|<span data-ttu-id="3e64c-116">Ein Fibukonto für jede Kostenart</span><span class="sxs-lookup"><span data-stu-id="3e64c-116">One general ledger account for each cost type</span></span>|<span data-ttu-id="3e64c-117">Ein Fibukonto</span><span class="sxs-lookup"><span data-stu-id="3e64c-117">One general ledger account</span></span>|<span data-ttu-id="3e64c-118">Eine Kostenart</span><span class="sxs-lookup"><span data-stu-id="3e64c-118">One cost type</span></span>|  
|<span data-ttu-id="3e64c-119">Mehrere Fibukonten für eine Kostenart</span><span class="sxs-lookup"><span data-stu-id="3e64c-119">Several general ledger accounts for one cost type</span></span>|<span data-ttu-id="3e64c-120">Fibukontobereich, z. B. 7110 ... 7193 für jedes Fibukonto</span><span class="sxs-lookup"><span data-stu-id="3e64c-120">General ledger account range, for example, 7110..7193 for each general ledger account</span></span>|<span data-ttu-id="3e64c-121">Für jedes Fibukonto im Bereich gibt es nur eine Kostenart</span><span class="sxs-lookup"><span data-stu-id="3e64c-121">For each general ledger account in the range, there is only one cost type</span></span>|  
|<span data-ttu-id="3e64c-122">Kostenarten ohne entsprechende Fibukonten</span><span class="sxs-lookup"><span data-stu-id="3e64c-122">Cost types without corresponding general ledger accounts</span></span>|<Empty>||  
|<span data-ttu-id="3e64c-123">Fibukonten, deren Posten nicht übertragen werden</span><span class="sxs-lookup"><span data-stu-id="3e64c-123">General ledger accounts whose entries will not be transferred</span></span>||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a><span data-ttu-id="3e64c-124">Kostenarten ohne Beziehung zum Fibukonto</span><span class="sxs-lookup"><span data-stu-id="3e64c-124">Cost Types Without a Relationship to the General Ledger</span></span>  
<span data-ttu-id="3e64c-125">Eine Kostenart hat möglicherweise keine Beziehung zu Fibukonten, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3e64c-125">A cost type may not have a relationship to general ledger accounts if one of the following conditions is true:</span></span>  

* <span data-ttu-id="3e64c-126">Konten für die betriebliche Buchhaltung, wie Berech. Zinsen und Abschreibungen, entnehmen nur Kosten aus der betrieblichen Buchhaltung.</span><span class="sxs-lookup"><span data-stu-id="3e64c-126">Accounts for operational accounting, such as Calc. Interest and Depreciation, only take costs from the operational accounting.</span></span>  
* <span data-ttu-id="3e64c-127">Helfende Kostenarten, wie Kostenarten 9901, 9902 und 9903 in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank, werden als Haben- und Sollbeträge für Zuordnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e64c-127">Helping cost types, such as cost types 9901, 9902, and 9903 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, are used as credit and debit accounts for allocations.</span></span>  
* <span data-ttu-id="3e64c-128">Das helfende Konto, 9920 in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank, enthält tatsächliche Zugänge, die die Differenz zwischen Kosten und Ausgaben des Fibukontos anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3e64c-128">The helping account, 9920 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, contains actual accruals that show the difference between costs and the expense from the general ledger.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3e64c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e64c-129">See Also</span></span>  
[<span data-ttu-id="3e64c-130">Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="3e64c-130">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="3e64c-131">[Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="3e64c-131">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
[<span data-ttu-id="3e64c-132">Informationen zur Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="3e64c-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="3e64c-133">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3e64c-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
