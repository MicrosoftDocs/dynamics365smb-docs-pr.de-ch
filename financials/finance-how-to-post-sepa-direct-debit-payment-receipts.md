---
title: SEPA Lastschriftzahlungen | Microsoft Docs
description: "Wenn ein Basislastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5beb5f6795bd7f4943a6ed9d8b691c05fc5ecb63
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="40698-103">Vorgehensweise: SEPA-Basislastschrift-Zahlungseingänge buchen</span><span class="sxs-lookup"><span data-stu-id="40698-103">How to: Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="40698-104">Wenn ein Basislastschrifteinzug von Ihrer Bank erfolgreich verarbeitet wird, können Sie den Eingang der Zahlungen für die betreffenden Verkaufsrechnungen buchen.</span><span class="sxs-lookup"><span data-stu-id="40698-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="40698-105">Weitere Informationen finden Sie unter [Vorgehensweise: SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)</span><span class="sxs-lookup"><span data-stu-id="40698-105">For more information, see [How to: Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="40698-106">Sie können der Zahlungseingang direkt aus dem **Lastschriften** oder im **Direct Debit Collect. Posten** buchen.</span><span class="sxs-lookup"><span data-stu-id="40698-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="40698-107">Sie können auch die Arbeit an einen anderen Benutzer übertragen, indem Sie die zugehörigen Erf.-Journalzeilen vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="40698-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="40698-108">Buchen eines Basislastschrifteingangs im Basislastschriftfenster</span><span class="sxs-lookup"><span data-stu-id="40698-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="40698-109">Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Berichtsymbol suchen") und geben **Lastschriften** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="40698-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="40698-110">Wählen Sie eine Zeile für die Basislastschrifterfassung, die in eine Bankdatei exportiert und von der Bank erfolgreich verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="40698-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="40698-111">Weitere Informationen finden Sie unter [Vorgehensweise: SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)</span><span class="sxs-lookup"><span data-stu-id="40698-111">For more information, see [How to: Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="40698-112">Wählen Sie die Aktion **Zahlungseingang buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="40698-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="40698-113">Füllen Sie im Fenster **Lastschrift erstellen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="40698-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="40698-114">Feld</span><span class="sxs-lookup"><span data-stu-id="40698-114">Field</span></span>|<span data-ttu-id="40698-115">Description</span><span class="sxs-lookup"><span data-stu-id="40698-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="40698-116">**Basislastschriftnr.**</span><span class="sxs-lookup"><span data-stu-id="40698-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="40698-117">Geben Sie den Basislastschrifteinzug an, für den Sie den Zahlungseingang buchen wollen.</span><span class="sxs-lookup"><span data-stu-id="40698-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="40698-118">**Fibu Erf.-Journalvorlage**</span><span class="sxs-lookup"><span data-stu-id="40698-118">**General Journal Template**</span></span>|<span data-ttu-id="40698-119">Geben Sie an, welche Fibu Erf.-Journalvorlage zum Buchen des Zahlungseingangs verwendet werden soll, etwa die Vorlage für Bareingänge.</span><span class="sxs-lookup"><span data-stu-id="40698-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="40698-120">**Fibu Erf.-Journalname**</span><span class="sxs-lookup"><span data-stu-id="40698-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="40698-121">Geben Sie an, welcher Fibu Erf.-Journalname für die Buchung des Zahlungseingangs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="40698-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="40698-122">**Nur Erf.-Journal erstellen**</span><span class="sxs-lookup"><span data-stu-id="40698-122">**Create Journal Only**</span></span>|<span data-ttu-id="40698-123">Markieren Sie dieses Kontrollkästchen, wenn Sie den Zahlungseingang nicht buchen wollen, wenn Sie die Schaltfläche **OK** wählen.</span><span class="sxs-lookup"><span data-stu-id="40698-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="40698-124">Der Zahlungseingang wird in dem angegebenen Buch vorbereitet und erst gebucht, wenn jemand die fraglichen Erf.-Journal-Zeilen bucht.</span><span class="sxs-lookup"><span data-stu-id="40698-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="40698-125">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="40698-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="40698-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40698-126">See Also</span></span>  
 <span data-ttu-id="40698-127">[Erfassen von Zahlungen per Basislastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="40698-127">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="40698-128">Verkauf</span><span class="sxs-lookup"><span data-stu-id="40698-128">Sales</span></span>](sales-manage-sales.md)

