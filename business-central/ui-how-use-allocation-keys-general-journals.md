---
title: Verwenden von Umlageschlüsseln in Fibu Erf.-Journals | Microsoft Docs
description: Erfahren Sie, wie Sie Verteilungsschlüssel in Buch.-Blättern verwenden können.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 84ea436a7e7edc6851b97b718b66195edddd2da2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760506"
---
# <a name="use-allocation-keys-in-general-journals"></a><span data-ttu-id="f8398-103">Verwenden von Umlageschlüsseln in Fibu Erf.-Journals</span><span class="sxs-lookup"><span data-stu-id="f8398-103">Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="f8398-104">Die Posten einer Fibu Erf.-Journalzeile lassen sich beim Buchen des Erf.-Journals auf verschiedene Konten verteilen.</span><span class="sxs-lookup"><span data-stu-id="f8398-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="f8398-105">Die Verteilung kann nach Anzahl, Prozent oder Betrag vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="f8398-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="f8398-106">Einrichten von Verteilungsschlüsseln</span><span class="sxs-lookup"><span data-stu-id="f8398-106">To set up allocation keys</span></span>
1. <span data-ttu-id="f8398-107">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Wiederk. Fibu Erf.-Journal** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="f8398-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="f8398-108">Wählen Sie auf der Seite **Fibu Erf.-Journalnamen** den **Erf.-Journalnamen**.</span><span class="sxs-lookup"><span data-stu-id="f8398-108">Choose the **Batch Name** field to open the **General Journal Batches** page.</span></span>
3. <span data-ttu-id="f8398-109">Sie können entweder Zuordnungen in einer vorhandene Charge in der Liste ändern oder eine neue Charge mit Zuordnungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f8398-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="f8398-110">Um eine neue Chargennummer zu erstellen, wählen Sie die Aktion **Neu** und gehen Sie zum nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="f8398-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="f8398-111">Um die Zuordnungen eines vorhandenen Erfassungsjournals zu ändern, wählen Sie das Erfassungsjournal und gehen Sie zum Schritt 7.</span><span class="sxs-lookup"><span data-stu-id="f8398-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="f8398-112">Geben Sie im Feld **Name** einen Namen für das Buch.-Blatt ein, wie beispielsweise REINIGUNG.</span><span class="sxs-lookup"><span data-stu-id="f8398-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="f8398-113">Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie z. B. Reinigungsausgaben Erfassungsjournal.</span><span class="sxs-lookup"><span data-stu-id="f8398-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="f8398-114">Wenn Sie fertig sind, schliessen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f8398-114">When you are done, close the page.</span></span> <span data-ttu-id="f8398-115">Ein neues, leeres wiederkehrendes Erfassungsjournal wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f8398-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="f8398-116">Füllen Sie die Felder in der Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="f8398-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="f8398-117">Wählen Sie die Aktion **Verteilung** aus.</span><span class="sxs-lookup"><span data-stu-id="f8398-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="f8398-118">Erstellen Sie für jede Verteilung eine Zeile.</span><span class="sxs-lookup"><span data-stu-id="f8398-118">Add a line for each allocation.</span></span> <span data-ttu-id="f8398-119">Sie müssen entweder das Feld **Verteilung %**, **Anzahl Verteilungen** oder **Betrag** ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="f8398-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="f8398-120">Sie müssen ebenfalls das Feld **Kontonr.** ausfüllen und, wenn Sie auf globale Dimensionen verteilen, auch die Felder "globale Dimensionen".</span><span class="sxs-lookup"><span data-stu-id="f8398-120">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="f8398-121">Wenn Sie in der Zeile einen Prozentsatz eingeben, wird der Betrag im Feld **Betrag** automatisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="f8398-121">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="f8398-122">Diese Beträge haben das gegenteilige Vorzeichen von dem Gesamtbetrag im Feld **Betrag** des wiederkehrenden Erfassungsjournals.</span><span class="sxs-lookup"><span data-stu-id="f8398-122">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="f8398-123">Nachdem Sie die Zuteilungszeilen eingegeben haben, wählen Sie **OK** aus, um zur Seite **Wiederk. Fibu Erf.-Journal** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="f8398-123">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** page.</span></span> <span data-ttu-id="f8398-124">Das Feld **Zugewiesener Betrag (USD)** ist ausgefüllt und entspricht dem Feld **Betrag**.</span><span class="sxs-lookup"><span data-stu-id="f8398-124">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="f8398-125">Buchen Sie die Erf.-Journalzeile.</span><span class="sxs-lookup"><span data-stu-id="f8398-125">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="f8398-126">Ändern eines bereits eingerichteten Umlageschlüssels</span><span class="sxs-lookup"><span data-stu-id="f8398-126">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="f8398-127">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Wiederk. Fibu Erf.-Journal** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="f8398-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="f8398-128">Wählen Sie auf der Seite **Wiederk. Fibu Erf.-Journal** das Erf.-Journal mit der Verteilung aus.</span><span class="sxs-lookup"><span data-stu-id="f8398-128">On the **Recurring General Journal** page, select the journal with the allocation.</span></span>
3. <span data-ttu-id="f8398-129">Wählen Sie die Zeile mit der Verteilung, und wählen Sie dann die Aktion **Zuweisungen** aus.</span><span class="sxs-lookup"><span data-stu-id="f8398-129">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="f8398-130">Ändern Sie die relevanten Felder und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f8398-130">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8398-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8398-131">See Also</span></span>
[<span data-ttu-id="f8398-132">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="f8398-132">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="f8398-133">Journale und Belege buchen</span><span class="sxs-lookup"><span data-stu-id="f8398-133">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="f8398-134">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f8398-134">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
