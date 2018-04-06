---
title: Manuelles Erstellen von Lieferbenachrichtigungen
description: "In Business Central können Sie Lieferbenachrichtigungen erstellen, wenn eine Bestellung nicht wie erwartet geliefert wurde. Sie können eine einzelne Lieferbenachrichtigung manuell erstellen oder Sie können Lieferbenachrichtigungen für alle überfälligen Lieferungen erstellen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a041c22f158121a553ce47197bab4337fbd47d38
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-delivery-reminders-manually"></a><span data-ttu-id="8a593-104">So erstellen Sie Lieferanmahnungen manuell</span><span class="sxs-lookup"><span data-stu-id="8a593-104">Create Delivery Reminders Manually</span></span>
<span data-ttu-id="8a593-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], können Sie Lieferbenachrichtigungen erstellen, wenn eine Bestellung nicht wie erwartet geliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="8a593-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can create delivery reminders when a purchase has not been delivered as expected.</span></span> <span data-ttu-id="8a593-106">Sie können eine einzelne Lieferbenachrichtigung manuell erstellen oder Sie können Lieferbenachrichtigungen für alle überfälligen Lieferungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a593-106">You can create a single delivery reminder manually, or you can generate delivery reminders for all overdue deliveries.</span></span> <span data-ttu-id="8a593-107">Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-generate-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="8a593-107">For more information, see [Generate Delivery Reminders](how-to-generate-delivery-reminders.md).</span></span>

> [!NOTE]
> <span data-ttu-id="8a593-108">Um Lieferbenachrichtigungen zu erstellen, müssen Sie Eigenschaften für Lieferbenachrichtigungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="8a593-108">To create delivery reminders, you must set up the delivery reminder properties.</span></span> <span data-ttu-id="8a593-109">Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-set-up-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="8a593-109">For more information, see [Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md).</span></span>

## <a name="to-create-a-delivery-reminder-manually"></a><span data-ttu-id="8a593-110">So erstellen Sie eine Lieferbenachrichtigung manuell</span><span class="sxs-lookup"><span data-stu-id="8a593-110">To create a delivery reminder manually</span></span>  

1.  <span data-ttu-id="8a593-111">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und öffnen die **Lieferbenachrichtigung**. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8a593-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8a593-112">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="8a593-112">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="8a593-113">Füllen Sie im Fenster **Lieferbenachrichtigung** im Inforegister **Allgemein** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="8a593-113">In the **Delivery Reminder** window, on the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="8a593-114">Feld</span><span class="sxs-lookup"><span data-stu-id="8a593-114">Field</span></span>|<span data-ttu-id="8a593-115">Description</span><span class="sxs-lookup"><span data-stu-id="8a593-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="8a593-116">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="8a593-116">**No.**</span></span>|<span data-ttu-id="8a593-117">Die eindeutige Kennnummer für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="8a593-117">The unique identification number for the delivery reminder.</span></span>|  
    |<span data-ttu-id="8a593-118">**Kreditorennr**</span><span class="sxs-lookup"><span data-stu-id="8a593-118">**Vendor No.**</span></span>|<span data-ttu-id="8a593-119">Die Nummer des Kreditors, für den Sie die Lieferbenachrichtigung buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="8a593-119">The number of the vendor for whom you want to post the delivery reminder.</span></span><br /><br /> <span data-ttu-id="8a593-120">Wenn Sie die Kreditorennummer auswählen, werden die Felder **Name**, **Adresse**, **PLZ-Code/Ort** und **Kontakt** automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="8a593-120">When you select the vendor number, the **Name**, **Address**, **Post Code/City**, and **Contact** fields are filled in automatically.</span></span>|  
    |<span data-ttu-id="8a593-121">**Buchungsdatum**</span><span class="sxs-lookup"><span data-stu-id="8a593-121">**Posting Date**</span></span>|<span data-ttu-id="8a593-122">Das Buchungsdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="8a593-122">The posting date for the delivery reminder.</span></span> <span data-ttu-id="8a593-123">Dieses Datum wird in alle Lieferbenachrichtigungsposten kopiert.</span><span class="sxs-lookup"><span data-stu-id="8a593-123">This date is copied to all of the delivery reminder ledger entries.</span></span>|  
    |<span data-ttu-id="8a593-124">**Belegdatum**</span><span class="sxs-lookup"><span data-stu-id="8a593-124">**Document Date**</span></span>|<span data-ttu-id="8a593-125">Das Belegdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="8a593-125">The document date for the delivery reminder.</span></span> <span data-ttu-id="8a593-126">Dieses Datum wird auch verwendet, um das Fälligkeitsdatum der Lieferbenachrichtigung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="8a593-126">This date is also used to calculate the due date for the delivery reminder.</span></span> <span data-ttu-id="8a593-127">Sie können das Buchungsdatum bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="8a593-127">You can modify the posting date if required.</span></span>|  
    |<span data-ttu-id="8a593-128">**Mahnstufe**</span><span class="sxs-lookup"><span data-stu-id="8a593-128">**Reminder Level**</span></span>|<span data-ttu-id="8a593-129">Die Lieferbenachrichtigungsstufe.</span><span class="sxs-lookup"><span data-stu-id="8a593-129">The delivery reminder level.</span></span> <span data-ttu-id="8a593-130">Dieser Wert basiert auf der Anzahl der Lieferbenachrichtigungen, die bereits gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="8a593-130">This value is based on the number of delivery reminders that have already been sent.</span></span> <span data-ttu-id="8a593-131">Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="8a593-131">For more information, see [Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span></span>|  
    |<span data-ttu-id="8a593-132">**Mahnmethodencode**</span><span class="sxs-lookup"><span data-stu-id="8a593-132">**Reminder Terms Code**</span></span>|<span data-ttu-id="8a593-133">Geben Sie den Lieferbenachrichtigungsmethodencode an, der für den Kreditor eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="8a593-133">Specify the delivery reminder terms code that is set up for the vendor.</span></span>|  
    |<span data-ttu-id="8a593-134">**Fälligkeitsdatum**</span><span class="sxs-lookup"><span data-stu-id="8a593-134">**Due Date**</span></span>|<span data-ttu-id="8a593-135">Das Fälligkeitsdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="8a593-135">The due date for the delivery reminder.</span></span>|  

4.  <span data-ttu-id="8a593-136">Wählen Sie die Aktion **Mahnungszeile vorschlagen**</span><span class="sxs-lookup"><span data-stu-id="8a593-136">Choose the **Suggest Reminder Lines** action</span></span>  

    <span data-ttu-id="8a593-137">Bei überfälligen Lieferungen vom angegebenen Kreditor werden diese der Lieferbenachrichtigung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8a593-137">If there are overdue deliveries from the specified vendor, these are added to the deliver reminder.</span></span>  

5.  <span data-ttu-id="8a593-138">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="8a593-138">Choose the **OK** button.</span></span>  

    <span data-ttu-id="8a593-139">Die Lieferbenachrichtigung wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="8a593-139">The delivery reminder is created.</span></span> <span data-ttu-id="8a593-140">Jetzt können Sie die Lieferbenachrichtigungen ausstellen und drucken.</span><span class="sxs-lookup"><span data-stu-id="8a593-140">You can now issue and print the delivery reminder.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8a593-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a593-141">See Also</span></span>  
 <span data-ttu-id="8a593-142">[Lieferanmahnungen](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="8a593-142">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="8a593-143">[So erstellen Sie Lieferanmahnungen](how-to-generate-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="8a593-143">[Generate Delivery Reminders](how-to-generate-delivery-reminders.md) </span></span>  
 <span data-ttu-id="8a593-144">[Gewusst wie: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="8a593-144">[Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md) </span></span>  
 <span data-ttu-id="8a593-145">[Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span><span class="sxs-lookup"><span data-stu-id="8a593-145">[Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span></span>  
 <span data-ttu-id="8a593-146">[So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="8a593-146">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 <span data-ttu-id="8a593-147">[Lieferbenachrichtigung registrieren](how-to-issue-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="8a593-147">[Issue Delivery Reminders](how-to-issue-delivery-reminders.md) </span></span>  
 [<span data-ttu-id="8a593-148">So drucken Sie Testberichte vor dem Registrieren von Lieferanmahnungen</span><span class="sxs-lookup"><span data-stu-id="8a593-148">Print Test Reports for Delivery Reminders</span></span>](how-to-print-test-reports-for-delivery-reminders.md)

