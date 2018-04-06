---
title: Datenbereich in Finance and Operations, Business edition  | Microsoft Docs einrichten
description: "Erhalten von Informationen zum Anzeigen von Daten aus bestimmten Zeiträumen mithilfe von Finance and Operations, Business edition"
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0494a04e67803049df71cfefe779c831c9f31674
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="a932a-103">Datenbereiche eingeben</span><span class="sxs-lookup"><span data-stu-id="a932a-103">Entering Date Ranges</span></span> 
<span data-ttu-id="a932a-104">Sie können Filter mit einem Start- und Enddatum setzen, sodass lediglich die Daten angezeigt werden, die innerhalb eines bestimmten Datumsbereichs oder Zeitintervalls liegen.</span><span class="sxs-lookup"><span data-stu-id="a932a-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="a932a-105">Für das Festlegen von Datumsbereichen gelten besondere Regeln.</span><span class="sxs-lookup"><span data-stu-id="a932a-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="a932a-106">Als Beispiel nehmen wir die **Top 10 Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="a932a-106">Let's take the **Customer Top 10** as an example:</span></span>

![Einen Datumsbereich auf der Anforderungsseite der Top 10 Debitorenliste festlegen](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="a932a-108">Hier können Sie den Bericht auf eine Gültigkeit wie den letzten 2 Wochen oder insgesamt 6 Wochen oder einen beliebigen Bereich einschränken.</span><span class="sxs-lookup"><span data-stu-id="a932a-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="a932a-109">Um eine Gültigkeit festzulegen, geben Sie Daten ein und verwenden anschliessend **..**</span><span class="sxs-lookup"><span data-stu-id="a932a-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="a932a-110">oder **|**, um den Bereich zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a932a-110">or **|** to set the range.</span></span> <span data-ttu-id="a932a-111">Im vorliegenden Beispiel müssen Sie, um die ersten zwei Wochen des Mai für die Top 10 Debitoren anzuzeigen, den Datumsfilter auf *05 01 17..05 14 17* setzen.</span><span class="sxs-lookup"><span data-stu-id="a932a-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="a932a-112">Hier finden Sie einige andere Beispiele:</span><span class="sxs-lookup"><span data-stu-id="a932a-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="a932a-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a932a-113">Meaning</span></span> | <span data-ttu-id="a932a-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a932a-114">Example</span></span> | <span data-ttu-id="a932a-115">Enthaltene Posten</span><span class="sxs-lookup"><span data-stu-id="a932a-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="a932a-116">Ist gleich</span><span class="sxs-lookup"><span data-stu-id="a932a-116">Equal to</span></span>| <span data-ttu-id="a932a-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="a932a-117">12 15 16</span></span> |<span data-ttu-id="a932a-118">Nur jene, die am 15. Deuzember 2016 gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="a932a-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="a932a-119">Intervall</span><span class="sxs-lookup"><span data-stu-id="a932a-119">Interval</span></span>| <span data-ttu-id="a932a-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="a932a-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="a932a-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="a932a-121">..12 15 16</span></span>|<span data-ttu-id="a932a-122">Jene, die zwischen dem 15. Dezember 2016 und dem 15. Januar 2017 (einschliesslich) gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="a932a-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="a932a-123">Jene, die bis zum 15. Dezember 2016 oder früher gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="a932a-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="a932a-124">Entweder/oder</span><span class="sxs-lookup"><span data-stu-id="a932a-124">Either/or</span></span>|<span data-ttu-id="a932a-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="a932a-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="a932a-126">Entweder am 15. Dezember oder am 16. Dezember 2016 gebucht.</span><span class="sxs-lookup"><span data-stu-id="a932a-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="a932a-127">Falls es Posten gibt, die an einem der beiden Tage gebucht wurden, werden diese angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a932a-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="a932a-128">Sie können auch die verschiedenen Formattypen miteinander kombinieren.</span><span class="sxs-lookup"><span data-stu-id="a932a-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="a932a-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a932a-129">Example</span></span> | <span data-ttu-id="a932a-130">Enthaltene Posten</span><span class="sxs-lookup"><span data-stu-id="a932a-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="a932a-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="a932a-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="a932a-132">Posten, die am 15. Dezember 2016 oder zwischen dem 01. Dezember 2016 und 31. Mai 2017 (einschliesslich) gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="a932a-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="a932a-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="a932a-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="a932a-134">Posten, die bis einschliesslich zum 14. Dezember oder am bzw. nach dem 30. Dezember gebucht wurden. Mit diesem Filter können Sie alle Posten ausschliessen, die zwischen den beiden angegebenen Tagen gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="a932a-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="a932a-135">Beachten Sie, dass wir das US-Datumsformat MMDDYY hier verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="a932a-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="a932a-136">[!INCLUDE[d365fin](includes/d365fin_md.md)] wird verfügbar in anderen Märkten, Sie haben die Möglichkeit, die Formaten zu verwenden, die möchten.</span><span class="sxs-lookup"><span data-stu-id="a932a-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="see-also"></a><span data-ttu-id="a932a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a932a-137">See Also</span></span>
<span data-ttu-id="a932a-138">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a932a-138">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a932a-139">Eingeben von Kriterien in Filtern</span><span class="sxs-lookup"><span data-stu-id="a932a-139">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="a932a-140">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="a932a-140">General Business Functionality</span></span>](ui-across-business-areas.md)

