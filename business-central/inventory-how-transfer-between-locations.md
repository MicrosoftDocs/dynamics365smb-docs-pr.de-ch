---
title: "So geht's: Lagerbestand zwischen Lagerplätzen umlagern| Microsoft Docs"
description: "Beschreibt, wie vom Bestand von einem Bereich oder von einem Lager an einen anderen Ort umgebucht wird, entweder mit dem Umlagerungs Erf.-Journal mit oder den Umlagerungsaufträgen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0e21299ab25f05f465b8a33d3a12bc35d9037d0b
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="00095-103">Lagerbestand zwischen Lagerplätzen umlagern</span><span class="sxs-lookup"><span data-stu-id="00095-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="00095-104">Sie können Bestandsartikel zwischen Lagerplätzen umlagern, indem Sie Umlagerungsaufträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="00095-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="00095-105">Sie können auch das Einkaufs-Erfassungsjournal verwenden.</span><span class="sxs-lookup"><span data-stu-id="00095-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="00095-106">Bei Umlagerungsaufträgen senden Sie die ausgehende Umlagerung von einem Lagerplatz und empfangen die eingehende Umlagerung am anderen Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="00095-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="00095-107">Dies ermöglicht es Ihnen, die einbezogenen Lageraktivitäten zu verwalten und bietet mehr Sicherheit, dass Lagerbestandsmengen korrekt aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="00095-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="00095-108">Mit dem Umlagerungs Buch.-Blatt füllen Sie einfach die Felder **Lagerortcode** und **Neuer Lagerortcode** aus.</span><span class="sxs-lookup"><span data-stu-id="00095-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="00095-109">Wenn Sie das Erfassungsjournal buchen, werden die Lagerposten an den fraglichen Lagerplätzen reguliert.</span><span class="sxs-lookup"><span data-stu-id="00095-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="00095-110">Mit dieser Methode werden Lageraktivitäten nicht verwaltet.</span><span class="sxs-lookup"><span data-stu-id="00095-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="00095-111">Wenn Sie Artikel haben, die in Ihrem Lager ohne Lagerortcode erfasst sind, wie beispielsweise aus einer Zeit, als Sie nur ein Lager hatten, dann können Sie diejenigen Artikel nicht mithilfe von Umlagerungsaufträgen übertragen.</span><span class="sxs-lookup"><span data-stu-id="00095-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="00095-112">Stattdessen müssen Sie das Umlagerungs Erf.-Journal verwenden, um die Artikel aus einem leeren Lagerortcode zu einem tatsächlichen Lagerortcode umzubuchen.</span><span class="sxs-lookup"><span data-stu-id="00095-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="00095-113">Weitere Informationen finden Sie Schritt 3 im "Artikel mit Abschnitt des Artikel Umlag. Erf.-Journales übertragen".</span><span class="sxs-lookup"><span data-stu-id="00095-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="00095-114">Um Artikel umzulagern, müssen Lagerplätze und Umlagerungsrouten eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="00095-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="00095-115">Weitere Informationen finden Sie unter [Einrichten von Lagerorten](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="00095-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="00095-116">So lagern Sie Artikel mit einem Umlagerungsauftrag um</span><span class="sxs-lookup"><span data-stu-id="00095-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="00095-117">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Transferaufträge** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="00095-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="00095-118">Füllen Sie im Fenster **Umlagerungsauftrag** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="00095-118">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   <span data-ttu-id="00095-119">Wenn Sie die Felder **In Transit Code**, **Spediteurcode** und **Spediteurtransportart** im Fenster **Umlagerungsroutenspezifikation** ausgefüllt haben, als Sie die Umlagerungsrouten zwischen diesen Lagerorten eingerichtet haben, werden die entsprechenden Felder im Umlagerungsauftrag automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="00095-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.** window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="00095-120">Wenn Sie das Feld **Zustellertransportarten** ausfüllen, wird das Zugangsdatum am Ziellagerplatz berechnet, indem Sie die Transportzeit der Zustellertransportart zum Lieferdatum hinzuaddieren.</span><span class="sxs-lookup"><span data-stu-id="00095-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="00095-121">Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel auszuliefern.</span><span class="sxs-lookup"><span data-stu-id="00095-121">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="00095-122">Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Warenausgang**, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="00095-122">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="00095-123">Die Artikel befinden sich jetzt in der Umlagerung zwischen den angegebenen Lagerplätzen, entsprechend der angegebenen Umlagerungsroute.</span><span class="sxs-lookup"><span data-stu-id="00095-123">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="00095-124">Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel zu empfangen</span><span class="sxs-lookup"><span data-stu-id="00095-124">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="00095-125">Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Eingang**, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="00095-125">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="00095-126">So lagern Sie Artikel mit dem Artikel Umlag. Erfassungsjournal um</span><span class="sxs-lookup"><span data-stu-id="00095-126">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="00095-127">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Artikel Umbuch.-Erfassungsjournale** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="00095-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="00095-128">Füllen Sie im Fenster **Umlagerungs Buch.-Blatt** die notwendigen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="00095-128">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="00095-129">Geben Sie im Feld **Lagerortcode** den Lagerplatz ein, an dem die Artikel aktuell gelagert sind.</span><span class="sxs-lookup"><span data-stu-id="00095-129">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="00095-130">Um Artikel umzulagern die keinen Lagerortcode haben, belassen Sie das Feld **Lagerortcode** leer.</span><span class="sxs-lookup"><span data-stu-id="00095-130">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="00095-131">Im Feld **Neuer Lagerortcode** geben Sie den Lagerplatz ein, an den Sie die Artikel umlagern möchten.</span><span class="sxs-lookup"><span data-stu-id="00095-131">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="00095-132">Wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="00095-132">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="00095-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00095-133">See Also</span></span>
[<span data-ttu-id="00095-134">Verwalten des Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="00095-134">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="00095-135">Einrichten von Lagerorten</span><span class="sxs-lookup"><span data-stu-id="00095-135">Set Up Locations</span></span>](inventory-how-setup-locations.md)  
<span data-ttu-id="00095-136">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="00095-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="00095-137">Sie können auswählen, welche Funktionen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="00095-137">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="00095-138">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="00095-138">General Business Functionality</span></span>](ui-across-business-areas.md)

