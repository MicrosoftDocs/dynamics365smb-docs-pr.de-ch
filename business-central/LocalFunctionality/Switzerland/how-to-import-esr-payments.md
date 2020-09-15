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
ms.author: edupont
ms.openlocfilehash: 13de027afc9aca21812198a3b7bac5b633a2d291
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779839"
---
# <a name="import-esr-payments"></a>Importieren von ESR-Zahlungen
Nach Eingang einer Zahlung eines Debitors erhalten Sie eine Datei mit Informationen zu bezahlten Rechnungen. Sie können diese Datei elektronisch von der Bank oder per E-Mail empfangen.  

Sie können die ESR (Einzahlungsschein mit Referenznummer)-Rechnungsdaten aus der Datei importieren, die Daten mithilfe des ESR-Berichts für Verkaufsrechnungen oder des ESR-Abschnittberichts drucken und diese vor der Buchung überprüfen. Weitere Informationen finden Sie unter [Drucken von ESR-Rechnungen](how-to-print-esr-invoices.md).  

## <a name="to-import-esr-payments"></a>So importieren Sie ESR-Zahlungen  

1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](../../media/ui-search/search_small.png "Tell me-Funktion"), geben Sie **Zlg.-Eing. Erfassungsjournale** ein und wählen Sie dann den entsprechenden Link.  
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
