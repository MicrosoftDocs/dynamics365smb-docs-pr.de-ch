---
title: Wie Sie Daten in die Felder eingeben| Microsoft Docs
description: Informationen zu allgemeinen Funktionen, die Ihnen dabei helfen, Daten in die Felder einzugeben.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/03/2019
ms.author: jswymer
ms.openlocfilehash: d0fac96313b41a0e41ea96ab4fedd25565498f12
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621174"
---
# <a name="entering-data"></a><span data-ttu-id="90921-103">Eingeben von Daten</span><span class="sxs-lookup"><span data-stu-id="90921-103">Entering Data</span></span>

<span data-ttu-id="90921-104">Es gibt eine Vielzahl allgemeiner Funktionen, die Ihnen dabei helfen, die Daten einfacher, schneller und genaueren einzugeben.</span><span class="sxs-lookup"><span data-stu-id="90921-104">There are many general features that help you enter data easier, faster, and more accurate.</span></span> <span data-ttu-id="90921-105">Die allgemeinen Funktionen für die Eingabe von Daten werden alle in diesem Artikel beschrieben.</span><span class="sxs-lookup"><span data-stu-id="90921-105">The general features for entering data are described in this article.</span></span>  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a><span data-ttu-id="90921-106">Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="90921-106">Keyboard Shortcuts</span></span>

<span data-ttu-id="90921-107">Es gibt mehrere Tastenkombinationen, mit denen Sie ohne Maus arbeiten und Ihre Dateneingabe beschleunigen können, insbesondere bei Posten im großen Umfangs und wiederkehrenden Tippaufgaben.</span><span class="sxs-lookup"><span data-stu-id="90921-107">There are several keyboard shortcuts that let you to work "mouse-free" and speed up your data entry, especially with large scale entries and repetitive typing tasks.</span></span>

<span data-ttu-id="90921-108">Weitere Informationen zu diesen Tastenkombinationen finden Sie unter [Tastenkombinationen](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="90921-108">For more information about shortcuts, see [Keyboard Shortcuts](keyboard-shortcuts.md).</span></span> <span data-ttu-id="90921-109">Einige der Tastenkombinationen werden in diesem erläutert Artikel.</span><span class="sxs-lookup"><span data-stu-id="90921-109">A few of the shortcuts are discussed in this article.</span></span>

## <a name="QuickEntry"></a><span data-ttu-id="90921-110">Beschleunigende der Dateneingabe mithilfe der Schnelleingabe</span><span class="sxs-lookup"><span data-stu-id="90921-110">Accelerating Data Entry Using Quick Entry</span></span>

<span data-ttu-id="90921-111">Die Schnelleingabe ist eine Funktion für die Dateneingabe bei Verwendung der Tastatur.</span><span class="sxs-lookup"><span data-stu-id="90921-111">Quick Entry is a feature designed for data entry when using the keyboard.</span></span> <span data-ttu-id="90921-112">Schnelleingabe funktioniert bei Feldern (wie in Kartenseiten) und in Listen (Zeilen und Spalten).</span><span class="sxs-lookup"><span data-stu-id="90921-112">Quick Entry works on fields (like on card pages) and in lists (rows and columns).</span></span> <span data-ttu-id="90921-113">Sie ist bei der Durchführung wiederkehrende Tippaufgaben hilfreich, die mehrere Datensätze nacheinander erfordern, wie ein Stapel von Verkaufsaufträgen oder der Registrierung neuer Artikel.</span><span class="sxs-lookup"><span data-stu-id="90921-113">It is beneficial when performing repetitive typing tasks that require creating multiple records in sequence, such as a batch of sales orders or registering new items.</span></span>

<span data-ttu-id="90921-114">Sie sind möglicherweise bereits mit der Anwendung die TAB-TASTE vertraut, um von einem Feld einer Seite zum nächsten bearbeitbaren Feld zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="90921-114">You might already be familiar with using the Tab key to navigate from one field on a page to the next editable field.</span></span> <span data-ttu-id="90921-115">Der Nachteil der Anwendung von TAB ist, dass sie stets fortlaufend zum nächsten Feld navigiert.</span><span class="sxs-lookup"><span data-stu-id="90921-115">A disadvantage of using Tab is that it always goes sequentially to the next field.</span></span> <!-- even if the field is non-editable or seldom filled it in.--><span data-ttu-id="90921-116">Mit Schnelleintrag können Sie den Pfad ändern.</span><span class="sxs-lookup"><span data-stu-id="90921-116">Quick Entry lets you change this path.</span></span> <span data-ttu-id="90921-117">Mit Schnelleintrag verwenden Sie ENTER, um nur durch diejenigen Felder zu navigieren, an den Sie interessiert sind, und Sie überspringen die nicht-bearbeitbaren Felder und Felder, die Sie üblicherweise nicht ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="90921-117">With Quick Entry, you use the Enter key to navigate through only those fields that you are interested in, skipping non-editable fields and fields that you typically do not fill in.</span></span> <span data-ttu-id="90921-118">Sie haben dieses Verhalten möglicherweise bereits auf einigen Seiten bemerkt.</span><span class="sxs-lookup"><span data-stu-id="90921-118">You might have already noticed this behavior on some pages.</span></span> <span data-ttu-id="90921-119">Der Grund ist, dass die Anwendung bereits festlegt, welche Felder eingeschlossen werden, wenn die Eingabetaste gedrückt wird und welche Felder übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="90921-119">This is because the application already designates which fields to include when pressing Enter and which ones to skip.</span></span> <span data-ttu-id="90921-120">Sie können die Schnelleingabe anpassen, indem Sie den Arbeitsbereich personalisieren und optimieren, wie Sie Daten auf jeder Seite eingeben.</span><span class="sxs-lookup"><span data-stu-id="90921-120">You can customize Quick Entry by personalizing your workspace and optimizing how you enter data on each page.</span></span>

### <a name="how-quick-entry-works"></a><span data-ttu-id="90921-121">So funktioniert die Schnelleingabe</span><span class="sxs-lookup"><span data-stu-id="90921-121">How Quick Entry Works</span></span>

<span data-ttu-id="90921-122">Jedes Feld kann als *in Schnelleingabe enthalten* oder *aus Schnelleingabe ausgeschlossen* markiert werden.</span><span class="sxs-lookup"><span data-stu-id="90921-122">Every field can be marked as either being *included in Quick Entry* or *excluded from Quick Entry*.</span></span> <span data-ttu-id="90921-123">Felder, die in der Schnelleingabe enthalten sind, sind im Pfad enthalten, wenn Sie ENTER drücken; Felder, die aus der Schnelleingabe ausgeschlossen sind, nicht.</span><span class="sxs-lookup"><span data-stu-id="90921-123">Fields that are included in Quick Entry, will be included in the path when you press Enter; fields that are excluded from Quick Entry, will not.</span></span>

<span data-ttu-id="90921-124">Wenn Sie die Dateneingabe in einem Feld beendet haben, drücken Sie einfach ENTER, um die Änderungen zu bestätigen und zum nächsten Feld zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="90921-124">When you are finished entering data in a field, you simply press Enter to confirm the changes and go to the next field.</span></span> <span data-ttu-id="90921-125">Wenn Sie die Richtung umkehren und zum vorherigen Feld gehen möchten, drücken SHIFT+ENTER.</span><span class="sxs-lookup"><span data-stu-id="90921-125">If you want to reverse direction, and go the previous field, press Shift+Enter.</span></span> <span data-ttu-id="90921-126">Weitere Informationen zu diesen Tastenkombinationen finden Sie unter [Tastenkombinationen der Schnelleingabe für Felder](keyboard-shortcuts.md#QuickEntry).</span><span class="sxs-lookup"><span data-stu-id="90921-126">For more information about shortcuts, see [Quick Entry Keyboard Shortcuts for Fields](keyboard-shortcuts.md#QuickEntry).</span></span>

#### <a name="tips-and-tricks"></a><span data-ttu-id="90921-127">Tipps und Tricks</span><span class="sxs-lookup"><span data-stu-id="90921-127">Tips and tricks</span></span>
<span data-ttu-id="90921-128">Es folgen einige nützliche Informationen zur Anwendung der Schnelleingabe.</span><span class="sxs-lookup"><span data-stu-id="90921-128">The following provides some useful information about using Quick Entry.</span></span>

- <span data-ttu-id="90921-129">Sie ist für alle bearbeitbaren Felder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90921-129">It is available for any editable fields.</span></span>
- <span data-ttu-id="90921-130">Sie funktioniert auch über Spalten und Zeilen hinweg.</span><span class="sxs-lookup"><span data-stu-id="90921-130">It also works across columns and rows.</span></span>
- <span data-ttu-id="90921-131">Sie verhindert nicht den Zugriff auf andere Elemente einer Seite wie Aktionen.</span><span class="sxs-lookup"><span data-stu-id="90921-131">It does not prevent accessing other elements of a page, such as actions.</span></span> <span data-ttu-id="90921-132">Auf diese kann noch mit TAB und SHIFT+TAB zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="90921-132">These are still accessible by using Tab and Shift+Tab.</span></span>  
- <span data-ttu-id="90921-133">Inforegister müssen nicht erweitert werden, damit die Schnelleingabe funktioniert.</span><span class="sxs-lookup"><span data-stu-id="90921-133">FastTabs do not have to be expanded for Quick Entry to work.</span></span> <span data-ttu-id="90921-134">Wenn sich das nächste Feld der Schnelleingabe in einem reduzierten Inforegister befindet, wird das Inforegister automatisch mit Fokus auf dem festgelegten Feld erweitert.</span><span class="sxs-lookup"><span data-stu-id="90921-134">If the next Quick Entry field is located in a collapsed FastTab, that FastTab will automatically expand and focus on the designated field.</span></span>
- <span data-ttu-id="90921-135">Schnelleingabe funktioniert ungeachtet davon, ob Felder erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="90921-135">Quick Entry works irrespective of whether fields are mandatory.</span></span> <span data-ttu-id="90921-136">Daher ist es vorteilhaft, sicherzustellen, dass erforderliche Felder in der Schnelleingabe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="90921-136">So it is a good idea to ensure that mandatory fields are included in Quick Entry.</span></span>
- <span data-ttu-id="90921-137">Standardmäßig sind die meisten Felder automatisch im der Schnelleingabe enthalten.</span><span class="sxs-lookup"><span data-stu-id="90921-137">By default, most fields are automatically included in Quick Entry.</span></span> <span data-ttu-id="90921-138">Daher wird die Aufgabe höchstwahrscheinlich zunächst darin bestehen, Felder aus der Schnelleingabe auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="90921-138">So initially your task will most likely be excluding fields from Quick Entry.</span></span>

### <a name="how-to-change-quick-entry-fields"></a><span data-ttu-id="90921-139">So ändern Sie Felder der Schnelleingabe</span><span class="sxs-lookup"><span data-stu-id="90921-139">How to Change Quick Entry Fields</span></span>

<span data-ttu-id="90921-140">Um zu ändern, welche Felder einer Seite in die Schnelleingabe eingeschlossen oder daraus ausgeschlossen werden, verwenden Sie die Personalisierung.</span><span class="sxs-lookup"><span data-stu-id="90921-140">To change which fields are included in or excluded from Quick Entry on a page, you use personalization.</span></span>

1. <span data-ttu-id="90921-141">Beginnen Sie mit der Personalisierung, indem Sie das ![Einstellungen](media/ui-experience/settings_icon_small.png "Symbol für Rollencenter einstellen") und dann **Personalisieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="90921-141">Start personalization by selecting the ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center") icon, and then **Personalize**.</span></span>
2. <span data-ttu-id="90921-142">Wählen Sie ein Feld, das Sie ändern möchten, oder wählen Sie in Listen die entsprechende Spaltenüberschrift und dann entweder **In Schnelleingabe einschließen** oder **Aus Schnellausgabe ausschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="90921-142">Select a field that you want change, or in lists, select the corresponding column heading, and then choose either **Include in Quick Entry** or **Exclude from Quick Entry**.</span></span>

<span data-ttu-id="90921-143">Weitere Informationen zur Personalisierung finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="90921-143">For more information about personalization, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="90921-144">Pflichtfelder</span><span class="sxs-lookup"><span data-stu-id="90921-144">Mandatory Fields</span></span>

<span data-ttu-id="90921-145">Wenn Sie Daten auf Seiten in eingeben, werden bestimmte Felder mit einem roten Sternchen markiert.</span><span class="sxs-lookup"><span data-stu-id="90921-145">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="90921-146">Das rote Sternchen bedeutet, dass das Feld ausgefüllt werden muss, um einen bestimmten Prozess, der das Feld verwendet, abzuschliessen (Beispiel: Buchung einer Transaktion, die den Wert in dem Feld verwendet).</span><span class="sxs-lookup"><span data-stu-id="90921-146">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="90921-147">Selbst wenn das Feld ein rotes Sternchen enthält, sind Sie nicht gezwungen, das Feld auszufüllen, bevor Sie mit anderen Feldern fortfahren oder die Seite schliessen.</span><span class="sxs-lookup"><span data-stu-id="90921-147">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="90921-148">Das rote Sternchen dient nur als Erinnerung, dass Sie am Beenden eines bestimmten Prozesses gehindert werden.</span><span class="sxs-lookup"><span data-stu-id="90921-148">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  

## <a name="finding-data-as-you-type"></a><span data-ttu-id="90921-149">Suchen von Daten bei der Eingabe</span><span class="sxs-lookup"><span data-stu-id="90921-149">Finding Data As You Type</span></span>

 <span data-ttu-id="90921-150">Wenn Sie mit der Eingabe von Zeichen in einem Feld beginnen, wird eine Dropdownliste mit möglichen Feldwerten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90921-150">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="90921-151">Die Anzeige der Dropdownliste ändert sich bei Eingabe weiterer Zeichen, und Sie können den korrekten Wert auswählen, wenn dieser angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="90921-151">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="90921-152">Viele Felder haben eine Schaltfläche mit einem nach unten zeigenden Pfeil, den Sie auswählen können.</span><span class="sxs-lookup"><span data-stu-id="90921-152">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="90921-153">Durch Klicken auf diesen Pfeil wird eine Liste der Daten angezeigt, die in das Feld eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="90921-153">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="90921-154">Die Schaltfläche bietet abhängig vom Feldtyp zwei Funktionen:</span><span class="sxs-lookup"><span data-stu-id="90921-154">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="90921-155">Lookup – Zeigt Informationen aus einer anderen Tabelle an, die im Feld eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="90921-155">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="90921-156">Es kann jeweils ein Datenelement ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="90921-156">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="90921-157">Dropdown – Zeigt die Optionen an, die für das Feld verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="90921-157">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="90921-158">Sie können nur eine der Optionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="90921-158">You can select only one of the options.</span></span>  

## <a name="copying-and-pasting-fields-and-lines"></a><span data-ttu-id="90921-159">Felder und Zeilen kopieren und einfügen</span><span class="sxs-lookup"><span data-stu-id="90921-159">Copying and Pasting Fields and Lines</span></span>

<span data-ttu-id="90921-160">Sie können eine oder mehrere Zeilen aus einer Liste oder einem einzelnen Feld auf einer Seite kopieren und die kopierten Daten dann auf der gleichen Seite, einer andere Seite oder einem externen Beleg (wie Microsoft Excel und Outlook-E-Mail) einfügen.</span><span class="sxs-lookup"><span data-stu-id="90921-160">You can copy one or more rows from a list or a single field on a page, and then paste what you copied into the same page, another page, or an external document (like Microsoft Excel and Outlook email).</span></span> <span data-ttu-id="90921-161">Kurz gesagt, zum Kopieren drücken Sie CTRL+C (cmd+C in Mac Os) auf Ihrer Tastatur.</span><span class="sxs-lookup"><span data-stu-id="90921-161">In short, to copy, you press CTRL+C (cmd+C in macOS) on your keyboard.</span></span> <span data-ttu-id="90921-162">Zum Einfügen drücken Sie CTRL+V (cmd+V in Mac Os).</span><span class="sxs-lookup"><span data-stu-id="90921-162">To paste, you press CTRL+V (cmd+V in macOS).</span></span>

<span data-ttu-id="90921-163">Um das Feld in einer Liste in der gleichen Spalte der Zeile darüber zu kopieren, und es in die aktuelle Zeile einzufügen, drücken Sie einfach F8.</span><span class="sxs-lookup"><span data-stu-id="90921-163">In a list, to copy the field in the same column of the row above, and paste it into the current row, just press F8.</span></span>

<span data-ttu-id="90921-164">Weitere Informationen finden Sie unter [Kopieren und Einfügen in Business Central](ui-copy-paste.md).</span><span class="sxs-lookup"><span data-stu-id="90921-164">For more information, see [Copying and Pasting in Business Central](ui-copy-paste.md).</span></span>

## <a name="Focus"></a><span data-ttu-id="90921-165">Fokussieren auf Positionsartikel</span><span class="sxs-lookup"><span data-stu-id="90921-165">Focusing on Line Items</span></span>

<span data-ttu-id="90921-166">Wenn Sie in Belegen arbeiten, die einen Positionsartikelteil haben, wie Verkaufsauftrag oder Rechnungsseite, können Sie die Ansicht umschalten, um nur auf die Positionsartikel zu fokussieren und den Positionsartikelteil gewissermaßen zu erweitern, damit er fast den gesamten Arbeitsbereich ausfüllt - dabei werden andere Teile der Seite außer dem Aktionsbereich oben ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="90921-166">When working on documents that include a line items part, like a sales order or invoice page, you can switch your view to focus only on the line items, essentially expanding the line items part so that it occupies pretty much the entire workspace - hiding other parts of the page except the actions area at the top.</span></span> <span data-ttu-id="90921-167">Damit erhalten Sie einen besseren Überblick über die Positionsartikel und mehr Platz, um daran zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="90921-167">This gives you a better overview of the lines items, and provides more room to work on them.</span></span> <span data-ttu-id="90921-168">Dies ist besonders nützlich, wenn Sie mit großen Positionsartikellisten arbeiten und schnelle Dateneingabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="90921-168">This is particularly beneficial when working with large line item lists and fast data entry is desired.</span></span>

<span data-ttu-id="90921-169">Ein anderer Vorteil besteht darin, dass auch erweiterte Filterungsfunktion, wie auf anderen Listen, bereitgestellt werden, sodass Durchsuchen und Suchen nach Belegpositionen sogar einfacher wird.</span><span class="sxs-lookup"><span data-stu-id="90921-169">Another advantage is that it also provides advanced filtering capability, like on other lists, so browsing and searching through line items becomes even easier.</span></span>

### <a name="switching-the-focus-on-and-off"></a><span data-ttu-id="90921-170">Den Fokus zwischen An- und Ausschalten wechseln</span><span class="sxs-lookup"><span data-stu-id="90921-170">Switching the Focus On and Off</span></span>

<span data-ttu-id="90921-171">Um sich auf Positionsartikel zu konzentrieren, wählen Sie einen beliebigen Bereich des Positionsartikelteils aus und wählen Sie dann das ![Fokusmodussymbol](media/focus-mode.png "Fokusmodussymbol") in der oberen rechten Ecke aus oder drücken Sie CTRL+SHIFT+F12.</span><span class="sxs-lookup"><span data-stu-id="90921-171">To focus on lines items, select anywhere in the line item part, and then choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") in the upper right corner or press Ctrl+Shift+F12.</span></span>

<span data-ttu-id="90921-172">Um zur Normalansicht zurückzukehren, wählen Sie das ![Fokusmodussymbol](media/focus-mode.png "Fokusmodussymbol") aus oder drücken Sie CTRL+SHIFT+F12 erneut.</span><span class="sxs-lookup"><span data-stu-id="90921-172">To switch back to the normal view, choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") or press Ctrl+Shift+F12 again.</span></span>

### <a name="filtering-the-line-items"></a><span data-ttu-id="90921-173">Filtern der Positionsartikel</span><span class="sxs-lookup"><span data-stu-id="90921-173">Filtering the Line Items</span></span>

<span data-ttu-id="90921-174">Um mit dem Filtern zu beginnen, wählen Sie ![Filterbereichssymbol](media/open-filter-pane-icon.png "Filterbereichssymbol") in der Liste, oder drücken Sie auf **Shift+F3**, um den Filterbereich zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="90921-174">To start filtering, select ![Filter pane icon](media/open-filter-pane-icon.png "Filter pane icon") at the top of the list or press **Shift+F3** to open the filter pane.</span></span> <span data-ttu-id="90921-175">Sie arbeiten mit Filterbereich, wie in jeder anderen Liste.</span><span class="sxs-lookup"><span data-stu-id="90921-175">You work with the filter pane as you do on any other list.</span></span> <span data-ttu-id="90921-176">Weitere Informationen finden Sie unter [Filterung](ui-enter-criteria-filters.md#Filtering).</span><span class="sxs-lookup"><span data-stu-id="90921-176">For more information, see [Filtering](ui-enter-criteria-filters.md#Filtering).</span></span>

<span data-ttu-id="90921-177">Filterung ist besonders dann von Nutzen, wenn längere Belege anzeigt und analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="90921-177">Filtering is especially helpful when viewing and analysing longer documents.</span></span> <span data-ttu-id="90921-178">Stellen Sie sich beispielsweise vor, dass Sie eine gebuchte Verkaufsrechnung öffnen und filtern, dass alle Positionsartikel mit einem Einzelrabatt von 5 % haben, oder Sie filtern, dass nur Fahrradzubehör mit "Pro" im Namen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="90921-178">For example, imagine you open a posted sales invoice and filter the line items to display all line items that have an individual discount above 5%, or filter to display only bike accessories with 'pro' in the name.</span></span>

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="90921-179">Eingeben von Mengen durch Berechnung</span><span class="sxs-lookup"><span data-stu-id="90921-179">Entering Quantities by Calculation</span></span>

<span data-ttu-id="90921-180">Beim Eingeben von Zahlen in die Mengenfelder, beispielsweise in das Feld **Menge** in einer Artikel Erf.-Journalzeile, kann anstelle der Summenmenge die Formel eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="90921-180">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

### <a name="examples"></a><span data-ttu-id="90921-181">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90921-181">Examples</span></span>  

-   <span data-ttu-id="90921-182">Bei Eingabe von 19+19 wird im Feld als Wert 38 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90921-182">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="90921-183">Bei Eingabe von 41-9 wird im Feld als Wert 32 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90921-183">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="90921-184">Bei Eingabe von 12\*4 wird im Feld als Wert 48 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90921-184">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="90921-185">Bei Eingabe von 12/4 wird im Feld als Wert 3 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90921-185">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="90921-186">Eingeben von negativen Zahlen</span><span class="sxs-lookup"><span data-stu-id="90921-186">Entering Negative Numbers</span></span>

<span data-ttu-id="90921-187">Sie können negative Zahlen auf zwei Arten eingeben.</span><span class="sxs-lookup"><span data-stu-id="90921-187">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="90921-188">Die Zahl. -20,5 kann so eingegeben werden:</span><span class="sxs-lookup"><span data-stu-id="90921-188">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="90921-189">-20.5</span><span class="sxs-lookup"><span data-stu-id="90921-189">-20.5</span></span>  

    <span data-ttu-id="90921-190">Oder</span><span class="sxs-lookup"><span data-stu-id="90921-190">or</span></span>
-   <span data-ttu-id="90921-191">20.5-</span><span class="sxs-lookup"><span data-stu-id="90921-191">20.5-</span></span>  

 <span data-ttu-id="90921-192">In beiden Fällen wird der Betrag als -20,5 erfasst.</span><span class="sxs-lookup"><span data-stu-id="90921-192">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="90921-193">Wenn das letzte Zeichen des Ausdrucks **+** oder **-** ist, wird der gesamte Ausdruck mit diesem Vorzeichen erfasst.</span><span class="sxs-lookup"><span data-stu-id="90921-193">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="90921-194">Ein Beispiel, **10-20+** ergibt 10 und nicht -10.</span><span class="sxs-lookup"><span data-stu-id="90921-194">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="90921-195">Daten und Zeit eingeben</span><span class="sxs-lookup"><span data-stu-id="90921-195">Entering Dates and Times</span></span>

<span data-ttu-id="90921-196">Datums- und Uhrzeitwerte können in alle Felder eingegeben werden, die speziell für Datumswerte vorgesehen sind (Datumsfelder).</span><span class="sxs-lookup"><span data-stu-id="90921-196">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="90921-197">Datumswerte können mit oder ohne Trennzeichen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="90921-197">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="90921-198">Wie Sie Daten und Uhrzeiten eingeben, hängt von Ihren Einstellungen in Ihrer**Region** ab.</span><span class="sxs-lookup"><span data-stu-id="90921-198">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="90921-199">Weitere Informationen finden Sie unter [Ändern von Grundeinstellungen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="90921-199">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="90921-200">Eingeben von Datumswerten</span><span class="sxs-lookup"><span data-stu-id="90921-200">Entering Dates</span></span>

<span data-ttu-id="90921-201">Für Datumsfelder können Sie die Datenauswahl verwenden, mit der Sie ein Datum aus einem Kalender auswählen können, oder Sie können Datumswerte manuell eingeben.</span><span class="sxs-lookup"><span data-stu-id="90921-201">For date fields, you can either use the data picker, which lets you select a date from a calender, or you can enter dates manually.</span></span> <span data-ttu-id="90921-202">Dieser Abschnitt bietet eine kurze Übersicht über die Dateneingabe.</span><span class="sxs-lookup"><span data-stu-id="90921-202">This section provides a brief overview of how to enter dates.</span></span> <span data-ttu-id="90921-203">Weitere Informationen finden Sie unter [Arbeiten mit Datumsangaben und Uhrzeiten in Kalendern](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="90921-203">For more details, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

<span data-ttu-id="90921-204">Für manuelle Eingaben von Datumsangaben können zwei-, vier-, sechs- oder achtstellige Werte eingegeben werden:</span><span class="sxs-lookup"><span data-stu-id="90921-204">For manually date entry, you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="90921-205">Wenn Sie nur zwei Ziffern eingeben, wird dies als Tagesangabe interpretiert, es gilt also der Monat und das Jahr des Arbeitsdatums.</span><span class="sxs-lookup"><span data-stu-id="90921-205">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="90921-206">Wenn Sie vier Ziffern eingeben, wird dies als Tages- und Monatsangabe interpretiert, es gilt also das Jahr des Arbeitsdatums.</span><span class="sxs-lookup"><span data-stu-id="90921-206">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="90921-207">Wenn Sie ein Datum zwischen dem 01.01.1930 und dem 31.12.2029 eingeben wollen, können Sie das Jahr zweistellig eingeben; ansonsten sollten Sie das Jahr vierstellig angeben.</span><span class="sxs-lookup"><span data-stu-id="90921-207">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

<span data-ttu-id="90921-208">Sie können auch einen Wochentag gefolgt von einer Kalenderwoche (und optional einer Jahresangabe) für das Datum verwenden. So steht beispielsweise "mo25" oder "Mo25" für den Montag in der 25. Kalenderwoche.</span><span class="sxs-lookup"><span data-stu-id="90921-208">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

<span data-ttu-id="90921-209">Anstatt ein bestimmtes Datum direkt einzugeben, können Sie auch einen dieser Codes verwenden.</span><span class="sxs-lookup"><span data-stu-id="90921-209">Instead of entering a specific date, you can enter one of these codes.</span></span>  

|<span data-ttu-id="90921-210">Code</span><span class="sxs-lookup"><span data-stu-id="90921-210">Code</span></span>|<span data-ttu-id="90921-211">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="90921-211">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="90921-212">h</span><span class="sxs-lookup"><span data-stu-id="90921-212">t</span></span>|<span data-ttu-id="90921-213">Dies gibt das heutige Datum (das Systemdatum des Computers) an.</span><span class="sxs-lookup"><span data-stu-id="90921-213">This specifies today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="90921-214">p</span><span class="sxs-lookup"><span data-stu-id="90921-214">p</span></span>|<span data-ttu-id="90921-215">Dies gibt einen Buchhaltungszeitraum an, wobei `p` den ersten Buchhaltungszeitraum bezeichnet, `p2` den zweiten Buchhaltungszeitraum angibt usw.</span><span class="sxs-lookup"><span data-stu-id="90921-215">This specifies an accounting period´, where `p`means the first accounting period, `p2` means the second accountin period, and so on.</span></span> |
|<span data-ttu-id="90921-216">a</span><span class="sxs-lookup"><span data-stu-id="90921-216">w</span></span>|<span data-ttu-id="90921-217">Dies gibt das Arbeitsdatum an, das in der Anwendung eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="90921-217">This specifies the work date that is setup in the application.</span></span> <span data-ttu-id="90921-218">Um das Arbeitsdatum zu ändern, siehe [Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="90921-218">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="90921-219">Die Verwendung des Arbeitsdatums ist hilfreich, wenn eine Vielzahl von Transaktionen zu einem Datum ausgeführt werden müssen, das vom Systemdatum abweicht.</span><span class="sxs-lookup"><span data-stu-id="90921-219">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|
|<span data-ttu-id="90921-220">c</span><span class="sxs-lookup"><span data-stu-id="90921-220">c</span></span>|<span data-ttu-id="90921-221">Dieses gibt an, dass das Datum nach `c` einem Ultimodatum ist, z. B. `C123101`.</span><span class="sxs-lookup"><span data-stu-id="90921-221">This specifies that the date after `c`is a closing date, for example `C123101`.</span></span>|  

## <a name="entering-times"></a><span data-ttu-id="90921-222">Eingeben von Uhrzeiten</span><span class="sxs-lookup"><span data-stu-id="90921-222">Entering Times</span></span>

<span data-ttu-id="90921-223">Beim Eingeben von Uhrzeiten kann zwischen den Zeiteinheiten ein beliebiges Trennzeichen (oder auch kein Trennzeichen) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90921-223">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="90921-224">Die Angabe von Minuten, Sekunden oder AM/PM ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="90921-224">You do not have to write minutes, seconds, or AM/PM.</span></span>  

<span data-ttu-id="90921-225">In der folgenden Tabelle finden Sie eine Liste über die Möglichkeiten zum Angeben von Uhrzeiten sowie die Interpretation der jeweiligen Angabe.</span><span class="sxs-lookup"><span data-stu-id="90921-225">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="90921-226">Eingabe</span><span class="sxs-lookup"><span data-stu-id="90921-226">Entry</span></span>|<span data-ttu-id="90921-227">Interpretation</span><span class="sxs-lookup"><span data-stu-id="90921-227">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="90921-228">5</span><span class="sxs-lookup"><span data-stu-id="90921-228">5</span></span>|<span data-ttu-id="90921-229">05:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-229">05:00:00</span></span>|  
|<span data-ttu-id="90921-230">5:30</span><span class="sxs-lookup"><span data-stu-id="90921-230">5:30</span></span>|<span data-ttu-id="90921-231">05:30:00</span><span class="sxs-lookup"><span data-stu-id="90921-231">05:30:00</span></span>|  
|<span data-ttu-id="90921-232">0530</span><span class="sxs-lookup"><span data-stu-id="90921-232">0530</span></span>|<span data-ttu-id="90921-233">05:30:00</span><span class="sxs-lookup"><span data-stu-id="90921-233">05:30:00</span></span>|  
|<span data-ttu-id="90921-234">5:30:5</span><span class="sxs-lookup"><span data-stu-id="90921-234">5:30:5</span></span>|<span data-ttu-id="90921-235">05:30:05</span><span class="sxs-lookup"><span data-stu-id="90921-235">05:30:05</span></span>|  
|<span data-ttu-id="90921-236">053005</span><span class="sxs-lookup"><span data-stu-id="90921-236">053005</span></span>|<span data-ttu-id="90921-237">05:30:05</span><span class="sxs-lookup"><span data-stu-id="90921-237">05:30:05</span></span>|  
|<span data-ttu-id="90921-238">5:30:5,50</span><span class="sxs-lookup"><span data-stu-id="90921-238">5:30:5,50</span></span>|<span data-ttu-id="90921-239">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="90921-239">05:30:05.5</span></span>|  
|<span data-ttu-id="90921-240">053005050</span><span class="sxs-lookup"><span data-stu-id="90921-240">053005050</span></span>|<span data-ttu-id="90921-241">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="90921-241">05:30:05.05</span></span>|  

 <span data-ttu-id="90921-242">Sie müssen für jede Zeiteinheit, die Sie eintragen, zwei Zeichen eingeben, wenn Sie kein Trennzeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="90921-242">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="90921-243">Datums-/Uhrzeitangaben eingeben</span><span class="sxs-lookup"><span data-stu-id="90921-243">Entering Datetimes</span></span>

<span data-ttu-id="90921-244">Wenn Sie eine Datum-/Zeiteingabe eingeben, müssen Sie zwischen dem Datum und der Zeiteingabe einen Leerschritt einfügen.</span><span class="sxs-lookup"><span data-stu-id="90921-244">When you enter datetimes you must enter a space between the date and the time.</span></span>  

<span data-ttu-id="90921-245">In der folgenden Tabelle finden Sie eine Liste über die Möglichkeiten zum Eingeben von Datums-/Uhrzeitangaben sowie die Interpretation der jeweiligen Angabe.</span><span class="sxs-lookup"><span data-stu-id="90921-245">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="90921-246">Posten</span><span class="sxs-lookup"><span data-stu-id="90921-246">Entry</span></span>|<span data-ttu-id="90921-247">Interpretation</span><span class="sxs-lookup"><span data-stu-id="90921-247">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="90921-248">131202 132455</span><span class="sxs-lookup"><span data-stu-id="90921-248">131202 132455</span></span>|<span data-ttu-id="90921-249">13-12-02 13:24:55</span><span class="sxs-lookup"><span data-stu-id="90921-249">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="90921-250">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="90921-250">1-12-02 10</span></span>|<span data-ttu-id="90921-251">01-12-02 10:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-251">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="90921-252">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="90921-252">1.12.02 5</span></span>|<span data-ttu-id="90921-253">01-12-02 05:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-253">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="90921-254">1.12.02</span><span class="sxs-lookup"><span data-stu-id="90921-254">1.12.02</span></span>|<span data-ttu-id="90921-255">01-12-02 00:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-255">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="90921-256">11 12</span><span class="sxs-lookup"><span data-stu-id="90921-256">11 12</span></span>|<span data-ttu-id="90921-257">11-aktueller Monat-aktuelles Jahr 12:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-257">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="90921-258">1112 12</span><span class="sxs-lookup"><span data-stu-id="90921-258">1112 12</span></span>|<span data-ttu-id="90921-259">11-12-aktuelles Jahr 12:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-259">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="90921-260">h für heute</span><span class="sxs-lookup"><span data-stu-id="90921-260">t or today</span></span>|<span data-ttu-id="90921-261">heutiges Datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-261">today's date 00:00:00</span></span>|  
|<span data-ttu-id="90921-262">t Zeit</span><span class="sxs-lookup"><span data-stu-id="90921-262">t time</span></span>|<span data-ttu-id="90921-263">heutiges Datum aktuelle Zeit</span><span class="sxs-lookup"><span data-stu-id="90921-263">today's date actual time</span></span>|  
|<span data-ttu-id="90921-264">h 10:30</span><span class="sxs-lookup"><span data-stu-id="90921-264">t 10:30</span></span>|<span data-ttu-id="90921-265">heutiges Datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="90921-265">today's date 10:30:00</span></span>|  
|<span data-ttu-id="90921-266">h 3:3:3</span><span class="sxs-lookup"><span data-stu-id="90921-266">t 3:3:3</span></span>|<span data-ttu-id="90921-267">heutiges Datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="90921-267">today's date 03:03:03</span></span>|  
|<span data-ttu-id="90921-268">a oder Arbeitsdatum</span><span class="sxs-lookup"><span data-stu-id="90921-268">w or workdate</span></span>|<span data-ttu-id="90921-269">das Arbeitsdatum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-269">the working date 00:00:00</span></span>|  
|<span data-ttu-id="90921-270">"m" oder "Montag"</span><span class="sxs-lookup"><span data-stu-id="90921-270">m or Monday</span></span>|<span data-ttu-id="90921-271">Montag der aktuellen Woche 00:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-271">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="90921-272">"d" oder "Dienstag"</span><span class="sxs-lookup"><span data-stu-id="90921-272">tu or Tuesday</span></span>|<span data-ttu-id="90921-273">Dienstag der aktuellen Woche 00:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-273">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="90921-274">"mi" oder "Mittwoch"</span><span class="sxs-lookup"><span data-stu-id="90921-274">we or Wednesday</span></span>|<span data-ttu-id="90921-275">Mittwoch der aktuellen Woche 00:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-275">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="90921-276">"do" oder "Donnerstag"</span><span class="sxs-lookup"><span data-stu-id="90921-276">th or Thursday</span></span>|<span data-ttu-id="90921-277">Donnerstag der aktuellen Woche 00:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-277">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="90921-278">"f" oder "Freitag"</span><span class="sxs-lookup"><span data-stu-id="90921-278">f or Friday</span></span>|<span data-ttu-id="90921-279">Freitag der aktuellen Woche 00:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-279">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="90921-280">"s" oder "Sonnabend"</span><span class="sxs-lookup"><span data-stu-id="90921-280">s or Saturday</span></span>|<span data-ttu-id="90921-281">Samstag der aktuellen Woche 00:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-281">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="90921-282">"so" oder "Sonntag"</span><span class="sxs-lookup"><span data-stu-id="90921-282">su or Sunday</span></span>|<span data-ttu-id="90921-283">Sonntag der aktuellen Woche 00:00:00</span><span class="sxs-lookup"><span data-stu-id="90921-283">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="90921-284">di 10:30</span><span class="sxs-lookup"><span data-stu-id="90921-284">tu 10:30</span></span>|<span data-ttu-id="90921-285">Dienstag der aktuellen Woche 10:30:00</span><span class="sxs-lookup"><span data-stu-id="90921-285">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="90921-286">d 3:3:3</span><span class="sxs-lookup"><span data-stu-id="90921-286">tu 3:3:3</span></span>|<span data-ttu-id="90921-287">Dienstag der aktuellen Woche 03:03:03</span><span class="sxs-lookup"><span data-stu-id="90921-287">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="90921-288">Eingeben von Terminen</span><span class="sxs-lookup"><span data-stu-id="90921-288">Entering Duration</span></span>

<span data-ttu-id="90921-289">Sie können Zeitdauern als Zahl gefolgt von der entsprechenden Einheit eingeben.</span><span class="sxs-lookup"><span data-stu-id="90921-289">You enter a duration as a number followed by its unit of measure.</span></span>  

<span data-ttu-id="90921-290">Hier folgen einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="90921-290">Here are some examples.</span></span>  

|<span data-ttu-id="90921-291">Termine</span><span class="sxs-lookup"><span data-stu-id="90921-291">Duration</span></span>|<span data-ttu-id="90921-292">Masseinheit\*\*</span><span class="sxs-lookup"><span data-stu-id="90921-292">Unit of measure\*\*</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="90921-293">2h</span><span class="sxs-lookup"><span data-stu-id="90921-293">2h</span></span>|<span data-ttu-id="90921-294">2 Stunden</span><span class="sxs-lookup"><span data-stu-id="90921-294">2 hrs</span></span>|  
|<span data-ttu-id="90921-295">6h 30m</span><span class="sxs-lookup"><span data-stu-id="90921-295">6h 30 m</span></span>|<span data-ttu-id="90921-296">6 Stunden 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="90921-296">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="90921-297">6,5h</span><span class="sxs-lookup"><span data-stu-id="90921-297">6.5h</span></span>|<span data-ttu-id="90921-298">6 Stunden 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="90921-298">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="90921-299">90m</span><span class="sxs-lookup"><span data-stu-id="90921-299">90m</span></span>|<span data-ttu-id="90921-300">1 Stunde 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="90921-300">1 hr 30 mins</span></span>|  
|<span data-ttu-id="90921-301">2d 6h 30m</span><span class="sxs-lookup"><span data-stu-id="90921-301">2d 6h 30m</span></span>|<span data-ttu-id="90921-302">2 Tage 6 Stunden 30 Minuten</span><span class="sxs-lookup"><span data-stu-id="90921-302">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="90921-303">2d 6h 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="90921-303">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="90921-304">2 Tage 6 Stunden 30 Minuten 56 Sekunden 600 Millisekunden</span><span class="sxs-lookup"><span data-stu-id="90921-304">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="90921-305">Sie haben auch die Möglichkeit, eine Zahl einzugeben, die dann automatisch in einen Zeitraum umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="90921-305">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="90921-306">Die Zahl, welche Sie eingeben, wird entsprechend der Vorgabeeinheit, die Sie für das Dauer-Feld definiert haben, konvertiert.</span><span class="sxs-lookup"><span data-stu-id="90921-306">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="90921-307">Geben Sie zum Ermitteln der Einheit, die für ein Feld vom Typ "Dauer" verwendet wird, eine Zahl ein. Am Ergebnis können Sie ablesen, in welche Einheit diese konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="90921-307">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="90921-308">Die Zahl 5 wird in 5 h konvertiert, wenn Stunden als Einheit angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="90921-308">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a><span data-ttu-id="90921-309">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90921-309">See Also</span></span>  
 [<span data-ttu-id="90921-310">Sortieren, Durchsuchen und Filtern von Listen</span><span class="sxs-lookup"><span data-stu-id="90921-310">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="90921-311">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="90921-311">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
