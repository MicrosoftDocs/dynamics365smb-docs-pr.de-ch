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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 17b29e5ed357f139b6bbcef96204c78736404762
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676641"
---
# <a name="post-lsv-payments"></a><span data-ttu-id="eb557-103">Buchen von LSV+-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="eb557-103">Post LSV+ Payments</span></span>
<span data-ttu-id="eb557-104">Zahlungen können nach Empfang einer LSV+ (Lastschrift Verfahren)-Zahlungsanzeige von der Bank gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="eb557-104">You can post payments after you have received Lastschrift Verfahren (LSV+) payment advice from the bank.</span></span>  

## <a name="to-post-lsv-payments"></a><span data-ttu-id="eb557-105">So buchen Sie LSV+-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="eb557-105">To post LSV+ payments</span></span>  

1.  <span data-ttu-id="eb557-106">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](../../media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Zlg.-Eing. Erfassungsjournale** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="eb557-106">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cash Receipt Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="eb557-107">Wählen Sie das entsprechende Journal aus und wählen Sie dass **Journal bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="eb557-107">Select the required journal, and then choose the **Edit Journal** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="eb557-108">Sie können den Erf.-Journalnamen für LSV auswählen, wo das betreffende Gegenkonto definiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb557-108">You can select the journal batch for LSV where the balance account you want to address is defined.</span></span> <span data-ttu-id="eb557-109">Es kann jeweils nur eine LSV-Journalzeile in ein Zahlungseingangs Erf.-Journal importiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb557-109">You cannot import more than one LSV journal line into the same cash receipt journal.</span></span> <span data-ttu-id="eb557-110">Weitere Informationen finden Sie unter Zahlungseingangs Erf.-Journal (Seite).</span><span class="sxs-lookup"><span data-stu-id="eb557-110">For more information, see the Cash Receipt Journal page.</span></span>  

3.  <span data-ttu-id="eb557-111">Wählen Sie die Aktion **von LSV-Erf.-Journal abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="eb557-111">Choose the **Get From LSV Journal** action.</span></span>  
4.  <span data-ttu-id="eb557-112">Wählen Sie auf der Seite **LSV-Journal Liste** die LSV-Journalzeile aus, die Sie in das Zahlungseingangs Erf.-Journal importieren möchten.</span><span class="sxs-lookup"><span data-stu-id="eb557-112">On the **LSV Journal List** page, select the LSV journal line that you want to import to the cash receipt journal.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="eb557-113">Es können nur Erf.-Journalzeilen importiert werden, in denen das Feld **LSV-Status** auf **Datei erstellt** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="eb557-113">You can only import journal lines where the **LSV Status** field is set to **File Created**.</span></span>  

5.  <span data-ttu-id="eb557-114">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="eb557-114">Choose the **OK** button.</span></span>  

    <span data-ttu-id="eb557-115">Die LSV-Journalzeile wird in das Zahlungseingangs Erf.-Journal importiert.</span><span class="sxs-lookup"><span data-stu-id="eb557-115">The LSV journal line is imported into the cash receipt journal.</span></span> <span data-ttu-id="eb557-116">Der Wert im Feld **LSV-Status** auf der Seite **LSV-Journal Liste** ändert sich von **Datei erstellt** in **Beendet**.</span><span class="sxs-lookup"><span data-stu-id="eb557-116">The value in the **LSV Status** field on the **LSV Journal List** page changes from **File Created** to **Finished**.</span></span>  

    <span data-ttu-id="eb557-117">Sie können die importierten Zahlungen überprüfen und sie mit der Bankzahlungsanzeige auf der Seite **Zahlungseingangs Erf.-Journal** vergleichen.</span><span class="sxs-lookup"><span data-stu-id="eb557-117">You can check the imported payments, and compare them with your bank payment advice on the **Cash Receipt Journal** page.</span></span> <span data-ttu-id="eb557-118">Sie können auch die Zahlungszeilen löschen, die von der Bank nicht verarbeitet werden konnten und für die Sie sich manuell mit dem Debitor in Verbindung setzen müssen.</span><span class="sxs-lookup"><span data-stu-id="eb557-118">You can also delete the payment lines that could not be processed by the bank, and for which you must follow up with the customer manually.</span></span>  

6.  <span data-ttu-id="eb557-119">Wählen Sie die Aktion **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="eb557-119">Choose the **Post** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eb557-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb557-120">See Also</span></span>  
 <span data-ttu-id="eb557-121">[Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="eb557-121">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 <span data-ttu-id="eb557-122">[Verarbeiten eines LSV-Einzugs](how-to-process-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="eb557-122">[Process an LSV Collection](how-to-process-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="eb557-123">[Abschliessen eines LSV-Einzugs](how-to-close-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="eb557-123">[Close an LSV Collection](how-to-close-an-lsv-collection.md) </span></span>  
 [<span data-ttu-id="eb557-124">Exportieren von Zahlungen mit LSV</span><span class="sxs-lookup"><span data-stu-id="eb557-124">Export Payments Using LSV</span></span>](how-to-export-payments-using-lsv.md) 
