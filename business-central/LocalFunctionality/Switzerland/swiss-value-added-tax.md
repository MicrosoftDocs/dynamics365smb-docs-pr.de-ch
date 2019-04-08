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
ms.date: 10/15/2018
ms.author: sgroespe
ms.openlocfilehash: 7db6bce91246e2b76240f6641790ff44294c3522
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "827195"
---
# <a name="swiss-value-added-tax"></a><span data-ttu-id="7f3bc-103">Mehrwertsteuer (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="7f3bc-103">Swiss Value Added Tax</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="7f3bc-104">enthält die folgenden Erweiterungen für die Schweizer Mehrwertsteuerberichterstellung:</span><span class="sxs-lookup"><span data-stu-id="7f3bc-104">includes the following enhancements to Swiss VAT reporting:</span></span>  

- <span data-ttu-id="7f3bc-105">Automatische Regulierung von MWST-Beträgen für Rechnungen entsprechend dem Skonto</span><span class="sxs-lookup"><span data-stu-id="7f3bc-105">Automatic adjustment of VAT amounts for invoices, according to payment discounts.</span></span>  
- <span data-ttu-id="7f3bc-106">Zusätzliche MWST-Wechselkurse für Rechnungen in Fremdwährungen</span><span class="sxs-lookup"><span data-stu-id="7f3bc-106">Additional VAT exchange rates for invoices in foreign currencies.</span></span>  

<span data-ttu-id="7f3bc-107">Weitere Informationen über die Schweizer Mehrwertsteuerberichterstellung und die Codierungsanforderungen finden Sie unter [Schweizer MWST-Informationen](https://www.estv.admin.ch/estv/en/home/estv-suissetax/sw-hersteller.html).</span><span class="sxs-lookup"><span data-stu-id="7f3bc-107">For more information about Swiss VAT reporting and coding requirements, see [Swiss VAT Information](https://www.estv.admin.ch/estv/en/home/estv-suissetax/sw-hersteller.html).</span></span> <span data-ttu-id="7f3bc-108">Die Information ist für Französisch, Deutsch und Italienisch verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-108">The information is available in French, German, and Italian.</span></span>  

## <a name="vat-amounts-and-vat-exchange-rates"></a><span data-ttu-id="7f3bc-109">MWST-Beträge und MWST-Wechselkurse</span><span class="sxs-lookup"><span data-stu-id="7f3bc-109">VAT Amounts and VAT Exchange Rates</span></span>  
<span data-ttu-id="7f3bc-110">Entsprechend den lokalen Mehrwertsteuer-Gesetzen kann der MWST Basisbetrag um den Skontobetrag reduziert werden, wenn Skonto gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-110">According to local VAT laws, the VAT base amount for an invoice can be reduced by the payment discount if a discount is granted.</span></span> <span data-ttu-id="7f3bc-111">Um automatische Mehrwertsteueranpassungen für ein Skonto einer Rechnung zuzulassen wir das Feld **Skonto berichtigen** standardmässig auf der Seite **Fibuposten Einrichtung** ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-111">To allow automatic VAT adjustment for a payment discount on an invoice, the **Adjust for Payment Discount** field is activated by default on the **General Ledger Setup** page.</span></span> <span data-ttu-id="7f3bc-112">Sie können diese Funktion in der MWST-Buchungsmatrix-Einrichtung " aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-112">You can also activate this function in the VAT posting setup.</span></span> <span data-ttu-id="7f3bc-113">Weitere Informationen finden Sie in der Tabelle "Fibuposten einrichten" und "MWST-Buchungsmatrix einrichten".</span><span class="sxs-lookup"><span data-stu-id="7f3bc-113">For more information, see the General Ledger Setup table and the VAT Posting Setup table.</span></span>  

### <a name="currency-exchange-rates-for-vat-reporting"></a><span data-ttu-id="7f3bc-114">Währungswechselkurse für die MWST-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="7f3bc-114">Currency Exchange Rates for VAT Reporting</span></span>  
<span data-ttu-id="7f3bc-115">Für Rechnungen in Fremdwährungen muss der offizielle Wechselkurs der Regierung für die MWST-Berechnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-115">For invoices in foreign currency, you must use the official exchange rate provided by the government for the VAT calculation itself.</span></span> <span data-ttu-id="7f3bc-116">Sie können zusätzliche MWST-Wechselkurse einrichten, die für andere Rechnungsbelange als die MWST-Berechnung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-116">You can also set up additional exchange rates for VAT, which you can use for aspects of the invoice other than the VAT calculation.</span></span> <span data-ttu-id="7f3bc-117">Der korrekte offizielle MWST-Wechselkurs kann für jede relevante Fremdwährung in der Wechselkurseinrichtung für Rechnungen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-117">You can provide the correct government VAT exchange rate for each relevant foreign currency in the exchange rate setup for invoices.</span></span> <span data-ttu-id="7f3bc-118">Weitere Informationen finden Sie in der Tabelle "Wechselkurse".</span><span class="sxs-lookup"><span data-stu-id="7f3bc-118">For more information, see the Currency Exchange Rate table.</span></span>  

<span data-ttu-id="7f3bc-119">Es ist auch möglich, alle aus Fremdwährungstransaktionen resultierenden MWST-Beträge in MWST-Posten zu regulieren.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-119">You can also adjust all VAT amounts in VAT entries that result from foreign currency transactions.</span></span> <span data-ttu-id="7f3bc-120">Wenn Sie die Funktion für die MWST-Wechselkursregulierung aktivieren, werden die MWST-Wechselkurse automatisch reguliert.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-120">When you activate the adjust VAT exchange rate function, VAT exchange rates are adjusted automatically.</span></span> <span data-ttu-id="7f3bc-121">Die durch Wechselkurse verursachten positiven Differenzen werden auf Kursgewinnkonten gebucht.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-121">The positive differences that result from exchange rates are posted to exchange rate gain accounts.</span></span> <span data-ttu-id="7f3bc-122">Die durch Wechselkurse verursachten negativen Differenzen werden auf Kursverlustkonten gebucht.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-122">The negative differences that result from exchange rates are posted to exchange rate loss accounts.</span></span> <span data-ttu-id="7f3bc-123">Weitere Informationen finden Sie unter Stapelverarbeitungsauftrag "Wechselkurse regulieren".</span><span class="sxs-lookup"><span data-stu-id="7f3bc-123">For more information, see the Adjust Exchange Rates batch job.</span></span>  

<span data-ttu-id="7f3bc-124">In die MWST-Posten werden weitere Angaben übertragen, z. B. der MWST-Satz und der ursprüngliche Währungsbetrag.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-124">Additional information, such as VAT rate and original currency amount, is transferred to the VAT entries.</span></span> <span data-ttu-id="7f3bc-125">Weitere Informationen finden Sie in der MWST-Postentabelle.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-125">For more information, see the VAT Entry table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7f3bc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f3bc-126">See Also</span></span>  
 <span data-ttu-id="7f3bc-127">[MWST-Sätze für die Schweiz](vat-rates-for-switzerland.md) </span><span class="sxs-lookup"><span data-stu-id="7f3bc-127">[VAT Rates for Switzerland](vat-rates-for-switzerland.md) </span></span>  
 <span data-ttu-id="7f3bc-128">[Erstellen und Drucken einer Schweizer MWST-Abrechnung](how-to-create-and-print-a-swiss-vat-statement.md) </span><span class="sxs-lookup"><span data-stu-id="7f3bc-128">[Create and Print a Swiss VAT Statement](how-to-create-and-print-a-swiss-vat-statement.md) </span></span>  
 [<span data-ttu-id="7f3bc-129">Lokale Funktion (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="7f3bc-129">Switzerland Local Functionality</span></span>](switzerland-local-functionality.md)   
