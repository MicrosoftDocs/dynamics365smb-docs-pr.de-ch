---
title: Einrichten des Kontenplans | Microsoft Docs
description: "Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 69d4a8d4482999ed9d622d73654c3d8a4c3d8394
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="6e49c-103">Einrichten oder Ändern des Kontenplans</span><span class="sxs-lookup"><span data-stu-id="6e49c-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="6e49c-104">Der Kontenplan zeigt die Sachkonten an, die Ihre Finanzdaten speichern.</span><span class="sxs-lookup"><span data-stu-id="6e49c-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]<span data-ttu-id="6e49c-105">umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.</span><span class="sxs-lookup"><span data-stu-id="6e49c-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="6e49c-106">Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6e49c-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="6e49c-107">Konten hinzufügen oder ändern</span><span class="sxs-lookup"><span data-stu-id="6e49c-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="6e49c-108">Im Kontenplan können Sie jedes Fibukonto öffnen und Einstellungen hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="6e49c-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6e49c-109">Sie können ein Fibukonto löschen.</span><span class="sxs-lookup"><span data-stu-id="6e49c-109">You can delete a general ledger account.</span></span> <span data-ttu-id="6e49c-110">Bevor es gelöscht wird, müssen allerdings folgende Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="6e49c-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="6e49c-111">Der Saldo des Kontos muss Null betragen.</span><span class="sxs-lookup"><span data-stu-id="6e49c-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="6e49c-112">Das Feld **Löschen v. Sachkonten zul. vor** im Fenster **Finanzbuchhaltung Einrichtung** muss ausgefüllt sein, und das Konto darf keine Posten an oder nach diesem Datum enthalten.</span><span class="sxs-lookup"><span data-stu-id="6e49c-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="6e49c-113">Ist das Feld **Fibukontoverwendung prüfen** im Fenster **Finanzbuchhaltung Einrichtung** ausgewählt, darf dieses Konto nicht in Buchungsgruppen oder der Buchungsmatrix Einrichtung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e49c-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6e49c-114">verhindert, dass Sie ein Sachkonto löschen, in dem Daten gespeichert werden, die im Kontenplan erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6e49c-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6e49c-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e49c-115">See Also</span></span>
[<span data-ttu-id="6e49c-116">Die Finanzbuchhaltung und der Kontenplan</span><span class="sxs-lookup"><span data-stu-id="6e49c-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="6e49c-117">Verwalten von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="6e49c-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="6e49c-118">Arbeiten mit Dimensionen</span><span class="sxs-lookup"><span data-stu-id="6e49c-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="6e49c-119">Aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="6e49c-119">Importing from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="6e49c-120">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6e49c-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

