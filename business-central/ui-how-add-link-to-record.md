---
title: "Vorgehensweise: Verknüpfung von Datensätzen zu externen Informationen oder Programmen | Microsoft Docs"
description: "Fügen Sie einem Dokument oder einer Website einen Link zu einem bestimmten Datensatz hinzu, beispielsweise zu einer Debitorenkarte oder einem Dokument."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 8927d2ca670b3faa38cd03ea10ae524e595721ad
ms.contentlocale: de-ch
ms.lasthandoff: 11/26/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="374e1-103">Hinzufügen von Links zu Websites, Belegen oder Programmen auf Datensätze</span><span class="sxs-lookup"><span data-stu-id="374e1-103">Adding Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="374e1-104">An einem bestimmten Datensatz, beispielsweise einem Debitoren Beleg oder Verkaufsauftrag, können Sie einen Link einem externen Beleg, einer Website oder einer Anwendung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="374e1-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="374e1-105">Möglicherweise möchten Sie einen Link einrichten, durch den eine neue leere E-Mail an einen bestimmten Empfänger geöffnet wird, wenn darauf geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="374e1-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="374e1-106">Die Kartenseite für einige Einträge wie Debitoren- und Kreditorenkarten beinhalten ein Feld mit der Bezeichnung **Homepage**, in dem eine URL eingegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="374e1-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="374e1-107">Wenn Sie andere Links einbeziehen möchten, können Sie die Methode verwenden, die in diesem Artikel beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="374e1-107">To include other links, you can use the method described in this article.</span></span>

<span data-ttu-id="374e1-108">Ein anderes Beispiel könnte sein, wenn Sie gedruckte Rechnungen von Kreditoren erhalten.</span><span class="sxs-lookup"><span data-stu-id="374e1-108">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="374e1-109">Sie können diese durchsuchen und als .pdf Datei auf einer SharePoint-Site speichern.</span><span class="sxs-lookup"><span data-stu-id="374e1-109">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="374e1-110">Anschliessend kann eine Einkaufsrechnung in  [!INCLUDE[d365fin_md](includes/d365fin_md.md)] mit der entsprechenden Rechnung im SharePoint Server verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="374e1-110">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="374e1-111">Zudem besteht die Möglichkeit, eine Artikelkarte mit der entsprechenden Seite im Onlinekatalog des Kreditors zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="374e1-111">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="374e1-112">Um einen Link aus einem Datensatz zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="374e1-112">To add a link on a record</span></span>   

1.  <span data-ttu-id="374e1-113">Öffnen Sie den Datensatz, dem Sie den Link zuordnen möchten (beispielsweise Debitorenkarte oder Verkaufsauftrag).</span><span class="sxs-lookup"><span data-stu-id="374e1-113">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="374e1-114">Wenn Sie den Link einer bestimmten Zeile (beispielsweise eine Erf.-Journalzeile) zuordnen möchten, wählen Sie die Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="374e1-114">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="374e1-115">Wählen Sie die **Links** Aktion aus, um die **Links** Seiten zu öffnen, die alle aktuellen und Links anzeigt, die dem Datensatz hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="374e1-115">Choose the **Links** action to open the **Links** pages that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="374e1-116">Um neue Benutzer zu erstellen, wählen Sie **+Neu**.</span><span class="sxs-lookup"><span data-stu-id="374e1-116">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="374e1-117">Geben Sie im Feld **Link Adresse** ein</span><span class="sxs-lookup"><span data-stu-id="374e1-117">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="374e1-118">Um eine Datei auf dem Computer oder dem Netzwerk zu verknüpfen, geben Sie den vollständigen Pfad und den Dateinamen, wie **C:My Documentsinvoice1.doc** ein.</span><span class="sxs-lookup"><span data-stu-id="374e1-118">To link to a file on your computer or network, enter the full path and file name, such as  **C:My Documentsinvoice1.doc**.</span></span>
    -   <span data-ttu-id="374e1-119">Um auf die Website zu verknüpfen, geben Sie die Internetadresse (URL), wie **www.microsoft.com** ein.</span><span class="sxs-lookup"><span data-stu-id="374e1-119">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="374e1-120">Um auf die Website zu verknüpfen, geben Sie die Internetadresse (URL), wie **www.microsoft.com** ein.</span><span class="sxs-lookup"><span data-stu-id="374e1-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="374e1-121">Um eine Anwendung zu verknüpfen, Sie geben eine bestimmte Zeichenfolge ein, um die Anwendung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="374e1-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="374e1-122">Zum Beispiel, um OneNote mit einer bestimmten Seite zu öffnen, geben Sie **onenote:///C:\Eigene Dateien\test.one** ein.</span><span class="sxs-lookup"><span data-stu-id="374e1-122">For example, to open OneNote with a specific page, enter **onenote:///C:My Documentstest.one**.</span></span> <span data-ttu-id="374e1-123">Um Outlook mit einer neuen leeren E-Mail an en bestimmtes Alias zu öffnen, geben Sie **mailto:testalias** ein.</span><span class="sxs-lookup"><span data-stu-id="374e1-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="374e1-124">Geben Sie in das Feld **Beschreibung** Informationen zu dem Link ein.</span><span class="sxs-lookup"><span data-stu-id="374e1-124">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="374e1-125">Klicken Sie auf die Schaltfläche **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="374e1-125">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="374e1-126">So entfernen Sie einen Link aus einem Datensatz:</span><span class="sxs-lookup"><span data-stu-id="374e1-126">To delete a link from a record</span></span>  

<span data-ttu-id="374e1-127">Um einen Link auf der Seite **Links** zu deaktivieren, können Sie auf **…** und anschliessend **Löschen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="374e1-127">To delete a link, on the **Links** page, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="374e1-128">Wenn Sie einen einzelnen Datensatz (z. B. eine Verkaufszeile, einen Verkaufsauftrag oder eine Debitorenkarte) löschen, werden alle Links gelöscht, die dem Datensatz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="374e1-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="374e1-129">Wenn Datensätze dagegen mit einer Stapelverarbeitung gelöscht werden wie **Verrechneter Verkaufsauftrag löschen** Stapelverarbeitung, dann wird der Link in der Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="374e1-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="374e1-130">Wenn Sie diese Links aus der Datenbank löschen möchten, führen Sie die Codeunit **Nicht verbundene Datensatzverknüpfungen löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="374e1-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="374e1-131">Wählen Sie dazu das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben **Nicht verbundene Datensatzverknüpfungen löschen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="374e1-131">To do this, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="374e1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="374e1-132">See Also</span></span>  
<span data-ttu-id="374e1-133">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="374e1-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

