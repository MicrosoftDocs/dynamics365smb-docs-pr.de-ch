---
title: 'Gewusst wie: Importieren von Schweizer Postleitzahlen'
description: "Sie können die aktuelle PLZ importieren und damit die Tabelle **PLZ** aktualisieren. Die PLZ-Datei kann von der Website der Schweizer Post heruntergeladen werden. Nach dem Import der letzten PLZ können PLZ für Debitoren oder Kreditoren definiert werden."
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
ms.openlocfilehash: e053a7a32e091b34fbc0e2f06cea9ce4c79f19d4
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="import-swiss-post-codes"></a><span data-ttu-id="79d19-105">Importieren von Postleitzahlen (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="79d19-105">Import Swiss Post Codes</span></span>
<span data-ttu-id="79d19-106">Sie können die aktuelle PLZ importieren und damit die Tabelle **PLZ** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="79d19-106">You can import the latest post code file and use it to update the **Post Code** table.</span></span> <span data-ttu-id="79d19-107">Die PLZ-Datei kann von der Website der [Schweizer Post](http://go.microsoft.com/fwlink/?LinkId=150292) heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="79d19-107">The post code file can be downloaded from the [Swiss Post](http://go.microsoft.com/fwlink/?LinkId=150292) website.</span></span> <span data-ttu-id="79d19-108">Nach dem Import der letzten PLZ können PLZ für Debitoren oder Kreditoren definiert werden.</span><span class="sxs-lookup"><span data-stu-id="79d19-108">After importing the latest post code, you can define post codes for customers or vendors.</span></span> <span data-ttu-id="79d19-109">Weitere Informationen finden Sie unter [Neue Kunden registrieren](../../purchasing-how-register-new-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="79d19-109">For more information, see [Register New Vendors](../../purchasing-how-register-new-vendors.md).</span></span>  

## <a name="to-import-post-codes"></a><span data-ttu-id="79d19-110">So importieren Sie PLZ</span><span class="sxs-lookup"><span data-stu-id="79d19-110">To import post codes</span></span>  

1.  <span data-ttu-id="79d19-111">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Postleitzahlen-Codes** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="79d19-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Post Codes**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="79d19-112">Wählen Sie die Aktion**PLZ importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="79d19-112">Choose the **Import Post Codes** action.</span></span>  
3.  <span data-ttu-id="79d19-113">Geben Sie im Fenster **Postleitzahlen Import** im Feld **Dateiname** den Namen der PLZ-Datei ein, die Sie in die Tabelle **PLZ** importieren möchten.</span><span class="sxs-lookup"><span data-stu-id="79d19-113">In the **Import Post Codes** window, in the **Filename** field, enter the name of the post code file that you want to import to the **Post Code** table.</span></span>  
4.  <span data-ttu-id="79d19-114">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="79d19-114">Choose the **OK** button.</span></span>  

    <span data-ttu-id="79d19-115">Die aktuellen PLZ-Informationen werden importiert.</span><span class="sxs-lookup"><span data-stu-id="79d19-115">The latest post code information is imported.</span></span>  

<span data-ttu-id="79d19-116">Nachfolgend wird beschrieben, wie PLZ für Debitoren definiert werden, doch bei der Definition von PLZ für Kreditoren wird die gleiche Gewusst wie verwendet.</span><span class="sxs-lookup"><span data-stu-id="79d19-116">The following procedure describes how to define post codes for customers, but the same steps also apply to defining post codes for vendors.</span></span>  

## <a name="to-define-post-codes-for-customers"></a><span data-ttu-id="79d19-117">So definieren Sie PLZ für Debitoren</span><span class="sxs-lookup"><span data-stu-id="79d19-117">To define post codes for customers</span></span>  

1.  <span data-ttu-id="79d19-118">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kunden** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="79d19-118">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="79d19-119">Wählen Sie den Debitor, für den Sie eine PLZ definieren möchten, und wählen die **Bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="79d19-119">Select the customer for whom you want to define a post code, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="79d19-120">Im Fenster **Debitorenkarte** im Inforegister **Allgemein**, im Feld **PLZ**, wählen Sie die PLZ für die Adresse des Debitors aus.</span><span class="sxs-lookup"><span data-stu-id="79d19-120">In the **Customer Card** window, on the **General** FastTab, in the **Post Code** field, select the post code for the customer's address.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="79d19-121">Bei Auswahl der PLZ werden die Felder **Ort** und **Länder-/Regionscode** automatisch mit den Informationen aus der Tabelle **PLZ** ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="79d19-121">When you select the post code, the **City** and **Country/Region Code** fields populate automatically with the information from the **Post Code** table.</span></span> <span data-ttu-id="79d19-122">Weitere Informationen finden Sie unter [Neue Kunden registrieren](../../sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="79d19-122">For more information, see [Register New Customers](../../sales-how-register-new-customers.md).</span></span>  

4.  <span data-ttu-id="79d19-123">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="79d19-123">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="79d19-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79d19-124">See Also</span></span>   
 <span data-ttu-id="79d19-125">[Einkaufsbelege und Verkaufsbelege (Schweiz)](swiss-purchase-documents-and-sales-documents.md) </span><span class="sxs-lookup"><span data-stu-id="79d19-125">[Swiss Purchase Documents and Sales Documents](swiss-purchase-documents-and-sales-documents.md) </span></span>  
 <span data-ttu-id="79d19-126">[Drucken einer Lagerkommissionierliste von einem Auftrag](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span><span class="sxs-lookup"><span data-stu-id="79d19-126">[Print an Inventory Picking List from a Sales Order](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span></span>  
 <span data-ttu-id="79d19-127">[So drucken Sie im Verlauf von Stapelbuchungen Verkaufsaufträge und Bestellungen](how-to-print-sales-and-purchase-orders-during-batch-posting.md) </span><span class="sxs-lookup"><span data-stu-id="79d19-127">[Print Sales and Purchase Orders During Batch Posting](how-to-print-sales-and-purchase-orders-during-batch-posting.md) </span></span>  
 [<span data-ttu-id="79d19-128">Registriert einen neuen Kreditor</span><span class="sxs-lookup"><span data-stu-id="79d19-128">Register New Vendors</span></span>](../../purchasing-how-register-new-vendors.md)  

