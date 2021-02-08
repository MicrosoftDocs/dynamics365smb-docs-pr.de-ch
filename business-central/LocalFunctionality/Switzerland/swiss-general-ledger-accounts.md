---
title: Finanzbuchhaltungskonten (Schweiz)
description: Schweizer Erweiterungen enthalten spezielle Fibupostenfunktionen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3b6f77b344628dccda66a752573a1a982c45ed7f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753165"
---
# <a name="swiss-general-ledger-accounts"></a><span data-ttu-id="26503-103">Finanzbuchhaltungskonten (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="26503-103">Swiss General Ledger Accounts</span></span>
[!INCLUDE[prod_short](../../includes/prod_short.md)] <span data-ttu-id="26503-104">enthält Schweizer Erweiterungen für Fibuposten.</span><span class="sxs-lookup"><span data-stu-id="26503-104">includes Swiss enhancements to general ledger accounts.</span></span>

- <span data-ttu-id="26503-105">Verwalten der Fremdwährungssalden eines Bankkontos in der Finanzbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="26503-105">Maintain the foreign currency balances of a bank account in the general ledger.</span></span>  
- <span data-ttu-id="26503-106">Sortieren Sie Finanzbuchhaltungs-Kontonummern auf der Seite **Kontenplan**.</span><span class="sxs-lookup"><span data-stu-id="26503-106">Sort general ledger account numbers on the **Chart of Accounts** page.</span></span>  
- <span data-ttu-id="26503-107">Anzeigen einer Vorschau, mit deren Hilfe die Auswirkungen von Finanzbuchhaltungs-Erfassungsjournalbuchungen auf die Salden bestimmter Finanzbuchhaltungskonten vor der eigentlichen Buchung überprüft werden können</span><span class="sxs-lookup"><span data-stu-id="26503-107">Preview the effects that posting general journals would have on the balances of certain general ledger accounts before actually posting them.</span></span>  

## <a name="general-ledger-accounts-and-general-journals"></a><span data-ttu-id="26503-108">Finanzbuchhaltungskonten und Finanzbuchhaltungs-Erfassungsjournale</span><span class="sxs-lookup"><span data-stu-id="26503-108">General Ledger Accounts and General Journals</span></span>  
<span data-ttu-id="26503-109">Unternehmen arbeiten häufig mit unterschiedlichen Bankkonten für Fremdwährungen und verwenden für jedes Bankkonto ein Finanzbuchhaltungskonto.</span><span class="sxs-lookup"><span data-stu-id="26503-109">Companies often have different bank accounts for foreign currencies, and have a general ledger account for each bank account.</span></span> <span data-ttu-id="26503-110">In [!INCLUDE[prod_short](../../includes/prod_short.md)] können Sie Fremdwährungssaldoinformationen und Währungscodes und auf der Seite **Kontenplan** einrichten.</span><span class="sxs-lookup"><span data-stu-id="26503-110">In [!INCLUDE[prod_short](../../includes/prod_short.md)], you can set up currency code and foreign currency balance information on the **Chart of Accounts** page.</span></span> <span data-ttu-id="26503-111">Auf diese Weise kann der ursprüngliche Fremdwährungssaldo eines Bankkontos verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="26503-111">This allows you to maintain the original foreign currency balance of a bank account.</span></span> <span data-ttu-id="26503-112">Weitere Informationen finden Sie unter [Verständnis des Fibupostens und des COA](../../finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="26503-112">For more information, see [Understanding the General Ledger and the COA](../../finance-general-ledger.md).</span></span>  

<span data-ttu-id="26503-113">Angenommen, ein Unternehmen verfügt über zwei Bankkonten: eines für Landes- bzw. Mandantenwährung (MW) und eines für Euro (EUR).</span><span class="sxs-lookup"><span data-stu-id="26503-113">For example, a company has two bank accounts: one for local currency (LCY) and one for euros (EUR).</span></span> <span data-ttu-id="26503-114">Sie müssen ein Finanzbuchhaltungskonto für jedes Bankkonto erstellen.</span><span class="sxs-lookup"><span data-stu-id="26503-114">You must create a general ledger account for each bank account.</span></span> <span data-ttu-id="26503-115">Für das EUR-Konto definieren Sie den Währungscode **EUR** und buchen Erfassungsjournale in EUR oder MW.</span><span class="sxs-lookup"><span data-stu-id="26503-115">For the EUR account, define the currency code as **EUR** and post journals in EUR or LCY.</span></span>  

<span data-ttu-id="26503-116">Wenn sich der Wechselkurs für EUR und MW ändert, können Sie den Landeswährungssaldo für das EUR-Finanzbuchhaltungskonto mit dem Stapelverarbeitungsauftrag "Wechselkurse regulieren" aktualisieren und anpassen.</span><span class="sxs-lookup"><span data-stu-id="26503-116">When the exchange rate for EUR and LCY changes, you can update and adjust the local currency balance for the EUR general ledger account using the adjust exchange rates batch job.</span></span> <span data-ttu-id="26503-117">Bei dieser Stapelverarbeitung werden Währungsregulierungsposten in der Finanzbuchhaltung erstellt und gebucht, und der MW-Saldo wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="26503-117">This batch job creates and posts currency adjustment entries to the general ledger and updates the LCY balance.</span></span>  

## <a name="data-type-for-general-ledger-accounts"></a><span data-ttu-id="26503-118">Datentyp für Finanzbuchhaltungskonten</span><span class="sxs-lookup"><span data-stu-id="26503-118">Data Type for General Ledger Accounts</span></span>  
<span data-ttu-id="26503-119">Der Datentyp ist in der Fibupostennummer auf Text oder Kontocode festgelegt, um die Sortierungsanforderungen für den standardisierten Kontenplan von kleinen und mittleren Unternehmen (KMU) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="26503-119">The data type is set to text for the general ledger account number or account code to support the sorting requirements for the standardized Swiss Kontenrahmen Käfer (KMU) common chart of accounts.</span></span> <span data-ttu-id="26503-120">Die Kontonummernliste ist basierend auf dem Datentyp "Text" sortiert.</span><span class="sxs-lookup"><span data-stu-id="26503-120">The account numbers list is sorted based on the text data type.</span></span> <span data-ttu-id="26503-121">Der KMU-Kontenplan enthält die folgenden Kontonummern:</span><span class="sxs-lookup"><span data-stu-id="26503-121">The KMU chart of accounts contains the following account numbers:</span></span>  

- <span data-ttu-id="26503-122">1176</span><span class="sxs-lookup"><span data-stu-id="26503-122">1176</span></span>  
- <span data-ttu-id="26503-123">119.0</span><span class="sxs-lookup"><span data-stu-id="26503-123">119.0</span></span>  
- <span data-ttu-id="26503-124">1190</span><span class="sxs-lookup"><span data-stu-id="26503-124">1190</span></span>  

## <a name="viewing-temporary-balances-in-general-journals"></a><span data-ttu-id="26503-125">Anzeigen temporärer Salden in Finanzbuchhaltungs-Erfassungsjournalen</span><span class="sxs-lookup"><span data-stu-id="26503-125">Viewing Temporary Balances in General Journals</span></span>  
<span data-ttu-id="26503-126">Bevor Sie ein Finanzbuchhaltungs-Erfassungsjournal buchen, können Sie eine Vorschau anzeigen, die Aufschluss gibt über die Auswirkungen dieser Buchung auf die Salden bestimmter Finanzbuchhaltungskonten.</span><span class="sxs-lookup"><span data-stu-id="26503-126">Before posting a general journal you can preview the effect that posting would have on the balances of certain general ledger accounts.</span></span> <span data-ttu-id="26503-127">Sie können eine Statistikseite, die die Salden der Konten anzeigt, und die Salden der aktiven Zeilen öffnen, die ungebuchte Werte für das aktuelle Erf.-Journal umfassten.</span><span class="sxs-lookup"><span data-stu-id="26503-127">You can open a statistics page that shows the balances of the accounts, and the balances of the active lines that included the unposted values for the current journal.</span></span> <span data-ttu-id="26503-128">Weitere Informationen finden Sie unter [Anzeigen temporärer Salden in Finanzbuchhaltungs-Erfassungsjournalen](how-to-view-temporary-balances-in-general-ledger-journals.md).</span><span class="sxs-lookup"><span data-stu-id="26503-128">For more information, see [View Temporary Balances in General Ledger Journals](how-to-view-temporary-balances-in-general-ledger-journals.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="26503-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26503-129">See Also</span></span>

[<span data-ttu-id="26503-130">Anzeigen temporärer Salden in Finanzbuchhaltungs-Erfassungsjournalen</span><span class="sxs-lookup"><span data-stu-id="26503-130">View Temporary Balances in General Ledger Journals</span></span>](how-to-view-temporary-balances-in-general-ledger-journals.md)  
[<span data-ttu-id="26503-131">Lokale Funktion (Schweiz)</span><span class="sxs-lookup"><span data-stu-id="26503-131">Switzerland Local Functionality</span></span>](switzerland-local-functionality.md)  
