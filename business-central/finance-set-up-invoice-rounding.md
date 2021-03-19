---
title: Einrichten der Rechnungsrundung | Microsoft Docs
description: Sie können Rechnungsbeträge beim Erstellen von Rechnungen runden. Darüber hinaus muss die Rechnungsrundung möglicherweise aufgrund lokaler Vorgaben oder üblicher Vorgehensweisenauf eine bestimmte Weise erfolgen – beispielsweise auf einen Betrag, der durch 0,05 teilbar ist.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 59be392bd10805728af2c060e8a2ea2ecab6bb73
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392288"
---
# <a name="set-up-invoice-rounding"></a><span data-ttu-id="b0e99-104">Einrichten der Rechnungsrundung</span><span class="sxs-lookup"><span data-stu-id="b0e99-104">Set Up Invoice Rounding</span></span>
<span data-ttu-id="b0e99-105">Wenn Sie beim Erstellen von Rechnungen Rechnungsbeträge runden müssen, können Sie die automatische Rundungsfunktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="b0e99-105">If you need to round invoice amounts when you create invoices, you can use the automatic rounding function.</span></span> <span data-ttu-id="b0e99-106">Nach dem Runden einer Rechnung wird eine zusätzliche Zeile mit dem Rundungsbetrag eingefügt, die zusammen mit den anderen Rechnungszeilen gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="b0e99-106">When an invoice is rounded, an extra line is added with the rounding amount and posted with the other invoice lines.</span></span>

> [!NOTE]  
>  <span data-ttu-id="b0e99-107">Aufgrund gesetzlicher Vorgaben oder üblicher Vorgehensweisen muss die Rechnungsrundung möglicherweise auf eine bestimmte Weise erfolgen – beispielsweise auf einen Betrag, der durch 0,05 teilbar ist.</span><span class="sxs-lookup"><span data-stu-id="b0e99-107">Local regulations or local custom may require the invoice to be rounded in a specific way, for example, to an amount divisible by 0.05.</span></span>  

<span data-ttu-id="b0e99-108">Zum Verwenden der automatischen Rechnungsrundung müssen folgende Aktionen ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="b0e99-108">To use automatic invoice rounding, you must:</span></span>  

* <span data-ttu-id="b0e99-109">Geben Sie die Fibukonten zum Buchen der Rundungsdifferenzen an.</span><span class="sxs-lookup"><span data-stu-id="b0e99-109">Specify the general ledger accounts to which rounding differences will be posted.</span></span>  
* <span data-ttu-id="b0e99-110">Richten Sie Regeln für das Runden von Rechnungen in Mandanten- und Fremdwährung an.</span><span class="sxs-lookup"><span data-stu-id="b0e99-110">Set up rules for rounding invoices in local currency and in foreign currency.</span></span>  
* <span data-ttu-id="b0e99-111">Aktivieren Sie die Funktion.</span><span class="sxs-lookup"><span data-stu-id="b0e99-111">Activate the function.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b0e99-112">Zusätzlich zu den Rechnungsrundungsfeatures besteht auch die Möglichkeit, Beträge in Rechnungen mithilfe der Stückpreisrundung und der Betragsrundung zu runden.</span><span class="sxs-lookup"><span data-stu-id="b0e99-112">In addition to the invoice rounding features, you can round amounts on invoices by the unit-amount rounding feature and the amount rounding feature.</span></span>  

## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="b0e99-113">Fibukonten für Rechnungsrundungsdifferenzen einrichten</span><span class="sxs-lookup"><span data-stu-id="b0e99-113">Set up general ledger accounts for invoice rounding differences</span></span>
<span data-ttu-id="b0e99-114">Um die automatische Rundungsfunktion zu nutzen, müssen Sie Fibukonten einrichten, auf die Rundungsdifferenzen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="b0e99-114">To use the automatic invoice rounding function, you must set up the general ledger account or accounts where rounding differences will be posted.</span></span> <span data-ttu-id="b0e99-115">Bevor Sie dies tun können, müssen Sie die MWST-Produktbuchungsgruppen einrichten.</span><span class="sxs-lookup"><span data-stu-id="b0e99-115">Before you can do this, you must set up VAT product posting groups.</span></span> <span data-ttu-id="b0e99-116">Weitere Informationen finden Sie unter [MWST einrichten](finance-setup-vat.md).</span><span class="sxs-lookup"><span data-stu-id="b0e99-116">For more information, see [Set up VAT](finance-setup-vat.md).</span></span>  

### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="b0e99-117">Fibukonten für Rechnungsrundungsdifferenzen einrichten:</span><span class="sxs-lookup"><span data-stu-id="b0e99-117">To set up general ledger accounts for invoice rounding differences</span></span>  
1. <span data-ttu-id="b0e99-118">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="b0e99-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b0e99-119">Richten Sie das Konto im Fenster **Kontenplan** ein, und benennen Sie es mit **Rechnungsrundung** oder mit einem ähnlichen Namen.</span><span class="sxs-lookup"><span data-stu-id="b0e99-119">On the **Chart of Accounts** page, set up the account and name it **Invoice Rounding** or something similar.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)]<span data-ttu-id="b0e99-120">Die Anwendung verwendet den Kontonamen als Text in gerundeten Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="b0e99-120">will use the account name as text for invoices that are rounded.</span></span>  
3. <span data-ttu-id="b0e99-121">Abhängig davon, ob Sie Mehrwertsteuer oder Salestax verwenden, wählen Sie in den Feldern **Salestax-Produktbuchungsgruppe** oder **MWST-Produktbuchungsgruppe** eine Buchungsgruppe für Rundungsbeträge aus.</span><span class="sxs-lookup"><span data-stu-id="b0e99-121">Depending on whether you use VAT or sales tax, in the **Tax Prod. Posting Group** or **VAT Prod. Posting Group** fields, choose a posting group for rounded amounts.</span></span> <span data-ttu-id="b0e99-122">Es empfiehlt sich, eine neuen Gruppencode einzurichten, der für die Rechnungsrundung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b0e99-122">You may want to set up a new group code to use for invoice rounding.</span></span>
4. <span data-ttu-id="b0e99-123">Lassen Sie die Felder **Buchungsart** und **Salestax-Produktbuchungsgruppe** oder **MWST-Produktbuchungsgruppe** leer.</span><span class="sxs-lookup"><span data-stu-id="b0e99-123">Leave the **Gen. Posting Type**, and either the **Tax Bus. Posting Group** or **VAT Bus. Posting Group** fields blank.</span></span> <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

<span data-ttu-id="b0e99-124">Jetzt können Sie das Rechnungsrundungskonto den Buchungsgruppen auf der Seite **Kreditorenbuchungsgruppen** zuordnen.</span><span class="sxs-lookup"><span data-stu-id="b0e99-124">Now you can assign the invoice rounding account to posting groups on the **Vendor Posting Groups** page.</span></span>  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a><span data-ttu-id="b0e99-125">Rundungsregeln für Fremdwährungen und lokale Währungen einrichten</span><span class="sxs-lookup"><span data-stu-id="b0e99-125">Set up rounding for foreign and local currencies</span></span>
<span data-ttu-id="b0e99-126">Damit Sie die automatische Rechnungsrundungsfunktion verwenden können, müssen Sie Rundungsregeln für Fremdwährungen und lokale Währungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="b0e99-126">Before you can use the automatic invoice rounding function, you must set up rounding rules for foreign and local currencies.</span></span>

### <a name="to-set-up-rounding-for-foreign-currencies"></a><span data-ttu-id="b0e99-127">Einrichten von Rundungsregeln für Fremdwährungen</span><span class="sxs-lookup"><span data-stu-id="b0e99-127">To set up rounding for foreign currencies</span></span>  
1. <span data-ttu-id="b0e99-128">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Währungen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="b0e99-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b0e99-129">Füllen Sie auf der Seite **Währungen** die Fremdwährung aus, um die **Währungskarte** zu öffnen, und füllen Sie dann die Felder **Betragsrundungspräzision**, **Stückpreisrundungspräzision**, **Rechnungsrundungspräzision** und **Rechnungsrundungsmethode** aus.</span><span class="sxs-lookup"><span data-stu-id="b0e99-129">On the **Currencies** page, choose the foreign currency to open the **Currency Card**, and then fill in the **Amount Rounding Precision**, **Unit-Amount Rounding Precision**, **Invoice Rounding Precision** and **Invoice Rounding Type** fields.</span></span>

### <a name="to-set-up-rounding-for-your-local-currency"></a><span data-ttu-id="b0e99-130">Einrichten der Rundung für Ihre lokale Währung</span><span class="sxs-lookup"><span data-stu-id="b0e99-130">To set up rounding for your local currency</span></span>
1. <span data-ttu-id="b0e99-131">Wählen Sie die ![Glühbirne, die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Fibuposteneinrichtung** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="b0e99-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b0e99-132">Füllen Sie auf der Seite **Fibu Einrichtung** auf dem Inforegister **Allgemein** die Felder **Rechnungsrundungspräz.** und **Rechnungsrundungsmethode** aus.</span><span class="sxs-lookup"><span data-stu-id="b0e99-132">On the **General Ledger Setup** page, on the **General** FastTab, fill in the **Inv. Rounding Precision** and **Inv. Rounding Type** fields.</span></span>  

## <a name="activate-the-invoice-rounding-function"></a><span data-ttu-id="b0e99-133">Aktivieren der Rechnungsrundungsfunktion</span><span class="sxs-lookup"><span data-stu-id="b0e99-133">Activate the invoice rounding function</span></span>  
<span data-ttu-id="b0e99-134">Damit die Anwendung Einkaufs- und Verkaufsrechnungen automatisch gerundet werden, müssen Sie die Rechnungsrundungsfunktion aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b0e99-134">To ensure that sales and purchase invoices are rounded automatically, you must activate the invoice rounding function.</span></span> <span data-ttu-id="b0e99-135">Beachten Sie, dass Sie die Rechnungsrundung einzeln für Verkaufsrechnungen und Einkaufsrechnungen aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="b0e99-135">You activate invoice rounding separately for sales and purchase invoices.</span></span>

1. <span data-ttu-id="b0e99-136">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Verkauf und Forderungen – Einrichtung** oder **Einkauf und Verbindlichkeiten – Einrichtung** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="b0e99-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup** or **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b0e99-137">Markieren Sie im Inforegister **Allgemein** das Kontrollkästchen **Rechnungsrundung**.</span><span class="sxs-lookup"><span data-stu-id="b0e99-137">On the **General** FastTab, choose the **Invoice Rounding** check box.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b0e99-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0e99-138">See Also</span></span>  
[<span data-ttu-id="b0e99-139">Fakturieren eines Verkaufs</span><span class="sxs-lookup"><span data-stu-id="b0e99-139">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="b0e99-140">Erfassen eines Einkaufs</span><span class="sxs-lookup"><span data-stu-id="b0e99-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]