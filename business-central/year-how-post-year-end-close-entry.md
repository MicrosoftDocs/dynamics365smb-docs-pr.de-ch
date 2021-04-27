---
title: So buchen Sie den Jahresabschlussposten
description: Beschreibt, wie Sie das Erf.-Journal öffnen, dass Sie in der Stapelverarbeitung "Jahresabschluss" definiert haben und dann den Jahresabschlusseintrag überprüfen und buchen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5c822685ae5723bc6b13f9fedad45dbddefdb956
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776606"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="77c70-103">So buchen Sie den Jahresabschlussposten</span><span class="sxs-lookup"><span data-stu-id="77c70-103">Post the Year-End Closing Entry</span></span>

<span data-ttu-id="77c70-104">Nachdem Sie die Stapelverarbeitung **GuV-Konten Nullstellung** ausgeführt haben, um den bzw. die Ultimoposten für den Jahresabschluss zu generieren, müssen Sie das in der Stapelverarbeitung angegebene Buchungsblatt öffnen und die Posten überprüfen und buchen.</span><span class="sxs-lookup"><span data-stu-id="77c70-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>  

> [!TIP]
> <span data-ttu-id="77c70-105">Abhängig von den Arbeitsprozessen Ihres Unternehmens können Sie wählen, ob Abrechnungsperioden und Geschäftsjahre in [!INCLUDE [prod_short](includes/prod_short.md)] geschlossen werden sollen oder nicht.</span><span class="sxs-lookup"><span data-stu-id="77c70-105">Depending on your organizations work processes, you can choose to close or not close accounting periods and fiscal years in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="77c70-106">Das folgende Verfahren setzt voraus, dass Sie das Geschäftsjahr mit der Option *Buchhaltungsperioden* abgeschlossen haben, einen Jahresabschlusseintrag mit dem Batch-Job **Gewinn- und Verlustrechnung schliessen** generiert haben und nun bereit sind, den Abschlusseintrag zum Jahresende zusammen mit den Gegenbuchungen des Eigenkapitalkontos zu buchen.</span><span class="sxs-lookup"><span data-stu-id="77c70-106">The following procedure assumes that you have closed the fiscal year using the *Accounting Periods* option, generated a year-end closing entry using the **Close Income Statement** batch job, and are now ready to post the year-end closing entry along with the offsetting equity account entries.</span></span> <span data-ttu-id="77c70-107">Ihre Organisation kann sich dafür entscheiden, anders zu arbeiten, z. B. den Abschluss zum Jahresende als Teil des Abschlusses des Geschäftsjahres zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="77c70-107">Your organization can choose to work differently, such as post the year-end closing entry as part of closing the fiscal year.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="77c70-108">So buchen Sie den Jahresabschlussposten</span><span class="sxs-lookup"><span data-stu-id="77c70-108">To post the year end closing entry</span></span>

1. <span data-ttu-id="77c70-109">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Fibu Erf.-Journal** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="77c70-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="77c70-110">Wählen Sie auf der Seite **Fibu Erf.-Journal** im Feld **Erf.-Journalname** das Erf.-Journal mit den Abschlussposten aus.</span><span class="sxs-lookup"><span data-stu-id="77c70-110">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="77c70-111">Überprüfen Sie die Posten.</span><span class="sxs-lookup"><span data-stu-id="77c70-111">Review the entries.</span></span>
4. <span data-ttu-id="77c70-112">Wählen Sie auf der Registerkarte **Start** die Option Buchen aus, um das Erfassungsjournal zu buchen.</span><span class="sxs-lookup"><span data-stu-id="77c70-112">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
> <span data-ttu-id="77c70-113">Wenn ein Fehler erkannt wird, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77c70-113">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="77c70-114">Wurde die Buchung ordnungsgemäss durchgeführt, werden die gebuchten Posten aus dem Erfassungsjournal entfernt.</span><span class="sxs-lookup"><span data-stu-id="77c70-114">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="77c70-115">Nachdem die Buchung abgeschlossen ist, wird ein Posten auf jedes Erfolgsrechnungskonto gebucht, sodass der Saldo des Kontos Null ist und das Jahresergebnis in die Bilanz übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="77c70-115">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="77c70-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77c70-116">See Also</span></span>

[<span data-ttu-id="77c70-117">Schliessen von Buchhaltungsperioden</span><span class="sxs-lookup"><span data-stu-id="77c70-117">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="77c70-118">Schliessen der Bücher</span><span class="sxs-lookup"><span data-stu-id="77c70-118">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="77c70-119">GuV-Konten Nullstellung</span><span class="sxs-lookup"><span data-stu-id="77c70-119">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="77c70-120">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="77c70-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]