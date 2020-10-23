---
title: Exportieren von Zahlungen mit LSV
description: Nachdem der LSV-Einzug abgeschlossen wurde, können Sie LSV+-Dateien (Lastschriftverfahren) mit Zahlungsinformationen exportieren oder erstellen. Sie können die generierten Dateien auf einem Datenträger an die Bank senden oder eine elektronische Methode der Dateiübertragung wie die Onlinebankingsoftware oder ein Internetportal verwenden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0f1999dba518999a4715f2a2aebddb7bcb2347ba
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916411"
---
# <a name="export-payments-using-lsv"></a><span data-ttu-id="2c44c-104">Exportieren von Zahlungen mit LSV</span><span class="sxs-lookup"><span data-stu-id="2c44c-104">Export Payments Using LSV</span></span>
<span data-ttu-id="2c44c-105">Nachdem der LSV-Einzug abgeschlossen wurde, können Sie LSV+-Dateien (Lastschriftverfahren) mit Zahlungsinformationen exportieren oder erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c44c-105">You can export or write Lastschrift Verfahren (LSV+) files that contain payments information after closing the LSV collection.</span></span> <span data-ttu-id="2c44c-106">Sie können die generierten Dateien auf einem Datenträger an die Bank senden oder eine elektronische Methode der Dateiübertragung wie die Onlinebankingsoftware oder ein Internetportal verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c44c-106">You can send the generated files to the bank on a disk, or use an electronic file transfer such as your online banking software or an Internet portal.</span></span>  

## <a name="to-export-payments-using-lsv"></a><span data-ttu-id="2c44c-107">So exportieren Sie Zahlungen mit LSV</span><span class="sxs-lookup"><span data-stu-id="2c44c-107">To export payments using LSV</span></span>  

1.  <span data-ttu-id="2c44c-108">Wählen Sie das Symbol ![Glühbirne , das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Tell me-Funktion") aus, geben Sie **LSV-Erfassungsjournalliste** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="2c44c-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **LSV Journal List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2c44c-109">Wählen Sie auf der Seite **LSV-Journal Liste** das gewünschte LSV-Journal aus.</span><span class="sxs-lookup"><span data-stu-id="2c44c-109">On the **LSV Journal List** page, select the required LSV journal.</span></span>  
3.  <span data-ttu-id="2c44c-110">Wählen Sie die Aktion **LSV-Datei schreiben** aus.</span><span class="sxs-lookup"><span data-stu-id="2c44c-110">Choose the **Write LSV File** action.</span></span>  
4.  <span data-ttu-id="2c44c-111">Füllen Sie auf der Seite **LSV Datei schreiben** die Felder auf dem Inforegister **Optionen** wie in der folgenden Tabelle beschrieben aus.</span><span class="sxs-lookup"><span data-stu-id="2c44c-111">On the **Write LSV File** page, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="2c44c-112">Feld</span><span class="sxs-lookup"><span data-stu-id="2c44c-112">Field</span></span>|<span data-ttu-id="2c44c-113">Description</span><span class="sxs-lookup"><span data-stu-id="2c44c-113">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="2c44c-114">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="2c44c-114">**No.**</span></span>|<span data-ttu-id="2c44c-115">Geben Sie die Nummer des LSV-Journalsummer an, das Sie exportieren möchten.</span><span class="sxs-lookup"><span data-stu-id="2c44c-115">Specify the LSV journal number that you want to export.</span></span>|  
    |<span data-ttu-id="2c44c-116">**Prüfen**</span><span class="sxs-lookup"><span data-stu-id="2c44c-116">**Test**</span></span>|<span data-ttu-id="2c44c-117">Geben Sie an, ob Sie Testlieferungen an Ihre Bank senden.</span><span class="sxs-lookup"><span data-stu-id="2c44c-117">Specify if you are sending test deliveries to your bank.</span></span> <span data-ttu-id="2c44c-118">Testdateien werden nicht von der Bank verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2c44c-118">The bank does not process test files.</span></span>|  

5.  <span data-ttu-id="2c44c-119">Alle zugehörigen Zeilen werden in das LSV-Journal übertragen.</span><span class="sxs-lookup"><span data-stu-id="2c44c-119">All related lines are transferred to the LSV journal.</span></span> <span data-ttu-id="2c44c-120">Die LSV-Datei wird im angegebenen Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c44c-120">The LSV file is generated in the predetermined folder.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2c44c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c44c-121">See Also</span></span>  
 <span data-ttu-id="2c44c-122">[Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="2c44c-122">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 <span data-ttu-id="2c44c-123">[Verarbeiten eines LSV-Einzugs](how-to-process-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="2c44c-123">[Process an LSV Collection](how-to-process-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="2c44c-124">[Abschliessen eines LSV-Einzugs](how-to-close-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="2c44c-124">[Close an LSV Collection](how-to-close-an-lsv-collection.md) </span></span>  
 [<span data-ttu-id="2c44c-125">Buchen von LSV+-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="2c44c-125">Post LSV+ Payments</span></span>](how-to-post-lsv-payments.md)
