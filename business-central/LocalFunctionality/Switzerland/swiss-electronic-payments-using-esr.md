---
title: 'Elektronischer Zahlungsverkehr mit ESR [CH]'
description: 'In diesem Thema werden die verschiedenen Aufgaben erläutert, die Sie mit dem elektronischen Kreditorendienst Einzahlungsschein mit Referenznummer (ESR) abwickeln können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '3010531, 3010532'
ms.date: 06/21/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="swiss-electronic-payments-using-esr-in-the-swiss-version"></a>Elektronische Zahlungen mit ESR in der Schweizer Version
Die elektronische Zahlungsform "Einzahlungsschein mit Referenznummer" (ESR) ist ein elektronischer Debitorendienst, mit dem der Debitor offene Rechnungen in Schweizer Franken (CHF) und Euro (EUR) fakturieren und eingehende Zahlungen effizient buchen kann. Die Referenznummer oder Codezeile enthält alle relevanten Buchhaltungsdaten.  

Elektronische Zahlungen mittels ESR bieten folgende Möglichkeiten:  

- Senden Sie ESR-Einzahlungsscheine mit eindeutigen Referenznummern auf den Rechnungen. Durch die eindeutigen ESR-Referenznummern werden mit den Ausgleichszahlungen automatisch die zugehörigen Rechnungen ausgeglichen. Weitere Informationen finden Sie unter [Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md).  

- Laden Sie die ESR-Dateien täglich von der Bank herunter. Die Dateien enthalten Informationen zu allen bezahlten Rechnungen.  

- Importieren Sie die ESR-Dateien, und erstellen Sie automatisch für jede Zahlung Zahlungszeilen. Weitere Informationen finden Sie unter [Importieren von ESR-Zahlungen](how-to-import-esr-payments.md).  

> [!NOTE]  
>  Vor der Verwendung des ESR-Moduls müssen die Bank, das Bankkonto und der Dateiname eingerichtet werden. Sie müssen auch festlegen, ob ESR oder ESR+ verwendet werden soll.

Nachdem Sie die Einrichtungsinformationen überprüft haben, können Sie das Rechnungsformular anpassen und eine Testserie erstellen, die von der Bank oder dem Postdienst überprüft werden kann.  

Beachten Sie beim Einrichten von Nummernserien für Rechnungen die folgenden Richtlinien:  

- Verwenden Sie maximal acht Ziffern.  
- Verwenden Sie nur numerische Zeichen.  
- Stellen Sie den Nummern keine Nullen voran.  

## <a name="see-also"></a>Siehe auch
 [Elektronische Zahlungen (Schweiz)](swiss-electronic-payments.md)   
 [Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md)   
 [Importieren von ESR-Zahlungen](how-to-import-esr-payments.md)   
 [Elektronische Zahlungen mit LSV+ (Schweiz)](swiss-electronic-payments-using-lsv-.md)   
 [Zahlungen vornehmen](../../payables-make-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
