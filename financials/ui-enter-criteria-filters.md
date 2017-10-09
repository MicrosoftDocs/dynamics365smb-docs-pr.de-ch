---
title: Daten und das Eingeben von Filterkriterien finden | Microsoft Docs
description: Beschreibt, wie mit Filtern, wie Schnellfilter, gearbeitet wird, um Suchergebnisse zu verfeinern, wenn Sie Daten suchen.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11d7ef56e980ba263dba6328b2f2f08b86410242
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="searching-filtering-and-sorting-data"></a><span data-ttu-id="08b47-103">Ermitteln, filternd und Sortieren von Daten</span><span class="sxs-lookup"><span data-stu-id="08b47-103">Searching, Filtering, and Sorting Data</span></span>
<span data-ttu-id="08b47-104">Es gibt mehrere Elemente, wie Sie das tun können und die dabei helfen, Datensätze in einer Liste aufzufinden, festzulegen und zu scannen.</span><span class="sxs-lookup"><span data-stu-id="08b47-104">There are a few things that you can do that will help you find, pinpoint, and scan records in a list.</span></span> <span data-ttu-id="08b47-105">Diese umfassen die Sortierung, Suche und Filterung.</span><span class="sxs-lookup"><span data-stu-id="08b47-105">These include sorting, searching and filtering.</span></span>

<span data-ttu-id="08b47-106">Wenn Sie nach Daten, wie Debitorennamen, Adressen oder Produktgruppen suchen möchten, geben Sie Kriterien ein.</span><span class="sxs-lookup"><span data-stu-id="08b47-106">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="08b47-107">Beim Eingeben von Filterkriterien können alle Ziffern und Buchstaben verwendet werden, die auch normalerweise im Feld zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="08b47-107">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="08b47-108">Zudem können Sie Sonderzeichen verwenden, um eine zusätzliche Filterung der Ergebnisse zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="08b47-108">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="08b47-109">Es gibt zwei Arten zu suchen: mithilfe der Schnellfilter- oder der Spaltenfilter.</span><span class="sxs-lookup"><span data-stu-id="08b47-109">There are two ways to search: using the Quick Filter or column filters.</span></span>

## <a name="sorting"></a><span data-ttu-id="08b47-110">Sortieren</span><span class="sxs-lookup"><span data-stu-id="08b47-110">Sorting</span></span>
<span data-ttu-id="08b47-111">Dank der Sortierfunktion können Sie sich schnell und einfach einen Überblick über Ihre Daten verschaffen.</span><span class="sxs-lookup"><span data-stu-id="08b47-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="08b47-112">Wenn Sie beispielsweise über zahlreiche Debitorenkontakte verfügen, können Sie auswählen, um nach folgenden Kriterien zu sortieren: **Debitorennummer**, **Debitorenbuchungsgruppe**, **Währungscode**, **Länder-/Regionscode** oder **Salestax-Registrierung**, um die gewünschte Liste zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="08b47-112">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="08b47-113">Um eine Liste zu sortieren, können Sie entweder einen Spaltenüberschriftentext um das Menüband zu erweitern und Aufsteigen Absteigend Reihenfolge aus, oder wählen Sie kleine Abstiegpfeil in die Spaltenüberschrift, und wählen Sie dann **Aufsteigend** oder **Absteigend**</span><span class="sxs-lookup"><span data-stu-id="08b47-113">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small downs arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="08b47-114">Sortierung wird nicht auf Bilder, BLOB-Felder und FlowFilter unterstützt, die keiner Tabelle angehören.</span><span class="sxs-lookup"><span data-stu-id="08b47-114">Sorting is not supported images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching-by-using-the-quick-filter"></a><span data-ttu-id="08b47-115">Suchen mithilfe des Schnellfilters</span><span class="sxs-lookup"><span data-stu-id="08b47-115">Searching by using the Quick Filter</span></span>
<span data-ttu-id="08b47-116">Sie können allen Seiten Filter hinzufügen, indem Sie Schnellfilter oder erweiterte Filter verwenden.</span><span class="sxs-lookup"><span data-stu-id="08b47-116">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="08b47-117">Der Schnellfilter wird aktiviert, indem Sie das Lupensymbol in der oberen rechten Ecke einer Seite auswählen.</span><span class="sxs-lookup"><span data-stu-id="08b47-117">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="08b47-118">Diese Filterart wird für die schnelle Eingabe von Kriterien verwendet.</span><span class="sxs-lookup"><span data-stu-id="08b47-118">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="08b47-119">Der Schnellfilter bietet einen einfachen Zugriff auf Filterdaten durch die Eingabe reinen Texts, bietet aber auch zahlreiche Optionen für Suchkriterien.</span><span class="sxs-lookup"><span data-stu-id="08b47-119">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="08b47-120">Abhängig davon, ob Sie Freitext oder Text mit Symbolen eingeben, verhält sich der Schnellfilter unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="08b47-120">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="08b47-121">Wenn Sie Freitextangaben in den Suchkriterien eingeben, werden die Suchkriterien als die Groß-/Kleinschreibung nicht beachtend angesehen.</span><span class="sxs-lookup"><span data-stu-id="08b47-121">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="08b47-122">Wenn Sie Text mit Symbolen in den Suchkriterien eingeben, werden die Suchkriterien genau wie angegeben interpretiert, und die Groß-/Kleinschreibung wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="08b47-122">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="08b47-123">Schnelle Filterkriterien</span><span class="sxs-lookup"><span data-stu-id="08b47-123">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="08b47-124">Suchkriterien</span><span class="sxs-lookup"><span data-stu-id="08b47-124">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="08b47-125">Interpretiert als...</span><span class="sxs-lookup"><span data-stu-id="08b47-125">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="08b47-126">Reklamationen...</span><span class="sxs-lookup"><span data-stu-id="08b47-126">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="08b47-127">man</span><span class="sxs-lookup"><span data-stu-id="08b47-127">man</span></span></TD>
    <TD><span data-ttu-id="08b47-128">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="08b47-128">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="08b47-129">Alle Datensätze, die den Text <b>Mann</b> enthalten und die Groß-/Kleinschreibung nicht beachten.</span><span class="sxs-lookup"><span data-stu-id="08b47-129">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="08b47-130">se</span><span class="sxs-lookup"><span data-stu-id="08b47-130">se</span></span></TD>
    <TD><span data-ttu-id="08b47-131">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="08b47-131">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="08b47-132">Alle Datensätze, die den Text <b>se</b> enthalten und die Groß-/Kleinschreibung nicht beachten.</span><span class="sxs-lookup"><span data-stu-id="08b47-132">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="08b47-133">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="08b47-133">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="08b47-134">Beginnt mit <b>Man</b> und Groß-/Kleinschreibung beachten</span><span class="sxs-lookup"><span data-stu-id="08b47-134">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="08b47-135">Alle Datensätze, die mit dem Text <b>Mann</b> beginnen.</span><span class="sxs-lookup"><span data-stu-id="08b47-135">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="08b47-136">'man'</span><span class="sxs-lookup"><span data-stu-id="08b47-136">'man'</span></span></TD>
    <TD><span data-ttu-id="08b47-137">Exakter Text unter Berücksichtigung der Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="08b47-137">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="08b47-138">Alle Datensätze, die mit <b>Mann</b> genau übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="08b47-138">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="08b47-139">@man*</span><span class="sxs-lookup"><span data-stu-id="08b47-139">@man*</span></span> </TD>
    <TD><span data-ttu-id="08b47-140">Beginnt mit, Groß-/Kleinschreibung beachtet</span><span class="sxs-lookup"><span data-stu-id="08b47-140">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="08b47-141">Alle Datensätze, die mit <b>Mann</b> beginnen.</span><span class="sxs-lookup"><span data-stu-id="08b47-141">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="08b47-142">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="08b47-142">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="08b47-143">Endet mit, Groß-/Kleinschreibung beachtet</span><span class="sxs-lookup"><span data-stu-id="08b47-143">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="08b47-144">Alle Datensätze, die mit <b>mann</b> enden.</span><span class="sxs-lookup"><span data-stu-id="08b47-144">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="08b47-145">Sie können keinen Platzhalter beim Filtern in Aufzählungsfeldern, wie das Feld **Status** in Verkaufsaufträgen verwenden.</span><span class="sxs-lookup"><span data-stu-id="08b47-145">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="08b47-146">Wenn Sie einen Filter für diese Art von Feld eingeben möchten, können Sie den numerischen Wert als Filterparameter eingeben.</span><span class="sxs-lookup"><span data-stu-id="08b47-146">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="08b47-147">Beispielsweise im Feld **Status** in einem Verkaufsauftrag, der die Werte **Offen**, **Freigegeben**, **Genehmigung ausstehend** und **Vorauszahlung ausstehend** hat, verwenden Sie die Werte **0**, **1**, **2** und **3**, um für diese Optionen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="08b47-147">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span> 

## <a name="searching-by-using-column-filters"></a><span data-ttu-id="08b47-148">Suchen mithilfe der Spaltenfiltern</span><span class="sxs-lookup"><span data-stu-id="08b47-148">Searching by using column Filters</span></span>
<span data-ttu-id="08b47-149">Sie können einen Filter für einen oder mehreren Spalten aus einer Liste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="08b47-149">You can add a filter on one or more columns in a list.</span></span> <span data-ttu-id="08b47-150">Das Filtern in Spalten ist flexibel und erhöht als den Schnellfilter.</span><span class="sxs-lookup"><span data-stu-id="08b47-150">Filtering on columns is more flexible and enhanced than the Quick Filter.</span></span> 

### <a name="to-add-a-filter-on-a-column"></a><span data-ttu-id="08b47-151">Um einen Filter für eine Spalte hinzufügen</span><span class="sxs-lookup"><span data-stu-id="08b47-151">To add a filter on a column</span></span>
1.  <span data-ttu-id="08b47-152">Bevor Sie Filter hinzufügen, wählen Sie ![Anzeigen als Liste] (media/ui_show_as_list_icon.png "Anzeigen als linken Listenpfeil"), um die Listenansicht zu ändern.</span><span class="sxs-lookup"><span data-stu-id="08b47-152">Before you add a filter, choose ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to change to the list view.</span></span>
2. <span data-ttu-id="08b47-153">Wählen Sie den Abwärts-Pfeil in die Spaltenüberschrift, und wählen Sie dann **Filter**.</span><span class="sxs-lookup"><span data-stu-id="08b47-153">Choose the downwards arrow in the column heading, and then choose **Filter**.</span></span>
3. <span data-ttu-id="08b47-154">Führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="08b47-154">Do one of the following:</span></span> 
  -  <span data-ttu-id="08b47-155">Wählen Sie *...* neben dem Feld, um einen Wert aus einer Liste auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="08b47-155">Choose *...* next to the box to select a value from a list.</span></span>
  -  <span data-ttu-id="08b47-156">Eingeben von Kriterien in Filtern.</span><span class="sxs-lookup"><span data-stu-id="08b47-156">Enter filter criteria in the box.</span></span> <span data-ttu-id="08b47-157">Sehen Sie den nächsten Abschnitt für Einzelheiten.</span><span class="sxs-lookup"><span data-stu-id="08b47-157">See the next section for details.</span></span>
4. <span data-ttu-id="08b47-158">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="08b47-158">Choose the **OK** button.</span></span>

## <a name="filter-criteria-and-symbols"></a><span data-ttu-id="08b47-159">Filterkriterien und Bildsymbole</span><span class="sxs-lookup"><span data-stu-id="08b47-159">Filter criteria and symbols</span></span>
<span data-ttu-id="08b47-160">Beim Eingeben von Filterkriterien können alle Ziffern und Buchstaben verwendet werden, die auch normalerweise im Feld zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="08b47-160">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="08b47-161">Zudem können Sie Sonderzeichen verwenden, um eine zusätzliche Filterung der Ergebnisse zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="08b47-161">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="08b47-162">Die folgende Tabelle enthält die Symbole, die in Filtern verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="08b47-162">The following tables show the symbols which can be used in filters.</span></span>  
  
> [!IMPORTANT]  
>  <span data-ttu-id="08b47-163">Es kann Instanzen geben, in denen diese Feldwerte Symbole enthalten, die Sie filtern möchten.</span><span class="sxs-lookup"><span data-stu-id="08b47-163">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="08b47-164">Um dies zu tun, müssen Sie den Filterausdruck berücksichtigt der das Symbol in Anführungszeichen (") enthält.</span><span class="sxs-lookup"><span data-stu-id="08b47-164">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="08b47-165">Wenn Sie beispielsweise Datensätzen filtern möchten, die mit dem Text *S&R* beginnen, ist der Filterausdruck **'S&R*'**.</span><span class="sxs-lookup"><span data-stu-id="08b47-165">For example, if you want to filter on records that start with the text *S&R*, the filter expression is **'S&R*'**.</span></span>  
  
### <a name="-interval"></a><span data-ttu-id="08b47-166">(..) Intervall</span><span class="sxs-lookup"><span data-stu-id="08b47-166">(..) Interval</span></span>  
  
|<span data-ttu-id="08b47-167">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-167">Sample Expression</span></span>|<span data-ttu-id="08b47-168">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-168">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-169">1100..2100</span><span class="sxs-lookup"><span data-stu-id="08b47-169">1100..2100</span></span>|<span data-ttu-id="08b47-170">Nummer 1100 bis 2100</span><span class="sxs-lookup"><span data-stu-id="08b47-170">Numbers 1100 through 2100</span></span>|  
|<span data-ttu-id="08b47-171">..2500</span><span class="sxs-lookup"><span data-stu-id="08b47-171">..2500</span></span>|<span data-ttu-id="08b47-172">Bis einschliesslich 2500</span><span class="sxs-lookup"><span data-stu-id="08b47-172">Up to and including 2500</span></span>|  
|<span data-ttu-id="08b47-173">..31 12 00</span><span class="sxs-lookup"><span data-stu-id="08b47-173">..12 31 00</span></span>|<span data-ttu-id="08b47-174">Datum bis und einschliesslich 31.12.00</span><span class="sxs-lookup"><span data-stu-id="08b47-174">Dates up to and including 12 31 00</span></span>|  
|<span data-ttu-id="08b47-175">P8..</span><span class="sxs-lookup"><span data-stu-id="08b47-175">P8..</span></span>|<span data-ttu-id="08b47-176">Daten zur Buchhaltungsperiode 8 und folgende</span><span class="sxs-lookup"><span data-stu-id="08b47-176">Information for accounting period 8 and thereafter</span></span>|  
|<span data-ttu-id="08b47-177">..23</span><span class="sxs-lookup"><span data-stu-id="08b47-177">..23</span></span>|<span data-ttu-id="08b47-178">Vom Anfangsdatum bis zum 23. (aktueller Monat, aktuelles Jahr, 23:59:59)</span><span class="sxs-lookup"><span data-stu-id="08b47-178">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|<span data-ttu-id="08b47-179">23..</span><span class="sxs-lookup"><span data-stu-id="08b47-179">23..</span></span>|<span data-ttu-id="08b47-180">Vom 23-des aktuellen Monats-des aktuellen Jahres 0:00:00 bis zum Ende der Zeit</span><span class="sxs-lookup"><span data-stu-id="08b47-180">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|<span data-ttu-id="08b47-181">22..23</span><span class="sxs-lookup"><span data-stu-id="08b47-181">22..23</span></span>|<span data-ttu-id="08b47-182">Vom 22-des aktuellen Monats-aktuellen Jahres 0:00:00 bis zum 23-des aktuellen Monats-aktuellen Jahres 23:59:59</span><span class="sxs-lookup"><span data-stu-id="08b47-182">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  
  
### <a name="124-eitheror"></a><span data-ttu-id="08b47-183">(&#124;) Entweder/oder</span><span class="sxs-lookup"><span data-stu-id="08b47-183">(&#124;) Either/or</span></span>  
  
|<span data-ttu-id="08b47-184">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-184">Sample Expression</span></span>|<span data-ttu-id="08b47-185">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-185">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-186">1200&#124;1300</span><span class="sxs-lookup"><span data-stu-id="08b47-186">1200&#124;1300</span></span>|<span data-ttu-id="08b47-187">Nummern mit 1200 oder 1300</span><span class="sxs-lookup"><span data-stu-id="08b47-187">Numbers with 1200 or 1300</span></span>|  
  
### <a name="-not-equal-to"></a><span data-ttu-id="08b47-188">(<>) Ungleich</span><span class="sxs-lookup"><span data-stu-id="08b47-188">(<>) Not equal to</span></span>  
  
|<span data-ttu-id="08b47-189">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-189">Sample Expression</span></span>|<span data-ttu-id="08b47-190">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-190">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-191"><>0</span><span class="sxs-lookup"><span data-stu-id="08b47-191"><>0</span></span>|<span data-ttu-id="08b47-192">Alle Datensätze ausser der Nummer Null</span><span class="sxs-lookup"><span data-stu-id="08b47-192">All numbers except 0</span></span><br /><br /> <span data-ttu-id="08b47-193">Die SQL Server-Option ermöglicht es Ihnen, dieses Symbol mit einem Platzhalterausdruck zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="08b47-193">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="08b47-194">So wird beispielsweise mit "<>A*" Text beschrieben, der nicht mit einem grossen A beginnt.</span><span class="sxs-lookup"><span data-stu-id="08b47-194">For example, <>A* meaning not equal to any text that starts with A.</span></span>|  
  
### <a name="-greater-than"></a><span data-ttu-id="08b47-195">(>) Grösser als</span><span class="sxs-lookup"><span data-stu-id="08b47-195">(>) Greater than</span></span>  
  
|<span data-ttu-id="08b47-196">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-196">Sample Expression</span></span>|<span data-ttu-id="08b47-197">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-197">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-198">>1200</span><span class="sxs-lookup"><span data-stu-id="08b47-198">>1200</span></span>|<span data-ttu-id="08b47-199">Datensatznummern grösser als 1200</span><span class="sxs-lookup"><span data-stu-id="08b47-199">Numbers greater than 1200</span></span>|  
  
### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="08b47-200">(>=) Grösser oder gleich</span><span class="sxs-lookup"><span data-stu-id="08b47-200">(>=) Greater than or equal to</span></span>  
  
|<span data-ttu-id="08b47-201">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-201">Sample Expression</span></span>|<span data-ttu-id="08b47-202">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-202">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-203">>=1200</span><span class="sxs-lookup"><span data-stu-id="08b47-203">>=1200</span></span>|<span data-ttu-id="08b47-204">Datensatznummern ab einschliesslich 1200 aufwärts</span><span class="sxs-lookup"><span data-stu-id="08b47-204">Numbers greater than or equal to 1200</span></span>|  
  
### <a name="-less-than"></a><span data-ttu-id="08b47-205">(<) Kleiner als</span><span class="sxs-lookup"><span data-stu-id="08b47-205">(<) Less than</span></span>  
  
|<span data-ttu-id="08b47-206">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-206">Sample Expression</span></span>|<span data-ttu-id="08b47-207">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-207">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-208"><1200</span><span class="sxs-lookup"><span data-stu-id="08b47-208"><1200</span></span>|<span data-ttu-id="08b47-209">Datensatznummern kleiner als 1200</span><span class="sxs-lookup"><span data-stu-id="08b47-209">Numbers less than 1200</span></span>|  
  
### <a name="-less-than-or-equal-to"></a><span data-ttu-id="08b47-210">(<=) Kleiner oder gleich</span><span class="sxs-lookup"><span data-stu-id="08b47-210">(<=) Less than or equal to</span></span>  
  
|<span data-ttu-id="08b47-211">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-211">Sample Expression</span></span>|<span data-ttu-id="08b47-212">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-212">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-213"><=1200</span><span class="sxs-lookup"><span data-stu-id="08b47-213"><=1200</span></span>|<span data-ttu-id="08b47-214">Datensatznummern kleiner als oder gleich 1200</span><span class="sxs-lookup"><span data-stu-id="08b47-214">Numbers less than or equal to 1200</span></span>|  
  
### <a name="-and"></a><span data-ttu-id="08b47-215">(&) Und</span><span class="sxs-lookup"><span data-stu-id="08b47-215">(&) And</span></span>  
  
|<span data-ttu-id="08b47-216">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-216">Sample Expression</span></span>|<span data-ttu-id="08b47-217">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-217">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-218">>200&<1200</span><span class="sxs-lookup"><span data-stu-id="08b47-218">>200&<1200</span></span>|<span data-ttu-id="08b47-219">Nummern größer 200 und Nummern kleiner 1200.</span><span class="sxs-lookup"><span data-stu-id="08b47-219">Numbers greater than 200 and less than 1200</span></span>|  
  
### <a name="-an-exact-character-match"></a><span data-ttu-id="08b47-220">(") Eine genaue Zeichenübereinstimmung</span><span class="sxs-lookup"><span data-stu-id="08b47-220">('') An exact character match</span></span>  
  
|<span data-ttu-id="08b47-221">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-221">Sample Expression</span></span>|<span data-ttu-id="08b47-222">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-223">'man'</span><span class="sxs-lookup"><span data-stu-id="08b47-223">'man'</span></span>|<span data-ttu-id="08b47-224">Text, der genau übereinstimmt und die Groß-/Kleinschreibung berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="08b47-224">Text that matches man exactly and is case sensitive.</span></span>|  
  
### <a name="-case-insensitive"></a><span data-ttu-id="08b47-225">(@) Groß-/Kleinschreibung beachten</span><span class="sxs-lookup"><span data-stu-id="08b47-225">(@) Case insensitive</span></span>  
  
|<span data-ttu-id="08b47-226">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-226">Sample Expression</span></span>|<span data-ttu-id="08b47-227">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-227">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-228">@man*</span><span class="sxs-lookup"><span data-stu-id="08b47-228">@man*</span></span>|<span data-ttu-id="08b47-229">Text, der mit „Man“ beginnt und die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="08b47-229">Text that starts with man and is case insensitive.</span></span>|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="08b47-230">(*) Beliebig viele unbekannte Zeichen</span><span class="sxs-lookup"><span data-stu-id="08b47-230">(*) An indefinite number of unknown characters</span></span>  
  
|<span data-ttu-id="08b47-231">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-231">Sample Expression</span></span>|<span data-ttu-id="08b47-232">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-233">*Co*</span><span class="sxs-lookup"><span data-stu-id="08b47-233">*Co*</span></span>|<span data-ttu-id="08b47-234">Text, der die Zeichenfolge "Co" enthält und die Groß-/Kleinschreibung ist.</span><span class="sxs-lookup"><span data-stu-id="08b47-234">Text that contains "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="08b47-235">*Co</span><span class="sxs-lookup"><span data-stu-id="08b47-235">*Co</span></span>|<span data-ttu-id="08b47-236">Text, der mit "Co" endet und die Groß-/Kleinschreibung ist.</span><span class="sxs-lookup"><span data-stu-id="08b47-236">Text that ends with "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="08b47-237">Co*</span><span class="sxs-lookup"><span data-stu-id="08b47-237">Co*</span></span>|<span data-ttu-id="08b47-238">Text, der mit "Co" beginnt und die Groß-/Kleinschreibung ist.</span><span class="sxs-lookup"><span data-stu-id="08b47-238">Text that begins with "Co" and is case sensitive.</span></span>|  
  
### <a name="-one-unknown-character"></a><span data-ttu-id="08b47-239">(?) Ein unbekannter Buchstabe</span><span class="sxs-lookup"><span data-stu-id="08b47-239">(?) One unknown character</span></span>  
  
|<span data-ttu-id="08b47-240">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-240">Sample Expression</span></span>|<span data-ttu-id="08b47-241">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-241">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-242">Hans?n</span><span class="sxs-lookup"><span data-stu-id="08b47-242">Hans?n</span></span>|<span data-ttu-id="08b47-243">Text wie "Hansen" oder "Hanson"</span><span class="sxs-lookup"><span data-stu-id="08b47-243">Text such as Hansen or Hanson</span></span>|  
  
### <a name="combined-format-expressions"></a><span data-ttu-id="08b47-244">Kombinierte Formatausdrücke</span><span class="sxs-lookup"><span data-stu-id="08b47-244">Combined format expressions</span></span>  
  
|<span data-ttu-id="08b47-245">Beispielausdruck</span><span class="sxs-lookup"><span data-stu-id="08b47-245">Sample Expression</span></span>|<span data-ttu-id="08b47-246">Angezeigte Datensätze</span><span class="sxs-lookup"><span data-stu-id="08b47-246">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="08b47-247">5999&#124;8100..8490</span><span class="sxs-lookup"><span data-stu-id="08b47-247">5999&#124;8100..8490</span></span>|<span data-ttu-id="08b47-248">Alle Datensätze mit der Nummer 5999 oder zwischen 8100 bis 8490.</span><span class="sxs-lookup"><span data-stu-id="08b47-248">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="08b47-249">..1299&#124;1400..</span><span class="sxs-lookup"><span data-stu-id="08b47-249">..1299&#124;1400..</span></span>|<span data-ttu-id="08b47-250">Alle Datensätze mit Nummern kleiner als bzw. gleich 1299 oder mit Nummern grösser als bzw. gleich 1400, d. h. alle Datensatznummern ausser 1300 bis 1399.</span><span class="sxs-lookup"><span data-stu-id="08b47-250">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|<span data-ttu-id="08b47-251">>50&<100</span><span class="sxs-lookup"><span data-stu-id="08b47-251">>50&<100</span></span>|<span data-ttu-id="08b47-252">Alle Datensätze mit Nummern grösser als 50 und kleiner als 100, d. h. mit Nummern zwischen 51 und 99.</span><span class="sxs-lookup"><span data-stu-id="08b47-252">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  
 
## <a name="see-also"></a><span data-ttu-id="08b47-253">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08b47-253">See Also</span></span>
<span data-ttu-id="08b47-254">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="08b47-254">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

