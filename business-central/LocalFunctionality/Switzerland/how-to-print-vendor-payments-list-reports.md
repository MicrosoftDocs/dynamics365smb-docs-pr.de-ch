---
title: Drucken des Berichts "Kreditorenzahlungen - Liste"
description: Der Bericht Kreditorenzahlungen - Liste zeigt eine Liste von Zahlungen für jeden Kreditor an. Der Bericht kann Zahlungen chronologisch oder nach Kreditor gruppiert sortieren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e3d8e38ed8dfa9143c0436c366be1f090b18be55
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "930517"
---
# <a name="print-vendor-payments-list-reports"></a><span data-ttu-id="6556b-104">Gewusst wie: Druck von Listenberichten für Kreditorenzahlungen</span><span class="sxs-lookup"><span data-stu-id="6556b-104">Print Vendor Payments List Reports</span></span>
<span data-ttu-id="6556b-105">Die Liste **Kreditorenzahlungen** zeigt eine Liste von Zahlungen für jeden Kreditor an.</span><span class="sxs-lookup"><span data-stu-id="6556b-105">The **Vendor Payments List** report provides a list of payments for each vendor.</span></span> <span data-ttu-id="6556b-106">Der Bericht kann Zahlungen chronologisch oder nach Kreditor gruppiert sortieren.</span><span class="sxs-lookup"><span data-stu-id="6556b-106">The report can sort payments chronologically or grouped by vendor.</span></span>  

## <a name="to-print-the-vendor-payments-list-report"></a><span data-ttu-id="6556b-107">So drucken Sie den Bericht "Kreditorenzahlungen - Liste"</span><span class="sxs-lookup"><span data-stu-id="6556b-107">To print the vendor payments list report</span></span>  

1.  <span data-ttu-id="6556b-108">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen"), öffnen Sie **Kreditorenzahlungen - Liste**, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="6556b-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Payments List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6556b-109">Füllen Sie auf dem Inforegister **Optionen** die Felder wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="6556b-109">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="6556b-110">Feld</span><span class="sxs-lookup"><span data-stu-id="6556b-110">Field</span></span>|<span data-ttu-id="6556b-111">Description</span><span class="sxs-lookup"><span data-stu-id="6556b-111">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="6556b-112">**Sortieren**</span><span class="sxs-lookup"><span data-stu-id="6556b-112">**Sorting**</span></span>|<span data-ttu-id="6556b-113">Gibt die Sortierreihenfolge an.</span><span class="sxs-lookup"><span data-stu-id="6556b-113">Specifies the sort order.</span></span> <span data-ttu-id="6556b-114">Sie können nach Kreditor oder chronologisch sortieren.</span><span class="sxs-lookup"><span data-stu-id="6556b-114">You can sort by vendor or chronologically.</span></span> <span data-ttu-id="6556b-115">Falls Sie nach Kreditor sortieren, sehen Sie eine Zwischensumme für jeden Kreditor.</span><span class="sxs-lookup"><span data-stu-id="6556b-115">If you sort by vendor, you will see a subtotal for each vendor.</span></span> <span data-ttu-id="6556b-116">Falls Sie chronologisch sortieren, sehen Sie keine Zwischensummen.</span><span class="sxs-lookup"><span data-stu-id="6556b-116">If you sort chronologically, you will not see subtotals.</span></span>|  
    |<span data-ttu-id="6556b-117">**Layout**</span><span class="sxs-lookup"><span data-stu-id="6556b-117">**Layout**</span></span>|<span data-ttu-id="6556b-118">Legt das Berichtslayout fest.</span><span class="sxs-lookup"><span data-stu-id="6556b-118">Specifies the layout of the report.</span></span><br /><br /> <span data-ttu-id="6556b-119">Die Ergebnisse können in den folgenden Layouts angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="6556b-119">The results can be displayed in the following layouts:</span></span><br /><br /> <span data-ttu-id="6556b-120">**Standard**</span><span class="sxs-lookup"><span data-stu-id="6556b-120">**Standard**</span></span><br /> <span data-ttu-id="6556b-121">Zeigt Kreditorennummer und -name sowie die Buchungsdetails an, wie etwa Belegnummer und den Betrag in der lokalen Währung.</span><span class="sxs-lookup"><span data-stu-id="6556b-121">Displays the vendor number and vendor name, together with posting details, such as the document number and the amount in local currency.</span></span><br /><br /> <span data-ttu-id="6556b-122">**FCY-Beträge**</span><span class="sxs-lookup"><span data-stu-id="6556b-122">**FCY Amounts**</span></span><br /> <span data-ttu-id="6556b-123">Zeigt Kreditorennummer, -name, Belegnummer, Zahlungsstatus (O für offen, T für Teilzahlung und G für Gesamtzahlung) und Zahlungsbetrag an.</span><span class="sxs-lookup"><span data-stu-id="6556b-123">Displays the vendor number, vendor name, document number, payment status (O for open, PP for partial payment, and C for closed), and payment amount.</span></span><br /><br /> <span data-ttu-id="6556b-124">**Buchungsdaten**</span><span class="sxs-lookup"><span data-stu-id="6556b-124">**Posting Info**</span></span><br /> <span data-ttu-id="6556b-125">Zeigt Kreditorennummer, -name, Kostenstelle, Kostenträger, Benutzer-ID und Zahlungsbetrag an.</span><span class="sxs-lookup"><span data-stu-id="6556b-125">Displays the vendor number, vendor name, cost center, cost object, user ID, and payment amount.</span></span>|  

 <span data-ttu-id="6556b-126">Am Ende des Berichts wird die Anzahl der verarbeiteten Zahlungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6556b-126">At the end of the report, the number of processed payments is displayed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6556b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6556b-127">See Also</span></span>  
[<span data-ttu-id="6556b-128">Zahlungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="6556b-128">Making Payments</span></span>](../../payables-make-payments.md)
