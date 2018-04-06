---
title: Buchen von LSV+-Zahlungen
description: "Zahlungen können nach Empfang einer LSV+ (Lastschrift Verfahren)-Zahlungsanzeige von der Bank gebucht werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 26fa934e00b380b7416417f2a1d37e7bde4a5098
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="post-lsv-payments"></a><span data-ttu-id="fb3e3-103">Buchen von LSV+-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="fb3e3-103">Post LSV+ Payments</span></span>
<span data-ttu-id="fb3e3-104">Zahlungen können nach Empfang einer LSV+ (Lastschrift Verfahren)-Zahlungsanzeige von der Bank gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-104">You can post payments after you have received Lastschrift Verfahren (LSV+) payment advice from the bank.</span></span>  

## <a name="to-post-lsv-payments"></a><span data-ttu-id="fb3e3-105">So buchen Sie LSV+-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="fb3e3-105">To post LSV+ payments</span></span>  

1.  <span data-ttu-id="fb3e3-106">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Barbeleg-Buchblatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cash Receipt Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fb3e3-107">Wählen Sie das entsprechende Journal aus und wählen Sie dass **Journal bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-107">Select the required journal, and then choose the **Edit Journal** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="fb3e3-108">Sie können den Erf.-Journalnamen für LSV auswählen, wo das betreffende Gegenkonto definiert ist.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-108">You can select the journal batch for LSV where the balance account you want to address is defined.</span></span> <span data-ttu-id="fb3e3-109">Es kann jeweils nur eine LSV-Journalzeile in ein Zahlungseingangs Erf.-Journal importiert werden.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-109">You cannot import more than one LSV journal line into the same cash receipt journal.</span></span> <span data-ttu-id="fb3e3-110">Weitere Informationen finden Sie im Fenster "Zahlungseingangs Erf.-Journal".</span><span class="sxs-lookup"><span data-stu-id="fb3e3-110">For more information, see the Cash Receipt Journal window.</span></span>  

3.  <span data-ttu-id="fb3e3-111">Wählen Sie die Aktion **von LSV-Erf.-Journal abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-111">Choose the **Get From LSV Journal** action.</span></span>  
4.  <span data-ttu-id="fb3e3-112">Wählen Sie im Fenster **LSV-Journal Liste** die LSV-Journalzeile aus, die Sie in das Zahlungseingangs Erf.-Journal importieren möchten.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-112">In the **LSV Journal List** window, select the LSV journal line that you want to import to the cash receipt journal.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="fb3e3-113">Es können nur Erf.-Journalzeilen importiert werden, in denen das Feld **LSV-Status** auf **Datei erstellt** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-113">You can only import journal lines where the **LSV Status** field is set to **File Created**.</span></span>  

5.  <span data-ttu-id="fb3e3-114">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-114">Choose the **OK** button.</span></span>  

    <span data-ttu-id="fb3e3-115">Die LSV-Journalzeile wird in das Zahlungseingangs Erf.-Journal importiert.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-115">The LSV journal line is imported into the cash receipt journal.</span></span> <span data-ttu-id="fb3e3-116">Der Wert im Feld **LSV-Status** im Fenster **LSV-Journal Liste** ändert sich von **Datei erstellt** in **Beendet**.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-116">The value in the **LSV Status** field in the **LSV Journal List** window changes from **File Created** to **Finished**.</span></span>  

    <span data-ttu-id="fb3e3-117">Sie können die importierten Zahlungen überprüfen und sie mit der Bankzahlungsanzeige im Fenster **Zahlungseingangs Erf.-Journal** vergleichen.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-117">You can check the imported payments, and compare them with your bank payment advice in the **Cash Receipt Journal** window.</span></span> <span data-ttu-id="fb3e3-118">Sie können auch die Zahlungszeilen löschen, die von der Bank nicht verarbeitet werden konnten und für die Sie sich manuell mit dem Debitor in Verbindung setzen müssen.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-118">You can also delete the payment lines that could not be processed by the bank, and for which you must follow up with the customer manually.</span></span>  

6.  <span data-ttu-id="fb3e3-119">Wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="fb3e3-119">Choose the **Post** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fb3e3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb3e3-120">See Also</span></span>  
 <span data-ttu-id="fb3e3-121">[Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="fb3e3-121">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 <span data-ttu-id="fb3e3-122">[Verarbeiten eines LSV-Einzugs](how-to-process-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="fb3e3-122">[Process an LSV Collection](how-to-process-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="fb3e3-123">[Schliessen eines LSV-Einzugs](how-to-close-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="fb3e3-123">[Close an LSV Collection](how-to-close-an-lsv-collection.md) </span></span>  
 [<span data-ttu-id="fb3e3-124">Exportieren von Zahlungen mit LSV</span><span class="sxs-lookup"><span data-stu-id="fb3e3-124">Export Payments Using LSV</span></span>](how-to-export-payments-using-lsv.md) 

