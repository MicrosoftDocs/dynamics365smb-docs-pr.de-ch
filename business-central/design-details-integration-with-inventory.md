---
title: 'Designdetails: Integration mit dem Lagerbestand | Microsoft Docs'
description: Der Logistik-Anwendungsbereich und der Lager-Anwendungsbereich interagieren miteinander im physischen Bestand und in der Bestands- und Lageranpassung.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: bbc9c0e55041f4584ae7609f727179737adaa041
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185362"
---
# <a name="design-details-integration-with-inventory"></a><span data-ttu-id="6c4d9-103">Designdetails: Integration mit dem Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="6c4d9-103">Design Details: Integration with Inventory</span></span>
<span data-ttu-id="6c4d9-104">Der Logistik-Anwendungsbereich und der Lager-Anwendungsbereich interagieren miteinander im physischen Bestand und in der Bestands- und Lageranpassung.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-104">The Warehouse Management application area and the Inventory application area interact with one another in physical inventory and in inventory or warehouse adjustment.</span></span>  
  
## <a name="physical-inventory"></a><span data-ttu-id="6c4d9-105">Inventur</span><span class="sxs-lookup"><span data-stu-id="6c4d9-105">Physical Inventory</span></span>  
 <span data-ttu-id="6c4d9-106">Die **Logistik-Inventur-Erf.-Journal**-Seite wird mit der **Inventur Erf.-Journal**-Seite für alle erweiterten Lagerorte verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-106">The **Whse. Phys. Inventory Journal** page is used with the **Phys. Inventory Journal** page for all advanced warehouse locations.</span></span> <span data-ttu-id="6c4d9-107">Der Bestand auf Lagerplatzebene wird berechnet, und eine gedruckte Liste wird für den Lagermitarbeiter bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-107">The inventory on bin level is calculated, and a printed list is provided for the warehouse employee.</span></span> <span data-ttu-id="6c4d9-108">Die Liste zeigt, welche Artikel an welchen Lagerplätzen gezählt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-108">The list shows which items in which bins must be counted.</span></span>  
  
 <span data-ttu-id="6c4d9-109">Der Lagermitarbeiter gibt die gezählte Menge auf der**Logistik-Inventur-Erf.-Journal** Seite ein und bucht das Erf.-Journal.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-109">The warehouse employee enters the counted quantity on the **Whse. Phys. Inventory Journal** page and then posts the journal.</span></span>  
  
 <span data-ttu-id="6c4d9-110">Wenn die gezählte Menge grösser als die Menge auf der Erf.-Journalzeile ist, wird eine Umlagerung für diese Differenz aus dem Standard-Ausgleichslagerplatz zum gezählten Lagerplatz gebucht.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-110">If the counted quantity is greater than the quantity on the journal line, a movement is posted for this difference from the default adjustment bin to the counted bin.</span></span> <span data-ttu-id="6c4d9-111">Dieses erhöht die Menge im gezählten Lagerplatz und vermindert die Menge im Standard-Ausgleichslagerplatz.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-111">This increases the quantity in the counted bin and decreases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="6c4d9-112">Wenn die gezählte Menge geringer als die Menge auf der Erf.-Journalzeile ist, wird eine Umlagerung für diese Differenz aus dem gezählten Lagerplatz zum Standard-Ausgleichslagerplatz gebucht.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-112">If the quantity counted is less than the quantity on the journal line, a movement for this difference is posted from the counted bin to the default adjustment bin.</span></span> <span data-ttu-id="6c4d9-113">Dieses reduziert die Menge im gezählten Lagerplatz und erhöht die Menge im Standard-Ausgleichslagerplatz.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-113">This decreases the quantity in the counted bin and increases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="6c4d9-114">In erweiterten Lagerfunktionskonfigurationen wird der Wert im Feld **Menge (berechnet)** aus den Lagerposten einbezogen und der Wert im Feld **Menge (Phys. Lagerbestand)** aus den Lagerplatzposten ohne Ausgleichslagerplatzinhalt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-114">In advanced warehouse configurations, the value in the **Quantity (Calculated)** field is retrieved from item ledger entries and the value in the **Quantity (Phys. Inventory)** field is retrieved from warehouse entries, excluding the adjustment bin content.</span></span> <span data-ttu-id="6c4d9-115">Das Feld **Menge** gibt die Differenz zwischen den ersten beiden Feldern an, die dem Inhalt des Regulierungslagerplatzes entsprechen sollte.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-115">The **Quantity** field specifies the difference between the first two fields, which should be equal to the contents of the adjustment bin.</span></span>  
  
 <span data-ttu-id="6c4d9-116">Wenn Sie das Inventur Erf.-Journal buchen, werden der Lagerbestand und der Ausgleichslagerplatz aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-116">When you post the physical inventory journal, the inventory and the default adjustment bin are updated.</span></span>  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a><span data-ttu-id="6c4d9-117">Lagerplatz-Ausgleich mit dem Artikelposten</span><span class="sxs-lookup"><span data-stu-id="6c4d9-117">Warehouse Adjustments to the Item Ledger</span></span>  
 <span data-ttu-id="6c4d9-118">Sie verwenden die Seite **Artikel Erf.-Journal** und die Funktion **Ausgleich berechnen**, um den Lagerbestand im Artikelposten in Übereinstimmung mit einem Ausgleich anzupassen, der für die Artikelmenge in einem Lagerplatz vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-118">You use the **Item Journal** page and the **Calculate Whse. Adjustment** function to adjust inventory on the item ledger in accordance with an adjustment that has been made to the item quantity in a warehouse bin.</span></span> <span data-ttu-id="6c4d9-119">Um eine Verbindung zwischen den Lagerbestand und der Logistik zu erstellen, müssen Sie einen Vorgabe-Ausgleichslagerplatz pro Lagerort festlegen.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-119">To create a link between the inventory and the warehouse, you must define a default adjustment bin per location.</span></span>  
  
 <span data-ttu-id="6c4d9-120">Der Standard-Regulierungslagerplatz registriert Artikel im Lager, wenn Sie einen Zugang für den Bestand buchen.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-120">The default adjustment bin registers items in the warehouse when you post an increase for the inventory.</span></span> <span data-ttu-id="6c4d9-121">Wenn Sie jedoch einen Lagerabgang buchen, wird die Menge am Lagerplatz ebenfalls verringert.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-121">However, if you post a decrease, the quantity on the default bin is also decreased.</span></span> <span data-ttu-id="6c4d9-122">In beiden Fällen werden Lagerposten und Lagerposten erstellt.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-122">In both cases, item ledger entries and warehouse entries are created.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="6c4d9-123">Der Ausgleichslagerplatz ist nicht in der Verfügbarkeitsberechnung enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-123">The adjustment bin is not included in the availability calculation.</span></span>  
  
 <span data-ttu-id="6c4d9-124">Wenn Sie den Lagerplatzinhalt anpassen wollen, können Sie das Logistik Artikel-Erf.-Journal verwenden, von dem Sie die Artikelnummer, den Zonencode, den Lagerplatzcode und die Menge angeben können, die Sie anpassen möchten.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-124">If you want to adjust the bin content, you can use the warehouse item journal, from which you can enter the item number, zone code, bin code, and quantity that you want to adjust.</span></span>  
  
 <span data-ttu-id="6c4d9-125">Wenn Sie eine positive Menge eingeben und die Zeile buchen, wird der Bestand an dem Lagerplatz erhöht, und die Menge des Standard-Ausgleichslagerplatzes wird entsprechend vermindert.</span><span class="sxs-lookup"><span data-stu-id="6c4d9-125">If you enter a positive quantity and post the line, then the inventory stored in the bin increases, and the quantity of the default adjustment bin decreases correspondingly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c4d9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c4d9-126">See Also</span></span>  
 <span data-ttu-id="6c4d9-127">[Designdetails: Logistik](design-details-warehouse-management.md) </span><span class="sxs-lookup"><span data-stu-id="6c4d9-127">[Design Details: Warehouse Management](design-details-warehouse-management.md) </span></span>  
 [<span data-ttu-id="6c4d9-128">Designdetails: Verfügbarkeit im Lager</span><span class="sxs-lookup"><span data-stu-id="6c4d9-128">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)