---
title: Elektronische Zahlungen (Schweiz)
description: 'Schweizer Erweiterungen ermöglichen Ihnen, elektronisch Rechnungen an Debitoren zu senden. Sie können Rechnungen direkt mithilfe der Onlinebankingsoftware des Debitors ausstellen und bezahlen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 03/22/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Elektronische Zahlungen (Schweiz)

[!INCLUDE[prod_short](../../includes/prod_short.md)]ermöglicht Ihnen, elektronisch Rechnungen an Debitoren zu senden. Sie können Rechnungen direkt mithilfe der Onlinebankingsoftware des Debitors ausstellen und bezahlen.  

## Elektronische Zahlungsformen

Elektronische Zahlungen können mithilfe der folgenden Zahlungsformen durchgeführt werden:  

- Einzahlungsschein mit Referenznummer (ESR)  
- Lastschrift Verfahren (LSV+)  
- SEPA Kreditübertragungen  

## ESR

ESR ist ein elektronischer Kreditorendienst, der Zahlungsscheine zum Einziehen von Geld verwendet. Es ist das elektronische Standardzahlungssystem, das von Swiss Post ins Leben gerufen wurde. ESR-Zahlungsscheine können als Rechnungsanlage gedruckt, ESR-Referenznummern berechnet und ESR-Dateien, die Zahlungsinformationen von Banken enthalten, importiert werden. Weitere Informationen erhalten Sie unter [Elektronische Zahlungen mit ESR (Schweiz)](how-to-print-esr-invoices.md). ESR- und ESR+-Zahlungen können auch mithilfe der Bankversion dieser Zahlungsmethode mit der Bezeichnung Bank-ESR (BESR) durchgeführt werden.  

## LSV+

LSV+ ist ein Abbuchungsdienst, der für das Bearbeiten von Zahlungen verwendet wird. Unternehmen können Debitorenzahlungen direkt von der Bank des Debitors mit der Abbuchung freigeben. Debitorenzahlungen per Lastschrift können im LSV+-Bankformat oder im DebitDirect PostFinance-Format angefordert bzw. eingezogen werden. Weitere Informationen erhalten Sie unter [Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md).  

## SEPA Kreditübertragungen

Um Zahlungsvorschläge entsprechend dem SEPA-Standard zu exportieren, müssen Sie ein Bankkonto verwenden. In den Bankkonten muss das Feld **Bankkto.-Buchungsgruppe** das entsprechende Fibukonto angeben. Auf diese Weise werden die entsprechenden Fibuposten konsistent mit den Einträgen, die für die Schweizer Zahlungsmethoden generiert wurden. Weitere Informationen finden Sie unter [SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](../../finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)  

### <a name="iban-qr"></a>IBAN und QR-IBAN

In der Schweiz können Zahlungsanfragen auf Basis von SEPA Kreditübertragungen einen regulären IBAN-Code für das Bankkonto oder einen QR-IBAN-Code enthalten. Weitere Informationen finden Sie unter [QR-Rechnungsverwaltung](ui-extensions-qr-bill-management.md).  

Der IBAN-Typ im Bankkonto des Empfängers muss mit dem Zahlungsreferenztyp im Eintrag übereinstimmen, wenn Sie versuchen, einen Kreditor zu bezahlen. Falls es sich bei der Zahlungsreferenz um eine QR-Referenz handelt, überprüft [!INCLUDE [prod_short](../../includes/prod_short.md)], dass die IBAN im Kreditorenbankkonto ein QR-IBAN-Code ist. Falls es sich bei der Zahlungsreferenz um eine Kreditorenreferenz handelt, muss diese IBAN eine normale IBAN sein.  

> [!TIP]
> Falls ein Kreditor beide Kontotypen regelmäßig verwendet, erstellen Sie mehrere Kreditorenbankkonten und verwenden sie entsprechend. Weitere Informationen finden Sie unter [Verwendung mehrerer Bankkonten als Ersteller von QR-Rechnungen](ui-extensions-qr-bill-management.md#multiplebankaccounts).

## Weitere Informationen

[QR-Bill Management in der Schweizer Version](ui-extensions-qr-bill-management.md)  
[Importieren von Schweizer Bankenclearingnummern](how-to-import-swiss-bank-clearing-numbers.md)  
[Elektronische Zahlungen mit ESR (Schweiz)](swiss-electronic-payments-using-esr.md)  
[Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md)  
[Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md)  
[Lokale Funktion (Schweiz)](switzerland-local-functionality.md)  
[Zahlungen vornehmen](../../payables-make-payments.md)
[SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](../../finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]