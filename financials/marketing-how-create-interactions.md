---
title: "Erstellen von Aktivitäten zu Kontakten und Segmenten | Microsoft Docs"
description: "Sie erstellen Aktivitäten, um die Aktivitäten und Kommunikationen (z. B. E-Mails) mit Ihren Kontakten und Segmenten in Dynamics 365 zu erfassen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/15/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 57cbc08ab2e05777fae54018fe714d44b64d14e0
ms.contentlocale: de-ch
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-interactions-on-contacts-and-segments"></a><span data-ttu-id="5e1dd-103">Vorgehensweise: Erstellen von Aktivitäten zu Kontakten und Segmenten</span><span class="sxs-lookup"><span data-stu-id="5e1dd-103">How to: Create Interactions on Contacts and Segments</span></span>
<span data-ttu-id="5e1dd-104">Sie erstellen Aktivitäten, um die Aktivitäten und Kommunikationen (z. B. E-Mails) mit Ihren Kontakten und Segmenten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-104">You can create interactions to record all the interactions and communications you have with your contacts and segments, for example, direct mail.</span></span>

<span data-ttu-id="5e1dd-105">Bevor Sie Aktivitäten erstellen, müssen Sie Aktivitätenvorlagen einrichten.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-105">Before you create interactions, you must set up interaction templates.</span></span> <span data-ttu-id="5e1dd-106">Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Aktivitätvorlagen](marketing-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="5e1dd-106">For more information, see  [Set Up Interaction Templates](marketing-interactions.md).</span></span>

## <a name="to-create-an-interaction"></a><span data-ttu-id="5e1dd-107">So erstellen Sie eine Aktivität</span><span class="sxs-lookup"><span data-stu-id="5e1dd-107">To create an interaction</span></span>
1. <span data-ttu-id="5e1dd-108">Öffnen Sie den Kontakt, den Verkäufer oder den Aktivitätenprotokollposten.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-108">Open the contact, salesperson, or interaction log entry.</span></span>
2. <span data-ttu-id="5e1dd-109">Wählen Sie die Aktion **Aktivität erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-109">Choose the **Create Interaction** action.</span></span>
3. <span data-ttu-id="5e1dd-110">Füllen Sie die Felder aus, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-110">Fill in the fields, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="5e1dd-111">Wenn Sie eine andere Aufgabe ausführen müssen, bevor Sie die Aktivität abgeschlossen haben, können Sie **Abbrechen** auswählen und den Assistenten schließen und die Aktivität später abschließen.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-111">If you need to perform another task before finishing the interaction, you can choose **Cancel** and then finish the interaction at a later time.</span></span> <span data-ttu-id="5e1dd-112">Dieses verschiebt die Aktivität.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-112">This postpones the interaction.</span></span>

## <a name="to-finish-and-delete-postponed-interactions"></a><span data-ttu-id="5e1dd-113">Beenden und Löschen von zurückgestellten Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="5e1dd-113">To finish and delete postponed interactions</span></span>
1. <span data-ttu-id="5e1dd-114">Öffnen Sie den Kontakt, den Verkäufer oder den Aktivitätenprotokollposten.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-114">Open the contact, salesperson, or interaction log entry.</span></span>
2. <span data-ttu-id="5e1dd-115">Wählen Sie **Zurückgestellte Aktivitäten**.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-115">Choose **Postponed Interactions**.</span></span>
3. <span data-ttu-id="5e1dd-116">Wählen Sie die fertig zu stellende Aktivität aus, und klicken Sie anschließend auf die Aktion **Fortsetzen**.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-116">Select the interaction you want to finish, and then choose the **Resume** action.</span></span>

## <a name="to-create-an-interaction-on-a-segment"></a><span data-ttu-id="5e1dd-117">So erstellen Sie eine Aktivität für ein Segment</span><span class="sxs-lookup"><span data-stu-id="5e1dd-117">To create an interaction on a segment</span></span>
1. <span data-ttu-id="5e1dd-118">Wählen Sie auf der Startseite **Aktive Segmente**, oder wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Segmente** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-118">On the Home page, choose **Active Segments**, or choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Segments**, and then choose the related link.</span></span>
2. <span data-ttu-id="5e1dd-119">Füllen Sie im Fenster **Segment** die Felder im Abschnitt **Aktivität** aus, um zu anzugeben, welche Aktivität Sie dem Segment zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-119">In the **Segment window**, in the **Interaction** section, fill in the fields to specify which interaction you want to assign to the segment.</span></span>

    <span data-ttu-id="5e1dd-120">Nachdem Sie dem Segment eine Aktivität zugeordnet haben, können Sie die Aktivität für jeden einzelnen Kontakt personalisieren z. B., indem Sie eine andere Aktivitätenvorlage in den Zeilen des Fensters **Segment** auswählen.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-120">After you have assigned an interaction to the segment, you can personalize the interaction for each particular contact within the segment, for example, by selecting another interaction template on the lines in the **Segment** window.</span></span>  
3. <span data-ttu-id="5e1dd-121">Um das Segment und Aktivitäten zu protokollieren, wählen Sie die **Protokoll**-Aktion.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-121">To log the segment and interactions, choose the **Log** action.</span></span> <span data-ttu-id="5e1dd-122">Das Fenster **Segment protokollieren** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-122">The **Log Segment** window opens.</span></span>
4. <span data-ttu-id="5e1dd-123">Wenn Sie ein neues Segment erstellen möchten, das dieselben Kontakte enthält, aktivieren Sie das Kontrollkästchen **Anschluss-Segment erstellen**.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-123">If you want to create a new segment containing the same contacts, select the **Create Follow-up Segment** check box.</span></span> <span data-ttu-id="5e1dd-124">Um ein Anschluss-Segment zu erstellen, müssen Sie im Fenster **Marketing Vertrieb Einr.** bereits Nummernserien für Segmente angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-124">To create a follow-up segment, you must have specified number series for segments in the **Marketing Setup** window.</span></span>

<span data-ttu-id="5e1dd-125">Eine Aktivität wird für jeden Kontakt im Segment in der Tabelle **Aktivitätenprotokollposten** erfasst, und das Segment wird protokolliert.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-125">An interaction is recorded for each contact within the segment in the **Interaction Log Entry** table, and the segment is logged.</span></span> <span data-ttu-id="5e1dd-126">Protokollierte Segmente finden Sie im Fenster **Protokollierte Segmente**.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-126">Logged segments can be found in the **Logged Segment** window.</span></span>

<span data-ttu-id="5e1dd-127">Wenn Sie im Feld **Anschluss-Segment erstellen** ein Häkchen gesetzt haben, wird ein neues Segment erstellt, das dieselben Kontakte enthält wie das von Ihnen protokollierte Segment.</span><span class="sxs-lookup"><span data-stu-id="5e1dd-127">If you have selected the **Create Follow-up Segment** check box, a new segment is created that contains the same contacts as the segment you have just logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e1dd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e1dd-128">See Also</span></span>
[<span data-ttu-id="5e1dd-129">Aktivitäten aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="5e1dd-129">Recording Interactions</span></span>](marketing-interactions.md)  
[<span data-ttu-id="5e1dd-130">Kontakte verwalten</span><span class="sxs-lookup"><span data-stu-id="5e1dd-130">Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="5e1dd-131">Verkaufschancen verwalten</span><span class="sxs-lookup"><span data-stu-id="5e1dd-131">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="5e1dd-132">Marketing & Vertrieb einrichten</span><span class="sxs-lookup"><span data-stu-id="5e1dd-132">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="5e1dd-133">Arbeiten mit Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5e1dd-133">Working with Dynamics 365</span></span>](ui-work-product.md)

