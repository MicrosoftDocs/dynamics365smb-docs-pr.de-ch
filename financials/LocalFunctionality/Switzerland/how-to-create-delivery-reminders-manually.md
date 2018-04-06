---
title: 'Gewusst wie: Lieferbenachrichtigungen manuell erstellen'
description: In ADD INCLUDE<!--[!INCLUDE[navnow](../../includes/how-to-generate-delivery-reminders.md).
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 7e82038dc676da036419b47f9685b3678ce8d06e
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-delivery-reminders-manually"></a><span data-ttu-id="f4afd-103">So erstellen Sie Lieferanmahnungen manuell</span><span class="sxs-lookup"><span data-stu-id="f4afd-103">Create Delivery Reminders Manually</span></span>
<span data-ttu-id="f4afd-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], können Sie Lieferbenachrichtigungen erstellen, wenn eine Bestellung nicht wie erwartet geliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="f4afd-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can create delivery reminders when a purchase has not been delivered as expected.</span></span> <span data-ttu-id="f4afd-105">Sie können eine einzelne Lieferbenachrichtigung manuell erstellen oder Sie können Lieferbenachrichtigungen für alle überfälligen Lieferungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f4afd-105">You can create a single delivery reminder manually, or you can generate delivery reminders for all overdue deliveries.</span></span> <span data-ttu-id="f4afd-106">Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-generate-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="f4afd-106">For more information, see [Generate Delivery Reminders](how-to-generate-delivery-reminders.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f4afd-107">Um Lieferanmahnungen zu erstellen, müssen Sie die Lieferanmahnungseigenschaften einrichten.</span><span class="sxs-lookup"><span data-stu-id="f4afd-107">To create delivery reminders, you must set up the delivery reminder properties.</span></span> <span data-ttu-id="f4afd-108">Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-set-up-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="f4afd-108">For more information, see [Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md).</span></span>

## <a name="to-create-a-delivery-reminder-manually"></a><span data-ttu-id="f4afd-109">So erstellen Sie Lieferantenbenachrichtigungen manuell</span><span class="sxs-lookup"><span data-stu-id="f4afd-109">To create a delivery reminder manually</span></span>  

1.  <span data-ttu-id="f4afd-110">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und öffnen die **Lieferbenachrichtigung**. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f4afd-110">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f4afd-111">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f4afd-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="f4afd-112">Füllen Sie im Fenster **Lieferbenachrichtigung** im Inforegister **Allgemein** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="f4afd-112">In the **Delivery Reminder** window, on the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f4afd-113">Feld</span><span class="sxs-lookup"><span data-stu-id="f4afd-113">Field</span></span>|<span data-ttu-id="f4afd-114">Description</span><span class="sxs-lookup"><span data-stu-id="f4afd-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f4afd-115">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="f4afd-115">**No.**</span></span>|<span data-ttu-id="f4afd-116">Die eindeutige Kennnummer für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="f4afd-116">The unique identification number for the delivery reminder.</span></span>|  
    |<span data-ttu-id="f4afd-117">**Kreditorennr**</span><span class="sxs-lookup"><span data-stu-id="f4afd-117">**Vendor No.**</span></span>|<span data-ttu-id="f4afd-118">Die Nummer des Kreditors, für den Sie die Lieferbenachrichtigung buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="f4afd-118">The number of the vendor for whom you want to post the delivery reminder.</span></span><br /><br /> <span data-ttu-id="f4afd-119">Wenn Sie die Kreditorennummer auswählen, werden die Felder **Name**, **Adresse**, **PLZ-Code/Ort** und **Kontakt** automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f4afd-119">When you select the vendor number, the **Name**, **Address**, **Post Code/City**, and **Contact** fields are filled in automatically.</span></span>|  
    |<span data-ttu-id="f4afd-120">**Buchungsdatum**</span><span class="sxs-lookup"><span data-stu-id="f4afd-120">**Posting Date**</span></span>|<span data-ttu-id="f4afd-121">Das Buchungsdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="f4afd-121">The posting date for the delivery reminder.</span></span> <span data-ttu-id="f4afd-122">Dieses Datum wird in alle Lieferbenachrichtigungsposten kopiert.</span><span class="sxs-lookup"><span data-stu-id="f4afd-122">This date is copied to all of the delivery reminder ledger entries.</span></span>|  
    |<span data-ttu-id="f4afd-123">**Belegdatum**</span><span class="sxs-lookup"><span data-stu-id="f4afd-123">**Document Date**</span></span>|<span data-ttu-id="f4afd-124">Das Belegdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="f4afd-124">The document date for the delivery reminder.</span></span> <span data-ttu-id="f4afd-125">Dieses Datum wird auch verwendet, um das Fälligkeitsdatum der Lieferbenachrichtigung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f4afd-125">This date is also used to calculate the due date for the delivery reminder.</span></span> <span data-ttu-id="f4afd-126">Sie können das Buchungsdatum bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="f4afd-126">You can modify the posting date if required.</span></span>|  
    |<span data-ttu-id="f4afd-127">**Mahnstufe**</span><span class="sxs-lookup"><span data-stu-id="f4afd-127">**Reminder Level**</span></span>|<span data-ttu-id="f4afd-128">Die Lieferbenachrichtigungsstufe.</span><span class="sxs-lookup"><span data-stu-id="f4afd-128">The delivery reminder level.</span></span> <span data-ttu-id="f4afd-129">Dieser Wert basiert auf der Anzahl von Lieferbenachrichtigung, die bereits gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="f4afd-129">This value is based on the number of delivery reminders that have already been sent.</span></span> <span data-ttu-id="f4afd-130">Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="f4afd-130">For more information, see [Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span></span>|  
    |<span data-ttu-id="f4afd-131">**Mahnmethodencode**</span><span class="sxs-lookup"><span data-stu-id="f4afd-131">**Reminder Terms Code**</span></span>|<span data-ttu-id="f4afd-132">Geben Sie den Lieferbenachrichtigungsmethodencode an, der für den Kreditor eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="f4afd-132">Specify the delivery reminder terms code that is set up for the vendor.</span></span>|  
    |<span data-ttu-id="f4afd-133">**Fälligkeitsdatum**</span><span class="sxs-lookup"><span data-stu-id="f4afd-133">**Due Date**</span></span>|<span data-ttu-id="f4afd-134">Das Fälligkeitsdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="f4afd-134">The due date for the delivery reminder.</span></span>|  

4.  <span data-ttu-id="f4afd-135">Wählen Sie die Aktion **Mahnungszeile vorschlagen**</span><span class="sxs-lookup"><span data-stu-id="f4afd-135">Choose the **Suggest Reminder Lines** action</span></span>  

    <span data-ttu-id="f4afd-136">Bei überfälligen Lieferungen vom angegebenen Kreditor werden diese der Lieferbenachrichtigung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f4afd-136">If there are overdue deliveries from the specified vendor, these are added to the deliver reminder.</span></span>  

5.  <span data-ttu-id="f4afd-137">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f4afd-137">Choose the **OK** button.</span></span>  

    <span data-ttu-id="f4afd-138">Die Lieferbenachrichtigung wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="f4afd-138">The delivery reminder is created.</span></span> <span data-ttu-id="f4afd-139">So können die Lieferbenachrichtigungen ausgeben und erstellen.</span><span class="sxs-lookup"><span data-stu-id="f4afd-139">You can now issue and print the delivery reminder.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f4afd-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4afd-140">See Also</span></span>  
 <span data-ttu-id="f4afd-141">[Lieferanmahnungen](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="f4afd-141">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="f4afd-142">[So erstellen Sie Lieferanmahnungen](how-to-generate-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="f4afd-142">[Generate Delivery Reminders](how-to-generate-delivery-reminders.md) </span></span>  
 <span data-ttu-id="f4afd-143">[Gewusst wie: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="f4afd-143">[Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md) </span></span>  
 <span data-ttu-id="f4afd-144">[Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span><span class="sxs-lookup"><span data-stu-id="f4afd-144">[Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span></span>  
 <span data-ttu-id="f4afd-145">[So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="f4afd-145">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 <span data-ttu-id="f4afd-146">[Lieferbenachrichtigung registrieren](how-to-issue-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="f4afd-146">[Issue Delivery Reminders](how-to-issue-delivery-reminders.md) </span></span>  
 [<span data-ttu-id="f4afd-147">So drucken Sie Testberichte vor dem Registrieren von Lieferanmahnungen</span><span class="sxs-lookup"><span data-stu-id="f4afd-147">Print Test Reports for Delivery Reminders</span></span>](how-to-print-test-reports-for-delivery-reminders.md)

