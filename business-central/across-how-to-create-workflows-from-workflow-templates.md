---
title: 'Vorgehensweise: Workflows von Workflowvorlagen erstellen | Microsoft Docs'
description: "Um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 2a8da1e1f06a4556ebdfac28e5fe27adf169a7eb
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="e0a2a-103">Erstellen von Workflows aus Workflowvorlagen</span><span class="sxs-lookup"><span data-stu-id="e0a2a-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="e0a2a-104">Um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="e0a2a-105">Workflowvorlagen sind nicht-bearbeitbare Workflows, die Sie in der generischen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] finden.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e0a2a-106">Dem Code für von Microsoft hinzugefügte Workflowvorlagen ist „MS-“ vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="e0a2a-107">Eine andere Art, einen Workflow schnell zu erstellen ist es, einen vorhandenen Workflow zu importieren, den Sie in einer Datei ausserhalb von [!INCLUDE[d365fin](includes/d365fin_md.md)] haben.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e0a2a-108">Weitere Informationen finden Sie in [Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md)</span><span class="sxs-lookup"><span data-stu-id="e0a2a-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="e0a2a-109">Im Fenster **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="e0a2a-110">Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="e0a2a-111">Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="e0a2a-112">Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="e0a2a-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="e0a2a-113">Vorgehensweise: Workflows von Workflowvorlagen erstellen</span><span class="sxs-lookup"><span data-stu-id="e0a2a-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="e0a2a-114">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Workflows** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e0a2a-115">Wählen Sie die Aktion **Workflow von Vorlage erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="e0a2a-116">Das Fenster **Workflowvorlagen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-116">The **Workflow Templates** window opens.</span></span>  
3.  <span data-ttu-id="e0a2a-117">Wählen Sie eine Workflowvorlage aus, und wählen Sie dann die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="e0a2a-118">Das Fenster **Workflow** wird für einen neuen Workflow geöffnet, der alle Informationen der ausgewählten Vorlage enthält.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-118">The **Workflow** window opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="e0a2a-119">Der Wert im Feld **Code** wird beispielweise mit "-01 " erweitert. Dies zeigt an, dass dies der erste Workflow ist, der von der Workflowvorlage erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="e0a2a-120">Fahren Sie fort mit dem Erstellen des Workflows, indem Sie die Workflowschritte bearbeiten oder neue Schritte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e0a2a-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="e0a2a-121">Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="e0a2a-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="e0a2a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0a2a-122">See Also</span></span>  
 <span data-ttu-id="e0a2a-123">[Erstellen eines Workflows](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e0a2a-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="e0a2a-124">[Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e0a2a-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="e0a2a-125">[Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="e0a2a-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="e0a2a-126">[Löschen eines Workflows](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e0a2a-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="e0a2a-127">[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="e0a2a-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="e0a2a-128">[Einrichten von Workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e0a2a-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="e0a2a-129">[Verwenden von Workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e0a2a-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="e0a2a-130">Workflow</span><span class="sxs-lookup"><span data-stu-id="e0a2a-130">Workflow</span></span>](across-workflow.md)   

