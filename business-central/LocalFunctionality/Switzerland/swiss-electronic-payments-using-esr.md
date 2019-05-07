---
title: Elektronischer Zahlungsverkehr (Schweiz) mit ESR
description: Die elektronische Zahlungsform "Einzahlungsschein mit Referenznummer" (ESR) ist ein elektronischer Debitorendienst, mit dem der Debitor offene Rechnungen in Schweizer Franken (CHF) und Euro (EUR) fakturieren und eingehende Zahlungen effizient buchen kann.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a09c843d740e24ceef4a8d387ccf471cf02a8b7b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "935134"
---
# <a name="swiss-electronic-payments-using-esr"></a><span data-ttu-id="08478-103">Elektronischer Zahlungsverkehr (Schweiz) mit ESR</span><span class="sxs-lookup"><span data-stu-id="08478-103">Swiss Electronic Payments Using ESR</span></span>
<span data-ttu-id="08478-104">Die Zahlungsform mit Einzahlungsschein mit Referenznummer (ESR) ist ein elektronischer Schuldnerdienst, mit dem Kunden offene Rechnungen in Schweizer Franken (CHF) und Euro (EUR) begleichen können und eingehende Zahlungen effizient buchen können.</span><span class="sxs-lookup"><span data-stu-id="08478-104">The Einzahlungsschein mit Referenznummer (ESR) electronic payment method is an electronic debtor service that allows the customer to bill open invoices in Swiss Francs (CHF) and Euros (EUR), and to post incoming payments efficiently.</span></span> <span data-ttu-id="08478-105">Die Referenznummer oder Codezeile enthält alle relevanten Buchhaltungsdaten.</span><span class="sxs-lookup"><span data-stu-id="08478-105">The reference number, or code line, contains all relevant bookkeeping data.</span></span>  

<span data-ttu-id="08478-106">Elektronische Zahlungen mittels ESR bieten folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="08478-106">With ESR electronic payments, you can do the following:</span></span>  

- <span data-ttu-id="08478-107">Senden Sie ESR-Einzahlungsscheine mit eindeutigen Referenznummern auf den Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="08478-107">Send ESR payment slips with unique reference numbers on the invoices.</span></span> <span data-ttu-id="08478-108">Durch die eindeutigen ESR-Referenznummern werden mit den Ausgleichszahlungen automatisch die zugehörigen Rechnungen ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="08478-108">Because of the unique ESR reference numbers, the payments for settlement are automatically applied to the related invoices.</span></span> <span data-ttu-id="08478-109">Weitere Informationen finden Sie unter [Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="08478-109">For more information, see [Print ESR Invoices](how-to-print-esr-invoices.md).</span></span>  

- <span data-ttu-id="08478-110">Laden Sie die ESR-Dateien täglich von der Bank herunter.</span><span class="sxs-lookup"><span data-stu-id="08478-110">Download the ESR files from the bank daily.</span></span> <span data-ttu-id="08478-111">Die Dateien enthalten Informationen zu allen bezahlten Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="08478-111">The files contain information about all paid invoices.</span></span>  

- <span data-ttu-id="08478-112">Importieren Sie die ESR-Dateien, und erstellen Sie automatisch für jede Zahlung Zahlungszeilen.</span><span class="sxs-lookup"><span data-stu-id="08478-112">Import the ESR files and create payment lines automatically for each payment.</span></span> <span data-ttu-id="08478-113">Weitere Informationen finden Sie unter [Importieren von ESR-Zahlungen](how-to-import-esr-payments.md).</span><span class="sxs-lookup"><span data-stu-id="08478-113">For more information, see [Import ESR Payments](how-to-import-esr-payments.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="08478-114">Vor der Verwendung des ESR-Moduls müssen die Bank, das Bankkonto und der Dateiname eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="08478-114">Before you can use the ESR module, you must set up the bank, bank account, and file name.</span></span> <span data-ttu-id="08478-115">Sie müssen auch festlegen, ob ESR oder ESR+ verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08478-115">You must also specify whether ESR or ESR+ should be used.</span></span>

<span data-ttu-id="08478-116">Nachdem Sie die Einrichtungsinformationen überprüft haben, können Sie das Rechnungsformular anpassen und eine Testserie erstellen, die von der Bank oder dem Postdienst überprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="08478-116">When you have evaluated the setup information, you can adjust the invoice form, and you can create a test series that you can ask your bank or postal service to validate.</span></span>  

<span data-ttu-id="08478-117">Beachten Sie beim Einrichten von Nummernserien für Rechnungen die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="08478-117">When you set up number series for invoices, you must follow these guidelines:</span></span>  

- <span data-ttu-id="08478-118">Verwenden Sie maximal acht Ziffern.</span><span class="sxs-lookup"><span data-stu-id="08478-118">Use a maximum of eight digits.</span></span>  
- <span data-ttu-id="08478-119">Verwenden Sie nur numerische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="08478-119">Use only numeric characters.</span></span>  
- <span data-ttu-id="08478-120">Stellen Sie den Nummern keine Nullen voran.</span><span class="sxs-lookup"><span data-stu-id="08478-120">Do not precede numbers with zeros.</span></span>  

## <a name="see-also"></a><span data-ttu-id="08478-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08478-121">See Also</span></span>  
 <span data-ttu-id="08478-122">[Elektronische Zahlungen (Schweiz)](swiss-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="08478-122">[Swiss Electronic Payments](swiss-electronic-payments.md) </span></span>  
 <span data-ttu-id="08478-123">[Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md) </span><span class="sxs-lookup"><span data-stu-id="08478-123">[Print ESR Invoices](how-to-print-esr-invoices.md) </span></span>  
 <span data-ttu-id="08478-124">[Importieren von ESR-Zahlungen](how-to-import-esr-payments.md) </span><span class="sxs-lookup"><span data-stu-id="08478-124">[Import ESR Payments](how-to-import-esr-payments.md) </span></span>  
 <span data-ttu-id="08478-125">[Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="08478-125">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 [<span data-ttu-id="08478-126">Zahlungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="08478-126">Making Payments</span></span>](../../payables-make-payments.md)
