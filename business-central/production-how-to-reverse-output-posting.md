---
title: 'Vorgehensweise: Ausgangsbuchung stornieren | Microsoft Docs'
description: Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss. Dies ist z. B. der Fall, wenn eine fehlerhafte Dateneingabe passiert ist und eine falsche fertiggestellte Menge in einem Fertigungsauftrag gebucht wurde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ed275469dd172af43ceb96b85d5ac0aa99e96a2f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759056"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="d619d-104">Gebuchte fertig gestellte Menge stornieren</span><span class="sxs-lookup"><span data-stu-id="d619d-104">Reverse Output Posting</span></span>
<span data-ttu-id="d619d-105">Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d619d-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="d619d-106">Dies ist z. B. der Fall, wenn eine fehlerhafte Dateneingabe passiert ist und eine falsche fertiggestellte Menge in einem Fertigungsauftrag gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="d619d-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="d619d-107">Eine Ausgangsbuchung stornieren</span><span class="sxs-lookup"><span data-stu-id="d619d-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="d619d-108">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **FA-Istmeldungs Erf.-Journal** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="d619d-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="d619d-109">Wählen Sie Ihren Stapel aus.</span><span class="sxs-lookup"><span data-stu-id="d619d-109">Select your batch.</span></span>  
2. <span data-ttu-id="d619d-110">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="d619d-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="d619d-111">Weitere Informationen finden Sie unter [Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen](production-how-to-post-output-quantity.md)</span><span class="sxs-lookup"><span data-stu-id="d619d-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="d619d-112">Wählen Sie im Feld **Ausgleich mit Lfd. Nr.** den zugeordneten Lagerposten aus.</span><span class="sxs-lookup"><span data-stu-id="d619d-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="d619d-113">Dadurch werden der Kapazitäts- und der Lagerposten storniert.</span><span class="sxs-lookup"><span data-stu-id="d619d-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="d619d-114">Erfen Sie die Stornierung, indem Sie das Erf.-Journal buchen.</span><span class="sxs-lookup"><span data-stu-id="d619d-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="d619d-115">Die Posten im FA-Istmeldungsprotokoll werden im HauptLagerposten als positiver Ausgleich gebucht.</span><span class="sxs-lookup"><span data-stu-id="d619d-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d619d-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d619d-116">See Also</span></span>  
 <span data-ttu-id="d619d-117">[Bearbeitungen](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="d619d-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="d619d-118">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="d619d-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="d619d-119">[Planung](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="d619d-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="d619d-120">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="d619d-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="d619d-121">Einkauf</span><span class="sxs-lookup"><span data-stu-id="d619d-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="d619d-122">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d619d-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
