---
title: Verwenden von Workflows | Microsoft Docs
description: Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.
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
ms.openlocfilehash: 6535523fb34504a4f964971f41d4803bdc7b2117
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304770"
---
# <a name="using-workflows"></a><span data-ttu-id="a1473-105">Verwenden von Workflows</span><span class="sxs-lookup"><span data-stu-id="a1473-105">Using Workflows</span></span>
<span data-ttu-id="a1473-106">Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden.</span><span class="sxs-lookup"><span data-stu-id="a1473-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="a1473-107">Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben.</span><span class="sxs-lookup"><span data-stu-id="a1473-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="a1473-108">Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.</span><span class="sxs-lookup"><span data-stu-id="a1473-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="a1473-109">Bevor Sie beginnen können, Workflows zu verwenden, müssen Sie Workflowbenutzer einrichten, die Workflows erstellen, möglicherweise Codeanpassung berücksichtigen und angeben, wie Benutzer Benachrichtigungen empfangen sollen.</span><span class="sxs-lookup"><span data-stu-id="a1473-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="a1473-110">Weitere Informationen erhalten Sie unter [Workflows einrichten](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="a1473-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a1473-111">Typische Workflowschritte drehen sich um Benutzer, die Genehmigungen für Aufgaben anfordern, und Genehmiger, die Genehmigungsanforderungen annehmen oder ablehen.</span><span class="sxs-lookup"><span data-stu-id="a1473-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="a1473-112">Daher beschäftigen sich viele Themen in Bezug auf die Verwendung von Workflows mit Genehmigungen.</span><span class="sxs-lookup"><span data-stu-id="a1473-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="a1473-113">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="a1473-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="a1473-114">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="a1473-114">**To**</span></span>|<span data-ttu-id="a1473-115">**Informationen**</span><span class="sxs-lookup"><span data-stu-id="a1473-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="a1473-116">Richten Sie einen Workflow ein, der gestartet wird, wenn das erste Einstiegspunktereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="a1473-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="a1473-117">Aktivieren von Workflows</span><span class="sxs-lookup"><span data-stu-id="a1473-117">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="a1473-118">Anforderung der Genehmigung einer Aufgabe, Akzeptieren oder Delegieren von Genehmigungen oder Ablehnen von Genehmigungen, und Senden oder Anzeigen von Genehmigungsbenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="a1473-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="a1473-119">Artikelgenehmigungsworkflow verwenden</span><span class="sxs-lookup"><span data-stu-id="a1473-119">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="a1473-120">Erstellen Sie Workflowschritte, die einen bestimmten Datensatztyp für die Verwendung vor einem bestimmten Ereignis einschränken (beispielsweise, bevor der Datensatz genehmigt wird).</span><span class="sxs-lookup"><span data-stu-id="a1473-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="a1473-121"> Zulassen und Einschränken des Verbrauchs eines Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="a1473-121">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="a1473-122">Zeigen Sie Workflowschrittinstanzen mit dem Status „Abgeschlossen“ an.</span><span class="sxs-lookup"><span data-stu-id="a1473-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="a1473-123">Anzeigen von archivierten Workflowschritt-Instanzen</span><span class="sxs-lookup"><span data-stu-id="a1473-123">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="a1473-124">Löschen Sie einen Workflow, den Sie mit Gewissheit nicht mehr verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="a1473-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="a1473-125">Löschen eines Workflows</span><span class="sxs-lookup"><span data-stu-id="a1473-125">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="a1473-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1473-126">See Also</span></span>  
<span data-ttu-id="a1473-127">[Einrichten von Workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="a1473-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="a1473-128">[Workflow](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="a1473-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="a1473-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a1473-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
