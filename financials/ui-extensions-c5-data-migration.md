---
title: C5-Datenmigrations-Erweiterung verwenden | Microsoft Docs
description: Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Fibukonten von Microsoft Dynamics C5 2012 zu Financials zu migrieren.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d3b8d3d01ce75da59c1cce873077955776963ce9
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---

# <a name="the-c5-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="0c5c1-103">Die C5-Datenmigrations-Erweiterung für Finance and Operations, Business Edition</span><span class="sxs-lookup"><span data-stu-id="0c5c1-103">The C5 Data Migration Extension for Finance and Operations, Business edition</span></span>
<span data-ttu-id="0c5c1-104">Verwenden Sie diese Erweiterung, um Debitoren, Kreditoren, Artikel und Fibukonten von Microsoft Dynamics C5 2012 zu [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0c5c1-105">Sie können historische Posten auch für Fibukonten migrieren.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="0c5c1-106">Der Mandant darf in [!INCLUDE[d365fin](includes/d365fin_md.md)] keine Daten in enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="0c5c1-107">Nachdem Sie mit der Migration begonnen haben, erstellen Sie keine Debitoren, Kreditoren, Artikel oder Konten, bis die Migration beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

##<a name="what-data-is-migrated"></a><span data-ttu-id="0c5c1-108">Welche Daten migriert?</span><span class="sxs-lookup"><span data-stu-id="0c5c1-108">What Data is Migrated?</span></span>
<span data-ttu-id="0c5c1-109">Die folgenden Daten werden für jede Einheit migriert:</span><span class="sxs-lookup"><span data-stu-id="0c5c1-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="0c5c1-110">**Debitoren**</span><span class="sxs-lookup"><span data-stu-id="0c5c1-110">**Customers**</span></span>
* <span data-ttu-id="0c5c1-111">Ort</span><span class="sxs-lookup"><span data-stu-id="0c5c1-111">Location</span></span>
* <span data-ttu-id="0c5c1-112">Land</span><span class="sxs-lookup"><span data-stu-id="0c5c1-112">Country</span></span>
* <span data-ttu-id="0c5c1-113">Kunden-Dimensionen (Abteilung, Kostenträger, Kostenstelle)</span><span class="sxs-lookup"><span data-stu-id="0c5c1-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="0c5c1-114">Lieferbedingungsmethode</span><span class="sxs-lookup"><span data-stu-id="0c5c1-114">Shipment method</span></span>
* <span data-ttu-id="0c5c1-115">Vertriebsmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="0c5c1-115">Sales Person</span></span>
* <span data-ttu-id="0c5c1-116">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="0c5c1-116">Payment terms</span></span>
* <span data-ttu-id="0c5c1-117">Zahlungsform</span><span class="sxs-lookup"><span data-stu-id="0c5c1-117">Payment method</span></span>
* <span data-ttu-id="0c5c1-118">Debitorenpreisgruppe</span><span class="sxs-lookup"><span data-stu-id="0c5c1-118">Customer price group</span></span>
* <span data-ttu-id="0c5c1-119">Debitorenrechnungsrabatt</span><span class="sxs-lookup"><span data-stu-id="0c5c1-119">Customer invoice discount</span></span>

<span data-ttu-id="0c5c1-120">Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:</span><span class="sxs-lookup"><span data-stu-id="0c5c1-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="0c5c1-121">Debitorenbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0c5c1-121">Customer posting setup</span></span>
* <span data-ttu-id="0c5c1-122">Fibu Erf.-Journalname</span><span class="sxs-lookup"><span data-stu-id="0c5c1-122">General journal batch</span></span>
* <span data-ttu-id="0c5c1-123">Migrieren Sie offene Debitorenposten (Kundenbucheinträge)</span><span class="sxs-lookup"><span data-stu-id="0c5c1-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="0c5c1-124">**Kreditoren**</span><span class="sxs-lookup"><span data-stu-id="0c5c1-124">**Vendors**</span></span>
* <span data-ttu-id="0c5c1-125">Ort</span><span class="sxs-lookup"><span data-stu-id="0c5c1-125">Location</span></span>
* <span data-ttu-id="0c5c1-126">Land</span><span class="sxs-lookup"><span data-stu-id="0c5c1-126">Country</span></span>
* <span data-ttu-id="0c5c1-127">Kunden-Dimensionen (Abteilung, Kostenträger, Kostenstelle)</span><span class="sxs-lookup"><span data-stu-id="0c5c1-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="0c5c1-128">Rechnungsrabatt</span><span class="sxs-lookup"><span data-stu-id="0c5c1-128">Invoice discount</span></span>
* <span data-ttu-id="0c5c1-129">Lieferbedingungsmethode</span><span class="sxs-lookup"><span data-stu-id="0c5c1-129">Shipment method</span></span>
* <span data-ttu-id="0c5c1-130">Einkäufer</span><span class="sxs-lookup"><span data-stu-id="0c5c1-130">Purchaser</span></span>
* <span data-ttu-id="0c5c1-131">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="0c5c1-131">Payment terms</span></span>
* <span data-ttu-id="0c5c1-132">Zahlungsform</span><span class="sxs-lookup"><span data-stu-id="0c5c1-132">Payment method</span></span>
* <span data-ttu-id="0c5c1-133">Kreditorenrechnungsrabatte</span><span class="sxs-lookup"><span data-stu-id="0c5c1-133">Vendor invoice discount</span></span>

<span data-ttu-id="0c5c1-134">Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:</span><span class="sxs-lookup"><span data-stu-id="0c5c1-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="0c5c1-135">Kreditorenbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0c5c1-135">Vendor posting setup</span></span>
* <span data-ttu-id="0c5c1-136">Fibu Erf.-Journalname</span><span class="sxs-lookup"><span data-stu-id="0c5c1-136">General journal batch</span></span>
* <span data-ttu-id="0c5c1-137">Öffnen Sie das Fenster Transaktionen (Kreditorenposten)</span><span class="sxs-lookup"><span data-stu-id="0c5c1-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="0c5c1-138">**Arti&kel**</span><span class="sxs-lookup"><span data-stu-id="0c5c1-138">**Items**</span></span>
* <span data-ttu-id="0c5c1-139">Ort</span><span class="sxs-lookup"><span data-stu-id="0c5c1-139">Location</span></span>
* <span data-ttu-id="0c5c1-140">Land</span><span class="sxs-lookup"><span data-stu-id="0c5c1-140">Country</span></span>
* <span data-ttu-id="0c5c1-141">Element-Dimensionen (Abteilung, Kostenträger, Kostenstelle)</span><span class="sxs-lookup"><span data-stu-id="0c5c1-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="0c5c1-142">VK-Zeilenrabatte</span><span class="sxs-lookup"><span data-stu-id="0c5c1-142">Sales line discounts</span></span>
* <span data-ttu-id="0c5c1-143">Debitorenrabattgruppen</span><span class="sxs-lookup"><span data-stu-id="0c5c1-143">Customer discount groups</span></span>
* <span data-ttu-id="0c5c1-144">Artikelrabattgruppen</span><span class="sxs-lookup"><span data-stu-id="0c5c1-144">Item discount groups</span></span>
* <span data-ttu-id="0c5c1-145">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="0c5c1-145">Sales price</span></span>
* <span data-ttu-id="0c5c1-146">Zollposition</span><span class="sxs-lookup"><span data-stu-id="0c5c1-146">Tariff number</span></span>
* <span data-ttu-id="0c5c1-147">Einheiten</span><span class="sxs-lookup"><span data-stu-id="0c5c1-147">Units of measure</span></span>
* <span data-ttu-id="0c5c1-148">Artikelverfolgungscode</span><span class="sxs-lookup"><span data-stu-id="0c5c1-148">Item tracking code</span></span>
* <span data-ttu-id="0c5c1-149">Debitorenpreisgruppe</span><span class="sxs-lookup"><span data-stu-id="0c5c1-149">Customer price group</span></span>

<span data-ttu-id="0c5c1-150">Wenn Sie Konten migrieren, werden auch die folgenden Daten migriert:</span><span class="sxs-lookup"><span data-stu-id="0c5c1-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="0c5c1-151">Lagerbuchungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="0c5c1-151">Inventory posting setup</span></span>
* <span data-ttu-id="0c5c1-152">Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="0c5c1-152">General posting setup</span></span>
* <span data-ttu-id="0c5c1-153">Artikel Erf.-Journalname</span><span class="sxs-lookup"><span data-stu-id="0c5c1-153">Item journal batch</span></span>
* <span data-ttu-id="0c5c1-154">Öffnen Sie das Fenster Transaktionen (Lagerposten)</span><span class="sxs-lookup"><span data-stu-id="0c5c1-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="0c5c1-155">Wenn es offene Transaktionen gibt, die Fremdwährungen verwenden, werden die Wechselkurse für alle Währungen auch migriert.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="0c5c1-156">Andere Wechselkurse werden nicht migriert.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-156">Other exchange rates are not migrated.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="0c5c1-157">Um Daten zu migrieren</span><span class="sxs-lookup"><span data-stu-id="0c5c1-157">To migrate data</span></span>
<span data-ttu-id="0c5c1-158">Es gibt nur einige wenige Schritte, um die Daten aus C5 zu exportieren und sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu importieren:</span><span class="sxs-lookup"><span data-stu-id="0c5c1-158">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="0c5c1-159">In C5 verwenden Sie die Funktion **Datenbank exportieren**, um die Daten zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-159">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="0c5c1-160">Senden Sie dann den Exportordner an einen komprimierten (gezippten) Ordner.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-160">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="0c5c1-161">Wählen Sie dann in [!INCLUDE[d365fin](includes/d365fin_md.md)] das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben Sie **Datenmigration** ein und wählen dann **Datenmigration**.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-161">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="0c5c1-162">Schliessen Sie die Schritte im unterstützten Setup ab.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-162">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="0c5c1-163">Stellen Sie sicher, dass Sie**Importieren aus Microsoft Dynamcis C5 2012** als die Datenquelle auswählen.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-163">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="0c5c1-164">Mandanten fügen häufig Felder hinzu, um C5 für ihren jeweiligen Geschäftsbereich anzupassen.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-164">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="0c5c1-165"> migriert nicht Daten vom benutzerdefinierten Feldern.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-165"> does not migrate data from custom fields.</span></span> <span data-ttu-id="0c5c1-166">Die Migration schlägt fehl, wenn Sie mehr als 10 benutzerdefinierte Felder haben.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-166">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="0c5c1-167">Zeigt den Status der Datenmigration an</span><span class="sxs-lookup"><span data-stu-id="0c5c1-167">Viewing the Status of the Migration</span></span>
<span data-ttu-id="0c5c1-168">Verwenden Sie die Seite **Datenmigrations-Übersicht**, um den Erfolg der Migration zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-168">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="0c5c1-169">Die Seite zeigt Informationen wie die Anzahl von Einheiten, die migriert wurde, den Status der Migration und die Anzahl von Artikeln an, die migriert wurden und ob sie erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-169">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="0c5c1-170">Sie zeigt auch die Anzahl von Fehlern, Sie können überprüfen, was schief ging und macht es wenn möglich einfach, zur Einheit zu gehen und das Problem zu lösen.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-170">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="0c5c1-171">Weitere Informationen finden Sie im nächsten Abschnitt dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-171">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="0c5c1-172">Während Sie auf die Ergebnisse der Migration warten, müssen Sie die Seite aktualisieren, um die Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-172">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="0c5c1-173">Nachbesserung</span><span class="sxs-lookup"><span data-stu-id="0c5c1-173">Correcting Errors</span></span>
<span data-ttu-id="0c5c1-174">Falls etwas schief geht und ein Fehler auftritt, wird das **Status** Feld **Abgeschlossen mit Fehlern** angezeigt und das Feld **Fehlerzahl** zeigt an, wie viele es sind.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-174">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="0c5c1-175">Um eine Liste der Fehler anzuzeigen, können Sie die Seite öffnen indem Sie **Datenmigrations-Fehler** auswählen:</span><span class="sxs-lookup"><span data-stu-id="0c5c1-175">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="0c5c1-176">Die Nummer im Feld **Fehlerzahl** für die Einheit.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-176">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="0c5c1-177">Die Einheit und dann die Aktion **Fehler anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-177">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="0c5c1-178">Um auf der Seite **Datenmigrations-Fehler** einen Fehler zu korrigieren, können Sie eine Fehlermeldung auswählen, und dann **Datensatz bearbeiten** auswählen, um die Seite zu öffnen, welche de Daten für die migrierte Einheit enthält.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-178">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="0c5c1-179">Nachdem Sie eines oder mehrere Fehler korrigiert haben, können Sie **Migrieren von** wählen, um nur die Einheiten zu migrieren, die Sie korrigierten, ohne die Migration vollständig erneut durchführen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-179">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="0c5c1-180">Wenn Sie mehr als einen Fehler korrigiert haben, können Sie die Funktion **Weitere auswählen** verwenden, um mehrere Zeilen auszuwählen, um diese zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-180">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="0c5c1-181">Wenn es Fehler gibt, die nicht zur Korrektur wichtig sind, können Sie diese auswählen und dann **Auswahl überspringen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-181">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="0c5c1-182">Wenn Sie Artikel haben, die in der Stückliste enthalten sind, müssen Sie diese mehrmals migrieren, wenn der ursprüngliche Artikel nicht vor den Varianten erstellt wird, auf die sie verweist.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-182">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="0c5c1-183">Wenn eine Artikelvariante zuerst erzeugt wird, kann die Referenz zum ursprünglichen Artikel eine Fehlermeldung verursachen.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-183">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="0c5c1-184">Prüfen von Daten nach dem Migrieren</span><span class="sxs-lookup"><span data-stu-id="0c5c1-184">Verifying Data After Migrating</span></span>
<span data-ttu-id="0c5c1-185">Wenn Sie sicherstellen möchten, dass Ihre Daten ordnungsgemäss migriert werden, können Sie die nächste Seiten in C5 und in [!INCLUDE[d365fin](includes/d365fin_md.md)]anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-185">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="0c5c1-186">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="0c5c1-186">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="0c5c1-187">Debitoreneinträge</span><span class="sxs-lookup"><span data-stu-id="0c5c1-187">Customer Entries</span></span>| <span data-ttu-id="0c5c1-188">Fibu Erfassungsjournale</span><span class="sxs-lookup"><span data-stu-id="0c5c1-188">General Journals</span></span>|
|<span data-ttu-id="0c5c1-189">Kreditoreneinträge</span><span class="sxs-lookup"><span data-stu-id="0c5c1-189">Vendor Entries</span></span>| <span data-ttu-id="0c5c1-190">Fibu Erfassungsjournale</span><span class="sxs-lookup"><span data-stu-id="0c5c1-190">General Journals</span></span>|
|<span data-ttu-id="0c5c1-191">Lagerposten</span><span class="sxs-lookup"><span data-stu-id="0c5c1-191">Item Entries</span></span>| <span data-ttu-id="0c5c1-192">Artikel Erfassungsjournale</span><span class="sxs-lookup"><span data-stu-id="0c5c1-192">Item Journals</span></span>|

<span data-ttu-id="0c5c1-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], wird der Stapel für die migrierten Daten **C5MIGRATE** genannt.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span>

## <a name="stopping-data-migration"></a><span data-ttu-id="0c5c1-194">Datenmigration anhalten</span><span class="sxs-lookup"><span data-stu-id="0c5c1-194">Stopping Data Migration</span></span>
<span data-ttu-id="0c5c1-195">Sie können Datenmigration unterbrechen, indem Sie **Automatisches Beenden alle Migrationen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-195">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="0c5c1-196">Wenn Sie dies tun, werden alle offenen Migrationen beendet.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-196">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c5c1-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c5c1-197">See Also</span></span>
<span data-ttu-id="0c5c1-198">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzenb](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="0c5c1-198">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="0c5c1-199">[Willkommen bei [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="0c5c1-199">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

