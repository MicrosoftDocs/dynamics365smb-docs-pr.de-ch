---
title: Eingeben von Datumsangaben und Uhrzeiten in Business Central  | Microsoft Docs
description: Erfahren Sie, wie Sie Datumsangaben und Uhrzeiten einschliesslich verschiedener Produktivitätstipps wie Stenografie, Ausdrücke und Bereiche eingegeben. Filtern Sie Listen oder Berichte bis zu einem bestimmten Datum oder zu Zeiträumen.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 853a45dc32907c2d9b69f7b2e592dc164c20a094
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757381"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="ff48f-104">Arbeiten mit Datumsangaben und Uhrzeiten in Kalendern</span><span class="sxs-lookup"><span data-stu-id="ff48f-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[prod_short](includes/prod_long.md)] <span data-ttu-id="ff48f-105">bietet mehrere Möglichkeiten, Datumsangaben und Uhrzeiten einzugeben, einschliesslich leistungsstarker Funktionen, die die Dateneingabe beschleunigen oder Ihnen helfen, komplexe Kalenderausdrücke zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ff48f-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="ff48f-106">Es gibt verschiedene Bereiche in der Anwendung, in denen Sie Daten und Uhrzeiten in die Felder eingeben können.</span><span class="sxs-lookup"><span data-stu-id="ff48f-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="ff48f-107">So können Sie beispielsweise das Warenausgangsdatum für einen Auftrag festlegen.</span><span class="sxs-lookup"><span data-stu-id="ff48f-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="ff48f-108">Wenn Sie Listen oder Berichtsdaten filtern, können Sie Datumswerten und Uhrzeiten eingeben, um genau die Daten zu finden, an denen Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="ff48f-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="ff48f-109">Überprüfen Ihrer Bereichs- und Spracheneinstellungen</span><span class="sxs-lookup"><span data-stu-id="ff48f-109">Check your region and language settings</span></span>
<span data-ttu-id="ff48f-110">Die Seite **Meine Einstellungen** gibt die **Region** und **Sprache** an, die Sie in der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-110">The **My Settings** page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="ff48f-111">Diese Einstellungen beeinflussen, wie Sie Datumswerte und Uhrzeiten eingeben.</span><span class="sxs-lookup"><span data-stu-id="ff48f-111">These settings influence how you enter dates and times.</span></span>

-   <span data-ttu-id="ff48f-112">Die Einstellung **Region** bestimmt, wie Daten, Uhrzeiten, Ziffern und Währungen angezeigt oder formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="ff48f-113">Bei Datumsmustern, die Begriffe enthalten, muss die Sprache der Begriffe, die Sie verwenden, der **Sprache**-Einstellung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ff48f-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] <span data-ttu-id="ff48f-114">verwendet das gregorianische Kalendersystem.</span><span class="sxs-lookup"><span data-stu-id="ff48f-114">uses the Gregorian calendar system.</span></span>

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="ff48f-115">Datumswerte eingeben</span><span class="sxs-lookup"><span data-stu-id="ff48f-115">Entering Dates</span></span>

<span data-ttu-id="ff48f-116">In einem Datumsfeld können Sie unter Verwendung des Standardformats ein Datum für Ihre Bereichseinstellung eingeben.</span><span class="sxs-lookup"><span data-stu-id="ff48f-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="ff48f-117">Verschiedene Regionen können verschiedene Trennzeichen zwischen Tagen, Monaten und Jahren verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="ff48f-118">Beispielsweise werden in einigen Regionen Bindestriche verwendet (mm-tt-jjjj) und in anderen werden Schrägstriche verwenden (mm/tt/jjjj).</span><span class="sxs-lookup"><span data-stu-id="ff48f-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="ff48f-119">Sie können allerdings sämtliche Trennzeichen verwenden, sogar einen Leerzeichen, und das Datum wird automatisch zu den Trennzeichen geändert, die Ihrer Region entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ff48f-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="ff48f-120">Beachten Sie, dass, das Format, in dem Datumswerte in gedruckten Berichten oder per E-Mail gesendeten Belegen von Ihrer persönlichen Regionseinstellung nicht beeinflusst wird.</span><span class="sxs-lookup"><span data-stu-id="ff48f-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="ff48f-121">Um produktiver mit Datumswerten und Uhrzeiten zu arbeiten, können Sie alle Methoden oder Formate verwenden, die in den folgenden Abschnitten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span>

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="ff48f-122">Datumsangaben aus dem Kalender auswählen</span><span class="sxs-lookup"><span data-stu-id="ff48f-122">Picking dates from the calendar</span></span>

<span data-ttu-id="ff48f-123">Alle Felder, die ein Kalendersymbol anzeigen, können mithilfe der Kalendertagauswahl festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="ff48f-124">Um die Kalendertagauswahl anzuzeigen, aktivieren Sie das Kalendersymbol oder drücken Sie die Tastenkombination CTRL+Home im Feld.</span><span class="sxs-lookup"><span data-stu-id="ff48f-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="ff48f-125">![Datumsfelder](media/ui-date-field.png "Beispiel für ein Datumsfeld")</span><span class="sxs-lookup"><span data-stu-id="ff48f-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="ff48f-126">Weitere Informationen unter [Tastenkombinationen in der Kalenderdatumsauswahl](keyboard-shortcuts.md#calendarshortcuts).</span><span class="sxs-lookup"><span data-stu-id="ff48f-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts).</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="ff48f-127">Tag\-Woche\-Jahr-Muster</span><span class="sxs-lookup"><span data-stu-id="ff48f-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="ff48f-128">Sie können ein Datum als Wochentag gefolgt von einer Wochennummer und optional einem Jahr eingeben.</span><span class="sxs-lookup"><span data-stu-id="ff48f-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="ff48f-129">Beispielsweise bedeutet Mo25 oder mo25 Montag in der 25. Woche</span><span class="sxs-lookup"><span data-stu-id="ff48f-129">For example, Mon25 or mon25 means Monday in week 25.</span></span> <span data-ttu-id="ff48f-130">Wenn Sie kein Jahr eingeben, wird das Jahr des Arbeitsdatums verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff48f-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="ff48f-131">Anstatt das gesamte Wort für den Wochentag einzugeben, können Sie vom Anfang an einen Teil des Begriffs eingeben.</span><span class="sxs-lookup"><span data-stu-id="ff48f-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="ff48f-132">Bei Konflikten (wie bei S für Samstag oder Sonntag) werden die Tage entsprechend der Bereichseinstellung ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="ff48f-132">In case of conflicts (such as with s which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="ff48f-133">Die Eingabe wird zuerst nach Arbeitsdatum und heute ausgewertet, beachten Sie dies bei der Abkürzung.</span><span class="sxs-lookup"><span data-stu-id="ff48f-133">The input is first evaluated against workdate and today as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="ff48f-134">Beispielsweise bedeutet h heute, daher kann es nicht "Dienstag" oder "Donnerstag" bedeuten.</span><span class="sxs-lookup"><span data-stu-id="ff48f-134">For example, t already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="ff48f-135">Das Kalenderwocheschema folgt immer ISO 8601. Dabei ist Woche 1, in die der 4. Januar fällt, oder die Woche mit dem ersten Donnerstag des Jahres.</span><span class="sxs-lookup"><span data-stu-id="ff48f-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="ff48f-136">Ziffernmuster</span><span class="sxs-lookup"><span data-stu-id="ff48f-136">Digit patterns</span></span>

<span data-ttu-id="ff48f-137">In einem Datumsfeld können zwei-, vier-, sechs- oder achtstellige Werte eingegeben werden:</span><span class="sxs-lookup"><span data-stu-id="ff48f-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="ff48f-138">Wenn Sie nur zwei Ziffern eingeben, wird dies als Tagesangabe interpretiert, es gilt also der Monat und das Jahr des Arbeitsdatums.</span><span class="sxs-lookup"><span data-stu-id="ff48f-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="ff48f-139">Wenn Sie vier Ziffern eingeben, wird dies als Tages- und Monatsangabe interpretiert, es gilt also das Jahr des Arbeitsdatums.</span><span class="sxs-lookup"><span data-stu-id="ff48f-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="ff48f-140">Die Reihenfolge von Tag und Monat wird durch Ihre Regionseinstellungen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="ff48f-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="ff48f-141">Selbst wenn Ihre Regionseinstellungen das Jahr vor den Tag und Monat stellen, werden vier Ziffern als Tag und Monat interpretiert.</span><span class="sxs-lookup"><span data-stu-id="ff48f-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="ff48f-142">Wenn Sie ein Datum zwischen dem 01.01.1930 und dem 31.12.2029 eingeben wollen, können Sie das Jahr zweistellig eingeben; ansonsten sollten Sie das Jahr vierstellig angeben.</span><span class="sxs-lookup"><span data-stu-id="ff48f-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="ff48f-143">Heute</span><span class="sxs-lookup"><span data-stu-id="ff48f-143">Today</span></span>

<span data-ttu-id="ff48f-144">Geben Sie das Wort für heute in der Sprache ein, die von der **Sprach**-Einstellung festgelegt wird. Dadurch wird das Datum auf das aktuelle Datum festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ff48f-144">Enter the word for today, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="ff48f-145">Anstatt den gesamten Begriff einzugeben, können Sie einen Teil des Begriffs eingeben. Beginnen Sie mit h oder heu, sofern dies nicht auch der Beginn eines anderen Begriffs ist.</span><span class="sxs-lookup"><span data-stu-id="ff48f-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as t or tod, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="ff48f-146">Periode</span><span class="sxs-lookup"><span data-stu-id="ff48f-146">Period</span></span>

<span data-ttu-id="ff48f-147">Wenn Sie eine bestimmte Buchhaltungsperiode filtern möchten, geben Sie in einem Datumsfeld den Buchstaben P oder das Wort Periode ein, gefolgt von einer Nummer, die die Buchhaltungsperiode identifiziert, z. B. P2 oder Periode 4.</span><span class="sxs-lookup"><span data-stu-id="ff48f-147">To filter on a specific accounting period, in a date field enter the letter p, or the word period, followed by a number that identifies the accounting period, like p2 or period4.</span></span> <span data-ttu-id="ff48f-148">Die Buchhaltungsperiode ist relativ zum Geschäftsjahr des aktuellen Arbeitsdatums, das von Ihrem Rollencenter festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ff48f-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="ff48f-149">Wenn beispielsweise das Arbeitsdatum **21.03.20** lautet, dann filtert P1 oder einfach P in der ersten Buchhaltungsperiode des Geschäftsjahres 2020 (wie 1.1.20..31.1.20).</span><span class="sxs-lookup"><span data-stu-id="ff48f-149">For example, if the work date is **03/21/20**, then p1, or just p, filters on the first accounting period of the fiscal year 2020 (such as 01/01/20..01/31/20).</span></span> <span data-ttu-id="ff48f-150">P15 filtert den Fünfzehnten der Buchhaltungsperiode ab dem Anfang des Geschäftsjahres 2020 (wie 1.3.21..21.3.21).</span><span class="sxs-lookup"><span data-stu-id="ff48f-150">p15 filters on the fifteenth accounting period from the start of fiscal year 2020 (such as 03/01/21..03/31/21).</span></span>

<span data-ttu-id="ff48f-151">Die Buchhaltungsperioden werden auf der Seite **Buchhaltungsperiode** definiert.</span><span class="sxs-lookup"><span data-stu-id="ff48f-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="ff48f-152">Um die Buchhaltungsperioden anzuzeigen oder zu ändern, öffnen Sie [hier](https://businesscentral.dynamics.com/?page=100) die Seite.</span><span class="sxs-lookup"><span data-stu-id="ff48f-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="ff48f-153">Aktuelles Arbeitsdatum</span><span class="sxs-lookup"><span data-stu-id="ff48f-153">Current work date</span></span>

<span data-ttu-id="ff48f-154">Die Arbeitsdatumsfunktion ermöglicht es Ihnen Übergänge mithilfe eines Datums aufzuzeichnen, das sich vom aktuellen Datum unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="ff48f-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="ff48f-155">Das für Wort "Arbeitsdatum" in der Sprache, die in der Einstellung **Sprache** festgelegt ist, legt das Datum auf das aktuell festgelegte Arbeitsdatum fest, das auf der Seite **Meine Einstellungen** definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ff48f-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the **My Settings** page.</span></span> <span data-ttu-id="ff48f-156">Anstatt das gesamte Wort einzugeben, können Sie vom Anfang an einen Teil des Begriffs eingeben, z. B. 'A' oder 'Arbeit'.</span><span class="sxs-lookup"><span data-stu-id="ff48f-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="ff48f-157">Wenn Sie kein Arbeitsdatum definiert haben, wird das aktuelle Datum als Arbeitsdatum verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff48f-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="ff48f-158">Die Verwendung des Arbeitsdatums ist hilfreich, wenn eine Vielzahl von Transaktionen zu einem Datum ausgeführt werden müssen, das vom Systemdatum abweicht.</span><span class="sxs-lookup"><span data-stu-id="ff48f-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="ff48f-159">Weitere Informationen finden Sie unter [Ändern von grundlegenden Einstellungen, wie Arbeitsdatum](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="ff48f-159">See also [Change Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="ff48f-160">Ultimodatum</span><span class="sxs-lookup"><span data-stu-id="ff48f-160">Closing Date</span></span>

<span data-ttu-id="ff48f-161">Darüber hinaus gibt es das Ultimodatum, das bei einer Nullstellung der GuV-Konten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff48f-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="ff48f-162">Technisch gesehen liegt ein Ultimodatum zwischen zwei Datumswerten, beispielsweise zwischen dem 31. Dezember und dem 1. Januar.</span><span class="sxs-lookup"><span data-stu-id="ff48f-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="ff48f-163">Um zu definieren, dass eine Datumsangabe ein Abschlussdatum ist, setzen Sie ein A um anzugeben, dass es sich bei diesem Datum um ein Abschlussdatum handelt, z. B. A31.12.01.</span><span class="sxs-lookup"><span data-stu-id="ff48f-163">To specify that a date is a closing date, put C just before the date, such as C123101.</span></span> <span data-ttu-id="ff48f-164">Dies kann in Verbindung mit allen Datumsmustern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="ff48f-165">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff48f-165">Examples</span></span>

<span data-ttu-id="ff48f-166">Die folgende Tabelle enthält Beispiele von Datumsangaben, die alle diese Formate verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="ff48f-167">Es werden Regionseinstellungen angenommen, mit der die Uhrzeit wie folgt formatiert wird: **Tag.Monat.Jahr.**, eine Woche, die mit Montag beginnt und die englische Sprache.</span><span class="sxs-lookup"><span data-stu-id="ff48f-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="ff48f-168">**Eingabe**</span><span class="sxs-lookup"><span data-stu-id="ff48f-168">**Entry**</span></span>      |<span data-ttu-id="ff48f-169">**Interpretation**</span><span class="sxs-lookup"><span data-stu-id="ff48f-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="ff48f-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="ff48f-170">2018.12.31.</span></span>|<span data-ttu-id="ff48f-171">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="ff48f-171">2018.12.31.</span></span>|
|<span data-ttu-id="ff48f-172">181231</span><span class="sxs-lookup"><span data-stu-id="ff48f-172">181231</span></span>|<span data-ttu-id="ff48f-173">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="ff48f-173">2018.12.31.</span></span>|
|<span data-ttu-id="ff48f-174">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="ff48f-174">18.12.31.</span></span>|<span data-ttu-id="ff48f-175">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="ff48f-175">2018.12.31.</span></span>|
|<span data-ttu-id="ff48f-176">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="ff48f-176">18.12.31.</span></span>|<span data-ttu-id="ff48f-177">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="ff48f-177">2018.12.31.</span></span>|
|<span data-ttu-id="ff48f-178">20181231</span><span class="sxs-lookup"><span data-stu-id="ff48f-178">20181231</span></span>|<span data-ttu-id="ff48f-179">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="ff48f-179">2018.12.31.</span></span>|
|<span data-ttu-id="ff48f-180">18/12,31</span><span class="sxs-lookup"><span data-stu-id="ff48f-180">18/12,31</span></span>|<span data-ttu-id="ff48f-181">31.12.2018</span><span class="sxs-lookup"><span data-stu-id="ff48f-181">2018.12.31.</span></span>|
|<span data-ttu-id="ff48f-182">11</span><span class="sxs-lookup"><span data-stu-id="ff48f-182">11</span></span>|<span data-ttu-id="ff48f-183">11.Arbeitsdatum Monat.Arbeitsdatum Jahr</span><span class="sxs-lookup"><span data-stu-id="ff48f-183">work date year.work date month.11.</span></span>|
|<span data-ttu-id="ff48f-184">11.12</span><span class="sxs-lookup"><span data-stu-id="ff48f-184">1112</span></span>|<span data-ttu-id="ff48f-185">12.11.Arbeitsdatum Jahr.</span><span class="sxs-lookup"><span data-stu-id="ff48f-185">work date year.11.12.</span></span>|
|<span data-ttu-id="ff48f-186">h für heute</span><span class="sxs-lookup"><span data-stu-id="ff48f-186">t or today</span></span>|<span data-ttu-id="ff48f-187">heutiges Datum</span><span class="sxs-lookup"><span data-stu-id="ff48f-187">today's date</span></span>|
|<span data-ttu-id="ff48f-188">Periode4</span><span class="sxs-lookup"><span data-stu-id="ff48f-188">p4</span></span>|<span data-ttu-id="ff48f-189">Datumsbereich, der die vierte Buchhaltungsperiode enthält, z. B. 1.4.20..30.4.20</span><span class="sxs-lookup"><span data-stu-id="ff48f-189">date range that includes the fourth accounting period, such as 04/01/20..04/30/20</span></span>|
|<span data-ttu-id="ff48f-190">a oder Arbeitsdatum</span><span class="sxs-lookup"><span data-stu-id="ff48f-190">w or workdate</span></span>|<span data-ttu-id="ff48f-191">das Arbeitsdatum</span><span class="sxs-lookup"><span data-stu-id="ff48f-191">the working date</span></span>|
|<span data-ttu-id="ff48f-192">"m" oder "Montag"</span><span class="sxs-lookup"><span data-stu-id="ff48f-192">m or Monday</span></span>|<span data-ttu-id="ff48f-193">Montag der Woche des Arbeitsdatums</span><span class="sxs-lookup"><span data-stu-id="ff48f-193">Monday of the work date week</span></span>|
|<span data-ttu-id="ff48f-194">"d" oder "Dienstag"</span><span class="sxs-lookup"><span data-stu-id="ff48f-194">tu or Tuesday</span></span>|<span data-ttu-id="ff48f-195">Dienstag der Woche des Arbeitsdatums</span><span class="sxs-lookup"><span data-stu-id="ff48f-195">Tuesday of the work date week</span></span>|
|<span data-ttu-id="ff48f-196">Sa oder Samstag</span><span class="sxs-lookup"><span data-stu-id="ff48f-196">sa or Saturday</span></span>|<span data-ttu-id="ff48f-197">Samstag der Woche des Arbeitsdatums</span><span class="sxs-lookup"><span data-stu-id="ff48f-197">Saturday of the work date week</span></span>|
|<span data-ttu-id="ff48f-198">So oder Sonntag</span><span class="sxs-lookup"><span data-stu-id="ff48f-198">s or Sunday</span></span>|<span data-ttu-id="ff48f-199">Sonntag der Woche des Arbeitsdatums</span><span class="sxs-lookup"><span data-stu-id="ff48f-199">Sunday of the work date week</span></span>|
|<span data-ttu-id="ff48f-200">H23</span><span class="sxs-lookup"><span data-stu-id="ff48f-200">t23</span></span>|<span data-ttu-id="ff48f-201">Dienstag von Woche 23 des Arbeitsjahres</span><span class="sxs-lookup"><span data-stu-id="ff48f-201">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="ff48f-202">h 23</span><span class="sxs-lookup"><span data-stu-id="ff48f-202">t 23</span></span>|<span data-ttu-id="ff48f-203">Dienstag von Woche 23 des Arbeitsjahres</span><span class="sxs-lookup"><span data-stu-id="ff48f-203">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="ff48f-204">h-1</span><span class="sxs-lookup"><span data-stu-id="ff48f-204">t-1</span></span>|<span data-ttu-id="ff48f-205">Dienstag von Woche 1 des Arbeitsjahres</span><span class="sxs-lookup"><span data-stu-id="ff48f-205">Tuesday of week 1 of the work date year</span></span>|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="ff48f-206">Festlegen von Breichen</span><span class="sxs-lookup"><span data-stu-id="ff48f-206">Setting Ranges</span></span>

<span data-ttu-id="ff48f-207">In Listen, Summen und Berichten können Sie Filter für Datumsangaben, Uhrzeiten, Datums-/Uhrzeitangaben einrichten, die einen Startwert und optional einen Endwert haben, um nur die Datumsangaben anzuzeigen, die in diesem Bereich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ff48f-207">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="ff48f-208">Die Standardregeln gelten für die Methode, auf die Sie Datumsbereiche festlegen.</span><span class="sxs-lookup"><span data-stu-id="ff48f-208">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="ff48f-209">**Bedeutung**</span><span class="sxs-lookup"><span data-stu-id="ff48f-209">**Meaning**</span></span>|<span data-ttu-id="ff48f-210">**Beispielausdruck (Datum)**</span><span class="sxs-lookup"><span data-stu-id="ff48f-210">**Sample expression (Date)**</span></span>|<span data-ttu-id="ff48f-211">**Im Filter enthaltene Daten**</span><span class="sxs-lookup"><span data-stu-id="ff48f-211">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="ff48f-212">Intervall</span><span class="sxs-lookup"><span data-stu-id="ff48f-212">Interval</span></span>|<span data-ttu-id="ff48f-213">12.15 00:00:00 .. 01.15 01:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-213">12 15 00..01 15 01</span></span><br /><br /><span data-ttu-id="ff48f-214">..12.15 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-214">..12 15 00</span></span><br /><br /><span data-ttu-id="ff48f-215">Periode1..Periode4</span><span class="sxs-lookup"><span data-stu-id="ff48f-215">p1..p4</span></span>|<span data-ttu-id="ff48f-216">Datensätze mit Datumsangaben zwischen und einschliesslich dem 15.12.00 und dem 15.01.01.</span><span class="sxs-lookup"><span data-stu-id="ff48f-216">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="ff48f-217">Datensätze mit Datumsangaben vom 12 15 00 oder früher.</span><span class="sxs-lookup"><span data-stu-id="ff48f-217">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="ff48f-218">Datumsbereich, der die zweite, dritte und vierte Buchhaltungsperiode enthält, z. B. 01.01.20..30.04.20.</span><span class="sxs-lookup"><span data-stu-id="ff48f-218">Date range that includes the second, third, and fourth accounting periods, such as 01/01/20..04/30/20.</span></span>|
|<span data-ttu-id="ff48f-219">Entweder/oder</span><span class="sxs-lookup"><span data-stu-id="ff48f-219">Either/or</span></span>|<span data-ttu-id="ff48f-220">12 15 00\|12 16 00</span><span class="sxs-lookup"><span data-stu-id="ff48f-220">12 15 00\|12 16 00</span></span>|<span data-ttu-id="ff48f-221">Datensätze mit den Datumsangaben 12 15 00 oder 12 16 00.</span><span class="sxs-lookup"><span data-stu-id="ff48f-221">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="ff48f-222">Wenn es sowohl Datensätze mit Datumsangaben für beide Tage gibt, werden alle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ff48f-222">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="ff48f-223">Kombination</span><span class="sxs-lookup"><span data-stu-id="ff48f-223">Combination</span></span>|<span data-ttu-id="ff48f-224">12 15 00\|12 01 00..12 10 00</span><span class="sxs-lookup"><span data-stu-id="ff48f-224">12 15 00\|12 01 00..12 10 00</span></span>  <br /><br /><span data-ttu-id="ff48f-225">..12 14 00\|12 30 00..</span><span class="sxs-lookup"><span data-stu-id="ff48f-225">..12 14 00\|12 30 00..</span></span>|<span data-ttu-id="ff48f-226">Datensätze mit Datumsangaben vom 15.12.00 oder zwischen dem 01.12.00 und dem 10.12.00 einschliesslich.</span><span class="sxs-lookup"><span data-stu-id="ff48f-226">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <br /><br /><span data-ttu-id="ff48f-227">Datensätze mit einem Datum von 14.12.00 oder früher, oder mit einem Datum von 30.12.00 und später, d. h. alle Datensätze ausser solchen mit Datumsangaben zwischen dem 15.12.00 und dem 29.12.00 (jeweils einschliesslich).</span><span class="sxs-lookup"><span data-stu-id="ff48f-227">Records with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="ff48f-228">Sie können jedes der gültigen Formate in den Datumsbereichsfiltern verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-228">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="ff48f-229">Beispielsweise ergibt Mo 14.3..h 4P bei einem Datums-/Zeitangabenfeld einen Filter von 3 Uhr am Montag in der Woche 14 des Jahres des aktuellen Arbeitsdatums bis heute um 16 Uhr.</span><span class="sxs-lookup"><span data-stu-id="ff48f-229">For example, mon14 3..t 4p applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="ff48f-230">Datumsformeln verwenden</span><span class="sxs-lookup"><span data-stu-id="ff48f-230">Using Date Formulas</span></span>
<span data-ttu-id="ff48f-231">Bei einer Datumsformel handelt es sich um eine verkürzte Kombination aus Buchstaben und Zahlen, die zum Berechnen von Datumswerten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff48f-231">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="ff48f-232">Sie können Datumsformeln in verschiedenen Datumsberechnungsfeldern oder -filtern eingeben.</span><span class="sxs-lookup"><span data-stu-id="ff48f-232">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="ff48f-233">In allen Formelfeldern wird automatisch ein Tag aufgenommen, um den heutigen Tag als den Tag abzudecken, an dem die Periode beginnt.</span><span class="sxs-lookup"><span data-stu-id="ff48f-233">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="ff48f-234">Wenn Sie beispielsweise 1W eingeben, ist der Zeitraum tatsächlich acht Tage, da der aktuelle Tag (heute) eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ff48f-234">Accordingly, for example, if you enter 1W, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="ff48f-235">Um eine Periode von sieben Tagen \(tatsächlich eine Woche\) einschliesslich des Periodenstartdatums anzugeben, müssen Sie "6T" oder "1W-1T" eingeben.</span><span class="sxs-lookup"><span data-stu-id="ff48f-235">To specify a period of seven days \(one true week\) including the period starting date, then you must enter 6D or 1W-1D.</span></span>

<span data-ttu-id="ff48f-236">Nachfolgend einige Beispiele wie Datumsformeln eingesetzt werden können:</span><span class="sxs-lookup"><span data-stu-id="ff48f-236">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="ff48f-237">Die Datumsformel im Feld "Wiederholungsrate" in wiederkehrenden Journalen bestimmt, wie oft der Posten in der Journalzeile gebucht werden wird.</span><span class="sxs-lookup"><span data-stu-id="ff48f-237">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="ff48f-238">Anhand der Datumsformel im Feld **Toleranzperiode** für eine Mahnstufe wird die Zeit bestimmt, die vom Fälligkeitsdatum \(oder vom Datum der letzten Mahnung\) an vergehen muss, bevor eine Mahnung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ff48f-238">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="ff48f-239">Das Datumsformat im Feld **Berechnung des Fälligkeitsdatums** bestimmt, wie das Fälligkeitsdatum auf der Erinnerung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="ff48f-239">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="ff48f-240">Die Datumsformel kann maximal 20 Zeichen (Buchstaben und Zahlen) enthalten.</span><span class="sxs-lookup"><span data-stu-id="ff48f-240">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="ff48f-241">Für die Kalendereinheiten können die folgenden Abkürzungen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="ff48f-241">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="ff48f-242">Brief</span><span class="sxs-lookup"><span data-stu-id="ff48f-242">Letter</span></span>  |  <span data-ttu-id="ff48f-243">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ff48f-243">Meaning</span></span>  |
|----------|----------------------|
|<span data-ttu-id="ff48f-244">L</span><span class="sxs-lookup"><span data-stu-id="ff48f-244">C</span></span>|<span data-ttu-id="ff48f-245">Laufend</span><span class="sxs-lookup"><span data-stu-id="ff48f-245">Current</span></span>|
|<span data-ttu-id="ff48f-246">T</span><span class="sxs-lookup"><span data-stu-id="ff48f-246">D</span></span>|<span data-ttu-id="ff48f-247">Tag\(e\)</span><span class="sxs-lookup"><span data-stu-id="ff48f-247">Day\(s\)</span></span>|
|<span data-ttu-id="ff48f-248">W</span><span class="sxs-lookup"><span data-stu-id="ff48f-248">W</span></span>|<span data-ttu-id="ff48f-249">Woche\(n\)</span><span class="sxs-lookup"><span data-stu-id="ff48f-249">Week\(s\)</span></span>|
|<span data-ttu-id="ff48f-250">M</span><span class="sxs-lookup"><span data-stu-id="ff48f-250">M</span></span>|<span data-ttu-id="ff48f-251">Monat\(e\)</span><span class="sxs-lookup"><span data-stu-id="ff48f-251">Month\(s\)</span></span>|
|<span data-ttu-id="ff48f-252">Q</span><span class="sxs-lookup"><span data-stu-id="ff48f-252">Q</span></span>|<span data-ttu-id="ff48f-253">Quartal\(e\)</span><span class="sxs-lookup"><span data-stu-id="ff48f-253">Quarter\(s\)</span></span>|
|<span data-ttu-id="ff48f-254">J</span><span class="sxs-lookup"><span data-stu-id="ff48f-254">Y</span></span>|<span data-ttu-id="ff48f-255">Jahr\(e\)</span><span class="sxs-lookup"><span data-stu-id="ff48f-255">Year\(s\)</span></span>|

<span data-ttu-id="ff48f-256">Datumsformeln können auf drei Arten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-256">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="ff48f-257">Im folgenden Beispiel wird veranschaulicht, wie Sie A, für aktuell und eine Zeiteinheit verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-257">The following example shows how to use C, for current, and a time unit.</span></span>

|  <span data-ttu-id="ff48f-258">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="ff48f-258">Expression</span></span>  |  <span data-ttu-id="ff48f-259">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ff48f-259">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ff48f-260">LW</span><span class="sxs-lookup"><span data-stu-id="ff48f-260">CW</span></span>|<span data-ttu-id="ff48f-261">Laufende Woche</span><span class="sxs-lookup"><span data-stu-id="ff48f-261">Current week</span></span>|
|<span data-ttu-id="ff48f-262">LM</span><span class="sxs-lookup"><span data-stu-id="ff48f-262">CM</span></span>|<span data-ttu-id="ff48f-263">Laufender Monat</span><span class="sxs-lookup"><span data-stu-id="ff48f-263">Current month</span></span>|

<span data-ttu-id="ff48f-264">Im folgenden Beispiel wird veranschaulicht, wie Sie eine Zahl und eine Zeiteinheit verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-264">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="ff48f-265">Eine Zahl darf nicht grösser sein als 9999.</span><span class="sxs-lookup"><span data-stu-id="ff48f-265">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="ff48f-266">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="ff48f-266">Expression</span></span>  |  <span data-ttu-id="ff48f-267">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ff48f-267">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ff48f-268">10T</span><span class="sxs-lookup"><span data-stu-id="ff48f-268">10D</span></span>|<span data-ttu-id="ff48f-269">10 Tage von heute an</span><span class="sxs-lookup"><span data-stu-id="ff48f-269">10 days from today</span></span>|
|<span data-ttu-id="ff48f-270">2W</span><span class="sxs-lookup"><span data-stu-id="ff48f-270">2W</span></span>|<span data-ttu-id="ff48f-271">2 Wochen von heute an</span><span class="sxs-lookup"><span data-stu-id="ff48f-271">2 weeks from today</span></span>|

<span data-ttu-id="ff48f-272">Im folgenden Beispiel wird veranschaulicht, wie Sie eine Zeiteinheit und eine Zahl verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-272">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="ff48f-273">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="ff48f-273">Expression</span></span>  |  <span data-ttu-id="ff48f-274">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ff48f-274">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ff48f-275">T10</span><span class="sxs-lookup"><span data-stu-id="ff48f-275">D10</span></span>|<span data-ttu-id="ff48f-276">Am 10. des Monats</span><span class="sxs-lookup"><span data-stu-id="ff48f-276">The next 10th day of a month</span></span>|
|<span data-ttu-id="ff48f-277">WT4</span><span class="sxs-lookup"><span data-stu-id="ff48f-277">WD4</span></span>|<span data-ttu-id="ff48f-278">Der nächste 4. einer Woche \(Donnerstag\)</span><span class="sxs-lookup"><span data-stu-id="ff48f-278">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="ff48f-279">Das folgende Beispiel zeigt, wie Sie diese drei Formulare nach Bedarf kombinieren können.</span><span class="sxs-lookup"><span data-stu-id="ff48f-279">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="ff48f-280">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="ff48f-280">Expression</span></span>  |  <span data-ttu-id="ff48f-281">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ff48f-281">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ff48f-282">LM+10T</span><span class="sxs-lookup"><span data-stu-id="ff48f-282">CM+10D</span></span>|<span data-ttu-id="ff48f-283">Aktueller Monat\+ 10 Tage</span><span class="sxs-lookup"><span data-stu-id="ff48f-283">Current month \+ 10 days</span></span>|

<span data-ttu-id="ff48f-284">Das folgende Beispiel zeigt, wie Sie ein Minuszeichen verwenden können, um anzugeben, dass es sich um ein Datum in der Vergangenheit handelt.</span><span class="sxs-lookup"><span data-stu-id="ff48f-284">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="ff48f-285">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="ff48f-285">Expression</span></span>  |  <span data-ttu-id="ff48f-286">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ff48f-286">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ff48f-287">-1J</span><span class="sxs-lookup"><span data-stu-id="ff48f-287">-1Y</span></span>|<span data-ttu-id="ff48f-288">Heute vor einem Jahr</span><span class="sxs-lookup"><span data-stu-id="ff48f-288">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="ff48f-289">Wenn für den Lagerort einen Basiskalender verwendet, wird das Datumsformular, das Sie eingeben, zum Beispiel das Feld **Transportzeit**, entsprechend der Kalenderarbeitstage interpretiert.</span><span class="sxs-lookup"><span data-stu-id="ff48f-289">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="ff48f-290">Zum Beispiel entspricht 1W sieben Arbeitstagen.</span><span class="sxs-lookup"><span data-stu-id="ff48f-290">For example, 1W  means seven working days.</span></span>
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[prod_short](includes/prod_short.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a><span data-ttu-id="ff48f-291">Eingeben von Uhrzeiten</span><span class="sxs-lookup"><span data-stu-id="ff48f-291">Entering Times</span></span>
<span data-ttu-id="ff48f-292">Beim der Eingabe von Uhrzeiten können Sie alle Trennzeichen ausser Leerzeichen einfügen, die zwischen den Einheiten angegeben werden sollen. Bei der Verwendung von zweistelligen Zahlen für jede Einheit bis zu MilliseDebitoren ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ff48f-292">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="ff48f-293">Sie müssen lediglich die grössten Einheiten schreiben, die Sie benötigen; der Rest wird auf null gesetzt.</span><span class="sxs-lookup"><span data-stu-id="ff48f-293">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="ff48f-294">Sie können auch alle Tageszeitangaben (AM/PM) auslassen.</span><span class="sxs-lookup"><span data-stu-id="ff48f-294">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="ff48f-295">In der folgenden Tabelle finden Sie eine Liste über die Möglichkeiten zum Angeben von Uhrzeiten sowie die Interpretation der jeweiligen Angabe.</span><span class="sxs-lookup"><span data-stu-id="ff48f-295">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="ff48f-296">Es werden Regionseinstellungen angenommen, mit der die Uhrzeit wie folgt formatiert wird: **Stunden:Minuten: SeDebitoren:MilliseDebitoren.**</span><span class="sxs-lookup"><span data-stu-id="ff48f-296">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="ff48f-297">und verwenden die jeweiligen Tageszeitangaben (AM/PM).</span><span class="sxs-lookup"><span data-stu-id="ff48f-297">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="ff48f-298">**Eingabe**</span><span class="sxs-lookup"><span data-stu-id="ff48f-298">**Entry**</span></span>      |<span data-ttu-id="ff48f-299">**Interpretation**</span><span class="sxs-lookup"><span data-stu-id="ff48f-299">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="ff48f-300">05:23:17</span><span class="sxs-lookup"><span data-stu-id="ff48f-300">05:23:17</span></span>|<span data-ttu-id="ff48f-301">05:23:17</span><span class="sxs-lookup"><span data-stu-id="ff48f-301">05:23:17</span></span>|
|<span data-ttu-id="ff48f-302">5</span><span class="sxs-lookup"><span data-stu-id="ff48f-302">5</span></span>|<span data-ttu-id="ff48f-303">05:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-303">05:00:00</span></span>|
|<span data-ttu-id="ff48f-304">5AM</span><span class="sxs-lookup"><span data-stu-id="ff48f-304">5AM</span></span>|<span data-ttu-id="ff48f-305">05:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-305">05:00:00</span></span>|
|<span data-ttu-id="ff48f-306">5P</span><span class="sxs-lookup"><span data-stu-id="ff48f-306">5P</span></span>|<span data-ttu-id="ff48f-307">17:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-307">17:00:00</span></span>|
|<span data-ttu-id="ff48f-308">12</span><span class="sxs-lookup"><span data-stu-id="ff48f-308">12</span></span>|<span data-ttu-id="ff48f-309">12:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-309">12:00:00</span></span>|
|<span data-ttu-id="ff48f-310">12A</span><span class="sxs-lookup"><span data-stu-id="ff48f-310">12A</span></span>|<span data-ttu-id="ff48f-311">00:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-311">00:00:00</span></span>|
|<span data-ttu-id="ff48f-312">12P</span><span class="sxs-lookup"><span data-stu-id="ff48f-312">12P</span></span>|<span data-ttu-id="ff48f-313">12:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-313">12:00:00</span></span>|
|<span data-ttu-id="ff48f-314">17</span><span class="sxs-lookup"><span data-stu-id="ff48f-314">17</span></span>|<span data-ttu-id="ff48f-315">17:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-315">17:00:00</span></span>|
|<span data-ttu-id="ff48f-316">5:30</span><span class="sxs-lookup"><span data-stu-id="ff48f-316">5:30</span></span>|<span data-ttu-id="ff48f-317">05:30:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-317">05:30:00</span></span>|
|<span data-ttu-id="ff48f-318">0530</span><span class="sxs-lookup"><span data-stu-id="ff48f-318">0530</span></span>|<span data-ttu-id="ff48f-319">05:30:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-319">05:30:00</span></span>|
|<span data-ttu-id="ff48f-320">5:30:5</span><span class="sxs-lookup"><span data-stu-id="ff48f-320">5:30:5</span></span>|<span data-ttu-id="ff48f-321">05:30:05</span><span class="sxs-lookup"><span data-stu-id="ff48f-321">05:30:05</span></span>|
|<span data-ttu-id="ff48f-322">053005</span><span class="sxs-lookup"><span data-stu-id="ff48f-322">053005</span></span>|<span data-ttu-id="ff48f-323">05:30:05</span><span class="sxs-lookup"><span data-stu-id="ff48f-323">05:30:05</span></span>|
|<span data-ttu-id="ff48f-324">5:30:5,50</span><span class="sxs-lookup"><span data-stu-id="ff48f-324">5:30:5,50</span></span>|<span data-ttu-id="ff48f-325">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="ff48f-325">05:30:05.5</span></span>|
|<span data-ttu-id="ff48f-326">053005050</span><span class="sxs-lookup"><span data-stu-id="ff48f-326">053005050</span></span>|<span data-ttu-id="ff48f-327">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="ff48f-327">05:30:05.05</span></span>|

<span data-ttu-id="ff48f-328">Beachten Sie, dass MilliseDebitoren in Dezimalnotation angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-328">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="ff48f-329">Beispielsweise bedeuten 3, 30 und 300 Millisekunden während 03 bedeutet 39 und 003 bedeutet 3 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="ff48f-329">So, for example, 3, 30, and 300 all mean 300 milliseconds, while 03 means 30 and 003 means 3 milliseconds.</span></span>

<span data-ttu-id="ff48f-330">Sie können 24.00 nicht verwenden, um Mitternacht anzugeben oder einen Wert anzugeben, der grösser als 24:00 ist.</span><span class="sxs-lookup"><span data-stu-id="ff48f-330">You cannot use 24:00 to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="ff48f-331">Das für Wort für "Zeit" in der Sprache, die von [!INCLUDE[prod_short](includes/prod_long.md)] verwendet wird, wird in die aktuelle Uhrzeit auf Ihrem Computer oder mobilen Gerät umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="ff48f-331">The word for 'time' in the language used by [!INCLUDE[prod_short](includes/prod_long.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="ff48f-332">Sie können vom Anfang einem Teil des Begriffs eingeben, z. B. h oder TIM.</span><span class="sxs-lookup"><span data-stu-id="ff48f-332">You can enter any part of the word, starting from the beginning, such as t or TIM.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="ff48f-333">Eingeben kombinierter Datums- und Zeitangaben</span><span class="sxs-lookup"><span data-stu-id="ff48f-333">Entering combined Dates and Times</span></span>
<span data-ttu-id="ff48f-334">Wenn Sie Datums-/Uhrzeitangaben eingeben, die aus einem kombinierten Datum und einer Uhrzeit in einem Feld bestehen, müssen Sie ein Leerzeichen zwischen dem Datum und der Uhrzeit eingeben.</span><span class="sxs-lookup"><span data-stu-id="ff48f-334">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="ff48f-335">Der Datumsteil kann nur Stellen in Form von den offiziellen Datumstrennzeichen Ihrer Regionseinstellung enthalten.</span><span class="sxs-lookup"><span data-stu-id="ff48f-335">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="ff48f-336">Die Uhrzeit kann Stellen um die AM/AM-Angabe enthalten.</span><span class="sxs-lookup"><span data-stu-id="ff48f-336">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="ff48f-337">Sie können auch nur ein Datum in einem Datums-/Uhrzeitangabefeld eingeben, aber Sie können nicht bloss eine Uhrzeit angeben.</span><span class="sxs-lookup"><span data-stu-id="ff48f-337">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="ff48f-338">Die folgende Tabelle führt einige Beispiele von Datum-/Uhrzeitkombinationen auf.</span><span class="sxs-lookup"><span data-stu-id="ff48f-338">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="ff48f-339">Die Regionseinstellungen in den Beispielen zeigen Datumsangaben im Tag\-Monat\-Jahr-Format mit den AM/PM-Angaben, der englischen Sprache und Sonntag als Start der Woche an.</span><span class="sxs-lookup"><span data-stu-id="ff48f-339">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="ff48f-340">**Eingabe**</span><span class="sxs-lookup"><span data-stu-id="ff48f-340">**Entry**</span></span>      |<span data-ttu-id="ff48f-341">**Interpretation**</span><span class="sxs-lookup"><span data-stu-id="ff48f-341">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="ff48f-342">08-01-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="ff48f-342">08-01-2016 05:48:12 PM</span></span>|<span data-ttu-id="ff48f-343">08.01.2016 17:48:12</span><span class="sxs-lookup"><span data-stu-id="ff48f-343">08\-01\-2016 05:48:12 PM</span></span>|
|<span data-ttu-id="ff48f-344">131202 132455</span><span class="sxs-lookup"><span data-stu-id="ff48f-344">131202 132455</span></span>|<span data-ttu-id="ff48f-345">13.12.2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="ff48f-345">13\-12\-2002 13:24:55</span></span>|
|<span data-ttu-id="ff48f-346">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="ff48f-346">1-12-02 10</span></span>|<span data-ttu-id="ff48f-347">01.12.2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-347">01\-12\-2002 10:00:00</span></span>|
|<span data-ttu-id="ff48f-348">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="ff48f-348">1.12.02 5</span></span>|<span data-ttu-id="ff48f-349">01.12.2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-349">01\-12\-2002 05:00:00</span></span>|
|<span data-ttu-id="ff48f-350">1.12.02</span><span class="sxs-lookup"><span data-stu-id="ff48f-350">1.12.02</span></span>|<span data-ttu-id="ff48f-351">01.12.2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-351">01\-12\-2002 00:00:00</span></span>|
|<span data-ttu-id="ff48f-352">11 12</span><span class="sxs-lookup"><span data-stu-id="ff48f-352">11 12</span></span>|<span data-ttu-id="ff48f-353">11.Arbeitsdatum Monat.Arbeitsdatum Jahr 12:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-353">11\-work date month\-work date year 12:00:00</span></span>|
|<span data-ttu-id="ff48f-354">1112 12</span><span class="sxs-lookup"><span data-stu-id="ff48f-354">1112 12</span></span>|<span data-ttu-id="ff48f-355">11.12.Arbeitsdatum Jahr 12:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-355">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="ff48f-356">h für heute</span><span class="sxs-lookup"><span data-stu-id="ff48f-356">t or today</span></span>|<span data-ttu-id="ff48f-357">heutiges Datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-357">today's date 00:00:00</span></span>|
|<span data-ttu-id="ff48f-358">h 10:30</span><span class="sxs-lookup"><span data-stu-id="ff48f-358">t 10:30</span></span>|<span data-ttu-id="ff48f-359">heutiges Datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-359">today's date 10:30:00</span></span>|
|<span data-ttu-id="ff48f-360">h 3:3:3</span><span class="sxs-lookup"><span data-stu-id="ff48f-360">t 3:3:3</span></span>|<span data-ttu-id="ff48f-361">heutiges Datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="ff48f-361">today's date 03:03:03</span></span>|
|<span data-ttu-id="ff48f-362">a oder Arbeitsdatum</span><span class="sxs-lookup"><span data-stu-id="ff48f-362">w or workdate</span></span>|<span data-ttu-id="ff48f-363">das Arbeitsdatum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-363">the working date 00:00:00</span></span>|
|<span data-ttu-id="ff48f-364">"m" oder "Montag"</span><span class="sxs-lookup"><span data-stu-id="ff48f-364">m or Monday</span></span>|<span data-ttu-id="ff48f-365">Montag der Woche des Arbeitsdatums 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-365">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="ff48f-366">"d" oder "Dienstag"</span><span class="sxs-lookup"><span data-stu-id="ff48f-366">tu or Tuesday</span></span>|<span data-ttu-id="ff48f-367">Dienstag der Woche des Arbeitsdatums 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-367">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="ff48f-368">Sa oder Samstag</span><span class="sxs-lookup"><span data-stu-id="ff48f-368">sa or Saturday</span></span>|<span data-ttu-id="ff48f-369">Samstag der Woche des Arbeitsdatums 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-369">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="ff48f-370">So oder Sonntag</span><span class="sxs-lookup"><span data-stu-id="ff48f-370">s or Sunday</span></span>|<span data-ttu-id="ff48f-371">Sonntag der Woche des Arbeitsdatums 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-371">Sunday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="ff48f-372">di 10:30</span><span class="sxs-lookup"><span data-stu-id="ff48f-372">tu 10:30</span></span>|<span data-ttu-id="ff48f-373">Dienstag der Woche des Arbeitsdatums 10:30:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-373">Tuesday of the work date week 10:30:00</span></span>|
|<span data-ttu-id="ff48f-374">d 3:3:3</span><span class="sxs-lookup"><span data-stu-id="ff48f-374">tu 3:3:3</span></span>|<span data-ttu-id="ff48f-375">Dienstag der Woche des Arbeitsdatums 03:03:03</span><span class="sxs-lookup"><span data-stu-id="ff48f-375">Tuesday of the work date week 03:03:03</span></span>|
|<span data-ttu-id="ff48f-376">h23 h</span><span class="sxs-lookup"><span data-stu-id="ff48f-376">t23 t</span></span>|<span data-ttu-id="ff48f-377">Dienstag der Woche 23 des Jahres des Arbeitsdatums, aktuelle Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="ff48f-377">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="ff48f-378">H23</span><span class="sxs-lookup"><span data-stu-id="ff48f-378">t23</span></span>|<span data-ttu-id="ff48f-379">Dienstag von Woche 23 des Arbeitsjahres</span><span class="sxs-lookup"><span data-stu-id="ff48f-379">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="ff48f-380">h 23</span><span class="sxs-lookup"><span data-stu-id="ff48f-380">t 23</span></span>|<span data-ttu-id="ff48f-381">Heute 23:00:00</span><span class="sxs-lookup"><span data-stu-id="ff48f-381">Today 23:00:00</span></span>|
|<span data-ttu-id="ff48f-382">h-1</span><span class="sxs-lookup"><span data-stu-id="ff48f-382">t-1</span></span>|<span data-ttu-id="ff48f-383">Dienstag von Woche 1 des Arbeitsjahres</span><span class="sxs-lookup"><span data-stu-id="ff48f-383">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="ff48f-384">Eingeben von Terminen</span><span class="sxs-lookup"><span data-stu-id="ff48f-384">Entering Duration</span></span>
<span data-ttu-id="ff48f-385">Einige Felder in der Anwendung stellen eine Dauer oder Betrag der verstrichenen Uhrzeit, anstatt einer bestimmten Datums- oder Uhrzeitangabe dar.</span><span class="sxs-lookup"><span data-stu-id="ff48f-385">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="ff48f-386">Sie können Zeitdauern als Zahl gefolgt von der entsprechenden Einheit eingeben.</span><span class="sxs-lookup"><span data-stu-id="ff48f-386">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="ff48f-387">Hier folgen einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="ff48f-387">Here are some examples.</span></span>

|<span data-ttu-id="ff48f-388">**Termine**</span><span class="sxs-lookup"><span data-stu-id="ff48f-388">**Duration**</span></span>|<span data-ttu-id="ff48f-389">**Einheit**</span><span class="sxs-lookup"><span data-stu-id="ff48f-389">**Unit of measure**</span></span>|
|------------|-------------------|
|<span data-ttu-id="ff48f-390">2h</span><span class="sxs-lookup"><span data-stu-id="ff48f-390">2h</span></span>|<span data-ttu-id="ff48f-391">2 Stunden</span><span class="sxs-lookup"><span data-stu-id="ff48f-391">2 hrs</span></span>|
|<span data-ttu-id="ff48f-392">6h 30m</span><span class="sxs-lookup"><span data-stu-id="ff48f-392">6h 30 m</span></span>|<span data-ttu-id="ff48f-393">6 Stunden 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="ff48f-393">6 hrs 30 mins</span></span>|
|<span data-ttu-id="ff48f-394">6,5h</span><span class="sxs-lookup"><span data-stu-id="ff48f-394">6.5h</span></span>|<span data-ttu-id="ff48f-395">6 Stunden 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="ff48f-395">6 hrs 30 mins</span></span>|
|<span data-ttu-id="ff48f-396">90m</span><span class="sxs-lookup"><span data-stu-id="ff48f-396">90m</span></span>|<span data-ttu-id="ff48f-397">1 Stunde 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="ff48f-397">1 hr 30 mins</span></span>|
|<span data-ttu-id="ff48f-398">2d 6h 30m</span><span class="sxs-lookup"><span data-stu-id="ff48f-398">2d 6h 30m</span></span>|<span data-ttu-id="ff48f-399">2 Tage 6 Stunden 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="ff48f-399">2 days 6 hrs 30 mins</span></span>|
|<span data-ttu-id="ff48f-400">2d 6h 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="ff48f-400">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="ff48f-401">2 Tage 6 Stunden 30 Minuten 56 Sekunden 600 Millisekunden</span><span class="sxs-lookup"><span data-stu-id="ff48f-401">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="ff48f-402">Sie haben auch die Möglichkeit, eine Zahl einzugeben, die automatisch in einen Zeitraum umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="ff48f-402">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="ff48f-403">Die Zahl, welche Sie eingeben, wird entsprechend der Vorgabeeinheit, die Sie für das Dauer-Feld definiert haben, konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ff48f-403">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="ff48f-404">Geben Sie zum Ermitteln der Einheit, die für ein Feld vom Typ "Dauer" verwendet wird, eine Zahl ein. Am Ergebnis können Sie ablesen, in welche Einheit diese konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="ff48f-404">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="ff48f-405">Wenn die Masseinheit beispielsweise Stunden ist, wird die Zahl 5 in 5 Std. konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ff48f-405">For example, if the unit of measure is hours, the number 5 is converted to 5 hrs.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff48f-406">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff48f-406">See Also</span></span>
<span data-ttu-id="ff48f-407">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ff48f-407">[Working with [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ff48f-408">Terminberechnung für Einkäufe</span><span class="sxs-lookup"><span data-stu-id="ff48f-408">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="ff48f-409">Eingeben von Kriterien in Filtern</span><span class="sxs-lookup"><span data-stu-id="ff48f-409">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
