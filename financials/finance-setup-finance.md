---
title: Einrichten von Prozessen in Financials | Microsoft Docs
description: "Informationen zu Aufgaben, Finanzen in Ihrem Unternehmen einzurichten, um Ihrer Buchhaltung, oder Buchhaltungsanforderungen Prüfungen zu entsprechen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 08/10/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b63e2e65f92edbbe10bcb5e2c340db31b1acda28
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-finance"></a><span data-ttu-id="192e7-103">Finance einrichten</span><span class="sxs-lookup"><span data-stu-id="192e7-103">Setting Up Finance</span></span>
<span data-ttu-id="192e7-104">Damit Sie sich rasch zurechtfinden, enthält [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]  Standardkonfigurationen für die meisten Finanzprozesse.</span><span class="sxs-lookup"><span data-stu-id="192e7-104">To help you get going quickly, [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] includes standard configurations for most financial processes.</span></span> <span data-ttu-id="192e7-105">Wenn Sie die Konfiguration ändern müssen, um Ihrem Geschäft zu entsprechen, tun Sie es.</span><span class="sxs-lookup"><span data-stu-id="192e7-105">If you need to change the configurations to suit your business, go right ahead.</span></span> <span data-ttu-id="192e7-106">Sei können vom Startbildschirm auf eine unterstützte Einrichtung zugreifen, die Sie bespielsweise dabei unterstützt, Salestax abhängig von Ihrem Standort einzurichten.</span><span class="sxs-lookup"><span data-stu-id="192e7-106">For example, from the Home page you can use an assisted setup guide to set up sales tax rate for your location.</span></span>  

<span data-ttu-id="192e7-107">Es gibt jedoch mehrere Elemente, die Sie selber einrichten müssen.</span><span class="sxs-lookup"><span data-stu-id="192e7-107">However, there are some things you need to set up yourself.</span></span> <span data-ttu-id="192e7-108">Wenn Sie Dimensionen als Grundlage für Business Intelligence verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="192e7-108">For example, if you want to use dimensions as a basis for business intelligence.</span></span>  

<span data-ttu-id="192e7-109">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="192e7-109">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="192e7-110">An</span><span class="sxs-lookup"><span data-stu-id="192e7-110">To</span></span> | <span data-ttu-id="192e7-111">Informationen</span><span class="sxs-lookup"><span data-stu-id="192e7-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="192e7-112">Wählen Sie aus, wie Sie Ihre Kreditoren bezahlen.</span><span class="sxs-lookup"><span data-stu-id="192e7-112">Choose how you pay your vendors.</span></span> |[<span data-ttu-id="192e7-113">Zahlungsformen definieren</span><span class="sxs-lookup"><span data-stu-id="192e7-113">Defining Payment Methods</span></span>](finance-payment-methods.md) |
| <span data-ttu-id="192e7-114">Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Fibukonten.</span><span class="sxs-lookup"><span data-stu-id="192e7-114">Specify the posting groups that map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> |[<span data-ttu-id="192e7-115">Buchungsgruppen einrichten</span><span class="sxs-lookup"><span data-stu-id="192e7-115">Setting Up Posting Groups</span></span>](finance-posting-groups.md)|
|<span data-ttu-id="192e7-116">Einrichtung einer Toleranz, mit der das System eine Rechnung schließt, selbst wenn die Zahlung einschließlich aller Rabatte nicht vollständig den Betrag der Rechnung abdeckt.</span><span class="sxs-lookup"><span data-stu-id="192e7-116">Set up a tolerance by which the system closes an invoice even though the payment, including any discount, does not fully cover the amount on the invoice.</span></span>|[<span data-ttu-id="192e7-117">Vorgehensweise: Mit Zahlungstoleranzen und Skontotoleranzen arbeiten</span><span class="sxs-lookup"><span data-stu-id="192e7-117">How to: Work with Payment Tolerances and Payment Discount Tolerances</span></span>](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| <span data-ttu-id="192e7-118">Einrichten von Finanzzeiträumen</span><span class="sxs-lookup"><span data-stu-id="192e7-118">Set up fiscal periods.</span></span> |[<span data-ttu-id="192e7-119">So geht's: Ein neues Geschäftsjahr eröffnen</span><span class="sxs-lookup"><span data-stu-id="192e7-119">How to: Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md) |
| <span data-ttu-id="192e7-120">Definieren Sie, wie Sie Dienstleistungssteuerbeträge erstellen, die Sie für Verkäufe an das Finanzamt eingetrieben haben.</span><span class="sxs-lookup"><span data-stu-id="192e7-120">Define how you report value-added tax amounts that you have collected for sales to the tax authorities.</span></span> |[<span data-ttu-id="192e7-121">So gehts: Melden von MwSt. an die Steuerbehörden</span><span class="sxs-lookup"><span data-stu-id="192e7-121">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="192e7-122">Einrichten Ihrer Verkaufs- und Einkaufsfunktionen, um Zahlungen in Fremdwährungen abzuwickeln.</span><span class="sxs-lookup"><span data-stu-id="192e7-122">Set your Sales and Purchases features up to handle payments in foreign currencies.</span></span>|[<span data-ttu-id="192e7-123">So gehts: Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="192e7-123">How to: Enable Application of Ledger Entries in Different Currencies</span></span>](finance-how-enable-application-ledger-entries-different-currencies.md)
| <span data-ttu-id="192e7-124">Fügen Sie dem bestehenden Kontenplan neue Konten hinzu.</span><span class="sxs-lookup"><span data-stu-id="192e7-124">Add new accounts to the existing chart of accounts.</span></span> |[<span data-ttu-id="192e7-125">Einrichten des Kontenplans</span><span class="sxs-lookup"><span data-stu-id="192e7-125">Setting Up the Chart of Accounts</span></span>](finance-setup-chart-accounts.md) |
| <span data-ttu-id="192e7-126">Einrichten Business Intelligence (BI)- Diagrammen, um Cashflow zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="192e7-126">Set up business intelligence (BI) charts to analyze cash flow.</span></span> |[<span data-ttu-id="192e7-127">Aufstellungs-Cashflow-Analyse</span><span class="sxs-lookup"><span data-stu-id="192e7-127">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md) |
|<span data-ttu-id="192e7-128">Aktivierung der Rechnungstellung für einen Kunden, der nicht im System eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="192e7-128">Enable invoicing of a customer who is not set up in the system.</span></span>|[<span data-ttu-id="192e7-129">Vorgehensweise: Barkunden einrichten</span><span class="sxs-lookup"><span data-stu-id="192e7-129">How to: Set Up Cash Customers</span></span>](finance-how-to-set-up-cash-customers.md)|
| <span data-ttu-id="192e7-130">Einrichtung von Intrastat-Berichten und Übermitteln des Berichts an eine Behörde</span><span class="sxs-lookup"><span data-stu-id="192e7-130">Set up Intrastat reporting, and submit the report to an authority</span></span> | [<span data-ttu-id="192e7-131">Gewusst wie: Einrichten von Intrastat-Berichten</span><span class="sxs-lookup"><span data-stu-id="192e7-131">How to: Set Up and Report Intrastat</span></span>](finance-how-setup-report-intrastat.md)|

## <a name="see-also"></a><span data-ttu-id="192e7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="192e7-132">See Also</span></span>
<span data-ttu-id="192e7-133">[Finanzen](finance.md)]</span><span class="sxs-lookup"><span data-stu-id="192e7-133">[Finance](finance.md)]</span></span>  
[<span data-ttu-id="192e7-134">Verwalten von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="192e7-134">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="192e7-135">Arbeiten mit Dimensionen</span><span class="sxs-lookup"><span data-stu-id="192e7-135">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="192e7-136">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="192e7-136">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="192e7-137">Analysieren von Cashflow in Ihren Mandanten</span><span class="sxs-lookup"><span data-stu-id="192e7-137">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="192e7-138">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="192e7-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

