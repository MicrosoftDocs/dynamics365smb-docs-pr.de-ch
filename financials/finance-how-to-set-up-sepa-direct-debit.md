---
title: SEPA Direct Debit einrichten | Microsoft Docs
description: Erfahren Sie, wie Sie SEPA Abbuchung in Dynamics 365 for Financials einrichten.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a5f7a99a3e6bfd9c0146d87af4e3869cda381a67
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-sepa-direct-debit"></a><span data-ttu-id="8641c-103">Vorgehensweise: Einrichten von SEPA-Basislastschriften</span><span class="sxs-lookup"><span data-stu-id="8641c-103">How to: Set Up SEPA Direct Debit</span></span>
<span data-ttu-id="8641c-104">Im Fenster **Lastschriften**  können Sie Anweisungen in Ihre elektronische Bank exportieren, um eine Lastschrift vom Bankkonto des Debitors auf Ihr Bankkonto durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8641c-104">From the **Direct Debit Collections** window, you can export instructions to your electronic bank to perform a direct debit collection from the customer’s bank account to your bank account.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="8641c-105"> unterstützt das Abbuchungsformat SEPA, aber in Ihrem Land/die Region, sind möglicherweise andere Formate für den elektronischen Zahlungsverkehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8641c-105"> supports the SEPA direct debit format, but in your country/region,other formats for electronic payments may be available.</span></span>  

<span data-ttu-id="8641c-106">Um das Exportieren von Bankdateiformaten zu aktivieren, die nicht durch die allgemeine oder lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt werden, können Sie eine Datenaustauschdefinition einrichten, indem Sie das  Datenaustauschframework verwenden.</span><span class="sxs-lookup"><span data-stu-id="8641c-106">To enable export of a bank file formats that are not supported out of the box in [!INCLUDE[d365fin](includes/d365fin_md.md)] , you can set up a data exchange definition by using the data exchange framework.</span></span> <span data-ttu-id="8641c-107">Für weitere Informationen, siehe [Gewusst wie: Einrichten des Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="8641c-107">For more information, see [How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

<span data-ttu-id="8641c-108">Bevor Sie Debitorenzahlungen elektronisch durch den Export von Lastschriften im SEPA-Lastschriftformat verarbeiten können, müssen Sie die folgenden Einrichtungsschritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="8641c-108">Before you can process customer payments electronically by exporting direct debit instructions in the SEPA Direct Debit format, you must perform the following setup steps:</span></span>  

* <span data-ttu-id="8641c-109">Richten Sie zunächst das Exportformat der Bankdatei ein, wodurch Ihre Bank beauftragt wird, eine Lastschrift vom Bankkonto des Debitors auf Ihr Bankkonto durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8641c-109">Set up the export format of the bank file that instructs your bank to perform a direct debit collection from the customer’s bank account to your bank account.</span></span>  
* <span data-ttu-id="8641c-110">Richten Sie die Zahlungsmethode des Debitors ein.</span><span class="sxs-lookup"><span data-stu-id="8641c-110">Set up the customer’s payment method.</span></span>  
* <span data-ttu-id="8641c-111">Richten Sie das Lastschriftmandat ein, das Ihrer Übereinkunft mit dem Debitor zum Einzug seiner Zahlungen in einem bestimmten Zeitraum entspricht.</span><span class="sxs-lookup"><span data-stu-id="8641c-111">Set up the direct-debit mandate that reflects your agreement with the customer to collect their payments in a certain agreement period.</span></span>  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a><span data-ttu-id="8641c-112">Einrichten Ihres Bankkontos für die SEPA-Basislastschriftübertragung</span><span class="sxs-lookup"><span data-stu-id="8641c-112">To set up your bank account for SEPA direct debit</span></span>  
1. <span data-ttu-id="8641c-113">Geben Sie im Feld **Suchen** **Bankkonten** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8641c-113">In the **Search** box, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8641c-114">Öffnen Sie das Konto, das Sie für das Basislastschriftverfahren verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8641c-114">Open the bank account that you want to use for direct debit.</span></span>  
3. <span data-ttu-id="8641c-115">Wählen Sie im Inforegister **Umlagerung**, im Feld **SEPA-Lastschrift Exportformat** SEPA Lastschrift.</span><span class="sxs-lookup"><span data-stu-id="8641c-115">On the **Transfer** FastTab, in the **SEPA Direct Debit Export Format** field, choose the option for SEPA direct debit.</span></span>  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a><span data-ttu-id="8641c-116">Einrichten der Zahlungsmethode des Debitors für die SEPA-Basislastschriftübertragung</span><span class="sxs-lookup"><span data-stu-id="8641c-116">To set up the customer’s payment method for SEPA direct debit</span></span>  
1. <span data-ttu-id="8641c-117">Geben Sie im Feld **Suchen** einen Wert für **Zahlungsformen** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8641c-117">In the **Search** box, enter **Payment Methods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8641c-118">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="8641c-118">Choose the **New** action.</span></span>  
3. <span data-ttu-id="8641c-119">Richten Sie eine Zahlungsmethode ein.</span><span class="sxs-lookup"><span data-stu-id="8641c-119">Set up a payment method.</span></span> <span data-ttu-id="8641c-120">Füllen Sie die auf den Lastschrifteinzug bezüglichen Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="8641c-120">Fill in the direct debit\-specific fields as described in the following table.</span></span>  

    |<span data-ttu-id="8641c-121">Feld</span><span class="sxs-lookup"><span data-stu-id="8641c-121">Field</span></span>|<span data-ttu-id="8641c-122">[Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8641c-122">[Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="8641c-123">**Basislastschrift**</span><span class="sxs-lookup"><span data-stu-id="8641c-123">**Direct Debit**</span></span>|<span data-ttu-id="8641c-124">Geben Sie an, ob die Zahlungsmethode für die SEPA-Basislastschriftübertragung gilt.</span><span class="sxs-lookup"><span data-stu-id="8641c-124">Specify if the payment method is for SEPA direct debit collection.</span></span>|  
    |<span data-ttu-id="8641c-125">**Zahlungsbedingungscode Basislastschrift**</span><span class="sxs-lookup"><span data-stu-id="8641c-125">**Direct Debit Pmt. Terms Code**</span></span>|<span data-ttu-id="8641c-126">Geben Sie die Zahlungsbedingungen an, wie etwa NICHT ZAHLEN, die auf Verkaufsrechnungen angezeigt werden, die per SEPA-Basislastschriftübertragung bezahlt werden, um den Debitor darauf hinzuweisen, dass die Zahlung automatisch eingezogen wird.</span><span class="sxs-lookup"><span data-stu-id="8641c-126">Specify the payment terms, such as DON’T PAY, that are displayed on sales invoices that are paid with SEPA direct debit to indicate to the customer that the payment will be collected automatically.</span></span> <span data-ttu-id="8641c-127">Als Alternative können Sie das Feld leer lassen.</span><span class="sxs-lookup"><span data-stu-id="8641c-127">Alternatively, leave the field empty.</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="8641c-128">Geben Sie hier keinen Wert in **Bal. Kontonr.** ein</span><span class="sxs-lookup"><span data-stu-id="8641c-128">Do not enter a value in the **Bal. Account No.** field.</span></span>  

4. <span data-ttu-id="8641c-129">Wählen Sie die Schaltfläche **OK** aus, um das Fenster **Genehmigungskommentare** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="8641c-129">Choose the **OK** button to close the **Payment Methods** window.</span></span>  
5. <span data-ttu-id="8641c-130">Geben Sie im Feld **Suchen** **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8641c-130">In the **Search** box, enter **Customers**, and then choose the related link.</span></span>  
6. <span data-ttu-id="8641c-131">Öffnen Sie die Debitorenkarte für den Debitor, der für die SEPA-Basislastschriften eingerichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8641c-131">Open the customer card for the customer that you want to set up for SEPA direct debit collection.</span></span>  
7. <span data-ttu-id="8641c-132">Wählen Sie das Feld , und wählen Sie dann den **Zahlungsformcode**, den Sie in Schritt 3 angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="8641c-132">Choose the **Payment Method Code** field, and then select the payment method code that you specified in step 3.</span></span>  
8. <span data-ttu-id="8641c-133">Wiederholen Sie die Schritte 6 und 7 für alle Debitoren, die Sie für SEPA-Basislastschriften einrichten wollen.</span><span class="sxs-lookup"><span data-stu-id="8641c-133">Repeat steps 6 and 7 for all customers that you want to set up for SEPA direct debit collection.</span></span>  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a><span data-ttu-id="8641c-134">Einrichten der Einzugsermächtigung, entsprechend der Vereinbarung mit dem Debitor</span><span class="sxs-lookup"><span data-stu-id="8641c-134">To set up the direct-debit mandate that represents the customer agreement</span></span>  
1. <span data-ttu-id="8641c-135">Geben Sie im Feld **Suchen** **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8641c-135">In the **Search** box, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8641c-136">Öffnen Sie die Karte für den Debitor, der für die SEPA-Basislastschriften eingerichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8641c-136">Open the card for the customer that you want to set up for SEPA direct debits.</span></span>  
3. <span data-ttu-id="8641c-137">Wählen Sie die **Bankkonten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="8641c-137">Choose the **Bank Accounts** action.</span></span>  
4. <span data-ttu-id="8641c-138">Wählen Sie im Feld **Debitor-Bankkontenliste** das Debitorenbankkonto, das Basislastschriften verwenden wird, und wählen Sie dann auf der Registerkarte **Start**, in der Gruppe **Prozess**, **Einzugsermächtigungen**.</span><span class="sxs-lookup"><span data-stu-id="8641c-138">In the **Customer Bank Account List** window, select the customer bank account that will use direct debits, and then, on the **Home** tab, in the **Process** group, choose **Direct Debit Mandates**.</span></span>  
5. <span data-ttu-id="8641c-139">Füllen Sie im Fenster Liste der notwendigen **SEPA-Felder** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="8641c-139">In the **SEPA Direct Debit Mandates** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="8641c-140">[Feld</span><span class="sxs-lookup"><span data-stu-id="8641c-140">[Field</span></span>|<span data-ttu-id="8641c-141">Beschreibung]</span><span class="sxs-lookup"><span data-stu-id="8641c-141">Description]</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="8641c-142">**Debitor Bankkontocode**</span><span class="sxs-lookup"><span data-stu-id="8641c-142">**Customer Bank Account Code**</span></span>|<span data-ttu-id="8641c-143">Gibt das Bankkonto an, aus dem Lastschrifteinzüge abgebucht werden.</span><span class="sxs-lookup"><span data-stu-id="8641c-143">Specifies the bank account from which direct\-debit payments are collected.</span></span> <span data-ttu-id="8641c-144">Dieses Feld wird automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="8641c-144">This field is filled automatically.</span></span>|  
    |<span data-ttu-id="8641c-145">**Gültig ab**</span><span class="sxs-lookup"><span data-stu-id="8641c-145">**Valid From**</span></span>|<span data-ttu-id="8641c-146">Geben Sie das Datum an, an dem das Lastschrift-Mandat beginnt.</span><span class="sxs-lookup"><span data-stu-id="8641c-146">Specify the date when the direct\-debit mandate starts.</span></span>|  
    |<span data-ttu-id="8641c-147">**Gültig bis**</span><span class="sxs-lookup"><span data-stu-id="8641c-147">**Valid To**</span></span>|<span data-ttu-id="8641c-148">Geben Sie das Datum an, an dem das Lastschrift-Mandat endet.</span><span class="sxs-lookup"><span data-stu-id="8641c-148">Specify the date when the direct\-debit mandate ends.</span></span>|  
    |<span data-ttu-id="8641c-149">**Datum der Unterschrift**</span><span class="sxs-lookup"><span data-stu-id="8641c-149">**Date of Signature**</span></span>|<span data-ttu-id="8641c-150">Geben Sie das Datum an, an dem der Kunde das Lastschrift-Mandat unterzeichnet hat.</span><span class="sxs-lookup"><span data-stu-id="8641c-150">Specify the date when the customer signed the direct\-debit mandate.</span></span>|  
    |<span data-ttu-id="8641c-151">**Zahlungstyp**</span><span class="sxs-lookup"><span data-stu-id="8641c-151">**Sequence Type**</span></span>|<span data-ttu-id="8641c-152">Geben Sie an, ob die Übereinkunft mehrere (**Wiederkehrende**) oder einen einzelnen (**Einmalig**) Basislastschrifteinzug abdeckt.</span><span class="sxs-lookup"><span data-stu-id="8641c-152">Specify if the agreement covers multiple (**Recurring**) or a single (**One Off**) direct debit collection.</span></span>|  
    |<span data-ttu-id="8641c-153">**Erwartete Anzahl Sollbeträge**</span><span class="sxs-lookup"><span data-stu-id="8641c-153">**Expected Number of Debits**</span></span>|<span data-ttu-id="8641c-154">Geben Sie an, wie viele Basislastschrifteinzüge Sie zu tätigen erwarten.</span><span class="sxs-lookup"><span data-stu-id="8641c-154">Specify how many direct debit collections you expect to make.</span></span> <span data-ttu-id="8641c-155">Dieses Feld ist nur relevant, wenn Sie **Wiederkehrend** im Feld **Sequenzart**ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="8641c-155">This field is only relevant if you selected **Recurring** in the **Sequence Type** field.</span></span>|  
    |<span data-ttu-id="8641c-156">**Sollzähler**</span><span class="sxs-lookup"><span data-stu-id="8641c-156">**Debit Counter**</span></span>|<span data-ttu-id="8641c-157">Gibt an, wie viele Lastschrift-Einzüge mit diesem Lastschrift-Mandat durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="8641c-157">Specifies how many direct debit collections have been made using this direct\-debit mandate.</span></span> <span data-ttu-id="8641c-158">Dieses Feld wird automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8641c-158">This field is automatically updated.</span></span>|  
    |<span data-ttu-id="8641c-159">**Gesperrt**</span><span class="sxs-lookup"><span data-stu-id="8641c-159">**Blocked**</span></span>|<span data-ttu-id="8641c-160">Geben Sie an, dass Lastschrifteinzüge mit diesem Lastschrift-Mandat nicht durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="8641c-160">Specify that direct debit collections cannot be made using this direct\-debit mandate.</span></span>|  

6.  <span data-ttu-id="8641c-161">Wiederholen Sie die Schritte 1 bis 5 für alle Debitoren, die für die SEPA-Basislastschriften eingerichtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8641c-161">Repeat steps 1 through 5 for all customers that you want to set up for SEPA direct debits.</span></span>  

 <span data-ttu-id="8641c-162">Das Lastschrift-Mandat wird automatisch in das Feld **Lastschrift-Mandat-ID** eingegeben, wenn Sie eine Verkaufsrechnung für den Debitor erstellen, den Sie in Schritt 2 ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="8641c-162">The direct-debit mandate is automatically inserted in the **Direct Debit Mandate ID** field when you create a sales invoice for the customer that you selected in step 2.</span></span> <span data-ttu-id="8641c-163">Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="8641c-163">For more information, see [How to: Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="8641c-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8641c-164">See Also</span></span>  
[<span data-ttu-id="8641c-165">Erfassen von Zahlungen per Basislastschriftverfahren SEPA</span><span class="sxs-lookup"><span data-stu-id="8641c-165">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
<span data-ttu-id="8641c-166">[Vorgehensweise: Datenaustauschdefinitionen einrichten](across-how-to-set-up-data-exchange-definitions.md)
[Vorgehensweise: Wiederkehrende Verkaufs- und Einkaufszeilen einrichten](sales-how-work-standard-lines.md)
[Datenaustausch als elektronische Belege](across-data-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="8641c-166">[How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md)
[How to: Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md)
[Exchanging Data as Electronic Documents](across-data-exchange.md)</span></span>
