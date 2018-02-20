---
title: 'Vorgehensweise: Workflows von Workflowvorlagen erstellen | Microsoft Docs'
description: "Um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: be25518b225b479d5db21b7014817743f28837bd
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="b92bb-103">Erstellen von Workflows aus Workflowvorlagen</span><span class="sxs-lookup"><span data-stu-id="b92bb-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="b92bb-104">Um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="b92bb-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="b92bb-105">Workflowvorlagen sind nicht-bearbeitbare Workflows, die Sie in der generischen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] finden.</span><span class="sxs-lookup"><span data-stu-id="b92bb-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="b92bb-106">Dem Code für von Microsoft hinzugefügte Workflowvorlagen ist „MS-“ vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="b92bb-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="b92bb-107">Eine andere Art, einen Workflow schnell zu erstellen ist es, einen vorhandenen Workflow zu importieren, den Sie in einer Datei ausserhalb von [!INCLUDE[d365fin](includes/d365fin_md.md)] haben.</span><span class="sxs-lookup"><span data-stu-id="b92bb-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="b92bb-108">Weitere Informationen finden Sie in [Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md)</span><span class="sxs-lookup"><span data-stu-id="b92bb-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="b92bb-109">Im Fenster **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten.</span><span class="sxs-lookup"><span data-stu-id="b92bb-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="b92bb-110">Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort.</span><span class="sxs-lookup"><span data-stu-id="b92bb-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="b92bb-111">Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b92bb-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="b92bb-112">Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="b92bb-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="b92bb-113">Vorgehensweise: Workflows von Workflowvorlagen erstellen</span><span class="sxs-lookup"><span data-stu-id="b92bb-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="b92bb-114">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Workflows** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="b92bb-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b92bb-115">Wählen Sie die Aktion **Workflow von Vorlage erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b92bb-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="b92bb-116">Das Fenster **Workflowvorlagen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b92bb-116">The **Workflow Templates** window opens.</span></span>  
3.  <span data-ttu-id="b92bb-117">Wählen Sie eine Workflowvorlage aus, und wählen Sie dann die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="b92bb-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="b92bb-118">Das Fenster **Workflow** wird für einen neuen Workflow geöffnet, der alle Informationen der ausgewählten Vorlage enthält.</span><span class="sxs-lookup"><span data-stu-id="b92bb-118">The **Workflow** window opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="b92bb-119">Der Wert im Feld **Code** wird beispielweise mit "-01 " erweitert. Dies zeigt an, dass dies der erste Workflow ist, der von der Workflowvorlage erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b92bb-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="b92bb-120">Fahren Sie fort mit dem Erstellen des Workflows, indem Sie die Workflowschritte bearbeiten oder neue Schritte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b92bb-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="b92bb-121">Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="b92bb-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="b92bb-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b92bb-122">See Also</span></span>  
 <span data-ttu-id="b92bb-123">[Erstellen eines Workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="b92bb-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="b92bb-124">[Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="b92bb-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="b92bb-125">[Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="b92bb-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="b92bb-126">[Löschen eines Workflows](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="b92bb-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="b92bb-127">[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="b92bb-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="b92bb-128">[Einrichten von Workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="b92bb-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="b92bb-129">[Verwenden von Workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="b92bb-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="b92bb-130">Workflow</span><span class="sxs-lookup"><span data-stu-id="b92bb-130">Workflow</span></span>](across-workflow.md)   

