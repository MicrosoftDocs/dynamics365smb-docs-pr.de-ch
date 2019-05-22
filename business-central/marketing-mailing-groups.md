---
title: Versandgruppen für Kontakte einrichten| Microsoft Docs
description: Einrichten von Verteilern zum Identifizieren von Kontaktgruppen, denen die gleichen Informationen zugehen sollen, z. B. Marketingkampagnen oder Promotionen.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: fb9c540819279d042685ad69c790e36e71dcfbed
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238293"
---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="dd29b-103">Einrichten von Verteilern für Kontakte</span><span class="sxs-lookup"><span data-stu-id="dd29b-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="dd29b-104">Verteiler werden verwendet, um Kontaktgruppen zu identifizieren, die dieselben Informationen erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="dd29b-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="dd29b-105">Sie können z. B. einen Verteiler für die Kontakte erstellen, denen Sie eine Benachrichtigung über einen Büroumzug schicken möchten.</span><span class="sxs-lookup"><span data-stu-id="dd29b-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="dd29b-106">Die Nutzung von Verteilern zu Kontakten ist ein zwei Schritte umfassender Prozess.</span><span class="sxs-lookup"><span data-stu-id="dd29b-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="dd29b-107">Zuerst definieren Sie den Verteilercode.</span><span class="sxs-lookup"><span data-stu-id="dd29b-107">First, you define the mailing group code.</span></span> <span data-ttu-id="dd29b-108">Sie müssen diesen Schritt nur einmal für jeden Verteiler ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd29b-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="dd29b-109">Sobald Sie einen Verteilercode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="dd29b-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="dd29b-110">Definieren eines Verteilercodes</span><span class="sxs-lookup"><span data-stu-id="dd29b-110">To define mailing group codes</span></span>
<span data-ttu-id="dd29b-111">Der Verteilercode definiert die Art oder die Kategorie der Gruppe, z. B. UMZUG für einen Büroumzug, oder GESCHENK für ein Geburtstagsgeschenk.</span><span class="sxs-lookup"><span data-stu-id="dd29b-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="dd29b-112">Sie können mehrere Branchencodes haben.</span><span class="sxs-lookup"><span data-stu-id="dd29b-112">You can have several industry group codes.</span></span> <span data-ttu-id="dd29b-113">Um die Branchen zu definieren, verwenden Sie die **Verteiler**-Seite.</span><span class="sxs-lookup"><span data-stu-id="dd29b-113">To define the industry groups, you use the **Mailing Groups** page.</span></span>

1. <span data-ttu-id="dd29b-114">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Versandgruppen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="dd29b-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="dd29b-115">Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="dd29b-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="dd29b-116">Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.</span><span class="sxs-lookup"><span data-stu-id="dd29b-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="dd29b-117"><a name="AssignMailGroupContact">Um einem Kontakt einen Verteiler zuzuordnen:</a></span><span class="sxs-lookup"><span data-stu-id="dd29b-117"><a name="AssignMailGroupContact"></a> To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="dd29b-118">Öffnen Sie den Kontakt.</span><span class="sxs-lookup"><span data-stu-id="dd29b-118">Open the contact.</span></span>
2. <span data-ttu-id="dd29b-119">Wählen Sie die **Verteiler**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="dd29b-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="dd29b-120">Die Seite **Kontakt Verteiler** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="dd29b-120">The **Contact Mailing Groups** page opens.</span></span>
3. <span data-ttu-id="dd29b-121">Wählen Sie im Feld **Verteilercode** den Verteiler aus, den Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="dd29b-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="dd29b-122">Wiederholen Sie diese Schritte, um beliebig viele Verteiler einzurichten.</span><span class="sxs-lookup"><span data-stu-id="dd29b-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="dd29b-123">Außerdem können Sie Verteiler auf die gleiche Art in dem Fenster Kontaktliste zuordnen.</span><span class="sxs-lookup"><span data-stu-id="dd29b-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="dd29b-124">Die Anzahl der dem Kontakt zugeordneten Verteiler wird im Feld **Anzahl Verteiler** im Abschnitt **Segmentierung** auf der Seite **Kontakt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd29b-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="dd29b-125">Sobald Sie Ihren Kontakten Verteiler zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="dd29b-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="dd29b-126">Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="dd29b-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="dd29b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd29b-127">See Also</span></span>
[<span data-ttu-id="dd29b-128">Kontakte erstellen</span><span class="sxs-lookup"><span data-stu-id="dd29b-128">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="dd29b-129">Arbeiten mit Business Central</span><span class="sxs-lookup"><span data-stu-id="dd29b-129">Working with Business Central</span></span>](ui-work-product.md)
