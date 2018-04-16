---
title: Drucken des Berichts "Kreditorenzahlungen - Liste"
description: "Der Bericht **Kreditorenzahlungen - Liste** zeigt eine Liste von Zahlungen für jeden Kreditor an. Der Bericht kann Zahlungen chronologisch oder nach Kreditor gruppiert sortieren."
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
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: 9e3022a6b5c03dbf85d8c3877c195c01b6701c2c
ms.contentlocale: de-ch
ms.lasthandoff: 04/16/2018

---
# <a name="print-vendor-payments-list-reports"></a><span data-ttu-id="8c544-104">Gewusst wie: Druck von Listenberichten für Kreditorenzahlungen</span><span class="sxs-lookup"><span data-stu-id="8c544-104">Print Vendor Payments List Reports</span></span>
<span data-ttu-id="8c544-105">Die Liste **Kreditorenzahlungen** zeigt eine Liste von Zahlungen für jeden Kreditor an.</span><span class="sxs-lookup"><span data-stu-id="8c544-105">The **Vendor Payments List** report provides a list of payments for each vendor.</span></span> <span data-ttu-id="8c544-106">Der Bericht kann Zahlungen chronologisch oder nach Kreditor gruppiert sortieren.</span><span class="sxs-lookup"><span data-stu-id="8c544-106">The report can sort payments chronologically or grouped by vendor.</span></span>  

## <a name="to-print-the-vendor-payments-list-report"></a><span data-ttu-id="8c544-107">So drucken Sie den Bericht "Kreditorenzahlungen - Liste"</span><span class="sxs-lookup"><span data-stu-id="8c544-107">To print the vendor payments list report</span></span>  

1. <span data-ttu-id="8c544-108">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen"), öffnen Sie **Kreditorenzahlungen - Liste**, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8c544-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Payments List**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8c544-109">Füllen Sie auf dem Inforegister **Optionen** die Felder wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="8c544-109">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

   |<span data-ttu-id="8c544-110">Feld</span><span class="sxs-lookup"><span data-stu-id="8c544-110">Field</span></span>|<span data-ttu-id="8c544-111">Description</span><span class="sxs-lookup"><span data-stu-id="8c544-111">Description</span></span>|  
   |---------------------------------|---------------------------------------|  
   |<span data-ttu-id="8c544-112">**Sortieren**</span><span class="sxs-lookup"><span data-stu-id="8c544-112">**Sorting**</span></span>|<span data-ttu-id="8c544-113">Gibt die Sortierreihenfolge an.</span><span class="sxs-lookup"><span data-stu-id="8c544-113">Specifies the sort order.</span></span> <span data-ttu-id="8c544-114">Sie können nach Kreditor oder chronologisch sortieren.</span><span class="sxs-lookup"><span data-stu-id="8c544-114">You can sort by vendor or chronologically.</span></span> <span data-ttu-id="8c544-115">Falls Sie nach Kreditor sortieren, sehen Sie eine Zwischensumme für jeden Kreditor.</span><span class="sxs-lookup"><span data-stu-id="8c544-115">If you sort by vendor, you will see a subtotal for each vendor.</span></span> <span data-ttu-id="8c544-116">Falls Sie chronologisch sortieren, sehen Sie keine Zwischensummen.</span><span class="sxs-lookup"><span data-stu-id="8c544-116">If you sort chronologically, you will not see subtotals.</span></span>|  
   |<span data-ttu-id="8c544-117">**Layout**</span><span class="sxs-lookup"><span data-stu-id="8c544-117">**Layout**</span></span>|<span data-ttu-id="8c544-118">Legt das Berichtslayout fest.</span><span class="sxs-lookup"><span data-stu-id="8c544-118">Specifies the layout of the report.</span></span><br /><br /> <span data-ttu-id="8c544-119">Die Ergebnisse können in den folgenden Layouts angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="8c544-119">The results can be displayed in the following layouts:</span></span><br /><br /> <span data-ttu-id="8c544-120">**Standard**</span><span class="sxs-lookup"><span data-stu-id="8c544-120">**Standard**</span></span><br /> <span data-ttu-id="8c544-121">Zeigt Kreditorennummer und -name sowie die Buchungsdetails an, wie etwa Belegnummer und den Betrag in der lokalen Währung.</span><span class="sxs-lookup"><span data-stu-id="8c544-121">Displays the vendor number and vendor name, together with posting details, such as the document number and the amount in local currency.</span></span><br /><br /> <span data-ttu-id="8c544-122">**FCY-Beträge**</span><span class="sxs-lookup"><span data-stu-id="8c544-122">**FCY Amounts**</span></span><br /> <span data-ttu-id="8c544-123">Zeigt Kreditorennummer, -name, Belegnummer, Zahlungsstatus (O für offen, T für Teilzahlung und G für Gesamtzahlung) und Zahlungsbetrag an.</span><span class="sxs-lookup"><span data-stu-id="8c544-123">Displays the vendor number, vendor name, document number, payment status (O for open, PP for partial payment, and C for closed), and payment amount.</span></span><br /><br /> <span data-ttu-id="8c544-124">**Buchungsdaten**</span><span class="sxs-lookup"><span data-stu-id="8c544-124">**Posting Info**</span></span><br /> <span data-ttu-id="8c544-125">Zeigt Kreditorennummer, -name, Kostenstelle, Kostenträger, Benutzer-ID und Zahlungsbetrag an.</span><span class="sxs-lookup"><span data-stu-id="8c544-125">Displays the vendor number, vendor name, cost center, cost object, user ID, and payment amount.</span></span>|  

   <span data-ttu-id="8c544-126">Am Ende des Berichts wird die Anzahl der verarbeiteten Zahlungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c544-126">At the end of the report, the number of processed payments is displayed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8c544-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c544-127">See Also</span></span>  
[<span data-ttu-id="8c544-128">Zahlungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="8c544-128">Making Payments</span></span>](../../payables-make-payments.md)

