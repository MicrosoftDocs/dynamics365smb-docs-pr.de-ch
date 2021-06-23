---
title: Designdetails - Bestandkosten | Microsoft Docs
description: Diese Dokumentation stellt einen detaillierten technischen Einblick in die Konzepte und Prinzipien bereit, die in den Lagerkostenfunktionen in Business Central verwendet werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8bfcf2b10d9b302c9a65b7cf27c7fb336be68617
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215992"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="a3412-103">Designdetails: Lagerkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="a3412-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="a3412-104">Diese Dokumentation stellt einen detaillierten technischen Einblick in die Konzepte und Prinzipien bereit, die in den Lagerkostenfunktionen in [!INCLUDE[prod_short](includes/prod_short.md)] verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3412-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="a3412-105">Die Kostenverwaltung, die auch als "Lagerabgang" bezeichnet wird, dient zum Erfassen und Melden der Betriebskosten eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="a3412-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="a3412-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a3412-106">In This Section</span></span>  
[<span data-ttu-id="a3412-107">Designdetails: Kostenberechnungsmethoden</span><span class="sxs-lookup"><span data-stu-id="a3412-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="a3412-108">Designdetails: Artikelausgleich</span><span class="sxs-lookup"><span data-stu-id="a3412-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="a3412-109">Designdetails: Bekannte Artikelanwendungsprobleme</span><span class="sxs-lookup"><span data-stu-id="a3412-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="a3412-110">Designdetails: Kostenregulierung</span><span class="sxs-lookup"><span data-stu-id="a3412-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="a3412-111">Designdetails: Buchungsdatum auf Ausgleichs-Wertposten</span><span class="sxs-lookup"><span data-stu-id="a3412-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="a3412-112">Designdetails: Soll-Kosten-Buchen</span><span class="sxs-lookup"><span data-stu-id="a3412-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="a3412-113">Designdetails: Durchschnittskosten</span><span class="sxs-lookup"><span data-stu-id="a3412-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="a3412-114">Designdetails: Abweichung</span><span class="sxs-lookup"><span data-stu-id="a3412-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="a3412-115">Designdetails: Rundung</span><span class="sxs-lookup"><span data-stu-id="a3412-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="a3412-116">Designdetails: Kostenkomponenten</span><span class="sxs-lookup"><span data-stu-id="a3412-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="a3412-117">Designdetails: Bestandsperioden</span><span class="sxs-lookup"><span data-stu-id="a3412-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="a3412-118">Designdetails: Bestandsbuchung</span><span class="sxs-lookup"><span data-stu-id="a3412-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="a3412-119">Designdetails: Fertigungsauftragsbuchung</span><span class="sxs-lookup"><span data-stu-id="a3412-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="a3412-120">Designdetails: Montageauftragsbuchung</span><span class="sxs-lookup"><span data-stu-id="a3412-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="a3412-121">Designdetails: Abgleich mit der Fibuposten</span><span class="sxs-lookup"><span data-stu-id="a3412-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="a3412-122">Designdetails: Konten in der Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="a3412-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="a3412-123">Designdetails: Bestandsbewertung</span><span class="sxs-lookup"><span data-stu-id="a3412-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="a3412-124">Designdetails: Neubewertung</span><span class="sxs-lookup"><span data-stu-id="a3412-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]