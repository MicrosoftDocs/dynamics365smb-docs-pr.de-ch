---
title: "Einrichten und Verwenden von Standardzeilen für Wiederverkäufe und -einkäufe| Microsoft Docs"
description: "Sie können Verkaufszeilen und Einkaufszeilen einrichten, die Sie häufig machen und diese dann in Verkaufs- und Einkaufsbelegen einfügen, um die Zeilen mit Standardinformationen schnell auszufüllen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 980a0646317c2b5c02c0eadcde9ba984c11580c4
ms.contentlocale: de-ch
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="8f0a6-103">Vorgehensweise: Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen</span><span class="sxs-lookup"><span data-stu-id="8f0a6-103">How to: Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="8f0a6-104">Wenn Sie häufiger Verkaufs- und Einkaufszeilen mit ähnlichen Daten erstellen müssen, können Sie die Standardzeilen einrichten, die Sie in wiederkehrenden Verkaufs- und Einkaufsbelegen, z. B. für wiederkehrende Ersatzaufträge benötigen.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="8f0a6-105">Der folgende Ablauf zeigt, wie man Standardverkaufszeilen einrichtet.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="8f0a6-106">Es geht auf ähnliche Weise für Standardeinkaufszeilen.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="8f0a6-107">So richten Sie eine Standard-Verkaufszeile ein</span><span class="sxs-lookup"><span data-stu-id="8f0a6-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="8f0a6-108">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Standardverkaufscode** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Sales Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f0a6-109">Wählen Sie im Fenster **Standardverkaufszeile** die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="8f0a6-110">Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="8f0a6-111">Im Inforegister **Zeilen** können Sie Informationen in die Felder eingeben, um Verkaufszeilen vorzubereiten, die die Standardzeilen widerspiegeln, von der Sie erwarten, wiederkehrende Zeilen in Einkaufsbelegen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="8f0a6-112">Um auf einer Verkaufsrechnung Standardverkaufszeilen einfügen</span><span class="sxs-lookup"><span data-stu-id="8f0a6-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="8f0a6-113">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Rechnung** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="8f0a6-114">Öffnen Sie die Verkaufsrechnung, in die Sie eine oder mehrere Standard-Verkaufszeilen einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="8f0a6-115">Wählen Sie die **Wiederkehrende Verkaufszeilen abrufen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="8f0a6-116">Im Fenster **Wiederkehrende Verkaufszeilen** wählen Sie die Suchschaltfläche im Feld **Code**, und wählen einen Satz von Standardverkaufszeilen aus.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>
5. <span data-ttu-id="8f0a6-117">Wählen Sie die Schaltfläche **OK**, um die Standardverkaufszeilen in die Rechnung einzufügen, in die Sie Informationen verwenden ist beim oder bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-117">Choose the **OK** button to insert the standard sales lines on the invoice, where you can reuse as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="8f0a6-118">Vorgehensweise: Mehrere Verkaufsrechnungen auf der Grundlage von Standardverkaufscodes erstellen</span><span class="sxs-lookup"><span data-stu-id="8f0a6-118">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="8f0a6-119">Alternativ können Sie **Wiederkehrende Verkaufsrechnung erstellen** verwenden.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-119">You can use the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="8f0a6-120">Sie können mit der -Stapelverarbeitung Verkaufsrechnungen gemäß Standardverkaufscodes erstellen, die den Debitoren zugeordnet sind und Buchungsdaten enthalten, die innerhalb der Gültigkeitszeiträume liegen, die Sie im Standardverkaufscode festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-120">batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales code.</span></span>

<span data-ttu-id="8f0a6-121">Im Fenster **Wiederkehrende Verkaufszeilen** können Sie auch eine Einzugsmethode und ein Lastschrift-Mandat angeben.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-121">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="8f0a6-122">Die Verkaufsrechnung, die mit **Wiederkehrende Verkaufsrechn. erstellen** erstellt werden</span><span class="sxs-lookup"><span data-stu-id="8f0a6-122">The sales invoices that are created with the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="8f0a6-123">Batchauftrag umfasst dann die Informationen, die benötigt werden, die Zahlung der Verkaufsrechnungen mit Abbuchung SEPA zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-123">batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="8f0a6-124">Weitere Informationen finden Sie unter Einziehen von Zahlungen mit Abbuchung SEPA.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-124">For more information, see Collect Payments with SEPA Direct Debit.</span></span>

1. <span data-ttu-id="8f0a6-125">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Wiederkehrende Verkaufsrechnung** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="8f0a6-126">Im Fenster **Wiederkehrende Verkaufsrechn. erstellen**</span><span class="sxs-lookup"><span data-stu-id="8f0a6-126">In the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="8f0a6-127">füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-127">window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="8f0a6-128">In dem Feld **Code** geben Sie den Code der Standardverkaufscode ein, die einem Debitor zugewiesen sind, für den Verkaufsrechnungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-128">In the **Code** field, enter the code for standard sales lines assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="8f0a6-129">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-129">Choose the **OK** button.</span></span>

<span data-ttu-id="8f0a6-130">Verkaufsrechnungen werden für die Debitoren mit dem angegebenen Standard-Debitorenvertriebscode und allen angegebenen Direkteinzugsinformationen zur Buchung am angegebenen Datum erstellt.</span><span class="sxs-lookup"><span data-stu-id="8f0a6-130">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f0a6-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f0a6-131">See Also</span></span>  
[<span data-ttu-id="8f0a6-132">Verkauf</span><span class="sxs-lookup"><span data-stu-id="8f0a6-132">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="8f0a6-133">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f0a6-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

