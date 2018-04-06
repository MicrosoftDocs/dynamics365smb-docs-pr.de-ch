---
title: Verwalten von Verbindlichkeiten| Microsoft Docs
description: "Überblick darüber, wie Ihnen Financials hilft, Verbindlichkeiten inklusive Kreditorenzahlungen, Gläubiger, Schulden und geschuldete Beträge zu verwalten."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-financials
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 654c34bc09967247617bda7be070a9c0ec6f635d
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="managing-payables"></a><span data-ttu-id="3c2fb-103">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="3c2fb-103">Managing Payables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="3c2fb-104"> hat alles, was Sie brauchen, um Ihre Verbindlichkeiten effektiv zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-104"> has what you need to effectively manage accounts payable.</span></span>  

## <a name="payments"></a><span data-ttu-id="3c2fb-105">Zahlungen</span><span class="sxs-lookup"><span data-stu-id="3c2fb-105">Payments</span></span>
<span data-ttu-id="3c2fb-106">Es ist einfach, Zahlungen zu priorisieren, Gebühren für überfällige Zahlungen zu bezahlen und Skonto für frühzeitige Zahlungen zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-106">It's easy to prioritize payments, account for penalties for overdue payments, and handle discounts for early payments.</span></span>

<span data-ttu-id="3c2fb-107">Sie können Zahlungen in einem Fibu Erf.-Journal erfassen und anschliessend drucken und überprüfen, bevor das Zahlungsausgangs Erf.-Journal gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-107">You can record payments in a general journal, and then print checks before posting the payment journal.</span></span>

<span data-ttu-id="3c2fb-108">Eine Zahlung kann mit der entsprechenden Rechnung beim Buchen der Zahlung oder auch erst nach dem Buchen der Zahlung ausgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-108">You can apply payments to close invoices when you post the payment, or after you post the payment.</span></span> <span data-ttu-id="3c2fb-109">Mit dem Feld **Ausgleichsmethode** für den Kreditor (auf der **Kreditorenkarte**) wird festgelegt, ob ein manueller Ausgleich erforderlich ist oder ob der Ausgleich automatisch vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-109">The **Application Method** specified for the vendor (on the **Vendor Card**) determines whether you apply the payment manually, or automatically.</span></span> <span data-ttu-id="3c2fb-110">Die Verwendung des manuellen Ausgleichs von Transaktionen ist immer möglich.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-110">You can always apply transactions manually.</span></span> <span data-ttu-id="3c2fb-111">Ist jedoch als Ausgleichsmethode für den Kreditor die Option **Saldomethode** festgelegt, und es wird kein Beleg für den Zahlungsausgleich angegeben, wird die Zahlung mit dem ältesten offenen Posten für den Kreditor ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-111">However, if the application method for the vendor is **Apply to Oldest**, and you do not specify a document to apply the payment to, the payment is applied to the oldest open entry for the vendor.</span></span>

## <a name="suggest-vendor-payments"></a><span data-ttu-id="3c2fb-112">Zahlungsvorschlag</span><span class="sxs-lookup"><span data-stu-id="3c2fb-112">Suggest Vendor Payments</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="3c2fb-113"> kann verschiedene Zahlungen an Kreditoren vorschlagen, wie Zahlungen, die in Kürze fällig sind, oder Zahlungen, bei denen ein Rabatt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-113"> can suggest various payments to vendors, such as payments that will be due soon, or payments where a discount is available.</span></span> <span data-ttu-id="3c2fb-114">Der Zahlungsvorschlag kann einen bestimmten Betrag berücksichtigen, der für Zahlungen zur Verfügung steht und die Möglichkeit, einen Rabatt für fristgerechte Zahlung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-114">The payment suggestion can consider an amount that you specify as available funds for payment, and eligibility for payment discounts.</span></span>

## <a name="issue-checks"></a><span data-ttu-id="3c2fb-115">Schecks ausstellen</span><span class="sxs-lookup"><span data-stu-id="3c2fb-115">Issue Checks</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="3c2fb-116"> können Sie Schecks an Kreditoren manuell und elektronisch erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-116"> lets you issue checks to vendors manually and electronically.</span></span> <span data-ttu-id="3c2fb-117">Sie machen beides im Fenster **Zlg.-Ausg. Buch.-Blätter**, in dem Sie auch Schecks annullieren und Scheckposteneinträge anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-117">You do both in the **Payment Journals** window, where you can also void checks and view check ledger entries.</span></span>

## <a name="export-payments-to-a-bank-file"></a><span data-ttu-id="3c2fb-118">Zahlungen in eine Bankdatei exportieren</span><span class="sxs-lookup"><span data-stu-id="3c2fb-118">Export Payments to a Bank File</span></span>
<span data-ttu-id="3c2fb-119">Wenn Sie bereit sind, Zahlungen an Ihre Kreditoren im Fenster **Zahlung Buch.-Blatt** vorzunehmen, können Sie eine Datei mit den Zahlungsinformationen aus den Buch.-Blattzeilen exportieren.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-119">When you are ready to pay a vendor, from the **Payment Journal** window you can export a file with the payment information from the journal lines.</span></span> <span data-ttu-id="3c2fb-120">Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-120">You can then upload the file to your electronic bank to process the money transfers.</span></span>

<span data-ttu-id="3c2fb-121">Wenn Sie keine Erf.-Journalzeile für eine exportierte Zahlung buchen möchten, weil Sie beispielsweise eine Bestätigung erwarten, dass die Transaktion von der Bank verarbeitet wurde, können Sie die Erf.-Journalzeile einfach löschen.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-121">If you do not want to post a payment journal line for an exported payment, for example because you are waiting for the bank to confirm the transaction, just delete the journal line.</span></span> <span data-ttu-id="3c2fb-122">Falls Sie später eine Buch.-Blattzeile erstellen, um den Restbetrag der gebuchten Rechnung zu bezahlen, zeigt das **Exportierter Betrag gesamt**-Feld, wie viel des Zahlungsbetrags bereits exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-122">Later, when you create a payment journal line to pay the remaining amount on the invoice, the **Total Exported Amount** field shows how much of the payment amount has already been exported.</span></span> <span data-ttu-id="3c2fb-123">Detaillierte Informationen über die exportierte Summe können Sie auch finden, indem Sie die Schaltfläche **Posten im Kreditübertragungsjournal** auswählen, um Einzelheiten zu Dateien der exportierten Zahlung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-123">Also, you can find detailed information about the exported total by choosing the **Credit Transfer Reg. Entries** button.</span></span>

<span data-ttu-id="3c2fb-124">Wenn Sie abwarten, um Zahlungen zu buchen, bis die Bank bestätigt, dass Transaktionen verarbeitet wurden, gibt es zwei Möglichkeiten zu vermeiden, dass, Zahlungen für fällige Belege versehentlich erneut exportieren werden.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-124">If you wait to post payments until after your bank confirms that it has processed transactions, there are two ways to avoid accidently re-exporting payments for open documents:</span></span>  

* <span data-ttu-id="3c2fb-125">In einem Zahlungsausgangs-Buch.-Blatt mit vorgeschlagenen Zahlungszeilen, können Sie entweder nach der **In Zahlungsdatei exportiert**-Spalte oder nach **Exportierter Betrag gesamt** sortieren, und dann Zahlungsvorschläge für offene Rechnungen, für die bereits Zahlungen geleistet wurden und für die Sie keine Zahlungen leisten möchten, löschen.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-125">In a payment journal with suggested payment lines, sort on either the **Exported to Payment File** or **Total Exported Amount** columns, and then delete payment suggestions for open invoices for which payments have already been made and you do not want to make payments for.</span></span>

    <span data-ttu-id="3c2fb-126">**Hinweis** Möglicherweise müssen Sie diese Spalten der Liste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-126">**Note** You might have to add these columns to the list.</span></span> <span data-ttu-id="3c2fb-127">Weitere Informationen finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="3c2fb-127">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  
* <span data-ttu-id="3c2fb-128">Alternativ können Sie in der Stapelverarbeitung **Zahlungsvorschläge für Kreditoren**, in der Sie festlegen, welche Zahlungen in das Zahlungsausgangs Buch.-Blatt einzufügen sind, das Kontrollkästchen **Exportierte Zahlungen überspringen** aktivieren, wenn Sie keine Buch.-Blattzeilen für Zahlungen einfügen möchten, die bereits exportiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3c2fb-128">Alternatively, on the **Suggest Vendor Payments** batch job, where you specify the payments to include in the payment journal, you can specify not to insert journal lines for payments that have already been exported by choosing the **Skip Exported Payments** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c2fb-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c2fb-129">See Also</span></span>
[<span data-ttu-id="3c2fb-130">Zahlungsformen</span><span class="sxs-lookup"><span data-stu-id="3c2fb-130">Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="3c2fb-131">Finanzen</span><span class="sxs-lookup"><span data-stu-id="3c2fb-131">Finance</span></span>](finance.md)  
<span data-ttu-id="3c2fb-132">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3c2fb-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

