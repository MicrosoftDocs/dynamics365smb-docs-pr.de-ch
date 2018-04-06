---
title: "Vorbereiten zur Einrichtung von Geschäftsbeziehungscodes für Kontakte | Microsoft Docs"
description: "Geschäftsbeziehungen in Business Central werden verwendet, um das Marketing zu erleichtern und um die Geschäftsbeziehung anzuzeigen, die Sie mit Ihren Interessenten, Kunden und Debitoren haben, wie z. B. Bank oder Dienstleister."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f879d933822e061913975c1dbac2bf883ad9bbc1
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a><span data-ttu-id="13b3b-103">Einrichten von Geschäftsbeziehungen für Kontaktunternehmen</span><span class="sxs-lookup"><span data-stu-id="13b3b-103">Setting Up Business Relations on Contact Companies</span></span>
<span data-ttu-id="13b3b-104">Sie können Geschäftsbeziehungen verwenden, um die Geschäftsbeziehung anzuzeigen, die Sie mit Ihren Kontakten haben wie z. B. Interessent, Bank, Berater und Dienstleister usw. pflegen.</span><span class="sxs-lookup"><span data-stu-id="13b3b-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="13b3b-105">Die Nutzung von Geschäftsbeziehungen zu Kontakten ist ein zwei Schritte umfassender Prozess.</span><span class="sxs-lookup"><span data-stu-id="13b3b-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="13b3b-106">Zuerst definieren Sie den Geschäftsbeziehungscode.</span><span class="sxs-lookup"><span data-stu-id="13b3b-106">First, you define the business relation code.</span></span> <span data-ttu-id="13b3b-107">Sie müssen diesen Schritt nur einmal für jede Geschäftsbeziehung ausführen.</span><span class="sxs-lookup"><span data-stu-id="13b3b-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="13b3b-108">Sobald Sie einen Geschäftsbeziehungscode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="13b3b-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="13b3b-109">Wenn Sie planen, Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten in anderen Teilen der Anwendung zu synchronisieren, können Sie für sie eine Geschäftsbeziehung erstellen.</span><span class="sxs-lookup"><span data-stu-id="13b3b-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="13b3b-110">Definieren eines Geschäftsbeziehungscodes</span><span class="sxs-lookup"><span data-stu-id="13b3b-110">To define a business relation code</span></span>
<span data-ttu-id="13b3b-111">Der Geschäftsbeziehungscode definiert eine Kategorie oder einen Typ von Geschäftsbeziehung wie BANK oder Gesetz.</span><span class="sxs-lookup"><span data-stu-id="13b3b-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="13b3b-112">Sie können mehrere Geschäftsbeziehungscodes haben.</span><span class="sxs-lookup"><span data-stu-id="13b3b-112">You can have several business relation codes.</span></span> <span data-ttu-id="13b3b-113">Um die Geschäftsbeziehung zu definieren, verwenden Sie das **Geschäftsbeziehungen**-Fenster.</span><span class="sxs-lookup"><span data-stu-id="13b3b-113">To define the business relation, you use the **Business Relations** window.</span></span>

1. <span data-ttu-id="13b3b-114">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Geschäftsbeziehungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="13b3b-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="13b3b-115">Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="13b3b-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="13b3b-116">Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.</span><span class="sxs-lookup"><span data-stu-id="13b3b-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="13b3b-117"><a name="AssignBusRelContact">Um Kontakten Geschäftsbeziehungen zuzuordnen:</a></span><span class="sxs-lookup"><span data-stu-id="13b3b-117"><a name="AssignBusRelContact"></a> To assign business relations to a contact</span></span>
<span data-ttu-id="13b3b-118">Sie können Geschäftsbeziehungen nicht zu Personen zuordnen – nur zu Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="13b3b-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="13b3b-119">Öffnen Sie den Kontakt.</span><span class="sxs-lookup"><span data-stu-id="13b3b-119">Open the contact.</span></span>
2. <span data-ttu-id="13b3b-120">Wählen Sie die Aktion **Unternehmen** und dann die **Geschäftsbeziehungen**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="13b3b-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="13b3b-121">Das Fenster **Kontakt Geschäftsbeziehungen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="13b3b-121">The **Contact Business Relations** window opens.</span></span>
3. <span data-ttu-id="13b3b-122">Wählen Sie im Feld **Geschäftsbeziehungscode** die Geschäftsbeziehung aus, die Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="13b3b-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="13b3b-123">Wiederholen Sie diese Schritte, um beliebig viele Geschäftsbeziehungen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="13b3b-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="13b3b-124">Ausserdem können Sie Geschäftsbeziehungen auf die gleiche Art in dem Fenster Kontaktliste zuordnen.</span><span class="sxs-lookup"><span data-stu-id="13b3b-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="13b3b-125">Die Anzahl der Geschäftsbeziehungen, die Sie dem Kontakt auf der Kontaktkarte zugeordnet haben, wird im Feld **Anzahl Geschäftsbeziehungen** im Abschnitt **Segmentierung** im Fenster **Kontakt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="13b3b-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="13b3b-126">Nachdem Sie Ihren Kontakten Geschäftsbeziehungen zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="13b3b-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="13b3b-127">Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="13b3b-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="13b3b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13b3b-128">See Also</span></span>
[<span data-ttu-id="13b3b-129">Kontaktunternehmenerstellen</span><span class="sxs-lookup"><span data-stu-id="13b3b-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="13b3b-130">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="13b3b-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

