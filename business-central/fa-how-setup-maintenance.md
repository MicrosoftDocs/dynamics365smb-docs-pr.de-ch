---
title: Abschreibungsverwaltung einrichten| Microsoft Docs
description: "Um Anlagenreparaturen und -Dienst zu verwalten, geben Sie allgemeine Wartungsinformationen, Codes für die Art der Arbeit und eine Buchung für Kosten an."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: aef3d672bf01425a36bdd599e18d9ee9dac73b2d
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="e6f4c-103">Um Anlagenwartung einzurichten:</span><span class="sxs-lookup"><span data-stu-id="e6f4c-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="e6f4c-104">Um die Anlagenwartung zu verwalten, müssen Sie erst einige allgemeine Wartungsinformationen einrichten, ein Buchungskonto für Wartungskosten und Wartungscodes für die Arten von Arbeit, beispielsweise Instandhaltung oder Reparatur.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="e6f4c-105">So richten Sie allgemeine Wartungsinformationen ein:</span><span class="sxs-lookup"><span data-stu-id="e6f4c-105">To set up general maintenance information</span></span>
<span data-ttu-id="e6f4c-106">Wenn Sie die Felder für Wartung eingerichtet haben, können Sie Wartungsausgaben aus einem Erf.-Journal buchen.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="e6f4c-107">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Anlagen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="e6f4c-108">Wählen Sie die Anlage, für die Sie den Versicherungsposten festlegen wollen, und wählen die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="e6f4c-109">Füllen Sie auf dem Inforegister **Wartung** die notwendigen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="e6f4c-110">So richten Sie Wartungscodes ein</span><span class="sxs-lookup"><span data-stu-id="e6f4c-110">To set up maintenance codes</span></span>
<span data-ttu-id="e6f4c-111">Wenn Sie Wartungskosten aus einem Fibu Buch.-Blatt buchen, füllen Sie das Feld **Wartungscode** aus. So erfassen Sie, welche Art von Wartung durchgeführt wurde, beispielsweise Instandhaltung oder Reparatur.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="e6f4c-112">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verwaltung** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="e6f4c-113">Legen Sie im Fenster **Wartung** Codes für unterschiedliche Arten von Wartungsarbeiten fest.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-113">In the **Maintenance** window, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="e6f4c-114">So richten Sie Aufwandskonten für die Wartung ein</span><span class="sxs-lookup"><span data-stu-id="e6f4c-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="e6f4c-115">Um Wartungskosten zu buchen, müssen Sie erst eine Kontonummer im Fenster **Anlagenbuchungsgruppen** eingeben.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-115">To post maintenance costs, you must first enter an account number in the **FA Posting Groups** window.</span></span>

1. <span data-ttu-id="e6f4c-116">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Auftragsbuchungsruppen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="e6f4c-117">Füllen Sie das Feld **Aufwandskto. Wartung** für jede einzelne Buchungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e6f4c-118">Um festzulegen, ob Wartungskosten auf Kostenstellen und/oder Kostenträger verteilt werden, müssen Sie einen Verteilungsschlüssel einrichten.</span><span class="sxs-lookup"><span data-stu-id="e6f4c-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="e6f4c-119">Weitere Informationen finden Sie unter [Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="e6f4c-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e6f4c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6f4c-120">See Also</span></span>
[<span data-ttu-id="e6f4c-121">Anlagen einrichten</span><span class="sxs-lookup"><span data-stu-id="e6f4c-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="e6f4c-122">Anlagen</span><span class="sxs-lookup"><span data-stu-id="e6f4c-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="e6f4c-123">Finanzen</span><span class="sxs-lookup"><span data-stu-id="e6f4c-123">Finance</span></span>](finance.md)  
[<span data-ttu-id="e6f4c-124">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="e6f4c-124">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="e6f4c-125">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e6f4c-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

