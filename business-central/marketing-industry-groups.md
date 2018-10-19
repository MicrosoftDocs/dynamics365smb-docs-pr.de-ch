---
title: "Einrichten von Branchengruppen für Kontaktunternehmen| Microsoft Docs"
description: Beschreibt, wie eine Branche definiert und diese einem Kontaktunternehmen, beispielsweise Einzelhandelsbranche, oder der Automobilindustrie zuweist.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f1927938bc7e882902d8f609242c529e0ba29cd1
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-industry-groups-for-contact-companies"></a><span data-ttu-id="308cd-103">Einrichten von Branchen für Kontaktunternehmen</span><span class="sxs-lookup"><span data-stu-id="308cd-103">Set Up Industry Groups for Contact Companies</span></span>
<span data-ttu-id="308cd-104">Branchen werden verwendet, um die Branche anzugeben, zu der Ihre Kontakte gehören z. B. die Einzelhandelsbranche und die Automobilbranche.</span><span class="sxs-lookup"><span data-stu-id="308cd-104">You use industry groups to indicate the type of industry to which your contacts belong, for example, the retail industry or the automobile industry.</span></span>

<span data-ttu-id="308cd-105">Die Nutzung von Branchen zu Kontakten ist ein zwei Schritte umfassender Prozess.</span><span class="sxs-lookup"><span data-stu-id="308cd-105">Using industry groups on contacts is a two-step process.</span></span> <span data-ttu-id="308cd-106">Zuerst definieren Sie den Branchenscode.</span><span class="sxs-lookup"><span data-stu-id="308cd-106">First, you define the industry group code.</span></span> <span data-ttu-id="308cd-107">Sie müssen diesen Schritt nur einmal für jede Branche ausführen.</span><span class="sxs-lookup"><span data-stu-id="308cd-107">You only have to perform this step one time for each industry group.</span></span> <span data-ttu-id="308cd-108">Sobald Sie einen Branchencode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="308cd-108">Once you have an industry group code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="308cd-109">Wenn Sie planen, Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten in anderen Teilen der Anwendung zu synchronisieren, können Sie für sie eine Geschäftsbeziehung erstellen.</span><span class="sxs-lookup"><span data-stu-id="308cd-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-an-industry-group-code"></a><span data-ttu-id="308cd-110">Branchengruppencode definieren</span><span class="sxs-lookup"><span data-stu-id="308cd-110">To define an industry group code</span></span>
<span data-ttu-id="308cd-111">Der Branchencode definiert die Art oder die Kategorie der Gruppe, z. B. WERBUNG für Werbung oder PRESSE für TV und Radio.</span><span class="sxs-lookup"><span data-stu-id="308cd-111">The industry group code defines the type or category of the group, such as ADVERT for advertising, or PRESS, for TV and radio.</span></span> <span data-ttu-id="308cd-112">Sie können mehrere Branchencodes haben.</span><span class="sxs-lookup"><span data-stu-id="308cd-112">You can have several industry group codes.</span></span> <span data-ttu-id="308cd-113">Um die Branchen zu definieren, verwenden Sie das **Branchen**-Fenster.</span><span class="sxs-lookup"><span data-stu-id="308cd-113">To define the industry groups, you use the **Industry Groups** window.</span></span>

1. <span data-ttu-id="308cd-114">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Branchengruppen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="308cd-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Industry Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="308cd-115">Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="308cd-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="308cd-116">Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.</span><span class="sxs-lookup"><span data-stu-id="308cd-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="308cd-117"><a name="AssignIndustryGroupContact">Um einem Kontakt eine Branche zuzuordnen:</a></span><span class="sxs-lookup"><span data-stu-id="308cd-117"><a name="AssignIndustryGroupContact"></a> To assign industry groups to a contact</span></span>
<span data-ttu-id="308cd-118">Sie können Branchen nicht zu Personen zuordnen – nur zu Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="308cd-118">You cannot assign industry groups to a contact person - only companies.</span></span>

1. <span data-ttu-id="308cd-119">Öffnen Sie den Kontakt.</span><span class="sxs-lookup"><span data-stu-id="308cd-119">Open the contact.</span></span>
2. <span data-ttu-id="308cd-120">Wählen Sie die Aktion **Unternehmen** und dann die **Branchen**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="308cd-120">Choose the **Company** action, and then the **Industry Groups** action.</span></span> <span data-ttu-id="308cd-121">Das Fenster **Kontakt Branchen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="308cd-121">The **Contact Industry Groups** window opens.</span></span>
3. <span data-ttu-id="308cd-122">Wählen Sie im Feld **Branchencode** die Branchen aus, die Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="308cd-122">In the **Industry Groups Code** field, select the industry groups you want to assign.</span></span>

<span data-ttu-id="308cd-123">Wiederholen Sie diese Schritte, um beliebig viele Branchen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="308cd-123">Repeat these steps to assign as many industry groups as you want.</span></span> <span data-ttu-id="308cd-124">Sie können in dem Fenster Kontaktliste ebenfalls Branchen zuordnen, indem Sie denselben Schritten folgen.</span><span class="sxs-lookup"><span data-stu-id="308cd-124">You can also assign industry groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="308cd-125">Die Anzahl der Branchen, die Sie dem Kontakt zugeordnet haben, wird im Feld **Anzahl Branchen** im Inforegister **Segmentierung** im Fenster **Kontakt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="308cd-125">The number of industry groups that you have assigned to the contact is displayed in the **No. of Industry Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="308cd-126">Nachdem Sie Ihren Kontakten Branchen zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="308cd-126">After you have assigned industry groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="308cd-127">Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="308cd-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="308cd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="308cd-128">See Also</span></span>
[<span data-ttu-id="308cd-129">Kontaktunternehmenerstellen</span><span class="sxs-lookup"><span data-stu-id="308cd-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="308cd-130">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="308cd-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

