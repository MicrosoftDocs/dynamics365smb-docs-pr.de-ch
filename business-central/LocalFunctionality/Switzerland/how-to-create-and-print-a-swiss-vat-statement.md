---
title: Erstellen und Drucken einer Schweizer MWST-Abrechnung
description: Auf Grundlage der Informationen, die Sie auf der Seite MWST-Buchungsmatrix Einr. angegeben haben, kann Business Central automatisch eine neue MWST-Abrechnungseinrichtung für die realisierten MWST-Berichte erstellen. Bevor Sie mit den Gewusst wien in diesem Thema fortfahren, stellen Sie sicher, dass Sie die MWST-Buchungsmatrix mit Werten eingerichtet haben, die für die Verkaufs- und Einkaufsziffernfelder festgelegt wurden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dde79f3c62b47516718f2e409ad172f64199ff2c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775699"
---
# <a name="create-and-print-a-swiss-vat-statement"></a>Erstellen und Drucken einer Schweizer MWST-Abrechnung
Auf Grundlage der Informationen, die Sie auf der Seite **MWST-Buchungsmatrix Einr.** angegeben haben, kann [!INCLUDE[prod_short](../../includes/prod_short.md)] automatisch eine neue MWST-Abrechnungseinrichtung für die realisierten MWST-Berichte erstellen. Bevor Sie mit den Gewusst wien in diesem Thema fortfahren, stellen Sie sicher, dass Sie die MWST-Buchungsmatrix mit Werten eingerichtet haben, die für die Verkaufs- und Einkaufsziffernfelder festgelegt wurden.  

## <a name="to-set-up-a-swiss-vat-statement-template"></a>So richten Sie eine MWST-Abrechnungsvorlage für die Schweiz ein  

1.  Wählen Sie das Symbol ![Glühbirne , das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Tell me-Funktion") aus, geben Sie **MWST-Abrechnungsvorlage aktualisieren** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie eine Vorlage im Feld **Name für MWST-Abrechnung Vorlage**.
3.  Wählen Sie die Schaltfläche **OK** aus. Wählen Sie die Schaltfläche **Ja** aus, um zu bestätigen, dass Sie eine neue Vorlage erstellen möchten.  
4.  Überprüfen Sie die daraus entstehende MWST-Abrechnung, und passen Sie sie bei Bedarf an.  

     Die MWST-Abrechnungs-Seite enthält das Feld **MWST-Abrechnungs-Verschlüsselung**, das angibt, in welche Verschlüsselung des Berichts das Ergebnis gedruckt wird. Das Feld wird von der Stapelverarbeitung automatisch anhand der Informationen auf der Seite **MWST-Buchungsmatrix Einr.** ausgefüllt. Das Feld kann bei Bedarf bearbeitet werden.  

## <a name="to-print-the-swiss-vat-statement"></a>So drucken Sie die MWST-Abrechnung (Schweiz)  

1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](../../media/ui-search/search_small.png "Tell me-Funktion") Symbol öffnet, geben Sie **MWST-Abrechnung Schweiz** ein und wählen Sie dann den entsprechenden Link.  
2.  Füllen Sie auf dem Inforegister **Optionen** die Felder wie in der folgenden Tabelle beschrieben aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Startdatum**|Geben Sie das Datum ein, an dem das Zeitintervall für die Anzeige von MWST-Abrechnungszeilen im Bericht beginnen soll.|  
    |**Enddatum**|Geben Sie das Datum ein, an dem das Zeitintervall für die Anzeige von MWST-Abrechnungszeilen im Bericht enden soll.|  
    |**Geschlossen mit MWST-Journalnr.**|Wählen Sie das MWST-Journal aus, das die Buchungsspurcodes der MWST-Regulierungsposten enthält. Mit dieser Option werden also bereits ausgeglichene Abrechnungsperioden ausgewertet. Wenn Sie diese Option nicht wählen, legen Sie in den folgenden **MWST-Posten einschliessen**-Feldern keine Optionen fest.|  
    |**MWST-Posten einschliessen**|Wählen Sie eine der verfügbaren Optionen.|  
    |**MWST-Posten einschliessen**|Wählen Sie eine der verfügbaren Optionen.|  
    |**Normalsatz %**|Geben Sie den standardmässigen MWST-Satz für den Zeitraum ein.|  
    |**Reduzierter Satz %**|Geben Sie den reduzierten MWST-Satz für bestimmte Waren und Dienstleistungen ein.|  
    |**Beherbergungssatz %**|Geben Sie den MWST-Satz für Beherbergung für den Zeitraum ein.|  
    |**Normal (anderer Satz) %**|Geben Sie einen alternativen MWST-Satz für Standardtransaktionen ein, der für bestimmte Transaktionen während des Zeitraums gilt.|  
    |**Reduziert (anderer Satz) %**|Geben Sie einen alternativen MWST-Satz für andere Transaktionen ein, der für bestimmte Transaktionen während des Zeitraums gilt.|  
    |**Beherbergung (anderer Satz) %**|Geben Sie einen alternativen MWST-Satz für Beherbergung ein, der für bestimmte Transaktionen während des Zeitraums gilt.|  
    |**Beträge in Berichtswährung anzeigen**|Option, um Beträge in einer zusätzlichen Berichtswährung anzuzeigen.|  

## <a name="see-also"></a>Siehe auch  
 [Schweizer Salestax](swiss-value-added-tax.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]