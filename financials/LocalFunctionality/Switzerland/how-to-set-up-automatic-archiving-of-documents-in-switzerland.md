---
title: Einrichten einer automatischen Archivierung von Belegen (Schweiz)
description: "Sie können die automatische Archivierung von Verkaufs- und Einkaufsbelegen einrichten – beispielsweise Angebote, Rahmenbestellungen und Aufträge – bevor Sie Belege löschen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 09fca5cba94bed83b862cd8bb9d4b5be895c509d
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-automatic-archiving-of-documents-in-switzerland"></a><span data-ttu-id="f0b02-103">Einrichten einer automatischen Archivierung von Belegen (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="f0b02-103">Set Up Automatic Archiving of Documents in Switzerland</span></span>
<span data-ttu-id="f0b02-104">Sie können die automatische Archivierung von Verkaufs- und Einkaufsbelegen einrichten – beispielsweise Offerten, Rahmenbestellungen und Aufträge – bevor Sie Belege löschen.</span><span class="sxs-lookup"><span data-stu-id="f0b02-104">You can set up automatic archiving of sales documents and purchase documents—such as quotes, blanket orders, and orders—before you delete documents.</span></span>  

<span data-ttu-id="f0b02-105">Nachfolgend wird beschrieben, wie die automatische Archivierung von Verkaufsbelegen eingerichtet wird. Diese Gewusst wie gilt allerdings auch für Einkaufsbelege.</span><span class="sxs-lookup"><span data-stu-id="f0b02-105">The following procedure describes how to set up automatic archiving of sales documents, but the same steps apply to purchase documents.</span></span>  

## <a name="to-set-up-automatic-archiving-of-documents"></a><span data-ttu-id="f0b02-106">So richten Sie die automatische Archivierung von Belegen ein</span><span class="sxs-lookup"><span data-stu-id="f0b02-106">To set up automatic archiving of documents</span></span>  

1.  <span data-ttu-id="f0b02-107">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Debit&oren && Verkauf Einr.** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f0b02-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f0b02-108">Füllen Sie im Fenster **Debitoren & Verkauf Einr.** im Inforegister **Archivierung** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="f0b02-108">On the **Sales & Receivables Setup** window, on the **Archiving** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f0b02-109">Feld</span><span class="sxs-lookup"><span data-stu-id="f0b02-109">Field</span></span>|<span data-ttu-id="f0b02-110">Description</span><span class="sxs-lookup"><span data-stu-id="f0b02-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f0b02-111">**Offerte archivieren**</span><span class="sxs-lookup"><span data-stu-id="f0b02-111">**Archiving Sales Quote**</span></span>|<span data-ttu-id="f0b02-112">**Nie**, wenn Verkaufsbelege beim Löschen nie archiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0b02-112">**Never** to never archive sales quotes when they are deleted.</span></span><br /><br /> <span data-ttu-id="f0b02-113">–oder–</span><span class="sxs-lookup"><span data-stu-id="f0b02-113">–or–</span></span><br /><br /> <span data-ttu-id="f0b02-114">**Frage**, wenn der Benutzer angeben soll, ob er Verkaufsbelege beim Löschen archivieren möchte.</span><span class="sxs-lookup"><span data-stu-id="f0b02-114">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span><br /><br /> <span data-ttu-id="f0b02-115">–oder–</span><span class="sxs-lookup"><span data-stu-id="f0b02-115">–or–</span></span><br /><br /> <span data-ttu-id="f0b02-116">**Immer**, wenn Verkaufsofferten automatisch beim Löschen archiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0b02-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|  
    |<span data-ttu-id="f0b02-117">**Rahmenaufträge archivieren**</span><span class="sxs-lookup"><span data-stu-id="f0b02-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="f0b02-118">Wählen Sie diese Option aus, um Rahmenaufträge bei jedem Löschen automatisch zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="f0b02-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|  
    |<span data-ttu-id="f0b02-119">**Aufträge und Reklamationen archivieren**</span><span class="sxs-lookup"><span data-stu-id="f0b02-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="f0b02-120">Wählen Sie diese Option aus, um Verkaufsaufträge bei jedem Löschen automatisch zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="f0b02-120">Select to automatically archive sales orders each time they are deleted.</span></span>|  
    |<span data-ttu-id="f0b02-121">**Automatisches Aktivitätenprotokoll**</span><span class="sxs-lookup"><span data-stu-id="f0b02-121">**Automatic Interaction Log**</span></span>|<span data-ttu-id="f0b02-122">Wählen Sie diese Option aus, um automatisch einen Eintrag für den Kontakt im Aktivitätenprotokoll zu erstellen, wenn ein Verkaufsauftrag oder eine Teillieferung gebucht wird oder wenn eine Verkaufsofferte in einen Verkaufsauftrag umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="f0b02-122">Select to automatically create an entry for the contact in the interaction log when a sales order or partial shipment is posted, or when a sales quote is converted into a sales order.</span></span> <span data-ttu-id="f0b02-123">**Hinweis:** Dieses Feld ist auf der Seite **Kreditoren & Einkauf Einr.** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0b02-123">**Note:**  This field is not available on the **Purchases & Payables Setup** page.</span></span>|  

3.  <span data-ttu-id="f0b02-124">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f0b02-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f0b02-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0b02-125">See Also</span></span>  
 <span data-ttu-id="f0b02-126">[Einkaufsbelege und Verkaufsbelege (Schweiz)](swiss-purchase-documents-and-sales-documents.md) </span><span class="sxs-lookup"><span data-stu-id="f0b02-126">[Swiss Purchase Documents and Sales Documents](swiss-purchase-documents-and-sales-documents.md) </span></span>  
 <span data-ttu-id="f0b02-127">[Importieren von Postleitzahlen (Schweiz)](how-to-import-swiss-post-codes.md) </span><span class="sxs-lookup"><span data-stu-id="f0b02-127">[Import Swiss Post Codes](how-to-import-swiss-post-codes.md) </span></span>  
 <span data-ttu-id="f0b02-128">[Drucken einer Lagerkommissionierliste von einem Auftrag](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span><span class="sxs-lookup"><span data-stu-id="f0b02-128">[Print an Inventory Picking List from a Sales Order](how-to-print-an-inventory-picking-list-from-a-sales-order.md) </span></span>  
 [<span data-ttu-id="f0b02-129">So drucken Sie im Verlauf von Stapelbuchungen Verkaufsaufträge und Bestellungen</span><span class="sxs-lookup"><span data-stu-id="f0b02-129">Print Sales and Purchase Orders During Batch Posting</span></span>](how-to-print-sales-and-purchase-orders-during-batch-posting.md)

