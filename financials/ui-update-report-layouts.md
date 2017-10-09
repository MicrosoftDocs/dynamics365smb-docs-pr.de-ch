---
title: Ein Berichtslayout aktuell behalten | Microsoft Docs
description: "Gelegentlich müssen Sie möglicherweise ein benutzerdefiniertes Berichtslayout aktualisieren, das in einem Bericht verwendet wird. Dies ist obligatorisch, wenn es eine Entwurfsänderung an dem Datensatz des Berichts gegeben hat, wenn zum Beispiel ein Feld, das im Layout verwendet wird, aus dem Berichtsdatensatz entfernt wurde."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c94729c84470267421207a6edaa413116718f715
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="updating-report-or-document-layouts"></a><span data-ttu-id="855fb-104">Verwaltung von Berichts- und Beleg-Layouts</span><span class="sxs-lookup"><span data-stu-id="855fb-104">Updating Report or Document Layouts</span></span>
<span data-ttu-id="855fb-105">Gelegentlich müssen Sie möglicherweise ein benutzerdefiniertes Berichtslayout aktualisieren, das in einem Bericht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="855fb-105">Occasionally, you may need to update a custom report layout that is used on a report.</span></span> <span data-ttu-id="855fb-106">Dies ist obligatorisch, wenn es eine Entwurfsänderung an dem Datensatz des Berichts gegeben hat, wenn zum Beispiel ein Feld, das im Layout verwendet wird, aus dem Berichtsdatensatz entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="855fb-106">This is required when there has been a design change to the report's data set, for example, a field that is used in the layout has been removed from the report data set.</span></span> <span data-ttu-id="855fb-107">Wenn ein Berichtlayout eine Aktualisierung benötigt, erhalten Sie eine Fehlermeldung, wenn Sie versuchen, die Berichtvorschau anzeigen, zu drucken oder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="855fb-107">If a report layout requires updating, you will get an error message when you try to preview, print or save the report.</span></span>  
  
<span data-ttu-id="855fb-108">Um Berichtlayout aus der Fehlermeldung automatisch zu aktualisieren, die angezeigt wird, wenn Sie diesen Bericht ausführen, wählen Sie die Schaltfläche **Ja** auf der Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="855fb-108">You can automatically update a report layout from the error message that appears when you run the report by choosing the **Yes** button on the error message.</span></span> <span data-ttu-id="855fb-109">Oder im Voraus, wenn Sie Berichte ausführen, können Sie bestimmte Berichtslayouts oder alle benutzerdefinierten Berichtslayouts aktualisieren, auf die sich Datasetänderungen auswirken können.</span><span class="sxs-lookup"><span data-stu-id="855fb-109">Or, in advance of running reports, you can update specific report layouts or all custom report layouts that might be affected by dataset changes.</span></span>  
  
<span data-ttu-id="855fb-110">Sie haben auch die Option, Aktualisierungen zu testen, ohne die erforderlichen Änderungen für die benutzerdefinierten Berichtslayouts zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="855fb-110">You also have the option to test updates without applying the required changes to the custom report layouts.</span></span> <span data-ttu-id="855fb-111">Dies ermöglicht Ihnen, festzustellen, welche Änderungen für das Berichtslayout übernommen werden, und mögliche Probleme im Verfahren zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="855fb-111">This enables you to see what changes will be applied to the report layout and identify possible issues in the process.</span></span> <span data-ttu-id="855fb-112">Aus den Testergebnissen können Sie die benutzerdefinierten Berichtslayouts direkt zur Bearbeitung öffnen, um Probleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="855fb-112">From the test results, you can open the custom report layouts directly for editing to fix any issues.</span></span> <span data-ttu-id="855fb-113">Es ist empfehlenswert, dass Sie das Berichtslayoutupdate testen, bevor Sie die Updates übernehmen.</span><span class="sxs-lookup"><span data-stu-id="855fb-113">We recommend that you test the report layout update before you apply the updates.</span></span>  
  
<span data-ttu-id="855fb-114">Nicht alle Berichtsdatasetänderungen können automatisch aktualisiert werden in den Berichtslayouts.</span><span class="sxs-lookup"><span data-stu-id="855fb-114">Not all report dataset changes can be automatically updated in the report layouts.</span></span> <span data-ttu-id="855fb-115">Einige Änderungen erfordern, dass Sie das Berichtslayout manuell bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="855fb-115">Some changes will require that you manually edit the report layout.</span></span> <span data-ttu-id="855fb-116">Weitere Informationen finden Sie unter [Einschränkungen des Updates des benutzerdefinierten Berichtslayouts](ui-update-report-layouts.md#UpdateLimitations).</span><span class="sxs-lookup"><span data-stu-id="855fb-116">For more information, see [Limitations of the Custom Report Layout Update](ui-update-report-layouts.md#UpdateLimitations).</span></span>  
  
## <a name="to-update-one-or-more-custom-report-layouts"></a><span data-ttu-id="855fb-117">Um eine oder mehrere benutzerdefinierten Berichtslayouts zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="855fb-117">To update one or more custom report layouts</span></span>  
  
1.  <span data-ttu-id="855fb-118">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Berichtslayout** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="855fb-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Layouts**, and then choose the related link.</span></span>  
  
2.  <span data-ttu-id="855fb-119">Im **Berichtslayouts** Fenster wenn Sie einen bestimmten Bericht aktualisieren möchten, wählen Sie das Layout aus der Liste, und wählen die **Layout aktualisieren** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="855fb-119">In the **Report Layouts** window, if you want to update a specific report, select the layout from the list, and then choose the **Update Layout** action.</span></span> <span data-ttu-id="855fb-120">Oder, wenn alle benutzerdefinierten Berichtslayouts des Unternehmens aktualisieren möchten, wählen Sie die Aktion **Alle Layouts aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="855fb-120">Or, if you want to update all custom report layouts for the company, choose the **Update All Layouts** action.</span></span>  

<span data-ttu-id="855fb-121">Wenn keine Fehler auftreten, wird die Aktualisierung für die Berichtslayouts übernommen.</span><span class="sxs-lookup"><span data-stu-id="855fb-121">If no errors occur, then the updates is applied to the report layouts.</span></span> <span data-ttu-id="855fb-122">Wenn Fehler auftreten, dann erscheint eine Meldung, die die Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="855fb-122">If errors occur, then a message that contains the errors appears.</span></span> <span data-ttu-id="855fb-123">Sie müssen dann manuell das benutzerdefinierte Berichtslayout bearbeiten, um den Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="855fb-123">You will then have to manually edit the custom report layout to fix the error.</span></span> <span data-ttu-id="855fb-124">Weitere Informationen finden Sie unter [Beheben von Fehlern](ui-update-report-layouts.md#FixErrors).</span><span class="sxs-lookup"><span data-stu-id="855fb-124">For more information, see [Fixing Errors](ui-update-report-layouts.md#FixErrors).</span></span>  

## <a name="to-test-custom-report-layout-updates"></a><span data-ttu-id="855fb-125">Updates zu benutzerdefinierten Berichtslayouts testen</span><span class="sxs-lookup"><span data-stu-id="855fb-125">To test custom report layout updates</span></span>  
  
1.  <span data-ttu-id="855fb-126">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Berichtauswahl** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="855fb-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
  
2.  <span data-ttu-id="855fb-127">Im Fenster **Auswahl des Berichtslayouts** wählen Sie die **Testlayout-Aktualisierungen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="855fb-127">In the **Report Layout Selection** window, choose the **Test Layout Updates** action.</span></span>  
  
 <span data-ttu-id="855fb-128">Änderungen der Berichtslayouts werden getestet, jedoch nicht angewendet mit den tatsächlich Berichtslayouts.</span><span class="sxs-lookup"><span data-stu-id="855fb-128">Chnages to the report layouts are tested but not applied to the actual report layouts.</span></span> <span data-ttu-id="855fb-129">Ein **Aktualisierungsprotokoll Berichtlayout**-Fenster wird angezeigt, das den Status potenzieller Aktualisierungen für jedes Berichtslayout bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="855fb-129">A **Report Layout Update Log** window appears that provides the status a potential updates for each report layout.</span></span> <span data-ttu-id="855fb-130">Gibt es Fehler für ein Berichtslayout, können Sie auf das Berichtslayout zwecks Bearbeitung direkt aus der Meldung zugreifen, um sämtliche Probleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="855fb-130">If there are errors for a report layout, you can access the report layout directly for editing from the message to fix any issues.</span></span> <span data-ttu-id="855fb-131">Weitere Informationen finden Sie unter [Beheben von Fehlern](ui-update-report-layouts.md#FixErrors).</span><span class="sxs-lookup"><span data-stu-id="855fb-131">For more information, see [Fixing Errors](ui-update-report-layouts.md#FixErrors).</span></span>  
  
##  <span data-ttu-id="855fb-132"><a name="UpdateLimitations"></a> Einschränkungen des Updates des benutzerdefinierten Berichtslayouts</span><span class="sxs-lookup"><span data-stu-id="855fb-132"><a name="UpdateLimitations"></a> Limitations of the Custom Report Layout Update</span></span>  
 <span data-ttu-id="855fb-133">Es gibt verschiedene Arten von Änderungen, die die automatische Aktualisieren für benutzerdefinierte Berichtslayouts übernehmen kann, zum Beispiel ein Feld, das im Layout verwendet wird, das aus dem Berichtsdataset entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="855fb-133">There are several types of changes that the automatic update can apply to custom report layouts, for example, a field that is used in the layout has been removed from the report data set.</span></span> <span data-ttu-id="855fb-134">Jedoch kann das automatische Aktualisieren die folgenden Änderungen an einem Berichtsdataset nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="855fb-134">However, the automatic update cannot handle the following changes to a report dataset.</span></span>  
  
1.  <span data-ttu-id="855fb-135">Gelöschte Felder, Beschriftungen oder Datenelemente.</span><span class="sxs-lookup"><span data-stu-id="855fb-135">Deleted fields, labels, or data items.</span></span>  
  
2.  <span data-ttu-id="855fb-136">Kopieren von Feldnamen im Berichtslayout, nachdem ein Feld im Dataset umbenannt wurde.</span><span class="sxs-lookup"><span data-stu-id="855fb-136">Duplicate field names in the report layout after a field has been renamed in the dataset.</span></span> <span data-ttu-id="855fb-137">Dieses sollte als Designfehler behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="855fb-137">This should be treated as a design error.</span></span>  
  
3.  <span data-ttu-id="855fb-138">Aktualisieren von Szenarien, in denen es noch mehrere Iterationen eines Berichtslayouts gibt, das mehrere Umbenennungsaktionen bei denselben Feldern, Beschriftungen oder Datenelementen verursacht.</span><span class="sxs-lookup"><span data-stu-id="855fb-138">Upgrade scenarios where there are multiple iterations of a report layout that causes multiple rename actions on the same fields, labels or data items.</span></span>  
  
 <span data-ttu-id="855fb-139">Wenn der Aktualisierungsvorgang eines dieser Probleme erkennt, kann die Aktualisierung nicht angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="855fb-139">If the update process detects any one of these issues, the update cannot be applied.</span></span> <span data-ttu-id="855fb-140">Sie müssen die Probleme manuell korrigieren, indem Sie beispielsweise das Berichtslayout in Word bearbeiten, oder programmgesteuert, indem Sie Upgrade-Codeunits verwenden.</span><span class="sxs-lookup"><span data-stu-id="855fb-140">You will have to fix the issues manually, for example by editing the report layout in Word, or programmatically by using upgrade codeunits.</span></span>  
  
##  <span data-ttu-id="855fb-141"><a name="FixErrors"></a> Beheben von Fehlern</span><span class="sxs-lookup"><span data-stu-id="855fb-141"><a name="FixErrors"></a> Fixing Errors</span></span>  
 <span data-ttu-id="855fb-142">Wenn Sie eine Fehlermeldung bei der Aktualisierung oder dem Testen von Berichtslayoutupdates erhalten, dann müssen Sie wahrscheinlich das Berichtlayout ändern, um das Problem zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="855fb-142">If you get an error message when you update or test report layout updates, you most likely will have to modify the report layout to fix the problem.</span></span> <span data-ttu-id="855fb-143">Lesen sie die Fehlermeldung, um den Grund des Problems zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="855fb-143">Read the error message to help determine the cause of the problem.</span></span>  
  
 <span data-ttu-id="855fb-144">Das häufigste Problem ist, wenn ein Feld, das im Layout verwendet wird, dem Berichtsdataset entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="855fb-144">The most typical problem occurs when a field that is used on the layout has been removed from the report dataset.</span></span> <span data-ttu-id="855fb-145">In diesem Fall sehen Sie eine Zeile in der Fehlermeldung, die angibt, dass ein Artikel entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="855fb-145">In this case, you will see a line in the error message that states that an item has been removed.</span></span> <span data-ttu-id="855fb-146">Um dieses Problem zu beheben, müssen Sie das Layout bearbeiten und das betreffende Feld entfernen.</span><span class="sxs-lookup"><span data-stu-id="855fb-146">To fix this issue, you will have to modify the layout and remove the field in question.</span></span>  
  
 <span data-ttu-id="855fb-147">Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen und bearbeiten  eines benutzerdefinierten Berichts- oder Dokumentenlayout](ui-how-create-custom-report-layout.md#ModifyCustomLayout).</span><span class="sxs-lookup"><span data-stu-id="855fb-147">For more information, see [How to: Create and Modify a Custom Report Layout](ui-how-create-custom-report-layout.md#ModifyCustomLayout).</span></span>  
  
 <span data-ttu-id="855fb-148">Nachdem Sie das Layout ändern, versuchen Sie, das Layout erneut zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="855fb-148">After you modify the layout, try to update the layout again.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="855fb-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="855fb-149">See Also</span></span>  
 [<span data-ttu-id="855fb-150">Verwalten von Berichtslayouts</span><span class="sxs-lookup"><span data-stu-id="855fb-150">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
 [<span data-ttu-id="855fb-151">Arbeiten mit Berichten</span><span class="sxs-lookup"><span data-stu-id="855fb-151">Working with Reports</span></span>](ui-work-report.md)  