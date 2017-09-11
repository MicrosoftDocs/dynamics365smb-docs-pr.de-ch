---
title: "Erstellen und führen Sie eine Stapelverarbeitung | Microsoft Docs"
description: "Sie führen Stapelverarbeitungen durch , um Daten zu verarbeiten und Informationen zu aktualisieren, um periodische Buchhaltungsaktivitäten oder Berechnungen durchzuführen."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6844d5fe3efba5349eef166161c5956116bc7fc0
ms.contentlocale: de-ch
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-run-batch-jobs"></a><span data-ttu-id="18f18-103">Vorgehensweise: Ausführen von Stapelverarbeitungen</span><span class="sxs-lookup"><span data-stu-id="18f18-103">How to: Run Batch Jobs</span></span>
<span data-ttu-id="18f18-104">Bei einer Stapelverarbeitung handelt es sich um einen Vorgang, bei dem Daten stapelweise verarbeitet werden, beispielsweise bei der Stapelverarbeitung **Wechselkurs regulieren**.</span><span class="sxs-lookup"><span data-stu-id="18f18-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="18f18-105">Es stehen Stapelverarbeitungen für periodische Buchhaltungsaktivitäten zur Verfügung, beispielsweise zum Abschließen der Erfolgsrechnung am Ende eines Geschäftsjahrs.</span><span class="sxs-lookup"><span data-stu-id="18f18-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="18f18-106">Viele Stapelverarbeitungen dienen zum Ausführen von Berechnungsaufgaben – beispielsweise zum Berechnen von Zuschlägen, Wechselkursregulierungen oder VK-Preisen.</span><span class="sxs-lookup"><span data-stu-id="18f18-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="18f18-107">Eine Stapelverarbeitung gleicht einem Bericht, die Ergebnisse der Stapelverarbeitung werden jedoch zur direkten Aktualisierung der Informationen verwendet, anstatt diese lediglich auszugeben.</span><span class="sxs-lookup"><span data-stu-id="18f18-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="18f18-108">So führen Sie eine Stapelverarbeitung aus:</span><span class="sxs-lookup"><span data-stu-id="18f18-108">To run a batch job</span></span>
1. <span data-ttu-id="18f18-109">Um das Anforderungsfenster für die gewünschte Stapelverarbeitung zu öffnen, wählen Sie das Symbol ![Suche für Seite oder Bericht](media/ui-search/search_small.png "Nach Seite oder Bericht suchen ")und geben den Namen der Stapelverarbeitung ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="18f18-109">To open the request window for the relevant batch job, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="18f18-110">Ist für die Stapelverarbeitung ein Inforegister vom Typ **Optionen** verfügbar, füllen Sie die Felder aus, um die Stapelverarbeitung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="18f18-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="18f18-111">Das Fenster kann mehrere Inforegister mit Filtern enthalten, mit denen sich die in die Stapelverarbeitung einzubeziehenden Daten einschränken lassen.</span><span class="sxs-lookup"><span data-stu-id="18f18-111">The window may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="18f18-112">Sie können Kriterien in die vorgeschlagenen Filter eingeben oder weitere Filter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="18f18-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="18f18-113">Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.</span><span class="sxs-lookup"><span data-stu-id="18f18-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="18f18-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18f18-114">See Also</span></span>
[<span data-ttu-id="18f18-115">Eingeben von Kriterien in Filtern</span><span class="sxs-lookup"><span data-stu-id="18f18-115">Entering Criteria in Filters</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="18f18-116">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="18f18-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

