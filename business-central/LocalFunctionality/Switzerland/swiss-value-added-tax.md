---
title: Mehrwertsteuer (Schweiz)
description: Schweizer Erweiterungen enthalten spezielle Mehrwertsteuerberichterstellungsfunktionen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d0a9c4bc1f589d8de1b137ea1e2a6363f6f5f969
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244807"
---
# <a name="swiss-value-added-tax"></a><span data-ttu-id="d06e4-103">Mehrwertsteuer (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="d06e4-103">Swiss Value Added Tax</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="d06e4-104">enthält die folgenden Erweiterungen für die Schweizer Mehrwertsteuerberichterstellung:</span><span class="sxs-lookup"><span data-stu-id="d06e4-104">includes the following enhancements to Swiss VAT reporting:</span></span>  

- <span data-ttu-id="d06e4-105">Automatische Regulierung von MWST-Beträgen für Rechnungen entsprechend dem Skonto</span><span class="sxs-lookup"><span data-stu-id="d06e4-105">Automatic adjustment of VAT amounts for invoices, according to payment discounts.</span></span>  
- <span data-ttu-id="d06e4-106">Zusätzliche MWST-Wechselkurse für Rechnungen in Fremdwährungen</span><span class="sxs-lookup"><span data-stu-id="d06e4-106">Additional VAT exchange rates for invoices in foreign currencies.</span></span>  

<span data-ttu-id="d06e4-107">Weitere Informationen über die Schweizer Mehrwertsteuerberichterstellung und die Codierungsanforderungen finden Sie unter [Schweizer MWST-Informationen](https://www.estv.admin.ch/estv/en/home/estv-suissetax/sw-hersteller.html).</span><span class="sxs-lookup"><span data-stu-id="d06e4-107">For more information about Swiss VAT reporting and coding requirements, see [Swiss VAT Information](https://www.estv.admin.ch/estv/en/home/estv-suissetax/sw-hersteller.html).</span></span> <span data-ttu-id="d06e4-108">Die Information ist für Französisch, Deutsch und Italienisch verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d06e4-108">The information is available in French, German, and Italian.</span></span>  

## <a name="vat-amounts-and-vat-exchange-rates"></a><span data-ttu-id="d06e4-109">MWST-Beträge und MWST-Wechselkurse</span><span class="sxs-lookup"><span data-stu-id="d06e4-109">VAT Amounts and VAT Exchange Rates</span></span>  
<span data-ttu-id="d06e4-110">Entsprechend den lokalen Mehrwertsteuer-Gesetzen kann der MWST Basisbetrag um den Skontobetrag reduziert werden, wenn Skonto gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="d06e4-110">According to local VAT laws, the VAT base amount for an invoice can be reduced by the payment discount if a discount is granted.</span></span> <span data-ttu-id="d06e4-111">Um automatische Mehrwertsteueranpassungen für ein Skonto einer Rechnung zuzulassen wir das Feld **Skonto berichtigen** standardmässig auf der Seite **Fibuposten Einrichtung** ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d06e4-111">To allow automatic VAT adjustment for a payment discount on an invoice, the **Adjust for Payment Discount** field is activated by default on the **General Ledger Setup** page.</span></span> <span data-ttu-id="d06e4-112">Sie können diese Funktion in der MWST-Buchungsmatrix-Einrichtung " aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d06e4-112">You can also activate this function in the VAT posting setup.</span></span> <span data-ttu-id="d06e4-113">Weitere Informationen finden Sie in der Tabelle "Fibuposten einrichten" und "MWST-Buchungsmatrix einrichten".</span><span class="sxs-lookup"><span data-stu-id="d06e4-113">For more information, see the General Ledger Setup table and the VAT Posting Setup table.</span></span>  

### <a name="currency-exchange-rates-for-vat-reporting"></a><span data-ttu-id="d06e4-114">Währungswechselkurse für die MWST-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="d06e4-114">Currency Exchange Rates for VAT Reporting</span></span>  
<span data-ttu-id="d06e4-115">Für Rechnungen in Fremdwährungen muss der offizielle Wechselkurs der Regierung für die MWST-Berechnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d06e4-115">For invoices in foreign currency, you must use the official exchange rate provided by the government for the VAT calculation itself.</span></span> <span data-ttu-id="d06e4-116">Sie können zusätzliche MWST-Wechselkurse einrichten, die für andere Rechnungsbelange als die MWST-Berechnung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d06e4-116">You can also set up additional exchange rates for VAT, which you can use for aspects of the invoice other than the VAT calculation.</span></span> <span data-ttu-id="d06e4-117">Der korrekte offizielle MWST-Wechselkurs kann für jede relevante Fremdwährung in der Wechselkurseinrichtung für Rechnungen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d06e4-117">You can provide the correct government VAT exchange rate for each relevant foreign currency in the exchange rate setup for invoices.</span></span> <span data-ttu-id="d06e4-118">Weitere Informationen finden Sie in der Tabelle "Wechselkurse".</span><span class="sxs-lookup"><span data-stu-id="d06e4-118">For more information, see the Currency Exchange Rate table.</span></span>  

<span data-ttu-id="d06e4-119">Es ist auch möglich, alle aus Fremdwährungstransaktionen resultierenden MWST-Beträge in MWST-Posten zu regulieren.</span><span class="sxs-lookup"><span data-stu-id="d06e4-119">You can also adjust all VAT amounts in VAT entries that result from foreign currency transactions.</span></span> <span data-ttu-id="d06e4-120">Wenn Sie die Funktion für die MWST-Wechselkursregulierung aktivieren, werden die MWST-Wechselkurse automatisch reguliert.</span><span class="sxs-lookup"><span data-stu-id="d06e4-120">When you activate the adjust VAT exchange rate function, VAT exchange rates are adjusted automatically.</span></span> <span data-ttu-id="d06e4-121">Die durch Wechselkurse verursachten positiven Differenzen werden auf Kursgewinnkonten gebucht.</span><span class="sxs-lookup"><span data-stu-id="d06e4-121">The positive differences that result from exchange rates are posted to exchange rate gain accounts.</span></span> <span data-ttu-id="d06e4-122">Die durch Wechselkurse verursachten negativen Differenzen werden auf Kursverlustkonten gebucht.</span><span class="sxs-lookup"><span data-stu-id="d06e4-122">The negative differences that result from exchange rates are posted to exchange rate loss accounts.</span></span> <span data-ttu-id="d06e4-123">Weitere Informationen finden Sie unter Stapelverarbeitungsauftrag "Wechselkurse regulieren".</span><span class="sxs-lookup"><span data-stu-id="d06e4-123">For more information, see the Adjust Exchange Rates batch job.</span></span>  

<span data-ttu-id="d06e4-124">In die MWST-Posten werden weitere Angaben übertragen, z. B. der MWST-Satz und der ursprüngliche Währungsbetrag.</span><span class="sxs-lookup"><span data-stu-id="d06e4-124">Additional information, such as VAT rate and original currency amount, is transferred to the VAT entries.</span></span> <span data-ttu-id="d06e4-125">Weitere Informationen finden Sie in der MWST-Postentabelle.</span><span class="sxs-lookup"><span data-stu-id="d06e4-125">For more information, see the VAT Entry table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d06e4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d06e4-126">See Also</span></span>  
 <span data-ttu-id="d06e4-127">[MWST-Sätze für die Schweiz](vat-rates-for-switzerland.md) </span><span class="sxs-lookup"><span data-stu-id="d06e4-127">[VAT Rates for Switzerland](vat-rates-for-switzerland.md) </span></span>  
 <span data-ttu-id="d06e4-128">[Erstellen und Drucken einer Schweizer MWST-Abrechnung](how-to-create-and-print-a-swiss-vat-statement.md) </span><span class="sxs-lookup"><span data-stu-id="d06e4-128">[Create and Print a Swiss VAT Statement](how-to-create-and-print-a-swiss-vat-statement.md) </span></span>  
 [<span data-ttu-id="d06e4-129">Lokale Funktion (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="d06e4-129">Switzerland Local Functionality</span></span>](switzerland-local-functionality.md)   
