---
title: Lieferbenachrichtigungen
description: "Lieferbenachrichtigung werden verwendet, um überfällige Kreditorenlieferungen zu verfolgen und um Kreditoren an überfällige Lieferungen zu erinnern."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7b2634ba14ec0429ebc24bcf59f6d9cedeba7754
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="delivery-reminders"></a><span data-ttu-id="bbd61-103">Lieferbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bbd61-103">Delivery Reminders</span></span>
<span data-ttu-id="bbd61-104">Lieferbenachrichtigung werden verwendet, um überfällige Kreditorenlieferungen zu verfolgen und um Kreditoren an überfällige Lieferungen zu erinnern.</span><span class="sxs-lookup"><span data-stu-id="bbd61-104">Delivery reminders are used to track overdue vendor shipments, and to remind vendors about overdue deliveries.</span></span> <span data-ttu-id="bbd61-105">Um Lieferbenachrichtigung zu erstellen, müssen Sie Folgendes einrichten:</span><span class="sxs-lookup"><span data-stu-id="bbd61-105">To create delivery reminders, you must set up the following:</span></span>  

- <span data-ttu-id="bbd61-106">Lieferbenachrichtigungsbestimmungen</span><span class="sxs-lookup"><span data-stu-id="bbd61-106">Delivery reminder terms</span></span>  

    <span data-ttu-id="bbd61-107">Lieferbenachrichtigungsbestimmungen werden durch einen Code identifiziert, der Kreditoren zugewiesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="bbd61-107">Delivery reminder terms are identified by a code that must be assigned to vendors.</span></span> <span data-ttu-id="bbd61-108">Wenn mehr als eine Kombination der Einstellungen verwendet werden soll, müssen Sie für jede Kombination einen eigenen Code einrichten.</span><span class="sxs-lookup"><span data-stu-id="bbd61-108">To use more than one combination of settings, you must set up a code for each setting separately.</span></span> <span data-ttu-id="bbd61-109">Sie können eine beliebige Anzahl an Lieferbenachrichtigungsbestimmungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="bbd61-109">You can set up any number of delivery reminder terms.</span></span>  

- <span data-ttu-id="bbd61-110">Lieferbenachrichtigungsstufen</span><span class="sxs-lookup"><span data-stu-id="bbd61-110">Delivery reminder levels</span></span>  

    <span data-ttu-id="bbd61-111">Für jede Lieferbenachrichtigungsbestimmung müssen Sie Lieferbenachrichtigungsebenen definieren.</span><span class="sxs-lookup"><span data-stu-id="bbd61-111">For every delivery reminder term, you must set up delivery reminder levels.</span></span> <span data-ttu-id="bbd61-112">Diese Stufen legen fest, wie häufig Lieferbenachrichtigung für eine bestimmte Methode erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="bbd61-112">These levels determine how often delivery reminders can be created for a specific term.</span></span> <span data-ttu-id="bbd61-113">Stufe 1 ist die erste Lieferbenachrichtigung, die Sie für eine überfällige Lieferung erstellen.</span><span class="sxs-lookup"><span data-stu-id="bbd61-113">Level 1 is the first delivery reminder that you create for an overdue delivery.</span></span> <span data-ttu-id="bbd61-114">Stufe 2 ist die zweite Lieferbenachrichtigung und so weiter.</span><span class="sxs-lookup"><span data-stu-id="bbd61-114">Level 2 is the second delivery reminder, and so on.</span></span> <span data-ttu-id="bbd61-115">Wenn Lieferbenachrichtigungen erstellt werden, werden die Anzahl von Mahnungen, die zuvor erzeugt wurden und die aktuelle Nummer verwendet, um Methoden anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="bbd61-115">When delivery reminders are created, the number of reminders that were created previously is considered, and the current number is used to apply terms.</span></span>  

- <span data-ttu-id="bbd61-116">Lieferbenachrichtigungstextnachrichten</span><span class="sxs-lookup"><span data-stu-id="bbd61-116">Delivery reminder texts messages</span></span>  

    <span data-ttu-id="bbd61-117">Für jede Lieferbenachrichtigungstextnachricht müssen Sie Lieferbenachrichtigungsebenen definieren.</span><span class="sxs-lookup"><span data-stu-id="bbd61-117">You must set up delivery reminder text messages for every delivery reminder level.</span></span> <span data-ttu-id="bbd61-118">Es gibt zwei Arten von Lieferbenachrichtigungstexten: Vortexte und Nachtexte.</span><span class="sxs-lookup"><span data-stu-id="bbd61-118">There are two types of delivery reminder text messages: beginning and ending.</span></span> <span data-ttu-id="bbd61-119">Die Vortextnachricht wird unter dem Kopfabschnitt gedruckt, vor der Liste der Posten, die zur Mahnung markiert sind.</span><span class="sxs-lookup"><span data-stu-id="bbd61-119">The beginning text message is printed under the header section, before the list of entries that are marked for reminder.</span></span> <span data-ttu-id="bbd61-120">Die Nachtextnachricht wird nach dieser Liste gedruckt.</span><span class="sxs-lookup"><span data-stu-id="bbd61-120">The ending text message is printed after this list.</span></span>  

<span data-ttu-id="bbd61-121">Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="bbd61-121">For more information, see [Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md).</span></span>  

<span data-ttu-id="bbd61-122">Nach dem Einrichten der Lieferbestimmungen müssen die Lieferbenachrichtigungsbestimmungscodes den Kreditoren zuweisen.</span><span class="sxs-lookup"><span data-stu-id="bbd61-122">After you have set up the delivery terms, you must assign the delivery reminder term codes to vendors.</span></span> <span data-ttu-id="bbd61-123">Weitere Informationen finden Sie unter [Vorgehensweise: Zuweisen von Lieferbenachrichtigungen zu Kreditoren](how-to-assign-delivery-reminder-codes-to-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="bbd61-123">For more information, see [Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md).</span></span>  

<span data-ttu-id="bbd61-124">Lieferbenachrichtigung können manuell oder automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bbd61-124">You can create delivery reminders manually or automatically.</span></span> <span data-ttu-id="bbd61-125">Sie können die Stapelverarbeitung **Lieferbenachrichtigung erstellen** verwenden, um Lieferbenachrichtigungen automatisch zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bbd61-125">You can use the **Create Delivery Reminder** batch job to create delivery reminders automatically.</span></span> <span data-ttu-id="bbd61-126">Dieser Batchauftrag ermöglicht es Ihnen, die Bestellungen auszuwählen, für die Lieferbenachrichtigungen erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="bbd61-126">This batch job allows you to select the purchase orders for which delivery reminders must be created.</span></span> <span data-ttu-id="bbd61-127">Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-issue-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="bbd61-127">For more information, see [Generate Delivery Reminders](how-to-issue-delivery-reminders.md).</span></span>  

<span data-ttu-id="bbd61-128">Sie können Belege auch in Bezug auf Bestellzeilen und Verkaufsauftragszeilen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="bbd61-128">You can also track documents in relation to purchase order lines and sales order lines.</span></span>  

[!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="bbd61-129">stellt die folgenden Berichte bereit:</span><span class="sxs-lookup"><span data-stu-id="bbd61-129"> provides the following reports:</span></span>  

- <span data-ttu-id="bbd61-130">**Registrierte Lieferbenachrichtigung** -, Um die Lieferbenachrichtigung für Kreditoren anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bbd61-130">**Issued Delivery Reminder** - To view the delivery reminders for vendors.</span></span>  
- <span data-ttu-id="bbd61-131">**Lieferbenachrichtigung - Test** -, Um die Lieferbenachrichtigung zu prüfen, bevor Sie diese registrieren.</span><span class="sxs-lookup"><span data-stu-id="bbd61-131">**Delivery Reminder - Test** - To verify the delivery reminders before you issue them.</span></span>  

<span data-ttu-id="bbd61-132">Weitere Informationen finden Sie unter [Vorgehensweise: Drucken von Testberichten für  Lieferbenachrichtigungen](how-to-print-test-reports-for-delivery-reminders.md).</span><span class="sxs-lookup"><span data-stu-id="bbd61-132">For more information, see [Print Test Reports for Delivery Reminders](how-to-print-test-reports-for-delivery-reminders.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="bbd61-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbd61-133">See Also</span></span>  
 <span data-ttu-id="bbd61-134">[Gewusst wie: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="bbd61-134">[Set Up Delivery Reminders](how-to-set-up-delivery-reminders.md) </span></span>  
 <span data-ttu-id="bbd61-135">[Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span><span class="sxs-lookup"><span data-stu-id="bbd61-135">[Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span></span>  
 <span data-ttu-id="bbd61-136">[So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="bbd61-136">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 <span data-ttu-id="bbd61-137">[So erstellen Sie Lieferanmahnungen](how-to-generate-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="bbd61-137">[Generate Delivery Reminders](how-to-generate-delivery-reminders.md) </span></span>  
 <span data-ttu-id="bbd61-138">[So erstellen Sie Lieferanmahnungen manuell](how-to-create-delivery-reminders-manually.md) </span><span class="sxs-lookup"><span data-stu-id="bbd61-138">[Create Delivery Reminders Manually](how-to-create-delivery-reminders-manually.md) </span></span>  
 <span data-ttu-id="bbd61-139">[Lieferbenachrichtigung registrieren](how-to-issue-delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="bbd61-139">[Issue Delivery Reminders](how-to-issue-delivery-reminders.md) </span></span>  
 [<span data-ttu-id="bbd61-140">So drucken Sie Testberichte vor dem Registrieren von Lieferanmahnungen</span><span class="sxs-lookup"><span data-stu-id="bbd61-140">Print Test Reports for Delivery Reminders</span></span>](how-to-print-test-reports-for-delivery-reminders.md)

