---
title: Migrieren von Daten von Dynamics GP mit der Datenmigrations-Erweiterung | Microsoft Docs
description: Verwenden Sie die GP-Datenmigrationserweiterung, um Debitoren, Kreditoren, Artikel und Konten von Dynamics GP auf Dynamics 365 Business edition zu migrieren.
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: b97c074b1283a981522b7a9651fcc7c552f1f930
ms.contentlocale: de-ch
ms.lasthandoff: 11/10/2017

---
# <a name="the-dynamics-gp-data-migration-extension-for-dynamics-365-business-edition"></a><span data-ttu-id="21400-103">Die Dynamics GP-Datenmigrations-Erweiterung für Dynamics 365 Business edition</span><span class="sxs-lookup"><span data-stu-id="21400-103">The Dynamics GP Data Migration Extension for Dynamics 365 Business edition</span></span> 
<span data-ttu-id="21400-104">Diese Erweiterung macht es einfach, Debitoren, Kreditoren und Artikel aus Dynamics GP in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="21400-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="21400-105">Wenn Ihr Geschäft Dynamics GP heute verwendet, können Sie die Daten exportieren und dann eine unterstützte Einrichtungsanleitung öffnen, um die Daten hochzuladen und in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="21400-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="21400-106">Weitere Informationen finden Sie unter [Geschäftsdaten aus anderen Finanzsystemen migrieren](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="21400-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="21400-107">Exportieren von Daten aus Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="21400-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="21400-108">Sie müssen Ihre bestehenden Debitoren, Kreditoren, Artikel und Konten mit der Exportdatenenfunktionalität in Dynamics GP exportiert haben.</span><span class="sxs-lookup"><span data-stu-id="21400-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="21400-109">Zum Zweck des [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie die folgenden Datentypen exportieren:</span><span class="sxs-lookup"><span data-stu-id="21400-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="21400-110">Konto</span><span class="sxs-lookup"><span data-stu-id="21400-110">Account</span></span>  
* <span data-ttu-id="21400-111">Debitor</span><span class="sxs-lookup"><span data-stu-id="21400-111">Customer</span></span>  
* <span data-ttu-id="21400-112">Option</span><span class="sxs-lookup"><span data-stu-id="21400-112">Item</span></span>  
* <span data-ttu-id="21400-113">Kreditor</span><span class="sxs-lookup"><span data-stu-id="21400-113">Vendor</span></span>  

<span data-ttu-id="21400-114">Die Dynamics GP-Datenmigrationserweiterung ordnet automatisch die exportierten Daten zu, so dass Sie Ihre bestehenden Daten rasch im [!INCLUDE[d365fin](includes/d365fin_md.md)] Unternehmen bereitstehen.</span><span class="sxs-lookup"><span data-stu-id="21400-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="21400-115">Während des Prozesses werden unterstützende Einrichtungsinformationen wie z. B. Buchungsgruppen erstellt.</span><span class="sxs-lookup"><span data-stu-id="21400-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="21400-116">Lagerartikel werden im System mit FIFO als die Bewertungsmethode mit Kosten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="21400-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="21400-117">Konten werden als das Hauptkontosegment von Dynamics GP mit Dimensionen eingerichtet, da sie keine[!INCLUDE[d365fin](includes/d365fin_long_md.md)] Kontensegmente haben.</span><span class="sxs-lookup"><span data-stu-id="21400-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="21400-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21400-118">See Also</span></span>
[<span data-ttu-id="21400-119">Geschäftsdaten aus anderen Finanzsystemen migrieren</span><span class="sxs-lookup"><span data-stu-id="21400-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="21400-120">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzenb](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="21400-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

