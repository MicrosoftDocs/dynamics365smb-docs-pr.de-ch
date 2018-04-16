---
title: "Erstellen Sie Neuwert-Posten für Artikel im Lagerbestand| Microsoft Docs"
description: Beschreiben Sie, wie der Wert eines oder mehrerer Artikel im Lager abgeschrieben oder neu bewertet wird, indem Sie den aktuellen, berechneten Wert buchen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: 6307db87dd8c637f45697735fb223c4db5e073a2
ms.contentlocale: de-ch
ms.lasthandoff: 04/16/2018

---
# <a name="revalue-inventory"></a><span data-ttu-id="925bd-103">Neubewerten von Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="925bd-103">Revalue Inventory</span></span>
<span data-ttu-id="925bd-104">Wenn Sie den Lagerwert eines Artikels oder den eines bestimmten Lagerpostens nach oben oder unten verändern möchten, müssen Sie das Neubewertungs Erf.-Journal verwenden.</span><span class="sxs-lookup"><span data-stu-id="925bd-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="925bd-105">Neubewerten von Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="925bd-105">To revalue inventory</span></span>
1. <span data-ttu-id="925bd-106">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Neubewertung Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="925bd-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="925bd-107">Wählen Sie die Aktion **Lagerwert berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="925bd-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="925bd-108">Füllen Sie im Fenster **Lagerwert berechnen** die Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="925bd-108">In the **Calculate Inventory Value** window, fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="925bd-109">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="925bd-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="925bd-110">In jeder Zeile im Fenster **Neubewertungs-Blatt-Blatt** im Feld **Einheitskosten (neu bewertet)** geben Sie den neuen Einstandspreis ein.</span><span class="sxs-lookup"><span data-stu-id="925bd-110">On each line in the **Revaluation Journal** window, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="925bd-111">Oder geben Sie den Gesamtbetrag im Feld **Lagerwert (neu bewertet)** ein.</span><span class="sxs-lookup"><span data-stu-id="925bd-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="925bd-112">Die entsprechenden Felder werden automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="925bd-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="925bd-113">Beachten Sie, dass das Feld **Betrag** die tatsächliche Änderung des Lagerwertes für den ausgewählten Lagerposten zeigt.</span><span class="sxs-lookup"><span data-stu-id="925bd-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="925bd-114">Es berechnet die Differenz zwischen den Feldern **Lagerwert (berechnet)** und **Lagerwert (neu bewertet)**.</span><span class="sxs-lookup"><span data-stu-id="925bd-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="925bd-115">Wenn Sie das Einlagern der Artikel abgeschlossen haben, wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="925bd-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="925bd-116">Neue Wertposten werden nun erstellt, um die Neubewertungen abzubilden, die Sie gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="925bd-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="925bd-117">Sie können die neuen Werte in der entsprechenden Artikelkarten sehen.</span><span class="sxs-lookup"><span data-stu-id="925bd-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="925bd-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="925bd-118">See Also</span></span>
[<span data-ttu-id="925bd-119">Designdetails: Neubewertung</span><span class="sxs-lookup"><span data-stu-id="925bd-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="925bd-120">Lagerbest.</span><span class="sxs-lookup"><span data-stu-id="925bd-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="925bd-121">Verkauf</span><span class="sxs-lookup"><span data-stu-id="925bd-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="925bd-122">Einkauf</span><span class="sxs-lookup"><span data-stu-id="925bd-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="925bd-123">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="925bd-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

