---
title: 'Gewusst wie: Drucken einer Lager-Kommissionierliste aus Verkaufsaufträgen'
description: Eine Lagerkommissionierliste kann direkt von einem Verkaufsauftrag gedruckt werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 4b7cefc82313b1e6967ec3c54759ab77ee0ae7fd
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245647"
---
# <a name="print-an-inventory-picking-list-from-a-sales-order"></a><span data-ttu-id="925d0-103">Drucken einer Lagerkommissionierliste von einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="925d0-103">Print an Inventory Picking List from a Sales Order</span></span>
<span data-ttu-id="925d0-104">Eine Lagerkommissionierliste kann direkt von einem Verkaufsauftrag gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="925d0-104">You can print an inventory picking list directly from a sales order.</span></span> <span data-ttu-id="925d0-105">Die Kommissionierliste enthält eine Liste von Artikeln mit den folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="925d0-105">The picking list contains a list of items with the following information:</span></span>  

- <span data-ttu-id="925d0-106">Lagerplatzcode</span><span class="sxs-lookup"><span data-stu-id="925d0-106">Bin code</span></span>  
- <span data-ttu-id="925d0-107">Lagerortcode</span><span class="sxs-lookup"><span data-stu-id="925d0-107">Location code</span></span>  
- <span data-ttu-id="925d0-108">Seriennummer</span><span class="sxs-lookup"><span data-stu-id="925d0-108">Serial number</span></span>  
- <span data-ttu-id="925d0-109">Menge</span><span class="sxs-lookup"><span data-stu-id="925d0-109">Quantity</span></span>  

<span data-ttu-id="925d0-110">Die Kommissionierliste enthält nur die Artikel, deren Versandmenge grösser als 0 ist.</span><span class="sxs-lookup"><span data-stu-id="925d0-110">The picking list includes only those items with a shipping quantity greater than 0.</span></span>  

## <a name="to-print-an-inventory-picking-list-from-a-sales-order"></a><span data-ttu-id="925d0-111">So drucken Sie eine Lagerkommissionierliste von einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="925d0-111">To print an inventory picking list from a sales order</span></span>  

1.  <span data-ttu-id="925d0-112">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsauftrag** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="925d0-112">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="925d0-113">Wählen Sie den relevanten Verkaufsauftrag aus und wählen Sie dann auf der Registerkarte Start **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="925d0-113">Select the required sales order, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="925d0-114">Wählen Sie die Aktion **Liste auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="925d0-114">Choose the **Picking List** action.</span></span>  
4.  <span data-ttu-id="925d0-115">Geben Sie auf dem Inforegister **Optionen** im Feld **Anzahl Kopien** die erforderliche Anzahl von Kopien ein.</span><span class="sxs-lookup"><span data-stu-id="925d0-115">On the **Options** FastTab, in the **No. of Copies** field, enter the required number of copies.</span></span>  
5.  <span data-ttu-id="925d0-116">Wählen Sie die Schaltfläche **Drucken** aus, um die Auswahlliste zu drucken oder wählen Sie die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="925d0-116">Choose the **Print** button to print the picking list or choose the **Preview** button to view it on the screen.</span></span>  

## <a name="see-also"></a><span data-ttu-id="925d0-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="925d0-117">See Also</span></span>  
 <span data-ttu-id="925d0-118">[Einkaufsbelege und Verkaufsbelege (Schweiz)](swiss-purchase-documents-and-sales-documents.md) </span><span class="sxs-lookup"><span data-stu-id="925d0-118">[Swiss Purchase Documents and Sales Documents](swiss-purchase-documents-and-sales-documents.md) </span></span>  
 <span data-ttu-id="925d0-119">[Importieren von Postleitzahlen (Schweiz)](how-to-import-swiss-post-codes.md) </span><span class="sxs-lookup"><span data-stu-id="925d0-119">[Import Swiss Post Codes](how-to-import-swiss-post-codes.md) </span></span>  
 [<span data-ttu-id="925d0-120">So drucken Sie im Verlauf von Stapelbuchungen Verkaufsaufträge und Bestellungen</span><span class="sxs-lookup"><span data-stu-id="925d0-120">Print Sales and Purchase Orders During Batch Posting</span></span>](how-to-print-sales-and-purchase-orders-during-batch-posting.md)
