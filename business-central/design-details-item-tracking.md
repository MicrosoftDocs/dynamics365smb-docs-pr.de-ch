---
title: 'Designdetails: Artikeltrackingdesign | Microsoft Docs'
description: Dieses Thema zeigt eine Übersicht über Entwurfsdetails für Artikeltracking.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2e770792bea2c4ddbc66128f20726d58654737d1
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185050"
---
# <a name="design-details-item-tracking"></a><span data-ttu-id="af2b3-103">Designdetails: Artikeltracking</span><span class="sxs-lookup"><span data-stu-id="af2b3-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="af2b3-104">Da der Warenfluss in heutigen Lieferketten immer komplexer wird, wird die Möglichkeit, Artikel nachzuverfolgen für die involvierten Unternehmen immer wichtiger.</span><span class="sxs-lookup"><span data-stu-id="af2b3-104">As the flow of goods in today’s supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="af2b3-105">Den Transaktionsfluss eines Artikels zu überwachen ist eine gesetzlich vorgeschriebenes Erfordernis in Bezug auf medizinische und chemische Vorräte, andere Sektoren haben Produkte mit Garantien oder Ablaufdatumsangaben für Kundenservicegründe zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="af2b3-105">Monitoring an item’s transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="af2b3-106">Ein Artikeltrackingsystem sollte für eine einfache Handhabung der Serien- und Chargennummern bieten, unter Berücksichtigung, dass jeder Artikel eine eindeutige Ware darstellt, Empfang und Eingang, Lagerort und Verkaufsdatum anzeigt.</span><span class="sxs-lookup"><span data-stu-id="af2b3-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="af2b3-107">hat schrittweise seine Abdeckung dieser Geschäftsanforderung erweitert und stellt heute eine breite Funktionalität und festes Kernstück in den Erweiterungen bereit.einen widerrufen Kernstück bereitstellt, in denen Erweiterungen definieren.</span><span class="sxs-lookup"><span data-stu-id="af2b3-107">has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="af2b3-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="af2b3-108">In This Section</span></span>  
[<span data-ttu-id="af2b3-109">Designdetails: Artikeltrackingdesign</span><span class="sxs-lookup"><span data-stu-id="af2b3-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="af2b3-110">Designdetails: Artikeltracking-Buchungsstruktur</span><span class="sxs-lookup"><span data-stu-id="af2b3-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="af2b3-111">Designdetails: Aktive vs. historische Artikeltrackingposten</span><span class="sxs-lookup"><span data-stu-id="af2b3-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="af2b3-112">Designdetails – Artikeltrackingzeilenfenster-Seite</span><span class="sxs-lookup"><span data-stu-id="af2b3-112">Design Details: Item Tracking Lines Page</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="af2b3-113">Designdetails: Artikeltrackingverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="af2b3-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="af2b3-114">Designdetails: Artikeltracking und Planung</span><span class="sxs-lookup"><span data-stu-id="af2b3-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="af2b3-115">Designdetails: Artikeltracking und Reservierungen</span><span class="sxs-lookup"><span data-stu-id="af2b3-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="af2b3-116">Designdetails: Artikeltracking im Lager</span><span class="sxs-lookup"><span data-stu-id="af2b3-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)
