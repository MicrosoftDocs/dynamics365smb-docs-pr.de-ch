---
title: Erstellen Sie eine Einkaufsofferte, um ein Angebot von Ihrem Lieferanten anzufordern | Microsoft Docs
description: Beschreibt, wie Verkaufsofferten oder eine Anforderung erstellt wird, um Ihre Offerte zu erfassen, um unter bestimmten Bedingungen einem Debitoren zu verkaufen.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 416c5a4e4376932c16a1496f2db2b0c79307d22b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772643"
---
# <a name="request-quotes"></a><span data-ttu-id="eca39-103">Offertenanforderungen</span><span class="sxs-lookup"><span data-stu-id="eca39-103">Request Quotes</span></span>
<span data-ttu-id="eca39-104">Eine Einkaufsofferte kann als erster Entwurf für eine Bestellung verwendet werden. Die Bestellung kann dann in eine Rechnung oder einen Auftrag umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="eca39-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="eca39-105">So erstellen Sie eine Einkaufsofferte</span><span class="sxs-lookup"><span data-stu-id="eca39-105">To create a purchase quote</span></span>
1. <span data-ttu-id="eca39-106">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Einkaufsanfragen** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="eca39-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="eca39-107">Erstellen eines neuen Belegs, so wie Sie eine Bestellung erstellen.</span><span class="sxs-lookup"><span data-stu-id="eca39-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="eca39-108">Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="eca39-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="eca39-109">So konvertieren Sie eine Einkaufsofferte in eine Einkaufsbestellung</span><span class="sxs-lookup"><span data-stu-id="eca39-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="eca39-110">Wenn Sie die Offerte akzeptiert haben, können Sie diese mit einer Einkaufsrechnung oder einem Auftrag umwandeln, um den Einkauf zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="eca39-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="eca39-111">Öffnen Sie eine Einkaufsofferte, die bereit ist zum umzuwandeln, und wählen Sie die **Bestellung erst.** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="eca39-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="eca39-112">Die Einkaufsofferte wird aus der Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="eca39-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="eca39-113">Eine Einkaufsrechnung oder ein Einkaufsauftrag wird auf der Basis der Informationen in der Einkaufsofferte erstellt, in der Sie den Einkauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="eca39-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="eca39-114">In der erstellten Einkaufsrechnung bzw. -bestellung gibt das Feld **Offertennr.** die Nummer der Einkaufsofferte an, aus der sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="eca39-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="eca39-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eca39-115">See Also</span></span>
[<span data-ttu-id="eca39-116">Einkauf</span><span class="sxs-lookup"><span data-stu-id="eca39-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="eca39-117">Einkaufeinrichten</span><span class="sxs-lookup"><span data-stu-id="eca39-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="eca39-118">Senden von Belegen über E-Mail</span><span class="sxs-lookup"><span data-stu-id="eca39-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="eca39-119">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eca39-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]