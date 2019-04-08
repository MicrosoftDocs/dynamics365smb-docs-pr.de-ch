---
title: Erstellen und Drucken einer Schweizer MWST-Abrechnung
description: Auf Grundlage der Informationen, die Sie auf der Seite MWST-Buchungsmatrix Einr. angegeben haben, kann Business Central automatisch eine neue MWST-Abrechnungseinrichtung für die realisierten MWST-Berichte erstellen. Bevor Sie mit den Gewusst wien in diesem Thema fortfahren, stellen Sie sicher, dass Sie die MWST-Buchungsmatrix mit Werten eingerichtet haben, die für die Verkaufs- und Einkaufsziffernfelder festgelegt wurden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: cb555b9fccc4a39acd629878818dd0301e1b034b
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "827235"
---
# <a name="create-and-print-a-swiss-vat-statement"></a>Erstellen und Drucken einer Schweizer MWST-Abrechnung
Auf Grundlage der Informationen, die Sie auf der Seite **MWST-Buchungsmatrix Einr.** angegeben haben, kann [!INCLUDE[d365fin](../../includes/d365fin_md.md)] automatisch eine neue MWST-Abrechnungseinrichtung für die realisierten MWST-Berichte erstellen. Bevor Sie mit den Gewusst wien in diesem Thema fortfahren, stellen Sie sicher, dass Sie die MWST-Buchungsmatrix mit Werten eingerichtet haben, die für die Verkaufs- und Einkaufsziffernfelder festgelegt wurden.  

## <a name="to-set-up-a-swiss-vat-statement-template"></a>So richten Sie eine MWST-Abrechnungsvorlage für die Schweiz ein  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und öffnen **MWST-Abrechnung Vorlage aktualisieren**. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie eine Vorlage im Feld **Name für MWST-Abrechnung Vorlage**.
3.  Wählen Sie die Schaltfläche **OK** aus. Wählen Sie die Schaltfläche **Ja** aus, um zu bestätigen, dass Sie eine neue Vorlage erstellen möchten.  
4.  Überprüfen Sie die daraus entstehende MWST-Abrechnung, und passen Sie sie bei Bedarf an.  

     Die MWST-Abrechnungs-Seite enthält das Feld **MWST-Abrechnungs-Verschlüsselung**, das angibt, in welche Verschlüsselung des Berichts das Ergebnis gedruckt wird. Das Feld wird von der Stapelverarbeitung automatisch anhand der Informationen auf der Seite **MWST-Buchungsmatrix Einr.** ausgefüllt. Das Feld kann bei Bedarf bearbeitet werden.  

## <a name="to-print-the-swiss-vat-statement"></a>So drucken Sie die MWST-Abrechnung (Schweiz)  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und öffnen **MWST-Abrechnung Schweiz**. Wählen Sie dann den zugehörigen Link aus.  
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
 [Mehrwertsteuer (Schweiz)](swiss-value-added-tax.md)
