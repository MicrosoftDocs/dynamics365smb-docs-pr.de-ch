---
title: 'Designdetails: Codeunit 408 Dimension Management | Microsoft Docs'
description: Codeunit 408 Dimension Management ist eine Funktionsbibliothek, die häufige Aufgaben im Zusammenhang mit Dimensionen behandelt, wie etwa das Kopieren von einer Tabelle zu einer anderen oder von einem Beleg zu einem anderen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-dimension-set-entries
ms.openlocfilehash: 1b0238fb26b71310b1f02e15be7d7040832ca644
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/16/2019
ms.locfileid: "938528"
---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="48ac4-103">Designdetails: Codeunit 408 Dimension Management</span><span class="sxs-lookup"><span data-stu-id="48ac4-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="48ac4-104">Codeunit 408 Dimension Management ist eine Funktionsbibliothek, die häufige Aufgaben im Zusammenhang mit Dimensionen behandelt, wie etwa das Kopieren von einer Tabelle zu einer anderen oder von einem Beleg zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="48ac4-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="48ac4-105">Dieses Thema listet die Funktionen auf, die in Microsoft Dynamics NAV 2013 R2 geändert werden und gibt an, was mit den Funktionen durchgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="48ac4-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="48ac4-106">Viele Funktionalitäten werden gelöscht, da ein Kopieren zwischen Dimensionstabellen nicht erforderlich gibt.</span><span class="sxs-lookup"><span data-stu-id="48ac4-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="48ac4-107">Geänderte Funktionen</span><span class="sxs-lookup"><span data-stu-id="48ac4-107">Modified Functions</span></span>  

|<span data-ttu-id="48ac4-108">Funktionsname</span><span class="sxs-lookup"><span data-stu-id="48ac4-108">Function Name</span></span>|<span data-ttu-id="48ac4-109">Modifizierungsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="48ac4-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="48ac4-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="48ac4-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="48ac4-111">Neue Funktion, die die anderen Scheckfunktionen ersetzt und nimmt eine Dimensionssatz-ID als ein Argument anstelle einer Dimensionstabelle.</span><span class="sxs-lookup"><span data-stu-id="48ac4-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="48ac4-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="48ac4-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="48ac4-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="48ac4-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="48ac4-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="48ac4-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="48ac4-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="48ac4-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="48ac4-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="48ac4-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="48ac4-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="48ac4-117">CheckDimValueComb</span></span>|<span data-ttu-id="48ac4-118">LÖSCHEN.</span><span class="sxs-lookup"><span data-stu-id="48ac4-118">Delete.</span></span> <span data-ttu-id="48ac4-119">Die gesamte Nutzung sollte zu CheckDimSetIDComb geändert werden.</span><span class="sxs-lookup"><span data-stu-id="48ac4-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="48ac4-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-120">GetDefaultDim</span></span>|<span data-ttu-id="48ac4-121">"Ändern", um eine ganzzahlige Dimensionssatz-ID anstelle eines Satzes von Datensätzen zurückzusenden.</span><span class="sxs-lookup"><span data-stu-id="48ac4-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="48ac4-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="48ac4-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="48ac4-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="48ac4-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="48ac4-126">Ändern, um mit DimSetID zu arbeiten - > ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="48ac4-127">Gelöschte Funktionen</span><span class="sxs-lookup"><span data-stu-id="48ac4-127">Deleted Functions</span></span>  
 <span data-ttu-id="48ac4-128">Funktionen, die aus Codeunit 408 in Verbindung mit den Dimensionssatzposten gelöscht werden, werden unten aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="48ac4-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="48ac4-129">Während des Upgrades des Anwendungscodes von Microsoft Dynamics NAV 2009 oder früheren Versionen zu Microsoft Dynamics NAV 2016 sind die folgenden Funktionen nicht in Microsoft Dynamics NAV 2016 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="48ac4-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="48ac4-130">Wenn Sie Anpassungen haben, die einen oder mehrere der Funktionalitäten verwenden, müssen Sie diesen Code entsprechend aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="48ac4-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="48ac4-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="48ac4-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="48ac4-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="48ac4-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="48ac4-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="48ac4-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-136">InsertDocDim</span></span>  

 <span data-ttu-id="48ac4-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="48ac4-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="48ac4-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="48ac4-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="48ac4-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-141">InsertServContractDim</span></span>  

 <span data-ttu-id="48ac4-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="48ac4-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="48ac4-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="48ac4-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-144">GetDocDim</span></span>  

 <span data-ttu-id="48ac4-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-145">GetProdDocDim</span></span>  

 <span data-ttu-id="48ac4-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="48ac4-146">TypeToTableID1</span></span>  

 <span data-ttu-id="48ac4-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="48ac4-147">TypeToTableID2</span></span>  

 <span data-ttu-id="48ac4-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="48ac4-148">TypeToTableID3</span></span>  

 <span data-ttu-id="48ac4-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="48ac4-149">TypeToTableID4</span></span>  

 <span data-ttu-id="48ac4-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="48ac4-150">TypeToTableID5</span></span>  

 <span data-ttu-id="48ac4-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="48ac4-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-152">DeleteDocDim</span></span>  

 <span data-ttu-id="48ac4-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="48ac4-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="48ac4-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="48ac4-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="48ac4-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="48ac4-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="48ac4-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="48ac4-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-160">ShowDocDim</span></span>  

 <span data-ttu-id="48ac4-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-161">SaveDocDim</span></span>  

 <span data-ttu-id="48ac4-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="48ac4-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="48ac4-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-164">ShowTempDim</span></span>  

 <span data-ttu-id="48ac4-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-165">SaveTempDim</span></span>  

 <span data-ttu-id="48ac4-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="48ac4-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="48ac4-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-168">SaveServContractDim</span></span>  

 <span data-ttu-id="48ac4-169">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="48ac4-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="48ac4-171">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="48ac4-172">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="48ac4-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="48ac4-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="48ac4-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="48ac4-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="48ac4-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="48ac4-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="48ac4-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="48ac4-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="48ac4-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="48ac4-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="48ac4-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="48ac4-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="48ac4-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="48ac4-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="48ac4-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="48ac4-188">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="48ac4-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="48ac4-190">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="48ac4-191">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="48ac4-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="48ac4-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="48ac4-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="48ac4-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="48ac4-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="48ac4-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="48ac4-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="48ac4-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="48ac4-198">TestDimValue</span></span>  

 <span data-ttu-id="48ac4-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="48ac4-199">TestNewDimValue</span></span>  

 <span data-ttu-id="48ac4-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="48ac4-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="48ac4-201">(Löschen, da die ItemBudgetDim-Tabelle gelöscht ist.)</span><span class="sxs-lookup"><span data-stu-id="48ac4-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="48ac4-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-202">GetServContractDim</span></span>  

 <span data-ttu-id="48ac4-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="48ac4-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="48ac4-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="48ac4-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="48ac4-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="48ac4-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="48ac4-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="48ac4-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="48ac4-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48ac4-207">See Also</span></span>
 <span data-ttu-id="48ac4-208">[Designdetails: Dimensionssatzposten](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="48ac4-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="48ac4-209">[Designdetails: Dimensionssatzposten Übersicht](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="48ac4-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="48ac4-210">[Designdetails: Suche nach Dimensionskombinationen](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="48ac4-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="48ac4-211">[Designdetails: Tabellenstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="48ac4-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="48ac4-212">Designdetails: Codebeispiele von geänderten Mustern in Änderungen</span><span class="sxs-lookup"><span data-stu-id="48ac4-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
