---
title: Designdetails - Bestandberioden | Microsoft Docs
description: "Rückdatierte Transaktions- oder Kostenregulierungen beeinflussen häufig Salden und Bestandsbewertungen für Buchhaltungsperioden, die als geschlossen gelten. Dies kann nachteilige Auswirkungen auf eine genaue Berichterstellung haben, insbesondere innerhalb von weltweiten Unternehmen. Die Funktion „Bestandsperioden“ kann verwendet werden, um solche Probleme zu vermeiden, indem Bestandsperioden geöffnet oder geschlossen werden, um die Buchung in einer bestimmten Periode zu beschränken."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 742891cc8037696748b7beb459cc877ea482e2a1
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-inventory-periods"></a><span data-ttu-id="7bc0b-105">Designdetails: Bestandsperioden</span><span class="sxs-lookup"><span data-stu-id="7bc0b-105">Design Details: Inventory Periods</span></span>
<span data-ttu-id="7bc0b-106">Rückdatierte Transaktions- oder Kostenregulierungen beeinflussen häufig Salden und Bestandsbewertungen für Buchhaltungsperioden, die als geschlossen gelten.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-106">Backdated transactions or cost adjustments often affect balances and stock valuations for accounting periods that may be considered closed.</span></span> <span data-ttu-id="7bc0b-107">Dies kann nachteilige Auswirkungen auf eine genaue Berichterstellung haben, insbesondere innerhalb von weltweiten Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-107">This can have adverse effects on accurate reporting, especially within global corporations.</span></span> <span data-ttu-id="7bc0b-108">Die Funktion „Bestandsperioden“ kann verwendet werden, um solche Probleme zu vermeiden, indem Bestandsperioden geöffnet oder geschlossen werden, um die Buchung in einer bestimmten Periode zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-108">The Inventory Periods feature can be used to avoid such problems by opening or closing inventory periods to limit posting in a set period of time.</span></span>  

 <span data-ttu-id="7bc0b-109">Eine Lagerbuchungsperiode ist ein Zeitraum, der von einem Enddatum definiert ist, und innerhalb dessen Sie Lagertransaktionen buchen müssen.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-109">An inventory period is a period of time, defined by an ending date, in which you post inventory transactions.</span></span> <span data-ttu-id="7bc0b-110">Wenn Sie eine Lagerbuchungsperiode schließen, können keine Wertänderungen in der geschlossenen Periode gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-110">When you close an inventory period, no value changes can be posted in the closed period.</span></span> <span data-ttu-id="7bc0b-111">Dazu gehören neue Wertbuchungen, erwartete oder fakturierte Buchungen, Änderungen bestehender Werte und Kostenregulierungen.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-111">This includes new value postings, expected or invoiced postings, changes to existing values, and cost adjustments.</span></span> <span data-ttu-id="7bc0b-112">Sie können jedoch dennoch mit einen offenen Lagerposten ausgleichen, der in die geschlossene Periode fällt.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-112">However, you can still apply to an open item ledger entry that falls in the closed period.</span></span> <span data-ttu-id="7bc0b-113">[Weitere Informationen finden Sie unter "Designdetails: Artikelverfolgung".](design-details-item-application.md)</span><span class="sxs-lookup"><span data-stu-id="7bc0b-113">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span>  

 <span data-ttu-id="7bc0b-114">Um sicherzustellen, dass alle Transaktionsposten in einer geschlossenen Periode endgültig sind, müssen die folgenden Bedingungen erfüllt sein, bevor eine Lagerbuchungsperiode abgeschlossen werden kann:</span><span class="sxs-lookup"><span data-stu-id="7bc0b-114">To make sure that all transaction entries in a closed period are final, the following conditions must be met before an inventory period can close:</span></span>  

-   <span data-ttu-id="7bc0b-115">Alle offenen ausgehenden Lagerposten in der Periode müssen geschlossen werden (d. h. kein negativer Lagerbestand).</span><span class="sxs-lookup"><span data-stu-id="7bc0b-115">All outbound item ledger entries in the period must be closed (no negative inventory).</span></span>  
-   <span data-ttu-id="7bc0b-116">Alle Artikelkosten in der Periode müssen korrigiert werden.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-116">All item costs in the period must be adjusted.</span></span>  
-   <span data-ttu-id="7bc0b-117">Alle freigegebenen und beendeten Fertigungsaufträge in der Periode müssen einer Kostenanpassung unterzogen werden.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-117">All released and finished production orders in the period must be cost adjusted.</span></span>  

 <span data-ttu-id="7bc0b-118">Wenn Sie eine Lagerbuchungsperiode schließen, wird ein Lagerbuchungsperioden-Posten erstellt, indem die Nummer des letzten Lagerjournals verwendet wird, das in die Lagerbuchungsperiode fällt.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-118">When you close an inventory period, an inventory period entry is created by using the number of the last item register that falls in the inventory period.</span></span> <span data-ttu-id="7bc0b-119">Außerdem werden die Zeit, das Datum und der Benutzercode, die die Periode schließen, im Lagerbuchungsperioden-Posten erfasst.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-119">In addition, the time, date, and user code of the user closing the period are recorded in the inventory period entry.</span></span> <span data-ttu-id="7bc0b-120">Wenn Sie diese Information mit dem letzten Lagerpostens für die vorherige Periode verwenden, können Sie sehen, welche Lagertransaktionen in der Lagerbuchungsperiode gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-120">By using this information with the last item register for the previous period, you can see which inventory transactions were posted in the inventory period.</span></span> <span data-ttu-id="7bc0b-121">Es ist ebenfalls möglich, Lagerbuchungsperioden erneut zu öffnen, wenn Sie in einer geschlossenen Periode buchen müssen.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-121">It is also possible to reopen inventory periods if you need to post in a closed period.</span></span> <span data-ttu-id="7bc0b-122">Wenn Sie eine Lagerbuchungsperiode erneut öffnen, wird ein Lagerbuchungsperioden-Posten erstellt.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-122">When you reopen an inventory period, an inventory period entry is created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7bc0b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bc0b-123">See Also</span></span>  
 <span data-ttu-id="7bc0b-124">[Unter Designdetails: Lagerkosten](design-details-inventory-costing.md) [Verwalten der Lagerkosten](finance-manage-inventory-costs.md) [Finanzen](finance.md)</span><span class="sxs-lookup"><span data-stu-id="7bc0b-124">[Design Details: Inventory Costing](design-details-inventory-costing.md) [Managing Inventory Costs](finance-manage-inventory-costs.md) [Finance](finance.md)</span></span>  
 [<span data-ttu-id="7bc0b-125">Arbeiten mit Financials</span><span class="sxs-lookup"><span data-stu-id="7bc0b-125">Working with Financials</span></span>](ui-work-product.md)
