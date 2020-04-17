---
title: Elektronischer Zahlungsverkehr (Schweiz) mit LSV+
description: Die elektronische Zahlungsform Lastschrift Verfahren (LSV+) oder Einzug, eine optimierte Version von LSV, ermöglicht Firmen das direkte Abrufen von Zahlungen von Debitorenbankkonten. Zum Abrufen von Debitorenzahlungen muss eine LSV-Datei an die Bank gesendet werden, die dann die Abbuchung der in der Datei angeforderten Zahlungen abwickelt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: aece4b61f060b38adafb2c4f3d5fc22f3a404f80
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189075"
---
# <a name="swiss-electronic-payments-using-lsv"></a><span data-ttu-id="f60c5-104">Elektronischer Zahlungsverkehr (Schweiz) mit LSV+</span><span class="sxs-lookup"><span data-stu-id="f60c5-104">Swiss Electronic Payments Using LSV+</span></span>
<span data-ttu-id="f60c5-105">Die elektronische Zahlungsform Lastschrift Verfahren (LSV+) oder Einzug, eine optimierte Version von LSV, ermöglicht Firmen das direkte Abrufen von Zahlungen von Debitorenbankkonten.</span><span class="sxs-lookup"><span data-stu-id="f60c5-105">The Lastschrift Verfahren (LSV+)—or direct debit—electronic payment method, an improved version of LSV, allows companies to retrieve payments directly from its customers’ bank accounts.</span></span> <span data-ttu-id="f60c5-106">Zum Abrufen von Debitorenzahlungen muss eine LSV-Datei an die Bank gesendet werden, die dann die Abbuchung der in der Datei angeforderten Zahlungen abwickelt.</span><span class="sxs-lookup"><span data-stu-id="f60c5-106">To retrieve customer payments, you must send an LSV file to the bank, and the bank will collect the payments requested in the file.</span></span>  

<span data-ttu-id="f60c5-107">Die LSV+-Methode ist ein Einzugsverfahren mit Recht auf Widerspruch.</span><span class="sxs-lookup"><span data-stu-id="f60c5-107">The LSV+ method is a direct debit principle with right of objection.</span></span> <span data-ttu-id="f60c5-108">BDD (Business Direct Debit) ist ein Einzugsverfahren ohne Recht auf Widerspruch.</span><span class="sxs-lookup"><span data-stu-id="f60c5-108">Business Direct Debit (BDD) is a direct debit system without right of objection.</span></span> <span data-ttu-id="f60c5-109">Die Formate der an die Bank gesendeten Dateien sind für LSV+ und BDD identisch.</span><span class="sxs-lookup"><span data-stu-id="f60c5-109">The file format to be sent to the bank is the same for LSV+ and BDD.</span></span>  

<span data-ttu-id="f60c5-110">Bevor Sie das LSV-Modul verwenden, müssen die Einstellungen auf der Seite **LSV Einrichtung** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f60c5-110">Before using the LSV module, you must define the settings on the **LSV Setup** page.</span></span>

## <a name="automatic-esr-processing"></a><span data-ttu-id="f60c5-111">Automatische ESR-Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="f60c5-111">Automatic ESR Processing</span></span>  
<span data-ttu-id="f60c5-112">Sie können Zahlungsgutschrifttransaktionen im Einzahlungsschein mit Referenznummer (ESR)-Dateiformat von der Bank herunterladen.</span><span class="sxs-lookup"><span data-stu-id="f60c5-112">You can download payment credit transactions in Einzahlungsschein mit Referenznummer (ESR) file format from the bank.</span></span> <span data-ttu-id="f60c5-113">Wenn die ESR-Referenznummer in das LSV+-System integriert ist, können Sie verarbeitete LSV-Zahlungen in der ESR-Datei erhalten.</span><span class="sxs-lookup"><span data-stu-id="f60c5-113">You can receive processed LSV payments in the ESR file if the ESR reference number is integrated with the LSV+ system.</span></span> <span data-ttu-id="f60c5-114">Wenn LSV+-Zahlungen in Ihren importierten LSV-Dateien enthalten sind, werden die entsprechenden LSV-Journalzeilen automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="f60c5-114">If LSV+ payments are included in your imported LSV files, the related LSV journal lines are closed automatically.</span></span> <span data-ttu-id="f60c5-115">Die automatische ESR-Verarbeitung wird nur bei Zahlungen in Schweizer Franken (CHF) durchgeführt. Hierzu müssen Sie folgende Schritte durchführen:</span><span class="sxs-lookup"><span data-stu-id="f60c5-115">Automatic ESR processing is performed only for payments that use Swiss Francs (CHF), and requires that you do the following:</span></span>  

- <span data-ttu-id="f60c5-116">Nachdem Sie die LSV+-Datei an die Bank gesendet haben, übermitteln Sie innerhalb von drei Tagen nach dem angeforderten LSV-Verarbeitungsdatum einen Zahlungsbericht.</span><span class="sxs-lookup"><span data-stu-id="f60c5-116">After you have sent the LSV+ file to the bank, submit a payments report within three business days following the requested LSV processing date.</span></span>  

- <span data-ttu-id="f60c5-117">Importieren Sie die ESR-Dateien, und buchen Sie die ESR-Journale.</span><span class="sxs-lookup"><span data-stu-id="f60c5-117">Import the ESR files, and post the ESR journals.</span></span> <span data-ttu-id="f60c5-118">Falls eine importierte ESR-Transaktion mit einer offenen LSV+-Zahlungszeile verknüpft ist, wird die entsprechende LSV-Journalzeile automatisch von ESR geschlossen.</span><span class="sxs-lookup"><span data-stu-id="f60c5-118">If an imported ESR transaction is related to an open LSV+ payment line, then the appropriate LSV journal line is automatically closed by ESR.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f60c5-119">Beim Importieren einer ESR-Datei wird die LSV-Journalzeile unabhängig vom ESR-Transaktionstyp von ESR geschlossen, falls das entsprechende LSV-Journal gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="f60c5-119">When importing an ESR file, the LSV journal line is closed by ESR if the appropriate LSV journal is found, regardless of the ESR transaction type.</span></span>  

- <span data-ttu-id="f60c5-120">Nach dem LSV-Verarbeitungsdatum können Sie die LSV-Journalzeilen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f60c5-120">After the LSV processing date, you can check the LSV journal lines.</span></span> <span data-ttu-id="f60c5-121">Wenn alle LSV-Journalzeilen geschlossen sind, wird der **LSV-Status** zu **Beendet** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f60c5-121">If all of the LSV journal lines are closed, then the status of the **LSV Status** field is updated to  **Finished**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f60c5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f60c5-122">See Also</span></span>  
 <span data-ttu-id="f60c5-123">[Verarbeiten eines LSV-Einzugs](how-to-process-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="f60c5-123">[Process an LSV Collection](how-to-process-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="f60c5-124">[Schliessen eines LSV-Einzugs](how-to-close-an-lsv-collection.md) </span><span class="sxs-lookup"><span data-stu-id="f60c5-124">[Close an LSV Collection](how-to-close-an-lsv-collection.md) </span></span>  
 <span data-ttu-id="f60c5-125">[Buchen von LSV+ Zahlungen](how-to-post-lsv-payments.md) </span><span class="sxs-lookup"><span data-stu-id="f60c5-125">[Post LSV+ Payments](how-to-post-lsv-payments.md) </span></span>  
 <span data-ttu-id="f60c5-126">[Exportieren von Zahlungen mit LSV](how-to-export-payments-using-lsv.md) </span><span class="sxs-lookup"><span data-stu-id="f60c5-126">[Export Payments Using LSV](how-to-export-payments-using-lsv.md) </span></span>  
 <span data-ttu-id="f60c5-127">[Elektronische Zahlungen (Schweiz)](swiss-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="f60c5-127">[Swiss Electronic Payments](swiss-electronic-payments.md) </span></span>  
 <span data-ttu-id="f60c5-128">[Elektronische Zahlungen mit ESR (Schweiz)](swiss-electronic-payments-using-esr.md) </span><span class="sxs-lookup"><span data-stu-id="f60c5-128">[Swiss Electronic Payments Using ESR](swiss-electronic-payments-using-esr.md) </span></span>  
 [<span data-ttu-id="f60c5-129">Zahlungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="f60c5-129">Making Payments</span></span>](../../payables-make-payments.md)
