---
title: So sperren Sie Artikel vom Verkauf oder Einkauf
description: Sie können verhindern, dass ein Artikel beispielsweise für Verkaufs- oder Einkaufsbelege verwendet wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 467b43b14f1905018c2a26a06c15abc5a0a17e99
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410658"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="aa6b5-103">Artikel vom Verkauf oder Einkauf sperren</span><span class="sxs-lookup"><span data-stu-id="aa6b5-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="aa6b5-104">Sie können einen Artikel sperren, damit er nicht in Zeilen von Verkaufs- oder Einkaufsbelegen eingegeben und in einer Transaktion nicht gebucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-104">You can block an item from being entered on lines in sales or purchase documents, and you can block it from being posted in any transaction.</span></span> <span data-ttu-id="aa6b5-105">Dies ist beispielsweise nützlich, wenn ein Artikel einen bekannten Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-105">For example, this is useful when an item has a known defect.</span></span> <span data-ttu-id="aa6b5-106">Wenn jemand in einem Verkaufs- oder Einkaufsbeleg einen gesperrten Artikel auswählt, wird er durch eine Nachricht darüber informiert, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-106">If someone chooses a blocked item on a sales or purchase document a message will inform them that the item is blocked.</span></span>

<span data-ttu-id="aa6b5-107">In der folgenden Tabelle wird beschrieben, was geschieht, wenn Artikel gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-107">The following table describes what occurs when items are blocked.</span></span>  

|<span data-ttu-id="aa6b5-108">Option</span><span class="sxs-lookup"><span data-stu-id="aa6b5-108">Option</span></span>|<span data-ttu-id="aa6b5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa6b5-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="aa6b5-110">**Vertrieb gesperrt**</span><span class="sxs-lookup"><span data-stu-id="aa6b5-110">**Sales Blocked**</span></span>|<span data-ttu-id="aa6b5-111">Der Artikel kann nicht in einem Verkaufsbeleg oder einem Erf.-Journal für Verkaufsartikel eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-111">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="aa6b5-112">**Einkauf gesperrt**</span><span class="sxs-lookup"><span data-stu-id="aa6b5-112">**Purchasing Blocked**</span></span>|<span data-ttu-id="aa6b5-113">Der Artikel kann nicht in einem Einkaufsbeleg, einem Erf.-Journal für Einkaufsartikel oder in Einkaufsplanungsprozessen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-113">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="aa6b5-114">**Gesperrt**</span><span class="sxs-lookup"><span data-stu-id="aa6b5-114">**Blocked**</span></span>|<span data-ttu-id="aa6b5-115">Sie können diesen Artikel nicht für Artikeltransaktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-115">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="aa6b5-116">Blockierte Artikel können zurückgesendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-116">Blocked items can be returned.</span></span> <span data-ttu-id="aa6b5-117">Das bedeutet, dass keine der obigen Einstellungen gilt, wenn der Artikel für Reklamationen und Gutschriften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-117">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="aa6b5-118">Wenn Sie die Funktion **Aus Beleg kopieren** verwenden, um neue Belege auf der Grundlage vorhandener Belege zu erstellen, werden Sie benachrichtigt, wenn Positionen in den Zeilen des Quellbelegs blockiert sind.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-118">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="aa6b5-119">Die gesperrten Belegzeilen werden vom neuen Beleg ausgeschlossen, und eine Benachrichtigung zeigt eine Übersicht aller Belegzeilen, die im Quellbeleg gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-119">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="aa6b5-120">So sperren Sie einen Artikel vom Eintrag auf Verkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="aa6b5-120">To block an item from being entered on sales lines</span></span>  
1.  <span data-ttu-id="aa6b5-121">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="aa6b5-122">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Verkauf gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-122">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="aa6b5-123">So sperren Sie einen Artikel vom Eintrag auf Einkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="aa6b5-123">To block an item from being entered on purchase lines</span></span>  
1.  <span data-ttu-id="aa6b5-124">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="aa6b5-125">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Einkauf gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-125">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="aa6b5-126">So sperren Sie einen Artikel vor der Buchung</span><span class="sxs-lookup"><span data-stu-id="aa6b5-126">To block an item from being posted</span></span>
1. <span data-ttu-id="aa6b5-127">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="aa6b5-128">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa6b5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa6b5-129">See Also</span></span>  
[<span data-ttu-id="aa6b5-130">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="aa6b5-130">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="aa6b5-131">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="aa6b5-131">Inventory</span></span>](inventory-manage-inventory.md)  
