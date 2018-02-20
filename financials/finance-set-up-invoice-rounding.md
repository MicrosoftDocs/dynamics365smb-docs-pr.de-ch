---
title: Einrichten der Rechnungsrundung | Microsoft Docs
description: "Sie können Rechnungsbeträge beim Erstellen von Rechnungen runden. Darüber hinaus muss die Rechnungsrundung möglicherweise aufgrund lokaler Vorgaben oder üblicher Vorgehensweisenauf eine bestimmte Weise erfolgen – beispielsweise auf einen Betrag, der durch 0,05 teilbar ist."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ceebeeac325c00d6aef25d8ca51fcfee1ab4e1d5
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-invoice-rounding"></a><span data-ttu-id="67ddd-104">Einrichten der Rechnungsrundung</span><span class="sxs-lookup"><span data-stu-id="67ddd-104">Set Up Invoice Rounding</span></span>
<span data-ttu-id="67ddd-105">Wenn Sie beim Erstellen von Rechnungen Rechnungsbeträge runden müssen, können Sie die automatische Rundungsfunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="67ddd-105">If you need to round invoice amounts when you create invoices, you can use the automatic rounding function.</span></span> <span data-ttu-id="67ddd-106">Nach dem Runden einer Rechnung wird eine zusätzliche Zeile mit dem Rundungsbetrag eingefügt, die zusammen mit den anderen Rechnungszeilen gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="67ddd-106">When an invoice is rounded, an extra line is added with the rounding amount and posted with the other invoice lines.</span></span>

> [!NOTE]  
>  <span data-ttu-id="67ddd-107">Aufgrund gesetzlicher Vorgaben oder üblicher Vorgehensweisen muss die Rechnungsrundung möglicherweise auf eine bestimmte Weise erfolgen – beispielsweise auf einen Betrag, der durch 0,05 teilbar ist.</span><span class="sxs-lookup"><span data-stu-id="67ddd-107">Local regulations or local custom may require the invoice to be rounded in a specific way, for example, to an amount divisible by 0.05.</span></span>  
  
<span data-ttu-id="67ddd-108">Zum Verwenden der automatischen Rechnungsrundung müssen folgende Aktionen ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="67ddd-108">To use automatic invoice rounding, you must:</span></span>  
  
* <span data-ttu-id="67ddd-109">Geben Sie die Fibukonten zum Buchen der Rundungsdifferenzen an.</span><span class="sxs-lookup"><span data-stu-id="67ddd-109">Specify the general ledger accounts to which rounding differences will be posted.</span></span>  
* <span data-ttu-id="67ddd-110">Richten Sie Regeln für das Runden von Rechnungen in Mandanten- und Fremdwährung an.</span><span class="sxs-lookup"><span data-stu-id="67ddd-110">Set up rules for rounding invoices in local currency and in foreign currency.</span></span>  
* <span data-ttu-id="67ddd-111">Aktivieren Sie die Funktion.</span><span class="sxs-lookup"><span data-stu-id="67ddd-111">Activate the function.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="67ddd-112">Zusätzlich zu den Rechnungsrundungsfeatures besteht auch die Möglichkeit, Beträge in Rechnungen mithilfe der Stückpreisrundung und der Betragsrundung zu runden.</span><span class="sxs-lookup"><span data-stu-id="67ddd-112">In addition to the invoice rounding features, you can round amounts on invoices by the unit-amount rounding feature and the amount rounding feature.</span></span>  
 
## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="67ddd-113">Fibukonten für Rechnungsrundungsdifferenzen einrichten</span><span class="sxs-lookup"><span data-stu-id="67ddd-113">Set up general ledger accounts for invoice rounding differences</span></span>
<span data-ttu-id="67ddd-114">Um die automatische Rundungsfunktion zu nutzen, müssen Sie Sachkonten einrichten, auf die Rundungsdifferenzen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="67ddd-114">To use the automatic invoice rounding function, you must set up the general ledger account or accounts where rounding differences will be posted.</span></span> <span data-ttu-id="67ddd-115">Bevor Sie dies tun können, müssen Sie die MWST-Produktbuchungsgruppen einrichten.</span><span class="sxs-lookup"><span data-stu-id="67ddd-115">Before you can do this, you must set up VAT product posting groups.</span></span> <span data-ttu-id="67ddd-116">Weitere Informationen finden Sie unter [MWST einrichten](finance-setup-vat.md).</span><span class="sxs-lookup"><span data-stu-id="67ddd-116">For more information, see [Set up VAT](finance-setup-vat.md).</span></span>  
  
### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="67ddd-117">Sachkonten für Rechnungsrundungsdifferenzen einrichten:</span><span class="sxs-lookup"><span data-stu-id="67ddd-117">To set up general ledger accounts for invoice rounding differences</span></span>  
1. <span data-ttu-id="67ddd-118">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben **Kontenplan** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="67ddd-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="67ddd-119">Richten Sie das Konto im Fenster **Kontenplan** ein, und benennen Sie es mit **Rechnungsrundung** oder mit einem ähnlichen Namen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-119">On the **Chart of Accounts** page, set up the account and name it **Invoice Rounding** or something similar.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="67ddd-120">Die Anwendung verwendet den Kontonamen als Text in gerundeten Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-120"> will use the account name as text for invoices that are rounded.</span></span>  
3. <span data-ttu-id="67ddd-121">Abhängig davon, ob Sie Mehrwertsteuer oder Salestax verwenden, wählen Sie in den Feldern **Salestax-Produktbuchungsgruppe** oder **MWST-Produktbuchungsgruppe** eine Buchungsgruppe für Rundungsbeträge aus.</span><span class="sxs-lookup"><span data-stu-id="67ddd-121">Depending on whether you use VAT or sales tax, in the **Tax Prod. Posting Group** or **VAT Prod. Posting Group** fields, choose a posting group for rounded amounts.</span></span> <span data-ttu-id="67ddd-122">Es empfiehlt sich, eine neuen Gruppencode einzurichten, der für die Rechnungsrundung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="67ddd-122">You may want to set up a new group code to use for invoice rounding.</span></span>
4. <span data-ttu-id="67ddd-123">Lassen Sie die Felder **Buchungsart** und **Salestax-Produktbuchungsgruppe** oder **MWST-Produktbuchungsgruppe** leer.</span><span class="sxs-lookup"><span data-stu-id="67ddd-123">Leave the **Gen. Posting Type**, and either the **Tax Bus. Posting Group** or **VAT Bus. Posting Group** fields blank.</span></span> <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  
  
<span data-ttu-id="67ddd-124">Jetzt können Sie das Rechnungsrundungskonto den Buchungsgruppen auf der Seite **Kreditorenbuchungsgruppen** zuordnen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-124">Now you can assign the invoice rounding account to posting groups on the **Vendor Posting Groups** page.</span></span>  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a><span data-ttu-id="67ddd-125">Rundungsregeln für Fremdwährungen und lokale Währungen einrichten</span><span class="sxs-lookup"><span data-stu-id="67ddd-125">Set up rounding for foreign and local currencies</span></span>
<span data-ttu-id="67ddd-126">Damit Sie die automatische Rechnungsrundungsfunktion verwenden können, müssen Sie Rundungsregeln für Fremdwährungen und lokale Währungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="67ddd-126">Before you can use the automatic invoice rounding function, you must set up rounding rules for foreign and local currencies.</span></span>

### <a name="to-set-up-rounding-for-foreign-currencies"></a><span data-ttu-id="67ddd-127">Einrichten von Rundungsregeln für Fremdwährungen</span><span class="sxs-lookup"><span data-stu-id="67ddd-127">To set up rounding for foreign currencies</span></span>  
1. <span data-ttu-id="67ddd-128">Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") ein und wählen **Währungswechselkurs-Dienste** und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="67ddd-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="67ddd-129">Füllen Sie auf der Seite **Währungen** die Fremdwährung aus, um die **Währungskarte** zu öffnen, und füllen Sie dann die Felder **Betragsrundungspräzision**, **Stückpreisrundungspräzision**, **Rechnungsrundungspräzision** und **Rechnungsrundungsmethode** aus.</span><span class="sxs-lookup"><span data-stu-id="67ddd-129">On the **Currencies** page, choose the foreign currency to open the **Currency Card**, and then fill in the **Amount Rounding Precision**, **Unit-Amount Rounding Precision**, **Invoice Rounding Precision** and **Invoice Rounding Type** fields.</span></span>
  
### <a name="to-set-up-rounding-for-your-local-currency"></a><span data-ttu-id="67ddd-130">Einrichten der Rundung für Ihre lokale Währung</span><span class="sxs-lookup"><span data-stu-id="67ddd-130">To set up rounding for your local currency</span></span>
1. <span data-ttu-id="67ddd-131">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Finanzbuchhaltung einrichten** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="67ddd-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="67ddd-132">Füllen Sie auf der Seite **Fibu Einrichtung** auf dem Inforegister **Allgemein** die Felder **Rechnungsrundungspräz.** und **Rechnungsrundungsmethode** aus.</span><span class="sxs-lookup"><span data-stu-id="67ddd-132">On the **General Ledger Setup** page, on the **General** FastTab, fill in the **Inv. Rounding Precision** and **Inv. Rounding Type** fields.</span></span>  

## <a name="activate-the-invoice-rounding-function"></a><span data-ttu-id="67ddd-133">Aktivieren der Rechnungsrundungsfunktion</span><span class="sxs-lookup"><span data-stu-id="67ddd-133">Activate the invoice rounding function</span></span>  
<span data-ttu-id="67ddd-134">Damit die Anwendung Einkaufs- und Verkaufsrechnungen automatisch gerundet werden, müssen Sie die Rechnungsrundungsfunktion aktivieren.</span><span class="sxs-lookup"><span data-stu-id="67ddd-134">To ensure that sales and purchase invoices are rounded automatically, you must activate the invoice rounding function.</span></span> <span data-ttu-id="67ddd-135">Beachten Sie, dass Sie die Rechnungsrundung einzeln für Verkaufsrechnungen und Einkaufsrechnungen aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="67ddd-135">You activate invoice rounding separately for sales and purchase invoices.</span></span>

1. <span data-ttu-id="67ddd-136">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Debitoren & Verkauf Einrichtung** oder **Kreditoren & Einkauf Einrichtung** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="67ddd-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup** or **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="67ddd-137">Markieren Sie im Inforegister **Allgemein** das Kontrollkästchen **Rechnungsrundung**.</span><span class="sxs-lookup"><span data-stu-id="67ddd-137">On the **General** FastTab, choose the **Invoice Rounding** check box.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67ddd-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67ddd-138">See Also</span></span>  
[<span data-ttu-id="67ddd-139">Verkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="67ddd-139">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="67ddd-140">Erfassen eines Einkaufs</span><span class="sxs-lookup"><span data-stu-id="67ddd-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)
