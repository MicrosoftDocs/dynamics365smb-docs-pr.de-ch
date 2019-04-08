---
title: 'Gewusst wie: Verarbeiten eines LSV-Einzugs'
description: Mithilfe von LSV-Journalen können Zahlungen von LSV+-Debitoren (Lastschriftverfahren) erstellt und verarbeitet werden. Sie können diese Zahlungen im Zahlungseingangs-Erfassungsjournal erfassen, eine LSV-Datei erstellen und dann den Einzugsauftrag drucken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 9a05a80e5a49fb7c0e65f98cbad55a5a46ec7767
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "827230"
---
# <a name="process-an-lsv-collection"></a><span data-ttu-id="534b7-104">Verarbeiten eines LSV-Einzugs</span><span class="sxs-lookup"><span data-stu-id="534b7-104">Process an LSV Collection</span></span>
<span data-ttu-id="534b7-105">Mithilfe der **LSV-Erf.-Journal**-Seite können Zahlungen von LSV+-Debitoren (Lastschriftverfahren) erstellt und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="534b7-105">You can use the **LSV Journal** page to create and process payments from Lastschrift Verfahren (LSV+) customers.</span></span> <span data-ttu-id="534b7-106">Sie können diese Zahlungen im Zahlungseingangs-Erfassungsjournal erfassen, eine LSV-Datei erstellen und dann den Einzugsauftrag drucken.</span><span class="sxs-lookup"><span data-stu-id="534b7-106">You can register these payments in the cash receipt journal, create an LSV file, and then print the collection order.</span></span> <span data-ttu-id="534b7-107">Weitere Informationen finden Sie unter Zahlungseingangs Erf.-Journal (Seite) und [Exportieren von Zahlungen mit LSV](how-to-export-payments-using-lsv.md).</span><span class="sxs-lookup"><span data-stu-id="534b7-107">For more information, see the Cash Receipt Journal page and [Export Payments Using LSV](how-to-export-payments-using-lsv.md).</span></span>  

<span data-ttu-id="534b7-108">Wenn Sie den Stapelverarbeitungsauftrag **LSV Einzugsvorschlag** ausführen, wird jeder vorgeschlagene Einzug in einer LSV-Journalzeile erfasst, und die offenen Rechnungen werden in die LSV-Journale übertragen.</span><span class="sxs-lookup"><span data-stu-id="534b7-108">When you run the **LSV Suggest Collection** batch job, each suggested collection is registered on an LSV journal line, and the open invoices are transferred to the LSV journals.</span></span> <span data-ttu-id="534b7-109">Weitere Informationen finden Sie unter LSV-Erf.-Journal – Tabelle.</span><span class="sxs-lookup"><span data-stu-id="534b7-109">For more information, see the LSV Journal table.</span></span>  

<span data-ttu-id="534b7-110">Sie können die vorgeschlagenen Zahlungszeilen anzeigen, bearbeiten oder löschen.</span><span class="sxs-lookup"><span data-stu-id="534b7-110">You can view, edit, or delete the suggested payment lines.</span></span> <span data-ttu-id="534b7-111">Falls Sie den vorgeschlagenen Betrag korrigieren, wird die Differenz als Rabatt markiert.</span><span class="sxs-lookup"><span data-stu-id="534b7-111">If you correct the suggested amount, then the difference is marked as a discount.</span></span> <span data-ttu-id="534b7-112">Der Stapelverarbeitungsauftrag kann mehrmals für unterschiedliche Debitorengruppen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="534b7-112">You can run the batch job multiple times for different customer groups.</span></span> <span data-ttu-id="534b7-113">Die Vorschlagszeilen können in dasselbe Erfassungsjournal eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="534b7-113">The suggestion lines can be placed in the same journal.</span></span>  

## <a name="to-create-an-lsv-collection"></a><span data-ttu-id="534b7-114">So erstellen Sie einen LSV-Einzug</span><span class="sxs-lookup"><span data-stu-id="534b7-114">To create an LSV collection</span></span>  

1.  <span data-ttu-id="534b7-115">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite ober Bericht suchen") und geben **LSV Erf.-Journal Liste** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="534b7-115">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **LSV Journal List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="534b7-116">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="534b7-116">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="534b7-117">Füllen Sie auf der Seite **LSV-Journal Liste** die erforderlichen Felder wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="534b7-117">On the **LSV Journal List** page, fill in the required fields as described in the following table.</span></span>  

    |<span data-ttu-id="534b7-118">Feld</span><span class="sxs-lookup"><span data-stu-id="534b7-118">Field</span></span>|<span data-ttu-id="534b7-119">Description</span><span class="sxs-lookup"><span data-stu-id="534b7-119">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="534b7-120">**LSV Bankcode**</span><span class="sxs-lookup"><span data-stu-id="534b7-120">**LSV Bank Code**</span></span>|<span data-ttu-id="534b7-121">Wählen Sie den LSV Bankcode für die Bank, die die Konsolidierung durchführt.</span><span class="sxs-lookup"><span data-stu-id="534b7-121">Select the LSV bank code for the bank that will perform the collection.</span></span>|  
    |<span data-ttu-id="534b7-122">**LSV Journalbeschreibung**</span><span class="sxs-lookup"><span data-stu-id="534b7-122">**LSV Journal Description**</span></span>|<span data-ttu-id="534b7-123">Geben Sie eine Beschreibung für den Eintrag ein.</span><span class="sxs-lookup"><span data-stu-id="534b7-123">Enter a description for the entry.</span></span>|

4.  <span data-ttu-id="534b7-124">Wählen Sie den erforderlichen LSV-Journaleintrag, und wählen die Aktion **LSV Sammlung vorschlagen** aus, um die Zahlungen automatisch von LSV zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="534b7-124">Select the required LSV journal entry, and then choose the **LSV Suggest Collection** action to create the payments to be collected automatically by LSV+.</span></span>  
5.  <span data-ttu-id="534b7-125">Füllen Sie auf der Seite **LSV Einzugsvorschlag** die Felder auf dem Inforegister **Optionen** wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="534b7-125">On the **LSV Suggest Collection** page, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="534b7-126">Feld</span><span class="sxs-lookup"><span data-stu-id="534b7-126">Field</span></span>|<span data-ttu-id="534b7-127">Description</span><span class="sxs-lookup"><span data-stu-id="534b7-127">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="534b7-128">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="534b7-128">**No.**</span></span>|<span data-ttu-id="534b7-129">Geben Sie die LSV Erf.-Journalzeilen ein.</span><span class="sxs-lookup"><span data-stu-id="534b7-129">Enter the LSV journal number.</span></span>|  
    |<span data-ttu-id="534b7-130">**Von Fälligkeitsdatum**</span><span class="sxs-lookup"><span data-stu-id="534b7-130">**From due date**</span></span>|<span data-ttu-id="534b7-131">Geben Sie das Start- Fälligkeitsdatum von offenen Posten an, die für die Sammlung vorgeschlagen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="534b7-131">Specify the starting due date of open entries to be suggested for collection.</span></span>|  
    |<span data-ttu-id="534b7-132">**Bis Fälligkeitsdatum**</span><span class="sxs-lookup"><span data-stu-id="534b7-132">**To due date**</span></span>|<span data-ttu-id="534b7-133">Geben Sie das End- Fälligkeitsdatum von offenen Posten an, die für die Sammlung vorgeschlagen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="534b7-133">Specify the ending due date of open entries to be suggested for collection.</span></span>|  
    |<span data-ttu-id="534b7-134">**Einzugsdatum**</span><span class="sxs-lookup"><span data-stu-id="534b7-134">**Collection date**</span></span>|<span data-ttu-id="534b7-135">Geben Sie das Datum an, an dem die Sammlung schliesst.</span><span class="sxs-lookup"><span data-stu-id="534b7-135">Specify the date on which the collection closes.</span></span> <span data-ttu-id="534b7-136">Der LSV+-Einzugsauftrag muss mindestens drei Banktage vor dem Einzugsdatum gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="534b7-136">The LSV+ order must be submitted at least three banking days before the collection date.</span></span>|  

6.  <span data-ttu-id="534b7-137">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="534b7-137">Choose the **OK** button.</span></span>  

<span data-ttu-id="534b7-138">Alle zugehörigen Zeilen werden in das LSV-Journal übertragen.</span><span class="sxs-lookup"><span data-stu-id="534b7-138">All related lines are transferred to the LSV journal.</span></span> <span data-ttu-id="534b7-139">Nach der Verarbeitung des LSV-Einzugs können Sie die vorgeschlagenen Zahlungen auf der Seite **LSV Journal** anzeigen, überprüfen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="534b7-139">After processing the LSV collection, you can view, check, or edit the suggested payments on the **LSV Journal** page.</span></span> <span data-ttu-id="534b7-140">Weitere Informationen finden Sie unter LSV-Erf.-Journal-Zeilen – Tabelle.</span><span class="sxs-lookup"><span data-stu-id="534b7-140">For more information, see the LSV Journal Line table.</span></span>  

## <a name="to-manage-suggested-payments"></a><span data-ttu-id="534b7-141">So verwalten Sie vorgeschlagene Zahlungen</span><span class="sxs-lookup"><span data-stu-id="534b7-141">To manage suggested payments</span></span>  

1.  <span data-ttu-id="534b7-142">Auf der Seite **LSV-Erf.-Journal-Liste** wählen Sie den erforderlichen Journaleintrag, und wählen die **LSV-Erf.-Journalzeile** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="534b7-142">On the **LSV Journal List** page, select the required journal entry, and then choose the **LSV Journal Line** action.</span></span>  

    <span data-ttu-id="534b7-143">Sie können die vorgeschlagenen Zahlungen auf dieser Seite anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="534b7-143">You can view and modify the suggested payments in this page.</span></span> <span data-ttu-id="534b7-144">Dieser Wert kann bei Bedarf manuell eingegeben oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="534b7-144">You can enter the required payments manually.</span></span> <span data-ttu-id="534b7-145">Für neue Erfassungsjournalzeilen wird das Feld **LSV-Status** auf **Öffnen** festgelegt, um anzugeben, dass die Rechnung unbezahlt ist.</span><span class="sxs-lookup"><span data-stu-id="534b7-145">For new journal lines, the **LSV Status** field is set to **Open** to indicate that the invoice is unpaid.</span></span>  

3.  <span data-ttu-id="534b7-146">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="534b7-146">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="534b7-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="534b7-147">See Also</span></span>  
 <span data-ttu-id="534b7-148">[Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="534b7-148">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 <span data-ttu-id="534b7-149">[Schliessen eines LSV-Einzugs](how-to-close-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="534b7-149">[Close an LSV Collection](how-to-close-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="534b7-150">[Buchen von LSV+ Zahlungen](how-to-post-lsv-payments.md) </span><span class="sxs-lookup"><span data-stu-id="534b7-150">[Post LSV+ Payments](how-to-post-lsv-payments.md) </span></span>  
 [<span data-ttu-id="534b7-151">Exportieren von Zahlungen mit LSV</span><span class="sxs-lookup"><span data-stu-id="534b7-151">Export Payments Using LSV</span></span>](how-to-export-payments-using-lsv.md)
