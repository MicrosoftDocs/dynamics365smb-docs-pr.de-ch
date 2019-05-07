---
title: 'Gewusst wie: Drucken von ESR.-Rechnungen'
description: Sie können einen Einzahlungsschein mit Referenznummer (ESR) auf mehrere Arten drucken.
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
ms.openlocfilehash: 7897b15140e8ee3dbe63ab4707c8bfbc89008e2b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "932002"
---
# <a name="print-esr-invoices"></a><span data-ttu-id="54162-103">Drucken von ESR-Rechnungen</span><span class="sxs-lookup"><span data-stu-id="54162-103">Print ESR Invoices</span></span>
<span data-ttu-id="54162-104">Zum Drucken von Einzahlungsscheinen mit Referenznummer (ESR) stehen folgende Methoden zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="54162-104">You can print an Einzahlungsschein mit Referenznummer (ESR) payment slip in the following ways:</span></span>  

- <span data-ttu-id="54162-105">Als Teil der Verkaufsrechnung ESR.</span><span class="sxs-lookup"><span data-stu-id="54162-105">As part of the sales invoice ESR.</span></span>  
- <span data-ttu-id="54162-106">Als separaten Beleg, dem ESR-Coupon.</span><span class="sxs-lookup"><span data-stu-id="54162-106">As a separate document called an ESR coupon.</span></span>  

<span data-ttu-id="54162-107">Der Bericht "Verkauf ESR Rechnung" entspricht der Verkaufsrechnung mit beigefügtem zusätzlichem ESR-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="54162-107">The sales invoice ESR report corresponds with the sales invoice that is accompanied by an additional ESR coupon.</span></span> <span data-ttu-id="54162-108">Indem Sie den Verkauf ESR-Couponsbericht verwenden, können Sie den blauen Einzahlungsbeleg drucken.</span><span class="sxs-lookup"><span data-stu-id="54162-108">By using the sales ESR coupon report, you can print the blue deposit slip.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="54162-109">Sie müssen bei der Installation des ESR-Zahlungsmoduls einen Drucker und Einstellungen auswählen, damit der Einzahlungsbeleg korrekt gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="54162-109">You must select a printer and select settings during the ESR payment module installation to print the deposit slip correctly.</span></span> <span data-ttu-id="54162-110">Weitere Informationen finden Sie unter Druckerauswahl – Tabelle.</span><span class="sxs-lookup"><span data-stu-id="54162-110">For more information, see the Printer Selection table.</span></span>  

<span data-ttu-id="54162-111">Im folgenden Verfahren wird das Drucken von ESR-Verkaufsrechnungen beschrieben, dieselben Schritte gelten jedoch auch für ESR-Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="54162-111">The following procedure describes how to print ESR sales invoices, but the same steps also apply for printing ESR coupons.</span></span>  

## <a name="to-print-esr-invoices"></a><span data-ttu-id="54162-112">So drucken Sie ESR-Rechnungen</span><span class="sxs-lookup"><span data-stu-id="54162-112">To print ESR invoices</span></span>  

1.  <span data-ttu-id="54162-113">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **ESR-Rechnung** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="54162-113">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoice ESR**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="54162-114">Füllen Sie im Stapelverarbeitungsauftrag **Verkauf ESR Rechnung** die Felder auf dem Inforegister **Optionen** wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="54162-114">In the **Sales Invoice ESR** batch job, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="54162-115">Feld</span><span class="sxs-lookup"><span data-stu-id="54162-115">Field</span></span>|<span data-ttu-id="54162-116">Description</span><span class="sxs-lookup"><span data-stu-id="54162-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="54162-117">**Anzahl Kopien**</span><span class="sxs-lookup"><span data-stu-id="54162-117">**No. of copies**</span></span>|<span data-ttu-id="54162-118">Geben Sie die gewünschte Anzahl der Berichtskopien ein.</span><span class="sxs-lookup"><span data-stu-id="54162-118">Enter the required number of report copies.</span></span>|  
    |<span data-ttu-id="54162-119">**ESR-Bank**</span><span class="sxs-lookup"><span data-stu-id="54162-119">**ESR Bank**</span></span>|<span data-ttu-id="54162-120">Wählen Sie die ESR-Bankleitzahl aus, die in dem Bericht gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="54162-120">Select the ESR bank code that is to be printed in the report.</span></span><br /><br /> <span data-ttu-id="54162-121">Wenn der Wert in diesem Feld <Blank> und der ESR-Zahlungsformcode nicht auf der Seite **ESR-Einrichtung** definiert ist, wird die ESR-Hauptbank, die auf der Seite **ESR-Einrichtung** ausgewählt wird, gedruckt.</span><span class="sxs-lookup"><span data-stu-id="54162-121">If the value in this field is <Blank> and the ESR payment method code is not defined on the **ESR Setup** page, then the ESR main bank selected on the **ESR Setup** page will be printed.</span></span>|  
    |<span data-ttu-id="54162-122">**Aktivität protokollieren**</span><span class="sxs-lookup"><span data-stu-id="54162-122">**LogInteraction**</span></span>|<span data-ttu-id="54162-123">Gibt an, ob die Aktivitäten, die Sie mit Ihren Kontakten haben, protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="54162-123">Specify if the interactions that you have with your contacts will be logged.</span></span>|  
    |<span data-ttu-id="54162-124">**ESR-System**</span><span class="sxs-lookup"><span data-stu-id="54162-124">**ESR System**</span></span>|<span data-ttu-id="54162-125">Wählen Sie das ESR-System aus, über das Sie neue ESR-Coupons an Kunden schicken können.</span><span class="sxs-lookup"><span data-stu-id="54162-125">Select the ESR system through which you can send new ESR coupons to customers.</span></span> <span data-ttu-id="54162-126">Wählen Sie **Gemäss ESR-Bank**, um das ESR-System der im Feld **ESR-Bank** angegebenen Bank zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="54162-126">To use the ESR system that is used by the bank that you have specified in **ESR Bank** field, select **Based on ESR Bank**.</span></span>|  

3.  <span data-ttu-id="54162-127">Wählen Sie die Schaltfläche **Drucken** aus, um den Bericht zu drucken, oder die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="54162-127">Choose the **Print** button to print the report or choose the **Preview** button to view it on the screen.</span></span>  

<span data-ttu-id="54162-128">Sie können den Bericht "Verkauf ESR Rechnung" oder "Verkauf ESR Abschnitt" auch erneut drucken.</span><span class="sxs-lookup"><span data-stu-id="54162-128">You can also reprint the sales invoice ESR report or sales ESR coupon report.</span></span>  

## <a name="see-also"></a><span data-ttu-id="54162-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54162-129">See Also</span></span>  
 <span data-ttu-id="54162-130">[Elektronische Zahlungen mit ESR (Schweiz)](swiss-electronic-payments-using-esr.md) </span><span class="sxs-lookup"><span data-stu-id="54162-130">[Swiss Electronic Payments Using ESR](swiss-electronic-payments-using-esr.md) </span></span>  
 [<span data-ttu-id="54162-131">Importieren von ESR-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="54162-131">Import ESR Payments</span></span>](how-to-import-esr-payments.md)
