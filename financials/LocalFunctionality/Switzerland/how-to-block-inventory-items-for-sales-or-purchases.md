---
title: "Sperren von Lagerartikeln für Verkäufe oder Einkäufe"
description: "Ein Artikel kann als für Verkäufe, Einkäufe oder alle Verwendungszwecke gesperrt gekennzeichnet werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/02/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: 4a64a29e005713b3aa8d839bdb21cff3034edc81
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="block-inventory-items-for-sales-or-purchases"></a><span data-ttu-id="eb593-103">Sperren von Lagerartikeln für Verkäufe oder Einkäufe</span><span class="sxs-lookup"><span data-stu-id="eb593-103">Block Inventory Items for Sales or Purchases</span></span>
<span data-ttu-id="eb593-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kann ein Artikel als für Verkäufe, Einkäufe oder alle Verwendungszwecke gesperrt gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="eb593-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], an item can be marked as blocked for sales, blocked for purchase, or blocked for all purposes.</span></span>  

<span data-ttu-id="eb593-105">In der folgenden Tabelle wird veranschaulicht, was beim Sperren von Artikeln passiert.</span><span class="sxs-lookup"><span data-stu-id="eb593-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="eb593-106">Artikel gekennzeichnet als</span><span class="sxs-lookup"><span data-stu-id="eb593-106">Item marked as</span></span>|<span data-ttu-id="eb593-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="eb593-107">Result</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="eb593-108">**Verkauf gesperrt**</span><span class="sxs-lookup"><span data-stu-id="eb593-108">**Sale blocked**</span></span>|<span data-ttu-id="eb593-109">Der Artikel kann nicht in einem Verkaufsbeleg oder einem Erf.-Journal für Verkaufsartikel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb593-109">You cannot use the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="eb593-110">**Einkauf gesperrt**</span><span class="sxs-lookup"><span data-stu-id="eb593-110">**Purchase blocked**</span></span>|<span data-ttu-id="eb593-111">Der Artikel kann nicht in einem Einkaufsbeleg, einem Erf.-Journal für Einkaufsartikel oder in Einkaufsplanungsprozessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb593-111">You cannot use the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="eb593-112">**Gesperrt**</span><span class="sxs-lookup"><span data-stu-id="eb593-112">**Blocked**</span></span>|<span data-ttu-id="eb593-113">Der Artikel kann für keine Artikeltransaktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb593-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="eb593-114">Weitere Informationen zum Sperren eines Artikels für alle Zwecke erhalten Sie unter "Artikelkarte".</span><span class="sxs-lookup"><span data-stu-id="eb593-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-inventory-items-for-sales"></a><span data-ttu-id="eb593-115">So sperren Sie Lagerartikel für den Verkauf</span><span class="sxs-lookup"><span data-stu-id="eb593-115">To block inventory items for sales</span></span>  

1.  <span data-ttu-id="eb593-116">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="eb593-116">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="eb593-117">Wählen Sie den Artikel, den Sie sperren möchten, und wählen Sie dann die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="eb593-117">Select the item that you want to block, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="eb593-118">Aktivieren Sie auf dem Inforegister **Preise und Verkauf** das Kontrollkästchen **Verkauf gesperrt**, um den ausgewählten Artikel für Verkaufstransaktionen zu sperren.</span><span class="sxs-lookup"><span data-stu-id="eb593-118">To block the selected item for sales transactions, on the **Prices & Sales** FastTab, select the **Sale blocked** check box.</span></span>  
4.  <span data-ttu-id="eb593-119">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="eb593-119">Choose the **OK** button.</span></span>  

## <a name="to-block-inventory-items-for-purchase"></a><span data-ttu-id="eb593-120">So sperren Sie Lagerartikel für den Einkauf</span><span class="sxs-lookup"><span data-stu-id="eb593-120">To block inventory items for purchase</span></span>  

1.  <span data-ttu-id="eb593-121">Wählen Sie ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="eb593-121">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="eb593-122">Wählen Sie den Artikel, den Sie sperren möchten, und wählen Sie dann die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="eb593-122">Select the item that you want to block, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="eb593-123">Aktivieren Sie auf dem Inforegister **Beschaffung** das Kontrollkästchen **Einkauf gesperrt**, um den ausgewählten Artikel für Einkaufstransaktionen zu sperren.</span><span class="sxs-lookup"><span data-stu-id="eb593-123">To block an item for purchase transactions, on the **Replenishment** FastTab, select the **Purchase blocked** check box.</span></span>  
4.  <span data-ttu-id="eb593-124">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="eb593-124">Choose the **OK** button.</span></span>  

<span data-ttu-id="eb593-125">Für folgende Aktionen erhalten Sie eine Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="eb593-125">You will receive an error message if you try to do the following:</span></span>  

- <span data-ttu-id="eb593-126">Eingeben von Verkaufs- und Einkaufszeilen in Verkaufs- bzw. Einkaufsbelege für gesperrte Artikel.</span><span class="sxs-lookup"><span data-stu-id="eb593-126">Enter sales lines and purchase lines in sales documents and purchase documents for blocked items.</span></span> <span data-ttu-id="eb593-127">Weitere Informationen erhalten Sie in den Tabellen "Verkaufszeile" und "Einkaufszeile".</span><span class="sxs-lookup"><span data-stu-id="eb593-127">For more information, see the Sales Line table and the Purchase Line table.</span></span>  
- <span data-ttu-id="eb593-128">Erstellen von Artikel-Erf.-Journalen für gesperrte Artikel.</span><span class="sxs-lookup"><span data-stu-id="eb593-128">Create new lines in an item journal for blocked items.</span></span> <span data-ttu-id="eb593-129">Weitere Informationen erhalten Sie im Fenster "Artikel Erf.-Journal".</span><span class="sxs-lookup"><span data-stu-id="eb593-129">For more information, see the Item Journal window.</span></span>  
- <span data-ttu-id="eb593-130">Buchen von Artikeltransaktionen für gesperrte Artikel.</span><span class="sxs-lookup"><span data-stu-id="eb593-130">Post item transactions for blocked items.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eb593-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb593-131">See Also</span></span>  
 <span data-ttu-id="eb593-132">[Lagerverwaltung (Schweiz)](swiss-inventory-management.md) </span><span class="sxs-lookup"><span data-stu-id="eb593-132">[Swiss Inventory Management](swiss-inventory-management.md) </span></span>  
 <span data-ttu-id="eb593-133">[Kopieren von vorhandenen Elementen in neue Elemente](how-to-copy-existing-items-to-new-items.md) </span><span class="sxs-lookup"><span data-stu-id="eb593-133">[Copy Existing Items to New Items](how-to-copy-existing-items-to-new-items.md) </span></span>  
 [<span data-ttu-id="eb593-134">Deaktivieren des Artikelpreistrackings</span><span class="sxs-lookup"><span data-stu-id="eb593-134">Deactivate Item Cost Tracking</span></span>](how-to-deactivate-item-cost-tracking.md)

