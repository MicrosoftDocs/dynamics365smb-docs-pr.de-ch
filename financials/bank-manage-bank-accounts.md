---
title: Verwalten von Bankkonten| Microsoft Docs
description: "Sie müssen regelmäßig Bankposteneinträge in Financials mit den verknüpften Banktransaktionen in Ihren Bankkonten abstimmen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dcefa921d7e8b901d906085e6bce01d6e0aa6ac4
ms.contentlocale: de-ch
ms.lasthandoff: 09/11/2017

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="d682f-103">Verwalten von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="d682f-103">Managing Bank Accounts</span></span>
<span data-ttu-id="d682f-104">In regelmäßigen Abständen müssen Sie Ihre Bankposten in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit den entsprechenden Banktransaktionen auf den Konten bei Ihrer Bank abstimmen, und dann den Saldo auf Ihrem Bankkonto buchen.</span><span class="sxs-lookup"><span data-stu-id="d682f-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="d682f-105">Diese Aufgabe kann als Teil der Zahlungsverarbeitung auf einem Bankauszug im **Zahlungsabstimmungs-Erfassungsjournal** dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d682f-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="d682f-106">Alternativ können Sie die Aufgabe unabhängig von der Zahlungsverarbeitung im Fenster **Bankkontoabstimmung** ausführen, in dem Scheckposten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d682f-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window, which supports check ledger entries.</span></span> <span data-ttu-id="d682f-107">In beiden Fällen füllen Sie das Fenster aus, indem Sie den Bankkontoauszug in [!INCLUDE[d365fin](includes/d365fin_md.md)] importieren.</span><span class="sxs-lookup"><span data-stu-id="d682f-107">In both cases, you fill in the windows by importing the bank statement into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="d682f-108">Manchmal müssen Sie Beträge zwischen Bankkonten im [!INCLUDE[d365fin](includes/d365fin_md.md)]  transferieren, um Überweisungen bei Ihrer Bank widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="d682f-108">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="d682f-109">Diese Aufgabe wird im Fenster **Fibu Erf.-Journal** auf unterschiedliche Arten, abhängig von der Währung der Geldmittel ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d682f-109">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="d682f-110">Bevor Sie Bankkonten verwalten können, müssen Sie jedes Bankkonto als Bankkontokarte einrichten.</span><span class="sxs-lookup"><span data-stu-id="d682f-110">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="d682f-111">Darüber hinaus müssen Sie elektronische Dienste einrichten, die Sie ggf. für den Bankauszugsimport und Zahlungsdateiexport verwenden.</span><span class="sxs-lookup"><span data-stu-id="d682f-111">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="d682f-112">Weitere Informationen finden Sie unter [So gehts: Einrichten von Bankkonten](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="d682f-112">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="d682f-113">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="d682f-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="d682f-114">Aktion</span><span class="sxs-lookup"><span data-stu-id="d682f-114">To</span></span> | <span data-ttu-id="d682f-115">Informationen</span><span class="sxs-lookup"><span data-stu-id="d682f-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="d682f-116">Abstimmen von Bankkonten in Verbindung mit der Zahlungsverarbeitung im Fenster **Zahlungsabstimmungs-Erfassungsjournal**.</span><span class="sxs-lookup"><span data-stu-id="d682f-116">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="d682f-117">Zahlungen automatisch vornehmen und Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="d682f-117">Apply Payments Automatically and Reconcile Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="d682f-118">Abstimmen von Bankkonten, inklusive Scheckposten, als separate Aufgabe im Fenster **Bankkontoabstimmung**.</span><span class="sxs-lookup"><span data-stu-id="d682f-118">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="d682f-119">Gewusst wie: Bankkonten separat abstimmen</span><span class="sxs-lookup"><span data-stu-id="d682f-119">How to: Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="d682f-120">Buchen von Überweisungen zwischen Bankkonten in der gleichen oder in unterschiedlichen Währungen.</span><span class="sxs-lookup"><span data-stu-id="d682f-120">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="d682f-121">Gewusst wie: Bank-Geldmittel überweisen</span><span class="sxs-lookup"><span data-stu-id="d682f-121">How to: Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="d682f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d682f-122">See Also</span></span>
[<span data-ttu-id="d682f-123">Einrichten von Banken</span><span class="sxs-lookup"><span data-stu-id="d682f-123">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="d682f-124">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="d682f-124">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="d682f-125">[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="d682f-125">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="d682f-126">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d682f-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d682f-127">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="d682f-127">General Business Functionality</span></span>](ui-across-business-areas.md)  

