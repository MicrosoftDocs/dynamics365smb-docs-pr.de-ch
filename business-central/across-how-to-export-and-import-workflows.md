---
title: 'Vorgehensweise: Exportieren und Importieren von Workflows | Microsoft Docs'
description: Um Workflows auf andere Business Central-Datenbanken zu übertragen, beispielsweise um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Workflows exportiert und importiert werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4d11bc57066c0124bcb004894ed6b2c9dc4b812e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754781"
---
# <a name="export-and-import-workflows"></a>Exportieren und Importieren von Workflows
Um Workflows auf andere [!INCLUDE[prod_short](includes/prod_short.md)]-Datenbanken zu übertragen, beispielsweise um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Workflows exportiert und importiert werden.  

 Eine andere Art, Workflows schnell zu erstellen, besteht darin, Workflows aus Workflow-Vorlagen zu erstellen. Weitere Informationen finden Sie unter [Workflows von Workflow-Vorlagen erstellen](across-how-to-create-workflows-from-workflow-templates.md).  

 Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden. Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>So exportieren Sie ein Workflow  
1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Workflows** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie einen Workflow, und wählen die **In Datei exportieren** Aktion aus.  
3.  Klicken Sie auf der Seite **Datei exportieren** auf die Schaltfläche **Speichern**.  
4.  Wählen Sie auf der Seite **Exportieren** einen Dateistandort aus, und wählen Sie dann die Schaltfläche **Speichern** aus.  

## <a name="to-import-a-workflow"></a>So importieren Sie einen Workflow  
1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Workflows** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Importieren aus Datei** aus.  
3.  Wählen Sie auf der Seite **Importieren** die XML-Datei aus, die den Workflow enthält, und wählen Sie dann die Schaltfläche **Öffnen**.  

> [!CAUTION]  
>  Wenn der Workflowcode bereits in der Datenbank vorhanden ist, werden die Workflowschritte mit den Schritten im importierten Workflow überschrieben.  

## <a name="see-also"></a>Siehe auch  
 [Erstellen eines Workflows](across-how-to-create-workflows.md)   
 [Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md)   
 [Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md)   
 [Löschen eines Workflows](across-how-to-delete-workflows.md)   
 [Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Einrichten von Workflows](across-set-up-workflows.md)   
 [Verwenden von Workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]