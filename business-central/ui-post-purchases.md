---
title: Verstehen, wie Einkaufsbelege gebucht werden | Microsoft Docs
description: Mehr zu den unterschiedlichen Buchungsfunktionen erfahren, um Einkaufsbelege zu buchen.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d4d1c86f88acfce861a3330ba5457ce3f80c264c
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="posting-purchases"></a><span data-ttu-id="28fd2-103">Einkäufe buchen</span><span class="sxs-lookup"><span data-stu-id="28fd2-103">Posting Purchases</span></span>
<span data-ttu-id="28fd2-104">Wenn Sie die Schaltfläche **Gruppe Buchen** in einem Einkaufsbeleg auswählen, können Sie zwischen den folgenden Buchungsfunktionen auswählen:</span><span class="sxs-lookup"><span data-stu-id="28fd2-104">In the **Posting group** on a purchase document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="28fd2-105">**Veröffentlichen**</span><span class="sxs-lookup"><span data-stu-id="28fd2-105">**Post**</span></span>
* <span data-ttu-id="28fd2-106">**Buchungsvorschau**</span><span class="sxs-lookup"><span data-stu-id="28fd2-106">**Preview Posting**</span></span>
* <span data-ttu-id="28fd2-107">**Buchen und Drucken**</span><span class="sxs-lookup"><span data-stu-id="28fd2-107">**Post and Print**</span></span>
* <span data-ttu-id="28fd2-108">**Testbericht**</span><span class="sxs-lookup"><span data-stu-id="28fd2-108">**Test Report**</span></span>
* <span data-ttu-id="28fd2-109">**Stapelbuchung**</span><span class="sxs-lookup"><span data-stu-id="28fd2-109">**Post Batch**</span></span>

<span data-ttu-id="28fd2-110">Wenn Sie die Zeilen der Einkaufsbestellung ausgefüllt haben, können Sie sie buchen, d. h., eine Lieferung und eine Rechnung erzeugen.</span><span class="sxs-lookup"><span data-stu-id="28fd2-110">When you have completed all the lines and entered all the information on the purchase order, you can post it, that is, create a receipt and an invoice.</span></span>

<span data-ttu-id="28fd2-111">Wenn eine Einkaufsbestellung gebucht wird, werden das Kreditorenkonto, die Fibuposten und die Lagerposten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="28fd2-111">When a purchase order is posted, the vendor's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="28fd2-112">Für jede Einkaufsbestellung wird ein Einkaufsposten in der Tabelle **Fibuposten** erstellt.</span><span class="sxs-lookup"><span data-stu-id="28fd2-112">For each purchase order, a purchase entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="28fd2-113">Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Fibuposten im entsprechenden Einkaufskonto.</span><span class="sxs-lookup"><span data-stu-id="28fd2-113">An entry is also created in the vendor's account in the **Vendor Ledger Entry** table and a G/L entry is created in the relevant payables account.</span></span> <span data-ttu-id="28fd2-114">Zusätzlich kann das Buchen in einem MWST-Posten und einem Fibuposten für den Rabattbetrag resultieren.</span><span class="sxs-lookup"><span data-stu-id="28fd2-114">In addition, posting the order may result in a VAT entry and a G/L entry for the discount amount.</span></span> <span data-ttu-id="28fd2-115">Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** im Fenster **Kreditoren & Einkauf einrichten** ab.</span><span class="sxs-lookup"><span data-stu-id="28fd2-115">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Purchases & Payables Setup** window.</span></span>

<span data-ttu-id="28fd2-116">Für jede Einkaufsbestellungszeile wird ein Lagerposten in der Tabelle **Lagerposten** erstellt (wenn die Einkaufszeilen Artikelnummern enthalten) oder es wird ein Fibuposten in der Tabelle **Fibuposten** erstellt (wenn die Einkaufszeilen eine Fibukontonummer enthalten).</span><span class="sxs-lookup"><span data-stu-id="28fd2-116">For each purchase order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the purchase lines contain item numbers) or a G/L entry will be created in the **G/L Entry** table (if the purchase lines contain a G/L account).</span></span> <span data-ttu-id="28fd2-117">Zusätzlich werden Einkaufsbestellungen immer in den Tabellen **Einkaufslieferkopf** und **Einkaufsrechnungskopf** erfasst.</span><span class="sxs-lookup"><span data-stu-id="28fd2-117">In addition, purchase orders are always recorded in the **Purch. Recpt. Header** and **Purch. Inv. Header** tables.</span></span>

<span data-ttu-id="28fd2-118">Bevor Sie buchen, können Sie einen Testbericht ausdrucken, der alle Daten der Einkaufsbestellung und etwaige Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="28fd2-118">Before you start to post, you can print a test report that contains all the information in the purchase order and indicates any errors there.</span></span> <span data-ttu-id="28fd2-119">Um den Bericht zu drucken, wählen Sie **Buchen** und wählen **Testbericht** aus.</span><span class="sxs-lookup"><span data-stu-id="28fd2-119">To print the report, choose **Posting**, and then choose **Test Report**.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="28fd2-120">Wenn Sie eine Bestellung buchen, können Sie sowohl eine Lieferung als auch eine Rechnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="28fd2-120">When you post an order, you can create both a receipt and an invoice.</span></span> <span data-ttu-id="28fd2-121">Dies kann gleichzeitig oder unabhängig voneinander durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="28fd2-121">These can be done simultaneously or independently.</span></span> <span data-ttu-id="28fd2-122">Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Zu liefernde Menge** und/oder **Zu fakturierende Menge** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen.</span><span class="sxs-lookup"><span data-stu-id="28fd2-122">You can also create a partial receipt and a partial invoice by completing the **Qty. to Receive** and **Qty. to Invoice** fields on the individual purchase order lines before you post.</span></span> <span data-ttu-id="28fd2-123">Beachten Sie, dass Sie keine Rechnung für Mengen erstellen können, die noch nicht geliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="28fd2-123">Note that you cannot create an invoice for something that has not been received.</span></span> <span data-ttu-id="28fd2-124">Das bedeutet, dass Sie vor der Fakturierung eine Lieferung gebucht haben müssen oder Sie müssen "Liefern und Fakturieren" wählen.</span><span class="sxs-lookup"><span data-stu-id="28fd2-124">That is, before you can invoice, you must have recorded a receipt, or you must choose to receive and invoice at the same time.</span></span>

<span data-ttu-id="28fd2-125">Sie können entweder buchen oder buchen und drucken.</span><span class="sxs-lookup"><span data-stu-id="28fd2-125">You can either post, or post and print.</span></span> <span data-ttu-id="28fd2-126">Wenn Sie sich entscheiden, zu buchen und zu drucken, wird ein Bericht gedruckt, wenn der Auftrag gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="28fd2-126">If you choose to post and print, a report is printed when the order is posted.</span></span> <span data-ttu-id="28fd2-127">Sie können auch die Funktion **Stapelbuchen** wählen, mit der Sie mehrere Aufträge gleichzeitig buchen können.</span><span class="sxs-lookup"><span data-stu-id="28fd2-127">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span>

<span data-ttu-id="28fd2-128">Wenn die Buchung vollständig ist, werden die gebuchten Einkaufszeilen aus der Bestellung entfernt.</span><span class="sxs-lookup"><span data-stu-id="28fd2-128">When the posting is completed, the posted purchase lines are removed from the order.</span></span> <span data-ttu-id="28fd2-129">Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="28fd2-129">A message tells you when the posting is completed.</span></span> <span data-ttu-id="28fd2-130">Im Anschluss können Sie die gebuchten Posten in den verschiedenen Fenstern einsehen, die gebuchte Posten enthalten ( **Kreditorenposten**, **Fibuposten**, **Lagerposten**, **Lagerplatzposten**, **Einkaufsrechnung** ).</span><span class="sxs-lookup"><span data-stu-id="28fd2-130">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Vendor Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Purchase Receipts**, and **Posted Purchase Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="28fd2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28fd2-131">See Also</span></span>
[<span data-ttu-id="28fd2-132">Einkauf</span><span class="sxs-lookup"><span data-stu-id="28fd2-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="28fd2-133">Journale und Dokumente buchen</span><span class="sxs-lookup"><span data-stu-id="28fd2-133">Post Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="28fd2-134">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="28fd2-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


