---
title: So erstellen Sie Serviceofferten | Microsoft Docs
description: "Sie können das Fenster **Serviceofferte** verwenden, um Belege zu erstellen, in die Sie Informationen über den Service (Reparatur und Wartung) von Serviceartikeln auf Kundenanfrage eingeben. Serviceofferten können als Vorentwürfe von Serviceaufträgen betrachtet werden, die dann von der Offerte in einen Auftrag umgewandelt werden."
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
ms.openlocfilehash: 9d4f8d21d0c79adbac238b2d26accc4c08656c77
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="create-service-quotes"></a><span data-ttu-id="3b308-104">Serviceofferten erstellen</span><span class="sxs-lookup"><span data-stu-id="3b308-104">Create Service Quotes</span></span>
<span data-ttu-id="3b308-105">Sie können an Serviceofferten als Basis für Serviceaufträge denken.</span><span class="sxs-lookup"><span data-stu-id="3b308-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="3b308-106">Tatsächlich sind sie fast identisch.</span><span class="sxs-lookup"><span data-stu-id="3b308-106">In fact, they are almost identical.</span></span> <span data-ttu-id="3b308-107">Sie enthalten sowohl die Serviceartikelbeschreibung, wie der Debitor, die Art des Auftrags, den Artikel, für den Service, Gebührenzählung und benötigte Versandinformationen, und die Informationen über die tatsächliche Dienstarbeit.</span><span class="sxs-lookup"><span data-stu-id="3b308-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="3b308-108">Serviceofferten können als Vorentwürfe von Serviceaufträgen betrachtet werden, die dann von der Offerte in einen Auftrag umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="3b308-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="3b308-109">So erstellen Sie eine Serviceofferte</span><span class="sxs-lookup"><span data-stu-id="3b308-109">To create a service quote</span></span>  
1. <span data-ttu-id="3b308-110">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceofferten** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="3b308-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3b308-111">Erstellen Sie eine neue Serviceofferte.</span><span class="sxs-lookup"><span data-stu-id="3b308-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="3b308-112">Geben Sie im Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="3b308-112">In the **No.**</span></span> <span data-ttu-id="3b308-113">eine Nummer für die Serviceofferte ein.</span><span class="sxs-lookup"><span data-stu-id="3b308-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="3b308-114">Wenn Sie Nummernserien für Serviceofferten im Fenster **Service Einrichtung** definiert haben, drücken Sie die Eingabetaste, um die nächste verfügbare Serviceoffertennummer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3b308-114">Alternatively, if you have set up a number series for service quotes in the **Service Mgt. Setup** window, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="3b308-115">Klicken Sie im Feld **Debitorennr.**</span><span class="sxs-lookup"><span data-stu-id="3b308-115">In the **Customer No.**</span></span>  <span data-ttu-id="3b308-116">Feld wählen Sie den relevanten Debitoren aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="3b308-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="3b308-117">Die Debitorenfelder werden automatisch mit Informationen aus der Karte **Debitor** gefüllt.</span><span class="sxs-lookup"><span data-stu-id="3b308-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="3b308-118">Wenn keine **Debitor**-Karte für den Debitor vorhanden ist und Sie eine Debitorenvorlage eingerichtet haben, können Sie aus der Serviceofferte heraus einen Debitor erstellen.</span><span class="sxs-lookup"><span data-stu-id="3b308-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="3b308-119">Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **Kunde erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="3b308-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="3b308-120">Abhängig von den Einstellungen auf dem Inforegister **Pflichtfelder** im Fenster  **Service Einrichtung** muss das Feld **Serviceauftragsart** auf dem Inforegister **Verkäufercode** ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="3b308-120">Depending on the settings on the **Mandatory Fields** FastTab in the **Service Mgt. Setup** window, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="3b308-121">Füllen Sie die Serviceartikelzeilen aus.</span><span class="sxs-lookup"><span data-stu-id="3b308-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="3b308-122">Erfassen Sie die geschätzten Kosten in den Servicezeilen.</span><span class="sxs-lookup"><span data-stu-id="3b308-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b308-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b308-123">See Also</span></span>  
[<span data-ttu-id="3b308-124">Erstellen von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="3b308-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="3b308-125">Mit Serviceaufgaben arbeiten</span><span class="sxs-lookup"><span data-stu-id="3b308-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 
