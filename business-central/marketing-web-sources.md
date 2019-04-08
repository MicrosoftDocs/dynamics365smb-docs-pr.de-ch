---
title: Einrichten von Internetfavoriten für Kontaktunternehmen| Microsoft Docs
description: Sie können Internet oder Internetfavoriten definieren und diese einem Kontaktunternehmen zuordnen, die Ihnen helfen, zu identifizieren, wie Sie nach Informationen über die Kontakte suchen möchten.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 22b9f0be189fa24f366c1ffa20934d2d8e7e8fc5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "819548"
---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="358dc-103">Einrichten von Internetfavoriten für Kontaktunternehmen</span><span class="sxs-lookup"><span data-stu-id="358dc-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="358dc-104">Sie können Ihren Kontakten Internetfavoriten (z. B. Suchmaschinen und Websites) zuordnen, um anzuzeigen, wo Sie im Internet nach Informationen über die Kontakte suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="358dc-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="358dc-105">Wenn Sie Internetfavoriten zuordnen, legen Sie fest, welche Suchmaschine und welchen Suchbegriff die Anwendung bei der Suche nach der gewünschten Information verwendet.</span><span class="sxs-lookup"><span data-stu-id="358dc-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="358dc-106">Die Nutzung von Internetfavoriten zu Kontakten ist ein zwei Schritte umfassender Prozess.</span><span class="sxs-lookup"><span data-stu-id="358dc-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="358dc-107">Zuerst definieren Sie den Buchungsspurcode.</span><span class="sxs-lookup"><span data-stu-id="358dc-107">First, you define the web source code.</span></span> <span data-ttu-id="358dc-108">Sie müssen diesen Schritt nur einmal für jeden Internetfavoriten ausführen.</span><span class="sxs-lookup"><span data-stu-id="358dc-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="358dc-109">Sobald Sie einen Buchungsspurcode haben, können Sie den Code zu den Kontaktpersonen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="358dc-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="358dc-110">um einen Internetfavoritencode zu definieren</span><span class="sxs-lookup"><span data-stu-id="358dc-110">To define a web source code</span></span>
1. <span data-ttu-id="358dc-111">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Webressourcen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="358dc-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="358dc-112">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="358dc-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="358dc-113">Füllen Sie die Felder **Code**, **Beschreibung** und **URL** aus.</span><span class="sxs-lookup"><span data-stu-id="358dc-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="358dc-114">Geben Sie %1 im Feld **URL** ein, um einen Platzhalter für einen Suchbegriff in der URL einzufügen.</span><span class="sxs-lookup"><span data-stu-id="358dc-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="358dc-115">Wenn Sie den Internetfavoriten von einer Kontaktkarte aus aktivieren, wird %1 automatisch durch das Suchwort ersetzt (z. B. den Namen eines Unternehmens), das Sie auf der Seite **Kontakt-Internetfavoriten** eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="358dc-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered on the **Contact Web Sources** page.</span></span>

<span data-ttu-id="358dc-116">Wiederholen Sie diese Schritte, um weitere Internetfavoriten einzurichten.</span><span class="sxs-lookup"><span data-stu-id="358dc-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="358dc-117">Um Internetfavoriten zu einem Kontaktunternehmen zuzuordnen</span><span class="sxs-lookup"><span data-stu-id="358dc-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="358dc-118">Wenn Sie Internetfavoriten zuordnen, legen Sie fest, welche Suchmaschine und welchen Suchbegriff die Anwendung bei der Suche nach der gewünschten Information verwendet.</span><span class="sxs-lookup"><span data-stu-id="358dc-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="358dc-119">Öffnen Sie den Kontakt.</span><span class="sxs-lookup"><span data-stu-id="358dc-119">Open the contact.</span></span>
2. <span data-ttu-id="358dc-120">Wählen Sie die Aktion **Unternehmen** und dann die **Internetfavoriten**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="358dc-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="358dc-121">Die Seite **Kontakt Internetfavoriten** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="358dc-121">The **Contact Web Sources** page opens.</span></span>
3. <span data-ttu-id="358dc-122">Wählen Sie im Feld **Internetfavoritencode** den Internetfavoriten aus, den Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="358dc-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="358dc-123">Geben Sie im Feld **Suchbegriff** den Suchbegriff ein, der bei der Suche nach der Information verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="358dc-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="358dc-124">Wiederholen Sie diese Schritte, um weitere Internetfavoriten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="358dc-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="358dc-125">Ausserdem können Sie Internetfavoriten auf die gleiche Art auf der Seite **Kontaktliste** zuordnen.</span><span class="sxs-lookup"><span data-stu-id="358dc-125">You can also assign web sources from the **Contact List** page by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="358dc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="358dc-126">See Also</span></span>
[<span data-ttu-id="358dc-127">Kontakte erstellen</span><span class="sxs-lookup"><span data-stu-id="358dc-127">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="358dc-128">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="358dc-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
