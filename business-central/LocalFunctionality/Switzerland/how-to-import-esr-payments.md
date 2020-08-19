---
title: Importieren von ESR-Zahlungen
description: Nach Eingang einer Zahlung eines Debitors erhalten Sie eine Datei mit Informationen zu bezahlten Rechnungen. Sie können diese Datei elektronisch von der Bank oder per E-Mail empfangen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 19c9947e8a036df4755846e0ae3f627097d21ebf
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677099"
---
# <a name="import-esr-payments"></a><span data-ttu-id="c181f-104">Importieren von ESR-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="c181f-104">Import ESR Payments</span></span>
<span data-ttu-id="c181f-105">Nach Eingang einer Zahlung eines Debitors erhalten Sie eine Datei mit Informationen zu bezahlten Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="c181f-105">After you receive payment from a customer, you receive a file that contains information about paid invoices.</span></span> <span data-ttu-id="c181f-106">Sie können diese Datei elektronisch von der Bank oder per E-Mail empfangen.</span><span class="sxs-lookup"><span data-stu-id="c181f-106">You can receive this file from your bank electronically, or by mail.</span></span>  

<span data-ttu-id="c181f-107">Sie können die ESR (Einzahlungsschein mit Referenznummer)-Rechnungsdaten aus der Datei importieren, die Daten mithilfe des ESR-Berichts für Verkaufsrechnungen oder des ESR-Abschnittberichts drucken und diese vor der Buchung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c181f-107">You can import the Einzahlungsschein mit Referenznummer (ESR) invoice data from the file, print the data by using the sales invoice ESR report or the sales ESR coupon report, and verify before posting.</span></span> <span data-ttu-id="c181f-108">Weitere Informationen finden Sie unter [Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="c181f-108">For more information, see [Print ESR Invoices](how-to-print-esr-invoices.md).</span></span>  

## <a name="to-import-esr-payments"></a><span data-ttu-id="c181f-109">So importieren Sie ESR-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="c181f-109">To import ESR payments</span></span>  

1.  <span data-ttu-id="c181f-110">Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](../../media/ui-search/search_small.png "Tell me-Funktion"), geben Sie **Zlg.-Eing. Erfassungsjournale** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="c181f-110">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cash Receipt Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c181f-111">Wählen Sie im Feld **Erf.-Journalname** den erforderlichen Erf.-Journalnamen aus.</span><span class="sxs-lookup"><span data-stu-id="c181f-111">In the **Batch Name** field, select the required journal batch.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c181f-112">Das Erfassungsjournal muss leer sein, bevor die ESR-Datei importiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c181f-112">The journal must be empty before you import the ESR file.</span></span> <span data-ttu-id="c181f-113">Sie können jeweils nur eine ESR-Datei in ein Zahlungseingangs Erf.-Journal importieren.</span><span class="sxs-lookup"><span data-stu-id="c181f-113">You cannot import more than one ESR file into the same cash receipt journal.</span></span>  

3.  <span data-ttu-id="c181f-114">Wählen Sie die Aktion **ESR-Datei lesen** aus.</span><span class="sxs-lookup"><span data-stu-id="c181f-114">Choose the **Read ESR File** action.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c181f-115">Falls Sie mehr als eine ESR-Bank definiert haben, werden Sie in einer Warnmeldung zur Auswahl der entsprechenden Bank aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c181f-115">If you have defined more than one ESR bank, a warning message displays instructing you to choose the relevant bank.</span></span> <span data-ttu-id="c181f-116">Weitere Informationen finden Sie in der Tabelle "ESR Einrichtung".</span><span class="sxs-lookup"><span data-stu-id="c181f-116">For more information, see the ESR Setup table.</span></span>  

4.  <span data-ttu-id="c181f-117">Wählen Sie die Schaltfläche **Ja**, und wählen Sie dann die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="c181f-117">Choose the **Yes** button, and then choose the **OK** button.</span></span>  

<span data-ttu-id="c181f-118">Die Zahlungsinformationen werden in die Journalzeilen importiert.</span><span class="sxs-lookup"><span data-stu-id="c181f-118">The payments information is imported to the journal lines.</span></span> <span data-ttu-id="c181f-119">Die Zahlungen werden automatisch für die jeweiligen Rechnungen entsprechend den eindeutigen ESR-Referenznummern übernommen.</span><span class="sxs-lookup"><span data-stu-id="c181f-119">The payments are automatically applied to the respective invoices according to unique ESR reference numbers.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c181f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c181f-120">See Also</span></span>  
 <span data-ttu-id="c181f-121">[Elektronische Zahlungen mit ESR (Schweiz)](swiss-electronic-payments-using-esr.md) </span><span class="sxs-lookup"><span data-stu-id="c181f-121">[Swiss Electronic Payments Using ESR](swiss-electronic-payments-using-esr.md) </span></span>  
 [<span data-ttu-id="c181f-122">Drucken von ESR-Rechnungen</span><span class="sxs-lookup"><span data-stu-id="c181f-122">Print ESR Invoices</span></span>](how-to-print-esr-invoices.md)
