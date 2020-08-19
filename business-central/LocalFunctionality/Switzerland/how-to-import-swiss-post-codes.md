---
title: 'Gewusst wie: Importieren von Schweizer Postleitzahlen'
description: Sie können die aktuelle PLZ importieren und damit die Tabelle PLZ aktualisieren. Die PLZ-Datei kann von der Website der Schweizer Post heruntergeladen werden. Nach dem Import der letzten PLZ können PLZ für Debitoren oder Kreditoren definiert werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 127c28b6cdb683f329494ce202b5ce6e39429295
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677188"
---
# <a name="import-swiss-post-codes"></a><span data-ttu-id="c20ca-105">Importieren von Postleitzahlen (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="c20ca-105">Import Swiss Post Codes</span></span>
<span data-ttu-id="c20ca-106">Sie können die aktuelle PLZ importieren und damit die Tabelle **PLZ** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c20ca-106">You can import the latest post code file and use it to update the **Post Code** table.</span></span> <span data-ttu-id="c20ca-107">Die PLZ-Datei kann von der Website der [Schweizer Post](https://go.microsoft.com/fwlink/?LinkId=150292) heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c20ca-107">The post code file can be downloaded from the [Swiss Post](https://go.microsoft.com/fwlink/?LinkId=150292) website.</span></span> <span data-ttu-id="c20ca-108">Nach dem Import der letzten PLZ können PLZ für Debitoren oder Kreditoren definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c20ca-108">After importing the latest post code, you can define post codes for customers or vendors.</span></span> <span data-ttu-id="c20ca-109">Weitere Informationen finden Sie unter [Neue Kreditoren registrieren](../../purchasing-how-register-new-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="c20ca-109">For more information, see [Register New Vendors](../../purchasing-how-register-new-vendors.md).</span></span>  

## <a name="to-import-post-codes"></a><span data-ttu-id="c20ca-110">So importieren Sie PLZ</span><span class="sxs-lookup"><span data-stu-id="c20ca-110">To import post codes</span></span>  

1.  <span data-ttu-id="c20ca-111">Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Tell me-Funktion") aus, geben Sie **PLZ** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="c20ca-111">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Post Codes**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c20ca-112">Wählen Sie die Aktion**PLZ importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="c20ca-112">Choose the **Import Post Codes** action.</span></span>  
3.  <span data-ttu-id="c20ca-113">Geben Sie auf der Seite **Postleitzahlen Import** im Feld **Dateiname** den Namen der PLZ-Datei ein, die Sie in die Tabelle **PLZ** importieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c20ca-113">On the **Import Post Codes** page, in the **Filename** field, enter the name of the post code file that you want to import to the **Post Code** table.</span></span>  
4.  <span data-ttu-id="c20ca-114">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="c20ca-114">Choose the **OK** button.</span></span>  

    <span data-ttu-id="c20ca-115">Die aktuellen PLZ-Informationen werden importiert.</span><span class="sxs-lookup"><span data-stu-id="c20ca-115">The latest post code information is imported.</span></span>  

<span data-ttu-id="c20ca-116">Nachfolgend wird beschrieben, wie PLZ für Debitoren definiert werden, doch bei der Definition von PLZ für Kreditoren wird die gleiche Gewusst wie verwendet.</span><span class="sxs-lookup"><span data-stu-id="c20ca-116">The following procedure describes how to define post codes for customers, but the same steps also apply to defining post codes for vendors.</span></span>  

## <a name="to-define-post-codes-for-customers"></a><span data-ttu-id="c20ca-117">So definieren Sie PLZ für Debitoren</span><span class="sxs-lookup"><span data-stu-id="c20ca-117">To define post codes for customers</span></span>  

1.  <span data-ttu-id="c20ca-118">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Tell me-Funktion") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="c20ca-118">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c20ca-119">Wählen Sie den Debitor, für den Sie eine PLZ definieren möchten, und wählen die **Bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="c20ca-119">Select the customer for whom you want to define a post code, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="c20ca-120">Wählen Sie auf der Seite **Debitorenkarte** auf dem Inforegister **Allgemein** im Feld **PLZ** die PLZ für die Adresse des Debitors aus.</span><span class="sxs-lookup"><span data-stu-id="c20ca-120">On the **Customer Card** page, on the **General** FastTab, in the **Post Code** field, select the post code for the customer's address.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c20ca-121">Bei Auswahl der PLZ werden die Felder **Ort** und **Länder-/Regionscode** automatisch mit den Informationen aus der Tabelle **PLZ** ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="c20ca-121">When you select the post code, the **City** and **Country/Region Code** fields populate automatically with the information from the **Post Code** table.</span></span> <span data-ttu-id="c20ca-122">Weitere Informationen finden Sie unter [Neue Debitoren registrieren](../../sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="c20ca-122">For more information, see [Register New Customers](../../sales-how-register-new-customers.md).</span></span>  

4.  <span data-ttu-id="c20ca-123">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="c20ca-123">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c20ca-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c20ca-124">See Also</span></span>   
 <span data-ttu-id="c20ca-125">[Einkaufsbelege und Verkaufsbelege (Schweiz)](swiss-purchase-documents-and-sales-documents.md) </span><span class="sxs-lookup"><span data-stu-id="c20ca-125">[Swiss Purchase Documents and Sales Documents](swiss-purchase-documents-and-sales-documents.md) </span></span>  
 <span data-ttu-id="c20ca-126">[Drucken einer Lagerkommissionierliste von einem Auftrag](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span><span class="sxs-lookup"><span data-stu-id="c20ca-126">[Print an Inventory Picking List from a Sales Order](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span></span>  
 [<span data-ttu-id="c20ca-127">Registriert einen neuen Kreditor</span><span class="sxs-lookup"><span data-stu-id="c20ca-127">Register New Vendors</span></span>](../../purchasing-how-register-new-vendors.md)  
