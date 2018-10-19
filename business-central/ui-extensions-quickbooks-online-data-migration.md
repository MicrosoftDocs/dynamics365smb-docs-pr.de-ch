---
title: QuickBooks-Migrations-Erweiterung verwenden | Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Debitoren, Kreditoren, Artikel und Konten aus QuickBooks Online auf Business Central zu migrieren
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e9b0a481f16d8f0bc1647640b62a81b3ea441028
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---

# <a name="the-quickbooks-online-data-migration-extension"></a><span data-ttu-id="799b5-103">Die QuickBooks-Online-Datenmigrations-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="799b5-103">The QuickBooks Online Data Migration Extension</span></span>
<span data-ttu-id="799b5-104">Diese Erweiterung ist im unterstützten Einrichtungshandbuch **Datenmigration** enthalten, um Ihnen zu helfen, wichtige Geschäftsdaten von QuickBooks in Online zu [!INCLUDE[d365fin](includes/d365fin_md.md)]migrieren.</span><span class="sxs-lookup"><span data-stu-id="799b5-104">This extension is included in the **Data Migration** assisted setup guide to help you migrate important business data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="799b5-105">Dies ist beispielsweise dann nützlich, wenn Ihr Unternehmen wächst und Sie sich entschieden haben, Ihre Geschäftsführungs-App zu aktualisieren, indem Sie mit [!INCLUDE[d365fin](includes/d365fin_md.md)]  verwenden.</span><span class="sxs-lookup"><span data-stu-id="799b5-105">For example, this is useful when your business is growing, and you've decided to upgrade your business management app by starting to use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="what-data-can-i-import-from-quickbooks-online"></a><span data-ttu-id="799b5-106">Welche Daten kann ich von QuickBooks online importieren?</span><span class="sxs-lookup"><span data-stu-id="799b5-106">What data can I import from QuickBooks Online?</span></span>
<span data-ttu-id="799b5-107">Sie können die folgenden Daten aus QuickBooks online importieren [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="799b5-107">You can import the following data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

* <span data-ttu-id="799b5-108">Debitoren</span><span class="sxs-lookup"><span data-stu-id="799b5-108">Customers</span></span>
* <span data-ttu-id="799b5-109">Kreditoren</span><span class="sxs-lookup"><span data-stu-id="799b5-109">Vendors</span></span>
* <span data-ttu-id="799b5-110">Arti&kel</span><span class="sxs-lookup"><span data-stu-id="799b5-110">Items</span></span>
* <span data-ttu-id="799b5-111">Kontenplan</span><span class="sxs-lookup"><span data-stu-id="799b5-111">Chart of accounts</span></span>
* <span data-ttu-id="799b5-112">Saldovortragtransaktion im Fibuposten</span><span class="sxs-lookup"><span data-stu-id="799b5-112">Beginning balance transaction in the general ledger</span></span>
* <span data-ttu-id="799b5-113">Verfügbare Mengen für Lagerartikel</span><span class="sxs-lookup"><span data-stu-id="799b5-113">On-hand quantities for inventory items</span></span>
* <span data-ttu-id="799b5-114">Offene Belege für Debitoren und Kreditoren, wie beispielsweise Rechnungen, Gutschriften und Zahlungen</span><span class="sxs-lookup"><span data-stu-id="799b5-114">Open documents for customers and vendors, such as invoices, credit memos, and payments</span></span>

<span data-ttu-id="799b5-115">Es migrieren nur Gesamtbeträge auf Einkaufs- und Verkaufsbelegen.</span><span class="sxs-lookup"><span data-stu-id="799b5-115">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="799b5-116">Wir aktualisieren keine teilweise bezahlten Beträge.</span><span class="sxs-lookup"><span data-stu-id="799b5-116">We do not update partially paid amounts.</span></span> <span data-ttu-id="799b5-117">Wenn ein Debitor 300 von insgesamt 500 Dollar einer Verkaufsrechnung bezahlt hat, migrieren wir die vollständigen 500.</span><span class="sxs-lookup"><span data-stu-id="799b5-117">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="799b5-118">Wenn Sie Teilzahlungen erhalten, müssen Sie diese manuell aktualisieren, entweder, vor oder nach dem Sie Daten migrieren.</span><span class="sxs-lookup"><span data-stu-id="799b5-118">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="799b5-119">Es ist empfehlenswert, ausstehende Transaktionen anzuwenden, bevor Sie migrieren, das ist einfacher danach.</span><span class="sxs-lookup"><span data-stu-id="799b5-119">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]  
>   <span data-ttu-id="799b5-120">Wir migrieren keine Einkaufsbestellungen oder Verkaufsaufträge.</span><span class="sxs-lookup"><span data-stu-id="799b5-120">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="799b5-121">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="799b5-121">Before you start</span></span>
<span data-ttu-id="799b5-122">Ein wichtiger Teil des Migrationsvorgangs ist es, Konten anzugeben, um Transaktionen zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="799b5-122">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="799b5-123">Es ist empfehlenswert, diese Zuordnung zu planen, bevor Sie Daten migrieren.</span><span class="sxs-lookup"><span data-stu-id="799b5-123">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="799b5-124">Beispielsweise die Konten, die Sie für Transaktionen buchen:</span><span class="sxs-lookup"><span data-stu-id="799b5-124">For example, the accounts where you post transactions for:</span></span>  

* <span data-ttu-id="799b5-125">Der Verkauf von Artikeln oder Services an einen Kunden.</span><span class="sxs-lookup"><span data-stu-id="799b5-125">The sale of items or services to customers.</span></span>
* <span data-ttu-id="799b5-126">Der Kauf von Waren oder Dienste von einem Kreditor.</span><span class="sxs-lookup"><span data-stu-id="799b5-126">The purchase of items or services from vendors.</span></span>  
* <span data-ttu-id="799b5-127">Änderungen im Fibuposten.</span><span class="sxs-lookup"><span data-stu-id="799b5-127">Adjustments in the general ledger.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="799b5-128">erfordert, dass Sachkonten die Kontonummern haben, die ihm zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="799b5-128">requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="799b5-129">Überprüfen Sie, ob Sie Kontonummern Ihren Konten in QuickBooks online zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="799b5-129">Make sure that account numbers are assigned to your accounts in QuickBooks Online.</span></span>

<span data-ttu-id="799b5-130">Wenn Transaktionen in QuickBooks online Steuerbeträge haben, müssen Sie eine MwSt einrichten für Ihre Steuerzuständigkeiten in, [!INCLUDE[d365fin](includes/d365fin_md.md)] bevor Sie Buchungen durchführen können.</span><span class="sxs-lookup"><span data-stu-id="799b5-130">If transactions in QuickBooks Online have tax amounts, you must set up a tax account for your tax jurisdictions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you can post transactions.</span></span>

## <a name="how-do-i-start-using-the-extension"></a><span data-ttu-id="799b5-131">Wie beginne ich, die Erweiterung zu nutzen?</span><span class="sxs-lookup"><span data-stu-id="799b5-131">How do I start using the extension?</span></span>
<span data-ttu-id="799b5-132">Erste Schritte sind einfach.</span><span class="sxs-lookup"><span data-stu-id="799b5-132">Getting started is easy.</span></span> <span data-ttu-id="799b5-133">Sie müssen nur das unterstütze Einrichtungshandbuch **Datenmigration** ausführen.</span><span class="sxs-lookup"><span data-stu-id="799b5-133">All you need to do is run the **Data Migration** assisted setup guide.</span></span> <span data-ttu-id="799b5-134">So geht es:</span><span class="sxs-lookup"><span data-stu-id="799b5-134">Here's how:</span></span>

1. <span data-ttu-id="799b5-135">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Unterstütztes Setup** ein, und wählen dann **Geschäftsdaten migrieren** aus.</span><span class="sxs-lookup"><span data-stu-id="799b5-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Assisted Setup**, and then choose **Migrate business data**.</span></span>
2. <span data-ttu-id="799b5-136">Befolgen Sie die Anweisungen für jeden Schritt im unterstützten Anleitungshandbuch.</span><span class="sxs-lookup"><span data-stu-id="799b5-136">Follow the instructions on each step in the assisted setup guide.</span></span>

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="799b5-137">Was tue ich, nachdem ich Daten migriert habe?</span><span class="sxs-lookup"><span data-stu-id="799b5-137">What do I do after I migrate data?</span></span>
<span data-ttu-id="799b5-138">Nachdem Sie Daten migriert haben, haben die Transaktionen den Status **Nicht gebucht**, sodass Sie sie überprüfen und Korrekturen vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="799b5-138">After you migrate data, transactions have the status **Unposted**, so you can review them and make adjustments.</span></span> <span data-ttu-id="799b5-139">Um die Transaktionen zu überprüfen, wechseln Sie zur Seite in der Sie normalerweise suchen müssen.</span><span class="sxs-lookup"><span data-stu-id="799b5-139">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="799b5-140">Beispielsweise um nicht gebuchten Verkaufsrechnungen zu überprüfen, wechseln Sie ins Fenster **Verkaufsrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="799b5-140">For example, to review unposted sales invoices, go to the **Sales Invoices** window.</span></span> <span data-ttu-id="799b5-141">Um Zahlungsausgangs Buch.-Blätter zu überprüfen, wechseln Sie ins Fenster **Zlg.-Ausg. Buch.-Blätter**.</span><span class="sxs-lookup"><span data-stu-id="799b5-141">To review payment journals, go to the **Payment Journals** window.</span></span>   

<span data-ttu-id="799b5-142">Es gibt mehrere Dinge, die Sie durchführen sollten:</span><span class="sxs-lookup"><span data-stu-id="799b5-142">There are a few things in particular that you should do:</span></span>

* <span data-ttu-id="799b5-143">Wenn die Transaktionen in QuickBooks online Markup oder Rabattbeträge aufweisen, müssen Sie die Beträge zu den verwandten Transaktionen manuell hinzufügen, [!INCLUDE[d365fin](includes/d365fin_md.md)] bevor Sie diese buchen.</span><span class="sxs-lookup"><span data-stu-id="799b5-143">If the transactions in QuickBooks Online had markup or discount amounts, you must manually add the amounts to the related transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you post them.</span></span>
* <span data-ttu-id="799b5-144">Wenn Sie MWST verwenden, können Sie eine Geschäftsbuchungsgruppe und eine Produktbuchungsgruppe "Buchungsmatrix Einrichtung" hinzufügen, sodass Sie MWST-Beträge buchen können.</span><span class="sxs-lookup"><span data-stu-id="799b5-144">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
* <span data-ttu-id="799b5-145">Prüfen Sie die Startkapitale für Konten im Fibuposten.</span><span class="sxs-lookup"><span data-stu-id="799b5-145">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="799b5-146">QuickBooks online speichert nicht den aktuellen Saldo für alle Konten, daher müssen Sie möglicherweise Startkapitale korrigieren.</span><span class="sxs-lookup"><span data-stu-id="799b5-146">QuickBooks Online does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="799b5-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="799b5-147">See Also</span></span>
[<span data-ttu-id="799b5-148">Geschäftsdaten aus anderen Finanzsystemen migrieren</span><span class="sxs-lookup"><span data-stu-id="799b5-148">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="799b5-149">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzenb](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="799b5-149">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  

