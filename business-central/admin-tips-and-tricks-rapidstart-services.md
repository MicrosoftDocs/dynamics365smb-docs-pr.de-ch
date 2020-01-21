---
title: Tipps und Tricks – RapidStart Services | Microsoft Docs
description: Wenn Sie Unternehmen mit RapidStart Services konfigurieren, gibt es einige Tipps und Tricks, die Sie für eine reibungslose Implementierung nutzen können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 890a6e87ec25293232f089b68e57a577fec6aa56
ms.sourcegitcommit: 53565fea987af861f3846e5c1e0e868c279aeb30
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/20/2019
ms.locfileid: "2918180"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="9a5e8-103">Tipps und Tricks: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="9a5e8-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="9a5e8-104">Wenn Sie Unternehmen mit RapidStart Services konfigurieren, gibt es einige Tipps und Tricks, die Sie für eine reibungslose Implementierung nutzen können.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="9a5e8-105">Konfigurationsvorlagen nutzen</span><span class="sxs-lookup"><span data-stu-id="9a5e8-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="9a5e8-106">Mit Konfigurationsvorlagen können Sie Ihren Implementierungsprozess optimieren.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="9a5e8-107">Sie können damit ähnliche Debitoren in Segmente einbinden und dann ein Implementierungsprotokoll entwickeln, das alle Debitoren in einem Segment in ähnlicher Weise behandelt.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="9a5e8-108">Auf diese Art können Sie bei jedem Segment eine bestimmte Vorkonfiguration anwenden und mit einer schnelle Implementierung fortfahren.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="9a5e8-109">Konfigurationsfragebögen</span><span class="sxs-lookup"><span data-stu-id="9a5e8-109">Configuration questionnaires</span></span>  
<span data-ttu-id="9a5e8-110">Um das Ausfüllen eines Konfigurationsfragebogens zu unterstützen, erwägen Sie, Standardantworten zu definieren, um auf bewährte Methoden hinzuweisen.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="9a5e8-111">Stapelerstellung von Erfassungsjournalzeilen</span><span class="sxs-lookup"><span data-stu-id="9a5e8-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="9a5e8-112">Es wird empfohlen, die Datenmigrationswerkzeuge für die Migration von Blatteinträgen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="9a5e8-113">Bei der Erstellung von Erfassungsjournalzeilen mit der Stapelverarbeitung steht andernfalls nur ein begrenzter Bereich zur Verfügung, und es werden nur Verzugsfelder in einem Erfassungsjournal generiert.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="9a5e8-114">Der Rest des Erfassungsjournals muss anschliessend manuell ausgefüllt werden werden.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="9a5e8-115">Migrierung von Transaktionen</span><span class="sxs-lookup"><span data-stu-id="9a5e8-115">Migrating transactions</span></span>  
<span data-ttu-id="9a5e8-116">Es wird empfohlen, Eröffnungssalden in der folgenden Reihenfolge in mehreren Schritten zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-116">We recommend that you migrate opening balances in the following order.</span></span> <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines--> 

1.  <span data-ttu-id="9a5e8-117">Migrieren Sie die Eröffnungssalden des Fibukontos, ohne die untergeordneten Konten des Fibukontos zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="9a5e8-118">Verwenden Sie bestimmte Ausgleichskonten für Eröffnungssalden, wobei pro untergeordnetes Sachkonto eines eingerichtet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="9a5e8-119">Richten Sie für direkte Buchungen Ausgleichskonten ein.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="9a5e8-120">Migrieren Sie offene Debitorenposten.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-120">Migrate open customer ledger entries.</span></span>  <!--work on these-->
3.  <span data-ttu-id="9a5e8-121">Migrieren Sie offene Lagerposten.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="9a5e8-122">Migrieren Sie offene Anlagenposten.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9a5e8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a5e8-123">See Also</span></span>  
[<span data-ttu-id="9a5e8-124">Mandanten mit RapidStart Services einrichten</span><span class="sxs-lookup"><span data-stu-id="9a5e8-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="9a5e8-125">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="9a5e8-125">Administration</span></span>](admin-setup-and-administration.md)
