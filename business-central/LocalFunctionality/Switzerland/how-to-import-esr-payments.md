---
title: Importieren von ESR-Zahlungen [CH]
description: Nach Eingang einer Zahlung eines Debitors erhalten Sie eine ESR-Datei mit Informationen zu bezahlten Rechnungen auf elektronischem Weg von der Bank.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 3010531, 3010532
ms.date: 06/21/2021
ms.author: edupont
ms.openlocfilehash: 069b5ba67f023f60fb7d57f88d680cb8a3a9773b
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136621"
---
# <a name="import-esr-payments-in-the-swiss-version"></a>ESR-Zahlungen importieren in der Schweizer Version
Nach Eingang einer Zahlung eines Debitors erhalten Sie eine Datei mit Informationen zu bezahlten Rechnungen. Sie können diese Datei elektronisch von der Bank oder per E-Mail empfangen.  

Sie können die ESR (Einzahlungsschein mit Referenznummer)-Rechnungsdaten aus der Datei importieren, die Daten mithilfe des ESR-Berichts für Verkaufsrechnungen oder des ESR-Abschnittberichts drucken und diese vor der Buchung überprüfen. Weitere Informationen finden Sie unter [Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md).  

## <a name="to-import-esr-payments"></a>So importieren Sie ESR-Zahlungen  

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../media/ui-search/search_small.png "Tell me-Funktion") Geben Sie im **Zahlungseingangsprotokolle** ein, und wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie im Feld **Erf.-Journalname** den erforderlichen Erf.-Journalnamen aus.  

    > [!NOTE]  
    >  Das Erfassungsjournal muss leer sein, bevor die ESR-Datei importiert werden kann. Sie können jeweils nur eine ESR-Datei in ein Zahlungseingangs Erf.-Journal importieren.  

3.  Wählen Sie die Aktion **ESR-Datei lesen** aus.  

    > [!NOTE]  
    >  Falls Sie mehr als eine ESR-Bank definiert haben, werden Sie in einer Warnmeldung zur Auswahl der entsprechenden Bank aufgefordert. Weitere Informationen finden Sie in der Tabelle "ESR Einrichtung".  

4.  Wählen Sie die Schaltfläche **Ja**, und wählen Sie dann die Schaltfläche **OK**.  

Die Zahlungsinformationen werden in die Journalzeilen importiert. Die Zahlungen werden automatisch für die jeweiligen Rechnungen entsprechend den eindeutigen ESR-Referenznummern übernommen.  

## <a name="see-also"></a>Siehe auch  
 [Elektronische Zahlungen mit ESR (Schweiz)](swiss-electronic-payments-using-esr.md)   
 [Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]