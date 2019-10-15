---
title: Artikelreferenzen verwenden | Microsoft Docs
description: Wenn Sie eine Artikelreferenzen zwischen der Artikelbeschreibung definieren, die Sie für den Artikel und die Beschreibung verwenden, die der Kreditor dieses Artikels verwendet, wird die Artikelbeschreibung des Kreditors automatisch auf Verkaufsbelegen für den Kreditor eingegeben, wenn Sie die **Referenznr.** ausfüllen Feld
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
ms.openlocfilehash: 8f7c409759716e741edfe1a352ff81da9fdea0db
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309666"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="39f75-104">Artikelreferenzen verwenden</span><span class="sxs-lookup"><span data-stu-id="39f75-104">Use Item Cross References</span></span>
<span data-ttu-id="39f75-105">Wenn Sie eine Artikelreferenzen zwischen der Artikelbeschreibung definieren, die Sie für den Artikel und die Beschreibung verwenden, die der Kreditor dieses Artikels verwendet, wird die Artikelbeschreibung des Kreditors automatisch auf Verkaufsbelegen für den Kreditor eingegeben, wenn Sie die **Referenznr.** ausfüllen</span><span class="sxs-lookup"><span data-stu-id="39f75-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="39f75-106">Feld</span><span class="sxs-lookup"><span data-stu-id="39f75-106">field.</span></span> <span data-ttu-id="39f75-107">Dieselbe Funktionalität gilt für Debitorenartikelnummern in Verkaufsbelegen.</span><span class="sxs-lookup"><span data-stu-id="39f75-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="39f75-108">Die folgenden Verfahren beschreiben, wie Artikelreferenzen beim Einkauf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39f75-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="39f75-109">Die Schritte sind für den Verkauf ähnlich.</span><span class="sxs-lookup"><span data-stu-id="39f75-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="39f75-110">Eine Artikelreferenz zur Artikelbeschreibung des Kreditor einrichten</span><span class="sxs-lookup"><span data-stu-id="39f75-110">To set up an item cross reference to a vendor's item description</span></span>
1. <span data-ttu-id="39f75-111">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren?“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="39f75-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="39f75-112">Öffnen Sie die Karte eines Artikels, für den Sie eine Referenz zur Artikelbeschreibung erstellen möchten, die der Kreditor für diesen Artikel verwendet.</span><span class="sxs-lookup"><span data-stu-id="39f75-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="39f75-113">Wählen Sie die **Referenzen**-Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="39f75-113">Choose the **Cross References** action.</span></span>
4. <span data-ttu-id="39f75-114">In einer neuen Zeile auf der Seite **Artikelreferenzposten** füllen Sie die Felder wie notwendig aus.</span><span class="sxs-lookup"><span data-stu-id="39f75-114">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="39f75-115">.</span><span class="sxs-lookup"><span data-stu-id="39f75-115">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="39f75-116">So geben Sie die Artikelbeschreibung eines Kreditors auf einer Einkaufsbestellung ein</span><span class="sxs-lookup"><span data-stu-id="39f75-116">To enter a vendor's item description on a purchase order</span></span>
1. <span data-ttu-id="39f75-117">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufaufträge** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="39f75-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="39f75-118">Erstellen Sie eine Bestellung für den Kreditor, für den Sie im vorherigen Verfahren eine Artikelreferenz eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="39f75-118">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="39f75-119">Erstellen Sie eine Einkaufszeile für den Artikel, für den Sie im vorherigen Verfahren eine Artikelreferenz eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="39f75-119">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="39f75-120">Wählen Sie im Feld **Referenznr.**</span><span class="sxs-lookup"><span data-stu-id="39f75-120">In the **Cross-Reference No.**</span></span> <span data-ttu-id="39f75-121">die Artikelreferenz aus, die Sie erstellt haben, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="39f75-121">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="39f75-122">Das Feld **Beschreibung** in der Zeile wird mit der Artikelbeschreibung des Kreditors überschrieben, wie im Artikelreferenzposten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="39f75-122">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="39f75-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39f75-123">See Also</span></span>
[<span data-ttu-id="39f75-124">Neue Artikel registrieren</span><span class="sxs-lookup"><span data-stu-id="39f75-124">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="39f75-125">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="39f75-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="39f75-126">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39f75-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
