---
title: Verwalten von Bankkonten| Microsoft Docs
description: Sie müssen regelmässig Bankposten mit den zugehörigen Banktransaktionen in Ihren Bankkonten abstimmen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 050519c77f7c1dca5dd451a57ac47f71b4803a91
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186202"
---
# <a name="reconciling-bank-accounts"></a><span data-ttu-id="26251-103">Abstimmen von Bankkonten</span><span class="sxs-lookup"><span data-stu-id="26251-103">Reconciling Bank Accounts</span></span>
<span data-ttu-id="26251-104">Eine Bankabstimmung sollte in regelmässigen Abständen für alle Ihre Bankkonten durchgeführt werden, um sicherzustellen, dass die Kassenunterlagen des Unternehmens korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="26251-104">A bank reconciliation should be completed at regular intervals for all your bank accounts to ensure that the company's cash records are correct.</span></span> <span data-ttu-id="26251-105">Sie tun dies, indem Sie die Einträge in Ihren internen Bankkonten mit den Banktransaktionen in Ihrer Bank vergleichen und abgleichen und dann die Salden auf Ihre internen Bankkonten buchen, um den Finanzmanagern Gesamtsummen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="26251-105">You do this by comparing and matching entries in your internal bank accounts with bank transactions at your bank, and then posting the balances to your internal bank accounts to make totals available to finance managers.</span></span> <span data-ttu-id="26251-106">Der Bankabgleich ist auch eine praktische Methode, um fehlende Zahlungen und Buchhaltungsfehler zu ermitteln und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="26251-106">Bank reconciliation is also a practical way to discover and resolve missing payments and bookkeeping errors.</span></span>

<span data-ttu-id="26251-107">Sie können die Aufgabe auf der Seite **Bankkonto Abstimmen** ausführen, auf der Sie die Bankkontoauszugszeilen auf der linken Bereichsseite mit Ihrem internen Bankposten im rechten Fensterbereich abstimmen (abgleichen).</span><span class="sxs-lookup"><span data-stu-id="26251-107">You can perform the task on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="26251-108">Alternativ können Sie diese Aufgabe auf der Seite **Zahlungsabstimmungserf.-Journal** als Teil der Verarbeitung der Zahlungen durchgeführt werden, die auf einem Bankauszug dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="26251-108">Alternatively, you can perform this task on the **Payment Reconciliation Journal** page as part of processing the payments that are represented on a bank statement.</span></span> <span data-ttu-id="26251-109">Auf beiden Seiten können Sie die Bankkontoauszugsinformationen ausfüllen, indem Sie eine Datei oder einen Feed importieren oder automatische entsprechende Vorschläge verwenden.</span><span class="sxs-lookup"><span data-stu-id="26251-109">On both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="26251-110">In den nordamerikanischen Versionen können Sie auf der Seite **Bank Rec. Vorschlag** durchführen, das besser für Schecks und Einzahlungen-Vorgänge geeignet ist, jedoch keine Bankkontoauszugsdateien bietet.</span><span class="sxs-lookup"><span data-stu-id="26251-110">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="26251-111">Um diese Seite **Bankkontoabstimmung** anstelle des Fensters zu verwenden, wählen Sie das Feld **Bankabstimmung mit automatischem Abgleich** auf der Seite **Fibuposten Einrichtung**.</span><span class="sxs-lookup"><span data-stu-id="26251-111">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="26251-112">Weitere Informationen finden Sie im Abschnitt "Bankkonten abstimmen" unter der der lokalen USA-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="26251-112">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="26251-113">Bevor Sie Ihre Bankkonten in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwalten können, müssen Sie jedes Bankkonto als Bankkontokarte einrichten.</span><span class="sxs-lookup"><span data-stu-id="26251-113">Before you can manage your bank accounts within [!INCLUDE[d365fin](includes/d365fin_md.md)], you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="26251-114">Darüber hinaus müssen Sie elektronische Dienste einrichten, die Sie ggf. für den Bankauszugsimport und Zahlungsdateiexport verwenden.</span><span class="sxs-lookup"><span data-stu-id="26251-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="26251-115">Weitere Informationen finden Sie unter [So gehts: Einrichten von Bankkonten](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="26251-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="26251-116">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert</span><span class="sxs-lookup"><span data-stu-id="26251-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="26251-117">Bis</span><span class="sxs-lookup"><span data-stu-id="26251-117">To</span></span> | <span data-ttu-id="26251-118">Siehe</span><span class="sxs-lookup"><span data-stu-id="26251-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="26251-119">Stimmen Sie Bankkonten als separate Aufgabe auf der Seite **Bankkontoabstimmung** ab.</span><span class="sxs-lookup"><span data-stu-id="26251-119">Reconcile bank accounts as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="26251-120">Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="26251-120">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="26251-121">Abstimmen von Bankkonten in Verbindung mit der Zahlungsverarbeitung auf der Seite **Zahlungsabstimmungserf.-Journal**.</span><span class="sxs-lookup"><span data-stu-id="26251-121">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="26251-122">Zahlungen automatisch vornehmen und Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="26251-122">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="26251-123">Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="26251-123">See Related Training at [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="26251-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26251-124">See Also</span></span>
[<span data-ttu-id="26251-125">Einrichten von Banken</span><span class="sxs-lookup"><span data-stu-id="26251-125">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="26251-126">Bank-Geldmittel überweisen</span><span class="sxs-lookup"><span data-stu-id="26251-126">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md)  
[<span data-ttu-id="26251-127">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="26251-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="26251-128">[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="26251-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="26251-129">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26251-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="26251-130">Allgemeine Geschäftsfunktionen</span><span class="sxs-lookup"><span data-stu-id="26251-130">General Business Functionality</span></span>](ui-across-business-areas.md)
