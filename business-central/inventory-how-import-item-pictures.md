---
title: Importieren vieler Artikelbilder über eine ZIP-Datei | Microsoft Docs
description: Sie können mehrere Artikelbilder in einem Durchgang importieren. Benennen Sie einfach Ihre Bilddateien mit Namen entsprechend zu Ihren Artikelnummern, komprimieren Sie sie in einer ZIP-Datei und verwenden Sie dann die Seite „Artikelbilder importieren”, um zu verwalten, welche Artikel importiert werden sollen.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fa859d3e350cedb845df47521ee58ba8d2e4aade
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "940615"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="54458-104">Mehrere Artikelbilder importieren</span><span class="sxs-lookup"><span data-stu-id="54458-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="54458-105">Sie können mehrere Artikelbilder in einem Durchgang importieren.</span><span class="sxs-lookup"><span data-stu-id="54458-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="54458-106">Benennen Sie einfach Ihre Bilddateien mit Namen entsprechend zu Ihren Artikelnummern, komprimieren Sie sie in einer ZIP-Datei und verwenden Sie dann die Seite **Artikelbilder importieren**, um zu verwalten, welche Artikel importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="54458-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="54458-107">Alle gängigen Dateiformate werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="54458-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="54458-108">So benennen Sie Bilddateien anhand des Artikelnamens und bereiten die ZIP-Datei vor:</span><span class="sxs-lookup"><span data-stu-id="54458-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="54458-109">Gehen Sie zu dem Ort, an dem Ihre Artikelbilder gespeichert sind, und benennen Sie die einzelnen Dateien entsprechend der Nummer des zugehörigen Artikels.</span><span class="sxs-lookup"><span data-stu-id="54458-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="54458-110">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="54458-110">For example:</span></span>

    |<span data-ttu-id="54458-111">Artikelnr.</span><span class="sxs-lookup"><span data-stu-id="54458-111">Item No.</span></span>|<span data-ttu-id="54458-112">Dateiname</span><span class="sxs-lookup"><span data-stu-id="54458-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="54458-113">1000</span><span class="sxs-lookup"><span data-stu-id="54458-113">1000</span></span>|<span data-ttu-id="54458-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="54458-114">1000.bmp</span></span>|
    |<span data-ttu-id="54458-115">1001</span><span class="sxs-lookup"><span data-stu-id="54458-115">1001</span></span>|<span data-ttu-id="54458-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="54458-116">1001.bmp</span></span>|
    |<span data-ttu-id="54458-117">1002</span><span class="sxs-lookup"><span data-stu-id="54458-117">1002</span></span>|<span data-ttu-id="54458-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="54458-118">1002.bmp</span></span>|

2. <span data-ttu-id="54458-119">Sammeln Sie alle Dateien in einer ZIP-Datei.</span><span class="sxs-lookup"><span data-stu-id="54458-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="54458-120">Wählen Sie zum Beispiel in Windows Explorer die Dateien und dann **Senden an**, **Komprimierter (gezippter) Ordner** aus.</span><span class="sxs-lookup"><span data-stu-id="54458-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="54458-121">So importieren Sie Artikelbilder</span><span class="sxs-lookup"><span data-stu-id="54458-121">To import item pictures</span></span>
1. <span data-ttu-id="54458-122">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagereinrichtung** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="54458-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="54458-123">Wählen Sie die Aktion **Artikelbilder importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="54458-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="54458-124">Wählen Sie im Feld **ZIP-Datei auswählen** den relevanten ZIP-Ordner und dann die Schaltfläche **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="54458-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="54458-125">Eine Zeile für jeden Artikel und jedes Bild wurde auf der Seite **Artikelbilder importieren** erstellt.</span><span class="sxs-lookup"><span data-stu-id="54458-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="54458-126">Für Artikelkarten, die bereits ein Bild haben, wird das Kontrollkästchen **Bild bereits vorhanden** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="54458-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="54458-127">Wenn keine vorhandenen Bilder ersetzt werden sollen, entfernen Sie das Häkchen aus dem Kontrollkästchen **Bilder ersetzen**.</span><span class="sxs-lookup"><span data-stu-id="54458-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="54458-128">Wenn einzelne vorhandene Bilder nicht ersetzt werden sollen, löschen Sie die entsprechenden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="54458-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="54458-129">Wählen Sie die Aktion **Bilder importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="54458-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="54458-130">Das Feld **Importstatus** wird aktualisiert, um anzuzeigen, ob der Bildimport übersprungen oder abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="54458-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="54458-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54458-131">See Also</span></span>
[<span data-ttu-id="54458-132">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="54458-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="54458-133">Erstellen von Nummernkreisen</span><span class="sxs-lookup"><span data-stu-id="54458-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="54458-134">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="54458-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="54458-135">Einkauf</span><span class="sxs-lookup"><span data-stu-id="54458-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="54458-136">Verkauf</span><span class="sxs-lookup"><span data-stu-id="54458-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="54458-137">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="54458-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
