---
title: "Abschliessen der Buchhaltungsperioden für ein Geschäftsjahr | Microsoft Docs"
description: "Beschreibt, wie Sie die Buchhaltungsperioden schliessen, die das Geschäftsjahr ausmachen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 23a9cd7a8a7f579f63937ac4fc28e6d4958f3f9a
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="close-accounting-periods"></a><span data-ttu-id="5e3b6-103">Schliessen von Buchhaltungsperioden</span><span class="sxs-lookup"><span data-stu-id="5e3b6-103">Close Accounting Periods</span></span>
<span data-ttu-id="5e3b6-104">Wenn ein Geschäftsjahr vorbei ist, müssen die Perioden, aus denen es besteht, geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="5e3b6-105">Buchhaltungsperioden schliessen:</span><span class="sxs-lookup"><span data-stu-id="5e3b6-105">To close accounting periods</span></span>
1. <span data-ttu-id="5e3b6-106">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Buchungsperioden** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="5e3b6-107">Im Fenster **Buchhaltungsperioden** wählen Sie die Aktion **Jahr abschliessen**.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-107">In the **Accounting Periods** window, choose the **Close Year** action.</span></span>

    <span data-ttu-id="5e3b6-108">Sind mehrere Geschäftsjahre offen, wird angenommen, dass das früheste automatisch abgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="5e3b6-109">Ein Mitteilungsfenster wird angezeigt, in dem das zu schliessende Jahr angegeben wird und die Konsequenzen erklärt werden.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="5e3b6-110">Wählen Sie die Schaltfläche **Ja** aus, um das Jahr zu schliessen.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="5e3b6-111">Das Geschäftsjahr ist geschlossen und die Felder **Abgeschlossen** und **Datum gesperrt** werden für alle Perioden des Jahres aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="5e3b6-112">Das Geschäftsjahr kann nicht erneut geöffnet werden und Sie können das Häkchen aus den Feldern **Abgeschlossen** oder **Datum gesperrt** nicht mehr entfernen.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="5e3b6-113">Sie können ein Geschäftsjahr erst abschliessen, wenn Sie ein neues erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="5e3b6-114">Beachten Sie, dass Sie nach dem Abschluss eines Geschäftsjahres das Startdatum des folgenden Geschäftsjahres nicht mehr ändern können.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="5e3b6-115">Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Fibuposten gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="5e3b6-116">In diesen Fällen wird in den Posten vermerkt, dass die Buchung in einem abgeschlossenen Geschäftsjahr erfolgte, d. h., das Feld **Nachbuchung** wird mit einem Häkchen versehen.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="5e3b6-117">Nachdem ein Geschäftsjahr abgeschlossen wurde, müssen Sie die Erfolgsrechnungsnullstellung durchführen und das Ergebnis auf ein Bilanzkonto übertragen lassen.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="5e3b6-118">Dies können das jedes Mal wiederholen, wenn Sie in ein abgeschlossenes Geschäftsjahr gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e3b6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e3b6-119">See Also</span></span>
[<span data-ttu-id="5e3b6-120">Schliessen der Bücher</span><span class="sxs-lookup"><span data-stu-id="5e3b6-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="5e3b6-121">So buchen Sie den Jahresabschlussposten</span><span class="sxs-lookup"><span data-stu-id="5e3b6-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="5e3b6-122">Ein neues Geschäftsjahres eröffnen</span><span class="sxs-lookup"><span data-stu-id="5e3b6-122">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="5e3b6-123">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e3b6-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

