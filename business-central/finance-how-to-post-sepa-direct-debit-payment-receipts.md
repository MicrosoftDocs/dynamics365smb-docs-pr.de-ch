---
title: SEPA Lastschriftzahlungen | Microsoft Docs
description: Wenn ein Basislastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 6c646575ba803358aa00309ce02742423bcc7de8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "930769"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="4b197-103">SEPA-Lastschrifteinzug-Zahlungseingänge buchen</span><span class="sxs-lookup"><span data-stu-id="4b197-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="4b197-104">Wenn ein Basislastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen.</span><span class="sxs-lookup"><span data-stu-id="4b197-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="4b197-105">Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)</span><span class="sxs-lookup"><span data-stu-id="4b197-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="4b197-106">Sie können der Zahlungseingang direkt aus dem **Lastschriften** oder im **Direct Debit Collect. Posten** buchen.</span><span class="sxs-lookup"><span data-stu-id="4b197-106">You can post the payment receipt directly from the **Direct Debit Collections** page or the **Direct Debit Collect. Entries** page.</span></span> <span data-ttu-id="4b197-107">Sie können auch die Arbeit an einen anderen Benutzer übertragen, indem Sie die zugehörigen Erf.-Journalzeilen vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="4b197-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a><span data-ttu-id="4b197-108">Buchen eines Lastschrifteingangs aus der Lastschrift-Einzugsseite</span><span class="sxs-lookup"><span data-stu-id="4b197-108">To post a direct-debit payment receipt from the Direct Debit Collections page</span></span>  
1. <span data-ttu-id="4b197-109">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lastschriften** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="4b197-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4b197-110">Wählen Sie eine Zeile für die Basislastschrifterfassung, die in eine Bankdatei exportiert und von der Bank erfolgreich verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="4b197-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="4b197-111">Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)</span><span class="sxs-lookup"><span data-stu-id="4b197-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="4b197-112">Wählen Sie die Aktion **Zahlungseingang buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="4b197-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="4b197-113">Füllen Sie auf der Seite **Lastschrift buchen** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="4b197-113">On the **Post Direct Debit Collection** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="4b197-114">Feld</span><span class="sxs-lookup"><span data-stu-id="4b197-114">Field</span></span>|<span data-ttu-id="4b197-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b197-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="4b197-116">**Basislastschriftnr.**</span><span class="sxs-lookup"><span data-stu-id="4b197-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="4b197-117">Geben Sie den Basislastschrifteinzug an, für den Sie den Zahlungseingang buchen wollen.</span><span class="sxs-lookup"><span data-stu-id="4b197-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="4b197-118">**Fibu Erf.-Journalvorlage**</span><span class="sxs-lookup"><span data-stu-id="4b197-118">**General Journal Template**</span></span>|<span data-ttu-id="4b197-119">Geben Sie an, welche Fibu Erf.-Journalvorlage zum Buchen des Zahlungseingangs verwendet werden soll, etwa die Vorlage für Bareingänge.</span><span class="sxs-lookup"><span data-stu-id="4b197-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="4b197-120">**Fibu Erf.-Journalname**</span><span class="sxs-lookup"><span data-stu-id="4b197-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="4b197-121">Geben Sie an, welcher Fibu Erf.-Journalname für die Buchung des Zahlungseingangs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b197-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="4b197-122">**Nur Erf.-Journal erstellen**</span><span class="sxs-lookup"><span data-stu-id="4b197-122">**Create Journal Only**</span></span>|<span data-ttu-id="4b197-123">Markieren Sie dieses Kontrollkästchen, wenn Sie den Zahlungseingang nicht buchen wollen, wenn Sie die Schaltfläche **OK** wählen.</span><span class="sxs-lookup"><span data-stu-id="4b197-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="4b197-124">Der Zahlungseingang wird in dem angegebenen Buch vorbereitet und erst gebucht, wenn jemand die fraglichen Erf.-Journal-Zeilen bucht.</span><span class="sxs-lookup"><span data-stu-id="4b197-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="4b197-125">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4b197-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4b197-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b197-126">See Also</span></span>  
 <span data-ttu-id="4b197-127">[Erfassen von Zahlungen per Basislastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="4b197-127">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="4b197-128">Verkauf</span><span class="sxs-lookup"><span data-stu-id="4b197-128">Sales</span></span>](sales-manage-sales.md)
