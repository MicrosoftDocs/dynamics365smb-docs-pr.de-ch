---
title: "Vorgehensweise: Übertragen von Fibuposten in Kostenposten | Microsoft Docs"
description: "Sie können Fibuposten in Kostenposten übertragen."
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
ms.openlocfilehash: 62ed00ef7ca278245b9cdd1a28a4ee70cf9a8f11
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="db0aa-103">So übertragen Sie Fibuposten in Kostenposten</span><span class="sxs-lookup"><span data-stu-id="db0aa-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="db0aa-104">Sie können Fibuposten in Kostenposten übertragen.</span><span class="sxs-lookup"><span data-stu-id="db0aa-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="db0aa-105">Bevor Sie den Vorgang für das Übertragen von Fibuposten in Kostenposten durchführen, müssen Sie die Übertragung vorbereiten, um manuelle Korrekturbuchungen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="db0aa-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="db0aa-106">So bereiten Sie die Übertragung vor</span><span class="sxs-lookup"><span data-stu-id="db0aa-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="db0aa-107">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kostenrechnung einrichten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="db0aa-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="db0aa-108">Stellen Sie im Fenster **Kostenrechnungseinrichtung** sicher, dass im Feld **Startdatum für Sachkontenübertragung** der richtige Wert eingetragen ist.</span><span class="sxs-lookup"><span data-stu-id="db0aa-108">In the **Cost Accounting Setup** window, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="db0aa-109">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan Kontenarten** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="db0aa-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="db0aa-110">Im Fenster **Kostenartkarte** prüfen Sie, dass das Feld **Fibukontobereich** für jede Kostenart korrekt verknüpft ist, um Posten aus der Fibu zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="db0aa-110">In the **Cost Type Card** window, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="db0aa-111">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="db0aa-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="db0aa-112">Überprüfen Sie für jedes Fibukonto im Fenster **Fibukontokarte**, ob das **Kostenartnr.**</span><span class="sxs-lookup"><span data-stu-id="db0aa-112">For each relevant general ledger account, in the **G/L Account Card** window, verify that the **Cost Type No.**</span></span> <span data-ttu-id="db0aa-113">Feld wird korrekt zu einer Kostenart verknüpft.</span><span class="sxs-lookup"><span data-stu-id="db0aa-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="db0aa-114">Weitere Informationen finden Sie unter [Definieren der Beziehung zwischen Kostenarten und Fibukonten](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="db0aa-114">For more information, see [Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span></span>  
7.  <span data-ttu-id="db0aa-115">Vergewissern Sie sich, dass alle entsprechenden Fibuposten Dimensionswerte haben, die einer Kostenstelle und zu einem Kostenträger entsprechen.</span><span class="sxs-lookup"><span data-stu-id="db0aa-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="db0aa-116">So übertragen Sie Fibuposten in Kostenposten</span><span class="sxs-lookup"><span data-stu-id="db0aa-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="db0aa-117">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Transfer-Einträge‌ in CA** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="db0aa-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="db0aa-118">Wählen Sie auf Schaltfläche **OK**, um die Umlagerung zu starten.</span><span class="sxs-lookup"><span data-stu-id="db0aa-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="db0aa-119">Der Prozess überträgt alle Fibuposten, die nicht bereits übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="db0aa-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="db0aa-120">Während der Übertragung erstellt der Vorgang Verknüpfungen in den Posten **Posteneintrag** und **Kostentabelle**.</span><span class="sxs-lookup"><span data-stu-id="db0aa-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="db0aa-121">Dies ermöglicht es Ihnen, die Herkunft von Kostenposten nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="db0aa-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="db0aa-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db0aa-122">See Also</span></span>  
 <span data-ttu-id="db0aa-123">[Kriterien für die Übertragung von Sachposten in Kostenposten](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="db0aa-123">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="db0aa-124">[Automatische Übertragung und kombinierte Posten](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="db0aa-124">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
 <span data-ttu-id="db0aa-125">[Ergebnisse der Übertragung](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="db0aa-125">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 <span data-ttu-id="db0aa-126">[Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="db0aa-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="db0aa-127">Definieren der Beziehung zwischen Kostenarten und Sachkonten</span><span class="sxs-lookup"><span data-stu-id="db0aa-127">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

