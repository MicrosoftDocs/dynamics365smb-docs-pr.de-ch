---
title: Buchungsdatum auf Wertposten
description: Erfahren Sie wie die Stapelverarbeitung Lagerreg gekennzeichnet wird und ein Buchungsdatum auf Wertposten zugewiesen wird, der die Stapelverarbeitung erstellt.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 918a450ea40676447f872ba95eb489c7cc210211
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215117"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="240db-103">Designdetails: Buchungsdatum auf Ausgleichs-Wertposten</span><span class="sxs-lookup"><span data-stu-id="240db-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="240db-104">Dieser Artikel setzt Anleitung für Benutzer der Lager-Kostenberechnungsfunktionalität fest in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="240db-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="240db-105">Der spezifische Artikel informiert, wie die Stapelverarbeitung **Lagerreg. fakt. Einst.-Preise** kennzeichnet und ein Buchungsdatum auf Wertposten zuweist, die die Stapelverarbeitung erstellt.</span><span class="sxs-lookup"><span data-stu-id="240db-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="240db-106">Zuerst wird der Begriff des Prozesses wiederholt, wie die Stapelverarbeitung das Buchungsdatum zuweist und Wertposten erstellt.</span><span class="sxs-lookup"><span data-stu-id="240db-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="240db-107">Danach gibt es einige freigegebene Szenarien, auf die wir Support-Team gelegentlich stossen und es gibt eine Zusammenfassung der Begriffe, die verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="240db-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="240db-108">Das Konzept</span><span class="sxs-lookup"><span data-stu-id="240db-108">The Concept</span></span>  
<span data-ttu-id="240db-109">Die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** weist ein Buchungsdatum dem Wertposten zu, den sie im Begriffe ist, in den nachfolgenden Schritten zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="240db-109">The **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="240db-110">Das Buchungsdatum des Postens hat das gleiche Datum, wie der angepasste Posten.</span><span class="sxs-lookup"><span data-stu-id="240db-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="240db-111">Das Buchungsdatum wird mit den Lagerbuchungsperioden und/oder Fibuposteneinrichtung überprüft.</span><span class="sxs-lookup"><span data-stu-id="240db-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="240db-112">Zuweisung des Buchungsdatums; wenn das ursprüngliche Buchungsdatum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums liegt, wird die Stapelverarbeitung ein zulässiges Buchungsdatum aus entweder Fibuposteneinrichtung oder Lagerbuchungsperiode zuweisen.</span><span class="sxs-lookup"><span data-stu-id="240db-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="240db-113">Wenn die Lagerbuchungsperioden und die zugelassenen Buchungszeiträume in der Fibuposteneinrichtung festgelegt wurden, wird das Datum der beiden dem Ausgleichs-Wertposten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="240db-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="240db-114">Lassen Sie uns dieses Verfahren in der Praxis überprüfen.</span><span class="sxs-lookup"><span data-stu-id="240db-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="240db-115">Angenommen, wir haben einen Lagerposten zum Verkauf.</span><span class="sxs-lookup"><span data-stu-id="240db-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="240db-116">Der Artikel wurde am 5. September 2013 geliefert und er wurde am darauffolgenden Tag fakturiert.</span><span class="sxs-lookup"><span data-stu-id="240db-116">The item was shipped on September 5, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="240db-117">![Zustand der Lagerposten im Szenario](media/helene/TechArticleAdjustcost1.png "Zustand der Lagerposten im Szenario")</span><span class="sxs-lookup"><span data-stu-id="240db-117">![State of item ledger entries in the scenario](media/helene/TechArticleAdjustcost1.png "State of item ledger entries in the scenario")</span></span>  

<span data-ttu-id="240db-118">Unten zeigt der erste Wertposten (379) die Lieferung an und enthält dasselbe Buchungsdatum wie der Lagerposten des übergeordneten Artikels.</span><span class="sxs-lookup"><span data-stu-id="240db-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="240db-119">Der zweite Wertposten (381) zeigt die Rechnung an.</span><span class="sxs-lookup"><span data-stu-id="240db-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="240db-120">Der dritte Wertposten (391) ist eine Anpassung des Wertpostens Rechnungsstellung (381)</span><span class="sxs-lookup"><span data-stu-id="240db-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="240db-121">![Zustand der Werteinträge im Szenario](media/helene/TechArticleAdjustcost2.png "Status der Werteinträge im Szenario")</span><span class="sxs-lookup"><span data-stu-id="240db-121">![State of value entries in the scenario](media/helene/TechArticleAdjustcost2.png "State of value entries in the scenario")</span></span>  

 <span data-ttu-id="240db-122">Schritt 1: Der zu erstellende Wertposten wird dem selben Buchungsdatum zugeordnet, wie der angepasste Eintrag, wie in oben durch Wertposten 391 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="240db-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="240db-123">Schritt 2: Prüfung des zugewiesenen Buchungsdatums.</span><span class="sxs-lookup"><span data-stu-id="240db-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="240db-124">Die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** bestimmt, ob das ursprüngliche Buchungsdatum des Ausgleichs-Wertpostens innerhalb des Bereichs des zugelassenen Buchungszeitraums ist, der auf Lagerbuchungsperioden und/oder Fibuposteneinrichtung basiert.</span><span class="sxs-lookup"><span data-stu-id="240db-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="240db-125">Wir überprüfen den oben erwähnten Verkauf, indem wir die zugelassenen Buchungszeiträume hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="240db-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="240db-126">Lagerbuchungsperioden:</span><span class="sxs-lookup"><span data-stu-id="240db-126">Inventory Periods:</span></span>  

<span data-ttu-id="240db-127">![Bestandsperioden im Szenario](media/helene/TechArticleAdjustcost3.png "Inventarisierungszeiträume im Szenario")</span><span class="sxs-lookup"><span data-stu-id="240db-127">![Inventory periods in the scenario](media/helene/TechArticleAdjustcost3.png "Inventory periods in the scenario")</span></span>

 <span data-ttu-id="240db-128">Erster zugelassener Buchungszeitraum ist der erste Tag der ersten offenen Periode.</span><span class="sxs-lookup"><span data-stu-id="240db-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="240db-129">1. September 2013.</span><span class="sxs-lookup"><span data-stu-id="240db-129">September 1, 2013.</span></span>  

 <span data-ttu-id="240db-130">Fibuposteneinrichtung:</span><span class="sxs-lookup"><span data-stu-id="240db-130">General Ledger Setup:</span></span>  

<span data-ttu-id="240db-131">![Finanzbuchhaltung einrichten im Szenario](media/helene/TechArticleAdjustcost4.png "Sachkonteneinrichtung im Szenario")</span><span class="sxs-lookup"><span data-stu-id="240db-131">![G/L Setup in the scenario](media/helene/TechArticleAdjustcost4.png "G/L Setup in the scenario")</span></span>

 <span data-ttu-id="240db-132">Erster zugelassener Buchungszeitraum ist das Datum, das im Feld angezeigt wird, ab 10. September 2013.</span><span class="sxs-lookup"><span data-stu-id="240db-132">First allowed posting date is the date stated in field Allow Posting From: September 10, 2013.</span></span>  

 <span data-ttu-id="240db-133">Wenn die Lagerbuchungsperioden und die zugelassenen Buchungszeiträume in der Fibuposteneinrichtung festgelegt wurden, wird das Datum der beiden dem zugelassenen Ausgleichs-Wertposten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="240db-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="240db-134">Schritt 3: Zuweisung eines zugelassenen Buchungszeitraums;</span><span class="sxs-lookup"><span data-stu-id="240db-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="240db-135">Das zugewiesene Buchungsdatum war 6. September, wie in Schritt 1 veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="240db-135">The initial assigned Posting Date was September 6 as illustrated in step 1.</span></span> <span data-ttu-id="240db-136">Im zweiten Schritt erkennt die Stapelverarbeitung „Lagerreg. fakt. Einst.-Preise“ jedoch, dass das früheste zulässige Buchungsdatum der 10. September ist, und ordnet somit den 10. September dem unten stehenden Ausgleichs-Wertposten zu.</span><span class="sxs-lookup"><span data-stu-id="240db-136">However, in the second step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10 and thereby assigns September 10 to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="240db-137">![Zustand der Werteinträge im Szenario 2](media/helene/TechArticleAdjustcost5.png "Zustand der Werteinträge im Szenario 2")</span><span class="sxs-lookup"><span data-stu-id="240db-137">![State of value entries in the scenario 2](media/helene/TechArticleAdjustcost5.png "State of value entries in the scenario 2")</span></span>

 <span data-ttu-id="240db-138">Es haben jetzt das Vorgehen für das Zuweisen von Buchungsdaten für Werteinträge wiederholt, durch die Stapelverarbeitung Lagerreg. fakt. Einst. Preise.</span><span class="sxs-lookup"><span data-stu-id="240db-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="240db-139">Lassen Sie uns fortfahren, um verschiedene Szenarien zu überprüfen, auf die wir im Support-Team gelegentlich stossen, und zwar in Bezug auf ein Buchungsdatum in der Stapelverarbeitung Lagerreg und dem Zuordnen der zugehörigen Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="240db-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="240db-140">Szenarien</span><span class="sxs-lookup"><span data-stu-id="240db-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="240db-141">Szenario I: "Buchungsdatum liegt nicht innerhalb des zugelassenen Buchungszeitraums..."</span><span class="sxs-lookup"><span data-stu-id="240db-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="240db-142">Dies ist ein Szenario, in dem ein Benutzer eine Fehlermeldung erhält, wenn die Lagerreg. fakt. Einst. Preise Stapelverarbeitung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="240db-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="240db-143">Im vorherigen Abschnitt wird das Vorgehen für das Zuweisen des Buchungdatums beschrieben, die  Absicht der Stapelverarbeitung Lagerreg. fakt. Einst. Preise ist es, einen Wertposten mit Buchungsdatum am 10. September zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="240db-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="240db-144">![Fehlermeldung zum Buchungsdatum](media/helene/TechArticleAdjustcost6.png "Fehlermeldung zum Buchungsdatum")</span><span class="sxs-lookup"><span data-stu-id="240db-144">![Error message about posting date](media/helene/TechArticleAdjustcost6.png "Error message about posting date")</span></span>

 <span data-ttu-id="240db-145">Wir nehmen die Benutzer Einrichtung nochmals auf:</span><span class="sxs-lookup"><span data-stu-id="240db-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="240db-146">![Einstellung der zulässigen Buchungsdaten des Benutzers](media/helene/TechArticleAdjustcost7.png "Einrichtung der erlaubten Buchungsdaten der Benutzer")</span><span class="sxs-lookup"><span data-stu-id="240db-146">![User's allowed posting dates setup](media/helene/TechArticleAdjustcost7.png "User's allowed posting dates setup")</span></span>

 <span data-ttu-id="240db-147">Der Anwender hat in diesem Fall einen Bereich des zugelassenen Buchungszeitraums vom 11. September bis zum 30. September und es wird dadurch nicht erlaubt, den Ausgleichs-Wertposten mit dem Buchungsdatum am 10. September zu buchen.</span><span class="sxs-lookup"><span data-stu-id="240db-147">The user in this case has an allowed posting date range from September 11 to September 30 and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="240db-148">![Überblick über die Einrichtung des beteiligten Buchungsdatums](media/helene/TechArticleAdjustcost8.png "Übersicht über die Einstellung des beteiligten Buchungsdatums")</span><span class="sxs-lookup"><span data-stu-id="240db-148">![Overview of involved posting date setup](media/helene/TechArticleAdjustcost8.png "Overview of involved posting date setup")</span></span>

 <span data-ttu-id="240db-149">Knowledge Base-Artikel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) erläutert weitere Szenarien, die mit erwähnter Fehlermeldung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="240db-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses more scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="240db-150">Szenario II: Buchungsdatum auf Wertposten mit Buchungsdatum des Postens, der dem Ausgleich wie Neubewertung oder Artikel Zu-/Abschlag zugeordnet wird</span><span class="sxs-lookup"><span data-stu-id="240db-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="240db-151">Neubewertungsszenario:</span><span class="sxs-lookup"><span data-stu-id="240db-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="240db-152">Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="240db-152">Prerequisites:</span></span>  

 <span data-ttu-id="240db-153">Lagereinrichtung:</span><span class="sxs-lookup"><span data-stu-id="240db-153">Inventory setup:</span></span>  

-   <span data-ttu-id="240db-154">Automatische Lagerbuchung = Ja</span><span class="sxs-lookup"><span data-stu-id="240db-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="240db-155">Automatische Lagerregulierung = Immer</span><span class="sxs-lookup"><span data-stu-id="240db-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="240db-156">Einst.-Pr.(durchschn.)Ber.-Art = Artikel</span><span class="sxs-lookup"><span data-stu-id="240db-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="240db-157">Durchschnittskostenperiode= Tag</span><span class="sxs-lookup"><span data-stu-id="240db-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="240db-158">Fibuposteneinrichtung:</span><span class="sxs-lookup"><span data-stu-id="240db-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="240db-159">Zulassen Buchung von = am 1. Januar 2014</span><span class="sxs-lookup"><span data-stu-id="240db-159">Allow Posting From = January 1, 2014</span></span>  

-   <span data-ttu-id="240db-160">Anlagenbuchungen zugel. bis= leer</span><span class="sxs-lookup"><span data-stu-id="240db-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="240db-161">Benutzereinrichtung:</span><span class="sxs-lookup"><span data-stu-id="240db-161">User Setup:</span></span>  

-   <span data-ttu-id="240db-162">Zulassen Buchung von = 1. Dezember 2013.</span><span class="sxs-lookup"><span data-stu-id="240db-162">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="240db-163">Anlagenbuchungen zugel. bis= leer</span><span class="sxs-lookup"><span data-stu-id="240db-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="240db-164">So führen Sie ein Testszenario aus</span><span class="sxs-lookup"><span data-stu-id="240db-164">To test the scenario</span></span>  

1.  <span data-ttu-id="240db-165">Artikel TEST erstellen:</span><span class="sxs-lookup"><span data-stu-id="240db-165">Create item TEST:</span></span>  

     <span data-ttu-id="240db-166">Basismasseinheit = PCS</span><span class="sxs-lookup"><span data-stu-id="240db-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="240db-167">Kostenberechnungsmethode = Durchschnitt</span><span class="sxs-lookup"><span data-stu-id="240db-167">Costing Method = Average</span></span>  

     <span data-ttu-id="240db-168">Wählen Sie Buchungsgruppen optional aus.</span><span class="sxs-lookup"><span data-stu-id="240db-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="240db-169">Erf.-Journal öffnen und eine Zeile wie folgt erstellen und buchen:</span><span class="sxs-lookup"><span data-stu-id="240db-169">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="240db-170">Buchungsdatum = 15. Dezember 2013</span><span class="sxs-lookup"><span data-stu-id="240db-170">Posting Date = December 15, 2013</span></span>  

     <span data-ttu-id="240db-171">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="240db-171">Item = TEST</span></span>  

     <span data-ttu-id="240db-172">Eink.-Posten ausgleichen = Einkauf</span><span class="sxs-lookup"><span data-stu-id="240db-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="240db-173">Menge = 100</span><span class="sxs-lookup"><span data-stu-id="240db-173">Quantity = 100</span></span>  

     <span data-ttu-id="240db-174">Stückpreis = 10</span><span class="sxs-lookup"><span data-stu-id="240db-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="240db-175">Erf.-Journal öffnen und eine Zeile wie folgt erstellen und buchen:</span><span class="sxs-lookup"><span data-stu-id="240db-175">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="240db-176">Datum = 20. Dezember 2013</span><span class="sxs-lookup"><span data-stu-id="240db-176">Date = December 20, 2013</span></span>  

     <span data-ttu-id="240db-177">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="240db-177">Item = TEST</span></span>  

     <span data-ttu-id="240db-178">Eingangsart = Negative Anpassung</span><span class="sxs-lookup"><span data-stu-id="240db-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="240db-179">Menge = 2</span><span class="sxs-lookup"><span data-stu-id="240db-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="240db-180">Erf.-Journal öffnen und eine Zeile wie folgt erstellen und buchen:</span><span class="sxs-lookup"><span data-stu-id="240db-180">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="240db-181">Datum = 15. Januar 2014</span><span class="sxs-lookup"><span data-stu-id="240db-181">Date = January 15, 2014</span></span>  

     <span data-ttu-id="240db-182">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="240db-182">Item = TEST</span></span>  

     <span data-ttu-id="240db-183">Eingangsart = Negative Anpassung</span><span class="sxs-lookup"><span data-stu-id="240db-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="240db-184">Menge = 3</span><span class="sxs-lookup"><span data-stu-id="240db-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="240db-185">Erf.-Journal Neubewertung öffnen und eine Zeile wie folgt erstellen und buchen:</span><span class="sxs-lookup"><span data-stu-id="240db-185">Open Revaluation Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="240db-186">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="240db-186">Item = TEST</span></span>  

     <span data-ttu-id="240db-187">Auf Eintrag anwenden = Einkaufsposten auswählen, der unter Schritt 2 gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="240db-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="240db-188">Das Buchungsdatum der Neubewertung ist derselbe, wie der Posten, der angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="240db-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="240db-189">Einstandspreis neu bewertet = 40</span><span class="sxs-lookup"><span data-stu-id="240db-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="240db-190">Die folgenden Artikel- und Wertposten wurden gebucht:</span><span class="sxs-lookup"><span data-stu-id="240db-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="240db-191">![Überblick über resultierende Artikelposten und Werteinträge 1](media/helene/TechArticleAdjustcost9.png "Übersicht der resultierenden Artikelposten- und Wertbuchungen 1")</span><span class="sxs-lookup"><span data-stu-id="240db-191">![Overview of resulting item ledger and value entries 1](media/helene/TechArticleAdjustcost9.png "Overview of resulting item ledger and value entries 1")</span></span>

 <span data-ttu-id="240db-192">![Überblick über resultierende Artikelposten und Werteinträge 2](media/helene/TechArticleAdjustcost10.png "Übersicht der resultierenden Artikelposten- und Wertbuchungen 2")</span><span class="sxs-lookup"><span data-stu-id="240db-192">![Overview of resulting item ledger and value entries 2](media/helene/TechArticleAdjustcost10.png "Overview of resulting item ledger and value entries 2")</span></span>

 <span data-ttu-id="240db-193">Die Stapelverarbeitung Lagerreg hat eine Änderung der Kosten realisiert und die negative Anpassung vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="240db-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="240db-194">**Überprüfung Buchungsdatum des erstellten Ausgleichs-Wertposten:** Der früheste zugelassene Buchungszeitraum, den die Stapelverarbeitung Lagerreg verknüpft, ist am 1. Januar 2014, wie in der Finanzbuchhaltungs-Einrichtung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="240db-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="240db-195">**Negative Anpassung in Schritt 3:** zugewiesenes Buchungsdatum ist am 1. Januar, wie von der Finanzbuchhaltung eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="240db-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1, provided by General Ledger Setup.</span></span> <span data-ttu-id="240db-196">Das Buchungsdatum des Wertpostens im Bereich für Ausgleich ist am 20. Dezember 2013.</span><span class="sxs-lookup"><span data-stu-id="240db-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="240db-197">Entsprechend der Finanzbuchhaltungseinrichtung ist das Datum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums.</span><span class="sxs-lookup"><span data-stu-id="240db-197">According to General Ledger Setup, the date is not within allowed posting date range.</span></span> <span data-ttu-id="240db-198">Daher werden die Buchungsdaten, die im Feld Buchungen zulassen in der Fibuposteneinrichtung festgelegt sind, den Ausgleichs-Wertposten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="240db-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="240db-199">**Abgang in Schritt 4:** weist Buchungsdatum 15. Januar auf.</span><span class="sxs-lookup"><span data-stu-id="240db-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15.</span></span> <span data-ttu-id="240db-200">Der Wertposten im Bereich des Ausgleichs hat Buchungsdatum am 15. Januar, das innerhalb des Bereichs des zugelassenen Buchungszeitraums entsprechend der Finanzbuchhaltungseinrichtung ist.</span><span class="sxs-lookup"><span data-stu-id="240db-200">The Value Entry in scope of adjustment has Posting Date January 15, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="240db-201">Der Ausgleich, der für den Abgang in Schritt 3 geändert wird, verursacht Diskussionen.</span><span class="sxs-lookup"><span data-stu-id="240db-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="240db-202">Das bevorzugte Buchungsdatum für den Ausgleichs-Wertposten wäre am 20. Dezember oder mindestens im Dezember während die Neubewertung eine Änderung im Lagerverbrauch verursacht, der im Dezember gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="240db-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20 or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="240db-203">Um den Ausgleich im Dezember im Feld Abgang in Schritt 3 zu erzielen, gestattet die Fibuposteneinrichtung die Buchung aus dem Feld und es muss ein Datum im Dezember angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="240db-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="240db-204">**Schlussfolgerung:**</span><span class="sxs-lookup"><span data-stu-id="240db-204">**Conclusion:**</span></span>  

 <span data-ttu-id="240db-205">Mit den Erfahrungen aus diesem Szenario sollten Sie bei der Überlegung, welche Einrichtung des zulässigen Buchungsdatumsbereichs für ein Unternehmen am besten geeignet ist, die folgenden Informationen berücksichtigen: Solange Sie zulassen, dass Bestandswertänderungen in einer Periode gebucht werden, in diesem Fall im Dezember, sollte die Einrichtung, die das Unternehmen für zulässige Buchungsdatumsbereiche verwendet, mit dieser Entscheidung in Einklang stehen.</span><span class="sxs-lookup"><span data-stu-id="240db-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, you might want to consider the following information: As long as you allow changes in inventory value to be posted in a period, December in this case, the setup that the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="240db-206">Buchung von zulassen in der Finanzbuchhaltungs-Einrichtung, in diesem Fall der 1. Dezember, würde die Neubewertung ermöglichen, die im Dezember erfolgte und an betroffene ausgehenden Posten in derselben Periode weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="240db-206">The Allow Posting From in the General Ledger Setup, stating December 1, would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="240db-207">Die Benutzergruppen, die nicht erlaubt sind, um im Dezember gebucht zu werden, sondern im Januar, sind wahrscheinlich durch die Fibuposteneinrichtung in diesem Szenario beschränkt und sollten stattdessen über die Benutzereinrichtung adressiert werden.</span><span class="sxs-lookup"><span data-stu-id="240db-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="240db-208">Artikel-Zu-/Abschlagszuweisung</span><span class="sxs-lookup"><span data-stu-id="240db-208">Item charge scenario:</span></span>  
 <span data-ttu-id="240db-209">Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="240db-209">Prerequisites:</span></span>  

 <span data-ttu-id="240db-210">Lagereinrichtung:</span><span class="sxs-lookup"><span data-stu-id="240db-210">Inventory setup:</span></span>  

-   <span data-ttu-id="240db-211">Automatische Lagerbuchung = Ja</span><span class="sxs-lookup"><span data-stu-id="240db-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="240db-212">Automatische Lagerregulierung = Immer</span><span class="sxs-lookup"><span data-stu-id="240db-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="240db-213">Einst.-Pr.(durchschn.)Ber.-Art = Artikel</span><span class="sxs-lookup"><span data-stu-id="240db-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="240db-214">Durchschnittskostenperiode= Tag</span><span class="sxs-lookup"><span data-stu-id="240db-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="240db-215">Fibuposteneinrichtung:</span><span class="sxs-lookup"><span data-stu-id="240db-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="240db-216">Zulassen Buchung von = 1. Dezember 2013.</span><span class="sxs-lookup"><span data-stu-id="240db-216">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="240db-217">Anlagenbuchungen zugel. bis= leer</span><span class="sxs-lookup"><span data-stu-id="240db-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="240db-218">Benutzereinrichtung:</span><span class="sxs-lookup"><span data-stu-id="240db-218">User Setup:</span></span>  

-   <span data-ttu-id="240db-219">Zulassen Buchung von = 1. Dezember 2013.</span><span class="sxs-lookup"><span data-stu-id="240db-219">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="240db-220">Anlagenbuchungen zugel. bis= leer</span><span class="sxs-lookup"><span data-stu-id="240db-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="240db-221">So führen Sie ein Testszenario aus</span><span class="sxs-lookup"><span data-stu-id="240db-221">To test the scenario</span></span>  

1.  <span data-ttu-id="240db-222">Artikel Zu-/Abschläge erstellen:</span><span class="sxs-lookup"><span data-stu-id="240db-222">Create item charge:</span></span>  

     <span data-ttu-id="240db-223">Basismasseinheit = PCS</span><span class="sxs-lookup"><span data-stu-id="240db-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="240db-224">Kostenberechnungsmethode = Durchschnitt</span><span class="sxs-lookup"><span data-stu-id="240db-224">Costing Method = Average</span></span>  

     <span data-ttu-id="240db-225">Wählen Sie Buchungsgruppen optional aus.</span><span class="sxs-lookup"><span data-stu-id="240db-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="240db-226">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="240db-226">Create new purchase order</span></span>  

     <span data-ttu-id="240db-227">Kreditorennr.: 10000</span><span class="sxs-lookup"><span data-stu-id="240db-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="240db-228">Buchungsdatum = 15. Dezember 2013</span><span class="sxs-lookup"><span data-stu-id="240db-228">Posting Date = December 15, 2013</span></span>  

     <span data-ttu-id="240db-229">Kred.-Rechnungsnr.: 1234</span><span class="sxs-lookup"><span data-stu-id="240db-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="240db-230">Lagerdurchlaufzeit der Einkaufsbestellung:</span><span class="sxs-lookup"><span data-stu-id="240db-230">On the purchase order line:</span></span>  

     <span data-ttu-id="240db-231">Artikel = ABSCHLAG</span><span class="sxs-lookup"><span data-stu-id="240db-231">Item = CHARGE</span></span>  

     <span data-ttu-id="240db-232">Menge = 1</span><span class="sxs-lookup"><span data-stu-id="240db-232">Quantity = 1</span></span>  

     <span data-ttu-id="240db-233">Direkte Einheitskosten = 100</span><span class="sxs-lookup"><span data-stu-id="240db-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="240db-234">Lieferung und Rechnung buchen.</span><span class="sxs-lookup"><span data-stu-id="240db-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="240db-235">Einen neuen Verkaufsauftrag erstellen:</span><span class="sxs-lookup"><span data-stu-id="240db-235">Create new sales order:</span></span>  

     <span data-ttu-id="240db-236">Auftraggeber Nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="240db-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="240db-237">Buchungsdatum = 16. Dezember 2013</span><span class="sxs-lookup"><span data-stu-id="240db-237">Posting Date = December 16, 2013</span></span>  

     <span data-ttu-id="240db-238">Lagerdurchlaufzeit der Einkaufsbestellung:</span><span class="sxs-lookup"><span data-stu-id="240db-238">On the sales order line:</span></span>  

     <span data-ttu-id="240db-239">Artikel = ABSCHLAG</span><span class="sxs-lookup"><span data-stu-id="240db-239">Item = CHARGE</span></span>  

     <span data-ttu-id="240db-240">Menge = 1</span><span class="sxs-lookup"><span data-stu-id="240db-240">Quantity = 1</span></span>  

     <span data-ttu-id="240db-241">VK-Preis = 135</span><span class="sxs-lookup"><span data-stu-id="240db-241">Unit Price = 135</span></span>  

     <span data-ttu-id="240db-242">Liefernung und Rechnung buchen.</span><span class="sxs-lookup"><span data-stu-id="240db-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="240db-243">Fibuposteneinrichtung:</span><span class="sxs-lookup"><span data-stu-id="240db-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="240db-244">Zulassen Buchung von = am 1. Januar 2014</span><span class="sxs-lookup"><span data-stu-id="240db-244">Allow Posting From = January 1, 2014</span></span>  

     <span data-ttu-id="240db-245">Anlagenbuchungen zugel. bis = leer</span><span class="sxs-lookup"><span data-stu-id="240db-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="240db-246">Neue Bestellung erstellen:</span><span class="sxs-lookup"><span data-stu-id="240db-246">Create new purchase order:</span></span>  

     <span data-ttu-id="240db-247">Kreditorennr.: 10000</span><span class="sxs-lookup"><span data-stu-id="240db-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="240db-248">Buchungsdatum = 2. Januar 2014</span><span class="sxs-lookup"><span data-stu-id="240db-248">Posting Date = January 2, 2014</span></span>  

     <span data-ttu-id="240db-249">Kred.-Rechnungsnr.: 2345</span><span class="sxs-lookup"><span data-stu-id="240db-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="240db-250">Lagerdurchlaufzeit der Einkaufsbestellung:</span><span class="sxs-lookup"><span data-stu-id="240db-250">On the purchase order line:</span></span>  

     <span data-ttu-id="240db-251">Artikelkosten = FRACHT</span><span class="sxs-lookup"><span data-stu-id="240db-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="240db-252">Menge = 1</span><span class="sxs-lookup"><span data-stu-id="240db-252">Quantity = 1</span></span>  

     <span data-ttu-id="240db-253">Direkte Einheitskosten = 3</span><span class="sxs-lookup"><span data-stu-id="240db-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="240db-254">Weisen Sie Artikeln Artikel-Zu-/Abschläge in die Einkaufslieferung von Schritt 2 zu.</span><span class="sxs-lookup"><span data-stu-id="240db-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="240db-255">Empfang und Rechnung buchen.</span><span class="sxs-lookup"><span data-stu-id="240db-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="240db-256">![Überblick über resultierende Artikelposten und Werteinträge 3](media/helene/TechArticleAdjustcost11.png "Übersicht der resultierenden Artikelposten- und Wertbuchungen 3")</span><span class="sxs-lookup"><span data-stu-id="240db-256">![Overview of resulting item ledger and value entries 3](media/helene/TechArticleAdjustcost11.png "Overview of resulting item ledger and value entries 3")</span></span>

6.  <span data-ttu-id="240db-257">Am Arbeitsdatum vom 3. Januar geht eine Einkaufsrechnung ein, die eine zusätzliche Belastung für den in Schritt 2 getätigten Einkauf enthält.</span><span class="sxs-lookup"><span data-stu-id="240db-257">On work date January 3, a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="240db-258">Diese Rechnung hat ein Belegdatum vom 30. Dezember und wird daher mit Buchungsdatum am 30. Dezember 2013 gebucht.</span><span class="sxs-lookup"><span data-stu-id="240db-258">This invoice has document date December 30 and is therefore posted with Posting Date December 30, 2013.</span></span>  

     <span data-ttu-id="240db-259">Neue Bestellung erstellen:</span><span class="sxs-lookup"><span data-stu-id="240db-259">Create new purchase order:</span></span>  

     <span data-ttu-id="240db-260">Kreditorennr.: 10000</span><span class="sxs-lookup"><span data-stu-id="240db-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="240db-261">Buchungsdatum = 30. Dezember 2013</span><span class="sxs-lookup"><span data-stu-id="240db-261">Posting Date = December 30, 2013</span></span>  

     <span data-ttu-id="240db-262">Kred.-Rechnungsnr.: 3456</span><span class="sxs-lookup"><span data-stu-id="240db-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="240db-263">Lagerdurchlaufzeit der Einkaufsbestellung:</span><span class="sxs-lookup"><span data-stu-id="240db-263">On the purchase order line:</span></span>  

     <span data-ttu-id="240db-264">Artikelkosten = FRACHT</span><span class="sxs-lookup"><span data-stu-id="240db-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="240db-265">Menge = 1</span><span class="sxs-lookup"><span data-stu-id="240db-265">Quantity = 1</span></span>  

     <span data-ttu-id="240db-266">Direkte Einheitskosten = 2</span><span class="sxs-lookup"><span data-stu-id="240db-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="240db-267">Weisen Sie Artikeln Artikel-Zu-/Abschläge in die Einkaufslieferung von Schritt 2 zu.</span><span class="sxs-lookup"><span data-stu-id="240db-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="240db-268">Empfang und Rechnung buchen.</span><span class="sxs-lookup"><span data-stu-id="240db-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="240db-269">![Überblick über resultierende Artikelposten und Werteinträge 4](media/helene/TechArticleAdjustcost12.png "Übersicht der resultierenden Artikelposten- und Wertbuchungen 4")</span><span class="sxs-lookup"><span data-stu-id="240db-269">![Overview of resulting item ledger and value entries 4](media/helene/TechArticleAdjustcost12.png "Overview of resulting item ledger and value entries 4")</span></span>

 <span data-ttu-id="240db-270">Lager-Bewertungsbericht wird mit 31. Dezember 2013 gedruckt</span><span class="sxs-lookup"><span data-stu-id="240db-270">Inventory Valuation report is printed as of Date December 31 , 2013</span></span>  

<span data-ttu-id="240db-271">![Inhalt des Inventarbewertungsberichts](media/helene/TechArticleAdjustcost13.png "Inhalt des Berichts zur Inventarbewertung")</span><span class="sxs-lookup"><span data-stu-id="240db-271">![Content of the Inventory Valuation report](media/helene/TechArticleAdjustcost13.png "Content of the Inventory Valuation report")</span></span>

 <span data-ttu-id="240db-272">**Zusammenfassung des Szenarios:**</span><span class="sxs-lookup"><span data-stu-id="240db-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="240db-273">Das oben beschriebene Szenario endet mit einem Lager-Bewertungsbericht und zeigt Menge = 0 an, während der Wert = 2 beträgt.</span><span class="sxs-lookup"><span data-stu-id="240db-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="240db-274">Der Artikelzuschlag, der in Schritt 11 gebucht wird, ist ein Teil des Lagerzugangswerts vom Dezember, wohingegen der Lagerabgang derselben Periode nicht berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="240db-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="240db-275">Der Finanzbuchhaltungs-Einrichtung angeben, Buchungen ab dem 1. Januar zuzulassen, war für den ersten Artikel-Zu/Abschlag gut.</span><span class="sxs-lookup"><span data-stu-id="240db-275">Having the General Ledger Setup stating Allow Posting From January 1 was a good thing for the first Item charge.</span></span> <span data-ttu-id="240db-276">Die Kosten des Lagerzugangs und des Feldes Abgang wurden in derselben Periode erfasst.</span><span class="sxs-lookup"><span data-stu-id="240db-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="240db-277">Für den zweiten Artikel-Zu-/Abschlag verursachte die Fibuposteneinrichtung jedoch die Änderung im Lagerverbrauch, der in der Periode danach erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="240db-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="240db-278">**Schlussfolgerung:**</span><span class="sxs-lookup"><span data-stu-id="240db-278">**Conclusion:**</span></span>  

 <span data-ttu-id="240db-279">Es ist eine Herausforderung, den Bestandbewertungsbericht zu haben, um Menge = O anzuzeigen, während der Wert<> Wert 0 ist.</span><span class="sxs-lookup"><span data-stu-id="240db-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="240db-280">In diesem Fall ist es ebenfalls schwieriger, die optimalen Einstellungen zu finden, da Verkaufsrechnungen am gleichen Tag ankommen, jedoch verschiedene Perioden oder sogar Geschäftsjahre adressieren.</span><span class="sxs-lookup"><span data-stu-id="240db-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="240db-281">Das Eindringen in ein neues Geschäftsjahr erfordert normalerweise eine Absatzplanung ist Teil der Einblicke der Stapelverarbeitung Lagerreg Artikelposten und muss berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="240db-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="240db-282">In diesem Szenario könnte eine Option sein, die Fibuposten so einzurichten, dass das Feld Buchung zulassen von ein Datum im Dezember für einige Tage mehr definiert und die Buchung des Zuschlages des ersten Artikelpostens zurückgestellt wird, um die Kosten für die vorherige Periode/das vorherige Finanzjahr für die Periode zu ermöglichen, um alle Kosten dort zuzuweisen, wo sie zuerst erkannt wurden und dann die erlaubten Buchungsdaten in die neue Periode des \/ Steuerjahrs zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="240db-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="240db-283">Die Kosten des ersten Artikelpostens mit Buchungsdatum am 2. Januar dann gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="240db-283">The first item charge with posting date January 2 could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="240db-284">Führen Sie die Stapelverarbeitung Lagerreg. fakt. Einst. Preise aus.</span><span class="sxs-lookup"><span data-stu-id="240db-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="240db-285">Unten finden Sie eine Zusammenfassung des Begriffs, der Buchungsdaten den Ausgleichs-Wertposten durch die Stapelverarbeitung „Lagerreg. fakt. Einst. Preise“ zuweist.</span><span class="sxs-lookup"><span data-stu-id="240db-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job.</span></span>  

### <a name="about-the-request-form-posting-date"></a><span data-ttu-id="240db-286">Informationen zum Veröffentlichungsdatum des Anfrageformulars:</span><span class="sxs-lookup"><span data-stu-id="240db-286">About the request form posting date:</span></span>  
 <span data-ttu-id="240db-287">Es gibt kein Buchungsdatum mehr, das im Anforderungsformular der Stapelverarbeitung Lagerreg angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="240db-287">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="240db-288">Die Stapelverarbeitung wird durch alle erforderlichen Änderungen vorgenommen und erstellt Wertposten mit dem Buchungsdatum, das in das Anforderungsfenster eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="240db-288">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="240db-289">Zuweisung des Buchungsdatums; wenn das ursprüngliche Buchungsdatum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums liegt, wird die Stapelverarbeitung ein zulässiges Buchungsdatum aus entweder Fibuposteneinrichtung oder Lagerbuchungsperiode zuweisen.</span><span class="sxs-lookup"><span data-stu-id="240db-289">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="240db-290">vgl. Beschreibung des Konzepts oben.</span><span class="sxs-lookup"><span data-stu-id="240db-290">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="240db-291">Verlauf der Lagerkostenbuchung auf den Stapelverarbeitungseintrag</span><span class="sxs-lookup"><span data-stu-id="240db-291">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="240db-292">Die Stapelverarbeitung "Lagerregulierung buchen" ist mit der Stapelverarbeitung Lagerreg eng verwandt, warum die Historie dieser Stapelverarbeitung auch hier zusammengefasst und freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="240db-292">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  
 
<span data-ttu-id="240db-293">![Ist-Kosten versus erwartete Kosten](media/helene/TechArticleAdjustcost14.png "Tatsächliche Kosten versus erwartete Kosten")</span><span class="sxs-lookup"><span data-stu-id="240db-293">![Actual cost versus expected cost](media/helene/TechArticleAdjustcost14.png "Actual cost versus expected cost")</span></span>

### <a name="about-the-posting-date"></a><span data-ttu-id="240db-294">Informationen zum Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="240db-294">About the posting date</span></span>
 <span data-ttu-id="240db-295">Es gibt kein Buchungsdatum mehr, das im Anforderungsformular der Stapelverarbeitung Lagerreg angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="240db-295">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="240db-296">Die Fibuposten werden mit dem gleichen Buchungsdatum wie der verwandte Wertposten erstellt.</span><span class="sxs-lookup"><span data-stu-id="240db-296">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="240db-297">Um die Stapelverarbeitung auszuführen, muss der mittlere des zugelassenen Buchungszeitraums das Buchungsdatum des erstellten Fibupostens erlauben.</span><span class="sxs-lookup"><span data-stu-id="240db-297">In order to complete the batch job, the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="240db-298">Wenn nicht, muss sich der Standort des zugelassenen Buchungszeitraums durch das Ändern oder Entfernen des festgelegten Datumsfilters Buchungen zugel und aus den Feldern der Finanzbuchhaltungseinrichtung vorübergehend erneut geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="240db-298">If not, the allowed posting date range must be temporarily reopened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="240db-299">Um Abstimmungsprobleme zu vermeiden, ist es notwendig, dass das Buchungsdatum des Fibupostens zum Buchungsdatum des Wertpostens entspricht.</span><span class="sxs-lookup"><span data-stu-id="240db-299">To avoid reconciliation issues, it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="240db-300">Die Stapelverarbeitungsscans scannt Tabelle 5811 - Buchen von Wertposten mit Sachkonten, um die Wertposten im Bereich für die Buchung im Fibuposten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="240db-300">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="240db-301">Nach erfolgreicher Ausführung wird die Tabelle geleert.</span><span class="sxs-lookup"><span data-stu-id="240db-301">After a successful run, the table is emptied.</span></span>

## <a name="see-also"></a><span data-ttu-id="240db-302">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="240db-302">See Also</span></span>  
[<span data-ttu-id="240db-303">Designdetails: Lagerkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="240db-303">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="240db-304">Designdetails: Artikelausgleich</span><span class="sxs-lookup"><span data-stu-id="240db-304">Design Details: Item Application</span></span>](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
