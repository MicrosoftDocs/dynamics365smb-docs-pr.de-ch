---
title: 'Gewusst wie: Einrichten von Lieferbenachrichtigungsbedingungen, -stufen und -text'
description: "Wenn Sie Lieferbenachrichtigung verwenden möchten, müssen Sie Lieferbenachrichtigungsmethoden, Lieferbenachrichtigungsstufen und Lieferbenachrichtigungstexte einrichten. Nachrichten"
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
ms.openlocfilehash: 6ddda815d211440dfd18982bcec5b8ae15aafc4c
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-delivery-reminder-terms-levels-and-text"></a><span data-ttu-id="2cf24-104">Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text</span><span class="sxs-lookup"><span data-stu-id="2cf24-104">Set Up Delivery Reminder Terms, Levels, and Text</span></span>
<span data-ttu-id="2cf24-105">Um Lieferbenachrichtigung zu erstellen, müssen Sie Folgendes einrichten:</span><span class="sxs-lookup"><span data-stu-id="2cf24-105">To create delivery reminders, you must set up the following:</span></span>  

- <span data-ttu-id="2cf24-106">Lieferbenachrichtigungsbestimmungen</span><span class="sxs-lookup"><span data-stu-id="2cf24-106">Delivery reminder terms</span></span>  
- <span data-ttu-id="2cf24-107">Lieferbenachrichtigungsstufen</span><span class="sxs-lookup"><span data-stu-id="2cf24-107">Delivery reminder levels</span></span>  
- <span data-ttu-id="2cf24-108">Lieferbenachrichtigungstextnachrichten</span><span class="sxs-lookup"><span data-stu-id="2cf24-108">Delivery reminder text messages</span></span>  

<span data-ttu-id="2cf24-109">Jede Lieferbenachrichtigungsmethode verfügt über eigene Lieferbenachrichtigungsstufen, und Sie können für jede der Lieferbenachrichtigungsstufe spezielle Lieferbenachrichtigungstexte definieren.</span><span class="sxs-lookup"><span data-stu-id="2cf24-109">Each delivery reminder term has two or more delivery reminder levels, and for each delivery reminder level, you can specify text that will be part of the delivery reminder.</span></span>  

<span data-ttu-id="2cf24-110">Weitere Informationen finden Sie unter [Lieferbenachrichtigungen](delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="2cf24-110">For more information, see [Delivery Reminders](delivery-reminders.md).</span></span>  

## <a name="to-set-up-delivery-reminder-terms"></a><span data-ttu-id="2cf24-111">Einrichten von Lieferbenachrichtigungsmethoden</span><span class="sxs-lookup"><span data-stu-id="2cf24-111">To set up delivery reminder terms</span></span>  

1.  <span data-ttu-id="2cf24-112">Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") und geben **Lieferbenachrichtigungsmethoden** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="2cf24-112">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delivery Reminder Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2cf24-113">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2cf24-113">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="2cf24-114">Füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="2cf24-114">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="2cf24-115">Feld</span><span class="sxs-lookup"><span data-stu-id="2cf24-115">Field</span></span>|<span data-ttu-id="2cf24-116">Description</span><span class="sxs-lookup"><span data-stu-id="2cf24-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="2cf24-117">**Code**</span><span class="sxs-lookup"><span data-stu-id="2cf24-117">**Code**</span></span>|<span data-ttu-id="2cf24-118">Der Code für das Fälligkeitsdatum der Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="2cf24-118">The code for the delivery reminder term.</span></span> <span data-ttu-id="2cf24-119">Sie können maximal 10 alphanumerische Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="2cf24-119">You can enter a maximum of 10 alphanumeric characters.</span></span>|  
    |<span data-ttu-id="2cf24-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2cf24-120">**Description**</span></span>|<span data-ttu-id="2cf24-121">Die Beschreibung für die Lieferbenachrichtigungsmethode.</span><span class="sxs-lookup"><span data-stu-id="2cf24-121">The description for the delivery reminder term.</span></span> <span data-ttu-id="2cf24-122">Sie können maximal 30 alphanumerische Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="2cf24-122">You can enter a maximum of 30 alphanumeric characters.</span></span>|  
    |<span data-ttu-id="2cf24-123">**Max. Anzahl Lieferbenachrichtigungen**</span><span class="sxs-lookup"><span data-stu-id="2cf24-123">**Max. No. of Delivery Reminders**</span></span>|<span data-ttu-id="2cf24-124">Gibt die maximale Anzahl von Lieferbenachrichtigungen an, die für eine Bestellung erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2cf24-124">The maximum number of delivery reminders that can be created for an order.</span></span><br /><br /> <span data-ttu-id="2cf24-125">**HINWEIS:** Dies ist die maximale Anzahl über alle Mahnstufen hinweg für diese Anmahnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="2cf24-125">**NOTE:** This is the maximum number across all reminder levels for this reminder term.</span></span> <span data-ttu-id="2cf24-126">Wenn Sie beispielsweise drei Stufen eingerichtet haben, und Sie **Max. Anzahl Lieferbenachrichtigungen** auf 5 festlegen, wird die erste Mahnung mit Stufe 1, die zweite mit Stufe 2 und die letzten drei mit Stufe 3 erstellt.</span><span class="sxs-lookup"><span data-stu-id="2cf24-126">For example, if you have set up three levels, and you set **Max. No. of Delivery Reminders** to 5, the first reminder is created at level 1, the second at level 2, and the last three at level 3.</span></span>|  

4.  <span data-ttu-id="2cf24-127">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2cf24-127">Choose the **OK** button.</span></span>  

## <a name="to-add-delivery-reminder-levels-to-a-delivery-reminder-term"></a><span data-ttu-id="2cf24-128">So richten Sie Lieferbenachrichtigungsstufen für Lieferbenachrichtigungsmethoden ein</span><span class="sxs-lookup"><span data-stu-id="2cf24-128">To add delivery reminder levels to a delivery reminder term</span></span>  

1.  <span data-ttu-id="2cf24-129">Klicken Sie im Fenster **Lieferbenachrichtigungsbestimmungen** in die Zeile mit der Methode, für die Sie Stufen anlegen möchten, und wählen Sie dann die Aktion **Stufen**.</span><span class="sxs-lookup"><span data-stu-id="2cf24-129">In the **Delivery Reminder Terms** window, select the delivery reminder term for which you want to set up levels, and then choose the **Levels** action.</span></span>  
2.  <span data-ttu-id="2cf24-130">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2cf24-130">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="2cf24-131">Füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="2cf24-131">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="2cf24-132">Feld</span><span class="sxs-lookup"><span data-stu-id="2cf24-132">Field</span></span>|<span data-ttu-id="2cf24-133">Description</span><span class="sxs-lookup"><span data-stu-id="2cf24-133">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="2cf24-134">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="2cf24-134">**No.**</span></span>|<span data-ttu-id="2cf24-135">Lieferbenachrichtigungsstufenzahl.</span><span class="sxs-lookup"><span data-stu-id="2cf24-135">The delivery reminder level number.</span></span> <span data-ttu-id="2cf24-136">Dieses Feld wird automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="2cf24-136">This field is filled in automatically.</span></span>|  
    |<span data-ttu-id="2cf24-137">**Berechnung Fälligkeitsdatum**</span><span class="sxs-lookup"><span data-stu-id="2cf24-137">**Due Date Calculation**</span></span>|<span data-ttu-id="2cf24-138">Die Formel für die Berechnung des Fälligkeitsdatums für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="2cf24-138">The formula for the due date calculation for the delivery reminder.</span></span> <span data-ttu-id="2cf24-139">Sie können eine Kombination von Nummern zwischen 0 und 9999 sowie Datumscodes eingeben (D für Tag, TW für Wochentag, W für Woche, M für Monat, Q für Quartal oder J für Jahr).</span><span class="sxs-lookup"><span data-stu-id="2cf24-139">You can enter a combination of numbers from 0 to 9999, and date codes (D for day, WD for weekday, W for week, M for month, Q for quarter, or Y for year).</span></span> <span data-ttu-id="2cf24-140">Die Formel für die Berechnung des Datencodes für das Fälligkeitsdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="2cf24-140">The date codes denote the calculation for the delivery reminder due date.</span></span> <span data-ttu-id="2cf24-141">Die Datumsberechnungsformel für das Fälligkeitsdatum kann maximal 20 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="2cf24-141">You can enter a maximum of 20 characters for the due date calculation formula.</span></span>|  

4.  <span data-ttu-id="2cf24-142">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2cf24-142">Choose the **OK** button.</span></span>  

<span data-ttu-id="2cf24-143">Für jede Lieferbenachrichtigungsstufe kann eine Textnachricht definiert werden, der in die Lieferbenachrichtigung aufgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="2cf24-143">For each delivery reminder level, you can define text messages that are added to the delivery reminder.</span></span> <span data-ttu-id="2cf24-144">Sie können Vortext definieren, der vor der Beschreibung der überfälligen Bestellung hinzugefügt wird, und Nachtext, der nach der Beschreibung der überfälligen Bestellung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2cf24-144">You can define beginning text that is added before the description of the overdue purchase order, and ending text that is added after the description of the overdue purchase order.</span></span>  

<span data-ttu-id="2cf24-145">Nachfolgend wird beschrieben, wie Vortextnachrichten eingerichtet werde. Aber dieselben Schritte gelten auch für das Einrichten von Nachtextnachrichten.</span><span class="sxs-lookup"><span data-stu-id="2cf24-145">The following procedure describes how to set up beginning text messages, but the same steps apply for setting up ending text messages.</span></span>  

## <a name="to-set-up-delivery-reminder-text-messages"></a><span data-ttu-id="2cf24-146">Lieferbenachrichtigungstextnachrichten einrichten</span><span class="sxs-lookup"><span data-stu-id="2cf24-146">To set up delivery reminder text messages</span></span>  

1.  <span data-ttu-id="2cf24-147">Im Fenster **Lieferbenachrichtigungsstufen** wählen Sie eine Ebene, und wählen die Aktion **Vortext** aus.</span><span class="sxs-lookup"><span data-stu-id="2cf24-147">In the **Delivery Reminder Levels** window, select a level, and then choose the **Beginning Text** action.</span></span>  
2.  <span data-ttu-id="2cf24-148">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2cf24-148">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="2cf24-149">Geben Sie im Feld **Beschreibung** die Vortextnachricht für die Lieferbenachrichtigung ein.</span><span class="sxs-lookup"><span data-stu-id="2cf24-149">In the **Description** field, enter the beginning text message for the delivery reminder.</span></span>  
4.  <span data-ttu-id="2cf24-150">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2cf24-150">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2cf24-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cf24-151">See Also</span></span>  
 <span data-ttu-id="2cf24-152">[Lieferanmahnungen](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="2cf24-152">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="2cf24-153">[Gewusst wie: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="2cf24-153">[Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md) </span></span>  
 <span data-ttu-id="2cf24-154">[So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="2cf24-154">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 <span data-ttu-id="2cf24-155">[So erstellen Sie Lieferanmahnungen manuell](how-to-create-delivery-reminders-manually.md) </span><span class="sxs-lookup"><span data-stu-id="2cf24-155">[Create Delivery Reminders Manually](how-to-create-delivery-reminders-manually.md) </span></span>  
 [<span data-ttu-id="2cf24-156">Lieferbenachrichtigung registrieren</span><span class="sxs-lookup"><span data-stu-id="2cf24-156">Issue Delivery Reminders</span></span>](how-to-issue-delivery-reminders.md)

