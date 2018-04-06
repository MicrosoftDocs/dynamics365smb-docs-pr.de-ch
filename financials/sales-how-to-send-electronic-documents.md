---
title: Senden Sie elektronische Belege | Microsoft Docs
description: Erfahren Sie, wie man Rechnungen elektronisch sendet.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fae5e37b8f1fcca84a474b2eac2039f7fc6d8245
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="send-electronic-documents"></a><span data-ttu-id="ce880-103">Elektronische Belege senden</span><span class="sxs-lookup"><span data-stu-id="ce880-103">Send Electronic Documents</span></span>
<span data-ttu-id="ce880-104">Die allgemeine Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt das Senden von elektronischen Rechnungen und Gutschriften im PEPPOL-Format, das von den grössten Anbietern von Belegaustauschdiensten unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ce880-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="ce880-105">Ein Anbieter von Belegaustauschdiensten leitet elektronische Belege zwischen Handelspartnern weiter.</span><span class="sxs-lookup"><span data-stu-id="ce880-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="ce880-106">Um Unterstützung für andere elektronische Belegformate zu bieten, verwenden Sie das Datenaustauschframework.</span><span class="sxs-lookup"><span data-stu-id="ce880-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="ce880-107">In der allgemeinen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] ist ein vorkonfigurierter Belegaustauschdienst enthalten, der für Ihren Mandanten eingerichtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce880-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="ce880-108">Weitere Informationen finden Sie unter [Belegaustausch-Dienst](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="ce880-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="ce880-109">Um eine Verkaufsrechnung als elektronischen PEPPOL-Beleg zu senden, wählen Sie die Option **Elektronischer Beleg** im Dialogfeld **Buchen und Senden** aus. Hier können Sie auch das standardmässige Belegsendeprofil für den Debitor einrichten.</span><span class="sxs-lookup"><span data-stu-id="ce880-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="ce880-110">Zuerst müssen Sie verschiedene Stammdaten einrichten, zum Beispiel Mandantendaten, Debitoren, Artikel und Masseinheiten.</span><span class="sxs-lookup"><span data-stu-id="ce880-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="ce880-111">Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Feldern in [Einrichten von Senden und Empfangen von elektronischen Dokumenten](across-how-to-set-up-electronic-document-sending-and-receiving.md)in Elemente in der ausgehenden Dokumentdatei konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="ce880-111">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="ce880-112">So senden Sie eine elektronische Verkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="ce880-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="ce880-113">Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsrechnung** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="ce880-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="ce880-114">Erstellen Sie eine neue Verkaufsrechnung.</span><span class="sxs-lookup"><span data-stu-id="ce880-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="ce880-115">Wenn die Verkaufsrechnung fakturiert werden kann, wählen Sie auf der Registerkarte **Aktionen** in der Gruppe **Buchung** die Option **Buchen und Senden** aus.</span><span class="sxs-lookup"><span data-stu-id="ce880-115">When the sales invoice is ready to be invoiced, on the **Actions** tab, in the **Posting** group, choose **Post and Send**.</span></span>  

     <span data-ttu-id="ce880-116">Wenn das Standardsendeprofil des Debitors **Elektronischer Beleg** lautet, wird es im Dialogfeld **Buchungs- und Sendebestätigung** angezeigt, und Sie müssen nur die Schaltfläche **Ja** auswählen, um die Rechnung im ausgewählten Format elektronisch zu buchen und zu senden.</span><span class="sxs-lookup"><span data-stu-id="ce880-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="ce880-117">Wählen Sie im Dialogfeld **Buchungs- und Sendebestätigung** die AssistEdit-Schaltfläche rechts vom Feld **Beleg senden an** aus.</span><span class="sxs-lookup"><span data-stu-id="ce880-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="ce880-118">Wählen Sie im Dialgofeld **Beleg senden an** im Feld **Elektronischer Beleg** die Option **Über Belegaustauschdienst** aus.</span><span class="sxs-lookup"><span data-stu-id="ce880-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="ce880-119">Wählen Sie im Feld **Format** die Option **PEPPOL** aus.</span><span class="sxs-lookup"><span data-stu-id="ce880-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="ce880-120">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ce880-120">Choose the **OK** button.</span></span> <span data-ttu-id="ce880-121">Das Dialogfeld **Buchungs- und Sendebestätigung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce880-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="ce880-122">**Elektronischer Beleg (PEPPOL)** wird im Feld **Beleg senden an** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ce880-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="ce880-123">Wählen Sie die Schaltfläche **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="ce880-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="ce880-124">Die Verkaufsrechnung wird gebucht und als elektronischer Beleg im PEPPOL-Format an den Debitor gesendet.</span><span class="sxs-lookup"><span data-stu-id="ce880-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ce880-125">Sie können auch eine gebuchte Verkaufsrechnung als elektronischen Beleg senden.</span><span class="sxs-lookup"><span data-stu-id="ce880-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="ce880-126">Dieser Vorgang ist derselbe wie im Thema für nicht gebuchte Verkaufsbelege beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ce880-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="ce880-127">Aktivieren Sie im Fenster **Gebuchte Verkaufsrechung** auf der Registerkarte **Aktionen** in der Gruppe **Allgemein** die Option **Aktivitätsprotokoll**, um den Status des elektronischen Belegs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ce880-127">In the **Posted Sales Invoice** window, on the **Actions** tab, in the **General** group, choose **Activity Log** to view the status of the electronic document.</span></span> <span data-ttu-id="ce880-128">Weitere Informationen finden Sie unter **Aktivitätsprotokoll**</span><span class="sxs-lookup"><span data-stu-id="ce880-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce880-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce880-129">See Also</span></span>  
[<span data-ttu-id="ce880-130">Verkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="ce880-130">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="ce880-131">Belegsendeprofile einrichten</span><span class="sxs-lookup"><span data-stu-id="ce880-131">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="ce880-132">Einrichten des Senden und Empfangen von elektronischen Belegen</span><span class="sxs-lookup"><span data-stu-id="ce880-132">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="ce880-133">So richten Sie einen Belegaustauschdienst ein</span><span class="sxs-lookup"><span data-stu-id="ce880-133">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="ce880-134">Richten Sie Datenaustauschdefinitionen ein.</span><span class="sxs-lookup"><span data-stu-id="ce880-134">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="ce880-135">Daten elektronisch austauschen</span><span class="sxs-lookup"><span data-stu-id="ce880-135">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="ce880-136">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ce880-136">General Business Functionality</span></span>](ui-across-business-areas.md)  

