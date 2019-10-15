---
title: Mehrere Verträge | Microsoft Docs
description: Abhängig von den Servicelevelvereinbarungen mit dem Kunden, kann es sein, dass Sie einen Serviceartikel in mehr als einem Servicevertrag berücksichtigen müssen.
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
ms.openlocfilehash: ccb677f128262435427f819ba0c24da254e3ce5c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315962"
---
# <a name="multiple-contracts"></a><span data-ttu-id="0e020-103">Mehrere Verträge</span><span class="sxs-lookup"><span data-stu-id="0e020-103">Multiple Contracts</span></span>
<span data-ttu-id="0e020-104">Abhängig von den Servicelevelvereinbarungen mit dem Kunden, kann es sein, dass Sie einen Serviceartikel in mehr als einem Servicevertrag berücksichtigen müssen.</span><span class="sxs-lookup"><span data-stu-id="0e020-104">Depending on your service level agreements with a customer, you may have to handle a service item under more than one service contract.</span></span>  
  
<span data-ttu-id="0e020-105">Wenn Sie einen Serviceartikel in mehreren Serviceverträgen berücksichtigen, können Sie folgendermassen vorgehen:</span><span class="sxs-lookup"><span data-stu-id="0e020-105">By handling a service item under multiple contracts, you can do the following:</span></span>  
  
* <span data-ttu-id="0e020-106">Verschiedene Verträge für denselben Serviceartikel ausstellen.</span><span class="sxs-lookup"><span data-stu-id="0e020-106">Issue different contracts for the same service item.</span></span>  
* <span data-ttu-id="0e020-107">Separaten Service für Teile leisten.</span><span class="sxs-lookup"><span data-stu-id="0e020-107">Service parts separately.</span></span>  
* <span data-ttu-id="0e020-108">Berücksichtigen, dass verschiedene Teile des Serviceartikels, wie z. B. mechanische Komponenten und Software, unterschiedliche Qualifikationen für die Serviceerbringung benötigen.</span><span class="sxs-lookup"><span data-stu-id="0e020-108">Consider different skills that are required to service different aspects of a service item, such as mechanical components and software.</span></span>  
* <span data-ttu-id="0e020-109">Verschiedene Reaktionszeiten und Serviceintervalle für verschiedene Teile des Serviceartikels vereinbaren.</span><span class="sxs-lookup"><span data-stu-id="0e020-109">Specify different response times and frequencies in servicing different parts of a service item.</span></span>  
* <span data-ttu-id="0e020-110">Verschiedene Serviceleistungen berücksichtigen, die an einem Serviceartikel ausgeführt werden müssen, wenn dieser verschiedene Arten von Serviceleistungen in verschiedenen Zeitintervallen benötigt.</span><span class="sxs-lookup"><span data-stu-id="0e020-110">Address different kinds of activities to be performed on a service item when the service item requires different types of service in different time periods.</span></span>  
* <span data-ttu-id="0e020-111">Einer Serviceartikelzeile eine geeignete Vertragsnummer zuordnen, wenn Sie einen Servicevertrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e020-111">Select and assign an appropriate contract number to a service item line when you are creating a service order.</span></span>  
* <span data-ttu-id="0e020-112">Relevante Finanzdaten zu Serviceartikeln und Servicelevelvereinbarungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="0e020-112">Handle relevant financial information about service items and service level agreements.</span></span>  
  
<span data-ttu-id="0e020-113">Die folgenden Beispiele zeigen den Verwendungszweck der Funktionalität "Mehrere Verträge".</span><span class="sxs-lookup"><span data-stu-id="0e020-113">You can consider the following examples of using the multiple contracts functionality.</span></span>  
  
## <a name="creating-multiple-contracts-per-service-item"></a><span data-ttu-id="0e020-114">Erstellen von mehreren Verträgen pro Serviceartikel</span><span class="sxs-lookup"><span data-stu-id="0e020-114">Creating Multiple Contracts per Service Item</span></span>  
<span data-ttu-id="0e020-115">Sie können manuell einen Servicevertrag oder eine Servicevertragsofferte für Serviceartikel erstellen, die bereits in ungekündigten Verträgen mit demselben Kunden enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0e020-115">You can manually create a service contract or contract quote for service items already registered in non-canceled contracts owned by the same customer.</span></span> <span data-ttu-id="0e020-116">Wenden Sie dazu die Standardvorgehensweise zur Erstellung eines Servicevertrags oder einer Servicevertragsofferte an.</span><span class="sxs-lookup"><span data-stu-id="0e020-116">To do this, follow the standard procedure of creating service contracts and service contract quotes.</span></span> <span data-ttu-id="0e020-117">Weitere Informationen finden Sie unter [Arbeiten mit Serviceverträgen und Servicevertragsofferten](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span><span class="sxs-lookup"><span data-stu-id="0e020-117">For more information, see [Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span></span>  
  
<span data-ttu-id="0e020-118">Wenn Sie einen Serviceartikel einer Vertragszeile hinzufügen, der bereits in einem anderen Servicevertrag oder einem anderen Servicevertragsangebot enthalten ist, erscheint eine Warnung, dass der Serviceartikel bereits zu einem oder mehreren Serviceverträgen oder Vertragsangeboten gehört.</span><span class="sxs-lookup"><span data-stu-id="0e020-118">When you add a service item on a contract line that is registered in other service contracts or contract quotes, a warning message is displayed stating that the service item already belongs to one or more service contracts or contract quotes.</span></span> <span data-ttu-id="0e020-119">Wenn Sie diese Warnung bestätigen, werden alle entsprechenden Serviceartikeldaten in eine neue Servicevertragszeile kopiert.</span><span class="sxs-lookup"><span data-stu-id="0e020-119">If you confirm this message, all relevant service item information is copied to a newly created contract line.</span></span>  
  
## <a name="copying-documents"></a><span data-ttu-id="0e020-120">Belege kopieren</span><span class="sxs-lookup"><span data-stu-id="0e020-120">Copying Documents</span></span>  
<span data-ttu-id="0e020-121">Sie können einen Servicevertrag oder eine Vertragsofferte für einen Serviceartikel automatisch erstellen, der bereits in einem anderen Servicevertrag oder einer Vertragsofferte enthalten ist, indem Sie die Funktion **Beleg kopieren** verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e020-121">You can automatically create a service contract or contract quote for service items that are already registered in other service contracts or contract quotes by using the **Copy Document** action.</span></span>  
  
## <a name="creating-service-orders-for-multiple-contracts"></a><span data-ttu-id="0e020-122">Erstellen von Serviceaufträgen für mehrere Verträge</span><span class="sxs-lookup"><span data-stu-id="0e020-122">Creating Service Orders for Multiple Contracts</span></span>  
<span data-ttu-id="0e020-123">Sie können manuell einen Serviceauftrag für einen Serviceartikel, der in mehreren aktiven Verträgen hinterlegt ist, erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e020-123">You can manually create a service order for a service item that is registered in multiple active contracts.</span></span> <span data-ttu-id="0e020-124">Ein Servicevertrag ist aktiv, wenn er unterzeichnet und nicht abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="0e020-124">A service contract is active when it is signed and not expired.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e020-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e020-125">See Also</span></span>  
[<span data-ttu-id="0e020-126">Erfüllen von Serviceverträgen</span><span class="sxs-lookup"><span data-stu-id="0e020-126">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)  
[<span data-ttu-id="0e020-127">Erstellen von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="0e020-127">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
