---
title: "Vorgehensweise: Einrichten von Codes für Standardservices | Microsoft Docs"
description: "Erfahren Sie, wie Codes für Dienstaktivitäten eingerichtet werden, die Sie häufig ausführen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2d617fa06ea18d6e74f473600020f14d8f286d98
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-standard-service-codes"></a><span data-ttu-id="87d6f-103">Standardservicecodes einrichten</span><span class="sxs-lookup"><span data-stu-id="87d6f-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="87d6f-104">Bei der Durchführung eines normalen Service müssen häufig Servicebelege erstellt werden, die Servicezeilen mit ähnlichen Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="87d6f-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="87d6f-105">Um dies Zeilen einfach zu erstellen, können Sie Standardservicecodes einrichten, die einen vordefinierten Satz Servicezeilen haben.</span><span class="sxs-lookup"><span data-stu-id="87d6f-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="87d6f-106">Wenn Sie den Code in einem Verkaufsbeleg auswählen, werden die Zeilen automatisch eingegeben.</span><span class="sxs-lookup"><span data-stu-id="87d6f-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="87d6f-107">Mit jedem Servicecode kann eine unbegrenzte Anzahl Servicezeilen verschiedener Arten, Artikel, Ressourcen, Kosten oder Standardtexten verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="87d6f-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="87d6f-108">Für jeden Standardservicecode können Servicezeilen im Fenster **Standard-Servicecodkarte** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="87d6f-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="87d6f-109">Sie können dann die Standardservicecodes Servicecodeartikelgruppen zuweisen im Fenster **Standardservicecodes Serviceartikelgruppen**.</span><span class="sxs-lookup"><span data-stu-id="87d6f-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="87d6f-110">Wenn Sie später einen Servicebeleg erstellen, können Sie die **Standardservicecodes abrufen** Aktion verwenden, um Servicezeilen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="87d6f-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="87d6f-111">Sie können das gleive Vorgehen verwenden, um Zeilen in Verkaufs- und Einkaufsbelegen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="87d6f-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="87d6f-112">Weitere Informationen finden Sie unter [Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="87d6f-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="87d6f-113">So richten Sie einen Standardservicecode ein</span><span class="sxs-lookup"><span data-stu-id="87d6f-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="87d6f-114">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Standardservicecode** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="87d6f-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87d6f-115">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="87d6f-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="87d6f-116">Füllen Sie die Servicezeilen aus, die mit diesem Servicecode verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="87d6f-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="87d6f-117">So weisen Sie einer Serviceartikelgruppe einen Standardservicecode zu</span><span class="sxs-lookup"><span data-stu-id="87d6f-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="87d6f-118">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceartikelgruppen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="87d6f-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87d6f-119">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="87d6f-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="87d6f-120">Füllen Sie die Servicezeilen aus, die mit diesem Servicecode verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="87d6f-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="87d6f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87d6f-121">See Also</span></span>
[<span data-ttu-id="87d6f-122">Service</span><span class="sxs-lookup"><span data-stu-id="87d6f-122">Service Management</span></span>](service-service.md)
