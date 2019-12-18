---
title: So sperren Sie Artikel vom Verkauf oder Einkauf
description: In Business Central kann ein Artikel als für Verkäufe, Einkäufe oder alle Verwendungszwecke gesperrt gekennzeichnet werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 12/04/2019
ms.author: sgroespe
ms.openlocfilehash: 0218cf1b4982b9e8c5b5c2817590bc5ebd8f1941
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896075"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="e7cab-103">Artikel vom Verkauf oder Einkauf sperren</span><span class="sxs-lookup"><span data-stu-id="e7cab-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="e7cab-104">Sie können einen Artikel sperren, damit er nicht auf Verkaufs- oder Einkaufszeilen eingetragen werden kann, und Sie können ihn sperren, damit er nicht in einer Transaktion gebucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="e7cab-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="e7cab-105">In der folgenden Tabelle wird veranschaulicht, was beim Sperren von Artikeln passiert.</span><span class="sxs-lookup"><span data-stu-id="e7cab-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="e7cab-106">Option</span><span class="sxs-lookup"><span data-stu-id="e7cab-106">Option</span></span>|<span data-ttu-id="e7cab-107">Description</span><span class="sxs-lookup"><span data-stu-id="e7cab-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="e7cab-108">**Vertrieb gesperrt**</span><span class="sxs-lookup"><span data-stu-id="e7cab-108">**Sales Blocked**</span></span>|<span data-ttu-id="e7cab-109">Der Artikel kann nicht in einem Verkaufsbeleg oder einem Erf.-Journal für Verkaufsartikel eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e7cab-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="e7cab-110">**Einkauf gesperrt**</span><span class="sxs-lookup"><span data-stu-id="e7cab-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="e7cab-111">Der Artikel kann nicht in einem Einkaufsbeleg, einem Erf.-Journal für Einkaufsartikel oder in Einkaufsplanungsprozessen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e7cab-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="e7cab-112">**Gesperrt**</span><span class="sxs-lookup"><span data-stu-id="e7cab-112">**Blocked**</span></span>|<span data-ttu-id="e7cab-113">Sie können diesen Artikel nicht für Artikeltransaktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7cab-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="e7cab-114">Blockierte Artikel können zurückgesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7cab-114">Blocked items can be returned.</span></span> <span data-ttu-id="e7cab-115">Das bedeutet, dass keine der obigen Einstellungen gilt, wenn der Artikel für Reklamationen und Gutschriften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7cab-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="e7cab-116">Wenn Sie die Funktion **Beleg kopieren** verwenden, um neue Belege auf der Grundlage vorhandener Belege zu erstellen, werden Sie benachrichtigt, wenn irgendwelche Elemente in den Quellbelegzeilen gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="e7cab-116">When you use the **Copy Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="e7cab-117">Die gesperrten Belegzeilen werden vom neuen Beleg ausgeschlossen, und eine Benachrichtigung zeigt eine Übersicht aller Belegzeilen, die im Quellbeleg gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="e7cab-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="e7cab-118">So sperren Sie einen Artikel vom Eintrag auf Verkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="e7cab-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="e7cab-119">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="e7cab-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e7cab-120">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Verkauf gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="e7cab-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="e7cab-121">Wenn Sie versuchen, den Artikel in einen Verkaufsbeleg oder eine Erf.-Journalzeile einzutragen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="e7cab-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="e7cab-122">So sperren Sie einen Artikel vom Eintrag auf Einkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="e7cab-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="e7cab-123">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="e7cab-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e7cab-124">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Einkauf gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="e7cab-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="e7cab-125">Wenn Sie versuchen, den Artikel in einen Einkaufsbeleg oder eine Erf.-Journalzeile einzutragen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="e7cab-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="e7cab-126">So sperren Sie einen Artikel vor der Buchung</span><span class="sxs-lookup"><span data-stu-id="e7cab-126">To block an item from being posted</span></span>
1. <span data-ttu-id="e7cab-127">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Elemente** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="e7cab-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="e7cab-128">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="e7cab-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="e7cab-129">Wenn Sie versuchen, irgendeine Transaktion für den Artikel zu buchen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="e7cab-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7cab-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7cab-130">See Also</span></span>  
[<span data-ttu-id="e7cab-131">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="e7cab-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="e7cab-132">Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="e7cab-132">Inventory</span></span>](inventory-manage-inventory.md)  
