---
title: "Vorgehensweise: Gemeinsames Erfassen und Buchen von Verbrauch und Ausgang für eine einzelne freigegebene Fertigungsauftragszeile | Microsoft Docs"
description: "Diese Ausführungsaufgabe wird im Fenster **Produktions Erfassungsjournal** ausgeführt. In diesem Erfassungsjournal werden die Funktionen des separaten FA-Verbrauchs Erf.-Journals und des FA-Istmeldungs Erf.-Journals in einem Erfassungsjournal kombiniert. Auf das kombinierte Erfassungsjournal wird direkt von einem freigegebenen Fertigungsauftrag aus zugegriffen. Es dient hauptsächlich dazu, den Verbrauch von Komponenten, die Menge der gefertigten Endartikel und die für die Arbeitsgänge aufgewendete Zeit manuell zu buchen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 493c6e24a42229bc6e5223319ca66c103ee08f96
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="register-consumption-and-output-for-one-released-production-order-line"></a>Gemeinsames Erfassen und Buchen von Verbrauch und Istmeldungen für eine einzelne freigegebene Fertigungsauftragszeile
Diese Ausführungsaufgabe wird im Fenster **Produktions Erfassungsjournal** ausgeführt. In diesem Erfassungsjournal werden die Funktionen des separaten FA-Verbrauchs Erf.-Journals und des FA-Istmeldungs Erf.-Journals in einem Erfassungsjournal kombiniert. Auf das kombinierte Erfassungsjournal wird direkt von einem freigegebenen Fertigungsauftrag aus zugegriffen. Es dient hauptsächlich dazu, den Verbrauch von Komponenten, die Menge der gefertigten Endartikel und die für die Arbeitsgänge aufgewendete Zeit manuell zu buchen. Die Werte werden als Posten unter dem freigegebenen Fertigungsauftrag gebucht. Verbrauchsmengen werden als negative Lagerposten gebucht, fertig gestellte Mengen werden als positive Posten gebucht, und die aufgewendeten Zeiten werden als Kapazitätsposten gebucht. Solche gebuchten Posten können auch unten im Erfassungsjournal als Ist-Mengen angezeigt werden.  

> [!NOTE]  
>  Da die Verbrauchsdaten gemeinsam mit den Istmeldungsdaten verwendet werden, bietet dieses Protokoll eine Möglichkeit zum Anzeigen verknüpfter Komponenten und Arbeitsgänge in einer logischen Prozessstruktur. Die Komponenten werden unter dem jeweils zugehörigen Arbeitsgang eingerückt. Dazu ist es erforderlich, dass Sie Verbindungscodes verwenden.  

> [!NOTE]  
>  Komponenten ohne Verbindungscodes werden im Erfassungsjournal zuerst aufgeführt.  

## <a name="to-register-consumption-and-output"></a>Verbrauch und Istmeldungen registrieren  
1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Freigegebene Produktionsaufträge** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Öffnen Sie eine freigegebene FA-Zeile, die zur Registrierung bereitsteht. Klicken Sie auf dem Inforegister **Zeilen** auf die Aktion **Zeilen** und klicken Sie dann auf **Produktions Erf.-Journal**.  

    Das Fenster **Produktions Erf.-Journal** wird geöffnet, und die Erf.-Journalzeilen für den Fertigungsauftrag werden gemäss den Fenstern **FA-Komponente** und **FA-Arbeitsplan** angezeigt. Diese Zeilen stammen aus der Fertigungsstückliste und dem Arbeitsplan, die dem Artikel zugewiesen wurden, der gefertigt wird. Weitere Informationen finden Sie unter [Erstellen von Montagestücklisten](production-how-to-create-routings.md).  

3.  Geben Sie im Feld **Buchungsdatum** ganz oben im Erfassungsjournal ein Buchungsdatum ein, das auf alle Zeilen angewendet wird. Standardmässig wird das Arbeitsdatum eingegeben. Das Feld soll dazu dienen, schnell die Buchungsdaten in allen Zeilen anzugleichen, falls dies erforderlich ist.  

    > [!NOTE]  
    >  Ein Buchungsdatum, das in einzelne Zeilen eingegeben wird, setzt dieses Feld ausser Kraft.  

4.  Im Feld **Buchungsmethodenfilter** ganz oben im Protokoll können Sie auswählen, ob auch der Verbrauch und die Istmeldungen angezeigt werden, die gemäss den jeweils für den Artikel und die Ressource definierten Buchungsmethoden automatisch gebucht werden.  

    In jeder Art von Zeilen des Erfassungsjournals werden nur die relevanten Felder angezeigt. Der Rest ist leer und schreibgeschützt.  

    Beim Öffnen des Erfassungsjournals sind die zu buchenden Mengen voreingestellt. Wenn bisher nichts gebucht wurde, werden in allen Mengenfeldern standardmässig die erwarteten Mengen angezeigt, die aus dem Fertigungsauftrag übernommen wurden. Wenn Teilbuchungen vorgenommen wurden, werden in den Mengenfeldern der Zeilen die Restmengen angezeigt. Die bereits für den Auftrag gebuchten Mengen und Zeiten werden unten im Erfassungsjournal als Ist-Posten angezeigt.  

    Für die Mengen im Feld **Fertig gestellte Menge** können Sie festlegen, welche Werte beim ersten Öffnen des Protokolls als Voreinstellung angezeigt werden. Dies erfolgt im Fenster **Produktion Einrichtung** auf dem Inforegister **Allgemein** im Feld **Vordef. fertig gest. Menge**. 

5.  Geben Sie anschliessend die entsprechenden Mengen in den veränderbaren Feldern für Verbrauch und/oder Istmeldungen ein.  

    > [!NOTE]  
    >  Nur mit der fertig gestellten Menge für die letzte Protokollzeile vom Postenart **Istmeldung** beim Buchen des Protokolls der Lagerbestand angepasst wird. Achten Sie deshalb darauf, dass Sie das Protokoll nicht mit der erwarteten fertig gestellten Menge als Voreinstellung in der letzten Istmeldungszeile buchen, solange nicht alle Endartikel tatsächlich gefertigt wurden.  

6.  Wählen Sie das Feld **Beendet** in den Istmeldungszeilen, um anzugeben, dass der Arbeitsgang beendet ist. Dieses Feld ist mit dem Feld **Arbeitsplanstatus** in einem Arbeitsgang eines Fertigungsauftrags verbunden.  
7.  Klicken Sie auf **Buchen**, um die eingegebenen Mengen zu registrieren und das Erfassungsjournal zu schliessen.  

Wenn Werte zu buchen übrig bleiben, enthält das Erfassungsjournal beim nächsten Öffnen diese verbleibenden Werte. Gebuchte Werte werden als tatsächliche Werte unten auf dem Erfassungsjournal angezeigt.  

> [!NOTE]  
>   Wenn ein im Verbrauch befindlicher Artikel gesperrt ist, werden vom Erfassungsjournal keine Verbrauchsmengen für diesen Artikel gebucht. Wenn ein Arbeitsplatz oder eine Arbeitsplatzgruppe gesperrt ist, werden vom Erfassungsjournal keine fertig gestellten Mengen oder Prozesszeiten für die fragliche Istmeldungszeile gebucht.  

> [!NOTE]  
>  Wenn Sie das Erf.-Journal schliessen, ohne eine Buchung vorzunehmen, gehen die Änderungen verloren.  

> [!WARNING]  
>  Das Fenster **Produktions Erfassungsjournal** kann nicht von zwei Benutzern gleichzeitig verwendet werden. Das bedeutet, wenn Benutzer 2 das Fenster öffnet und Daten eingibt, wenn Benutzer 1 bereits im Fenster arbeitet, dann verliert möglicherweise Benutzer 2 Daten, wenn Benutzer 1 das Fenster schliesst.  

## <a name="see-also"></a>Siehe auch  
[Bearbeitungen](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbesttand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

