---
title: Schliessen Sie Artikelbucheinträge, die aus einer festen Anwendung stammen
description: Erfahren Sie, wie Sie einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion im Artikel-Erfassungsjournal erstellen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/14/2020
ms.author: edupont
ms.openlocfilehash: 2cc663d580da4738247b9fcdbe5fc4504c37fa73
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013885"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="0419e-103">Schliessen von offenen Lagerposten aus einem festen Ausgleich im Artikel Erf.-Journal</span><span class="sxs-lookup"><span data-stu-id="0419e-103">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>

<span data-ttu-id="0419e-104">Sie können das Feld **Ausgegl. von Posten** auf der Seite **Artikel Erf.-Journal** verwenden, um einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0419e-104">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="0419e-105">Beispielsweise um die ausgehende Transaktion zu korrigieren oder ihre Rückgabe zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0419e-105">For example, to correct the outbound transaction or to process its return.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="0419e-106">Feste Ausgleiche, die auf diese Weise vorgenommen werden, gelten nur für die Kosten, nicht für die Menge.</span><span class="sxs-lookup"><span data-stu-id="0419e-106">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="0419e-107">Entsprechend schliesst der gebuchte positive Lagerposten nicht den angewendeten ausgehenden Posten und bleibt selbst offen.</span><span class="sxs-lookup"><span data-stu-id="0419e-107">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="0419e-108">Dies gilt auch, wenn Sie einen festen Ausgleich für einen positiven Posten mit einem negativen Posten buchen, der nicht durch einen positiven regulären Posten geschlossen wurde. Dann bleiben die positiven und negativen Posten offen.</span><span class="sxs-lookup"><span data-stu-id="0419e-108">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>
> <span data-ttu-id="0419e-109">Dies bedeutet auch, dass Sie eine Lagerbuchungsperiode nicht schliessen können, wenn ein solcher Posten vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0419e-109">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="0419e-110">Sie können Ausgleichsposten unter bestimmten Bedingungen ändern und erneut anwenden, indem Sie die Seite **Anwendungs-Arbeitsblatt** verwenden.</span><span class="sxs-lookup"><span data-stu-id="0419e-110">You can change and reapply application entries under certain conditions by using the **Application Worksheet** page.</span></span>  

<span data-ttu-id="0419e-111">Der folgende Ablauf zeigt, wie solche Posten durch Ausführen von zwei korrigierenden Buchungen im Artikel Erfassungsjournal geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="0419e-111">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="0419e-112">So schliessen Sie offene Lagerposten, die aus einem festen Ausgleich im Artikel Erfassungsjournal entstanden sind</span><span class="sxs-lookup"><span data-stu-id="0419e-112">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1. <span data-ttu-id="0419e-113">Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Zugang mit der entsprechenden Menge zu buchen.</span><span class="sxs-lookup"><span data-stu-id="0419e-113">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="0419e-114">Dadurch wird der ursprüngliche negative Posten mit einem festen Ausgleich geschlossen.</span><span class="sxs-lookup"><span data-stu-id="0419e-114">This closes the original negative entry with a fixed application.</span></span>  

    <span data-ttu-id="0419e-115">Das Feld **Ausgegl.-von-Posten** gibt die Nummer des ausgehenden Lagerpostens an, dessen Einstandspreis dem eingehenden Lagerposten weitergeleitet wird, wenn Sie eine eingehende Transaktion des Typs **Zugang** oder **Einkauf** mit dem Artikel Erf.-Journal buchen.</span><span class="sxs-lookup"><span data-stu-id="0419e-115">The **Applies-from Entry** field specifies the number of the outbound item ledger entry whose cost is forwarded to the inbound item ledger entry when you post an inbound transaction of type **Positive Adjmt.** or **Purchase** with the item journal.</span></span>  
2. <span data-ttu-id="0419e-116">Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Abgang zu buchen.</span><span class="sxs-lookup"><span data-stu-id="0419e-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="0419e-117">Dadurch wird der ursprüngliche korrigierende positive Posten mit einem festen Ausgleich geschlossen.</span><span class="sxs-lookup"><span data-stu-id="0419e-117">This closes the original corrective positive entry with a fixed application.</span></span>  

    <span data-ttu-id="0419e-118">Das Feld **Ausgegl.-von-Posten** gibt an, ob die Menge in der Artikel Erf.-Journalzeile mit einem bereits gebuchten Beleg ausgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0419e-118">The **Applies-to Entry** field specifies if the quantity in the item journal line should be applied to an already-posted document.</span></span> <span data-ttu-id="0419e-119">Ist dies der Fall, geben Sie die Postennummer des Lagerpostens ein, der mit der Artikel Erf.-Journalzeile ausgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0419e-119">If this is the case, enter the entry number of the item ledger entry to which the item journal line should be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="0419e-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0419e-120">See Also</span></span>

[<span data-ttu-id="0419e-121">Entfernen und erneutes Ausgleichen von Lagerposten</span><span class="sxs-lookup"><span data-stu-id="0419e-121">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
[<span data-ttu-id="0419e-122">Verarbeiten von Verkaufsrücklieferung und Stornierungen</span><span class="sxs-lookup"><span data-stu-id="0419e-122">Process Sales Returns and Cancellations</span></span>](sales-how-process-sales-returns-cancellations.md)  
[<span data-ttu-id="0419e-123">Einrichten der Lagerwertberechnung und der Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="0419e-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="0419e-124">Verwalten der Lagerregulierung</span><span class="sxs-lookup"><span data-stu-id="0419e-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="0419e-125">Designdetails: Kostenberechnungsmethoden</span><span class="sxs-lookup"><span data-stu-id="0419e-125">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
