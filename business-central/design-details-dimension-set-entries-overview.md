---
title: "Dimensionssatzposten Übersicht | Microsoft Docs"
description: In diesem Thema wird beschrieben, wie Dimensionssatzposten in Dynamics 365 gespeichert und gebucht werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1113f371caf00b693144d0ea6f74aed49bbbc9df
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="0586a-103">Dimensionssatz-Eintrags-Übersicht</span><span class="sxs-lookup"><span data-stu-id="0586a-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="0586a-104">In diesem Thema wird beschrieben, wie Dimensionssatzposten in [!INCLUDE[d365fin](includes/d365fin_md.md)] gespeichert und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="0586a-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
## <a name="dimension-sets"></a><span data-ttu-id="0586a-105">Dimensionssätze</span><span class="sxs-lookup"><span data-stu-id="0586a-105">Dimension Sets</span></span>  
<span data-ttu-id="0586a-106">Ein Dimensionssatz ist eine eindeutige Kombination von Dimensionswerten.</span><span class="sxs-lookup"><span data-stu-id="0586a-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="0586a-107">Er wird als Dimensionssatzposten in die Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0586a-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="0586a-108">Jeder Dimensionssatzposten stellt einen einzelnen Dimensionswert dar.</span><span class="sxs-lookup"><span data-stu-id="0586a-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="0586a-109">Der Dimensionssatz wird durch eine allgemeine Dimensionssatz-ID identifiziert, die jedem Dimensionssatzposten zugewiesen wird, der zum Dimensionssatz gehört.</span><span class="sxs-lookup"><span data-stu-id="0586a-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  
  
<span data-ttu-id="0586a-110">Im folgenden Beispiel wird ein Dimensionssatz gezeigt, der drei Dimensionssatzposten aufweist.</span><span class="sxs-lookup"><span data-stu-id="0586a-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="0586a-111">Der Dimensionssatz wird durch eine Dimensionssatz-ID, nämlich 108, identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0586a-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  
  
|<span data-ttu-id="0586a-112">Dimensionssatz-ID</span><span class="sxs-lookup"><span data-stu-id="0586a-112">Dimension Set ID</span></span>|<span data-ttu-id="0586a-113">Dimensionscode</span><span class="sxs-lookup"><span data-stu-id="0586a-113">Dimension Code</span></span>|<span data-ttu-id="0586a-114">Dimensionswertcode</span><span class="sxs-lookup"><span data-stu-id="0586a-114">Dimension Value Code</span></span>|<span data-ttu-id="0586a-115">Dimensionswertname</span><span class="sxs-lookup"><span data-stu-id="0586a-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="0586a-116">108</span><span class="sxs-lookup"><span data-stu-id="0586a-116">108</span></span>|<span data-ttu-id="0586a-117">BEREICH</span><span class="sxs-lookup"><span data-stu-id="0586a-117">AREA</span></span>|<span data-ttu-id="0586a-118">70</span><span class="sxs-lookup"><span data-stu-id="0586a-118">70</span></span>|<span data-ttu-id="0586a-119">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="0586a-119">America North</span></span>|  
|<span data-ttu-id="0586a-120">108</span><span class="sxs-lookup"><span data-stu-id="0586a-120">108</span></span>|<span data-ttu-id="0586a-121">UNTERNEHMENSGRUPPE</span><span class="sxs-lookup"><span data-stu-id="0586a-121">BUSINESSGROUP</span></span>|<span data-ttu-id="0586a-122">HOME</span><span class="sxs-lookup"><span data-stu-id="0586a-122">HOME</span></span>|<span data-ttu-id="0586a-123">Start</span><span class="sxs-lookup"><span data-stu-id="0586a-123">Home</span></span>|  
|<span data-ttu-id="0586a-124">108</span><span class="sxs-lookup"><span data-stu-id="0586a-124">108</span></span>|<span data-ttu-id="0586a-125">KOSTENSTELLE</span><span class="sxs-lookup"><span data-stu-id="0586a-125">DEPARTMENT</span></span>|<span data-ttu-id="0586a-126">VERKAUF</span><span class="sxs-lookup"><span data-stu-id="0586a-126">SALES</span></span>|<span data-ttu-id="0586a-127">Verkauf</span><span class="sxs-lookup"><span data-stu-id="0586a-127">Sales</span></span>|  
  
## <a name="dimension-set-entries"></a><span data-ttu-id="0586a-128">Dimensionssatzposten</span><span class="sxs-lookup"><span data-stu-id="0586a-128">Dimension Set Entries</span></span>  
<span data-ttu-id="0586a-129">Dimensionssätze werden in der Tabelle als **Dimensionssatzposten** mit derselben Dimensionssatz-ID gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0586a-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  
  
<span data-ttu-id="0586a-130">![Dimensions-Postenübersicht](media/dimensionentrynav7.png "DimensionEntryNAV7")</span><span class="sxs-lookup"><span data-stu-id="0586a-130">![Dimension Entry overview](media/dimensionentrynav7.png "DimensionEntryNAV7")</span></span>  
  
<span data-ttu-id="0586a-131">Wenn Sie eine neue Erfassungsjournalzeile, einen Belegkopf oder eine Belegzeile erstellen, können Sie eine Kombination von Dimensionswerten angeben.</span><span class="sxs-lookup"><span data-stu-id="0586a-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="0586a-132">Anstatt jeden Dimensionswert explizit in der Datenbank zu speichern, wird eine Dimensionssatz-ID der Erfassungsjournalzeile, dem Belegkopf oder der Belegzeile zugewiesen, um den Dimensionssatz anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0586a-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  
  
<span data-ttu-id="0586a-133">Wenn Sie das Fenster **Dimensionssatzeinträge bearbeiten**bearbeiten und schliessen, wird eine Prüfung ausgeführt, um festzustellen, ob die Kombination aus Dimensionswerten als Dimensionssatz in der Tabelle existiert.</span><span class="sxs-lookup"><span data-stu-id="0586a-133">When you edit and close the **Edit Dimension Set Entries** window, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="0586a-134">Wenn die Kombination in der Tabelle auftritt, wird die entsprechende Dimensionssatz-ID der Erfassungsjournalzeile, dem Belegkopf oder der Belegzeile zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0586a-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="0586a-135">Andernfalls wird ein neuer Dimensionssatz der Tabelle hinzugefügt, und die neue Dimensionssatz-ID wird der Erfassungsjournalzeile, dem Belegkopf oder der Belegzeile zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0586a-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>  
  
## <a name="performance-improvement"></a><span data-ttu-id="0586a-136">Leistungsverbesserung</span><span class="sxs-lookup"><span data-stu-id="0586a-136">Performance Improvement</span></span>  
<span data-ttu-id="0586a-137">Durch das einmalige Speichern von Dimensionssätzen in der Datenbank wird Datenbankplatz beibehalten und die Gesamtleistung verbessert.</span><span class="sxs-lookup"><span data-stu-id="0586a-137">By storing dimension sets once in the database, database space is preserved, and overall performance is improved.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0586a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0586a-138">See Also</span></span>  
<span data-ttu-id="0586a-139">[Designdetails: Suche nach Dimensionskombinationen](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="0586a-139">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="0586a-140">[Designdetails: Tabellenstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="0586a-140">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
<span data-ttu-id="0586a-141">[Designdetails: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="0586a-141">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
<span data-ttu-id="0586a-142">[Designdetails: Codebeispiele von geänderten Mustern in Änderungen](design-details-code-examples-of-changed-patterns-in-modifications.md) </span><span class="sxs-lookup"><span data-stu-id="0586a-142">[Design Details: Code Examples of Changed Patterns in Modifications](design-details-code-examples-of-changed-patterns-in-modifications.md) </span></span>  
[<span data-ttu-id="0586a-143">Designdetails: Dimensionssatzposten</span><span class="sxs-lookup"><span data-stu-id="0586a-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   

