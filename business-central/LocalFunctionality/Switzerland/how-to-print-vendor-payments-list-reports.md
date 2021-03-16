---
title: Drucken des Berichts "Kreditorenzahlungen - Liste"
description: Der Bericht Kreditorenzahlungen - Liste zeigt eine Liste von Zahlungen für jeden Kreditor an. Der Bericht kann Zahlungen chronologisch oder nach Kreditor gruppiert sortieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 10daa127d9de217aa36fd3222ee52735447ff8f3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382025"
---
# <a name="print-vendor-payments-list-reports"></a><span data-ttu-id="74518-104">Gewusst wie: Druck von Listenberichten für Kreditorenzahlungen</span><span class="sxs-lookup"><span data-stu-id="74518-104">Print Vendor Payments List Reports</span></span>

<span data-ttu-id="74518-105">Die Liste **Kreditorenzahlungen** zeigt eine Liste von Zahlungen für jeden Kreditor an.</span><span class="sxs-lookup"><span data-stu-id="74518-105">The **Vendor Payments List** report provides a list of payments for each vendor.</span></span> <span data-ttu-id="74518-106">Der Bericht kann Zahlungen chronologisch oder nach Kreditor gruppiert sortieren.</span><span class="sxs-lookup"><span data-stu-id="74518-106">The report can sort payments chronologically or grouped by vendor.</span></span>  

> [!NOTE]
> <span data-ttu-id="74518-107">Der Bericht **Liste für Kreditorenzahlungen** ist auf den folgenden Märkten verfügbar: Österreich, Deutschland, Schweiz.</span><span class="sxs-lookup"><span data-stu-id="74518-107">The **Vendor Payments List** report is available in the following markets: Austria, Germany, Switzerland.</span></span>

## <a name="to-print-the-vendor-payments-list-report"></a><span data-ttu-id="74518-108">So drucken Sie den Bericht "Kreditorenzahlungen - Liste"</span><span class="sxs-lookup"><span data-stu-id="74518-108">To print the vendor payments list report</span></span>  

1. <span data-ttu-id="74518-109">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Tell me-Funktion") aus, geben Sie **Kreditorenzahlungsliste** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="74518-109">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Payments List**, and then choose the related link.</span></span>  
2. <span data-ttu-id="74518-110">Füllen Sie auf dem Inforegister **Optionen** die Felder wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="74518-110">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="74518-111">Feld</span><span class="sxs-lookup"><span data-stu-id="74518-111">Field</span></span>|<span data-ttu-id="74518-112">Description</span><span class="sxs-lookup"><span data-stu-id="74518-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="74518-113">**Sortieren**</span><span class="sxs-lookup"><span data-stu-id="74518-113">**Sorting**</span></span>|<span data-ttu-id="74518-114">Gibt die Sortierreihenfolge an.</span><span class="sxs-lookup"><span data-stu-id="74518-114">Specifies the sort order.</span></span> <span data-ttu-id="74518-115">Sie können nach Kreditor oder chronologisch sortieren.</span><span class="sxs-lookup"><span data-stu-id="74518-115">You can sort by vendor or chronologically.</span></span> <span data-ttu-id="74518-116">Falls Sie nach Kreditor sortieren, sehen Sie eine Zwischensumme für jeden Kreditor.</span><span class="sxs-lookup"><span data-stu-id="74518-116">If you sort by vendor, you will see a subtotal for each vendor.</span></span> <span data-ttu-id="74518-117">Falls Sie chronologisch sortieren, sehen Sie keine Zwischensummen.</span><span class="sxs-lookup"><span data-stu-id="74518-117">If you sort chronologically, you will not see subtotals.</span></span>|  
    |<span data-ttu-id="74518-118">**Layout**</span><span class="sxs-lookup"><span data-stu-id="74518-118">**Layout**</span></span>|<span data-ttu-id="74518-119">Legt das Berichtslayout fest.</span><span class="sxs-lookup"><span data-stu-id="74518-119">Specifies the layout of the report.</span></span><br /><br /> <span data-ttu-id="74518-120">Die Ergebnisse können in den folgenden Layouts angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="74518-120">The results can be displayed in the following layouts:</span></span><br /><br /> <span data-ttu-id="74518-121">**Standard**</span><span class="sxs-lookup"><span data-stu-id="74518-121">**Standard**</span></span><br /> <span data-ttu-id="74518-122">Zeigt Kreditorennummer und -name sowie die Buchungsdetails an, wie etwa Belegnummer und den Betrag in der lokalen Währung.</span><span class="sxs-lookup"><span data-stu-id="74518-122">Displays the vendor number and vendor name, together with posting details, such as the document number and the amount in local currency.</span></span><br /><br /> <span data-ttu-id="74518-123">**FCY-Beträge**</span><span class="sxs-lookup"><span data-stu-id="74518-123">**FCY Amounts**</span></span><br /> <span data-ttu-id="74518-124">Zeigt Kreditorennummer, -name, Belegnummer, Zahlungsstatus (O für offen, T für Teilzahlung und G für Gesamtzahlung) und Zahlungsbetrag an.</span><span class="sxs-lookup"><span data-stu-id="74518-124">Displays the vendor number, vendor name, document number, payment status (O for open, PP for partial payment, and C for closed), and payment amount.</span></span><br /><br /> <span data-ttu-id="74518-125">**Buchungsdaten**</span><span class="sxs-lookup"><span data-stu-id="74518-125">**Posting Info**</span></span><br /> <span data-ttu-id="74518-126">Zeigt Kreditorennummer, -name, Kostenstelle, Kostenträger, Benutzer-ID und Zahlungsbetrag an.</span><span class="sxs-lookup"><span data-stu-id="74518-126">Displays the vendor number, vendor name, cost center, cost object, user ID, and payment amount.</span></span>|  

 <span data-ttu-id="74518-127">Am Ende des Berichts wird die Anzahl der verarbeiteten Zahlungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="74518-127">At the end of the report, the number of processed payments is displayed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="74518-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74518-128">See Also</span></span>

[<span data-ttu-id="74518-129">Zahlungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="74518-129">Making Payments</span></span>](../../payables-make-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]