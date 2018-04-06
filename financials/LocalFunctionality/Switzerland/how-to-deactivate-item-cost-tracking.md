---
title: Deaktivieren des Artikelpreistracking
description: "Wenn ein Artikel im Lager nicht nachverfolgt wird, müssen die Artikelpreise nicht nachverfolgt werden, und es muss kein Lagerposten erstellt werden."
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
ms.openlocfilehash: f094cc748d263c2ec2d1cfcc18c69b65029246b2
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="deactivate-item-cost-tracking"></a><span data-ttu-id="bb370-103">Deaktivieren des Artikelpreistrackings</span><span class="sxs-lookup"><span data-stu-id="bb370-103">Deactivate Item Cost Tracking</span></span>
<span data-ttu-id="bb370-104">Wenn ein Artikel im Lager nicht nachverfolgt wird, müssen die Artikelpreise nicht nachverfolgt werden, und es muss kein Lagerposten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bb370-104">When inventory is not tracked for an item, the item cost does not need to be tracked, and an item ledger entry does not need to be created.</span></span>  

<span data-ttu-id="bb370-105">Sie können das Artikelpreistracking für einen Artikel deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bb370-105">You can deactivate item cost tracking for an item.</span></span> <span data-ttu-id="bb370-106">Im Allgemeinen sollte das Artikelpreistracking für Verbrauchsartikel (z. B. Altpapierprodukte) und Dienste, die als Produkte gelten (z. B. feste Parkgebühren), deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="bb370-106">Generally, item cost tracking should be deactivated for consumable items, such as waste paper products and for services that are counted as items, such as flat rate parking fees.</span></span> <span data-ttu-id="bb370-107">Das Artikelpreistracking sollte für Artikel deaktiviert werden, bei denen die Verfolgung zu falschen Rückschlüssen führen würde.</span><span class="sxs-lookup"><span data-stu-id="bb370-107">Item cost tracking should be deactivated on items for which tracking could be misleading.</span></span> <span data-ttu-id="bb370-108">Für Artikel, für die das Artikelpreistracking deaktiviert wurde, sind folgende Funktionen bzw. Systeme nicht verfügbar: Reservierung, Verfügbarkeitsprüfung, Artikelverfolgung und Materialplanungssysteme.</span><span class="sxs-lookup"><span data-stu-id="bb370-108">Items for which item cost tracking has been deactivated are excluded from reservation, availability check, item tracking, and material planning systems.</span></span>  

## <a name="to-deactivate-item-cost-tracking"></a><span data-ttu-id="bb370-109">So deaktivieren Sie das Artikelpreistracking</span><span class="sxs-lookup"><span data-stu-id="bb370-109">To deactivate item cost tracking</span></span>  

1.  <span data-ttu-id="bb370-110">Wählen Sie ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="bb370-110">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bb370-111">Wählen Sie die entsprechende Elemente und wählen Sie dann die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="bb370-111">Select the required item, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="bb370-112">Aktivieren Sie auf dem Inforegister **Allgemein** das Kontrollkästchen **Keine Lagerführung**.</span><span class="sxs-lookup"><span data-stu-id="bb370-112">On the **General** FastTab, select the **No Stockkeeping** check box.</span></span>  

    <span data-ttu-id="bb370-113">Wenn eine Transaktion für diesen Artikel gebucht wird, wird kein Lagerposten erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb370-113">An item ledger entry will not be created when you post a transaction for this item.</span></span> <span data-ttu-id="bb370-114">Weitere Informationen erhalten Sie in der Tabelle "Lagerposten".</span><span class="sxs-lookup"><span data-stu-id="bb370-114">For more information, see the Item Ledger Entry table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="bb370-115">Das Kontrollkästchen **Keine Lagerführung** kann nicht für einen Artikel aktiviert werden, für den bereits Lagerposten gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="bb370-115">You cannot select the **No Stockkeeping** check box on an item for which item ledger entries have already been posted.</span></span>  

4.  <span data-ttu-id="bb370-116">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="bb370-116">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bb370-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb370-117">See Also</span></span>  
 <span data-ttu-id="bb370-118">[Lagerverwaltung (Schweiz)](swiss-inventory-management.md) </span><span class="sxs-lookup"><span data-stu-id="bb370-118">[Swiss Inventory Management](swiss-inventory-management.md) </span></span>  
 [<span data-ttu-id="bb370-119">Sperren von Lagerartikeln für Verkäufe oder Einkäufe</span><span class="sxs-lookup"><span data-stu-id="bb370-119">Block Inventory Items for Sales or Purchases</span></span>](how-to-block-inventory-items-for-sales-or-purchases.md)

