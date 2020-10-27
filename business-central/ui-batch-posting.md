---
title: So senden Sie mehrere Belege gleichzeitig | Microsoft Docs
description: Anstatt einzelne Belege einzeln zu buchen, können Sie mehrere nicht gebuchte Belege in einer Liste für die Stapelbuchung auswählen, entweder für die sofortige Buchung oder für die geplante Buchung zum Beispiel bis zum Tagesende.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1fd25f8b07a359414f62ef4757162f8a73889c27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912735"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="6e0b3-103">Mehrere Belege gleichzeitig buchen</span><span class="sxs-lookup"><span data-stu-id="6e0b3-103">Post Multiple Documents at the Same Time</span></span>

<span data-ttu-id="6e0b3-104">Anstatt einzelne Belege einzeln zu buchen, können Sie mehrere nicht gebuchte Belege in einer Liste für die Stapelbuchung auswählen, entweder für die sofortige Buchung oder für die geplante Buchung zum Beispiel am Tagesende.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="6e0b3-105">Dies kann hilfreich sein, wenn nur ein Supervisor Belege veröffentlichen kann, die von anderen Benutzern erstellt wurden, oder um zu vermeiden, dass Systemleistungsprobleme während der Arbeitszeit veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="6e0b3-106">Mehrere Einkaufsbestellungen sofort buchen</span><span class="sxs-lookup"><span data-stu-id="6e0b3-106">To post multiple purchase orders immediately</span></span>

<span data-ttu-id="6e0b3-107">Das folgende Verfahren erläutert, wie Sie mehrere Einkaufsbestellungen sofort buchen.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="6e0b3-108">Die Schritte sind für alle Einkaufs- und Verkaufsbelege ähnlich.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="6e0b3-109">Wählen Sie die ![Glühbirne, die das Tell Me Feature öffnet](media/ui-search/search_small.png "Tell Me-Funktion") Symbol, geben Sie **Bestellungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders** , and then choose the related link.</span></span>
2. <span data-ttu-id="6e0b3-110">Auf der Seite **Einkaufsbestellung** wählen Sie auf der folgenden Seite alle Bestellungen aus, die gebucht werden sollen:</span><span class="sxs-lookup"><span data-stu-id="6e0b3-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="6e0b3-111">Geben Sie im Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="6e0b3-111">In the **No.**</span></span> <span data-ttu-id="6e0b3-112">Wählen Sie in diesem Feld die drei vertikalen Punkte aus, um das Kontextmenü zu öffnen, und wählen Sie dann die Aktion **Wählen Sie Mehr** aus.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="6e0b3-113">Aktivieren Sie das Kontrollkästchen für alle Zeilen, die Aufträge darstellen, die Sie gleichzeitig buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="6e0b3-114">Wählen Sie die zu **buchende** Aktion aus, und wählen Sie dann die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="6e0b3-115">Klicken Sie auf die Schaltfläche **Ja** auf der Bestätigungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="6e0b3-116">Um mehrere Einkaufsbestellungen sofort zu buchen</span><span class="sxs-lookup"><span data-stu-id="6e0b3-116">To batch post multiple purchase orders</span></span>

<span data-ttu-id="6e0b3-117">Das folgende Verfahren erläutert, wie Sie mehrere Einkaufsbestellungen buchen.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="6e0b3-118">Die Schritte sind für alle Kauf- und Verkaufsbelege gleich, bei denen die Aktion **Stapelbuchung** verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="6e0b3-119">Die Stapelbuchung von Belegen erfolgt im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-119">Batch posting of documents happens in the background.</span></span> <span data-ttu-id="6e0b3-120">[!INCLUDE [prodshort](includes/prodshort.md)] online enthält Standardprojekte für die Hintergrundbuchung und die Stapelbuchung.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-120">[!INCLUDE [prodshort](includes/prodshort.md)] online includes default jobs for background posting and batch posting.</span></span> <span data-ttu-id="6e0b3-121">Weitere Informationen finden Sie unter [Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="6e0b3-121">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="6e0b3-122">Wählen Sie die ![Glühbirne, die das Tell Me Feature öffnet](media/ui-search/search_small.png "Tell Me-Funktion") Symbol, geben Sie **Bestellungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders** , and then choose the related link.</span></span>  
2. <span data-ttu-id="6e0b3-123">Auf der Seite **Einkaufsbestellung** wählen Sie auf der folgenden Seite alle Bestellungen aus, die gebucht werden sollen:</span><span class="sxs-lookup"><span data-stu-id="6e0b3-123">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="6e0b3-124">Geben Sie im Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="6e0b3-124">In the **No.**</span></span> <span data-ttu-id="6e0b3-125">Wählen Sie in diesem Feld die drei vertikalen Punkte aus, um das Kontextmenü zu öffnen, und wählen Sie dann die Aktion **Wählen Sie Mehr** aus.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-125">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="6e0b3-126">Aktivieren Sie das Kontrollkästchen für alle Zeilen, die Aufträge darstellen, die Sie gleichzeitig buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-126">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="6e0b3-127">Wählen Sie die zu **buchende** Aktion aus, und wählen Sie dann die Aktion **Stapelbuchung** aus.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-127">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="6e0b3-128">Füllen Sie auf der Seite **Stapelbuchung Einkaufsbestellung** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-128">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="6e0b3-129">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-129">Choose the **OK** button.</span></span>
8. <span data-ttu-id="6e0b3-130">Um mögliche Probleme anzuzeigen, die bei der Stapelbuchung von Belegen aufgetreten sind, öffnen Sie die Seite **Fehlermeldungsregister** .</span><span class="sxs-lookup"><span data-stu-id="6e0b3-130">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="6e0b3-131">Die Bestellungen werden nun zu einem dedizierten Auftragswarteschlangeneintrag hinzugefügt, der festlegt, wann die Belege gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-131">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="6e0b3-132">Weitere Informationen finden Sie unter [Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="6e0b3-132">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="6e0b3-133">Wenn Sie **PDF** in dem **Berichtausgabetyp** in diesem Feld auswählen, sind erfolgreich gebuchte Bestellungen im **Berichtseingang** Teil in Ihrem Rollencenter verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e0b3-133">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e0b3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e0b3-134">See Also</span></span>

[<span data-ttu-id="6e0b3-135">Journale und Belege buchen</span><span class="sxs-lookup"><span data-stu-id="6e0b3-135">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="6e0b3-136">Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="6e0b3-136">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="6e0b3-137">Gebuchte Belege bearbeiten</span><span class="sxs-lookup"><span data-stu-id="6e0b3-137">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="6e0b3-138">Ändern oder Löschen einer unbezahlten Einkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="6e0b3-138">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="6e0b3-139">Suchen von Seiten und Informationen mit Wie möchten Sie weiter verfahren</span><span class="sxs-lookup"><span data-stu-id="6e0b3-139">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="6e0b3-140">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6e0b3-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
