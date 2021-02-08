---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: df06e45136e3ab948fb6ca090c84d10609b76f45
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747544"
---
<span data-ttu-id="d81bf-101">In [!INCLUDE[prod_short](../../../includes/prod_short.md)] können Sie Lieferanmahnungen erstellen, wenn eine Bestellung nicht wie erwartet geliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="d81bf-101">In [!INCLUDE[prod_short](../../../includes/prod_short.md)], you can create delivery reminders when a purchase has not been delivered as expected.</span></span> <span data-ttu-id="d81bf-102">Sie können eine einzelne Lieferanmahnung manuell erstellen oder Sie können Lieferanmahnungen für alle überfälligen Lieferungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="d81bf-102">You can create a single delivery reminder manually, or you can generate delivery reminders for all overdue deliveries.</span></span>  

> [!NOTE]
> <span data-ttu-id="d81bf-103">Um Lieferanmahnungen zu erstellen, müssen Sie die Lieferanmahnungsbestimmungen, -stufen und -texte eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="d81bf-103">To create delivery reminders, you must have set up the delivery reminder terms, levels, and texts.</span></span>

## <a name="to-create-a-delivery-reminder-manually"></a><span data-ttu-id="d81bf-104">So erstellen Sie eine Lieferbenachrichtigung manuell</span><span class="sxs-lookup"><span data-stu-id="d81bf-104">To create a delivery reminder manually</span></span>  

1. <span data-ttu-id="d81bf-105">Wählen Sie das Symbol ![Glühbirne, das die Tell me Funktion](../../../media/ui-search/search_small.png "Tell me-Funktion") öffnet, geben Sie **Lieferanmahnung** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="d81bf-105">Choose the ![The lightbulb icon that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d81bf-106">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d81bf-106">Choose the **New** action.</span></span>  
3. <span data-ttu-id="d81bf-107">Füllen Sie auf der Seite **Lieferanmahnung** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="d81bf-107">On the **Delivery Reminder** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="d81bf-108">Feld</span><span class="sxs-lookup"><span data-stu-id="d81bf-108">Field</span></span>|<span data-ttu-id="d81bf-109">Description</span><span class="sxs-lookup"><span data-stu-id="d81bf-109">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="d81bf-110">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="d81bf-110">**No.**</span></span>|<span data-ttu-id="d81bf-111">Die eindeutige Kennnummer für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="d81bf-111">The unique identification number for the delivery reminder.</span></span>|  
    |<span data-ttu-id="d81bf-112">**Kreditorennr**</span><span class="sxs-lookup"><span data-stu-id="d81bf-112">**Vendor No.**</span></span>|<span data-ttu-id="d81bf-113">Die Nummer des Kreditors, für den Sie die Lieferbenachrichtigung buchen möchten.</span><span class="sxs-lookup"><span data-stu-id="d81bf-113">The number of the vendor for whom you want to post the delivery reminder.</span></span><br /><br /> <span data-ttu-id="d81bf-114">Wenn Sie die Kreditorennummer auswählen, werden die Felder **Name**, **Adresse**, **PLZ-Code/Ort** und **Kontakt** automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="d81bf-114">When you select the vendor number, the **Name**, **Address**, **Post Code/City**, and **Contact** fields are filled in automatically.</span></span>|  
    |<span data-ttu-id="d81bf-115">**Buchungsdatum**</span><span class="sxs-lookup"><span data-stu-id="d81bf-115">**Posting Date**</span></span>|<span data-ttu-id="d81bf-116">Das Buchungsdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="d81bf-116">The posting date for the delivery reminder.</span></span> <span data-ttu-id="d81bf-117">Dieses Datum wird in alle Lieferbenachrichtigungsposten kopiert.</span><span class="sxs-lookup"><span data-stu-id="d81bf-117">This date is copied to all of the delivery reminder ledger entries.</span></span>|  
    |<span data-ttu-id="d81bf-118">**Belegdatum**</span><span class="sxs-lookup"><span data-stu-id="d81bf-118">**Document Date**</span></span>|<span data-ttu-id="d81bf-119">Das Belegdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="d81bf-119">The document date for the delivery reminder.</span></span> <span data-ttu-id="d81bf-120">Dieses Datum wird auch verwendet, um das Fälligkeitsdatum der Lieferbenachrichtigung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="d81bf-120">This date is also used to calculate the due date for the delivery reminder.</span></span> <span data-ttu-id="d81bf-121">Sie können das Buchungsdatum bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="d81bf-121">You can modify the posting date if required.</span></span>|  
    |<span data-ttu-id="d81bf-122">**Mahnstufe**</span><span class="sxs-lookup"><span data-stu-id="d81bf-122">**Reminder Level**</span></span>|<span data-ttu-id="d81bf-123">Die Lieferbenachrichtigungsstufe.</span><span class="sxs-lookup"><span data-stu-id="d81bf-123">The delivery reminder level.</span></span> <span data-ttu-id="d81bf-124">Dieser Wert basiert auf der Anzahl der Lieferbenachrichtigungen, die bereits gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d81bf-124">This value is based on the number of delivery reminders that have already been sent.</span></span>|  
    |<span data-ttu-id="d81bf-125">**Mahnmethodencode**</span><span class="sxs-lookup"><span data-stu-id="d81bf-125">**Reminder Terms Code**</span></span>|<span data-ttu-id="d81bf-126">Geben Sie den Lieferbenachrichtigungsmethodencode an, der für den Kreditor eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="d81bf-126">Specify the delivery reminder terms code that is set up for the vendor.</span></span>|  
    |<span data-ttu-id="d81bf-127">**Fälligkeitsdatum**</span><span class="sxs-lookup"><span data-stu-id="d81bf-127">**Due Date**</span></span>|<span data-ttu-id="d81bf-128">Das Fälligkeitsdatum für die Lieferbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="d81bf-128">The due date for the delivery reminder.</span></span>|  

4. <span data-ttu-id="d81bf-129">Wählen Sie die Aktion **Mahnungszeile vorschlagen**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-129">Choose the **Suggest Reminder Lines** action.</span></span>  

    <span data-ttu-id="d81bf-130">Wenn es überfällige Lieferungen vom angegebenen Kreditor gibt, werden diese der Lieferanmahnung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d81bf-130">If there are overdue deliveries from the specified vendor, these are added to the delivery reminder.</span></span>  

5. <span data-ttu-id="d81bf-131">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="d81bf-131">Choose the **OK** button.</span></span>  

    <span data-ttu-id="d81bf-132">Die Lieferbenachrichtigung wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="d81bf-132">The delivery reminder is created.</span></span> <span data-ttu-id="d81bf-133">Jetzt können Sie die Lieferbenachrichtigungen ausstellen und drucken.</span><span class="sxs-lookup"><span data-stu-id="d81bf-133">You can now issue and print the delivery reminder.</span></span>  
