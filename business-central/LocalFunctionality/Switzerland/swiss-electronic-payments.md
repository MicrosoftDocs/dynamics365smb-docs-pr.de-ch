---
title: Elektronische Zahlungen (Schweiz)
description: "Schweizer Erweiterungen ermöglichen Ihnen, elektronisch Rechnungen an Debitoren zu senden. Sie können Rechnungen direkt mithilfe der Onlinebankingsoftware des Debitors ausstellen und bezahlen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 2486e653c19be631386cea9ea2d98ad97b7ff8a8
ms.contentlocale: de-ch
ms.lasthandoff: 11/26/2018

---
# <a name="swiss-electronic-payments"></a>Elektronische Zahlungen (Schweiz)
[!INCLUDE[d365fin](../../includes/d365fin_md.md)]ermöglicht Ihnen, elektronisch Rechnungen an Debitoren zu senden. Sie können Rechnungen direkt mithilfe der Onlinebankingsoftware des Debitors ausstellen und bezahlen.  

## <a name="electronic-payment-methods"></a>Elektronische Zahlungsformen  
Elektronische Zahlungen können mithilfe der folgenden Zahlungsformen durchgeführt werden:  

- Einzahlungsschein mit Referenznummer (ESR)  
- Lastschrift Verfahren (LSV+)  
- SEPA Kreditübertragungen  

## <a name="esr"></a>ESR  
ESR ist ein elektronischer Kreditorendienst, der Zahlungsscheine zum Einziehen von Geld verwendet. Es ist das elektronische Standardzahlungssystem, das von Swiss Post ins Leben gerufen wurde. ESR-Zahlungsscheine können als Rechnungsanlage gedruckt, ESR-Referenznummern berechnet und ESR-Dateien, die Zahlungsinformationen von Banken enthalten, importiert werden. Weitere Informationen erhalten Sie unter [Elektronische Zahlungen mit ESR (Schweiz)](how-to-print-esr-invoices.md). Sie können auch ESR- und ESR+-Zahlungen mithilfe der Version dieser Zahlungsform der Bank machen, die Bank-ESR (BESR) heisst.  

## <a name="lsv"></a>LSV+  
LSV+ ist ein Abbuchungsdienst, der für das Bearbeiten von Zahlungen verwendet wird. Unternehmen können Debitorenzahlungen direkt von der Bank des Debitors mit der Abbuchung freigeben. Debitorenzahlungen per Lastschrift können im LSV+-Bankformat oder im DebitDirect PostFinance-Format angefordert bzw. eingezogen werden. Weitere Informationen erhalten Sie unter [Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md).  

## <a name="sepa-credit-transfers"></a>SEPA Kreditübertragungen  
Um Zahlungsvorschläge entsprechend dem SEPA-Standard zu exportieren, müssen Sie ein Bankkonto verwenden. Um sicherzustellen, dass die entsprechenden Fibuposten mit den generierten für lokale Schweizer Zahlungsmethoden übereinstimmen (siehe oben), muss der Wert im Feld **Bankkonto Buchungsgruppe** auf der Seite **Bankkontokarte** auf das jeweilige Fibukonto weisen. Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](../../finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  

## <a name="see-also"></a>Siehe auch  
 [Importieren von Schweizer Bankenclearingnummern](how-to-import-swiss-bank-clearing-numbers.md)   
 [Elektronische Zahlungen mit ESR (Schweiz)](swiss-electronic-payments-using-esr.md)   
 [Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md)   
 [Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md)   
 [Lokale Funktionalität für die Schweiz](switzerland-local-functionality.md) [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](../../finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
 [Zahlungen vornehmen](../../payables-make-payments.md)

