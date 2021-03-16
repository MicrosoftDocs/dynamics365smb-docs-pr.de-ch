---
title: Elektronische Zahlungen (Schweiz)
description: Schweizer Erweiterungen ermöglichen Ihnen, elektronisch Rechnungen an Debitoren zu senden. Sie können Rechnungen direkt mithilfe der Onlinebankingsoftware des Debitors ausstellen und bezahlen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2c7ec0e1b6c497ba965233716480b66715ed8c8d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382693"
---
# <a name="swiss-electronic-payments"></a>Elektronische Zahlungen (Schweiz)
[!INCLUDE[prod_short](../../includes/prod_short.md)]ermöglicht Ihnen, elektronisch Rechnungen an Debitoren zu senden. Sie können Rechnungen direkt mithilfe der Onlinebankingsoftware des Debitors ausstellen und bezahlen.  

## <a name="electronic-payment-methods"></a>Elektronische Zahlungsformen  
Elektronische Zahlungen können mithilfe der folgenden Zahlungsformen durchgeführt werden:  

- Einzahlungsschein mit Referenznummer (ESR)  
- Lastschrift Verfahren (LSV+)  
- SEPA Kreditübertragungen  

## <a name="esr"></a>ESR  
ESR ist ein elektronischer Kreditorendienst, der Zahlungsscheine zum Einziehen von Geld verwendet. Es ist das elektronische Standardzahlungssystem, das von Swiss Post ins Leben gerufen wurde. ESR-Zahlungsscheine können als Rechnungsanlage gedruckt, ESR-Referenznummern berechnet und ESR-Dateien, die Zahlungsinformationen von Banken enthalten, importiert werden. Weitere Informationen erhalten Sie unter [Elektronische Zahlungen mit ESR (Schweiz)](how-to-print-esr-invoices.md). ESR- und ESR+-Zahlungen können auch mithilfe der Bankversion dieser Zahlungsmethode mit der Bezeichnung Bank-ESR (BESR) durchgeführt werden.  

## <a name="lsv"></a>LSV+  
LSV+ ist ein Abbuchungsdienst, der für das Bearbeiten von Zahlungen verwendet wird. Unternehmen können Debitorenzahlungen direkt von der Bank des Debitors mit der Abbuchung freigeben. Debitorenzahlungen per Lastschrift können im LSV+-Bankformat oder im DebitDirect PostFinance-Format angefordert bzw. eingezogen werden. Weitere Informationen erhalten Sie unter [Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md).  

## <a name="sepa-credit-transfers"></a>SEPA Kreditübertragungen  
Um Zahlungsvorschläge entsprechend dem SEPA-Standard zu exportieren, müssen Sie ein Bankkonto verwenden. Um sicherzustellen, dass die entsprechenden Fibuposten mit den generierten für lokale Schweizer Zahlungsformen übereinstimmen (siehe oben), muss der Wert im Feld **Bankkonto Buchungsgruppe** auf der Seite **Bankkontokarte** auf das jeweilige Fibukonto weisen. Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](../../finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)  

## <a name="see-also"></a>Siehe auch  
 [Importieren von Schweizer Bankenclearingnummern](how-to-import-swiss-bank-clearing-numbers.md)  
 [Elektronische Zahlungen mit ESR (Schweiz)](swiss-electronic-payments-using-esr.md)  
 [Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md)  
 [Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md)  
 [Lokale Funktion (Schweiz)](switzerland-local-functionality.md)  
 [Zahlungen vornehmen](../../payables-make-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]