---
title: "Einrichten von Internetfavoriten für Kontaktunternehmen| Microsoft Docs"
description: "Sie können Internet oder Internetfavoriten definieren und diese einem Kontaktunternehmen zuordnen, die Ihnen helfen, zu identifizieren, wie Sie nach Informationen über die Kontakte suchen möchten."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b80edfbbad575cfcaa15b2c1b79a4feacb077371
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="bb042-103">Einrichten von Internetfavoriten für Kontaktunternehmen</span><span class="sxs-lookup"><span data-stu-id="bb042-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="bb042-104">Sie können Ihren Kontakten Internetfavoriten (z. B. Suchmaschinen und Websites) zuordnen, um anzuzeigen, wo Sie im Internet nach Informationen über die Kontakte suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="bb042-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="bb042-105">Wenn Sie Internetfavoriten zuordnen, legen Sie fest, welche Suchmaschine und welchen Suchbegriff die Anwendung bei der Suche nach der gewünschten Information verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb042-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="bb042-106">Die Nutzung von Internetfavoriten zu Kontakten ist ein zwei Schritte umfassender Prozess.</span><span class="sxs-lookup"><span data-stu-id="bb042-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="bb042-107">Zuerst definieren Sie den Buchungsspurcode.</span><span class="sxs-lookup"><span data-stu-id="bb042-107">First, you define the web source code.</span></span> <span data-ttu-id="bb042-108">Sie müssen diesen Schritt nur einmal für jeden Internetfavoriten ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb042-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="bb042-109">Sobald Sie einen Buchungsspurcode haben, können Sie den Code zu den Kontaktpersonen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="bb042-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="bb042-110">um einen Internetfavoritencode zu definieren</span><span class="sxs-lookup"><span data-stu-id="bb042-110">To define a web source code</span></span>
1. <span data-ttu-id="bb042-111">Wählen Sie das Symbol ![Nach Seite oder Bericht](media/ui-search/search_small.png "Nach Seite oder Bericht suche") und geben **Internetquellen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="bb042-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="bb042-112">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="bb042-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="bb042-113">Füllen Sie die Felder **Code**, **Beschreibung** und **URL** aus.</span><span class="sxs-lookup"><span data-stu-id="bb042-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="bb042-114">Geben Sie %1 im Feld **URL** ein, um einen Platzhalter für einen Suchbegriff in der URL einzufügen.</span><span class="sxs-lookup"><span data-stu-id="bb042-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="bb042-115">Wenn Sie den Internetfavoriten von einer Kontaktkarte aus aktivieren, wird "%1" automatisch durch das Suchwort ersetzt (z. B. den Namen eines Unternehmens), das Sie in dem Fenster **Kontakt-Internetfavoriten** eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="bb042-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered in the **Contact Web Sources** window.</span></span>

<span data-ttu-id="bb042-116">Wiederholen Sie diese Schritte, um weitere Internetfavoriten einzurichten.</span><span class="sxs-lookup"><span data-stu-id="bb042-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="bb042-117">Um Internetfavoriten zu einem Kontaktunternehmen zuzuordnen</span><span class="sxs-lookup"><span data-stu-id="bb042-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="bb042-118">Wenn Sie Internetfavoriten zuordnen, legen Sie fest, welche Suchmaschine und welchen Suchbegriff die Anwendung bei der Suche nach der gewünschten Information verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb042-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="bb042-119">Öffnen Sie den Kontakt.</span><span class="sxs-lookup"><span data-stu-id="bb042-119">Open the contact.</span></span>
2. <span data-ttu-id="bb042-120">Wählen Sie die Aktion **Unternehmen** und dann die **Internetfavoriten**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="bb042-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="bb042-121">Das Fenster **Kontakt Internetfavoriten** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bb042-121">The **Contact Web Sources** window opens.</span></span>
3. <span data-ttu-id="bb042-122">Wählen Sie im Feld **Internetfavoritencode** den Internetfavoriten aus, den Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="bb042-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="bb042-123">Geben Sie im Feld **Suchbegriff** den Suchbegriff ein, der bei der Suche nach der Information verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb042-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="bb042-124">Wiederholen Sie diese Schritte, um weitere Internetfavoriten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="bb042-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="bb042-125">Ausserdem können Sie Internetfavoriten auf die gleiche Art in dem Fenster **Kontaktliste** zuordnen.</span><span class="sxs-lookup"><span data-stu-id="bb042-125">You can also assign web sources from the **Contact List** window by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb042-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb042-126">See Also</span></span>
[<span data-ttu-id="bb042-127">Kontaktunternehmenerstellen</span><span class="sxs-lookup"><span data-stu-id="bb042-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="bb042-128">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bb042-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

