---
title: Elektronischer Zahlungsverkehr (Schweiz) mit ESR
description: Die elektronische Zahlungsform "Einzahlungsschein mit Referenznummer" (ESR) ist ein elektronischer Debitorendienst, mit dem der Debitor offene Rechnungen in Schweizer Franken (CHF) und Euro (EUR) fakturieren und eingehende Zahlungen effizient buchen kann.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 61e80e2ae432a3615a608f2c3f174e0bd7e3f999
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382005"
---
# <a name="swiss-electronic-payments-using-esr"></a>Elektronischer Zahlungsverkehr (Schweiz) mit ESR
Die Zahlungsform mit Einzahlungsschein mit Referenznummer (ESR) ist ein elektronischer Schuldnerdienst, mit dem Kunden offene Rechnungen in Schweizer Franken (CHF) und Euro (EUR) begleichen können und eingehende Zahlungen effizient buchen können. Die Referenznummer oder Codezeile enthält alle relevanten Buchhaltungsdaten.  

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