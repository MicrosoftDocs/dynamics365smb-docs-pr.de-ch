---
title: Regulieren von Wechselkursen
description: "Wenn Sie steuerpflichtige Umsätze in Fremdwährung abrechnen, müssen die offiziellen Kurse der Eidg. Steuerverwaltung zur MWST-Kursumrechnung verwendet werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: a88b82e64349d6a614ba5190a9a51505f501a70f
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="adjust-exchange-rates"></a><span data-ttu-id="0b633-103">Wechselkurse regulieren</span><span class="sxs-lookup"><span data-stu-id="0b633-103">Adjust Exchange Rates</span></span>
<span data-ttu-id="0b633-104">Wenn Sie steuerpflichtige Umsätze in Fremdwährung abrechnen, müssen die offiziellen Kurse der Eidg. Steuerverwaltung zur MWST-Kursumrechnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b633-104">If you have taxable sales in a foreign currency, you must use the official rate for VAT currency conversion as set by the Federal Tax Administration.</span></span>  

<span data-ttu-id="0b633-105">Wenn diese Kurse nicht mit den Währungskursen in den Einkaufs- oder Verkaufsrechnungen übereinstimmen, müssen Sie die MWST-Sätze später mit einer Stapelverarbeitung regulieren.</span><span class="sxs-lookup"><span data-stu-id="0b633-105">If these rates do not match the currency rates used in the purchase or sales invoices, you will have to adjust the VAT rates with a batch job later.</span></span> <span data-ttu-id="0b633-106">Diese Regulierungen können nur mit einem autorisierten MWST-Satz durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0b633-106">These adjustments can only be run using an authorized VAT rate.</span></span>  

<span data-ttu-id="0b633-107">Sie können diese Stapelverarbeitung beliebig oft ausführen. Achten Sie aber darauf, sie immer vor der Erstellung einer MWST-Abrechnung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0b633-107">You can run this batch job as often as you like, however make sure that you always run it before creating a VAT statement.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0b633-108">Bei Verwendung einer Berichtswährung müssen Sie sicherstellen, dass das Feld **MWST-Kursregulierung** im Fenster **Finanzbuchhaltung Einrichtung** auf **Keine Regulierung** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="0b633-108">When using a report currency, make sure that the **VAT Exchange Rate Adjustment** field in the **General Ledger Setup** window is set to **No Adjustment**.</span></span>  

<span data-ttu-id="0b633-109">Weitere Informationen über MWST und Fremdwährungen finden Sie auf der [ESTV](http://go.microsoft.com/fwlink/?LinkId=285999)-Website.</span><span class="sxs-lookup"><span data-stu-id="0b633-109">For more information about VAT and foreign currencies, see the [ESTV](http://go.microsoft.com/fwlink/?LinkId=285999) website.</span></span>  

## <a name="to-adjust-an-exchange-rate"></a><span data-ttu-id="0b633-110">So regulieren Sie einen Wechselkurs</span><span class="sxs-lookup"><span data-stu-id="0b633-110">To adjust an exchange rate</span></span>  

1.  <span data-ttu-id="0b633-111">Wählen Sie ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") ein und wählen **Währungswechselkurs-Dienste** und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="0b633-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0b633-112">Wählen Sie die Aktion **Wechselkurse** aus.</span><span class="sxs-lookup"><span data-stu-id="0b633-112">Choose the **Exch. Rates** action.</span></span>  
3.  <span data-ttu-id="0b633-113">Geben Sie im Fenster **Währungswechselkurse** den offiziellen MWST-Satz pro Periode für die jeweilige Währung in die Felder **Anzahl MWST-Einheiten** und **MWST-Kurs** ein.</span><span class="sxs-lookup"><span data-stu-id="0b633-113">In the **Currency Exchange Rates** window, enter the official VAT rate per period for each currency in the **VAT Exch. Rate Amount** and the **Relational VAT Exch. Rate Amt** fields.</span></span>  
4.  <span data-ttu-id="0b633-114">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="0b633-114">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="0b633-115">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen"), öffnen Sie **Wechselkurse regulieren**, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="0b633-115">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Adjust Exchange Rates**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="0b633-116">Füllen Sie auf dem Inforegister **Optionen** die Felder wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="0b633-116">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>   

    |<span data-ttu-id="0b633-117">Feld</span><span class="sxs-lookup"><span data-stu-id="0b633-117">Field</span></span>|<span data-ttu-id="0b633-118">Description</span><span class="sxs-lookup"><span data-stu-id="0b633-118">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="0b633-119">**Startdatum**</span><span class="sxs-lookup"><span data-stu-id="0b633-119">**Starting Date**</span></span>|<span data-ttu-id="0b633-120">Geben Sie ein Datum ein, um den Anfang der Periode festzulegen, für die Posten reguliert werden.</span><span class="sxs-lookup"><span data-stu-id="0b633-120">Enter a date to specify the beginning of the period for which entries will be adjusted.</span></span>|  
    |<span data-ttu-id="0b633-121">**Enddatum**</span><span class="sxs-lookup"><span data-stu-id="0b633-121">**Ending Date**</span></span>|<span data-ttu-id="0b633-122">Geben Sie hier das letzte Datum ein, bis zu dem Posten reguliert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0b633-122">Enter the last date for which entries will be adjusted.</span></span> <span data-ttu-id="0b633-123">Dieses Datum entspricht normalerweise dem Buchungsdatum im Feld **Buchungsdatum**.</span><span class="sxs-lookup"><span data-stu-id="0b633-123">This date is typically the same as the posting date in the **Posting Date** field.</span></span>|  
    |<span data-ttu-id="0b633-124">**MWST-Kurs für Steuerverw. regulieren**</span><span class="sxs-lookup"><span data-stu-id="0b633-124">**Adjust VAT exch. rate**</span></span>|<span data-ttu-id="0b633-125">Geben Sie an, ob Sie den MWST-Wechselkurs regulieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0b633-125">Specify if you want to adjust the VAT exchange rate.</span></span>|  

7.  <span data-ttu-id="0b633-126">Wählen Sie die Schaltfläche **Drucken**, um den Batchauftrag zu starten.</span><span class="sxs-lookup"><span data-stu-id="0b633-126">Choose the **Print** button to start the batch job.</span></span> <span data-ttu-id="0b633-127">Diese Stapelverarbeitung legt fest, ob MWST-Posten reguliert werden müssen. Ausserdem bereitet sie einen Regulierungsposten für jeden dieser Posten für die Fibukonten "Unrealisierte/realisierte Kursregulierung" vor.</span><span class="sxs-lookup"><span data-stu-id="0b633-127">This batch job controls whether VAT entries have to be adjusted and prepares an adjusting entry for each of these entries for the Unrealized/Realized Exchange Rate Adjustment accounts.</span></span> <span data-ttu-id="0b633-128">Die vorhandenen MWST-Posten werden ebenfalls korrigiert.</span><span class="sxs-lookup"><span data-stu-id="0b633-128">The existing VAT entries are also corrected.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b633-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b633-129">See Also</span></span>  
 <span data-ttu-id="0b633-130">[Mehrwertsteuer (Schweiz)](swiss-value-added-tax.md) </span><span class="sxs-lookup"><span data-stu-id="0b633-130">[Swiss Value Added Tax](swiss-value-added-tax.md) </span></span>  
 <span data-ttu-id="0b633-131">[MWST-Sätze für die Schweiz](vat-rates-for-switzerland.md) </span><span class="sxs-lookup"><span data-stu-id="0b633-131">[VAT Rates for Switzerland](vat-rates-for-switzerland.md) </span></span>  
[<span data-ttu-id="0b633-132">Währungswechselkurse aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0b633-132">Update Currency Exchange Rates</span></span>](../../finance-how-update-currencies.md)

