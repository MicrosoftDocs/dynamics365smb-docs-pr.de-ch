---
title: Rückgängigmachen von Objekte als Web Services verfügbar | Microsoft Docs
description: Veröffentlichen Sie Objekte als Web Services, um sie sofort für Ihre Business Central-Lösung bereitzustellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 05/19/2020
ms.author: edupont
ms.openlocfilehash: 230f3a7fc11e19813d77da2ff15388433642c744
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697661"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="d58a0-103">Webdienst veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="d58a0-103">Publish a Web Service</span></span>

<span data-ttu-id="d58a0-104">Webdienste sind eine einfache Art, Anwendungsfunktionen für eine Vielzahl von externen Systemen und Benutzern zugänglich zu machen.</span><span class="sxs-lookup"><span data-stu-id="d58a0-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d58a0-105">enthält die Anzahl von Objekten, die als Webdienste standardmässig gegenüber die Integration anderer Microsoft-Dienstleistungen bereitgestellt werden, Sie können weitere Web Services hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d58a0-105">includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="d58a0-106">Sie richten im Internet einen Webdienst ein im [!INCLUDE[d365fin](includes/d365fin_md.md)] Client.</span><span class="sxs-lookup"><span data-stu-id="d58a0-106">You set up a web service in the [!INCLUDE[d365fin](includes/d365fin_md.md)] client.</span></span> <span data-ttu-id="d58a0-107">Sie müssen dann den Webdienst veröffentlichen, so dass er für Serviceanforderungen über das Netzwerk bereitsteht.</span><span class="sxs-lookup"><span data-stu-id="d58a0-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="d58a0-108">Benutzer können Webdienste erkennen, indem Sie auf einen Browser auf den Computer verweisen, der ausführt und eine Liste der verfügbaren Services anfordern.</span><span class="sxs-lookup"><span data-stu-id="d58a0-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="d58a0-109">Wenn Sie einen Webdienst veröffentlichen, ist er über das Netzwerk für authentifizierte Benutzer sofort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d58a0-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="d58a0-110">Alle autorisierten Benutzer können auf Metadaten für Webdienste zugreifen, aber nur Benutzer mit ausreichenden -Berechtigungen können auf tatsächliche Daten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d58a0-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="d58a0-111">Erstellen und Veröffentlichen eines Webdienstes</span><span class="sxs-lookup"><span data-stu-id="d58a0-111">Creating and Publishing a Web Service</span></span>

<span data-ttu-id="d58a0-112">Die folgenden Schritte erläutern, wie ein Webdienst erstellt und veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="d58a0-112">The following steps explain how to create and publish a web service.</span></span>  

<!--
    You can also create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] instead. Choose one of the following methods:

      - Use the **Create Data Set** action on the **Web Services** page
      - Use the **Set Up Reporting** Assisted Setup guide
      - Choose the **Edit in Excel** action in any lists
    -->

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="d58a0-113">So erstellen und veröffentlichen Sie einen Webdienst</span><span class="sxs-lookup"><span data-stu-id="d58a0-113">To create and publish a web service</span></span>  

1. <span data-ttu-id="d58a0-114">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Webdienste** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="d58a0-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d58a0-115">Wählen Sie auf der Seite **Webdienste** **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d58a0-115">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="d58a0-116">**Codeunit** und **Seite** sind gültige Arten für SOAP-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="d58a0-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="d58a0-117">**Seite** und **Abfrage** sind gültige Arten für OData-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="d58a0-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    > <span data-ttu-id="d58a0-118">Wenn die Datenbank mehrere Unternehmen enthält, können Sie eine Objekt-ID auswählen, die für eines der Unternehmen eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="d58a0-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="d58a0-119">Der Dienstname ist für Nutzer Ihres Webdiensts sichtbar und wird zum Identifizieren und Unterscheiden von Webdiensten verwendet, Sie sollten daher einen aussagefähigen Namen wählen.</span><span class="sxs-lookup"><span data-stu-id="d58a0-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="d58a0-120">Aktivieren Sie das Kontrollkästchen in der Spalte **Veröffentlicht**.</span><span class="sxs-lookup"><span data-stu-id="d58a0-120">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="d58a0-121">Wenn Sie den Webdienst veröffentlichen, sehen Sie in den Feldern **OData-URL** und **SOAP-URL** die URLs, die für den Webdienst erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="d58a0-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="d58a0-122">Sie können den Webdienst sofort testen, indem Sie die Links in den **OData-URL** und **SOAP-URL**-Feldern auswählen.</span><span class="sxs-lookup"><span data-stu-id="d58a0-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="d58a0-123">Optional können Sie den Wert des Felds kopieren und ihn für die spätere Verwendung speichern.</span><span class="sxs-lookup"><span data-stu-id="d58a0-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

> [!NOTE]
> <span data-ttu-id="d58a0-124">Wenn die als Webdienste bereitgestellten Objekt nicht online über [!INCLUDE[prodshort](includes/prodshort.md)] aufgerufen werden dürfen, müssen Sie die im Code verfügbaren Methoden als `[Scope('OnPrem')]` markieren.</span><span class="sxs-lookup"><span data-stu-id="d58a0-124">If the objects that you expose as web services must not be accessible from [!INCLUDE[prodshort](includes/prodshort.md)] online, you must mark the methods exposed in the code as `[Scope('OnPrem')]`.</span></span> <span data-ttu-id="d58a0-125">Weitere Informationen finden Sie unter [Bereichsattribut ](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span><span class="sxs-lookup"><span data-stu-id="d58a0-125">For more information, see [Scope Attribute](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span></span>

<span data-ttu-id="d58a0-126">Nachdem Sie einen Webdienst veröffentlichen, ist er für externe Seiten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d58a0-126">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="d58a0-127">Sie können die Verfügbarkeit dieses Webdienstes prüfen, indem Sie einen Browser verwenden, oder Sie können den Link in den **OData-URL** und **SOAP-URL** -Feldern auf der Seite **Webdienste** auswählen.</span><span class="sxs-lookup"><span data-stu-id="d58a0-127">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="d58a0-128">Im folgenden Verfahren wird gezeigt, wie Sie die Verfügbarkeit des Webdienstes für die spätere Verwendung prüfen können.</span><span class="sxs-lookup"><span data-stu-id="d58a0-128">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="d58a0-129">So prüfen Sie die Verfügbarkeit eines Webdienstes</span><span class="sxs-lookup"><span data-stu-id="d58a0-129">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="d58a0-130">Geben Sie in Ihrem Browser die entsprechende URL ein.</span><span class="sxs-lookup"><span data-stu-id="d58a0-130">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="d58a0-131">Die folgende Tabelle zeigt die Arten von URLs, die Sie für unterschiedliche Webservicearten eingeben können.</span><span class="sxs-lookup"><span data-stu-id="d58a0-131">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="d58a0-132">Art</span><span class="sxs-lookup"><span data-stu-id="d58a0-132">Type</span></span>|<span data-ttu-id="d58a0-133">Syntax</span><span class="sxs-lookup"><span data-stu-id="d58a0-133">Syntax</span></span>|<span data-ttu-id="d58a0-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d58a0-134">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="d58a0-135">SOAP</span><span class="sxs-lookup"><span data-stu-id="d58a0-135">SOAP</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="d58a0-136">OData-V4</span><span class="sxs-lookup"><span data-stu-id="d58a0-136">OData V4</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="d58a0-137">Das Feld „Unternehmensname“ berücksichtigt Gross-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="d58a0-137">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="d58a0-138">Überprüfen Sie die Informationen, die im Browser angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d58a0-138">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="d58a0-139">Vergewissern Sie sich, dass Sie den Namen des Webdienstes sehen, den Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="d58a0-139">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="d58a0-140">Wenn Sie auf einen Webdienst zugreifen und Daten wieder auf [!INCLUDE[d365fin](includes/d365fin_md.md)] schreiben möchten, müssen Sie den Firmennamen angeben.</span><span class="sxs-lookup"><span data-stu-id="d58a0-140">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="d58a0-141">Sie können den Mandanten als Teil des URI, wie in Beispielen angezeigt, angeben, oder Sie können den Mandanten als Teil der Abfrageparameter angeben.</span><span class="sxs-lookup"><span data-stu-id="d58a0-141">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="d58a0-142">Beispielsweise verweisen die folgenden URIs auf denselben OData-Webdienst, und beide sind gültige URIs.</span><span class="sxs-lookup"><span data-stu-id="d58a0-142">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="d58a0-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d58a0-143">See Also</span></span>

[<span data-ttu-id="d58a0-144">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d58a0-144">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="d58a0-145">Business Central-Web Services für Entwickler</span><span class="sxs-lookup"><span data-stu-id="d58a0-145">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[<span data-ttu-id="d58a0-146">OData-Anforderungslimits</span><span class="sxs-lookup"><span data-stu-id="d58a0-146">OData request limits</span></span>](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  
