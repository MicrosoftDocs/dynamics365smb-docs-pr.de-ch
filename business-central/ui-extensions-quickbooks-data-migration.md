---
title: QuickBooks-Migrations-Erweiterung verwenden | Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet werden, um Debitoren, Kreditoren, Artikel und Konten aus QuickBooks Desktop auf Business Central zu migrieren
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e53db4c1eef2a2f158f289e9f89ad291436a9b1a
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="the-quickbooks-data-migration-extension-for-business-central"></a><span data-ttu-id="f6347-103">Die QuickBooks Datenmigrations-Erweiterung für Business Central</span><span class="sxs-lookup"><span data-stu-id="f6347-103">The QuickBooks Data Migration Extension for Business Central</span></span>
<span data-ttu-id="f6347-104">Diese Erweiterung macht es einfach, Debitoren, Kreditoren und Artikel aus QuickBooks in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="f6347-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f6347-105">Wenn Ihr Geschäft QuickBooks heute verwendet, können Sie die Daten exportieren und dann eine unterstützte Einrichtungsanleitung öffnen, um die Daten hochzuladen und in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="f6347-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="f6347-106">Weitere Informationen finden Sie unter [Geschäftsdaten aus anderen Finanzsystemen zu importieren](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="f6347-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="f6347-107">Exportieren von Daten aus QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="f6347-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="f6347-108">Sie müssen einige oder alle Ihrer bestehenden Debitoren, Kreditoren, Lagerartikel und anderen Konten in ein Intuit-Austausch-Format (IIF) exportiert haben.</span><span class="sxs-lookup"><span data-stu-id="f6347-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="f6347-109">Die QuickBooks-Datenmigrationserweiterung umfasst eine Standardzuordnung von QuickBooks-Daten, sodass Sie Ihre bestehenden Daten verwenden können, um Ihre neue [!INCLUDE[d365fin](includes/d365fin_md.md)] Unternehmung zu testen.</span><span class="sxs-lookup"><span data-stu-id="f6347-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="f6347-110">Die Standardzuordnung ist in den meisten Fällen ausreichend, aber Sie können die Zuordnung in der unterstützten Einrichtung ändern.</span><span class="sxs-lookup"><span data-stu-id="f6347-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="f6347-111">In QuickBooks umfasst das Dateimenü ein Hilfsprogramm zu den Exporttarifen.</span><span class="sxs-lookup"><span data-stu-id="f6347-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="f6347-112">Zum Zweck des [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie die folgenden Listen exportieren:</span><span class="sxs-lookup"><span data-stu-id="f6347-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="f6347-113">Debitorenliste</span><span class="sxs-lookup"><span data-stu-id="f6347-113">Customer List</span></span>  
* <span data-ttu-id="f6347-114">Kreditorenliste</span><span class="sxs-lookup"><span data-stu-id="f6347-114">Vendor List</span></span>  
* <span data-ttu-id="f6347-115">Artikelliste</span><span class="sxs-lookup"><span data-stu-id="f6347-115">Item List</span></span>  
* <span data-ttu-id="f6347-116">Kontenliste</span><span class="sxs-lookup"><span data-stu-id="f6347-116">Account List</span></span>  

<span data-ttu-id="f6347-117">Die exportierten Daten werden IIF-Datei gespeichert, die Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] hochladen können.</span><span class="sxs-lookup"><span data-stu-id="f6347-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="f6347-118">Die QuickBooks-Datenmigrations-Erweiterung suchen</span><span class="sxs-lookup"><span data-stu-id="f6347-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="f6347-119">Die QuickBooks-Datenmigrationserweiterung ist eingerichtet und vorbereitet, um als integrierter Teil des unterstützten Setups bei der Datenmigration zu helfen.</span><span class="sxs-lookup"><span data-stu-id="f6347-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="f6347-120">Wenn Sie bereit sind jetzt anzufangen, und die Daten aus QuickBooks exportiert haben, wähen Sie ![Seite oder Bericht suchen](media/ui-search/search_small.png "Seiten- oder Berichtssymbol suchen") und geben **Unterstützte Einrichtung** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f6347-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="f6347-121">Wählen Sie **Migrieren von Geschäftsdaten** und anschliessend führen Sie die Schritte im Handbuch aus.</span><span class="sxs-lookup"><span data-stu-id="f6347-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6347-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6347-122">See Also</span></span>
[<span data-ttu-id="f6347-123">Geschäftsdaten aus anderen Finanzsystemen migrieren</span><span class="sxs-lookup"><span data-stu-id="f6347-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="f6347-124">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzenb](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="f6347-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

