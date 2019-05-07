---
title: Erhalten von Informationen zu Fibuposten und COA| Microsoft Docs
description: Beschreibt den Fibuposten, den Kontenplan und die Kontokategorien.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: b16c36bb5e6f3d9a6909f1937e793599062114c6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "914601"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="d7b57-103">Verständnis des Fibupostens und des COA</span><span class="sxs-lookup"><span data-stu-id="d7b57-103">Understanding the General Ledger and the COA</span></span>
<span data-ttu-id="d7b57-104">Die Fibuposten speichern Ihre Finanzdaten, und der Kontenplan zeigt die Konten, auf die alle Fibuposten gebucht werden, an.</span><span class="sxs-lookup"><span data-stu-id="d7b57-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="d7b57-105">umfasst einen Standardkontenplan, der zur Unterstützung Ihres Unternehmens bereit steht.</span><span class="sxs-lookup"><span data-stu-id="d7b57-105">includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="d7b57-106">Finanzbuchhaltung Einrichtung und Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="d7b57-106">General Ledger Setup and General Posting Setup</span></span>
<span data-ttu-id="d7b57-107">Die Einrichtung der Fibuposten ist das Kernstück der Finanzvorgängen, da sie definieren, wie Sie Daten buchen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="d7b57-108">Auf der Seite **Fibuposten einrichten** geben Sie an, wie bestimmte finanzbuchhalterische Sachverhalte in Ihrem Unternehmen gehandhabt werden sollen, wie beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="d7b57-108">On the **General Ledger Setup** page, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="d7b57-109">Rechnungsrundungskontodetails</span><span class="sxs-lookup"><span data-stu-id="d7b57-109">Invoice rounding details</span></span>  
* <span data-ttu-id="d7b57-110">Adressformate</span><span class="sxs-lookup"><span data-stu-id="d7b57-110">Address formats</span></span>  
* <span data-ttu-id="d7b57-111">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="d7b57-111">Financial reporting</span></span>  

<span data-ttu-id="d7b57-112">Ebenso geben Sie auf der Seite **Buchungsmatrix Einrichtung** an, wie Sie Kombinationen aus Geschäftsbuchungsgruppen und Produktbuchungsgruppen einrichten wollen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-112">Similarly, on the **General Posting Setup** page, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="d7b57-113">Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Fibukonten.</span><span class="sxs-lookup"><span data-stu-id="d7b57-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="d7b57-114">Für jede Kombination aus Geschäftsbuchungsgruppe und Produktbuchungsgruppe geben Sie eine Zeile ein.</span><span class="sxs-lookup"><span data-stu-id="d7b57-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="d7b57-115">Weitere Informationen finden Sie unter [Einrichten von Gruppenbuchungen ](finance-posting-groups.md)</span><span class="sxs-lookup"><span data-stu-id="d7b57-115">For more information, see [Posting Group Setups](finance-posting-groups.md)</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="d7b57-116">Kontenplan</span><span class="sxs-lookup"><span data-stu-id="d7b57-116">The Chart of Accounts</span></span>
<span data-ttu-id="d7b57-117">Der Kontenschema zeigt alle Fibukonten an.</span><span class="sxs-lookup"><span data-stu-id="d7b57-117">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="d7b57-118">Vom Kontenplan aus können Sie Dinge tun wie:</span><span class="sxs-lookup"><span data-stu-id="d7b57-118">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="d7b57-119">Berichte ansehen, die die Fibuposten und -Salden zeigen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-119">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="d7b57-120">Erfolgsrechnung-Kontennullstellung.</span><span class="sxs-lookup"><span data-stu-id="d7b57-120">Close your income statement.</span></span>  
* <span data-ttu-id="d7b57-121">Öffnen der Fibukontokarte, um Einstellungen hinzuzufügen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d7b57-121">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="d7b57-122">Sie können ausserdem eine Liste von Buchungsgruppen anzeigen, die auf dieses Konto buchen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-122">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="d7b57-123">Ansicht der Soll- und Habensalden von einzelnen Sachkonten</span><span class="sxs-lookup"><span data-stu-id="d7b57-123">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="d7b57-124">Sie können Fibukonten hinzufügen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-124">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="d7b57-125">Um jedoch Differenzen zu verhindern, können Sie ein Fibuposten nicht löschen, wenn Daten im Kontenschema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7b57-125">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="d7b57-126">Kontokategorien</span><span class="sxs-lookup"><span data-stu-id="d7b57-126">Account Categories</span></span>
<span data-ttu-id="d7b57-127">Sie können die Struktur der Finanzberichte personalisieren, indem Sie Fibukonten den Kontenkategorien hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-127">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="d7b57-128">Die Seite **Fibukontokategorien** zeigt Ihre vorhandenen Haupt- und Unterkategorien und die Fibukonten an, die Sie jeder Kategorie zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="d7b57-128">The **G/L Account Categories** page shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="d7b57-129">Sie können neue Unterkategorien erstellen und diese bestehenden Konten zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-129">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="d7b57-130">Sie erstellen eine Kategoriengruppe, indem Sie weitere Unterkategorien unter einer Zeile auf der Seite **Fibukontokategorien** einrücken.</span><span class="sxs-lookup"><span data-stu-id="d7b57-130">You create a category group by indenting other subcategories under a line on the **G/L Account Categories** page.</span></span> <span data-ttu-id="d7b57-131">Dieses erleichtert Ihnen den Überblick, da jede Gruppierung einen Gesamtsaldo anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d7b57-131">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="d7b57-132">Beispielsweise können Sie Unterkategorien für unterschiedliche Arten von Anlagen erstellen und dann Kategoriengruppen für Anlagen gegenüber Umlaufvermögen erstellen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-132">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="d7b57-133">Für jede Unterkategorie können Sie festlegen, ob Konten dieser Kategorie in bestimmte Arten von Finanzberichten enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-133">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="d7b57-134">Die Kontengruppen helfen Ihnen dabei, das Layout Ihrer Finanzberichte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d7b57-134">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="d7b57-135">Beispielsweise gibt es in der Standardsaldoabrechnung eine einzige Unterkategorie für Zahlungen unter Anlagen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-135">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="d7b57-136">Wenn Sie möchten, dass die Saldoabrechnung Handgeld und Giro berücksichtigt, können Sie:</span><span class="sxs-lookup"><span data-stu-id="d7b57-136">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="d7b57-137">Zwei neue Unterkategorien hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-137">Add two new subcategories.</span></span> <span data-ttu-id="d7b57-138">Eine für Handgeld und eine für Ihr Girokonto.</span><span class="sxs-lookup"><span data-stu-id="d7b57-138">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="d7b57-139">Geben Sie die zusätzlichen Berichtsdefinition **Bargeldkonten** für diese Unterkategorien an.</span><span class="sxs-lookup"><span data-stu-id="d7b57-139">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="d7b57-140">Fassen Sie diese in der Unterkategorie **Bar** zusammen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-140">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="d7b57-141">Wenn Sie das nächste Mal ein Kontenschema auf Grundlage Ihre Änderungen erstellt haben, wird die nächste Saldoabrechnung ein Gesamtsaldo für Zahlungen und zwei Zeilen mit Salden für Handgeld und das Girokonto anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7b57-141">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d7b57-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7b57-142">See Also</span></span>
[<span data-ttu-id="d7b57-143">Finanzen</span><span class="sxs-lookup"><span data-stu-id="d7b57-143">Finance</span></span>](finance.md)  
[<span data-ttu-id="d7b57-144">Einrichten oder Ändern des Kontenplans</span><span class="sxs-lookup"><span data-stu-id="d7b57-144">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="d7b57-145">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="d7b57-145">Business Intelligence</span></span>](bi.md)  
