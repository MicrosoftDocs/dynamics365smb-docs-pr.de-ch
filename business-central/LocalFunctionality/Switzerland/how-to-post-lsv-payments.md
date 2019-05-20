---
title: Buchen von LSV+-Zahlungen
description: Zahlungen können nach Empfang einer LSV+ (Lastschrift Verfahren)-Zahlungsanzeige von der Bank gebucht werden.
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
ms.openlocfilehash: f8dc03d4b11a14f442901ed40375467e9b8bf210
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241318"
---
# <a name="post-lsv-payments"></a><span data-ttu-id="cb63b-103">Buchen von LSV+-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="cb63b-103">Post LSV+ Payments</span></span>
<span data-ttu-id="cb63b-104">Zahlungen können nach Empfang einer LSV+ (Lastschrift Verfahren)-Zahlungsanzeige von der Bank gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="cb63b-104">You can post payments after you have received Lastschrift Verfahren (LSV+) payment advice from the bank.</span></span>  

## <a name="to-post-lsv-payments"></a><span data-ttu-id="cb63b-105">So buchen Sie LSV+-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="cb63b-105">To post LSV+ payments</span></span>  

1.  <span data-ttu-id="cb63b-106">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Barbeleg-Buchblatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="cb63b-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cash Receipt Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cb63b-107">Wählen Sie das entsprechende Journal aus und wählen Sie dass **Journal bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="cb63b-107">Select the required journal, and then choose the **Edit Journal** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="cb63b-108">Sie können den Erf.-Journalnamen für LSV auswählen, wo das betreffende Gegenkonto definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cb63b-108">You can select the journal batch for LSV where the balance account you want to address is defined.</span></span> <span data-ttu-id="cb63b-109">Es kann jeweils nur eine LSV-Journalzeile in ein Zahlungseingangs Erf.-Journal importiert werden.</span><span class="sxs-lookup"><span data-stu-id="cb63b-109">You cannot import more than one LSV journal line into the same cash receipt journal.</span></span> <span data-ttu-id="cb63b-110">Weitere Informationen finden Sie unter Zahlungseingangs Erf.-Journal (Seite).</span><span class="sxs-lookup"><span data-stu-id="cb63b-110">For more information, see the Cash Receipt Journal page.</span></span>  

3.  <span data-ttu-id="cb63b-111">Wählen Sie die Aktion **von LSV-Erf.-Journal abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="cb63b-111">Choose the **Get From LSV Journal** action.</span></span>  
4.  <span data-ttu-id="cb63b-112">Wählen Sie auf der Seite **LSV-Journal Liste** die LSV-Journalzeile aus, die Sie in das Zahlungseingangs Erf.-Journal importieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cb63b-112">On the **LSV Journal List** page, select the LSV journal line that you want to import to the cash receipt journal.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="cb63b-113">Es können nur Erf.-Journalzeilen importiert werden, in denen das Feld **LSV-Status** auf **Datei erstellt** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cb63b-113">You can only import journal lines where the **LSV Status** field is set to **File Created**.</span></span>  

5.  <span data-ttu-id="cb63b-114">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="cb63b-114">Choose the **OK** button.</span></span>  

    <span data-ttu-id="cb63b-115">Die LSV-Journalzeile wird in das Zahlungseingangs Erf.-Journal importiert.</span><span class="sxs-lookup"><span data-stu-id="cb63b-115">The LSV journal line is imported into the cash receipt journal.</span></span> <span data-ttu-id="cb63b-116">Der Wert im Feld **LSV-Status** auf der Seite **LSV-Journal Liste** ändert sich von **Datei erstellt** in **Beendet**.</span><span class="sxs-lookup"><span data-stu-id="cb63b-116">The value in the **LSV Status** field on the **LSV Journal List** page changes from **File Created** to **Finished**.</span></span>  

    <span data-ttu-id="cb63b-117">Sie können die importierten Zahlungen überprüfen und sie mit der Bankzahlungsanzeige auf der Seite **Zahlungseingangs Erf.-Journal** vergleichen.</span><span class="sxs-lookup"><span data-stu-id="cb63b-117">You can check the imported payments, and compare them with your bank payment advice on the **Cash Receipt Journal** page.</span></span> <span data-ttu-id="cb63b-118">Sie können auch die Zahlungszeilen löschen, die von der Bank nicht verarbeitet werden konnten und für die Sie sich manuell mit dem Debitor in Verbindung setzen müssen.</span><span class="sxs-lookup"><span data-stu-id="cb63b-118">You can also delete the payment lines that could not be processed by the bank, and for which you must follow up with the customer manually.</span></span>  

6.  <span data-ttu-id="cb63b-119">Wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="cb63b-119">Choose the **Post** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cb63b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb63b-120">See Also</span></span>  
 <span data-ttu-id="cb63b-121">[Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="cb63b-121">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 <span data-ttu-id="cb63b-122">[Verarbeiten eines LSV-Einzugs](how-to-process-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="cb63b-122">[Process an LSV Collection](how-to-process-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="cb63b-123">[Schliessen eines LSV-Einzugs](how-to-close-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="cb63b-123">[Close an LSV Collection](how-to-close-an-lsv-collection.md) </span></span>  
 [<span data-ttu-id="cb63b-124">Exportieren von Zahlungen mit LSV</span><span class="sxs-lookup"><span data-stu-id="cb63b-124">Export Payments Using LSV</span></span>](how-to-export-payments-using-lsv.md) 
