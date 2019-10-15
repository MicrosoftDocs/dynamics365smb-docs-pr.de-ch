---
title: 'Designdetails: Charge für Charge | Microsoft Docs'
description: Erfahren Sie, wie die Charge-für-Charge-Rrichtlinie verwendet wird, um die Bestellmenge auf Grundlage von Bedarf abzustimmen.
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
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 5669378383d94b33a25a60a882709885e1463a6d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303128"
---
# <a name="design-details-lot-for-lot"></a><span data-ttu-id="90515-103">Designdetails: Charge für Charge</span><span class="sxs-lookup"><span data-stu-id="90515-103">Design Details: Lot-for-Lot</span></span>
<span data-ttu-id="90515-104">Die Charge-für-Charge-Richtlinie ist die flexibelste, da das System nur auf tatsächlichen Bedarf reagiert; dazu reagiert sie auf voraussichtlichen Bedarf aus der Planung und auf Rahmenaufträge und gleicht die Auftragsmenge auf der Grundlage des Bedarfs ab.</span><span class="sxs-lookup"><span data-stu-id="90515-104">The lot-for-lot policy is the most flexible because the system only reacts on actual demand, plus it acts on anticipated demand from forecast and blanket orders and then settles the order quantity based on the demand.</span></span> <span data-ttu-id="90515-105">Die Charge-für-Charge-Richtlinie bezieht sich auf A- und B-Artikel, bei denen der bestand angenommen werden kann, jedoch vermieden werden sollte.</span><span class="sxs-lookup"><span data-stu-id="90515-105">The lot-for-lot policy is aimed at A- and B-items where inventory can be accepted but should be avoided.</span></span>  

<span data-ttu-id="90515-106">In mancher Hinsicht sieht die Charge-für-Charge-Richtlinie wie die Auftragsrichtlinie aus, sie verfolgt jedoch einen generischen Ansatz für Artikel; sie kann Mengen im Bestand akzeptieren und bündelt Bedarf und den entsprechenden Vorrat in Zeitrahmen, die vom Benutzer definiert werden.</span><span class="sxs-lookup"><span data-stu-id="90515-106">In some ways, the lot-for-lot policy looks like the Order policy, but it has a generic approach to items; it can accept quantities in inventory, and it bundles demand and corresponding supply in time buckets defined by the user.</span></span>  

<span data-ttu-id="90515-107">Das Zeitrahmen wird im Feld **Zeitrahmen** definiert.</span><span class="sxs-lookup"><span data-stu-id="90515-107">The time bucket is defined in the **Time Bucket** field.</span></span> <span data-ttu-id="90515-108">Die Anwendung arbeitet mit einem minimale Zeitrahmen von einem Tag, da dies die kleinste Zeiteinheit bei Bedarfs- und Vorratsereignissen im System ist (obwohl in der Praxis die Zeiteinheit in Fertigungsaufträgen und Komponentenbedarfen Sekunden sein kann).</span><span class="sxs-lookup"><span data-stu-id="90515-108">The system works with a minimum time bucket of one day, since this is the smallest time unit of measure on demand and supply events in the system (although, in practice, the time unit of measure on production orders and component needs can be seconds).</span></span>  

<span data-ttu-id="90515-109">Das Zeitrahmen legt auch Grenzen dafür fest, wann ein vorhandener Beschaffungsauftrag umgeplant werden soll, um einen angegebenen Bedarf zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="90515-109">The time bucket also sets limits on when an existing supply order should be rescheduled to meet a given demand.</span></span> <span data-ttu-id="90515-110">Wenn der Vorrat innerhalb des Zeitrahmens liegt, wird dieser ein- oder ausgeplant, um den Bedarf zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="90515-110">If the supply lies within the time bucket, it will be rescheduled in or out to meet the demand.</span></span> <span data-ttu-id="90515-111">Wenn er jedoch vor dem Zeitrahmen liegt, verursacht er eine unnötige Anhäufung des Lagerbestandes und sollte storniert werden.</span><span class="sxs-lookup"><span data-stu-id="90515-111">Otherwise, if it lies earlier, it will cause unnecessary build-up of inventory and should be canceled.</span></span> <span data-ttu-id="90515-112">Wenn es später liegt, wird stattdessen ein neuer Beschaffungsauftrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="90515-112">If it lies later, a new supply order will be created instead.</span></span>  

<span data-ttu-id="90515-113">Mit dieser Methode ist es möglich, einen Sicherheitsbestand festzulegen, um mögliche Schwankungen im Vorrat auszugleichen oder plötzlichen Bedarf zu decken.</span><span class="sxs-lookup"><span data-stu-id="90515-113">With this policy, it is also possible to define a safety stock in order to compensate for possible fluctuations in supply, or to meet sudden demand.</span></span>  

<span data-ttu-id="90515-114">Da die Beschaffungsauftragsmenge auf dem tatsächlichen Bedarf basiert, kann es sinnvoll sein, die Auftragsmodifikationen zu verwenden: Aufrunden der Auftragsmenge, um ein angegebenes Auftragsvielfaches zu erreichen (oder eine Einkaufsmengeneinheit), Erhöhen der Auftragsmenge auf eine angegebene Mindestauftragsmenge oder Vermindern der Menge auf die angegebene Auftragshöchstmenge (wodurch zwei oder mehr Vorräte zum Erreichen der insgesamt benötigten Menge erstellt werden).</span><span class="sxs-lookup"><span data-stu-id="90515-114">Because the supply order quantity is based on the actual demand it can make sense to use the order modifiers: round the order quantity up to meet a specified order multiple (or purchase unit of measure), increase the order to a specified minimum order quantity, or decrease the quantity to the specified maximum quantity (and thus create two or more supplies to reach the total needed quantity).</span></span>  

## <a name="see-also"></a><span data-ttu-id="90515-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90515-115">See Also</span></span>  
<span data-ttu-id="90515-116">[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="90515-116">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="90515-117">[Designdetails: Planungsparameter](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="90515-117">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="90515-118">[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="90515-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="90515-119">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="90515-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
