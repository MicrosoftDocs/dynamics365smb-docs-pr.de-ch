---
title: Suche nach Belegen ohne Dateianhänge| Microsoft Docs
Description: Sie können nach Fibuposten für gebuchte Einkaufs- und Verkaufsbelege suchen, die keine eingehenden elektronische Belege haben, wie importierte Rechnungen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: e1b5c2b5e2615e5051a410c88b5e972036b0d98e
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780574"
---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="6b02b-103">So finden Sie gebuchte Belege ohne zugehörige eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="6b02b-103">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="6b02b-104">Auf der Seiten **Kontenplan** und **Fibuposten** können Sie eine Suchfunktion verwenden, um Fibuposten für gebuchte Einkaufs- und Verkaufsbelege zu finden, für die keine eingehende Belegdatensätze vorhanden sind, und dann zentral eine Verknüpfung zu vorhandenen Datensätzen herstellen oder neue mit angefügten Belegdateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b02b-104">From the **Chart of Accounts** and **General Ledger Entries** pages, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="6b02b-105">So finden Sie gebuchte Belege ohne zugehörige eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="6b02b-105">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="6b02b-106">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="6b02b-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="6b02b-107">Wählen Sie eine Zeile für ein Fibukonto aus, für dessen Fibuposten Sie gebuchte Einkaufs- und Verkaufsbelege abrufen möchten, zu denen keine eingehenden Belege vorhanden sind, und wählen Sie dann die Aktion **Gebuchte Belege ohne eingehenden Beleg**.</span><span class="sxs-lookup"><span data-stu-id="6b02b-107">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="6b02b-108">Alternativ wählen Sie die Aktion **Posten** aus.</span><span class="sxs-lookup"><span data-stu-id="6b02b-108">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="6b02b-109">Wählen Sie auf der Seite **Fibuposten** die Aktion **Gebuchte Belege ohne eingehende Belege** aus.</span><span class="sxs-lookup"><span data-stu-id="6b02b-109">On the **General Ledger Entries** page, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="6b02b-110">Daraufhin wird die Seite **Gebuchte Belege ohne eingehenden Beleg** geöffnet, das die gebuchten Einkaufs- und Verkaufsbelege ohne zugehörige eingehende Belege enthält, die von Fibuposten auf dem Fibukonto dargestellt werden, für das Sie das Fenster geöffnet haben.</span><span class="sxs-lookup"><span data-stu-id="6b02b-110">The **Posted Documents without Incoming Document** page opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the page for.</span></span> <span data-ttu-id="6b02b-111">Die Seite kann maximal 1000 Zeilen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6b02b-111">The page can show a maximum of 1000 lines.</span></span> <span data-ttu-id="6b02b-112">Standardmässig enthält das Feld **Datumsfilter** daher einen Filter, der die Anzeige auf Einträge beschränkt, deren Buchungsdatum zwischen dem Beginn der Buchhaltungsperiode und dem Arbeitsdatum liegt.</span><span class="sxs-lookup"><span data-stu-id="6b02b-112">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="6b02b-113">So verknüpfen Sie gefundene Belege mit vorhandenen eingehenden Belegen</span><span class="sxs-lookup"><span data-stu-id="6b02b-113">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="6b02b-114">Wählen Sie auf der Seite **Gebuchte Belege ohne eingehenden Beleg** die Zeile für einen gebuchten Beleg aus, den Sie mit einem vorhandenen eingehenden Beleg verknüpfen möchten, und wählen Sie dann die Aktion **Eingehenden Beleg auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="6b02b-114">On the **Posted Documents without Incoming Document** page, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="6b02b-115">Wählen Sie auf der Seite **Eingehende Belege** den eingehenden Beleg aus, den Sie der gefundenen Buchung zuordnen möchten, und klicken Sie anschliessend auf die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b02b-115">On the **Incoming Documents** page, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="6b02b-116">Auf der Seite **Gebuchte Belege ohne eingehenden Beleg** wird der gewählte eingehende Beleg nun mit dem gebuchten Beleg verknüpft und in der Infobox **Eingehende Belegdateien** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6b02b-116">On the **Posted Documents without Incoming Document** page, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="6b02b-117">Wenn die Seite **Eingehende Belege** keinen relevanten Datensatz für einen eingehenden Beleg enthält, können Sie einen erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b02b-117">If a relevant incoming document record does not exist on the **Incoming Documents** page, then you can create it.</span></span> <span data-ttu-id="6b02b-118">Weitere Informationen finden Sie unter [So geht's: Eingehende Belege erstellen](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="6b02b-118">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6b02b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b02b-119">See Also</span></span>
[<span data-ttu-id="6b02b-120">Eingehende Belege verarbeiten</span><span class="sxs-lookup"><span data-stu-id="6b02b-120">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="6b02b-121">Eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="6b02b-121">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="6b02b-122">Einkauf</span><span class="sxs-lookup"><span data-stu-id="6b02b-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6b02b-123">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6b02b-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
