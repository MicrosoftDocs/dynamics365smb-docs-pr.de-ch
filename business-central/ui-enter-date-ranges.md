---
title: "Einstellungsgültigkeiten in Business Central  | Microsoft Docs"
description: "Erhalten von Informationen zum Anzeigen von Daten aus bestimmten Zeiträumen mithilfe von Business Central"
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: de-ch
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="b213b-103">Datenbereiche eingeben</span><span class="sxs-lookup"><span data-stu-id="b213b-103">Entering Date Ranges</span></span>
<span data-ttu-id="b213b-104">Sie können Filter mit einem Start- und Enddatum setzen, sodass lediglich die Daten angezeigt werden, die innerhalb eines bestimmten Datumsbereichs oder Zeitintervalls liegen.</span><span class="sxs-lookup"><span data-stu-id="b213b-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="b213b-105">Für das Festlegen von Datumsbereichen gelten besondere Regeln.</span><span class="sxs-lookup"><span data-stu-id="b213b-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="b213b-106">Als Beispiel nehmen wir die **Top 10 Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="b213b-106">Let's take the **Customer Top 10** as an example:</span></span>

![Einen Datumsbereich auf der Anforderungsseite der Top 10 Debitorenliste festlegen](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="b213b-108">Hier können Sie den Bericht auf eine Gültigkeit wie den letzten 2 Wochen oder insgesamt 6 Wochen oder einen beliebigen Bereich einschränken.</span><span class="sxs-lookup"><span data-stu-id="b213b-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="b213b-109">Um eine Gültigkeit festzulegen, geben Sie Daten ein und verwenden anschliessend **..**</span><span class="sxs-lookup"><span data-stu-id="b213b-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="b213b-110">oder **|**, um den Bereich zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b213b-110">or **|** to set the range.</span></span> <span data-ttu-id="b213b-111">Im vorliegenden Beispiel müssen Sie, um die ersten zwei Wochen des Mai für die Top 10 Debitoren anzuzeigen, den Datumsfilter auf *05 01 17..05 14 17* setzen.</span><span class="sxs-lookup"><span data-stu-id="b213b-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="b213b-112">Hier finden Sie einige andere Beispiele:</span><span class="sxs-lookup"><span data-stu-id="b213b-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="b213b-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b213b-113">Meaning</span></span> | <span data-ttu-id="b213b-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b213b-114">Example</span></span> | <span data-ttu-id="b213b-115">Enthaltene Posten</span><span class="sxs-lookup"><span data-stu-id="b213b-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="b213b-116">Ist gleich</span><span class="sxs-lookup"><span data-stu-id="b213b-116">Equal to</span></span>| <span data-ttu-id="b213b-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="b213b-117">12 15 16</span></span> |<span data-ttu-id="b213b-118">Nur jene, die am 15. Deuzember 2016 gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="b213b-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="b213b-119">Intervall</span><span class="sxs-lookup"><span data-stu-id="b213b-119">Interval</span></span>| <span data-ttu-id="b213b-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="b213b-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="b213b-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="b213b-121">..12 15 16</span></span>|<span data-ttu-id="b213b-122">Jene, die zwischen dem 15. Dezember 2016 und dem 15. Januar 2017 (einschliesslich) gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="b213b-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="b213b-123">Jene, die bis zum 15. Dezember 2016 oder früher gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="b213b-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="b213b-124">Entweder/oder</span><span class="sxs-lookup"><span data-stu-id="b213b-124">Either/or</span></span>|<span data-ttu-id="b213b-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="b213b-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="b213b-126">Entweder am 15. Dezember oder am 16. Dezember 2016 gebucht.</span><span class="sxs-lookup"><span data-stu-id="b213b-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="b213b-127">Falls es Posten gibt, die an einem der beiden Tage gebucht wurden, werden diese angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b213b-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="b213b-128">Sie können auch die verschiedenen Formattypen miteinander kombinieren.</span><span class="sxs-lookup"><span data-stu-id="b213b-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="b213b-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b213b-129">Example</span></span> | <span data-ttu-id="b213b-130">Enthaltene Posten</span><span class="sxs-lookup"><span data-stu-id="b213b-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="b213b-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="b213b-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="b213b-132">Posten, die am 15. Dezember 2016 oder zwischen dem 01. Dezember 2016 und 31. Mai 2017 (einschliesslich) gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="b213b-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="b213b-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="b213b-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="b213b-134">Posten, die bis einschliesslich zum 14. Dezember oder am bzw. nach dem 30. Dezember gebucht wurden. Mit diesem Filter können Sie alle Posten ausschliessen, die zwischen den beiden angegebenen Tagen gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="b213b-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="b213b-135">Beachten Sie, dass wir das US-Datumsformat MMDDYY hier verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="b213b-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="b213b-136">[!INCLUDE[d365fin](includes/d365fin_md.md)] wird verfügbar in anderen Märkten, Sie haben die Möglichkeit, die Formaten zu verwenden, die möchten.</span><span class="sxs-lookup"><span data-stu-id="b213b-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="b213b-137">Datumsformeln verwenden</span><span class="sxs-lookup"><span data-stu-id="b213b-137">Using Date Formulas</span></span>
<span data-ttu-id="b213b-138">Bei einer Datumsformel handelt es sich um eine verkürzte Kombination aus Buchstaben und Zahlen, die zum Berechnen von Datumswerten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b213b-138">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="b213b-139">Datumsformeln können in verschiedenen Datumsberechnungsfeldern sowie in Felder vom Typ "Wiederholungsrate" (in wiederkehrenden Erf.-Journalen) eingeben werden.</span><span class="sxs-lookup"><span data-stu-id="b213b-139">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>

> [!NOTE]
>  <span data-ttu-id="b213b-140">In allen Formelfeldern wird automatisch ein Tag aufgenommen, um den heutigen Tag als den Tag abzudecken, an dem die Periode beginnt.</span><span class="sxs-lookup"><span data-stu-id="b213b-140">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="b213b-141">Wenn Sie beispielsweise **1W** eingeben, ist der Zeitraum tatsächlich acht Tage, da der aktuelle Tag (heute) eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b213b-141">Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="b213b-142">Wenn Sie einen Zeitraum von sieben Tagen (genau eine Woche) angeben möchten, in der das Startdatum eingeschlossen ist, müssen Sie **6D** oder **1W\-1D** eingeben.</span><span class="sxs-lookup"><span data-stu-id="b213b-142">To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.</span></span>

<span data-ttu-id="b213b-143">Nachfolgend einige Beispiele wie Datumsformeln eingesetzt werden können:</span><span class="sxs-lookup"><span data-stu-id="b213b-143">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="b213b-144">Die Datumsformel im Feld "Wiederholungsrate" in wiederkehrenden Journalen bestimmt, wie oft der Posten in der Journalzeile gebucht werden wird.</span><span class="sxs-lookup"><span data-stu-id="b213b-144">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="b213b-145">Das Datumsformat im Feld **Frist** für eine bestimmte Erinnerungsstufe bestimmt den Zeitraum, der ab dem Fälligkeitsdatum (oder dem Fälligkeitsdatum der vorherigen Erinnerung) verstreichen muss, bevor eine Erinnerung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b213b-145">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.</span></span>

-   <span data-ttu-id="b213b-146">Das Datumsformat im Feld **Berechnung des Fälligkeitsdatums** bestimmt, wie das Fälligkeitsdatum auf der Erinnerung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="b213b-146">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="b213b-147">Die Datumsberechnungsformel kann maximal 20 Zeichen (Buchstaben und Zahlen) enthalten.</span><span class="sxs-lookup"><span data-stu-id="b213b-147">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="b213b-148">Für die Berechnungszeiträume können die folgenden Abkürzungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b213b-148">You can use the following letters, which are abbreviations for time specifications.</span></span>

|  <span data-ttu-id="b213b-149">Brief</span><span class="sxs-lookup"><span data-stu-id="b213b-149">Letter</span></span>  |  <span data-ttu-id="b213b-150">Zeitspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b213b-150">Time specification</span></span>  |
|----------|----------------------|
|<span data-ttu-id="b213b-151">U</span><span class="sxs-lookup"><span data-stu-id="b213b-151">C</span></span>|<span data-ttu-id="b213b-152">Aktuell</span><span class="sxs-lookup"><span data-stu-id="b213b-152">Current</span></span>|
|<span data-ttu-id="b213b-153">T</span><span class="sxs-lookup"><span data-stu-id="b213b-153">D</span></span>|<span data-ttu-id="b213b-154">Tag\(e\)</span><span class="sxs-lookup"><span data-stu-id="b213b-154">Day\(s\)</span></span>|
|<span data-ttu-id="b213b-155">W</span><span class="sxs-lookup"><span data-stu-id="b213b-155">W</span></span>|<span data-ttu-id="b213b-156">Woche\(n\)</span><span class="sxs-lookup"><span data-stu-id="b213b-156">Week\(s\)</span></span>|
|<span data-ttu-id="b213b-157">M</span><span class="sxs-lookup"><span data-stu-id="b213b-157">M</span></span>|<span data-ttu-id="b213b-158">Monat\(e\)</span><span class="sxs-lookup"><span data-stu-id="b213b-158">Month\(s\)</span></span>|
|<span data-ttu-id="b213b-159">Q</span><span class="sxs-lookup"><span data-stu-id="b213b-159">Q</span></span>|<span data-ttu-id="b213b-160">Quartal\(e\)</span><span class="sxs-lookup"><span data-stu-id="b213b-160">Quarter\(s\)</span></span>|
|<span data-ttu-id="b213b-161">J</span><span class="sxs-lookup"><span data-stu-id="b213b-161">Y</span></span>|<span data-ttu-id="b213b-162">Jahr\(e\)</span><span class="sxs-lookup"><span data-stu-id="b213b-162">Year\(s\)</span></span>|

<span data-ttu-id="b213b-163">Datumsformeln können auf drei Arten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b213b-163">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="b213b-164">Im folgenden Beispiel wird veranschaulicht, wie Sie **C**, für aktuell und eine Zeiteinheit verwenden.</span><span class="sxs-lookup"><span data-stu-id="b213b-164">The following example shows how to use **C**, for current, and a time unit.</span></span>

|  <span data-ttu-id="b213b-165">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="b213b-165">Expression</span></span>  |  <span data-ttu-id="b213b-166">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b213b-166">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="b213b-167">LW</span><span class="sxs-lookup"><span data-stu-id="b213b-167">CW</span></span>|<span data-ttu-id="b213b-168">Laufende Woche</span><span class="sxs-lookup"><span data-stu-id="b213b-168">Current week</span></span>|
|<span data-ttu-id="b213b-169">LM</span><span class="sxs-lookup"><span data-stu-id="b213b-169">CM</span></span>|<span data-ttu-id="b213b-170">Laufender Monat</span><span class="sxs-lookup"><span data-stu-id="b213b-170">Current month</span></span>|

<span data-ttu-id="b213b-171">Im folgenden Beispiel wird veranschaulicht, wie Sie eine Zahl und eine Zeiteinheit verwenden.</span><span class="sxs-lookup"><span data-stu-id="b213b-171">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="b213b-172">Eine Zahl darf nicht grösser sein als 9999.</span><span class="sxs-lookup"><span data-stu-id="b213b-172">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="b213b-173">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="b213b-173">Expression</span></span>  |  <span data-ttu-id="b213b-174">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b213b-174">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="b213b-175">10T</span><span class="sxs-lookup"><span data-stu-id="b213b-175">10D</span></span>|<span data-ttu-id="b213b-176">10 Tage von heute an</span><span class="sxs-lookup"><span data-stu-id="b213b-176">10 days from today</span></span>|
|<span data-ttu-id="b213b-177">2W</span><span class="sxs-lookup"><span data-stu-id="b213b-177">2W</span></span>|<span data-ttu-id="b213b-178">2 Wochen von heute an</span><span class="sxs-lookup"><span data-stu-id="b213b-178">2 weeks from today</span></span>|

<span data-ttu-id="b213b-179">Im folgenden Beispiel wird veranschaulicht, wie Sie eine Zeiteinheit und eine Zahl verwenden.</span><span class="sxs-lookup"><span data-stu-id="b213b-179">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="b213b-180">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="b213b-180">Expression</span></span>  |  <span data-ttu-id="b213b-181">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b213b-181">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="b213b-182">T10</span><span class="sxs-lookup"><span data-stu-id="b213b-182">D10</span></span>|<span data-ttu-id="b213b-183">Am 10. des Monats</span><span class="sxs-lookup"><span data-stu-id="b213b-183">The next 10th day of a month</span></span>|
|<span data-ttu-id="b213b-184">WT4</span><span class="sxs-lookup"><span data-stu-id="b213b-184">WD4</span></span>|<span data-ttu-id="b213b-185">Der nächste 4. einer Woche \(Donnerstag\)</span><span class="sxs-lookup"><span data-stu-id="b213b-185">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="b213b-186">Das folgende Beispiel zeigt, wie Sie diese drei Formulare nach Bedarf kombinieren können.</span><span class="sxs-lookup"><span data-stu-id="b213b-186">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="b213b-187">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="b213b-187">Expression</span></span>  |  <span data-ttu-id="b213b-188">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b213b-188">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="b213b-189">CM\+10D</span><span class="sxs-lookup"><span data-stu-id="b213b-189">CM\+10D</span></span>|<span data-ttu-id="b213b-190">Aktueller Monat\+ 10 Tage</span><span class="sxs-lookup"><span data-stu-id="b213b-190">Current month \+ 10 days</span></span>|

<span data-ttu-id="b213b-191">Das folgende Beispiel zeigt, wie Sie ein Minuszeichen verwenden können, um anzugeben, dass es sich um ein Datum in der Vergangenheit handelt.</span><span class="sxs-lookup"><span data-stu-id="b213b-191">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="b213b-192">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="b213b-192">Expression</span></span>  |  <span data-ttu-id="b213b-193">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b213b-193">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="b213b-194">-1J</span><span class="sxs-lookup"><span data-stu-id="b213b-194">-1Y</span></span>|<span data-ttu-id="b213b-195">Heute vor einem Jahr</span><span class="sxs-lookup"><span data-stu-id="b213b-195">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="b213b-196">Wenn für den Lagerort einen Basiskalender verwendet, wird das Datumsformular, das Sie eingeben, zum Beispiel das Feld **Transportzeit**, entsprechend der Kalenderarbeitstage interpretiert.</span><span class="sxs-lookup"><span data-stu-id="b213b-196">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="b213b-197">Zum Beispiel entspricht **1W** sieben Arbeitstagen.</span><span class="sxs-lookup"><span data-stu-id="b213b-197">For example, **1W**  means seven working days.</span></span>

## <a name="see-also"></a><span data-ttu-id="b213b-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b213b-198">See Also</span></span>
<span data-ttu-id="b213b-199">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b213b-199">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b213b-200">Terminberechnung für Einkäufe</span><span class="sxs-lookup"><span data-stu-id="b213b-200">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="b213b-201">Eingeben von Kriterien in Filtern</span><span class="sxs-lookup"><span data-stu-id="b213b-201">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

