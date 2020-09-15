---
title: 'Gewusst wie: Einrichten von Lieferbenachrichtigungsbedingungen, -stufen und -text'
description: Wenn Sie Lieferbenachrichtigung verwenden möchten, müssen Sie Lieferbenachrichtigungsmethoden, Lieferbenachrichtigungsstufen und Lieferbenachrichtigungstexte einrichten. Nachrichten
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 07997f58d13b21572545feb5f801b86ec8bd261c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778194"
---
# <a name="set-up-delivery-reminder-terms-levels-and-text"></a><span data-ttu-id="e74b2-104">Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text</span><span class="sxs-lookup"><span data-stu-id="e74b2-104">Set Up Delivery Reminder Terms, Levels, and Text</span></span>
<span data-ttu-id="e74b2-105">Um Lieferbenachrichtigung zu erstellen, müssen Sie Folgendes einrichten:</span><span class="sxs-lookup"><span data-stu-id="e74b2-105">To create delivery reminders, you must set up the following:</span></span>  

- <span data-ttu-id="e74b2-106">Lieferbenachrichtigungsbestimmungen</span><span class="sxs-lookup"><span data-stu-id="e74b2-106">Delivery reminder terms</span></span>  
- <span data-ttu-id="e74b2-107">Lieferbenachrichtigungsstufen</span><span class="sxs-lookup"><span data-stu-id="e74b2-107">Delivery reminder levels</span></span>  
- <span data-ttu-id="e74b2-108">Lieferbenachrichtigungstextnachrichten</span><span class="sxs-lookup"><span data-stu-id="e74b2-108">Delivery reminder text messages</span></span>  

<span data-ttu-id="e74b2-109">Jede Lieferbenachrichtigungsmethode verfügt über eigene Lieferbenachrichtigungsstufen, und Sie können für jede der Lieferbenachrichtigungsstufe spezielle Lieferbenachrichtigungstexte definieren.</span><span class="sxs-lookup"><span data-stu-id="e74b2-109">Each delivery reminder term has two or more delivery reminder levels, and for each delivery reminder level, you can specify text that will be part of the delivery reminder.</span></span>  

<span data-ttu-id="e74b2-110">Weitere Informationen finden Sie unter [Lieferbenachrichtigungen](delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="e74b2-110">For more information, see [Delivery Reminders](delivery-reminders.md).</span></span>  

## <a name="to-set-up-delivery-reminder-terms"></a><span data-ttu-id="e74b2-111">Einrichten von Lieferbenachrichtigungsmethoden</span><span class="sxs-lookup"><span data-stu-id="e74b2-111">To set up delivery reminder terms</span></span>  

1.  <span data-ttu-id="e74b2-112">Wählen Sie die ![Glühbirne, die das Tell Me Feature](../../media/ui-search/search_small.png "Tell me-Funktion") Symbol öffnet, geben Sie **Lieferanmahnungsbedingungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="e74b2-112">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delivery Reminder Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e74b2-113">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="e74b2-113">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="e74b2-114">Füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="e74b2-114">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="e74b2-115">Feld</span><span class="sxs-lookup"><span data-stu-id="e74b2-115">Field</span></span>|<span data-ttu-id="e74b2-116">Description</span><span class="sxs-lookup"><span data-stu-id="e74b2-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="e74b2-117">**Code**</span><span class="sxs-lookup"><span data-stu-id="e74b2-117">**Code**</span></span>|<span data-ttu-id="e74b2-118">Der Code für das Fälligkeitsdatum der Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="e74b2-118">The code for the delivery reminder term.</span></span> <span data-ttu-id="e74b2-119">Sie können maximal 10 alphanumerische Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="e74b2-119">You can enter a maximum of 10 alphanumeric characters.</span></span>|  
    |<span data-ttu-id="e74b2-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e74b2-120">**Description**</span></span>|<span data-ttu-id="e74b2-121">Die Beschreibung für die Lieferbenachrichtigungsmethode.</span><span class="sxs-lookup"><span data-stu-id="e74b2-121">The description for the delivery reminder term.</span></span> <span data-ttu-id="e74b2-122">Sie können maximal 30 alphanumerische Zeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="e74b2-122">You can enter a maximum of 30 alphanumeric characters.</span></span>|  
    |<span data-ttu-id="e74b2-123">**Max. Anzahl Lieferbenachrichtigungen**</span><span class="sxs-lookup"><span data-stu-id="e74b2-123">**Max. No. of Delivery Reminders**</span></span>|<span data-ttu-id="e74b2-124">Gibt die maximale Anzahl von Lieferbenachrichtigungen an, die für eine Bestellung erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e74b2-124">The maximum number of delivery reminders that can be created for an order.</span></span><br /><br /> <span data-ttu-id="e74b2-125">**HINWEIS:** Dies ist die maximale Anzahl über alle Mahnstufen hinweg für diese Anmahnungsmethode.</span><span class="sxs-lookup"><span data-stu-id="e74b2-125">**NOTE:** This is the maximum number across all reminder levels for this reminder term.</span></span> <span data-ttu-id="e74b2-126">Wenn Sie beispielsweise drei Stufen eingerichtet haben, und Sie **Max. Anzahl Lieferbenachrichtigungen** auf 5 festlegen, wird die erste Mahnung mit Stufe 1, die zweite mit Stufe 2 und die letzten drei mit Stufe 3 erstellt.</span><span class="sxs-lookup"><span data-stu-id="e74b2-126">For example, if you have set up three levels, and you set **Max. No. of Delivery Reminders** to 5, the first reminder is created at level 1, the second at level 2, and the last three at level 3.</span></span>|  

4.  <span data-ttu-id="e74b2-127">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e74b2-127">Choose the **OK** button.</span></span>  

## <a name="to-add-delivery-reminder-levels-to-a-delivery-reminder-term"></a><span data-ttu-id="e74b2-128">So richten Sie Lieferbenachrichtigungsstufen für Lieferbenachrichtigungsmethoden ein</span><span class="sxs-lookup"><span data-stu-id="e74b2-128">To add delivery reminder levels to a delivery reminder term</span></span>  

1.  <span data-ttu-id="e74b2-129">Wählen Sie auf der Seite **Lieferanmahnungsmethoden** die Lieferanmahnung aus, der Sie Stufen hinzufügen möchten, und wählen Sie dann die Aktion **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="e74b2-129">On the **Delivery Reminder Terms** page, select the delivery reminder term for which you want to set up levels, and then choose the **Levels** action.</span></span>  
2.  <span data-ttu-id="e74b2-130">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="e74b2-130">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="e74b2-131">Füllen Sie die Felder wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="e74b2-131">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="e74b2-132">Feld</span><span class="sxs-lookup"><span data-stu-id="e74b2-132">Field</span></span>|<span data-ttu-id="e74b2-133">Description</span><span class="sxs-lookup"><span data-stu-id="e74b2-133">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="e74b2-134">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="e74b2-134">**No.**</span></span>|<span data-ttu-id="e74b2-135">Lieferbenachrichtigungsstufenzahl.</span><span class="sxs-lookup"><span data-stu-id="e74b2-135">The delivery reminder level number.</span></span> <span data-ttu-id="e74b2-136">Dieses Feld wird automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="e74b2-136">This field is filled in automatically.</span></span>|  
    |<span data-ttu-id="e74b2-137">**Berechnung Fälligkeitsdatum**</span><span class="sxs-lookup"><span data-stu-id="e74b2-137">**Due Date Calculation**</span></span>|<span data-ttu-id="e74b2-138">Die Formel für die Berechnung des Fälligkeitsdatums für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="e74b2-138">The formula for the due date calculation for the delivery reminder.</span></span> <span data-ttu-id="e74b2-139">Sie können eine Kombination von Nummern zwischen 0 und 9999 sowie Datumscodes eingeben (D für Tag, TW für Wochentag, W für Woche, M für Monat, Q für Quartal oder J für Jahr).</span><span class="sxs-lookup"><span data-stu-id="e74b2-139">You can enter a combination of numbers from 0 to 9999, and date codes (D for day, WD for weekday, W for week, M for month, Q for quarter, or Y for year).</span></span> <span data-ttu-id="e74b2-140">Die Formel für die Berechnung des Datencodes für das Fälligkeitsdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="e74b2-140">The date codes denote the calculation for the delivery reminder due date.</span></span> <span data-ttu-id="e74b2-141">Die Datumsberechnungsformel für das Fälligkeitsdatum kann maximal 20 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e74b2-141">You can enter a maximum of 20 characters for the due date calculation formula.</span></span>|  

4.  <span data-ttu-id="e74b2-142">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e74b2-142">Choose the **OK** button.</span></span>  

<span data-ttu-id="e74b2-143">Für jede Lieferbenachrichtigungsstufe kann eine Textnachricht definiert werden, der in die Lieferbenachrichtigung aufgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="e74b2-143">For each delivery reminder level, you can define text messages that are added to the delivery reminder.</span></span> <span data-ttu-id="e74b2-144">Sie können Vortext definieren, der vor der Beschreibung der überfälligen Bestellung hinzugefügt wird, und Nachtext, der nach der Beschreibung der überfälligen Bestellung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e74b2-144">You can define beginning text that is added before the description of the overdue purchase order, and ending text that is added after the description of the overdue purchase order.</span></span>  

<span data-ttu-id="e74b2-145">Nachfolgend wird beschrieben, wie Vortextnachrichten eingerichtet werde. Aber dieselben Schritte gelten auch für das Einrichten von Nachtextnachrichten.</span><span class="sxs-lookup"><span data-stu-id="e74b2-145">The following procedure describes how to set up beginning text messages, but the same steps apply for setting up ending text messages.</span></span>  

## <a name="to-set-up-delivery-reminder-text-messages"></a><span data-ttu-id="e74b2-146">Lieferbenachrichtigungstextnachrichten einrichten</span><span class="sxs-lookup"><span data-stu-id="e74b2-146">To set up delivery reminder text messages</span></span>  

1.  <span data-ttu-id="e74b2-147">Wählen Sie auf der Seite **Lieferanmahnungsstufen** eine Stufe aus, und wählen Sie dann die Aktion **Vortext**.</span><span class="sxs-lookup"><span data-stu-id="e74b2-147">On the **Delivery Reminder Levels** page, select a level, and then choose the **Beginning Text** action.</span></span>  
2.  <span data-ttu-id="e74b2-148">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="e74b2-148">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="e74b2-149">Geben Sie im Feld **Beschreibung** die Vortextnachricht für die Lieferbenachrichtigung ein.</span><span class="sxs-lookup"><span data-stu-id="e74b2-149">In the **Description** field, enter the beginning text message for the delivery reminder.</span></span>  
4.  <span data-ttu-id="e74b2-150">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e74b2-150">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e74b2-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e74b2-151">See Also</span></span>  
 <span data-ttu-id="e74b2-152">[Lieferanmahnungen](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="e74b2-152">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="e74b2-153">[Gewusst wie: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="e74b2-153">[Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md) </span></span>  
 <span data-ttu-id="e74b2-154">[So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="e74b2-154">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 <span data-ttu-id="e74b2-155">[Manuelles Erstellen von Lieferanmahnungen](how-to-create-delivery-reminders-manually.md) </span><span class="sxs-lookup"><span data-stu-id="e74b2-155">[Create Delivery Reminders Manually](how-to-create-delivery-reminders-manually.md) </span></span>  
 [<span data-ttu-id="e74b2-156">Lieferbenachrichtigung registrieren</span><span class="sxs-lookup"><span data-stu-id="e74b2-156">Issue Delivery Reminders</span></span>](how-to-issue-delivery-reminders.md)
