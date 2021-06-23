---
title: Lagerplatzkarte einrichten und Umlagerungsroute definieren
description: Sie stellen eine Lagerortkarte für jedes Bundesland, den von Lagerartikel speichern, beispielsweise, ein Lager oder eine Vertriebsstelle und Einrichtungsrouten, um Artikel zwischen Lagerorten umlagern erstellen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184338"
---
# <a name="set-up-locations"></a><span data-ttu-id="3982b-103">Einrichten von Lagerorten</span><span class="sxs-lookup"><span data-stu-id="3982b-103">Set Up Locations</span></span>

<span data-ttu-id="3982b-104">Wenn Sie Artikel an mehreren Orten oder Lagern einkaufen, lagern oder verkaufen, müssen Sie für jeden Lagerort eine Standortkarte einrichten und Umlagerungsroute definieren.</span><span class="sxs-lookup"><span data-stu-id="3982b-104">If you buy, store, or sell items at more than one place or warehouse, you must set up each location with a location card and define transfer routes.</span></span> <span data-ttu-id="3982b-105">[!INCLUDE [prod_short](includes/prod_short.md)] verwendet Lagerorte, um den Bestand sowohl in einfacheren Fällen als auch in komplexeren Lagerprozessen zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="3982b-105">[!INCLUDE [prod_short](includes/prod_short.md)] uses locations to help keep track of inventory in both simpler cases and the more complex warehouse processes.</span></span>

<span data-ttu-id="3982b-106">Sie können dann Belegzeilen für einen bestimmten Lagerplatz erstellen, Verfügbarkeit nach Lagerplatz anzeigen und Lagerbestand zwischen Lagerplätzen umlagern.</span><span class="sxs-lookup"><span data-stu-id="3982b-106">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="3982b-107">Weitere Informationen finden Sie unter [Lagerbestand verwalten](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="3982b-107">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a><span data-ttu-id="3982b-108">Lagerortkarten</span><span class="sxs-lookup"><span data-stu-id="3982b-108">Location cards</span></span>

<span data-ttu-id="3982b-109">Die Lagerortkarte enthält Informationen zu einem Lagerort, z. B. ein Lager oder eine Vertriebsstelle.</span><span class="sxs-lookup"><span data-stu-id="3982b-109">The location card specifies information about a location, such as a warehouse or distribution center.</span></span> <span data-ttu-id="3982b-110">Sie vergeben für jeden Lagerort einen Namen und einen Code, der den Lagerort darstellt.</span><span class="sxs-lookup"><span data-stu-id="3982b-110">You give each location a name and a code that represents the location.</span></span> <span data-ttu-id="3982b-111">Sie können dann den Lagerortcode auch in anderen Bereichen des Programms angeben, wenn Sie die Transaktionen für einen bestimmten Lagerort speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="3982b-111">You can then enter the location code in other parts of the program when you want to record transactions for a given location.</span></span>  

<span data-ttu-id="3982b-112">Sie können Informationen zu Lagerplätzen und Lagerrichtlinien für jeden Lagerort eingeben.</span><span class="sxs-lookup"><span data-stu-id="3982b-112">You can enter information about bins and warehouse policies for each location.</span></span> <span data-ttu-id="3982b-113">Basierend auf den von Ihnen ausgewählten Lagerrichtlinien können Sie die Optionen des Inforegisters **Lagerplätze** verwenden, um die Lagerplätze zu definieren, die bei bestimmten Transaktionen als Standardlagerplätze verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3982b-113">Based on the warehouse policies you select, you can use the options on the **Bins** FastTab to define the bins that will be used as default bins when you are performing transactions.</span></span> <span data-ttu-id="3982b-114">Wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, verwenden Sie die meisten Optionen im Inforegister **Lagerplatzprüfung**, um festzulegen, wie Sie die zahlreichen erweiterten Logistikfunktionen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="3982b-114">If you are using directed put-away and pick, you use most of the options on the **Bin Policies** FastTab to define how you would like to use the various advanced warehousing features.</span></span>  

<span data-ttu-id="3982b-115">Einige Optionsfelder werden durch andere Einstellungen auf der Seite **Lagerortkarte** abgeblendet dargestellt und deaktiviert, um nicht unterstützte Einrichtungskombinationen zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="3982b-115">Some option fields are grayed and disabled by other settings in the **Location Card** page to restrict unsupported setup combinations.</span></span>  

<span data-ttu-id="3982b-116">Wählen Sie die Aktion **Zonen** oder **Lagerplätze** aus, um Informationen über Zonen und Lagerplätze anzuzeigen, die ggf. für den Lagerplatz festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3982b-116">Choose the **Zones** or **Bins** action to view information about zones and bins that may be defined for the location.</span></span>

### <a name="to-create-a-location-card"></a><span data-ttu-id="3982b-117">So erstellen Sie eine Lagerortkarte</span><span class="sxs-lookup"><span data-stu-id="3982b-117">To create a location card</span></span>

1. <span data-ttu-id="3982b-118">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Lagerorte** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="3982b-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="3982b-119">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="3982b-119">Choose the **New** action.</span></span>
3. <span data-ttu-id="3982b-120">Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="3982b-120">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="3982b-121">Wiederholen Sie die Schritte 2 und 3 für jeden Lagerplatz, an dem Sie Lagerbestand aufbewahren möchten.</span><span class="sxs-lookup"><span data-stu-id="3982b-121">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="3982b-122">Viele Felder auf der Lagerortkarte beziehen sich auf Auftragsabwicklung von Artikel in eingehenden und ausgehenden Lagerprozessen.</span><span class="sxs-lookup"><span data-stu-id="3982b-122">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="3982b-123">Für Unternehmen, die die komplexeren Lagerfunktionen nicht benötigen, sind die Felder nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="3982b-123">The fields are not relevant for companies that do not require the more complex warehouse functionality.</span></span> <span data-ttu-id="3982b-124">Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="3982b-124">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="3982b-125">Sie können die Konfiguration eines Lagerorts später ändern, die Einrichtung von Lagerorten mit Lagerposten jedoch nicht bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3982b-125">You can change the configuration of a location later, but you cannot edit the setup of locations that have item ledger entries.</span></span>  

<span data-ttu-id="3982b-126">Wenn Sie über mehrere Lagerorte verfügen, können Sie als Nächstes Umlagerungsrouten zwischen Lagerorten definieren.</span><span class="sxs-lookup"><span data-stu-id="3982b-126">Next, if you have multiple locations, you can define transfer routes between locations.</span></span>  

### <a name="to-create-a-transfer-route"></a><span data-ttu-id="3982b-127">So erstellen Sie eine Umlagerungsroute</span><span class="sxs-lookup"><span data-stu-id="3982b-127">To create a transfer route</span></span>

1. <span data-ttu-id="3982b-128">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Umlagerungsrouten** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="3982b-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="3982b-129">Wählen Sie von jedem beliebigen Fenster **Standortkarten** die Aktion **Umlagerungsrouten** aus.</span><span class="sxs-lookup"><span data-stu-id="3982b-129">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="3982b-130">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="3982b-130">Choose the **New** action.</span></span>
4. <span data-ttu-id="3982b-131">Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="3982b-131">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="3982b-132">Sie können jetzt die Lagerartikel zwischen zwei Lagerplätzen umlagern.</span><span class="sxs-lookup"><span data-stu-id="3982b-132">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="3982b-133">Weitere Informationen finden Sie unter [Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="3982b-133">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="bins"></a><span data-ttu-id="3982b-134">Lagerplätze</span><span class="sxs-lookup"><span data-stu-id="3982b-134">Bins</span></span>

<span data-ttu-id="3982b-135">Lagerplätze stellen die grundlegende Lagerstruktur dar und werden verwendet, um Vorschläge zur Einlagerung von Artikeln zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3982b-135">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="3982b-136">Wenn Sie Ihre Lagerplätze erzeugt haben, können Sie präzise festlegen, welche Inhalte in jeden Lagerplatz eingelagert werden soll, oder der Lagerplatz kann als freier Lagerplatz fungieren, dem kein bestimmter Inhalt zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="3982b-136">When you have created your bins, you can define precisely the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span> <span data-ttu-id="3982b-137">Lagerplätze werden überwiegend in grundlegenden und erweiterten Lagervorgängen eingesetzt.</span><span class="sxs-lookup"><span data-stu-id="3982b-137">Bins are predominantly used in basic and advance warehouse operations.</span></span> <span data-ttu-id="3982b-138">Wenn Sie das Lager in einer einfacheren Einrichtung verwalten, benötigen Sie wahrscheinlich keine Lagerplätze.</span><span class="sxs-lookup"><span data-stu-id="3982b-138">If you manage inventory in a more simple setup, you probably do not need bins.</span></span>

<span data-ttu-id="3982b-139">Um die Lagerplatzfunktionen an einem Lagerort zu verwenden, aktivieren Sie zuerst die Funktion auf der Karte **Lagerort**, indem Sie das Feld **Lagerplatz notwendig** im Inforegister **Lager** auswählen.</span><span class="sxs-lookup"><span data-stu-id="3982b-139">To use the bin functionality at a location, you first activate the functionality on the **Location** card by selecting the **Bins Mandatory** field on the **Warehouse** FastTab.</span></span> <span data-ttu-id="3982b-140">Dann entwerfen Sie den Warenfluss am Lagerort, indem Sie Lagerplatzcodes in den Einrichtungsfeldern angeben, die für die verschiedenen Ströme stehen.</span><span class="sxs-lookup"><span data-stu-id="3982b-140">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>

> [!NOTE]
> <span data-ttu-id="3982b-141">Bevor Sie Lagerplatzcodes auf der Lagerortkarte festlegen können, müssen die Lagerplatzcodes erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3982b-141">Before you can specify bin codes on the location card, the bin codes must be created.</span></span>

<span data-ttu-id="3982b-142">Weitere Informationen finden Sie unter [Erstellen von Lagerplätzen](warehouse-how-to-create-individual-bins.md) und [Lagerplatzarten einrichten](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="3982b-142">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md) and [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="zones"></a><span data-ttu-id="3982b-143">Zonen</span><span class="sxs-lookup"><span data-stu-id="3982b-143">Zones</span></span>

<span data-ttu-id="3982b-144">Wenn Sie Ihre Lagerplätze nach Zonen strukturieren möchten, haben Sie auf der Seite **Zonen** dazu die Möglichkeit.</span><span class="sxs-lookup"><span data-stu-id="3982b-144">If you want to structure your bins under zones, you can do that in the **Zones** page.</span></span>

<span data-ttu-id="3982b-145">[!INCLUDE [prod_short](includes/prod_short.md)] kopiert die Felder, die Sie für jede Zone einrichten, in alle zugehörigen Lagerplätze.</span><span class="sxs-lookup"><span data-stu-id="3982b-145">[!INCLUDE [prod_short](includes/prod_short.md)] copies the fields that you set for any particular zone to the bins within it.</span></span> <span data-ttu-id="3982b-146">Auf diese Weise können Sie eine Zone einem Lagerplatz oder einer Lagerplatzvorlage zuweisen (Filter für Lagerplatzerstellung), und verschiedene andere Felder werden dann automatisch gefüllt.</span><span class="sxs-lookup"><span data-stu-id="3982b-146">This way, you can assign a zone to a bin or a bin template (bin creation filter), and several other fields are then filled in automatically.</span></span>

<span data-ttu-id="3982b-147">Sie können jedoch auch nur eine Zone einrichten und Ihr Lager einfach auf Lagerplatzebene verwalten.</span><span class="sxs-lookup"><span data-stu-id="3982b-147">However, you can choose to set up just one zone and to organize your warehouse according to bins alone.</span></span> <span data-ttu-id="3982b-148">Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="3982b-148">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="3982b-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3982b-149">See Also</span></span>

[<span data-ttu-id="3982b-150">Verwalten des Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="3982b-150">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="3982b-151">Lagerbestand zwischen Lagerplätzen umlagern</span><span class="sxs-lookup"><span data-stu-id="3982b-151">Transfer Inventory Between Locations</span></span>](inventory-how-transfer-between-locations.md)  
[<span data-ttu-id="3982b-152">Lagerplätze erstellen</span><span class="sxs-lookup"><span data-stu-id="3982b-152">Create Bins</span></span>](warehouse-how-to-create-individual-bins.md)  
[<span data-ttu-id="3982b-153">Lagerplatzarten einrichten</span><span class="sxs-lookup"><span data-stu-id="3982b-153">Set Up Bin Types</span></span>](warehouse-how-to-set-up-bin-types.md)  
[<span data-ttu-id="3982b-154">Lagerortverwaltung einrichten</span><span class="sxs-lookup"><span data-stu-id="3982b-154">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
<span data-ttu-id="3982b-155">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3982b-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="3982b-156">Funktionen, die angezeigt werden ändern</span><span class="sxs-lookup"><span data-stu-id="3982b-156">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="3982b-157">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="3982b-157">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]