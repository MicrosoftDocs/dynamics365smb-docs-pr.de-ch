---
title: Elektronischer Zahlungsverkehr (Schweiz) mit ESR
description: Die elektronische Zahlungsform "Einzahlungsschein mit Referenznummer" (ESR) ist ein elektronischer Debitorendienst, mit dem der Debitor offene Rechnungen in Schweizer Franken (CHF) und Euro (EUR) fakturieren und eingehende Zahlungen effizient buchen kann.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5bb65a918616d03bac5294c67e67c7d84d879049
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916379"
---
# <a name="swiss-electronic-payments-using-esr"></a><span data-ttu-id="90d7b-103">Elektronischer Zahlungsverkehr (Schweiz) mit ESR</span><span class="sxs-lookup"><span data-stu-id="90d7b-103">Swiss Electronic Payments Using ESR</span></span>
<span data-ttu-id="90d7b-104">Die Zahlungsform mit Einzahlungsschein mit Referenznummer (ESR) ist ein elektronischer Schuldnerdienst, mit dem Kunden offene Rechnungen in Schweizer Franken (CHF) und Euro (EUR) begleichen können und eingehende Zahlungen effizient buchen können.</span><span class="sxs-lookup"><span data-stu-id="90d7b-104">The Einzahlungsschein mit Referenznummer (ESR) electronic payment method is an electronic debtor service that allows the customer to bill open invoices in Swiss Francs (CHF) and Euros (EUR), and to post incoming payments efficiently.</span></span> <span data-ttu-id="90d7b-105">Die Referenznummer oder Codezeile enthält alle relevanten Buchhaltungsdaten.</span><span class="sxs-lookup"><span data-stu-id="90d7b-105">The reference number, or code line, contains all relevant bookkeeping data.</span></span>  

<span data-ttu-id="90d7b-106">Elektronische Zahlungen mittels ESR bieten folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="90d7b-106">With ESR electronic payments, you can do the following:</span></span>  

- <span data-ttu-id="90d7b-107">Senden Sie ESR-Einzahlungsscheine mit eindeutigen Referenznummern auf den Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="90d7b-107">Send ESR payment slips with unique reference numbers on the invoices.</span></span> <span data-ttu-id="90d7b-108">Durch die eindeutigen ESR-Referenznummern werden mit den Ausgleichszahlungen automatisch die zugehörigen Rechnungen ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="90d7b-108">Because of the unique ESR reference numbers, the payments for settlement are automatically applied to the related invoices.</span></span> <span data-ttu-id="90d7b-109">Weitere Informationen finden Sie unter [Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="90d7b-109">For more information, see [Print ESR Invoices](how-to-print-esr-invoices.md).</span></span>  

- <span data-ttu-id="90d7b-110">Laden Sie die ESR-Dateien täglich von der Bank herunter.</span><span class="sxs-lookup"><span data-stu-id="90d7b-110">Download the ESR files from the bank daily.</span></span> <span data-ttu-id="90d7b-111">Die Dateien enthalten Informationen zu allen bezahlten Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="90d7b-111">The files contain information about all paid invoices.</span></span>  

- <span data-ttu-id="90d7b-112">Importieren Sie die ESR-Dateien, und erstellen Sie automatisch für jede Zahlung Zahlungszeilen.</span><span class="sxs-lookup"><span data-stu-id="90d7b-112">Import the ESR files and create payment lines automatically for each payment.</span></span> <span data-ttu-id="90d7b-113">Weitere Informationen finden Sie unter [Importieren von ESR-Zahlungen](how-to-import-esr-payments.md).</span><span class="sxs-lookup"><span data-stu-id="90d7b-113">For more information, see [Import ESR Payments](how-to-import-esr-payments.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="90d7b-114">Vor der Verwendung des ESR-Moduls müssen die Bank, das Bankkonto und der Dateiname eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="90d7b-114">Before you can use the ESR module, you must set up the bank, bank account, and file name.</span></span> <span data-ttu-id="90d7b-115">Sie müssen auch festlegen, ob ESR oder ESR+ verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="90d7b-115">You must also specify whether ESR or ESR+ should be used.</span></span>

<span data-ttu-id="90d7b-116">Nachdem Sie die Einrichtungsinformationen überprüft haben, können Sie das Rechnungsformular anpassen und eine Testserie erstellen, die von der Bank oder dem Postdienst überprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="90d7b-116">When you have evaluated the setup information, you can adjust the invoice form, and you can create a test series that you can ask your bank or postal service to validate.</span></span>  

<span data-ttu-id="90d7b-117">Beachten Sie beim Einrichten von Nummernserien für Rechnungen die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="90d7b-117">When you set up number series for invoices, you must follow these guidelines:</span></span>  

- <span data-ttu-id="90d7b-118">Verwenden Sie maximal acht Ziffern.</span><span class="sxs-lookup"><span data-stu-id="90d7b-118">Use a maximum of eight digits.</span></span>  
- <span data-ttu-id="90d7b-119">Verwenden Sie nur numerische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="90d7b-119">Use only numeric characters.</span></span>  
- <span data-ttu-id="90d7b-120">Stellen Sie den Nummern keine Nullen voran.</span><span class="sxs-lookup"><span data-stu-id="90d7b-120">Do not precede numbers with zeros.</span></span>  

## <a name="see-also"></a><span data-ttu-id="90d7b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90d7b-121">See Also</span></span>  
 <span data-ttu-id="90d7b-122">[Elektronische Zahlungen (Schweiz)](swiss-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="90d7b-122">[Swiss Electronic Payments](swiss-electronic-payments.md) </span></span>  
 <span data-ttu-id="90d7b-123">[Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md) </span><span class="sxs-lookup"><span data-stu-id="90d7b-123">[Print ESR Invoices](how-to-print-esr-invoices.md) </span></span>  
 <span data-ttu-id="90d7b-124">[Importieren von ESR-Zahlungen](how-to-import-esr-payments.md) </span><span class="sxs-lookup"><span data-stu-id="90d7b-124">[Import ESR Payments](how-to-import-esr-payments.md) </span></span>  
 <span data-ttu-id="90d7b-125">[Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="90d7b-125">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 [<span data-ttu-id="90d7b-126">Zahlungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="90d7b-126">Making Payments</span></span>](../../payables-make-payments.md)
