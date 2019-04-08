---
title: Designdetails - Lagerhausverwaltung | Microsoft Docs
description: Diese Dokumentation gibt einen Überblick über Konzepte und Prinzipien, die in den Logistikfunktionen in  Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 37c432a121c8105fbe982a4f8968094105530e3a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "819164"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="a56ab-103">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="a56ab-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="a56ab-104">Diese Dokumentation gibt einen Überblick über Konzepte und Prinzipien, die in den Logistikfunktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a56ab-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a56ab-105">Erläutert das Design hinter den Zentrallagerfunktionen und wie die Einlagerung mit anderen Lieferkettenfunktionen integriert ist.</span><span class="sxs-lookup"><span data-stu-id="a56ab-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="a56ab-106">Um die verschiedenen Komplexitätsniveaus der Lagerhaltung zu unterscheiden, ist diese Dokumentation in zwei allgemeine Gruppen, grundlegende und erweiterte Lagerhaltung aufgeteilt, angegeben durch Abteilungstitel.</span><span class="sxs-lookup"><span data-stu-id="a56ab-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="a56ab-107">Diese einfache Unterscheidung umfasst verschiedene Komplexitätsebenen, die durch definierte Produktdetails und Lagerorteinrichtung definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a56ab-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="a56ab-108">Weitere Informationen finden Sie unter [Designdetails: Lagerhaus einrichten](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a56ab-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="a56ab-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a56ab-109">In This Section</span></span>  
[<span data-ttu-id="a56ab-110">Designdetails: Lagerübersicht</span><span class="sxs-lookup"><span data-stu-id="a56ab-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="a56ab-111">Designdetails: Lagereinrichtung</span><span class="sxs-lookup"><span data-stu-id="a56ab-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="a56ab-112">Designdetails: Eingehender Lagerfluss</span><span class="sxs-lookup"><span data-stu-id="a56ab-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="a56ab-113">Designdetails: Interner Lagerfluss</span><span class="sxs-lookup"><span data-stu-id="a56ab-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="a56ab-114">Designdetails: Verfügbarkeit im Lager</span><span class="sxs-lookup"><span data-stu-id="a56ab-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="a56ab-115">Designdetails: Ausgehender Lagerfluss</span><span class="sxs-lookup"><span data-stu-id="a56ab-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="a56ab-116">Designdetails: Integration mit dem Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="a56ab-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)
