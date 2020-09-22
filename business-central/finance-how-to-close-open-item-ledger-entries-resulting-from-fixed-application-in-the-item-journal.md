---
title: 'Vorgehensweise: Schliessen von offenen Lagerposten aus einem festen Ausgleich im Artikel Erf.-Journal | Microsoft Docs'
description: Sie können das Feld **Ausgegl. von Posten** auf der Seite **Artikel Erf.-Journal** verwenden, um einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion zu erstellen. Beispielsweise um die ausgehende Transaktion zu korrigieren oder ihre Rückgabe zu verarbeiten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 7a7f31ea698a314d8a69c3bf9c2e7ab04ccd5f46
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783463"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="a9198-104">Schliessen von offenen Lagerposten aus einem festen Ausgleich im Artikel Erf.-Journal</span><span class="sxs-lookup"><span data-stu-id="a9198-104">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="a9198-105">Sie können das Feld **Ausgegl. von Posten** auf der Seite **Artikel Erf.-Journal** verwenden, um einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9198-105">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="a9198-106">Beispielsweise um die ausgehende Transaktion zu korrigieren oder ihre Rückgabe zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a9198-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="a9198-107">Weitere Informationen finden Sie unter Ausgegl. von Posten.</span><span class="sxs-lookup"><span data-stu-id="a9198-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="a9198-108">Feste Ausgleiche, die auf diese Weise vorgenommen werden, gelten nur für die Kosten, nicht für die Menge.</span><span class="sxs-lookup"><span data-stu-id="a9198-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="a9198-109">Entsprechend schliesst der gebuchte positive Lagerposten nicht den angewendeten ausgehenden Posten und bleibt selbst offen.</span><span class="sxs-lookup"><span data-stu-id="a9198-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="a9198-110">Dies gilt auch, wenn Sie einen festen Ausgleich für einen positiven Posten mit einem negativen Posten buchen, der nicht durch einen positiven regulären Posten geschlossen wurde. Dann bleiben die positiven und negativen Posten offen.</span><span class="sxs-lookup"><span data-stu-id="a9198-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="a9198-111">Dies bedeutet auch, dass Sie eine Lagerbuchungsperiode nicht schliessen können, wenn ein solcher Posten vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a9198-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="a9198-112">Der folgende Ablauf zeigt, wie solche Posten durch Ausführen von zwei korrigierenden Buchungen im Artikel Erfassungsjournal geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a9198-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="a9198-113">So schliessen Sie offene Lagerposten, die aus einem festen Ausgleich im Artikel Erfassungsjournal entstanden sind</span><span class="sxs-lookup"><span data-stu-id="a9198-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="a9198-114">Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Zugang mit der entsprechenden Menge zu buchen.</span><span class="sxs-lookup"><span data-stu-id="a9198-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="a9198-115">Dadurch wird der ursprüngliche negative Posten mit einem festen Ausgleich geschlossen.</span><span class="sxs-lookup"><span data-stu-id="a9198-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="a9198-116">Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Abgang zu buchen.</span><span class="sxs-lookup"><span data-stu-id="a9198-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="a9198-117">Dadurch wird der ursprüngliche korrigierende positive Posten mit einem festen Ausgleich geschlossen.</span><span class="sxs-lookup"><span data-stu-id="a9198-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a9198-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9198-118">See Also</span></span>  
[<span data-ttu-id="a9198-119">Entfernen und erneutes Ausgleichen von Lagerposten</span><span class="sxs-lookup"><span data-stu-id="a9198-119"> Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="a9198-120">[Verarbeiten von Verkaufsrücklieferung und Stornierungen](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="a9198-120">[Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="a9198-121">[Einrichten der Lagerwertberechnung und der Kostenrechnung](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="a9198-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="a9198-122">[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="a9198-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="a9198-123">Designdetails: Kostenberechnungsmethoden</span><span class="sxs-lookup"><span data-stu-id="a9198-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
