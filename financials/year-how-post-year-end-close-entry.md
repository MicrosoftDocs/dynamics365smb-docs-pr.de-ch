---
title: "Vorgehensweise: Buchen und überprüfen des Jahresabschlusspostens | Microsoft Docs"
description: "Beschreibt, wie Sie das Erf.-Journal öffnen, dass Sie in der Stapelverarbeitung \"Jahresabschluss\" definiert haben und dann den Jahresabschlusseintrag überprüfen und buchen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 78039e9387866ce17ff3be5a2ff509545e8439d2
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="d5c74-103">So buchen Sie den Jahresabschlussposten</span><span class="sxs-lookup"><span data-stu-id="d5c74-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="d5c74-104">Nachdem Sie die Stapelverarbeitung **GuV-Konten Nullstellung** ausgeführt haben, um den bzw. die Ultimoposten für den Jahresabschluss zu generieren, müssen Sie das in der Stapelverarbeitung angegebene Buchungsblatt öffnen und die Posten überprüfen und buchen.</span><span class="sxs-lookup"><span data-stu-id="d5c74-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="d5c74-105">So buchen Sie den Jahresabschlussposten</span><span class="sxs-lookup"><span data-stu-id="d5c74-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="d5c74-106">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite ober Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="d5c74-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="d5c74-107">Wählen Sie im Fenster **Fibu Erf.-Journal** im Feld **Erfassungsjournalname** das Erfassungsjournal mit den Abschlussposten aus.</span><span class="sxs-lookup"><span data-stu-id="d5c74-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="d5c74-108">Überprüfen Sie die Posten.</span><span class="sxs-lookup"><span data-stu-id="d5c74-108">Review the entries.</span></span>
4. <span data-ttu-id="d5c74-109">Wählen Sie auf der Registerkarte **Start** die Option Buchen aus, um das Erfassungsjournal zu buchen.</span><span class="sxs-lookup"><span data-stu-id="d5c74-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d5c74-110">Wenn ein Fehler erkannt wird, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5c74-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="d5c74-111">Wurde die Buchung ordnungsgemäss durchgeführt, werden die gebuchten Posten aus dem Erfassungsjournal entfernt.</span><span class="sxs-lookup"><span data-stu-id="d5c74-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="d5c74-112">Nachdem die Buchung abgeschlossen ist, wird ein Posten auf jedes Erfolgsrechnungskonto gebucht, sodass der Saldo des Kontos Null ist und das Jahresergebnis in die Bilanz übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="d5c74-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5c74-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5c74-113">See Also</span></span>
[<span data-ttu-id="d5c74-114">Schliessen von Buchhaltungsperioden</span><span class="sxs-lookup"><span data-stu-id="d5c74-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="d5c74-115">Schliessen der Bücher</span><span class="sxs-lookup"><span data-stu-id="d5c74-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="d5c74-116">GuV-Konten Nullstellung</span><span class="sxs-lookup"><span data-stu-id="d5c74-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="d5c74-117">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d5c74-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

