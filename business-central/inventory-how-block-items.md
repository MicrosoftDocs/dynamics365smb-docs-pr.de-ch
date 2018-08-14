---
title: So sperren Sie Artikel vom Verkauf oder Einkauf
description: "In Business Central kann ein Artikel als für Verkäufe, Einkäufe oder alle Verwendungszwecke gesperrt gekennzeichnet werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: c6f10f8252c00bf0a599f9fa794ee36c41ce92be
ms.openlocfilehash: 2f8be478dda62fef2cb34397de488f45d4fcfc0c
ms.contentlocale: de-ch
ms.lasthandoff: 07/30/2018

---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="0aa86-103">Artikel vom Verkauf oder Einkauf sperren</span><span class="sxs-lookup"><span data-stu-id="0aa86-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="0aa86-104">Sie können einen Artikel sperren, damit er nicht auf Verkaufs- oder Einkaufszeilen eingetragen werden kann, und Sie können ihn sperren, damit er nicht in einer Transaktion gebucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="0aa86-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="0aa86-105">In der folgenden Tabelle wird veranschaulicht, was beim Sperren von Artikeln passiert.</span><span class="sxs-lookup"><span data-stu-id="0aa86-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="0aa86-106">Option</span><span class="sxs-lookup"><span data-stu-id="0aa86-106">Option</span></span>|<span data-ttu-id="0aa86-107">Description</span><span class="sxs-lookup"><span data-stu-id="0aa86-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="0aa86-108">**Vertrieb gesperrt**</span><span class="sxs-lookup"><span data-stu-id="0aa86-108">**Sales Blocked**</span></span>|<span data-ttu-id="0aa86-109">Der Artikel kann nicht in einem Verkaufsbeleg oder einem Erf.-Journal für Verkaufsartikel eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0aa86-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="0aa86-110">**Einkauf gesperrt**</span><span class="sxs-lookup"><span data-stu-id="0aa86-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="0aa86-111">Der Artikel kann nicht in einem Einkaufsbeleg, einem Erf.-Journal für Einkaufsartikel oder in Einkaufsplanungsprozessen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0aa86-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="0aa86-112">**Gesperrt**</span><span class="sxs-lookup"><span data-stu-id="0aa86-112">**Blocked**</span></span>|<span data-ttu-id="0aa86-113">Der Artikel kann für keine Artikeltransaktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0aa86-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="0aa86-114">Weitere Informationen zum Sperren eines Artikels für alle Zwecke erhalten Sie unter "Artikelkarte".</span><span class="sxs-lookup"><span data-stu-id="0aa86-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="0aa86-115">So sperren Sie einen Artikel vom Eintrag auf Verkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="0aa86-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="0aa86-116">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="0aa86-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0aa86-117">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Verkauf gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="0aa86-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="0aa86-118">Wenn Sie versuchen, den Artikel in ein Verkaufsdokument oder eine Erf.-Journalzeile einzutragen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="0aa86-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="0aa86-119">So sperren Sie einen Artikel vom Eintrag auf Einkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="0aa86-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="0aa86-120">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="0aa86-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0aa86-121">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Einkauf gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="0aa86-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="0aa86-122">Wenn Sie versuchen, den Artikel in ein Einkaufsdokument oder eine Erf.-Journalzeile einzutragen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="0aa86-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="0aa86-123">So sperren Sie einen Artikel vor der Buchung</span><span class="sxs-lookup"><span data-stu-id="0aa86-123">To block an item from being posted</span></span>
1. <span data-ttu-id="0aa86-124">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="0aa86-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="0aa86-125">Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Gesperrt** aus.</span><span class="sxs-lookup"><span data-stu-id="0aa86-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="0aa86-126">Wenn Sie versuchen, irgendeine Transaktion für den Artikel zu buchen, erhalten Sie jetzt eine Fehlermeldung, dass der Artikel gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="0aa86-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="0aa86-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0aa86-127">See Also</span></span>  
[<span data-ttu-id="0aa86-128">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="0aa86-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="0aa86-129">Lagerbesttand</span><span class="sxs-lookup"><span data-stu-id="0aa86-129">Inventory</span></span>](inventory-manage-inventory.md)  

