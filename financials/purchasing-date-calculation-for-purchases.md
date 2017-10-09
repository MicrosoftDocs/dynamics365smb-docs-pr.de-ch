---
title: "Terminberechnung für Einkäufe  | Microsoft Docs"
description: "Das Programm berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist. Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7e569474e3d222a56500665fa73408f47480f338
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="5d36b-104">Terminberechnung für Einkäufe</span><span class="sxs-lookup"><span data-stu-id="5d36b-104">Date Calculation for Purchases</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="5d36b-105"> berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5d36b-105"> automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="5d36b-106">Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5d36b-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="5d36b-107">Wenn Sie ein gewünschtes Wareneingangsdatum in einem Einkaufsbestellkopf angeben, ist das berechnete Auftragsdatum das Datum, an dem die Bestellung erfolgen muss, um die Artikel an dem Datum zu erhalten, das Sie angefordert haben.</span><span class="sxs-lookup"><span data-stu-id="5d36b-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="5d36b-108">Dann wird das Datum, an dem die Artikel für die Kommissionierung zur Verfügung stehen, im Feld **Erwartetes Eingangsdatum** berechnet und eingegeben.</span><span class="sxs-lookup"><span data-stu-id="5d36b-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="5d36b-109">Wenn Sie kein gewünschtes Wareneingangsdatum angeben, wird das Bestelldatum in der Zeile als Ausgangspunkt zur Berechnung des Datums verwendet, an dem die Artikel eingehen sollen, und des Datums, an dem die Artikel für die Kommissionierung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="5d36b-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="5d36b-110">Berechnung mit einem gewünschten Wareneingangsdatum</span><span class="sxs-lookup"><span data-stu-id="5d36b-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="5d36b-111">Falls es ein gewünschtes Wareneingangsdatum in der Einkaufsbestellungszeile gibt, wird dieses Datum als Ausgangspunkt für die folgenden Berechnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d36b-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="5d36b-112">Gewünschtes Wareneingangsdatum – Beschaffungszeit = Bestelldatum</span><span class="sxs-lookup"><span data-stu-id="5d36b-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="5d36b-113">Gewünschtes Wareneingangsdatum + Eingeh. Lagerdurchlaufzeit + Beschaffungszeit = Erwartetes Wareneingangsdatum</span><span class="sxs-lookup"><span data-stu-id="5d36b-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="5d36b-114">Wenn Sie ein gewünschtes Wareneingangsdatum im Bestellkopf angegeben haben, wird dieses Datum in das entsprechende Feld in allen Zeilen kopiert.</span><span class="sxs-lookup"><span data-stu-id="5d36b-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="5d36b-115">Sie können dieses Datum in den einzelnen Zeilen ändern oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="5d36b-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="5d36b-116">Berechnung ohne ein gewünschtes Wareneingangsdatum</span><span class="sxs-lookup"><span data-stu-id="5d36b-116">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="5d36b-117">Wenn Sie eine Bestellzeile ohne ein gewünschtes Lieferdatum eingeben, füllt die Anwendung das Feld **Bestelldatum** in der Zeile mit dem **Bestelldatum** im Bestellkopf.</span><span class="sxs-lookup"><span data-stu-id="5d36b-117">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="5d36b-118">Hierbei handelt es sich entweder um das Datum, das Sie eingegeben haben, oder um das Arbeitsdatum.</span><span class="sxs-lookup"><span data-stu-id="5d36b-118">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="5d36b-119">Die folgenden Datumsangaben werden dann in der Einkaufsbestellungszeile berechnet, mit dem Bestelldatum als Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="5d36b-119">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="5d36b-120">Bestelldatum + Beschaffungszeit = Geplantes Wareneingangsdatum</span><span class="sxs-lookup"><span data-stu-id="5d36b-120">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="5d36b-121">Geplantes Wareneingangsdatum + Eingeh. Lagerdurchlaufzeit + Beschaffungszeit = Erwartetes Wareneingangsdatum</span><span class="sxs-lookup"><span data-stu-id="5d36b-121">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="5d36b-122">Falls Sie das Bestelldatum in der Zeile ändern (z. B. weil die Artikel bei dem Kreditor erst zu einem späteren Datum verfügbar sind), werden die entsprechenden Datumsangaben in der Zeile automatisch neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="5d36b-122">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="5d36b-123">Wenn Sie das Bestelldatum im Kopf ändern, wird das Datum in allen Zeilen in das Feld  kopiert, und alle zugehörigen **Datumsfelder** werden neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="5d36b-123">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5d36b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d36b-124">See Also</span></span>  
 <span data-ttu-id="5d36b-125">[Terminberechnung für Verkäufe](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="5d36b-125">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="5d36b-126">So wird's gemacht: Lieferterminzusagen berechnen</span><span class="sxs-lookup"><span data-stu-id="5d36b-126">How to: Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="5d36b-127">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5d36b-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

