---
title: So erstellen Sie Serviceofferten | Microsoft Docs
description: Sie können die Seite **Serviceofferte** verwenden, um Belege zu erstellen, in die Sie Informationen über den Service (Reparatur und Wartung) von Serviceartikeln auf Debitorenanfrage eingeben. Serviceofferten können als Vorentwürfe von Serviceaufträgen betrachtet werden, die dann von der Offerte in einen Auftrag umgewandelt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 26b250a6c902e70bd4badf712d620f835d4ebb5a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784448"
---
# <a name="create-service-quotes"></a><span data-ttu-id="9dd9a-104">Serviceofferten erstellen</span><span class="sxs-lookup"><span data-stu-id="9dd9a-104">Create Service Quotes</span></span>
<span data-ttu-id="9dd9a-105">Sie können an Serviceofferten als Basis für Serviceaufträge denken.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="9dd9a-106">Tatsächlich sind sie fast identisch.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-106">In fact, they are almost identical.</span></span> <span data-ttu-id="9dd9a-107">Sie enthalten sowohl die Serviceartikelbeschreibung, wie der Debitor, die Art des Auftrags, den Artikel, für den Service, Gebührenzählung und benötigte Versandinformationen, und die Informationen über die tatsächliche Dienstarbeit.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="9dd9a-108">Serviceofferten können als Vorentwürfe von Serviceaufträgen betrachtet werden, die dann von der Offerte in einen Auftrag umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="9dd9a-109">So erstellen Sie eine Serviceofferte</span><span class="sxs-lookup"><span data-stu-id="9dd9a-109">To create a service quote</span></span>  
1. <span data-ttu-id="9dd9a-110">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Serviceofferten** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9dd9a-111">Erstellen Sie eine neue Serviceofferte.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="9dd9a-112">Geben Sie im Feld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="9dd9a-112">In the **No.**</span></span> <span data-ttu-id="9dd9a-113">eine Nummer für die Serviceofferte ein.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="9dd9a-114">Wenn Sie Nummernserien für Serviceofferten auf der Seite **Service Einrichtung** definiert haben, drücken Sie die Eingabetaste, um die nächste verfügbare Serviceoffertennummer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-114">Alternatively, if you have set up a number series for service quotes on the **Service Mgt. Setup** page, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="9dd9a-115">Klicken Sie im Feld **Debitorennr.**</span><span class="sxs-lookup"><span data-stu-id="9dd9a-115">In the **Customer No.**</span></span>  <span data-ttu-id="9dd9a-116">Feld wählen Sie den relevanten Debitoren aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="9dd9a-117">Die Debitorenfelder werden automatisch mit Informationen aus der Karte **Debitor** gefüllt.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="9dd9a-118">Wenn keine **Debitor**-Karte für den Debitor vorhanden ist und Sie eine Debitorenvorlage eingerichtet haben, können Sie aus der Serviceofferte heraus einen Debitor erstellen.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="9dd9a-119">Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **Debitor erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="9dd9a-120">Abhängig von den Einstellungen auf dem Inforegister **Pflichtfelder** auf der Seite **Service Einrichtung** muss das Feld **Serviceauftragsart** auf dem Inforegister **Verkäufercode** ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-120">Depending on the settings on the **Mandatory Fields** FastTab on the **Service Mgt. Setup** page, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="9dd9a-121">Füllen Sie die Serviceartikelzeilen aus.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="9dd9a-122">Erfassen Sie die geschätzten Kosten in den Servicezeilen.</span><span class="sxs-lookup"><span data-stu-id="9dd9a-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9dd9a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dd9a-123">See Also</span></span>  
[<span data-ttu-id="9dd9a-124">Erstellen von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="9dd9a-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="9dd9a-125">Mit Serviceaufgaben arbeiten</span><span class="sxs-lookup"><span data-stu-id="9dd9a-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 