---
title: "Versandgruppen für Kontakte einrichten| Microsoft Docs"
description: Einrichten von Verteilern zum Identifizieren von Kontaktgruppen, denen die gleichen Informationen zugehen sollen, z. B. Marketingkampagnen oder Promotionen.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bc1c89b87426b72ce4f9522cb7f0dc31c77acad1
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-mailing-groups-for-contacts"></a><span data-ttu-id="a30fd-103">Vorgehensweise: Einrichten von Verteilern für Kontakte</span><span class="sxs-lookup"><span data-stu-id="a30fd-103">How to: Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="a30fd-104">Verteiler werden verwendet, um Kontaktgruppen zu identifizieren, die dieselben Informationen erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="a30fd-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="a30fd-105">Sie können z. B. einen Verteiler für die Kontakte erstellen, denen Sie eine Benachrichtigung über einen Büroumzug schicken möchten.</span><span class="sxs-lookup"><span data-stu-id="a30fd-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="a30fd-106">Die Nutzung von Verteilern zu Kontakten ist ein zwei Schritte umfassender Prozess.</span><span class="sxs-lookup"><span data-stu-id="a30fd-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="a30fd-107">Zuerst definieren Sie den Verteilercode.</span><span class="sxs-lookup"><span data-stu-id="a30fd-107">First, you define the mailing group code.</span></span> <span data-ttu-id="a30fd-108">Sie müssen diesen Schritt nur einmal für jeden Verteiler ausführen.</span><span class="sxs-lookup"><span data-stu-id="a30fd-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="a30fd-109">Sobald Sie einen Verteilercode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a30fd-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="a30fd-110">Definieren eines Verteilercodes</span><span class="sxs-lookup"><span data-stu-id="a30fd-110">To define mailing group codes</span></span>
<span data-ttu-id="a30fd-111">Der Verteilercode definiert die Art oder die Kategorie der Gruppe, z. B. UMZUG für einen Büroumzug, oder GESCHENK für ein Geburtstagsgeschenk.</span><span class="sxs-lookup"><span data-stu-id="a30fd-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="a30fd-112">Sie können mehrere Branchencodes haben.</span><span class="sxs-lookup"><span data-stu-id="a30fd-112">You can have several industry group codes.</span></span> <span data-ttu-id="a30fd-113">Um die Branchen zu definieren, verwenden Sie das **Verteiler**-Fenster.</span><span class="sxs-lookup"><span data-stu-id="a30fd-113">To define the industry groups, you use the **Mailing Groups** window.</span></span>

1. <span data-ttu-id="a30fd-114">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Versandgruppen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="a30fd-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="a30fd-115">Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="a30fd-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="a30fd-116">Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.</span><span class="sxs-lookup"><span data-stu-id="a30fd-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="a30fd-117"><a name="AssignMailGroupContact">Um einem Kontakt einen Verteiler zuzuordnen:</a></span><span class="sxs-lookup"><span data-stu-id="a30fd-117"><a name="AssignMailGroupContact"></a> To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="a30fd-118">Öffnen Sie den Kontakt.</span><span class="sxs-lookup"><span data-stu-id="a30fd-118">Open the contact.</span></span>
2. <span data-ttu-id="a30fd-119">Wählen Sie die **Verteiler**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="a30fd-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="a30fd-120">Das Fenster **Kontakt Verteiler** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a30fd-120">The **Contact Mailing Groups** window opens.</span></span>
3. <span data-ttu-id="a30fd-121">Wählen Sie im Feld **Verteilercode** den Verteiler aus, den Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="a30fd-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="a30fd-122">Wiederholen Sie diese Schritte, um beliebig viele Verteiler einzurichten.</span><span class="sxs-lookup"><span data-stu-id="a30fd-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="a30fd-123">Außerdem können Sie Verteiler auf die gleiche Art in dem Fenster Kontaktliste zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a30fd-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="a30fd-124">Die Anzahl der dem Kontakt zugeordneten Verteiler wird im Feld **Anzahl Verteiler** im Abschnitt **Segmentierung** im Fenster **Kontakt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a30fd-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="a30fd-125">Sobald Sie Ihren Kontakten Verteiler zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a30fd-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="a30fd-126">Weitere Informationen finden Sie unter [Vorgehensweise: Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="a30fd-126">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a30fd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a30fd-127">See Also</span></span>
[<span data-ttu-id="a30fd-128">Kontaktunternehmenerstellen</span><span class="sxs-lookup"><span data-stu-id="a30fd-128">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="a30fd-129">Kontaktpersonen erstellen</span><span class="sxs-lookup"><span data-stu-id="a30fd-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="a30fd-130">Arbeiten mit Financials</span><span class="sxs-lookup"><span data-stu-id="a30fd-130">Working with Financials</span></span>](ui-work-product.md)

