---
title: 'Exemplarische Vorgehensweise: Eingang und Einlagerung bei Basis-Lagerkonfigurationen | Microsoft Docs'
description: In Business Central können die eingehenden Prozesse für das Empfangen und Einlagern auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2020
ms.author: edupont
ms.openlocfilehash: 2b7a0c52417e9eff00ac692788b9eae073186e6c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786735"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="5212e-103">Exemplarische Vorgehensweise: Eingang und Einlagerung in Basis-Lagerkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="5212e-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

<span data-ttu-id="5212e-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)] können die eingehenden Prozesse für das Empfangen und Einlagern auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5212e-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="5212e-105">Art</span><span class="sxs-lookup"><span data-stu-id="5212e-105">Method</span></span>|<span data-ttu-id="5212e-106">Eingangsprozess</span><span class="sxs-lookup"><span data-stu-id="5212e-106">Inbound process</span></span>|<span data-ttu-id="5212e-107">Lagerplätze</span><span class="sxs-lookup"><span data-stu-id="5212e-107">Bins</span></span>|<span data-ttu-id="5212e-108">Geb. Umlag.-Eingänge</span><span class="sxs-lookup"><span data-stu-id="5212e-108">Receipts</span></span>|<span data-ttu-id="5212e-109">Einlagerungen</span><span class="sxs-lookup"><span data-stu-id="5212e-109">Put-aways</span></span>|<span data-ttu-id="5212e-110">Komplexitätsebene anzeigen (siehe [Designdetails: Lagerhaus-Einrichtung](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="5212e-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="5212e-111">A</span><span class="sxs-lookup"><span data-stu-id="5212e-111">A</span></span>|<span data-ttu-id="5212e-112">Posteinlieferungsschein und die Einlagerung der Auftragszeile</span><span class="sxs-lookup"><span data-stu-id="5212e-112">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="5212e-113">X</span><span class="sxs-lookup"><span data-stu-id="5212e-113">X</span></span>|||<span data-ttu-id="5212e-114">2</span><span class="sxs-lookup"><span data-stu-id="5212e-114">2</span></span>|  
|<span data-ttu-id="5212e-115">B</span><span class="sxs-lookup"><span data-stu-id="5212e-115">B</span></span>|<span data-ttu-id="5212e-116">Posteinlieferungsschein und Einlagerung aus dem Beleg "Lagereinlagerung"</span><span class="sxs-lookup"><span data-stu-id="5212e-116">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="5212e-117">X</span><span class="sxs-lookup"><span data-stu-id="5212e-117">X</span></span>|<span data-ttu-id="5212e-118">3</span><span class="sxs-lookup"><span data-stu-id="5212e-118">3</span></span>|  
|<span data-ttu-id="5212e-119">L</span><span class="sxs-lookup"><span data-stu-id="5212e-119">C</span></span>|<span data-ttu-id="5212e-120">Posteinlieferungsschein und Einlagerung aus einem Wareneingangsbeleg</span><span class="sxs-lookup"><span data-stu-id="5212e-120">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="5212e-121">X</span><span class="sxs-lookup"><span data-stu-id="5212e-121">X</span></span>||<span data-ttu-id="5212e-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="5212e-122">4/5/6</span></span>|  
|<span data-ttu-id="5212e-123">T</span><span class="sxs-lookup"><span data-stu-id="5212e-123">D</span></span>|<span data-ttu-id="5212e-124">Posteinlieferungsschein aus einem Wareneingangsbeleg und Posteinlagerung aus einem Einlagerungsbeleg</span><span class="sxs-lookup"><span data-stu-id="5212e-124">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="5212e-125">X</span><span class="sxs-lookup"><span data-stu-id="5212e-125">X</span></span>|<span data-ttu-id="5212e-126">X</span><span class="sxs-lookup"><span data-stu-id="5212e-126">X</span></span>|<span data-ttu-id="5212e-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="5212e-127">4/5/6</span></span>|  

<span data-ttu-id="5212e-128">Weitere Informationen finden Sie unter [Designdetails: Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="5212e-128">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="5212e-129">In der folgenden Vorgehensweise wird Methode B in der vorhergegangenen Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5212e-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="5212e-130">Informationen zu dieser exemplarischen Vorgehensweise</span><span class="sxs-lookup"><span data-stu-id="5212e-130">About This Walkthrough</span></span>  
<span data-ttu-id="5212e-131">Bei Basis-Lagerkonfigurationen gilt Folgendes: Wenn ein Lagerort so eingerichtet wurde, dass die Bearbeitung der Einlagerung erforderlich ist, die des Wareneingangs jedoch nicht erforderlich ist, verwenden Sie die Seite **Lagereinlagerung**, um Einlagerungs- und Wareneingangsinformationen für Ihre Herkunftsbelege zu erfassen und zu buchen.</span><span class="sxs-lookup"><span data-stu-id="5212e-131">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** page to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="5212e-132">Der eingehende Herkunftsbeleg kann eine Einkaufsbestellung, eine Verkaufsreklamation, ein eingehender Umlagerungsauftrag oder ein Fertigungsauftrag sein, dessen Endprodukt zur Einlagerung bereitsteht.</span><span class="sxs-lookup"><span data-stu-id="5212e-132">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="5212e-133">Obwohl die Einstellungen **Kommissionierung erforderlich** und **Einlagerung erforderlich** genannt werden, können Sie weiterhin Wareneingänge und Lieferungen direkt aus den Quellgeschäftsunterlagen an Lagerorten, in denen Sie diese Kontrollkästchen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5212e-133">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="5212e-134">In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert.</span><span class="sxs-lookup"><span data-stu-id="5212e-134">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="5212e-135">Einrichtung des SILBERNEN Lagerorts für Einlagerungen.</span><span class="sxs-lookup"><span data-stu-id="5212e-135">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="5212e-136">Einrichtung des SILBERNEN Lagerorts für Lagerplatzbehandlung.</span><span class="sxs-lookup"><span data-stu-id="5212e-136">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="5212e-137">Definieren eines Standardlagerplatzes für Artikel LS-81.</span><span class="sxs-lookup"><span data-stu-id="5212e-137">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="5212e-138">(LS-75 ist bereits in CRONUS eingerichtet.)</span><span class="sxs-lookup"><span data-stu-id="5212e-138">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="5212e-139">Erstellen einer Bestellung für den Kreditor 10000 für 40 Lautsprecher.</span><span class="sxs-lookup"><span data-stu-id="5212e-139">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="5212e-140">Überprüfen, dass Lagerplätze der Einlagerung durch Einrichtung voreingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5212e-140">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="5212e-141">Freigeben der Bestellung für Lagerdurchlaufzeit.</span><span class="sxs-lookup"><span data-stu-id="5212e-141">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="5212e-142">Erstellen einer Lagereinlagerung basierend auf einem freigegebenen Herkunftsbeleg.</span><span class="sxs-lookup"><span data-stu-id="5212e-142">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="5212e-143">Überprüfen, dass Lagerplätze der Einlagerung von der Einkaufsbestellung übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="5212e-143">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="5212e-144">Erfassen der Lagerplatzumlagerung in das Lager und gleichzeitig Buchen der Einkaufslieferung für die ursprüngliche Einkaufsbestellung.</span><span class="sxs-lookup"><span data-stu-id="5212e-144">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="5212e-145">Rollen</span><span class="sxs-lookup"><span data-stu-id="5212e-145">Roles</span></span>  
<span data-ttu-id="5212e-146">Die Aufgaben in dieser Demonstration werden von den folgenden Benutzerrollen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="5212e-146">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="5212e-147">Lagerortleiter</span><span class="sxs-lookup"><span data-stu-id="5212e-147">Warehouse Manager</span></span>  
-   <span data-ttu-id="5212e-148">Einkäufer</span><span class="sxs-lookup"><span data-stu-id="5212e-148">Purchasing Agent</span></span>  
-   <span data-ttu-id="5212e-149">Lagermitarbeiter</span><span class="sxs-lookup"><span data-stu-id="5212e-149">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="5212e-150">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5212e-150">Prerequisites</span></span>  
<span data-ttu-id="5212e-151">Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="5212e-151">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="5212e-152">CRONUS AG installieren.</span><span class="sxs-lookup"><span data-stu-id="5212e-152">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="5212e-153">Machen Sie sich anhand der nachfolgenden Schritte zu einem Lagermitarbeiter am Standort SILVER:</span><span class="sxs-lookup"><span data-stu-id="5212e-153">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="5212e-154">Wählen Sie die ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion") Symbol, geben Sie **Lagerort-Mitarbeiter** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="5212e-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="5212e-155">Wählen Sie das Feld **Benutzer-ID** aus, und wählen Sie Ihr eigenes Benutzerkonto auf der Seite **Benutzer** aus.</span><span class="sxs-lookup"><span data-stu-id="5212e-155">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
    3.  <span data-ttu-id="5212e-156">Geben Sie im Feld **Lagerortcode** SILVER ein.</span><span class="sxs-lookup"><span data-stu-id="5212e-156">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="5212e-157">Wählen Sie das Feld **Standard** aus.</span><span class="sxs-lookup"><span data-stu-id="5212e-157">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="5212e-158">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5212e-158">Story</span></span>  
<span data-ttu-id="5212e-159">Ellen, die Einkäuferin bei der CRONUS AG ist, erstellt eine Bestellung für 10 Einheiten des Artikels LS-75 und 30 Einheiten des Artikels LS-81 von dem Kreditor 10000, um zum SILVER-Lagerhaus geliefert zu werden.</span><span class="sxs-lookup"><span data-stu-id="5212e-159">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="5212e-160">Wenn die Lieferung im Lager eingeht, lagert John, der Lagermitarbeiter, die Artikel in die Standardlagerplätze ein, die für die Artikel eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="5212e-160">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="5212e-161">Wenn John Einlagerungen bucht, werden die Artikel gebucht als im Lager erhalten und verfügbar zum Verkauf oder anderen Bedarf.</span><span class="sxs-lookup"><span data-stu-id="5212e-161">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="5212e-162">Einrichten des Lagerorts</span><span class="sxs-lookup"><span data-stu-id="5212e-162">Setting up the Location</span></span>  
 <span data-ttu-id="5212e-163">Das Einrichten der Seite **Standortkarte** definiert die Warenflüsse des Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="5212e-163">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="5212e-164">So richten Sie den Lagerort ein</span><span class="sxs-lookup"><span data-stu-id="5212e-164">To set up the location</span></span>  

1.  <span data-ttu-id="5212e-165">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Lagerorte** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="5212e-165">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5212e-166">Öffnen Sie die SILBERNE Lagerortkarte.</span><span class="sxs-lookup"><span data-stu-id="5212e-166">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="5212e-167">Aktivieren Sie das Kontrollkästchen **Einlagerung erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5212e-167">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="5212e-168">Fahren Sie fort, um einen Vorgabelagerplatz für die beiden Artikelnummern einzurichten, um zu steuern, wo sie eingelagert werden.</span><span class="sxs-lookup"><span data-stu-id="5212e-168">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="5212e-169">Wählen Sie die Aktion **Lagerplätze** aus.</span><span class="sxs-lookup"><span data-stu-id="5212e-169">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="5212e-170">Wählen Sie die erste Zeile, für den Lagerplatz S-01-0001, und wählen die **Inhalt** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="5212e-170">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="5212e-171">Beachten Sie auf der Seite **Lagerplatzinhalt**, dass der Artikel LS-75 bereits als Inhalt im Lagerplatz S-01-0001 eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="5212e-171">Notice on the **Bin Content** page that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="5212e-172">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5212e-172">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="5212e-173">Wählen Sie die Felder **Fest** und **Standard** .</span><span class="sxs-lookup"><span data-stu-id="5212e-173">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="5212e-174">Geben Sie im Feld **Belegnr.** den Wert LS-81 ein.</span><span class="sxs-lookup"><span data-stu-id="5212e-174">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="5212e-175">Erstellen der Bestellung</span><span class="sxs-lookup"><span data-stu-id="5212e-175">Creating the Purchase Order</span></span>  
<span data-ttu-id="5212e-176">Bestellungen sind die häufigste Art des eingehenden Herkunftsbelegs.</span><span class="sxs-lookup"><span data-stu-id="5212e-176">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="5212e-177">Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="5212e-177">To create the purchase order</span></span>  

1.  <span data-ttu-id="5212e-178">Wählen Sie die ![Glühbirne, die das Tell Me Feature öffnet](media/ui-search/search_small.png "Tell Me-Funktion") Symbol, geben Sie **Bestellungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="5212e-178">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5212e-179">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5212e-179">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="5212e-180">Erstellen Sie eine Bestellung für den Kreditor 10000 auf das Arbeitsdatum (23. Januar) mit den folgenden Einkaufszeilen.</span><span class="sxs-lookup"><span data-stu-id="5212e-180">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="5212e-181">Artikel</span><span class="sxs-lookup"><span data-stu-id="5212e-181">Item</span></span>|<span data-ttu-id="5212e-182">Lagerortcode</span><span class="sxs-lookup"><span data-stu-id="5212e-182">Location code</span></span>|<span data-ttu-id="5212e-183">Lagerplatzcode</span><span class="sxs-lookup"><span data-stu-id="5212e-183">Bin code</span></span>|<span data-ttu-id="5212e-184">Menge</span><span class="sxs-lookup"><span data-stu-id="5212e-184">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="5212e-185">LS_75</span><span class="sxs-lookup"><span data-stu-id="5212e-185">LS_75</span></span>|<span data-ttu-id="5212e-186">SILBER</span><span class="sxs-lookup"><span data-stu-id="5212e-186">SILVER</span></span>|<span data-ttu-id="5212e-187">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="5212e-187">S-01-0001</span></span>|<span data-ttu-id="5212e-188">10</span><span class="sxs-lookup"><span data-stu-id="5212e-188">10</span></span>|  
    |<span data-ttu-id="5212e-189">LS-81</span><span class="sxs-lookup"><span data-stu-id="5212e-189">LS-81</span></span>|<span data-ttu-id="5212e-190">SILBER</span><span class="sxs-lookup"><span data-stu-id="5212e-190">SILVER</span></span>|<span data-ttu-id="5212e-191">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="5212e-191">S-01-0001</span></span>|<span data-ttu-id="5212e-192">30</span><span class="sxs-lookup"><span data-stu-id="5212e-192">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="5212e-193">Der Lagerplatzcode wird automatisch gemäss der Einrichtung eingegeben, dem Sie im "Aufstellung Lagerort" Abschnitt zulassen.</span><span class="sxs-lookup"><span data-stu-id="5212e-193">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="5212e-194">Fahren Sie fort, das Lager zu informieren, dass die Einkaufsbestellung in Lagerdurchlaufzeit bereit ist, wenn die Lieferung eingeht.</span><span class="sxs-lookup"><span data-stu-id="5212e-194">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="5212e-195">Wählen Sie die Aktion **Freigabe** aus.</span><span class="sxs-lookup"><span data-stu-id="5212e-195">Choose the **Release** action.</span></span>  

    <span data-ttu-id="5212e-196">Der Warenausgang von Lautsprechern vom Lieferanten 10000 ist im SILBERNEN Lager eingetroffen, und John fährt fort, um sie einzulagern.</span><span class="sxs-lookup"><span data-stu-id="5212e-196">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="5212e-197">Erhalten und Einlagern der Artikel</span><span class="sxs-lookup"><span data-stu-id="5212e-197">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="5212e-198">Auf der Seite **Lagerkommissionierung** können Sie alle eingehenden Lageraktivitäten für einen bestimmten Herkunftsbeleg, wie einen Einkauf, verwalten.</span><span class="sxs-lookup"><span data-stu-id="5212e-198">On the **Inventory Put-away** page, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="5212e-199">Artikel erhalten und einlagern</span><span class="sxs-lookup"><span data-stu-id="5212e-199">To receive and put the items away</span></span>  

1.  <span data-ttu-id="5212e-200">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Einlagerungslager** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="5212e-200">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5212e-201">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5212e-201">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="5212e-202">Wählen Sie das Feld **Herkunftsbeleg** , und wählen Sie **Einkaufsauftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="5212e-202">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="5212e-203">Wählen Sie das Feld **Herkunftsnr.** aus, wählen Sie die Zeile für den Einkauf von Kreditor 10000 aus, und wählen Sie dann die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="5212e-203">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="5212e-204">Alternativ können Sie auch die Aktion **Quellbeleg holen** wählen und dann die Bestellung auswählen.</span><span class="sxs-lookup"><span data-stu-id="5212e-204">Alternatively, choose the **Get Source Document** action, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="5212e-205">Wählen Sie die **Die zu verarbeitende Menge automatisch ausfüllen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="5212e-205">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="5212e-206">Alternativ im Feld **Menge zu verarbeiten** geben Sie 10 und 30 jeweils auf den zwei Lagerkommissionierzeilen ein.</span><span class="sxs-lookup"><span data-stu-id="5212e-206">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="5212e-207">Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Lieferung und Rechnung**, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5212e-207">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="5212e-208">Die 40 Lautsprecher werden nun erfasst, wie von den Lagereinlagerungsplätzen S-01-0001 kommissioniert, und ein positiver Lagerposten wird, die gebuchte Einkaufslieferung reflektierend, erstellt.</span><span class="sxs-lookup"><span data-stu-id="5212e-208">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5212e-209">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5212e-209">See Also</span></span>  
 <span data-ttu-id="5212e-210">[Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="5212e-210">[Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="5212e-211">[Einrichten von Basislagern mit Vorgangsbereichen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="5212e-211">[Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="5212e-212">[So verschieben Sie Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="5212e-212">[Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="5212e-213">[Kommissionierung für die Produktion oder Montage](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="5212e-213">[Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="5212e-214">[Ad-hoc-Umlagerung von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="5212e-214">[Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="5212e-215">[Designdetails: Eingehender Lagerfluss](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="5212e-215">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="5212e-216">Exemplarische Vorgehensweisen für Geschäftsprozesse</span><span class="sxs-lookup"><span data-stu-id="5212e-216">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="5212e-217">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5212e-217">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
