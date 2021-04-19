---
title: Lagerverwaltung (Schweiz)
description: Schweizer Erweiterungen enthalten spezielle Lagerverwaltungsfunktionen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 61501236fc923dca608fce50a2b6cef65a3d569d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784021"
---
# <a name="swiss-inventory-management"></a><span data-ttu-id="8d5fa-103">Lagerverwaltung (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="8d5fa-103">Swiss Inventory Management</span></span>
[!INCLUDE[prod_short](../../includes/prod_short.md)] <span data-ttu-id="8d5fa-104">enthält Schweizer Erweiterungen für Lagerverwaltung.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-104">includes Swiss enhancements to inventory management.</span></span> <span data-ttu-id="8d5fa-105">Dies beinhaltet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8d5fa-105">This includes the following:</span></span>  

- <span data-ttu-id="8d5fa-106">Detaillierte Berichte.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-106">Detailed reporting.</span></span>  <span data-ttu-id="8d5fa-107">Weitere Informationen finden Sie unter Verkaufstatistikbericht und Lagerlistenbericht.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-107">For more information, see the Inventory - Sales Statistics report and the Inventory - List report.</span></span>  
- <span data-ttu-id="8d5fa-108">Die Fähigkeit, eine Rechnung mit mehreren Lieferungen nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-108">The ability to track an invoice with multiple shipments.</span></span>  
- <span data-ttu-id="8d5fa-109">Einschliessen eines Artikelkarten-Lagerortcodes als Standardlagerortcode für Verkaufszeilen und Artikelerfassungsjournale.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-109">Including an item card location code as the default location code for sales lines and item journals.</span></span> <span data-ttu-id="8d5fa-110">Weitere Informationen finden Sie unter [Einrichten von Lagerorten](../../inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="8d5fa-110">For more information, see [Set Up Locations](../../inventory-how-setup-locations.md).</span></span>

## <a name="managing-item-details"></a><span data-ttu-id="8d5fa-111">Verwalten von Artikeldetails</span><span class="sxs-lookup"><span data-stu-id="8d5fa-111">Managing Item Details</span></span>  
<span data-ttu-id="8d5fa-112">Unternehmen haben u. U. verschiedene Lager für verschiedene Produktkategorien.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-112">Companies can have different warehouses for different product categories.</span></span> <span data-ttu-id="8d5fa-113">In diesem Fall muss der von der Artikelkarte abgerufene Standardlagerortcode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-113">In such cases, you must use the default location code retrieved from the item card.</span></span> <span data-ttu-id="8d5fa-114">Wenn Sie einen Lagerortcode für einen Artikel definieren, wird dieser auf die Verkaufszeilen und Artikelerfassungsjournale als Standardlagerortcode übertragen.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-114">When you define a location code for an item, it is transferred to the sales lines and item journals as a default item location code.</span></span> <span data-ttu-id="8d5fa-115">Weitere Informationen finden Sie unter Verkaufszeile und Artikel Erf.-Journalzeile.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-115">For more information, see the Sales Line and the Item Journal Line table.</span></span>  

<span data-ttu-id="8d5fa-116">Zusätzliche Informationen, wie Debitorennummer, Lieferadresscode und Debitorenvertriebsmitarbeitercode wird in Lagerposten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-116">Additional information, such as customer number, ship-to address code, and customer sales person code, is stored in item ledger entries.</span></span> <span data-ttu-id="8d5fa-117">Diese Informationen sollen dabei helfen, benutzerdefinierte Berichterstellungskriterien wie Einnahmen pro Debitor zu erstellen und Artikel oder Debitoren für Verkäufer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-117">This information helps you to create customized reporting criteria, such as revenue per customer, and item or sales provisions for sales people.</span></span> <span data-ttu-id="8d5fa-118">Weitere Informationen erhalten Sie in der Tabelle "Lagerposten".</span><span class="sxs-lookup"><span data-stu-id="8d5fa-118">For more information, see the Item Ledger Entry table.</span></span>  

## <a name="invoices-with-multiple-shipments"></a><span data-ttu-id="8d5fa-119">Rechnungen mit mehreren Lieferungen</span><span class="sxs-lookup"><span data-stu-id="8d5fa-119">Invoices with Multiple Shipments</span></span>  
<span data-ttu-id="8d5fa-120">Sind mehrere Lieferungen für einen Debitoren gebucht worden, können Sie Sammelrechnungen mit der Funktion **Lieferzeilen abrufen** erstellen.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-120">If multiple shipments have been posted for a customer, then you can create a combined invoice with the **Get Shipment Lines** function.</span></span> <span data-ttu-id="8d5fa-121">Weitere Informationen finden Sie auf der Seite „Versandzeilen abrufen“.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-121">For more information, see the Get Shipment Lines page.</span></span> <span data-ttu-id="8d5fa-122">Wenn Sie diese Funktion verwenden, enthält der Text, der in den Rechnungszeilen erstellt wird, die Informationen über die Nummer der Auslieferung und das Lieferdatum.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-122">When you use this function, the text created on the invoice lines includes information about the shipment number and the shipment date.</span></span> <span data-ttu-id="8d5fa-123">Beispielsweise kann der Text als Lieferungsnummer erscheinen.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-123">For example, the text could appear as Shipment No.</span></span> <span data-ttu-id="8d5fa-124">102040 von 25.01.01.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-124">102040 of 25.01.01.</span></span> <span data-ttu-id="8d5fa-125">Auf diese Weise können Sie Rechnungen mit mehreren Lieferungen verfolgen.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-125">This allows you to easily track invoices with multiple shipments.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8d5fa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d5fa-126">See Also</span></span>  
 <span data-ttu-id="8d5fa-127">[Lokale Funktion (Schweiz)](switzerland-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="8d5fa-127">[Switzerland Local Functionality](switzerland-local-functionality.md) </span></span>  
 [<span data-ttu-id="8d5fa-128">Einrichten von Lagerorten</span><span class="sxs-lookup"><span data-stu-id="8d5fa-128">Set Up Locations</span></span>](../../inventory-how-setup-locations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]