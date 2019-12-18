---
title: Terminberechnung für Verkäufe  | Microsoft Docs
description: Die Anwendung berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist. Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6080fd58b299a0bda74c1cdd9ff5758d8805b3a8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881391"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="79ba8-104">Terminberechnung für Verkäufe</span><span class="sxs-lookup"><span data-stu-id="79ba8-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="79ba8-105">berechnet automatisch das frühestmögliche Datum, an dem ein Artikel in einer Verkaufsauftragszeile geliefert werden kann.</span><span class="sxs-lookup"><span data-stu-id="79ba8-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="79ba8-106">Wenn der Debitor ein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel für die Kommissionierung zur Verfügung stehen müssen, damit dieser Liefertermin eingehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="79ba8-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="79ba8-107">Falls der Debitor kein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel geliefert werden können, ausgehend von dem Datum, an dem die Artikel für die Kommissionierung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="79ba8-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="79ba8-108">So berechnen Sie ein gewünschtes Wareneingangsdatum:</span><span class="sxs-lookup"><span data-stu-id="79ba8-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="79ba8-109">Wenn Sie in einer Verkaufszeile ein gewünschtes Lieferdatum eingeben, wird dieses Datum zum Ausgangspunkt für die folgenden Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="79ba8-109">If you specify a requested delivery date on the sales order line, that date becomes the starting point for the following calculations.</span></span>

- <span data-ttu-id="79ba8-110">Gewünschtes Lieferdatum - Transportzeit = Geplantes Warenausgangsdatum</span><span class="sxs-lookup"><span data-stu-id="79ba8-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="79ba8-111">Geplantes Warenausgangsdatum - Ausgeh. Lagerdurchlaufzeit = Warenausgangsdatum</span><span class="sxs-lookup"><span data-stu-id="79ba8-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="79ba8-112">Falls die Artikel am Lieferdatum zur Kommissionierung zur Verfügung stehen, kann der Verkaufsvorgang fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="79ba8-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span> <span data-ttu-id="79ba8-113">Anderenfalls wird eine Warnmeldung wegen fehlenden Bestands angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79ba8-113">Otherwise, a stock-out warning is displayed.</span></span>

> [!Note]
> <span data-ttu-id="79ba8-114">Falls Ihr Prozess auf einer Rückwärtsberechnung basiert, beispielsweise bei Verwendung des gewünschten Lieferdatums zum Ermitteln des geplanten Warenausgangsdatums, empfiehlt sich die Verwendung von Datumsformeln mit fester Dauer, wie etwa „5D“ für fünf Tage oder „1W“ für eine Woche.</span><span class="sxs-lookup"><span data-stu-id="79ba8-114">If your process is based on backward calculation, for example, if you use the requested delivery date to get the planned shipment date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="79ba8-115">Datumsformeln ohne feste Dauer, wie etwa „LW“ für laufende Woche oder „LM“ für laufender Monat können zu fehlerhaften Datumsberechnungen führen.</span><span class="sxs-lookup"><span data-stu-id="79ba8-115">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="79ba8-116">Weitere Informationen über Datumsformeln finden Sie unter [Arbeiten mit Datumsangaben und Uhrzeiten in Kalendern](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="79ba8-116">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="79ba8-117">So berechnen Sie das frühestmögliche Lieferdatum:</span><span class="sxs-lookup"><span data-stu-id="79ba8-117">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="79ba8-118">Wenn Sie kein angefordertes Lieferdatum auf der Verkaufsauftragszeile angeben oder das angeforderte Lieferdatum nicht eingehalten werden kann, wird das früheste Datum, an dem die Artikel verfügbar sind, berechnet.</span><span class="sxs-lookup"><span data-stu-id="79ba8-118">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="79ba8-119">Dieses Datum wird dann im Feld Versanddatum auf der Zeile eingegeben, und das Datum, an dem Sie planen, die Artikel zu liefern, sowie das Datum, an dem Sie an den Kunden ausgeliefert werden, werden anhand der nachfolgenden Formeln berechnet.</span><span class="sxs-lookup"><span data-stu-id="79ba8-119">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="79ba8-120">Warenausgangsdatum + Ausgeh. Lagerdurchlaufzeit = Geplantes Warenausgangsdatum</span><span class="sxs-lookup"><span data-stu-id="79ba8-120">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="79ba8-121">Geplantes Warenausgangsdatum + Transportzeit = Geplantes Lieferdatum</span><span class="sxs-lookup"><span data-stu-id="79ba8-121">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="79ba8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79ba8-122">See Also</span></span>  
 <span data-ttu-id="79ba8-123">[Terminberechnung für Einkäufe](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="79ba8-123">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="79ba8-124">Lieferterminzusagen-Daten berechnen</span><span class="sxs-lookup"><span data-stu-id="79ba8-124">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="79ba8-125">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="79ba8-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
