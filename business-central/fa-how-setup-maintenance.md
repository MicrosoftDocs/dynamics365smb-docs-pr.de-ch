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
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: b730e880a3cf9f2ba3a2abaa25a1b80848f52e97
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="f6064-103">Um Anlagenwartung einzurichten:</span><span class="sxs-lookup"><span data-stu-id="f6064-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="f6064-104">Um die Anlagenwartung zu verwalten, müssen Sie erst einige allgemeine Wartungsinformationen einrichten, ein Buchungskonto für Wartungskosten und Wartungscodes für die Arten von Arbeit, beispielsweise Instandhaltung oder Reparatur.</span><span class="sxs-lookup"><span data-stu-id="f6064-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="f6064-105">So richten Sie allgemeine Wartungsinformationen ein:</span><span class="sxs-lookup"><span data-stu-id="f6064-105">To set up general maintenance information</span></span>
<span data-ttu-id="f6064-106">Wenn Sie die Felder für Wartung eingerichtet haben, können Sie Wartungsausgaben aus einem Erf.-Journal buchen.</span><span class="sxs-lookup"><span data-stu-id="f6064-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="f6064-107">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f6064-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="f6064-108">Wählen Sie die Anlage, für die Sie den Versicherungsposten festlegen wollen, und wählen die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="f6064-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="f6064-109">Füllen Sie auf dem Inforegister **Wartung** die notwendigen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="f6064-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="f6064-110">So richten Sie Wartungscodes ein</span><span class="sxs-lookup"><span data-stu-id="f6064-110">To set up maintenance codes</span></span>
<span data-ttu-id="f6064-111">Wenn Sie Wartungskosten aus einem Fibu Buch.-Blatt buchen, füllen Sie das Feld **Wartungscode** aus. So erfassen Sie, welche Art von Wartung durchgeführt wurde, beispielsweise Instandhaltung oder Reparatur.</span><span class="sxs-lookup"><span data-stu-id="f6064-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="f6064-112">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Wartung** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f6064-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="f6064-113">Legen Sie im Fenster **Wartung** Codes für unterschiedliche Arten von Wartungsarbeiten fest.</span><span class="sxs-lookup"><span data-stu-id="f6064-113">In the **Maintenance** window, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="f6064-114">So richten Sie Aufwandskonten für die Wartung ein</span><span class="sxs-lookup"><span data-stu-id="f6064-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="f6064-115">Um Wartungskosten zu buchen, müssen Sie erst eine Kontonummer im Fenster **Anlagenbuchungsgruppen** eingeben.</span><span class="sxs-lookup"><span data-stu-id="f6064-115">To post maintenance costs, you must first enter an account number in the **FA Posting Groups** window.</span></span>

1. <span data-ttu-id="f6064-116">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen-Buchungsgruppe** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f6064-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="f6064-117">Füllen Sie das Feld **Aufwandskto. Wartung** für jede einzelne Buchungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="f6064-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f6064-118">Um festzulegen, ob Wartungskosten auf Kostenstellen und/oder Kostenträger verteilt werden, müssen Sie einen Verteilungsschlüssel einrichten.</span><span class="sxs-lookup"><span data-stu-id="f6064-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="f6064-119">Weitere Informationen finden Sie unter [Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="f6064-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f6064-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6064-120">See Also</span></span>
[<span data-ttu-id="f6064-121">Anlagen einrichten</span><span class="sxs-lookup"><span data-stu-id="f6064-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="f6064-122">Anlagen</span><span class="sxs-lookup"><span data-stu-id="f6064-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="f6064-123">Finanzen</span><span class="sxs-lookup"><span data-stu-id="f6064-123">Finance</span></span>](finance.md)  
[<span data-ttu-id="f6064-124">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="f6064-124">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="f6064-125">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f6064-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

