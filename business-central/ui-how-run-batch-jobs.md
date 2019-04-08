---
title: Erstellen und führen Sie eine Stapelverarbeitung | Microsoft Docs
description: Sie führen Stapelverarbeitungen durch , um Daten zu verarbeiten und Informationen zu aktualisieren, um periodische Buchhaltungsaktivitäten oder Berechnungen durchzuführen.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 260cd7761b130bbe3748de3cc109a9f4f56c1384
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/19/2019
ms.locfileid: "853272"
---
# <a name="run-batch-jobs"></a><span data-ttu-id="cd687-103">Ausführen von Stapelverarbeitungen</span><span class="sxs-lookup"><span data-stu-id="cd687-103">Run Batch Jobs</span></span>
<span data-ttu-id="cd687-104">Bei einer Stapelverarbeitung handelt es sich um einen Vorgang, bei dem Daten stapelweise verarbeitet werden, beispielsweise bei der Stapelverarbeitung **Wechselkurs regulieren**.</span><span class="sxs-lookup"><span data-stu-id="cd687-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="cd687-105">Es stehen Stapelverarbeitungen für periodische Buchhaltungsaktivitäten zur Verfügung, beispielsweise zum Abschließen der Erfolgsrechnung am Ende eines Geschäftsjahrs.</span><span class="sxs-lookup"><span data-stu-id="cd687-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="cd687-106">Viele Stapelverarbeitungen dienen zum Ausführen von Berechnungsaufgaben – beispielsweise zum Berechnen von Zuschlägen, Wechselkursregulierungen oder VK-Preisen.</span><span class="sxs-lookup"><span data-stu-id="cd687-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="cd687-107">Eine Stapelverarbeitung gleicht einem Bericht, die Ergebnisse der Stapelverarbeitung werden jedoch zur direkten Aktualisierung der Informationen verwendet, anstatt diese lediglich auszugeben.</span><span class="sxs-lookup"><span data-stu-id="cd687-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="cd687-108">So führen Sie eine Stapelverarbeitung aus:</span><span class="sxs-lookup"><span data-stu-id="cd687-108">To run a batch job</span></span>
1. <span data-ttu-id="cd687-109">Zum Öffnen der Anforderungsseite für die relevanten Stapelverarbeitung wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie den Namen der Stapelverarbeitung ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="cd687-109">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="cd687-110">Ist für die Stapelverarbeitung ein Inforegister vom Typ **Optionen** verfügbar, füllen Sie die Felder aus, um die Stapelverarbeitung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cd687-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="cd687-111">Die Seite kann mehrere Inforegister mit Filtern enthalten, mit denen sich die in die Stapelverarbeitung einzubeziehenden Daten einschränken lassen.</span><span class="sxs-lookup"><span data-stu-id="cd687-111">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="cd687-112">Sie können Kriterien in die vorgeschlagenen Filter eingeben oder weitere Filter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd687-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="cd687-113">Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.</span><span class="sxs-lookup"><span data-stu-id="cd687-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd687-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd687-114">See Also</span></span>
[<span data-ttu-id="cd687-115">Sortieren, Durchsuchen und Filtern von Listen</span><span class="sxs-lookup"><span data-stu-id="cd687-115">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="cd687-116">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cd687-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
