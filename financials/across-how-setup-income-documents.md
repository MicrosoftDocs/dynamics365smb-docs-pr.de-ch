---
title: Einrichten von eingehenden Belegen| Microsoft Docs
description: Verwenden Sie die Funktion der eingehenden Belege, um elektronische Belege zu erstellen, verwalten Sie OCRaufgaben, importieren Sie Rechnungen und wandeln Sie Bilddateien um.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 69cb1037da2f3873ecb9a3f498ce5fadfeabac1d
ms.contentlocale: de-ch
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-incoming-documents"></a><span data-ttu-id="10e36-103">Gewusst wie: Eingehende Belege einrichten</span><span class="sxs-lookup"><span data-stu-id="10e36-103">How to: Set Up Incoming Documents</span></span>
<span data-ttu-id="10e36-104">Wenn Sie Fibu Erfassungsjournalzeilen für eingehende Belegdatensätze erstellen, müssen Sie im Fenster **Einrichtung für eingehende Belege** angeben, welche Erfassungsjournalvorlage und welches Erfassungsjournal verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="10e36-104">If you create general journal lines from incoming document records, you must specify in the **Incoming Documents Setup** window which journal template and batch to use.</span></span>

<span data-ttu-id="10e36-105">Wenn Sie nicht möchten, dass Benutzer Rechnungen oder Fibu Erfassungsjournalzeilen anhand von eingehende Belegdatensätzen erstellen können, ausser, wenn diese genehmigt sind, müssen Sie Genehmiger im Fenster **Genehmiger für eingehenden Beleg** einrichten.</span><span class="sxs-lookup"><span data-stu-id="10e36-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers in the **Incoming Document Approvers** window.</span></span>

<span data-ttu-id="10e36-106">Um PDF und Bilddateien in elektronische Dokumente umzuwandeln, die in Dokumentdatensätze in Project '[!INCLUDE[d365fin](includes/d365fin_md.md)]' konvertiert werden, müssen Sie die OCR-Funktion einrichten und den Dienst aktivieren.</span><span class="sxs-lookup"><span data-stu-id="10e36-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="10e36-107">Wenn die Funktion für Eingangsbelege eingerichtet ist, können Sie verschiedene Funktionen zum Überprüfen von Ausgabenbelegen, Verwalten von OCR-Aufgaben und Konvertieren von Eingangsbelegen, manuell oder automatisch, in den entsprechenden Belegen oder Buch.-Blattzeilen verwenden.</span><span class="sxs-lookup"><span data-stu-id="10e36-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="10e36-108">Die externen Dateien können jeder Prozessphase zugeordnet werden, auch gebuchten Belegen und den resultierenden Kreditoren-, Debitoren- und Sachposten.</span><span class="sxs-lookup"><span data-stu-id="10e36-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="10e36-109">Weitere Informationen finden Sie unter [Eingehende Dokumente verarbeiten](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="10e36-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="10e36-110">So richten Sie die Funktion für Eingangsbelege ein</span><span class="sxs-lookup"><span data-stu-id="10e36-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="10e36-111">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png " Nach Seite oder Bericht suchen")und geben **Einrichtung für eingehende Dokumente** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="10e36-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="10e36-112">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="10e36-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="10e36-113">So richten Sie Genehmiger für Eingangsbelege ein</span><span class="sxs-lookup"><span data-stu-id="10e36-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="10e36-114">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png " Nach Seite oder Bericht suchen")und geben **Einrichtung für eingehende Dokumente** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="10e36-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="10e36-115">Wählen Sie im Fenster **Einrichtung für eingehende Belege** die Aktion **Genehmiger** aus.</span><span class="sxs-lookup"><span data-stu-id="10e36-115">In the **Incoming Documents Setup** window, choose the **Approvers** action.</span></span>

    <span data-ttu-id="10e36-116">Im Fenster **Genehmiger für eingehendes Dokument** werden alle Benutzer, die in Ihrem Project '[!INCLUDE[d365fin](includes/d365fin_md.md)]* eingerichtet sind, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="10e36-116">The **Incoming Document Approvers** window shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="10e36-117">Wählen Sie mindestens einen Benutzer aus, der einen eingehenden Beleg genehmigen kann, bevor eine zugehörige Beleg- oder Erf.-Journalzeile erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="10e36-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="10e36-118">Nachdem Sie Genehmiger im Fenster **Genehmiger für eingehenden Beleg** eingerichtet haben, können nur diese Benutzer einen eingehenden Beleg genehmigen, wenn im Fenster **Einrichtung für eingehende Belege** das Kontrollkästchen **Genehmigung zum Erstellen anfordern** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="10e36-118">When approvers have been set up in the **Incoming Document Approvers** window, only those users can approve an incoming document if the **Require Approval To Create** check box in the **Incoming Documents Setup** window is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="10e36-119">Diese Genehmigungseinrichtung ist nicht mit den Genehmigungsworkflows verknüpft.</span><span class="sxs-lookup"><span data-stu-id="10e36-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="10e36-120">Weitere Informationen erhalten Sie unter [So gehts: Genehmigungsworkflow verwenden](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="10e36-120">For more information, see [How to: Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="10e36-121">So richten Sie einen OCR-Service ein</span><span class="sxs-lookup"><span data-stu-id="10e36-121">To set up an OCR service</span></span>
1. <span data-ttu-id="10e36-122">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **OCR-Dienst einrichten** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="10e36-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="10e36-123">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="10e36-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a><span data-ttu-id="10e36-124">So verschlüsseln Sie Ihre Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="10e36-124">To encrypt your login information</span></span>
<span data-ttu-id="10e36-125">Es wird empfohlen, dass Sie die Anmeldeinformationen, die Sie im Fenster **OCR-Dienst einrichten** eingeben, schützen.</span><span class="sxs-lookup"><span data-stu-id="10e36-125">It is recommended that you protect the logon information that you enter in the **OCR Service Setup** window.</span></span> <span data-ttu-id="10e36-126">Sie können Daten auf dem Server verschlüsseln, indem Sie neue Verschlüsselungsschlüssel erstellen oder vorhandene importieren, die Sie auf der Serverinstanz aktivieren, die mit der Datenbank verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="10e36-126">You can encrypt data on the server by generating new or importing existing encryption keys that you enable on the server instance that connects to the database.</span></span>

1. <span data-ttu-id="10e36-127">Wählen Sie im Fenster **OCR-Dienst einrichten** die Aktion **Verschlüsselungsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="10e36-127">In the **OCR Service Setup** window, choose the **Encryption Management** action.</span></span>
2. <span data-ttu-id="10e36-128">Aktivieren Sie im Fenster **Datenverschlüsselungsverwaltung** die Verschlüsselung der Daten.</span><span class="sxs-lookup"><span data-stu-id="10e36-128">In the **Data Encryption Management** window, enable encryption of your data.</span></span>

## <a name="see-also"></a><span data-ttu-id="10e36-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10e36-129">See Also</span></span>
[<span data-ttu-id="10e36-130">Eingehende Dokumente verarbeiten</span><span class="sxs-lookup"><span data-stu-id="10e36-130">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="10e36-131">Eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="10e36-131">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="10e36-132">Einkauf</span><span class="sxs-lookup"><span data-stu-id="10e36-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="10e36-133">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="10e36-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

