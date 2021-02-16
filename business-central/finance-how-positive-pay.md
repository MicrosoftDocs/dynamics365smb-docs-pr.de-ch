---
title: Export von Positive Pay-Dateien| Microsoft Docs
description: Um sicherzustellen, dass Ihre Bank nur überprüfte Schecks und Beträge freigibt, können Sie ihr eine Positive Pay Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8856ee09ae728d685d3f57786abc29d9aca93778
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750869"
---
# <a name="export-a-positive-pay-file"></a><span data-ttu-id="d9dfa-103">Eine Positive Pay-Datei exportieren</span><span class="sxs-lookup"><span data-stu-id="d9dfa-103">Export a Positive Pay File</span></span>
<span data-ttu-id="d9dfa-104">Um sicherzustellen, dass eine Bank nur validierte Schecks und Beträge freigibt, können Sie eine Positive Pay-Datei exportieren, die die relevanten Zahlungsinformationen enthält wie Schecknummer und Zahlungsbetrag, die Sie als Referenz an die Bank senden, wenn Sie Zahlungen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-104">To make sure that your bank only clears validated checks and amounts, you can export a Positive Pay file that contains vendor information, check number, and payment amount, which you send to the bank for reference when you process payments.</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d9dfa-105">wird vorkonfiguriert, um Positive Pay-Dateien an die Bank of America und City Bank zu senden.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-105">is preconfigured to support Positive Pay files for Bank of America and City Bank.</span></span>

## <a name="to-set-up-a-bank-account-for-positive-pay"></a><span data-ttu-id="d9dfa-106">Um ein Bankkkonto für Positive Pay einzurichten</span><span class="sxs-lookup"><span data-stu-id="d9dfa-106">To set up a bank account for Positive Pay</span></span>
1. <span data-ttu-id="d9dfa-107">Wählen Sie die ![Glühbirne, die das Symbol Tell Me](media/ui-search/search_small.png "Tell Me-Funktion") öffnet, geben Sie **Bankkonten** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="d9dfa-108">Öffnen Sie die Karte des Bankkontos, für das Sie Positive Pay nutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-108">Open the card for the bank that you want to use Positive Pay for.</span></span>
3. <span data-ttu-id="d9dfa-109">In dem Feld **Positive Pay-Exportcode** geben Sie POSPAYBANK ein.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-109">In the **Positive Pay Export Code** field, enter POSPAYBANK.</span></span>
4. <span data-ttu-id="d9dfa-110">Schliessen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-110">Close the page.</span></span>

## <a name="to-export-a-positive-pay-file"></a><span data-ttu-id="d9dfa-111">Um eine Positive Pay-Datei zu exportieren</span><span class="sxs-lookup"><span data-stu-id="d9dfa-111">To export a Positive Pay file</span></span>
1. <span data-ttu-id="d9dfa-112">Wählen Sie die ![Glühbirne, die das Symbol Tell Me](media/ui-search/search_small.png "Tell Me-Funktion") öffnet, geben Sie **Bankkonten** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="d9dfa-113">Wählen Sie das Bankkonto aus, für das Sie eine Positive Pay-Datei exportieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-113">Select the bank account that you want to export a Positive Pay file for.</span></span>
3. <span data-ttu-id="d9dfa-114">Wählen Sie die Aktion **Positive Pay-Export** aus.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-114">Choose **Positive Pay Export** action.</span></span>

    <span data-ttu-id="d9dfa-115">Die Seite **Positive Pay-Export** wird geöffnet und zeigt Zahlungen an, die über das Bankkonto seit dem letzten Uploaddatum, wie in den Felder **Letztes Upload-Datum** **Letzte Upload-Zeit** angezeigt, geleistet wurden.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-115">The **Positive Pay Export** page opens displaying payments that have been made for the bank account since the last upload date, as shown in the **Last Upload Date** and **Last Upload Time** fields.</span></span>
4. <span data-ttu-id="d9dfa-116">Im Feld **Upload-Datum trennen** definieren Sie ein Datum, vor dem Zahlungen nicht in der exportierten Datei enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-116">In the **Cutoff Upload Date** field, specify a date before which payments are not included in the exported file.</span></span>
5. <span data-ttu-id="d9dfa-117">Wählen Sie die Aktion **Exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-117">Choose the **Export** action.</span></span>
6. <span data-ttu-id="d9dfa-118">Klicken Sie auf der Seite **Datei exportieren** auf die Schaltfläche **Speichern** und speichern Sie die Datei am gewünschten Speicherort.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-118">On the **Export File** page, choose the **Save** button, and then save the file to a convenient location.</span></span>
7. <span data-ttu-id="d9dfa-119">Laden Sie die Datei in Ihre elektronische Bankseite hoch.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-119">Upload the file to your electronic bank site.</span></span>
8. <span data-ttu-id="d9dfa-120">Schreiben oder kopieren Sie die Bestätigungsnummer, die angezeigt wird, wenn Sie die Datei erfolgreich hochgeladen haben.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-120">Write down or copy the confirmation number that is displayed when the file upload is successful.</span></span>

<span data-ttu-id="d9dfa-121">Um exportierte Positive Pay-Datensätze anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="d9dfa-121">To view exported Positive Pay records</span></span>

1. <span data-ttu-id="d9dfa-122">Wählen Sie die ![Glühbirne, die das Symbol Tell Me](media/ui-search/search_small.png "Tell Me-Funktion") öffnet, geben Sie **Bankkonten** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="d9dfa-123">Wählen Sie das Bankkonto aus, für das Sie einen Positive Pay-Datei-Export anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-123">Select the bank account that you want to view Positive Pay export records for.</span></span>
3. <span data-ttu-id="d9dfa-124">Wählen Sie die Aktion **Positive Pay-Einträge** aus.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-124">Choose the **Positive Pay Entries** action.</span></span>

    <span data-ttu-id="d9dfa-125">Auf der Seite **Positive Pay-Posten** können Sie alle Positive Pay-Exportdatensätze für das Bankkonto anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-125">On the **Positive Pay Entries** page, you can see all the Positive Pay export records for the bank account.</span></span>
4. <span data-ttu-id="d9dfa-126">Geben Sie im Feld **Bestätigungsnummer** für jeden Exportdatensatz die Bestätigungsnummer ein, die Sie gerade erhalten, wann der Dateiupload zur Bank ordnungsgemäss durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-126">In the **Confirmation Number** field, enter, for each export record, the confirmation number that you receive when the file upload to the bank is successful.</span></span>
5. <span data-ttu-id="d9dfa-127">Um die entsprechenden Zahlungszeilen anzuzeigen, wählen Sie die **Positive Pay-Postendetails** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-127">To view the related payment lines, choose the **Positive Pay Entry Details** action.</span></span>

<span data-ttu-id="d9dfa-128">Um Positive Pay-Dateien erneut zu exportieren</span><span class="sxs-lookup"><span data-stu-id="d9dfa-128">To reexport Positive Pay files</span></span>

1. <span data-ttu-id="d9dfa-129">Wählen Sie die ![Glühbirne, die das Symbol Tell Me](media/ui-search/search_small.png "Tell Me-Funktion") öffnet, geben Sie **Bankkonten** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-129">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="d9dfa-130">Wählen Sie das Bankkonto aus, für die Sie Positive Pay-Dateien erneut exportieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-130">Select the bank account that you want to reexport Positive Pay files for.</span></span>
3. <span data-ttu-id="d9dfa-131">Wählen Sie die Aktion **Positive Pay-Einträge** aus.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-131">Choose the **Positive Pay Entries** action.</span></span>
4. <span data-ttu-id="d9dfa-132">Wählen Sie die Zeile für die Positive Pay Exportdatei aus, die Sie erneut  exportieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-132">Select the line for the Positive Pay export file that you want to reexport.</span></span>
5. <span data-ttu-id="d9dfa-133">Auf der Seite **Positive Pay-Posten** wählen Sie die Aktion **Erneuter Positive Pay-Export in Datei** aus.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-133">On the **Positive Pay Entries** page, choose the **Reexport Positive Pay to File** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9dfa-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9dfa-134">See Also</span></span>
[<span data-ttu-id="d9dfa-135">Finanzen</span><span class="sxs-lookup"><span data-stu-id="d9dfa-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="d9dfa-136">Finanzen einrichten</span><span class="sxs-lookup"><span data-stu-id="d9dfa-136">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="d9dfa-137">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="d9dfa-137">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="d9dfa-138">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d9dfa-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
