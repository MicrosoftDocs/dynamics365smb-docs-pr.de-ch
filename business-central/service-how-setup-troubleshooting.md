---
title: Einrichten von Fehlerlösungsprozessen | Microsoft Docs
description: Erfahren Sie, wie Sie Vorgänge eingerichtet, die Techniker helfen, Probleme bei Serviceartikeln zu identifizieren und zu bearbeiten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7fdbc30e20e7d5a8feeb17a97ccdee3688fa7607
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380420"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="a9aa5-103">Problembehandlung für Serviceartikel einrichten</span><span class="sxs-lookup"><span data-stu-id="a9aa5-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="a9aa5-104">Sie können Lösungsanleitungen einrichten, die den Technikern helfen, Probleme zu lösen, wenn Sie einen Service ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9aa5-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="a9aa5-105">Beispielsweise könnten möglicherweise Richtlinien eine Liste der Schritte oder eine Reihe von Fragen sein, um den Artikel einzurichten.</span><span class="sxs-lookup"><span data-stu-id="a9aa5-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="a9aa5-106">In diesem Fenster können Sie Lösungsanleitungen festlegen, diese Serviceartikelgruppen, Artikeln oder Serviceartikeln zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a9aa5-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="a9aa5-107">Es gibt eine Übernahmehierarchie für Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="a9aa5-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="a9aa5-108">Wenn Sie diese einer Serviceartikelgruppe zuweisen, übernehmen die Artikel, die in die Gruppe enthalten sind, die Richtlinien, es sei denn, Sie definieren diese für den Artikel.</span><span class="sxs-lookup"><span data-stu-id="a9aa5-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="a9aa5-109">Analog übernehmen Serviceartikel Richtlinien der Artikel.</span><span class="sxs-lookup"><span data-stu-id="a9aa5-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="a9aa5-110">So richten Sie Lösungsanleitungen ein</span><span class="sxs-lookup"><span data-stu-id="a9aa5-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="a9aa5-111">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Problembehandlung** ein, und wählen Sie dann den zugehörigen Link.</span><span class="sxs-lookup"><span data-stu-id="a9aa5-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a9aa5-112">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="a9aa5-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="a9aa5-113">In diesem Fenster können Sie Lösungsanleitungen Serviceartikelgruppen, Artikeln oder Serviceartikeln zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a9aa5-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="a9aa5-114">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Artikel**, **Serviceartikel** oder **Serviceartikelgruppen** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="a9aa5-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a9aa5-115">Wählen Sie die entsprechende Einheit aus und wählen Sie dann die Aktion **Problemlösung** aus.</span><span class="sxs-lookup"><span data-stu-id="a9aa5-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a9aa5-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9aa5-116">See Also</span></span>
[<span data-ttu-id="a9aa5-117">Service</span><span class="sxs-lookup"><span data-stu-id="a9aa5-117">Service Management</span></span>](service-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]