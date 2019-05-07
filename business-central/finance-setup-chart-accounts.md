---
title: Einrichten eines Kontenplans
description: Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 8c75a214691b7d9886958866517afbb1d68b6f60
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "920715"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="9aece-103">Einrichten oder Ändern des Kontenplans</span><span class="sxs-lookup"><span data-stu-id="9aece-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="9aece-104">Der Kontenplan zeigt die Sachkonten an, die Ihre Finanzdaten speichern.</span><span class="sxs-lookup"><span data-stu-id="9aece-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9aece-105">umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.</span><span class="sxs-lookup"><span data-stu-id="9aece-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="9aece-106">Sie können jedoch die Standardkonten ändern und neue Konten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9aece-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="9aece-107">Konten hinzufügen oder ändern</span><span class="sxs-lookup"><span data-stu-id="9aece-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="9aece-108">Im Kontenplan können Sie jedes Fibukonto öffnen und Einstellungen hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="9aece-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9aece-109">Sie können ein Fibukonto löschen.</span><span class="sxs-lookup"><span data-stu-id="9aece-109">You can delete a general ledger account.</span></span> <span data-ttu-id="9aece-110">Bevor es gelöscht wird, müssen allerdings folgende Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="9aece-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="9aece-111">Der Saldo des Kontos muss Null betragen.</span><span class="sxs-lookup"><span data-stu-id="9aece-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="9aece-112">Das Feld **Löschen v. Fibukonten zul. vor** auf der Seite **Finanzbuchhaltungs-Einrichtung:** muss ausgefüllt sein, und das Konto darf keine Posten an oder nach diesem Datum enthalten.</span><span class="sxs-lookup"><span data-stu-id="9aece-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="9aece-113">Ist das Feld **Fibukontoverwendung prüfen** auf der Seite **Finanzbuchhaltungs-Einrichtung:** ausgewählt, darf dieses Konto nicht in Buchungsgruppen oder der Buchungsmatrix Einrichtung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9aece-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9aece-114">verhindert, dass Sie ein Sachkonto löschen, in dem Daten gespeichert werden, die im Kontenplan erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9aece-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9aece-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9aece-115">See Also</span></span>
[<span data-ttu-id="9aece-116">Die Finanzbuchhaltung und der Kontenplan</span><span class="sxs-lookup"><span data-stu-id="9aece-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="9aece-117">Verwalten von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="9aece-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="9aece-118">Arbeiten mit Dimensionen</span><span class="sxs-lookup"><span data-stu-id="9aece-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="9aece-119">Daten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="9aece-119">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="9aece-120">Arbeiten mit Kontenschema</span><span class="sxs-lookup"><span data-stu-id="9aece-120">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="9aece-121">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9aece-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
