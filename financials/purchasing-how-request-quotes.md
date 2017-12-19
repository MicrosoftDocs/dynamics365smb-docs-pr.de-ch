---
title: Erstellen Sie eine Einkaufsofferte, um ein Offerte von Ihrem Lieferanten anzufordern | Microsoft Docs
description: Beschreibt, wie Verkaufsofferten oder eine Anforderung erstellt wird, um Ihre Offerte zu erfassen, um unter bestimmten Bedingungen einem Kunden zu verkaufen.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: df1793d811dea11c01ff5e7d90a9f52b9e987c13
ms.contentlocale: de-ch
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-request-quotes"></a><span data-ttu-id="e2a79-103">Gewusst wie: Offerten anfordern</span><span class="sxs-lookup"><span data-stu-id="e2a79-103">How to: Request Quotes</span></span>
<span data-ttu-id="e2a79-104">Eine Einkaufsofferte kann als erster Entwurf für eine Bestellung verwendet werden. Die Bestellung kann dann in eine Rechnung oder einen Auftrag umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="e2a79-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="e2a79-105">So erstellen Sie eine Einkaufsofferte</span><span class="sxs-lookup"><span data-stu-id="e2a79-105">To create a purchase quote</span></span>
1. <span data-ttu-id="e2a79-106">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Einkaufsofferten** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e2a79-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="e2a79-107">Erstellen eines neuen Belegs, so wie Sie eine Bestellung erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2a79-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="e2a79-108">Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="e2a79-108">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="e2a79-109">So konvertieren Sie eine Einkaufsofferte in eine Einkaufsbestellung</span><span class="sxs-lookup"><span data-stu-id="e2a79-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="e2a79-110">Wenn Sie die Offerte akzeptiert haben, können Sie diese mit einer Einkaufsrechnung oder einem Auftrag umwandeln, um den Einkauf zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e2a79-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="e2a79-111">Öffnen Sie eine Einkaufsofferte, die bereit ist zum umzuwandeln, und wählen Sie die **Bestellung erst.** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="e2a79-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="e2a79-112">Die Einkaufsofferte wird aus der Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="e2a79-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="e2a79-113">Eine Einkaufsrechnung oder ein Einkaufsauftrag wird auf der Basis der Informationen in der Einkaufsofferte erstellt, in der Sie den Einkauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="e2a79-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="e2a79-114">In der erstellten Einkaufsrechnung bzw. -bestellung gibt das Feld **Offertennr.** die Nummer der Einkaufsofferte an, aus der sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e2a79-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2a79-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2a79-115">See Also</span></span>
[<span data-ttu-id="e2a79-116">Einkauf</span><span class="sxs-lookup"><span data-stu-id="e2a79-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="e2a79-117">Einkaufeinrichten</span><span class="sxs-lookup"><span data-stu-id="e2a79-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="e2a79-118">Gewusst wie: Senden von Belegen über E-Mail</span><span class="sxs-lookup"><span data-stu-id="e2a79-118">How to: Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="e2a79-119">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e2a79-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

