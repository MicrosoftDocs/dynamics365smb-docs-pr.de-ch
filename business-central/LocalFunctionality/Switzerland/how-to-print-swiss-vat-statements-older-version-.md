---
title: 'Gewusst wie: Drucken von MWST-Abrechnungen (Schweiz) (ältere Version)'
description: Die Schweizer MWST-Abrechnung ist der Standardberechnungsbericht für die Realisierung der MWST Sie können diesen Bericht drucken und ihn für die quartalsweise Steuerberichterstellung verwenden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e88c096007e1bc26636f9a73caecdc936b726cd9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776554"
---
# <a name="print-swiss-vat-statements-older-version"></a><span data-ttu-id="7b1c4-104">Drucken von MWST-Abrechnungen (Schweiz) (ältere Version)</span><span class="sxs-lookup"><span data-stu-id="7b1c4-104">Print Swiss VAT Statements (older version)</span></span>

> [!NOTE]  
>  <span data-ttu-id="7b1c4-105">In diesem Thema wird für Rückwärtskompatibilität mit dem Bericht **Schweizer MWST-Abrechnung** behandelt.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-105">This topic is retained for backward compatibility with the **Swiss VAT Statement** report.</span></span> <span data-ttu-id="7b1c4-106">Informationen zur Verwendung der späteren Schweizer MWST-Abrechnung, siehe Schweizer MWST-Abrechnung.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-106">For information about using the newer Swiss VAT Statement, see Swiss VAT Statement.</span></span>  

<span data-ttu-id="7b1c4-107">Die **Schweizer MWST-Abrechnung** ist der Standardberechnungsbericht für die Realisierung der MWST</span><span class="sxs-lookup"><span data-stu-id="7b1c4-107">The **Swiss VAT Statement** is the standard calculation report for realizing VAT.</span></span> <span data-ttu-id="7b1c4-108">Sie können diesen Bericht drucken und ihn für die quartalsweise Steuerberichterstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-108">You can print this report, and use it for quarterly tax reporting.</span></span> <span data-ttu-id="7b1c4-109">Das **Schweizer MWST-Abrechnung** enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7b1c4-109">The **Swiss VAT Statement** includes the following:</span></span>  

- <span data-ttu-id="7b1c4-110">Ein MWST-Posten.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-110">A VAT entry.</span></span>  
- <span data-ttu-id="7b1c4-111">MWST-Regulierungsposten.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-111">VAT adjusting entries.</span></span>  
- <span data-ttu-id="7b1c4-112">Ein Abrechnungsbogen.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-112">An accounting sheet.</span></span>  

## <a name="to-print-the-swiss-vat-statement"></a><span data-ttu-id="7b1c4-113">So drucken Sie die MWST-Abrechnung (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="7b1c4-113">To print the Swiss VAT statement</span></span>  

1.  <span data-ttu-id="7b1c4-114">Wählen Sie die ![Glühbirne, die das Tell Me Feature](../../media/ui-search/search_small.png "Tell me-Funktion") Symbol öffnet, geben Sie **MWST-Abrechnung Schweiz** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-114">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Swiss VAT Statement**, and then choose the related link.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="7b1c4-115">Sie erhalten eine Meldung die angibt, dass **Schweizer MWST-Abrechnung** in der Landessprache geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-115">You will receive a message stating that the **Swiss VAT Statement** will open in the local language.</span></span>  

2.  <span data-ttu-id="7b1c4-116">Füllen Sie auf dem Inforegister **Optionen** die Felder wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-116">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="7b1c4-117">Feld</span><span class="sxs-lookup"><span data-stu-id="7b1c4-117">Field</span></span>|<span data-ttu-id="7b1c4-118">Description</span><span class="sxs-lookup"><span data-stu-id="7b1c4-118">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="7b1c4-119">**Geschlossen mit Journalnummer**</span><span class="sxs-lookup"><span data-stu-id="7b1c4-119">**Closed with Journal no.**</span></span>|<span data-ttu-id="7b1c4-120">Wählen Sie die Finanzbuchhaltungserf.-Journale aus, die die Buchungsquelle der Mehrwertsteuerberichtigungsbuchungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-120">Select the general ledger journals that contain the posting source of the VAT adjusting entries.</span></span> <span data-ttu-id="7b1c4-121">In diesem Feld werden die Buchhaltungsperioden ausgewertet, die bereits ausgeglichen wurden.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-121">This field evaluates accounting periods that have already been settled.</span></span>|  
    |<span data-ttu-id="7b1c4-122">**Verfügbar bis (Datum)**</span><span class="sxs-lookup"><span data-stu-id="7b1c4-122">**Open until date**</span></span>|<span data-ttu-id="7b1c4-123">Wählen Sie das Datum, um offene oder erledigte MWST-Posten zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-123">Select the last date for settling open or unsettled VAT entries.</span></span>|  
    |<span data-ttu-id="7b1c4-124">**Buchungen anzeigen**</span><span class="sxs-lookup"><span data-stu-id="7b1c4-124">**Show Postings**</span></span>|<span data-ttu-id="7b1c4-125">Gibt an, ob alle MWST-Posten für jede Gruppe gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-125">Specifies if all of the VAT entries for each group will be printed.</span></span>|  
    |<span data-ttu-id="7b1c4-126">**Ausgleichsbuchungen anzeigen**</span><span class="sxs-lookup"><span data-stu-id="7b1c4-126">**Show Chargeback**</span></span>|<span data-ttu-id="7b1c4-127">Gibt an, ob MWST-Posten und Fibuposten mit abgeschlossenen Zusammenfassungen oder erneut gebuchte Steuern gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-127">Specifies if VAT entries and general ledger entries with closed summaries or reposted tax will be printed.</span></span>|  
    |<span data-ttu-id="7b1c4-128">**Normalsatz (MWST %)**</span><span class="sxs-lookup"><span data-stu-id="7b1c4-128">**Normal rate VAT %**</span></span>|<span data-ttu-id="7b1c4-129">Wählen Sie die aktuellen typischen Mehrwertsteuersätze aus, die verwendet werden, um die richtigen Sätze den Geschäfts- und Produktgruppen, die in den Mehrwertsteuereinstellungen definiert werden, zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-129">Select the current typical VAT rates used to assign the correct rates to the business and product groups defined in the VAT settings.</span></span>|  
    |<span data-ttu-id="7b1c4-130">**Reduzierter Satz (MWST %)**</span><span class="sxs-lookup"><span data-stu-id="7b1c4-130">**Reduced rate VAT %**</span></span>|<span data-ttu-id="7b1c4-131">Wählen Sie die aktuellen reduzierten Steuersätze aus, die verwendet werden, um die richtigen Sätze den Geschäfts- und Produktgruppen, die in den Mehrwertsteuereinstellungen definiert werden, zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-131">Select the current reduced tax rates used to assign the correct rates to the business and product groups defined in the VAT settings.</span></span>|  
    |<span data-ttu-id="7b1c4-132">**Sondersatz MWST %**</span><span class="sxs-lookup"><span data-stu-id="7b1c4-132">**Special rate VAT %**</span></span>|<span data-ttu-id="7b1c4-133">Wählen Sie die aktuellen besonderen Steuersätze aus, die verwendet werden, um die richtigen Sätze den Geschäfts- und Produktgruppen, die in den Mehrwertsteuereinstellungen definiert werden, zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-133">Select the current special tax rates used to assign the correct rates to the business and product groups defined in the VAT settings.</span></span>|  
    |<span data-ttu-id="7b1c4-134">**Vorsteuerabzug Investition/Betriebsaufwand (Fibukonto)**</span><span class="sxs-lookup"><span data-stu-id="7b1c4-134">**Investment/Operating Purchase VAT G/L Account**</span></span>|<span data-ttu-id="7b1c4-135">Wählen Sie das Fibukonto für die MWST aus.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-135">Select the VAT general ledger account.</span></span>|  
    |<span data-ttu-id="7b1c4-136">**Eigenverbrauch Gesch. Gruppe**</span><span class="sxs-lookup"><span data-stu-id="7b1c4-136">**Own Consumption Bus. Group**</span></span>|<span data-ttu-id="7b1c4-137">Wählen Sie in der Geschäfts- und Produktgruppe für den Eigenverbrauch aus.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-137">Select the business and product group for own consumptions.</span></span>|  
    |<span data-ttu-id="7b1c4-138">**Service Fremde Geschl Gruppe**</span><span class="sxs-lookup"><span data-stu-id="7b1c4-138">**Service Foreign Bus. Group**</span></span>|<span data-ttu-id="7b1c4-139">Wählen Sie das Auslandsdienstgeschäft und die Produktgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-139">Select the foreign service business and product group.</span></span>|  
    |<span data-ttu-id="7b1c4-140">**Exporte Gesch. Gruppe**</span><span class="sxs-lookup"><span data-stu-id="7b1c4-140">**Export Bus. Group**</span></span>|<span data-ttu-id="7b1c4-141">Wählen Sie in der Geschäfts- und Produktgruppe für den Export aus.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-141">Select the business and product group for exports.</span></span>|  

3.  <span data-ttu-id="7b1c4-142">Wählen Sie die Schaltfläche **Drucken** aus, um den MwSt-Bericht zu drucken, oder die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7b1c4-142">Choose the **Print** button to print the VAT statement or choose the **Preview** button to view it on the screen.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7b1c4-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b1c4-143">See Also</span></span>  
 <span data-ttu-id="7b1c4-144">[Mehrwertsteuer (Schweiz)](swiss-value-added-tax.md) </span><span class="sxs-lookup"><span data-stu-id="7b1c4-144">[Swiss Value Added Tax](swiss-value-added-tax.md) </span></span>  
 [<span data-ttu-id="7b1c4-145">Mehrwertsteuersätze der Schweiz</span><span class="sxs-lookup"><span data-stu-id="7b1c4-145">VAT Rates for Switzerland</span></span>](vat-rates-for-switzerland.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]