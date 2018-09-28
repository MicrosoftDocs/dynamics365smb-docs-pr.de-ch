---
title: Abschliessen eines LSV-Einzugs
description: "LSV+ (Lastschrift Verfahren)-Einzüge müssen abgeschlossen werden, um LSV-Dateien zu schreiben, die zum Zahlungseinzug an die Bank gesendet werden können. Wenn Sie einen Einzug abschliessen, ist dieser beendet, und die Buchungen im LSV-Journal werden kombiniert."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d340be0bcf21a45a6bc8610f40a7805700885561
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="close-an-lsv-collection"></a><span data-ttu-id="89ea5-104">Schliessen eines LSV-Einzugs</span><span class="sxs-lookup"><span data-stu-id="89ea5-104">Close an LSV Collection</span></span>
<span data-ttu-id="89ea5-105">LSV+ (Lastschrift Verfahren)-Einzüge müssen abgeschlossen werden, um LSV-Dateien zu schreiben, die zum Zahlungseinzug an die Bank gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="89ea5-105">You must close Lastschrift Verfahren (LSV+) collections to write LSV files that can be sent to the bank for payment collection.</span></span> <span data-ttu-id="89ea5-106">Wenn Sie einen Einzug abschliessen, ist dieser beendet, und die Buchungen im LSV-Journal werden kombiniert.</span><span class="sxs-lookup"><span data-stu-id="89ea5-106">When you close a collection, the collection is complete, and the postings in the LSV journal are combined.</span></span>  

<span data-ttu-id="89ea5-107">Wenn der Einzug abgeschlossen ist, wird die aktuelle Einzugsnummer im LSV-Journal auf Grundlage des letzten Einzugs zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="89ea5-107">When the collection is complete, the current collection number is assigned in the LSV journal, based on the last collection.</span></span> <span data-ttu-id="89ea5-108">Diese LSV-Nummer wird für alle ausstehenden Rechnungen an die Debitorenposten übertragen.</span><span class="sxs-lookup"><span data-stu-id="89ea5-108">This LSV number is transferred to the customer entries for all outstanding invoices.</span></span> <span data-ttu-id="89ea5-109">Anhand der LSV-Nummer kann die Einzugsdatei jederzeit rekonstruiert werden.</span><span class="sxs-lookup"><span data-stu-id="89ea5-109">The collection file can be reconstructed at any time using the LSV number.</span></span> <span data-ttu-id="89ea5-110">Das Feld **Abwarten** wird auch mit **LSV** in den Debitorenposten ausgefüllt, um die Duplizierung von offenen Posten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="89ea5-110">The **On Hold** field is also populated with **LSV** in the customer entries to avoid the duplication of open entries.</span></span> <span data-ttu-id="89ea5-111">Weitere Informationen finden Sie in den Tabellen **LSV Journal** und **Debitorenposten**.</span><span class="sxs-lookup"><span data-stu-id="89ea5-111">For more information, see the **LSV Journal** table and the **Cust. Ledger Entry** table.</span></span> <span data-ttu-id="89ea5-112">Ausserdem kann ein abgeschlossener Einzug auch erneut geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="89ea5-112">You can also reopen a closed collection.</span></span>  

## <a name="to-close-an-lsv-collection"></a><span data-ttu-id="89ea5-113">So schliessen Sie einen LSV-Einzug</span><span class="sxs-lookup"><span data-stu-id="89ea5-113">To close an LSV collection</span></span>  

1.  <span data-ttu-id="89ea5-114">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite ober Bericht suchen"), und öffnen Sie **LSV-Journal Liste**. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="89ea5-114">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **LSV Journal List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="89ea5-115">Wählen Sie die erforderliche Erf.-Journalzeile aus und wählen Sie die Aktion **Buchungsdatum bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="89ea5-115">Select the required journal line, and then choose the **Modify Posting Date** action.</span></span> <span data-ttu-id="89ea5-116">Dadurch wird der Wert im Feld **Valutadatum** geändert, indem der während des LSV-Einzugs vorgeschlagene Wert verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89ea5-116">This will modify the value in the **Credit Date** field by using the value suggested during the LSV collection.</span></span>  
3.  <span data-ttu-id="89ea5-117">Geben Sie im Feld **Neues Datum** das neue Datum ein.</span><span class="sxs-lookup"><span data-stu-id="89ea5-117">In the **New Date** field, enter the new date.</span></span>  
4.  <span data-ttu-id="89ea5-118">Wählen Sie die Aktion **Einzug beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="89ea5-118">Choose the **Close Collection* action*.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="89ea5-119">Die Felder auf dem Inforegister **Optionen** für die Stapelverarbeitung **LSV Einzug abschliessen** können nicht geändert werden und entsprechen der ausgewählten Erf.-Journalzeile.</span><span class="sxs-lookup"><span data-stu-id="89ea5-119">The fields on the **Options** FastTab for the **LSV Close Collection** batch job cannot be modified, and correspond to the selected journal line.</span></span>  

5.  <span data-ttu-id="89ea5-120">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="89ea5-120">Choose the **OK** button.</span></span>  

    <span data-ttu-id="89ea5-121">Im Fenster **LSV-Journal Liste** wird der Wert im Feld **LSV-Status** von **Bearbeiten** in **Freigegeben** geändert.</span><span class="sxs-lookup"><span data-stu-id="89ea5-121">In the **LSV Journal List** window, the value in the **LSV Status** field is changed from **Edit** to **Released**.</span></span> <span data-ttu-id="89ea5-122">Die Erf.-Journalzeilen können nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="89ea5-122">The journal lines can no longer be modified.</span></span>  

## <a name="to-reopen-an-lsv-collection"></a><span data-ttu-id="89ea5-123">So öffnen Sie einen LSV-Einzug erneut</span><span class="sxs-lookup"><span data-stu-id="89ea5-123">To reopen an LSV collection</span></span>  

1.  <span data-ttu-id="89ea5-124">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite ober Bericht suchen"), und öffnen Sie **LSV-Journal Liste**. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="89ea5-124">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **LSV Journal List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="89ea5-125">Wählen Sie die erforderliche Erf.-Journalzeile, für die Sie die Sammlung erneut öffnen möchten und wählen Sie dann die Aktion **Sammlung erneut öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="89ea5-125">Select the required journal line for which you want to reopen the collection, on then choose the **Reopen Collection** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="89ea5-126">Der Einzug kann nur erneut geöffnet werden, wenn die LSV+-Datei noch nicht an die Bank übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="89ea5-126">You can only reopen the collection if you have not yet submitted the LSV+ file to the bank.</span></span>  

3.  <span data-ttu-id="89ea5-127">Wählen Sie die Schaltfläche **Ja**, um das erneute Öffnen des Einzugs zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="89ea5-127">Choose the **Yes** button to confirm the reopening of the collection.</span></span>  

## <a name="see-also"></a><span data-ttu-id="89ea5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89ea5-128">See Also</span></span>  
 <span data-ttu-id="89ea5-129">[Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="89ea5-129">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 <span data-ttu-id="89ea5-130">[Verarbeiten eines LSV-Einzugs](how-to-process-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="89ea5-130">[Process an LSV Collection](how-to-process-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="89ea5-131">[Buchen von LSV+ Zahlungen](how-to-post-lsv-payments.md) </span><span class="sxs-lookup"><span data-stu-id="89ea5-131">[Post LSV+ Payments](how-to-post-lsv-payments.md) </span></span>  
 [<span data-ttu-id="89ea5-132">Exportieren von Zahlungen mit LSV</span><span class="sxs-lookup"><span data-stu-id="89ea5-132">Export Payments Using LSV</span></span>](how-to-export-payments-using-lsv.md)

