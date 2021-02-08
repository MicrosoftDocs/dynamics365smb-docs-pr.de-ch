---
title: Lagerverwaltung (Schweiz)
description: Schweizer Erweiterungen enthalten spezielle Lagerverwaltungsfunktionen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 413f3a7db5230373aaac066e25f385c64036bb58
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753169"
---
# <a name="swiss-inventory-management"></a><span data-ttu-id="2dcce-103">Lagerverwaltung (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="2dcce-103">Swiss Inventory Management</span></span>
[!INCLUDE[prod_short](../../includes/prod_short.md)] <span data-ttu-id="2dcce-104">enthält Schweizer Erweiterungen für Lagerverwaltung.</span><span class="sxs-lookup"><span data-stu-id="2dcce-104">includes Swiss enhancements to inventory management.</span></span> <span data-ttu-id="2dcce-105">Dies beinhaltet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2dcce-105">This includes the following:</span></span>  

- <span data-ttu-id="2dcce-106">Detaillierte Berichte.</span><span class="sxs-lookup"><span data-stu-id="2dcce-106">Detailed reporting.</span></span>  <span data-ttu-id="2dcce-107">Weitere Informationen finden Sie unter Verkaufstatistikbericht und Lagerlistenbericht.</span><span class="sxs-lookup"><span data-stu-id="2dcce-107">For more information, see the Inventory - Sales Statistics report and the Inventory - List report.</span></span>  
- <span data-ttu-id="2dcce-108">Die Fähigkeit, eine Rechnung mit mehreren Lieferungen nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="2dcce-108">The ability to track an invoice with multiple shipments.</span></span>  
- <span data-ttu-id="2dcce-109">Einschliessen eines Artikelkarten-Lagerortcodes als Standardlagerortcode für Verkaufszeilen und Artikelerfassungsjournale.</span><span class="sxs-lookup"><span data-stu-id="2dcce-109">Including an item card location code as the default location code for sales lines and item journals.</span></span> <span data-ttu-id="2dcce-110">Weitere Informationen finden Sie unter [Einrichten von Lagerorten](../../inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="2dcce-110">For more information, see [Set Up Locations](../../inventory-how-setup-locations.md).</span></span>

## <a name="managing-item-details"></a><span data-ttu-id="2dcce-111">Verwalten von Artikeldetails</span><span class="sxs-lookup"><span data-stu-id="2dcce-111">Managing Item Details</span></span>  
<span data-ttu-id="2dcce-112">Unternehmen haben u. U. verschiedene Lager für verschiedene Produktkategorien.</span><span class="sxs-lookup"><span data-stu-id="2dcce-112">Companies can have different warehouses for different product categories.</span></span> <span data-ttu-id="2dcce-113">In diesem Fall muss der von der Artikelkarte abgerufene Standardlagerortcode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2dcce-113">In such cases, you must use the default location code retrieved from the item card.</span></span> <span data-ttu-id="2dcce-114">Wenn Sie einen Lagerortcode für einen Artikel definieren, wird dieser auf die Verkaufszeilen und Artikelerfassungsjournale als Standardlagerortcode übertragen.</span><span class="sxs-lookup"><span data-stu-id="2dcce-114">When you define a location code for an item, it is transferred to the sales lines and item journals as a default item location code.</span></span> <span data-ttu-id="2dcce-115">Weitere Informationen finden Sie unter Verkaufszeile und Artikel Erf.-Journalzeile.</span><span class="sxs-lookup"><span data-stu-id="2dcce-115">For more information, see the Sales Line and the Item Journal Line table.</span></span>  

<span data-ttu-id="2dcce-116">Zusätzliche Informationen, wie Debitorennummer, Lieferadresscode und Debitorenvertriebsmitarbeitercode wird in Lagerposten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2dcce-116">Additional information, such as customer number, ship-to address code, and customer sales person code, is stored in item ledger entries.</span></span> <span data-ttu-id="2dcce-117">Diese Informationen sollen dabei helfen, benutzerdefinierte Berichterstellungskriterien wie Einnahmen pro Debitor zu erstellen und Artikel oder Debitoren für Verkäufer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2dcce-117">This information helps you to create customized reporting criteria, such as revenue per customer, and item or sales provisions for sales people.</span></span> <span data-ttu-id="2dcce-118">Weitere Informationen erhalten Sie in der Tabelle "Lagerposten".</span><span class="sxs-lookup"><span data-stu-id="2dcce-118">For more information, see the Item Ledger Entry table.</span></span>  

## <a name="invoices-with-multiple-shipments"></a><span data-ttu-id="2dcce-119">Rechnungen mit mehreren Lieferungen</span><span class="sxs-lookup"><span data-stu-id="2dcce-119">Invoices with Multiple Shipments</span></span>  
<span data-ttu-id="2dcce-120">Sind mehrere Lieferungen für einen Debitoren gebucht worden, können Sie Sammelrechnungen mit der Funktion **Lieferzeilen abrufen** erstellen.</span><span class="sxs-lookup"><span data-stu-id="2dcce-120">If multiple shipments have been posted for a customer, then you can create a combined invoice with the **Get Shipment Lines** function.</span></span> <span data-ttu-id="2dcce-121">Weitere Informationen finden Sie auf der Seite „Versandzeilen abrufen“.</span><span class="sxs-lookup"><span data-stu-id="2dcce-121">For more information, see the Get Shipment Lines page.</span></span> <span data-ttu-id="2dcce-122">Wenn Sie diese Funktion verwenden, enthält der Text, der in den Rechnungszeilen erstellt wird, die Informationen über die Nummer der Auslieferung und das Lieferdatum.</span><span class="sxs-lookup"><span data-stu-id="2dcce-122">When you use this function, the text created on the invoice lines includes information about the shipment number and the shipment date.</span></span> <span data-ttu-id="2dcce-123">Beispielsweise kann der Text als Lieferungsnummer erscheinen.</span><span class="sxs-lookup"><span data-stu-id="2dcce-123">For example, the text could appear as Shipment No.</span></span> <span data-ttu-id="2dcce-124">102040 von 25.01.01.</span><span class="sxs-lookup"><span data-stu-id="2dcce-124">102040 of 25.01.01.</span></span> <span data-ttu-id="2dcce-125">Auf diese Weise können Sie Rechnungen mit mehreren Lieferungen verfolgen.</span><span class="sxs-lookup"><span data-stu-id="2dcce-125">This allows you to easily track invoices with multiple shipments.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2dcce-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dcce-126">See Also</span></span>  
 <span data-ttu-id="2dcce-127">[Lokale Funktion (Schweiz)](switzerland-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="2dcce-127">[Switzerland Local Functionality](switzerland-local-functionality.md) </span></span>  
 [<span data-ttu-id="2dcce-128">Einrichten von Lagerorten</span><span class="sxs-lookup"><span data-stu-id="2dcce-128">Set Up Locations</span></span>](../../inventory-how-setup-locations.md)
