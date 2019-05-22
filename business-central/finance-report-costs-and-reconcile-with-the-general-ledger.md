---
title: Melden von Kosten und Abstimmen mit der Fibu | Microsoft Docs
description: Am Ende von (monatlichen, jährlichen oder anderen) Buchhaltungsperioden muss eine Reihe von Kostenkontroll- und Prüfungsaufgaben ausgeführt werden, um der Finanzabteilung einen korrekten und ausgewogenen Lagerwert mitteilen zu können. Neben der Buchungsroutine, durch die die einzelnen Artikelwertposten auf dedizierte Fibukonten gebucht werden, stehen dem Prüfer oder Controller, der mit dieser bedeutenden Aufgabe betraut ist, verschiedene Berichte, Nachverfolgungsfunktionen sowie ein spezielles Abstimmungstool zur Verfügung.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/02/2019
ms.author: sgroespe
ms.openlocfilehash: d92d732b99eedb06eb0185d1227252e1ace95334
ms.sourcegitcommit: dac212009aadf3227e54c99976c438f6e56f182a
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 05/02/2019
ms.locfileid: "1446890"
---
# <a name="reporting-costs-and-reconciling-with-the-general-ledger"></a><span data-ttu-id="bca8b-104">Melden von Kosten und Abstimmen mit der Fibu</span><span class="sxs-lookup"><span data-stu-id="bca8b-104">Reporting Costs and Reconciling with the General Ledger</span></span>
<span data-ttu-id="bca8b-105">Am Ende von (monatlichen, jährlichen oder anderen) Buchhaltungsperioden muss eine Reihe von Kostenkontroll- und Prüfungsaufgaben ausgeführt werden, um der Finanzabteilung einen korrekten und ausgewogenen Lagerwert mitteilen zu können.</span><span class="sxs-lookup"><span data-stu-id="bca8b-105">At the end of accounting periods, monthly, yearly or other, a sequence of cost control and auditing tasks must be performed to report a correct and balanced inventory value to the finance department.</span></span> <span data-ttu-id="bca8b-106">Neben der Buchungsroutine, durch die die einzelnen Artikelwertposten auf dedizierte Fibukonten gebucht werden, stehen dem Prüfer oder Controller, der mit dieser bedeutenden Aufgabe betraut ist, verschiedene Berichte, Nachverfolgungsfunktionen sowie ein spezielles Abstimmungstool zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="bca8b-106">Apart from the posting routine that transfers the individual item value entries to dedicated general ledger accounts, several reports, tracing functions, and a special reconciliation tool are available to the auditor or controller responsible for this business-critical work.</span></span>  

 <span data-ttu-id="bca8b-107">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="bca8b-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="bca8b-108">**Bis**</span><span class="sxs-lookup"><span data-stu-id="bca8b-108">**To**</span></span>|<span data-ttu-id="bca8b-109">**Siehe**</span><span class="sxs-lookup"><span data-stu-id="bca8b-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="bca8b-110">Anzeigen des Lagerwerts ausgewählter Artikel, einschliesslich Informationen zu Mengen und Werten bei Erhöhung oder Verringerung des Lagerbestands innerhalb eines bestimmten Zeitraums</span><span class="sxs-lookup"><span data-stu-id="bca8b-110">View the inventory value of selected items, including information about the quantities and values of increases and decreases in inventory over a selected period.</span></span>|<span data-ttu-id="bca8b-111">Bericht **Aktuellen Lagerwert ermitteln**</span><span class="sxs-lookup"><span data-stu-id="bca8b-111">**Inventory Valuation** report</span></span>|  
|<span data-ttu-id="bca8b-112">Anzeigen des Lagerwerts ausgewählter Fertigungsaufträge in "Aktiviert Lager", beispielsweise der Mengen und Werte für Verbrauch, Kapazitätsauslastung und Ausgabe in laufenden Fertigungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="bca8b-112">View the inventory value of selected production orders in your WIP (work in process) inventory, such as the quantities and values of consumption, capacity usage, and output in ongoing production orders.</span></span>|<span data-ttu-id="bca8b-113">Bericht **Lagerbewertung - Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="bca8b-113">**Inventory Valuation - WIP** report</span></span>|  
|<span data-ttu-id="bca8b-114">Anzeigen des Lagerwerts ausgewählter Artikel, einschliesslich der tatsächlichen Kosten und der Soll-Kosten zum angegebenen Datum</span><span class="sxs-lookup"><span data-stu-id="bca8b-114">View the inventory value of selected items, including their actual and expected cost on the date specified.</span></span>|<span data-ttu-id="bca8b-115">Bericht **Lagerbew.-Einst.-Pr.-Ermittl.**</span><span class="sxs-lookup"><span data-stu-id="bca8b-115">**Invt. Valuation - Cost Spec.** report</span></span>|  
|<span data-ttu-id="bca8b-116">Verwenden eines Berichts zum Analysieren der Ursachen für Kostenschwankungen oder zum Verschaffen eines Überblicks über den Kostenanteil verkaufter Artikel (Lagerverbrauch)</span><span class="sxs-lookup"><span data-stu-id="bca8b-116">Use a report to analyze the reasons for cost variances or to gain insight into the cost shares of sold items (COGS).</span></span>|<span data-ttu-id="bca8b-117">Bericht **Kostenanteilsanalyse**</span><span class="sxs-lookup"><span data-stu-id="bca8b-117">**Cost Shares Breakdown** report</span></span>|  
|<span data-ttu-id="bca8b-118">Periodisches Buchen der Wertposten von Artikeltransaktionen aus den Lagerposten auf die entsprechenden Fibukonten, um die beiden Bücher abzustimmen</span><span class="sxs-lookup"><span data-stu-id="bca8b-118">Periodically post the value entries of item transactions from the inventory ledger to the related G/L accounts to reconcile the two ledgers.</span></span>|[<span data-ttu-id="bca8b-119">Abstimmen der Lagerregulierung mit dem Fibuposten</span><span class="sxs-lookup"><span data-stu-id="bca8b-119">Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="bca8b-120">Bestimmen des WIP-Betrags, der im Rahmen der Berichterstellung am Periodenende auf Bilanzkonten gebucht werden muss</span><span class="sxs-lookup"><span data-stu-id="bca8b-120">Determine the WIP amount that needs to be posted to balance sheet accounts for period-end reporting.</span></span>|[<span data-ttu-id="bca8b-121">Überwachen des Status und der Leistung</span><span class="sxs-lookup"><span data-stu-id="bca8b-121">Monitor Job Progress and Performance</span></span>](projects-how-monitor-progress-performance.md)|

## <a name="see-also"></a><span data-ttu-id="bca8b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bca8b-122">See Also</span></span>  
[<span data-ttu-id="bca8b-123">Einrichten der Lagerwertberechnung und der Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="bca8b-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="bca8b-124">Verwalten der Lagerregulierung</span><span class="sxs-lookup"><span data-stu-id="bca8b-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="bca8b-125">Finanzen</span><span class="sxs-lookup"><span data-stu-id="bca8b-125">Finance</span></span>](finance.md)  
<span data-ttu-id="bca8b-126">[Lagerbest.](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="bca8b-126">[Inventory](inventory-manage-inventory.md) </span></span>  
<span data-ttu-id="bca8b-127">[Verkauf](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="bca8b-127">[Sales](sales-manage-sales.md) </span></span>  
[<span data-ttu-id="bca8b-128">Einkauf</span><span class="sxs-lookup"><span data-stu-id="bca8b-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="bca8b-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bca8b-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
