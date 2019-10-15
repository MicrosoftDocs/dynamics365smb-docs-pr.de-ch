---
title: 'Designdetails: Bedarf und Vorrat | Microsoft Docs'
description: Bedarf ist der Oberbegriff, der für jede Art Brutto-Bedarf verwendet wird, beispielsweise für Verkaufsauftrags und Komponentenbedarf aus einem Fertigungsauftrag. Darüber hinaus ermöglicht die Anwendung noch weitere technische Bedarfsarten, wie z.B. negative Lagerbestände und Einkaufsreklamationen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 8ef7211aa812b1faf784ecf36f1873a6e2dcc6fc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303652"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="fa5a1-104">Designdetails: Bedarf und Vorrat</span><span class="sxs-lookup"><span data-stu-id="fa5a1-104">Design Details: Demand and Supply</span></span>
<span data-ttu-id="fa5a1-105">Bedarf ist der Oberbegriff, der für jede Art Brutto-Bedarf verwendet wird, beispielsweise für Verkaufsauftrags und Komponentenbedarf aus einem Fertigungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="fa5a1-105">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="fa5a1-106">Darüber hinaus ermöglicht die Anwendung noch weitere technische Bedarfsarten, wie z.B. negative Lagerbestände und Einkaufsreklamationen.</span><span class="sxs-lookup"><span data-stu-id="fa5a1-106">In addition, application allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  

 <span data-ttu-id="fa5a1-107">Vorrat ist der allgemeine Begriff für jede Art von positiver oder eingehender Menge, wie etwa Bestands-, Einkauf-, Montage-, Fertigungs- oder eingehende Umlagerungen.</span><span class="sxs-lookup"><span data-stu-id="fa5a1-107">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="fa5a1-108">Darüber hinaus stellt möglicherweise eine Verkaufsreklamation ebenfalls einen Vorrat dar.</span><span class="sxs-lookup"><span data-stu-id="fa5a1-108">In addition, a sales return may also represent supply.</span></span>  

 <span data-ttu-id="fa5a1-109">Um die vielen Quellen von Nachfrage und Angebot zu sortieren, organisiert das Planungssystem sie auf zwei Zeitachsen, die Bestandsprofile genannt werden.</span><span class="sxs-lookup"><span data-stu-id="fa5a1-109">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="fa5a1-110">Das eine Profil enthält Bedarfsereignisse und das andere enthält die entsprechenden Zubehörereignisse.</span><span class="sxs-lookup"><span data-stu-id="fa5a1-110">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="fa5a1-111">Jedes Ereignis repräsentiert eine Auftragsnetzwerkeinheit, wie etwa eine Verkaufsauftragszeile, einen Lagerposten oder eine Fertigungsauftragszeile.</span><span class="sxs-lookup"><span data-stu-id="fa5a1-111">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  

 <span data-ttu-id="fa5a1-112">Wenn Bestandsprofile geladen werden, werden die verschiedenen BBedarf-Vorrat-Sätze ausgeglichen, um einen Beschaffungsplan auszustellen, der die aufgeführten Ziele erfüllt.</span><span class="sxs-lookup"><span data-stu-id="fa5a1-112">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  

 <span data-ttu-id="fa5a1-113">Planungsparameter und Lagerbestände sind andere Arten von Bedarf und Vorrat bzw. sind einem integrierten Ausgleich unterworfen, um den Lagerbestand wieder aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="fa5a1-113">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="fa5a1-114">Weitere Informationen finden Sie unter [Designdetails: Behandlungs-Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="fa5a1-114">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="fa5a1-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa5a1-115">See Also</span></span>  
 <span data-ttu-id="fa5a1-116">[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="fa5a1-116">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="fa5a1-117">[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="fa5a1-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="fa5a1-118">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="fa5a1-118">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
