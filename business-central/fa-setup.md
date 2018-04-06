---
title: Anlagen einrichten | Microsoft Docs
description: "Kennenlernen der die Abfolge von Aufgaben, die Sie ausführen müssen, um Anlagen einzurichten, wie Arbeitsplätze oder Gebäude."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c20d4997e84db416e2103d2318533082adc04b49
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="34b4d-103">Anlagen einrichten</span><span class="sxs-lookup"><span data-stu-id="34b4d-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="34b4d-104">Um mit Anlagen arbeiten können, müssen Sie einige Elemente festlegen:</span><span class="sxs-lookup"><span data-stu-id="34b4d-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="34b4d-105">Wie Sie Anlagen versichern, verwalten und abschreiben.</span><span class="sxs-lookup"><span data-stu-id="34b4d-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="34b4d-106">Wie Sie Kosten und andere Werte in der Fibuposten erfassen.</span><span class="sxs-lookup"><span data-stu-id="34b4d-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="34b4d-107">Die folgende Tabelle enthält Verknüpfungen für weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="34b4d-107">The table below has links to more information.</span></span> <span data-ttu-id="34b4d-108">Nachdem Sie diese Dinge festgelegt haben, können Sie die verschiedene Aktivitäten beginnen.</span><span class="sxs-lookup"><span data-stu-id="34b4d-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="34b4d-109">Weitere Informationen finden Siue unter [Anlagen](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="34b4d-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="34b4d-110">Sie können Anlagentransaktionen im Fenster **Anlagen Fibu Buch.-Blatt** oder im Fenster **Anlagen Buch-Blatt** erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="34b4d-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="34b4d-111">Die Hilfe zu den Anlagen beschreibt lediglich, wie das Fenster **Anlagen Fibu Buch.-Blatt** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34b4d-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="34b4d-112">Wenn Sie das Kontrollkästchen für eine Anlagenaktivität im Abschnitt **Fibu-Integration** im Fenster **AfA-Buch-Karte** aktiveren, wird das **Anlagen Fibu Buch.-Blatt** Fenster verwendet, um Transaktionen für die fragliche Aktivität zu buchen.</span><span class="sxs-lookup"><span data-stu-id="34b4d-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

<span data-ttu-id="34b4d-113">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="34b4d-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="34b4d-114">Aktion</span><span class="sxs-lookup"><span data-stu-id="34b4d-114">To</span></span> | <span data-ttu-id="34b4d-115">Informationen</span><span class="sxs-lookup"><span data-stu-id="34b4d-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="34b4d-116">Richten Sie Standardsachkonten, Verteilungsschlüssel, Buch.-Blattvorlagen und - namen für Anlagebuchungen ein und erstellen feste Anlageklassen und Unterklassen, wie beispielsweise materielle und immaterielle.</span><span class="sxs-lookup"><span data-stu-id="34b4d-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="34b4d-117">Allgemeine Anlagen-Informationen einrichten</span><span class="sxs-lookup"><span data-stu-id="34b4d-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="34b4d-118">Erstellen Sie Abschreibungsbücher, definieren verschiedene Abschreibungsmethoden, integrieren in die Fibuposten und aktivieren das Kopieren der Posten in mehrere Abschreibungsbücher.</span><span class="sxs-lookup"><span data-stu-id="34b4d-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="34b4d-119">Richten Sie eine neue Anlagenabschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="34b4d-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="34b4d-120">Aktivieren Sie Versicherungen von Anlagen, richten allgemeine Versicherungsinformationen und eine Versicherungskarte pro Versicherung ein und bereiten Buch.-Blätter vor, um Versicherungskosten zu buchen.</span><span class="sxs-lookup"><span data-stu-id="34b4d-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="34b4d-121">Um Anlagenversicherung einzurichten:</span><span class="sxs-lookup"><span data-stu-id="34b4d-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="34b4d-122">Aktivieren Sie die Wartung von Anlagen, richten allgemeine Wartungsinformationen und Wartungs-Buchungskonten ein, und definieren Sie Arten von Wartungsarbeiten.</span><span class="sxs-lookup"><span data-stu-id="34b4d-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="34b4d-123">Um Anlagenwartung einzurichten:</span><span class="sxs-lookup"><span data-stu-id="34b4d-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="34b4d-124">Informieren Sie sich über verschiedene Anlagen-Abschreibungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="34b4d-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="34b4d-125">Abschreibungsmethoden</span><span class="sxs-lookup"><span data-stu-id="34b4d-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="34b4d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34b4d-126">See Also</span></span>
[<span data-ttu-id="34b4d-127">Anlagen</span><span class="sxs-lookup"><span data-stu-id="34b4d-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="34b4d-128">Finanzen</span><span class="sxs-lookup"><span data-stu-id="34b4d-128">Finance</span></span>](finance.md)  
<span data-ttu-id="34b4d-129">[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="34b4d-129">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="34b4d-130">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="34b4d-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

