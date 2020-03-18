---
title: Elektronische Zahlungen (Schweiz)
description: Schweizer Erweiterungen ermöglichen Ihnen, elektronisch Rechnungen an Debitoren zu senden. Sie können Rechnungen direkt mithilfe der Onlinebankingsoftware des Debitors ausstellen und bezahlen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 859d1a9a6fd654e798fd42aef1e43abe3bd28cf6
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076774"
---
# <a name="swiss-electronic-payments"></a><span data-ttu-id="b02e7-104">Elektronische Zahlungen (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="b02e7-104">Swiss Electronic Payments</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)]<span data-ttu-id="b02e7-105">ermöglicht Ihnen, elektronisch Rechnungen an Debitoren zu senden.</span><span class="sxs-lookup"><span data-stu-id="b02e7-105">allows you to send invoices to customers electronically.</span></span> <span data-ttu-id="b02e7-106">Sie können Rechnungen direkt mithilfe der Onlinebankingsoftware des Debitors ausstellen und bezahlen.</span><span class="sxs-lookup"><span data-stu-id="b02e7-106">The invoices are presented and paid directly using the customer's online banking software.</span></span>  

## <a name="electronic-payment-methods"></a><span data-ttu-id="b02e7-107">Elektronische Zahlungsformen</span><span class="sxs-lookup"><span data-stu-id="b02e7-107">Electronic Payment Methods</span></span>  
<span data-ttu-id="b02e7-108">Elektronische Zahlungen können mithilfe der folgenden Zahlungsformen durchgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="b02e7-108">You can make electronic payments using the following methods:</span></span>  

- <span data-ttu-id="b02e7-109">Einzahlungsschein mit Referenznummer (ESR)</span><span class="sxs-lookup"><span data-stu-id="b02e7-109">Einzahlungsschein mit Referenznummer (ESR)</span></span>  
- <span data-ttu-id="b02e7-110">Lastschrift Verfahren (LSV+)</span><span class="sxs-lookup"><span data-stu-id="b02e7-110">Lastschrift Verfahren (LSV+)</span></span>  
- <span data-ttu-id="b02e7-111">SEPA Kreditübertragungen</span><span class="sxs-lookup"><span data-stu-id="b02e7-111">SEPA credit transfers</span></span>  

## <a name="esr"></a><span data-ttu-id="b02e7-112">ESR</span><span class="sxs-lookup"><span data-stu-id="b02e7-112">ESR</span></span>  
<span data-ttu-id="b02e7-113">ESR ist ein elektronischer Kreditorendienst, der Zahlungsscheine zum Einziehen von Geld verwendet.</span><span class="sxs-lookup"><span data-stu-id="b02e7-113">ESR is an electronic debtor service that uses payment slips to collect money.</span></span> <span data-ttu-id="b02e7-114">Es ist das elektronische Standardzahlungssystem, das von Swiss Post ins Leben gerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b02e7-114">It is the standard electronic payment system created by Swiss Post.</span></span> <span data-ttu-id="b02e7-115">ESR-Zahlungsscheine können als Rechnungsanlage gedruckt, ESR-Referenznummern berechnet und ESR-Dateien, die Zahlungsinformationen von Banken enthalten, importiert werden.</span><span class="sxs-lookup"><span data-stu-id="b02e7-115">You can print ESR payment slips as invoice attachments, calculate ESR reference numbers, and import ESR files that have payment information from banks.</span></span> <span data-ttu-id="b02e7-116">Weitere Informationen erhalten Sie unter [Elektronische Zahlungen mit ESR (Schweiz)](how-to-print-esr-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="b02e7-116">For more information, see [Swiss Electronic Payments Using ESR](how-to-print-esr-invoices.md).</span></span> <span data-ttu-id="b02e7-117">Sie können auch ESR- und ESR+-Zahlungen mithilfe der Version dieser Zahlungsform der Bank machen, die Bank-ESR (BESR) heisst.</span><span class="sxs-lookup"><span data-stu-id="b02e7-117">You can also make ESR and ESR+ payments using the bank’s version of this payment method, which is named Bank-ESR (BESR).</span></span>  

## <a name="lsv"></a><span data-ttu-id="b02e7-118">LSV+</span><span class="sxs-lookup"><span data-stu-id="b02e7-118">LSV+</span></span>  
<span data-ttu-id="b02e7-119">LSV+ ist ein Abbuchungsdienst, der für das Bearbeiten von Zahlungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b02e7-119">LSV+ is a direct debit service that is used for processing payments.</span></span> <span data-ttu-id="b02e7-120">Unternehmen können Debitorenzahlungen direkt von der Bank des Debitors mit der Abbuchung freigeben.</span><span class="sxs-lookup"><span data-stu-id="b02e7-120">Companies can release customer payments directly from the customer's bank using direct debit.</span></span> <span data-ttu-id="b02e7-121">Debitorenzahlungen per Lastschrift können im LSV+-Bankformat oder im DebitDirect PostFinance-Format angefordert bzw. eingezogen werden.</span><span class="sxs-lookup"><span data-stu-id="b02e7-121">You can request and collect customer payments using direct debit in the LSV+ bank format, or in the DebitDirect PostFinance format.</span></span> <span data-ttu-id="b02e7-122">Weitere Informationen erhalten Sie unter [Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md).</span><span class="sxs-lookup"><span data-stu-id="b02e7-122">For more information, see [Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md).</span></span>  

## <a name="sepa-credit-transfers"></a><span data-ttu-id="b02e7-123">SEPA Kreditübertragungen</span><span class="sxs-lookup"><span data-stu-id="b02e7-123">SEPA Credit Transfers</span></span>  
<span data-ttu-id="b02e7-124">Um Zahlungsvorschläge entsprechend dem SEPA-Standard zu exportieren, müssen Sie ein Bankkonto verwenden.</span><span class="sxs-lookup"><span data-stu-id="b02e7-124">To export payments according to the SEPA standard, you must use a bank account.</span></span> <span data-ttu-id="b02e7-125">Um sicherzustellen, dass die entsprechenden Fibuposten mit den generierten für lokale Schweizer Zahlungsformen übereinstimmen (siehe oben), muss der Wert im Feld **Bankkonto Buchungsgruppe** auf der Seite **Bankkontokarte** auf das jeweilige Fibukonto weisen.</span><span class="sxs-lookup"><span data-stu-id="b02e7-125">To make sure that the related general ledger entries are consistent with those generated for local Swiss payment methods (see above), the value in the **Bank Acc. Posting Group** field on the **Bank Account Card** page must point to the relevant general ledger account.</span></span> <span data-ttu-id="b02e7-126">Weitere Informationen zum Exportieren von SEPA-Zahlungen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](../../finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).</span><span class="sxs-lookup"><span data-stu-id="b02e7-126">For more information about how to export SEPA payments, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](../../finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)).</span></span>  

## <a name="see-also"></a><span data-ttu-id="b02e7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b02e7-127">See Also</span></span>  
 <span data-ttu-id="b02e7-128">[Importieren von Schweizer Bankenclearingnummern](how-to-import-swiss-bank-clearing-numbers.md) </span><span class="sxs-lookup"><span data-stu-id="b02e7-128">[Import Swiss Bank Clearing Numbers](how-to-import-swiss-bank-clearing-numbers.md) </span></span>  
 <span data-ttu-id="b02e7-129">[Elektronische Zahlungen mit ESR (Schweiz)](swiss-electronic-payments-using-esr.md) </span><span class="sxs-lookup"><span data-stu-id="b02e7-129">[Swiss Electronic Payments Using ESR](swiss-electronic-payments-using-esr.md) </span></span>  
 <span data-ttu-id="b02e7-130">[Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md) </span><span class="sxs-lookup"><span data-stu-id="b02e7-130">[Print ESR Invoices](how-to-print-esr-invoices.md) </span></span>  
 <span data-ttu-id="b02e7-131">[Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="b02e7-131">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 <span data-ttu-id="b02e7-132">[Lokale Funktion (Schweiz)](switzerland-local-functionality.md)  ' [Zahlungen vornehmen](../../payables-make-payments.md)</span><span class="sxs-lookup"><span data-stu-id="b02e7-132">[Switzerland Local Functionality](switzerland-local-functionality.md)  ' [Making Payments](../../payables-make-payments.md)</span></span>
