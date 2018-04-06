---
title: Daten mithilfe von Flow verbinden| Microsoft Docs
description: "Sie können Ihre Finanzdaten als Datenquelle zur Verfügung stellen und eine OData-URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe einem automatisierten Workflow erstellen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: dde99e50c6984a7ec162b4047e8640e6affb3f25
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="ca1ba-103">[!INCLUDE[d365fin](includes/d365fin_md.md)]in einem automatisierten Workflow nutzen</span><span class="sxs-lookup"><span data-stu-id="ca1ba-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="ca1ba-104">Sie können die Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Teil eines Workflows in Microsoft-Flow verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="ca1ba-105">Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] und Flow haben.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="ca1ba-106">Um [!INCLUDE[d365fin](includes/d365fin_md.md)] als Datenquelle in Flow hinzufügen</span><span class="sxs-lookup"><span data-stu-id="ca1ba-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="ca1ba-107">In Ihrem Browser navigieren Sie zu [flow.microsoft.com](https://flow.microsoft.com/en-us/) und melden sich dann an.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="ca1ba-108">Wählen Sie **My Flows** im Menüband oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="ca1ba-109">Im Fenster **My Flows** wählen Sie die Option **Aus Leer erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="ca1ba-110">Aus der Liste der verfügbaren Triggern, wählen Sie einen der [!INCLUDE[d365fin](includes/d365fin_md.md)] verfügbaren Trigger aus:</span><span class="sxs-lookup"><span data-stu-id="ca1ba-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="ca1ba-111">*Die Genehmigung für einen Debitor wird angefordert*,</span><span class="sxs-lookup"><span data-stu-id="ca1ba-111">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="ca1ba-112">*Genehmigung von Fibu Erf.-Journalname wird angefordert*,</span><span class="sxs-lookup"><span data-stu-id="ca1ba-112">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="ca1ba-113">*Genehmigung von Fibu Erf.-Journalzeile wird angefordert*,</span><span class="sxs-lookup"><span data-stu-id="ca1ba-113">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="ca1ba-114">*Die Genehmigung für einen Artikel wird angefordert*,</span><span class="sxs-lookup"><span data-stu-id="ca1ba-114">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="ca1ba-115">*Die Genehmigung für einen Einkaufsbeleg wird angefordert*,</span><span class="sxs-lookup"><span data-stu-id="ca1ba-115">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="ca1ba-116">*Die Genehmigung für einen Verkaufsbeleg wird angefordert* oder</span><span class="sxs-lookup"><span data-stu-id="ca1ba-116">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="ca1ba-117">*Die Genehmigung für einen Kreditor wird angefordert*.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-117">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="ca1ba-118">Flow fordert Sie auf, den Mandanten innerhalb Ihres Tenants [!INCLUDE[d365fin](includes/d365fin_md.md)] auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-118">Flow will prompt you to select a company within your [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant.</span></span> <span data-ttu-id="ca1ba-119">Da jede Schritt im Flow unabhängig vom darauffolgenden ist, werden Sie möglicherweise aufgefordert, den Mandanten mehrmals zu definieren, wenn Sie eine Vorlage [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-119">Because each step in the Flow is independent of the next, you may be required to define the company multiple times when using a [!INCLUDE[d365fin](includes/d365fin_md.md)] template.</span></span>

<span data-ttu-id="ca1ba-120">Zu diesem Zeitpunkt haben Sie erfolgreich Ihre Finance and Operations, Business edition-Daten verbunden und sind bereit, Ihren Flow zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-120">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="ca1ba-121">Weitere Informationen finden Sie in der [Flow Dokumentation](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="ca1ba-121">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="ca1ba-122">Bei Problemen mit Microsoft Flow siehe [Problembehandlung Integration mit Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="ca1ba-122">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ca1ba-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca1ba-123">See Also</span></span>
<span data-ttu-id="ca1ba-124">[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="ca1ba-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="ca1ba-125">Geschäftsdaten aus anderen Finanzsystemen migrieren</span><span class="sxs-lookup"><span data-stu-id="ca1ba-125">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="ca1ba-126">[Benutzer und ihre Berechtigungen verwalten.](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="ca1ba-126">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="ca1ba-127">[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="ca1ba-127">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="ca1ba-128">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ca1ba-128">Finance</span></span>](finance.md)  

