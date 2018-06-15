---
title: C5-Datenmigrations-Erweiterung verwenden | Microsoft Docs
description: Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Fibukonten von Microsoft Dynamics C5 2012 zu Business Central zu migrieren.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/09/208
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: fa6779ee8fb2bbb453014e32cb7f3cf8dcfa18da
ms.openlocfilehash: 698bde6949c6053501881d07135586810fc81bdd
ms.contentlocale: de-ch
ms.lasthandoff: 04/11/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="c0044-103">Die C5 Datenmigrations-Erweiterung für Business Central</span><span class="sxs-lookup"><span data-stu-id="c0044-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="c0044-104">Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Fibukonten von Microsoft Dynamics C5 2012 zu [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="c0044-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c0044-105">Sie können historische Posten auch für Fibukonten migrieren.</span><span class="sxs-lookup"><span data-stu-id="c0044-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="c0044-106">Der Mandant darf in [!INCLUDE[d365fin](includes/d365fin_md.md)] keine Daten in enthalten.</span><span class="sxs-lookup"><span data-stu-id="c0044-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="c0044-107">Nachdem Sie mit der Migration begonnen haben, erstellen Sie keine Debitoren, Kreditoren, Artikel oder Konten, bis die Migration beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c0044-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="c0044-108">Welche Daten migriert?</span><span class="sxs-lookup"><span data-stu-id="c0044-108">What Data is Migrated?</span></span>
<span data-ttu-id="c0044-109">Die folgenden Daten werden für jede Einheit migriert:</span><span class="sxs-lookup"><span data-stu-id="c0044-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="c0044-110">**Debitoren**</span><span class="sxs-lookup"><span data-stu-id="c0044-110">**Customers**</span></span>
* <span data-ttu-id="c0044-111">Ort</span><span class="sxs-lookup"><span data-stu-id="c0044-111">Location</span></span>
* <span data-ttu-id="c0044-112">Land</span><span class="sxs-lookup"><span data-stu-id="c0044-112">Country</span></span>
* <span data-ttu-id="c0044-113">Kunden-Dimensionen (Abteilung, Kostenträger, Kostenstelle)</span><span class="sxs-lookup"><span data-stu-id="c0044-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="c0044-114">Lieferbedingungsmethode</span><span class="sxs-lookup"><span data-stu-id="c0044-114">Shipment method</span></span>
* <span data-ttu-id="c0044-115">Vertriebsmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="c0044-115">Sales Person</span></span>
* <span data-ttu-id="c0044-116">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="c0044-116">Payment terms</span></span>
* <span data-ttu-id="c0044-117">Zahlungsform</span><span class="sxs-lookup"><span data-stu-id="c0044-117">Payment method</span></span>
* <span data-ttu-id="c0044-118">Debitorenpreisgruppe</span><span class="sxs-lookup"><span data-stu-id="c0044-118">Customer price group</span></span>
* <span data-ttu-id="c0044-119">Debitorenrechnungsrabatt</span><span class="sxs-lookup"><span data-stu-id="c0044-119">Customer invoice discount</span></span>

<span data-ttu-id="c0044-120">Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:</span><span class="sxs-lookup"><span data-stu-id="c0044-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="c0044-121">Debitorenbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="c0044-121">Customer posting setup</span></span>
* <span data-ttu-id="c0044-122">Fibu Erf.-Journalname</span><span class="sxs-lookup"><span data-stu-id="c0044-122">General journal batch</span></span>
* <span data-ttu-id="c0044-123">Migrieren Sie offene Debitorenposten (Kundenbucheinträge)</span><span class="sxs-lookup"><span data-stu-id="c0044-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="c0044-124">**Kreditoren**</span><span class="sxs-lookup"><span data-stu-id="c0044-124">**Vendors**</span></span>
* <span data-ttu-id="c0044-125">Ort</span><span class="sxs-lookup"><span data-stu-id="c0044-125">Location</span></span>
* <span data-ttu-id="c0044-126">Land</span><span class="sxs-lookup"><span data-stu-id="c0044-126">Country</span></span>
* <span data-ttu-id="c0044-127">Kunden-Dimensionen (Abteilung, Kostenträger, Kostenstelle)</span><span class="sxs-lookup"><span data-stu-id="c0044-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="c0044-128">Rechnungsrabatt</span><span class="sxs-lookup"><span data-stu-id="c0044-128">Invoice discount</span></span>
* <span data-ttu-id="c0044-129">Lieferbedingungsmethode</span><span class="sxs-lookup"><span data-stu-id="c0044-129">Shipment method</span></span>
* <span data-ttu-id="c0044-130">Einkäufer</span><span class="sxs-lookup"><span data-stu-id="c0044-130">Purchaser</span></span>
* <span data-ttu-id="c0044-131">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="c0044-131">Payment terms</span></span>
* <span data-ttu-id="c0044-132">Zahlungsform</span><span class="sxs-lookup"><span data-stu-id="c0044-132">Payment method</span></span>
* <span data-ttu-id="c0044-133">Kreditorenrechnungsrabatte</span><span class="sxs-lookup"><span data-stu-id="c0044-133">Vendor invoice discount</span></span>

<span data-ttu-id="c0044-134">Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:</span><span class="sxs-lookup"><span data-stu-id="c0044-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="c0044-135">Kreditorenbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="c0044-135">Vendor posting setup</span></span>
* <span data-ttu-id="c0044-136">Fibu Erf.-Journalname</span><span class="sxs-lookup"><span data-stu-id="c0044-136">General journal batch</span></span>
* <span data-ttu-id="c0044-137">Öffnen Sie das Fenster Transaktionen (Kreditorenposten)</span><span class="sxs-lookup"><span data-stu-id="c0044-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="c0044-138">**Arti&kel**</span><span class="sxs-lookup"><span data-stu-id="c0044-138">**Items**</span></span>
* <span data-ttu-id="c0044-139">Ort</span><span class="sxs-lookup"><span data-stu-id="c0044-139">Location</span></span>
* <span data-ttu-id="c0044-140">Land</span><span class="sxs-lookup"><span data-stu-id="c0044-140">Country</span></span>
* <span data-ttu-id="c0044-141">Element-Dimensionen (Abteilung, Kostenträger, Kostenstelle)</span><span class="sxs-lookup"><span data-stu-id="c0044-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="c0044-142">VK-Zeilenrabatte</span><span class="sxs-lookup"><span data-stu-id="c0044-142">Sales line discounts</span></span>
* <span data-ttu-id="c0044-143">Debitorenrabattgruppen</span><span class="sxs-lookup"><span data-stu-id="c0044-143">Customer discount groups</span></span>
* <span data-ttu-id="c0044-144">Artikelrabattgruppen</span><span class="sxs-lookup"><span data-stu-id="c0044-144">Item discount groups</span></span>
* <span data-ttu-id="c0044-145">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="c0044-145">Sales price</span></span>
* <span data-ttu-id="c0044-146">Zollposition</span><span class="sxs-lookup"><span data-stu-id="c0044-146">Tariff number</span></span>
* <span data-ttu-id="c0044-147">Einheiten</span><span class="sxs-lookup"><span data-stu-id="c0044-147">Units of measure</span></span>
* <span data-ttu-id="c0044-148">Artikelverfolgungscode</span><span class="sxs-lookup"><span data-stu-id="c0044-148">Item tracking code</span></span>
* <span data-ttu-id="c0044-149">Debitorenpreisgruppe</span><span class="sxs-lookup"><span data-stu-id="c0044-149">Customer price group</span></span>

<span data-ttu-id="c0044-150">Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:</span><span class="sxs-lookup"><span data-stu-id="c0044-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="c0044-151">Lagerbuchungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="c0044-151">Inventory posting setup</span></span>
* <span data-ttu-id="c0044-152">Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="c0044-152">General posting setup</span></span>
* <span data-ttu-id="c0044-153">Artikel Erf.-Journalname</span><span class="sxs-lookup"><span data-stu-id="c0044-153">Item journal batch</span></span>
* <span data-ttu-id="c0044-154">Öffnen Sie das Fenster Transaktionen (Lagerposten)</span><span class="sxs-lookup"><span data-stu-id="c0044-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="c0044-155">Wenn es offene Transaktionen gibt, die Fremdwährungen verwenden, werden die Wechselkurse für alle Währungen auch migriert.</span><span class="sxs-lookup"><span data-stu-id="c0044-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="c0044-156">Andere Wechselkurse werden nicht migriert.</span><span class="sxs-lookup"><span data-stu-id="c0044-156">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="c0044-157">**Kontenplan**</span><span class="sxs-lookup"><span data-stu-id="c0044-157">**Chart of Accounts**</span></span>  
* <span data-ttu-id="c0044-158">Standard-Dimensionen (Abteilung, Kostenträger, Kostenstelle)</span><span class="sxs-lookup"><span data-stu-id="c0044-158">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="c0044-159">Historische Transaktionen</span><span class="sxs-lookup"><span data-stu-id="c0044-159">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="c0044-160">Historische Transaktionen werden so gut unterschiedlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="c0044-160">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="c0044-161">Wenn Sie Daten migrieren, setzen Sie einen **Aktuelle Periode** Parameter.</span><span class="sxs-lookup"><span data-stu-id="c0044-161">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="c0044-162">Dieser Parameter gibt an, wie Ihre Transaktionen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c0044-162">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="c0044-163">Transaktionen nach diesem Datum werden einzeln migriert.</span><span class="sxs-lookup"><span data-stu-id="c0044-163">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="c0044-164">Transaktionen vor diesem Zeitpunkt werden pro Konto aggregiert und migriert als einzelner Betrag.</span><span class="sxs-lookup"><span data-stu-id="c0044-164">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="c0044-165">Nehmen wir an, es gibt Transaktionen 2015, 2016, 2017 und 2018 und Sie definieren 1. Januar 2017 im aktuellen Periodenfeld.</span><span class="sxs-lookup"><span data-stu-id="c0044-165">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="c0044-166">Für jedes Konto sind Beträge für Transaktionen an oder vor dem 31. Dezember 2106, in einer eigenen Fibu Erf.-Journalzeile für jedes Fibukonto aggregiert.</span><span class="sxs-lookup"><span data-stu-id="c0044-166">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="c0044-167">Transaktionen nach diesem Datum werden einzeln migriert.</span><span class="sxs-lookup"><span data-stu-id="c0044-167">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="c0044-168">Um Daten zu migrieren</span><span class="sxs-lookup"><span data-stu-id="c0044-168">To migrate data</span></span>
<span data-ttu-id="c0044-169">Es gibt nur einige wenige Schritte, um die Daten aus C5 zu exportieren und sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu importieren:</span><span class="sxs-lookup"><span data-stu-id="c0044-169">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="c0044-170">In C5 verwenden Sie die Funktion **Datenbank exportieren**, um die Daten zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="c0044-170">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="c0044-171">Senden Sie dann den Exportordner an einen komprimierten (gezippten) Ordner.</span><span class="sxs-lookup"><span data-stu-id="c0044-171">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="c0044-172">Wählen Sie dann in [!INCLUDE[d365fin](includes/d365fin_md.md)] das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben Sie **Datenmigration** ein und wählen dann **Datenmigration**.</span><span class="sxs-lookup"><span data-stu-id="c0044-172">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="c0044-173">Schliessen Sie die Schritte im unterstützten Setup ab.</span><span class="sxs-lookup"><span data-stu-id="c0044-173">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="c0044-174">Stellen Sie sicher, dass Sie**Importieren aus Microsoft Dynamcis C5 2012** als die Datenquelle auswählen.</span><span class="sxs-lookup"><span data-stu-id="c0044-174">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="c0044-175">Mandanten fügen häufig Felder hinzu, um C5 für ihren jeweiligen Geschäftsbereich anzupassen.</span><span class="sxs-lookup"><span data-stu-id="c0044-175">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="c0044-176"> migriert nicht Daten vom benutzerdefinierten Feldern.</span><span class="sxs-lookup"><span data-stu-id="c0044-176"> does not migrate data from custom fields.</span></span> <span data-ttu-id="c0044-177">Die Migration schlägt fehl, wenn Sie mehr als 10 benutzerdefinierte Felder haben.</span><span class="sxs-lookup"><span data-stu-id="c0044-177">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="c0044-178">Zeigt den Status der Datenmigration an</span><span class="sxs-lookup"><span data-stu-id="c0044-178">Viewing the Status of the Migration</span></span>
<span data-ttu-id="c0044-179">Verwenden Sie die Seite **Datenmigrations-Übersicht**, um den Erfolg der Migration zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="c0044-179">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="c0044-180">Die Seite zeigt Informationen wie die Anzahl von Einheiten, die migriert wurde, den Status der Migration und die Anzahl von Artikeln an, die migriert wurden und ob sie erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c0044-180">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="c0044-181">Sie zeigt auch die Anzahl von Fehlern, Sie können überprüfen, was schief ging und macht es wenn möglich einfach, zur Einheit zu gehen und das Problem zu lösen.</span><span class="sxs-lookup"><span data-stu-id="c0044-181">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="c0044-182">Weitere Informationen finden Sie im nächsten Abschnitt dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="c0044-182">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="c0044-183">Während Sie auf die Ergebnisse der Migration warten, müssen Sie die Seite aktualisieren, um die Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c0044-183">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="c0044-184">Wie Sie Doppel-Buchung vermeiden</span><span class="sxs-lookup"><span data-stu-id="c0044-184">How to Avoid Double-Posting</span></span>
<span data-ttu-id="c0044-185">Um Doppelbuchungen im Fibuposten zu vermeiden, werden folgende Gegenkonten für offene Transaktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="c0044-185">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  
  
* <span data-ttu-id="c0044-186">Für Kreditoren verwenden wir das A-/P-Konto in der Kreditorenbuchungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c0044-186">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="c0044-187">Für Kreditoren verwenden wir das A-/P-Konto in der Kreditorenbuchungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c0044-187">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="c0044-188">Für Artikel erstellen wir eine Buchungsmatrix, bei der im Korrekturkonto das Konto jenes ist, das als Lagerkonto in der Lagerbuchungseinrichtung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c0044-188">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="c0044-189">Nachbesserung</span><span class="sxs-lookup"><span data-stu-id="c0044-189">Correcting Errors</span></span>
<span data-ttu-id="c0044-190">Falls etwas schief geht und ein Fehler auftritt, wird das **Status** Feld **Abgeschlossen mit Fehlern** angezeigt und das Feld **Fehlerzahl** zeigt an, wie viele es sind.</span><span class="sxs-lookup"><span data-stu-id="c0044-190">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="c0044-191">Um eine Liste der Fehler anzuzeigen, können Sie die Seite öffnen indem Sie **Datenmigrations-Fehler** auswählen:</span><span class="sxs-lookup"><span data-stu-id="c0044-191">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="c0044-192">Die Nummer im Feld **Fehlerzahl** für die Einheit.</span><span class="sxs-lookup"><span data-stu-id="c0044-192">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="c0044-193">Die Einheit und dann die Aktion **Fehler anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="c0044-193">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="c0044-194">Um auf der Seite **Datenmigrations-Fehler** einen Fehler zu korrigieren, können Sie eine Fehlermeldung auswählen, und dann **Datensatz bearbeiten** auswählen, um die Seite zu öffnen, welche de Daten für die migrierte Einheit enthält.</span><span class="sxs-lookup"><span data-stu-id="c0044-194">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="c0044-195">Nachdem Sie eines oder mehrere Fehler korrigiert haben, können Sie **Migrieren von** wählen, um nur die Einheiten zu migrieren, die Sie korrigierten, ohne die Migration vollständig erneut durchführen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="c0044-195">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="c0044-196">Wenn Sie mehr als einen Fehler korrigiert haben, können Sie die Funktion **Weitere auswählen** verwenden, um mehrere Zeilen auszuwählen, um diese zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="c0044-196">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="c0044-197">Wenn es Fehler gibt, die nicht zur Korrektur wichtig sind, können Sie diese auswählen und dann **Auswahl überspringen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="c0044-197">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="c0044-198">Wenn Sie Artikel haben, die in der Stückliste enthalten sind, müssen Sie diese mehrmals migrieren, wenn der ursprüngliche Artikel nicht vor den Varianten erstellt wird, auf die sie verweist.</span><span class="sxs-lookup"><span data-stu-id="c0044-198">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="c0044-199">Wenn eine Artikelvariante zuerst erzeugt wird, kann die Referenz zum ursprünglichen Artikel eine Fehlermeldung verursachen.</span><span class="sxs-lookup"><span data-stu-id="c0044-199">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="c0044-200">Prüfen von Daten nach dem Migrieren</span><span class="sxs-lookup"><span data-stu-id="c0044-200">Verifying Data After Migrating</span></span>
<span data-ttu-id="c0044-201">Wenn Sie sicherstellen möchten, dass Ihre Daten ordnungsgemäss migriert werden, können Sie die nächste Seiten in C5 und in [!INCLUDE[d365fin](includes/d365fin_md.md)]anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c0044-201">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="c0044-202">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="c0044-202">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="c0044-203">Zu verwendender Batchauftrag</span><span class="sxs-lookup"><span data-stu-id="c0044-203">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="c0044-204">Debitoreneinträge</span><span class="sxs-lookup"><span data-stu-id="c0044-204">Customer Entries</span></span>| <span data-ttu-id="c0044-205">Fibu-Erfassungsjournale</span><span class="sxs-lookup"><span data-stu-id="c0044-205">General Journals</span></span>| <span data-ttu-id="c0044-206">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="c0044-206">CUSTMIGR</span></span> |
|<span data-ttu-id="c0044-207">Kreditoreneinträge</span><span class="sxs-lookup"><span data-stu-id="c0044-207">Vendor Entries</span></span>| <span data-ttu-id="c0044-208">Fibu-Erfassungsjournale</span><span class="sxs-lookup"><span data-stu-id="c0044-208">General Journals</span></span>| <span data-ttu-id="c0044-209">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="c0044-209">VENDMIGR</span></span>|
|<span data-ttu-id="c0044-210">Lagerposten</span><span class="sxs-lookup"><span data-stu-id="c0044-210">Item Entries</span></span>| <span data-ttu-id="c0044-211">Artikelerfassungsjournale</span><span class="sxs-lookup"><span data-stu-id="c0044-211">Item Journals</span></span>| <span data-ttu-id="c0044-212">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="c0044-212">ITEMMIGR</span></span> |
|<span data-ttu-id="c0044-213">Fibuposten</span><span class="sxs-lookup"><span data-stu-id="c0044-213">G/L Entries</span></span>| <span data-ttu-id="c0044-214">Fibu-Erfassungsjournale</span><span class="sxs-lookup"><span data-stu-id="c0044-214">General Journals</span></span>| <span data-ttu-id="c0044-215">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="c0044-215">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="c0044-216">Datenmigration anhalten</span><span class="sxs-lookup"><span data-stu-id="c0044-216">Stopping Data Migration</span></span>
<span data-ttu-id="c0044-217">Sie können Datenmigration unterbrechen, indem Sie **Automatisches Beenden alle Migrationen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="c0044-217">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="c0044-218">Wenn Sie dies tun, werden alle offenen Migrationen beendet.</span><span class="sxs-lookup"><span data-stu-id="c0044-218">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0044-219">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0044-219">See Also</span></span>
<span data-ttu-id="c0044-220">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzenb](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c0044-220">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="c0044-221">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="c0044-221">Getting Started</span></span>](product-get-started.md) 

