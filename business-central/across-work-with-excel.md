---
title: Anzeigen und Arbeit in Excel aus Business Central | Microsoft Docs
description: Mehr erfahren, wie Sie die Finanzaufstellungen in Microsoft Excel von  Business Central für eine Analyse der Daten öffnen können.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 01/13/2020
ms.author: jswymer
ms.openlocfilehash: 9fd5c6c242932d75addcfa5c1811bdd1aff99a94
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953070"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="4de06-103">Anzeigen und Arbeit in Excel aus Business Central</span><span class="sxs-lookup"><span data-stu-id="4de06-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="4de06-104">Mit Seiten, die eine Liste der Datensätze in den Zeilen und Spalten anzeigen, wie eine Liste von Debitoren von Verkaufsaufträgen oder Rechnungen können Sie die Daten mithilfe von Microsoft Excel anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4de06-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="4de06-105">Dazu haben Sie zwei Optionen.</span><span class="sxs-lookup"><span data-stu-id="4de06-105">To do this, you have two options.</span></span> <span data-ttu-id="4de06-106">Sie können entweder die **In Excel öffnen** Aktion oder die **Bearbeiten Sie in Excel** Aktion dieser Seite auswählen.</span><span class="sxs-lookup"><span data-stu-id="4de06-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="4de06-107">Der Unterschied zwischen den beiden Methoden ist der folgende:</span><span class="sxs-lookup"><span data-stu-id="4de06-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="4de06-108">In Excel öffnen</span><span class="sxs-lookup"><span data-stu-id="4de06-108">Open in Excel</span></span>

- <span data-ttu-id="4de06-109">Mit dieser Aktion respektiert Excel alle Filter auf der Seite, die die angezeigten Datensätze einschränken.</span><span class="sxs-lookup"><span data-stu-id="4de06-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="4de06-110">Das bedeutet, dass die Excel-Arbeitsmappe die gleichen Zeilen und Spalten enthält, die auf der Seite in [!INCLUDE[prodshort](includes/prodshort.md)] erscheinen.</span><span class="sxs-lookup"><span data-stu-id="4de06-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="4de06-111">Sie können Änderungen mit Datensätzen in Excel vornehmen, aber Sie können die Änderungen nicht auf  [!INCLUDE[prodshort](includes/prodshort.md)] veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="4de06-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="4de06-112">Sie können die Änderungen in die Excel-Datei nur auf dem Computer speichern.</span><span class="sxs-lookup"><span data-stu-id="4de06-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="4de06-113">Diese Aktion geht auf Windows und Mac Os.</span><span class="sxs-lookup"><span data-stu-id="4de06-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="4de06-114">Für [!INCLUDE[prodshort](includes/prodshort.md)] lokal ist die Aktion **In Excel öffnen** standardmässig verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4de06-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="4de06-115">Wenn Sie jedoch [!INCLUDE [prodshort](includes/prodshort.md)] lokal für die Bearbeitung von Daten in Excel einrichten, wird die Aktion **In Excel öffnen** durch die Aktion **In Excel bearbeiten** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="4de06-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="4de06-116">In Excel bearbeiten</span><span class="sxs-lookup"><span data-stu-id="4de06-116">Edit in Excel</span></span>

- <span data-ttu-id="4de06-117">Mit dieser Aktion berücksichtigt Excel die meisten Filter auf der Seite, die die angezeigten Datensätze einschränken.</span><span class="sxs-lookup"><span data-stu-id="4de06-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="4de06-118">Das bedeutet, dass die Excel-Arbeitsmappe fast die gleichen Datensätze und Spalten enthält.</span><span class="sxs-lookup"><span data-stu-id="4de06-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="4de06-119">Der Vorteil der **Bearbeiten Sie in Excel** Aktion ist, dass es Sie Änderungen mit Datensätzen in Excel vornimmt und die Änderungen zurück in [!INCLUDE[prodshort](includes/prodshort.md)] veröffentlichen können,</span><span class="sxs-lookup"><span data-stu-id="4de06-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="4de06-120">Das geht nur auf Windows; nicht Mac Os.</span><span class="sxs-lookup"><span data-stu-id="4de06-120">It only works on Windows; not macOS.</span></span>

<span data-ttu-id="4de06-121">Diese wurde 2019 in der Release-Welle 2 erweitert.</span><span class="sxs-lookup"><span data-stu-id="4de06-121">This was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="4de06-122">Weitere Informationen finden Sie unter [Erweiterungen der Excel-Integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="4de06-122">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="4de06-123">Für [!INCLUDE[prodshort](includes/prodshort.md)] lokal ist die Aktion **In Excel bearbeiten** nur verfügbar, wenn das Excel-Add-In von Ihrem Administrator konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="4de06-123">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator.</span></span> <span data-ttu-id="4de06-124">Wenn Sie als Administrator erfahren möchten, wie Sie das Excel-Add-In installieren, lesen Sie [Einrichtung des Excel-Add-Ins zur Bearbeitung von Business Central Daten](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="4de06-124">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="4de06-125">Bei [!INCLUDE[prodshort](includes/prodshort.md)] lokal ist diese Funktion nur für den Web-Client verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4de06-125">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, this feature is only available for the Web client.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="4de06-126">Sehen Sie sich die Unterschiede zwischen den Optionen an</span><span class="sxs-lookup"><span data-stu-id="4de06-126">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learnlearnmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex"></a><span data-ttu-id="4de06-127">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="4de06-127">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="4de06-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4de06-128">See Also</span></span>
[<span data-ttu-id="4de06-129">Arbeiten mit Business Central</span><span class="sxs-lookup"><span data-stu-id="4de06-129">Working with Business Central</span></span>](ui-work-product.md)  
