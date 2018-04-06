---
title: "Gewusst wie: Drucken von MWST-Abrechnungen (Schweiz) (ältere Version)"
description: "Die **Schweizer MWST-Abrechnung** ist der Standardberechnungsbericht für die Realisierung der MWST. Sie können diesen Bericht drucken und ihn für die quartalsweise Steuerberichterstellung verwenden."
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
ms.openlocfilehash: 7c6cf55b476b84e30315bdc10ed4c77b4b30f20c
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="print-swiss-vat-statements-older-version"></a><span data-ttu-id="8d1c0-104">Drucken von MWST-Abrechnungen (Schweiz) (ältere Version)</span><span class="sxs-lookup"><span data-stu-id="8d1c0-104">Print Swiss VAT Statements (older version)</span></span>

> [!NOTE]  
>  <span data-ttu-id="8d1c0-105">In diesem Thema wird für Rückwärtskompatibilität mit dem Bericht **Schweizer MWST-Abrechnung** behandelt.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-105">This topic is retained for backward compatibility with the **Swiss VAT Statement** report.</span></span> <span data-ttu-id="8d1c0-106">Informationen zur Verwendung der späteren Schweizer MWST-Abrechnung, siehe Schweizer MWST-Abrechnung.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-106">For information about using the newer Swiss VAT Statement, see Swiss VAT Statement.</span></span>  

<span data-ttu-id="8d1c0-107">Die **Schweizer MWST-Abrechnung** ist der Standardberechnungsbericht für die Realisierung der MWST</span><span class="sxs-lookup"><span data-stu-id="8d1c0-107">The **Swiss VAT Statement** is the standard calculation report for realizing VAT.</span></span> <span data-ttu-id="8d1c0-108">Sie können diesen Bericht drucken und ihn für die quartalsweise Steuerberichterstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-108">You can print this report, and use it for quarterly tax reporting.</span></span> <span data-ttu-id="8d1c0-109">Das **Schweizer MWST-Abrechnung** enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8d1c0-109">The **Swiss VAT Statement** includes the following:</span></span>  

- <span data-ttu-id="8d1c0-110">Ein MWST-Posten.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-110">A VAT entry.</span></span>  
- <span data-ttu-id="8d1c0-111">MWST-Regulierungsposten.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-111">VAT adjusting entries.</span></span>  
- <span data-ttu-id="8d1c0-112">Ein Abrechnungsbogen.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-112">An accounting sheet.</span></span>  

## <a name="to-print-the-swiss-vat-statement"></a><span data-ttu-id="8d1c0-113">So drucken Sie die MWST-Abrechnung (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="8d1c0-113">To print the Swiss VAT statement</span></span>  

1.  <span data-ttu-id="8d1c0-114">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und öffnen **MWST-Abrechnung Schweiz**. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-114">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Swiss VAT Statement**, and then choose the related link.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="8d1c0-115">Sie erhalten eine Meldung die angibt, dass **Schweizer MWST-Abrechnung** in der Landessprache geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-115">You will receive a message stating that the **Swiss VAT Statement** will open in the local language.</span></span>  

2.  <span data-ttu-id="8d1c0-116">Füllen Sie auf dem Inforegister **Optionen** die Felder wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-116">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="8d1c0-117">Feld</span><span class="sxs-lookup"><span data-stu-id="8d1c0-117">Field</span></span>|<span data-ttu-id="8d1c0-118">Description</span><span class="sxs-lookup"><span data-stu-id="8d1c0-118">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="8d1c0-119">**Geschlossen mit Journalnummer**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-119">**Closed with Journal no.**</span></span>|<span data-ttu-id="8d1c0-120">Wählen Sie die Finanzbuchhaltungserf.-Journale aus, die die Buchungsquelle der Mehrwertsteuerberichtigungsbuchungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-120">Select the general ledger journals that contain the posting source of the VAT adjusting entries.</span></span> <span data-ttu-id="8d1c0-121">In diesem Feld werden die Buchhaltungsperioden ausgewertet, die bereits ausgeglichen wurden.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-121">This field evaluates accounting periods that have already been settled.</span></span>|  
    |<span data-ttu-id="8d1c0-122">**Verfügbar bis (Datum)**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-122">**Open until date**</span></span>|<span data-ttu-id="8d1c0-123">Wählen Sie das Datum, um offene oder erledigte MWST-Posten zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-123">Select the last date for settling open or unsettled VAT entries.</span></span>|  
    |<span data-ttu-id="8d1c0-124">**Buchungen anzeigen**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-124">**Show Postings**</span></span>|<span data-ttu-id="8d1c0-125">Gibt an, ob alle MWST-Posten für jede Gruppe gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-125">Specifies if all of the VAT entries for each group will be printed.</span></span>|  
    |<span data-ttu-id="8d1c0-126">**Ausgleichsbuchungen anzeigen**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-126">**Show Chargeback**</span></span>|<span data-ttu-id="8d1c0-127">Gibt an, ob MWST-Posten und Fibuposten mit abgeschlossenen Zusammenfassungen oder erneut gebuchte Steuern gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-127">Specifies if VAT entries and general ledger entries with closed summaries or reposted tax will be printed.</span></span>|  
    |<span data-ttu-id="8d1c0-128">**Normalsatz (MWST %)**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-128">**Normal rate VAT %**</span></span>|<span data-ttu-id="8d1c0-129">Wählen Sie die aktuellen typischen Mehrwertsteuersätze aus, die verwendet werden, um die richtigen Sätze den Geschäfts- und Produktgruppen, die in den Mehrwertsteuereinstellungen definiert werden, zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-129">Select the current typical VAT rates used to assign the correct rates to the business and product groups defined in the VAT settings.</span></span>|  
    |<span data-ttu-id="8d1c0-130">**Reduzierter Satz (MWST %)**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-130">**Reduced rate VAT %**</span></span>|<span data-ttu-id="8d1c0-131">Wählen Sie die aktuellen reduzierten Steuersätze aus, die verwendet werden, um die richtigen Sätze den Geschäfts- und Produktgruppen, die in den Mehrwertsteuereinstellungen definiert werden, zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-131">Select the current reduced tax rates used to assign the correct rates to the business and product groups defined in the VAT settings.</span></span>|  
    |<span data-ttu-id="8d1c0-132">**Sondersatz MWST %**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-132">**Special rate VAT %**</span></span>|<span data-ttu-id="8d1c0-133">Wählen Sie die aktuellen besonderen Steuersätze aus, die verwendet werden, um die richtigen Sätze den Geschäfts- und Produktgruppen, die in den Mehrwertsteuereinstellungen definiert werden, zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-133">Select the current special tax rates used to assign the correct rates to the business and product groups defined in the VAT settings.</span></span>|  
    |<span data-ttu-id="8d1c0-134">**Vorsteuerabzug Investition/Betriebsaufwand (Fibukonto)**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-134">**Investment/Operating Purchase VAT G/L Account**</span></span>|<span data-ttu-id="8d1c0-135">Wählen Sie das Fibukonto für die MWST aus.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-135">Select the VAT general ledger account.</span></span>|  
    |<span data-ttu-id="8d1c0-136">**Eigenverbrauch Gesch. Gruppe**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-136">**Own Consumption Bus. Group**</span></span>|<span data-ttu-id="8d1c0-137">Wählen Sie in der Geschäfts- und Produktgruppe für den Eigenverbrauch aus.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-137">Select the business and product group for own consumptions.</span></span>|  
    |<span data-ttu-id="8d1c0-138">**Service Fremde Geschl Gruppe**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-138">**Service Foreign Bus. Group**</span></span>|<span data-ttu-id="8d1c0-139">Wählen Sie das Auslandsdienstgeschäft und die Produktgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-139">Select the foreign service business and product group.</span></span>|  
    |<span data-ttu-id="8d1c0-140">**Exporte Gesch. Gruppe**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-140">**Export Bus. Group**</span></span>|<span data-ttu-id="8d1c0-141">Wählen Sie in der Geschäfts- und Produktgruppe für den Export aus.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-141">Select the business and product group for exports.</span></span>|  

3.  <span data-ttu-id="8d1c0-142">Wählen Sie die Schaltfläche **Drucken** aus, um den MwSt-Bericht zu drucken, oder die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-142">Choose the **Print** button to print the VAT statement or choose the **Preview** button to view it on the screen.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8d1c0-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d1c0-143">See Also</span></span>  
 <span data-ttu-id="8d1c0-144">[Mehrwertsteuer (Schweiz)](swiss-value-added-tax.md) </span><span class="sxs-lookup"><span data-stu-id="8d1c0-144">[Swiss Value Added Tax](swiss-value-added-tax.md) </span></span>  
 [<span data-ttu-id="8d1c0-145">MWST-Sätze für die Schweiz</span><span class="sxs-lookup"><span data-stu-id="8d1c0-145">VAT Rates for Switzerland</span></span>](vat-rates-for-switzerland.md)

