---
title: "Vorgehensweise: Erstellen von Serviceaufträgen | Microsoft Docs"
description: "Im Fenster **Serviceauftrag** können Sie Belege erstellen, in die Sie Informationen über den Service (Reparatur und Wartung) von Serviceartikeln auf Kundenanfrage eingeben."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cb514fe04fd70836f640d3db4ea592680ab0fa1a
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-service-orders"></a>Vorgehensweise: Erstellen von Serviceaufträgen
Im Fenster **Serviceauftrag** können Sie Belege erstellen, in die Sie Informationen über den Service (Reparatur und Wartung) von Serviceartikeln auf Kundenanfrage eingeben.  
  
Wenn Sie einen Serviceauftrag erstellen, müssen Sie nur einige wenige Felder ausfüllen. Einige Felder sind optional und viele werden automatisch ausgefüllt, wenn Sie die damit verknüpften Felder ausfüllen.  
  
## <a name="to-create-a-service-order"></a>So erstellen Sie einen Serviceauftrag    
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceaufträge** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Erstellen Sie einen neuen Serviceauftrag.  
3. Geben Sie im Feld **Nr.** eine Nummer für den Serviceauftrag ein.  
  
     Wenn Sie im Fenster **Service Einrichtung** Nummernserien für Serviceaufträge definiert haben, drücken Sie EINGABE, um die nächste verfügbare Serviceauftragsnummer auszuwählen.  
  
4. Klicken Sie im Feld **Debitorennr.** Feld wählen Sie den relevanten Debitoren aus der Liste. Die für den Debitor relevanten Felder werden mit den Informationen aus der Tabelle **Debitor** ausgefüllt.  
  
5. Abhängig von den Einstellungen auf dem Inforegister **Pflichtfelder** im Fenster  **Service Einrichtung** muss das Feld **Serviceauftragsart** auf dem Inforegister **Verkäufercode** ausgefüllt werden.  
6. Optional können Sie die restlichen Felder ausfüllen.  
7. Erfassen Sie die Serviceartikelzeilen.  

## <a name="to-create-a-service-order-from-a-contract"></a>So erstellen Sie Serviceaufträge aus Verträgen  
Serviceaufträge können für die Wartung von Serviceartikeln aus Verträgen angelegt werden.  
  
1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Aufträge für Verträge erst.** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Geben Sie auf dem Inforegister **Servicevertragskopf** die gewünschten Filter ein.  
3. Füllen Sie auf dem Inforegister **Optionen** die Felder **Startdatum** und **Enddatum** mit dem Startdatum und dem Enddatum der Periode aus, für die Sie Serviceaufträge erstellen möchten. Die Stapelverarbeitung erzeugt Serviceaufträge mit Serviceartikeln aus Serviceverträgen mit einem Datum des Typs "Nächster geplanter Service am" innerhalb dieser Periode.  
  
    > [!NOTE]  
    >  Die Anzahl der Tage, die Sie als Zeitraum für diese Stapelverarbeitung verwenden können, ist eingeschränkt. Sie können diese Begrenzung im Feld **Serviceaufträge max. Tage** im Fenster **Service Einrichtung** festlegen.  
  
4. Wählen Sie im Feld **Aktion** den Eintrag **Serviceauftrag erstellen** aus.  

## <a name="to-convert-a-service-quote-to-a-service-order"></a>So konvertieren Sie eine Serviceofferte in einen Serviceauftrag
Wenn ein Debitor eine Offerte akzeptiert hat, wandeln Sie dieses in einen Serviceauftrag um. Die Offerte wird gelöscht, und es wird ein neuer Serviceauftrag mit derselben Beschreibung wie in der Serviceofferte eingerichtet. Die Felder "Reagieren bis (Datum)" und "Reagieren bis (Zeit)" werden erneut berechnet, und der Status des Serviceauftrags wird auf **Offen** festgelegt. Der Reparaturstatus der Serviceartikel in dem Auftrag wird auf **Anfang** geändert.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] sucht nach Zuordnungen für alle Serviceartikel der Serviceofferte mit dem Status **Aktiv**. Falls solche Zuordnungsposten gefunden werden, wird der Zuordnungsstatus auf **Neuzuordnung notwendig** aktualisiert. Wenn Sie die Serviceartikel in dem Serviceauftrag neu zuordnen, wird der Status der Zuordnungsposten, die für die Offerte erfasst wurden, auf **Erledigt** aktualisiert.   

1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Servicevertragsofferten** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Serviceofferte aus, die Sie in einen Serviceauftrag umwandeln möchten.  
3. Wählen Sie die **Auftrag erstellen** Aktion aus.  

## <a name="to-check-item-availability-for-one-or-more-orders"></a>So überprüfen Sie die Artikelverfügbarkeit für mindestens einen Auftrag  
Sie können überprüfen, ob ein Artikel, den Sie für einen Auftrag benötigen, auf Lager ist, und wenn nicht, wann der Artikel auf Lager sein wird. Ausserdem können Sie, wenn ein Artikel reservierbar ist, ihn reservieren, um sicherzustellen, dass er für Ihre Verwendung verfügbar ist. Sie können die Verfügbarkeit für einen bestimmten Auftrag oder für alle Aufträge überprüfen.  

1.  Wählen Sie ![Nach Seite oder Bericht sucheb](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") und geben Sie **Einsatzplanung** ein und wählen dann den zugehörigen Link aus.  
2. Führen Sie einen der folgenden Schritte aus:  
  
    * Für einen bestimmten Auftrag wählen Sie den Auftrag und dann die **Bedarfsübersicht** Aktion aus.  
    * Für alle Aufträge wählen Sie **Beleg anzeigen** aus. Das Fenster **Serviceauftrag** wird geöffnet.  
  
3. Erweitern Sie auf der Seite **Bedarfsübersicht** die Artikelgruppierung, und zeigen Sie Informationen über die Verfügbarkeit des Artikels an. Beispielsweise wird angezeigt, wie viele Artikel sich im Lager befinden. Sie können auch feststellen, ob und wann ein Artikel verfügbar ist, ob er sich in Rückstand befindet (das heisst, ob die Herkunftsart = Einkauf ist) oder ob er reserviert wurde. 

## <a name="to-reserve-an-item-for-a-service-order"></a>So reservieren Sie einen Artikel für einen Serviceauftrag:
Wenn Sie sicher sein müssen, dass ein Artikel für einen Serviceauftrag verfügbar ist, können Sie den Artikel reservieren. 

1. Geben Sie im Feld **Suchen** **Serviceaufträge** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie das Menü Bestellung, und wählen Sie dann **Bearbeiten**.  
3. Wählen Sie **Aktionen** , **Auftrag**, und klicken Sie anschließend auf **Servicezeilen**.  
4. Auf der Seite **Servicezeilen** wählen Sie den zu reservierenden Artikel und die **Reservieren** Aktion aus.  
5. Auf der Seite **Reservierung** wählen Sie **Von aktueller Zeile reservieren** aus. 

## <a name="to-insert-lines-based-on-standard-service-codes"></a>So fügen Sie Zeilen basierend auf Standardservicecodes ein  
Wenn Sie Standardservicecodes eingerichtet und Serviceartikelgruppen zugewiesen haben, können Sie die mit den Standardservicecodes verknüpften Standardzeilen in Servicebelege einfügen. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Standardservicecodes](service-how-setup-service-coding.md)   

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceaufträge** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Erstellen Sie einen neuen Serviceauftrag.  
3. Füllen Sie die Felder je nach Bedarf aus.  
4. Geben Sie in die Serviceartikelzeilen die erforderlichen Informationen ein.  
5. Wählen Sie die Zeile mit dem Serviceartikel, für den Sie Servicezeilen erstellen möchten, und wählen Sie dann **Std.-Servicecodes abrufen** aus. Das Fenster **Std.-Serviceartikelgr.-Codes** mit den Standardcodes für die Serviceartikelgruppe, die der Zeile entspricht, wird geöffnet.  
6. Wählen Sie den entsprechenden Code aus, und klicken Sie auf **OK**, um Standardservicezeilen einzugeben.  
  
> [!NOTE]  
>  Wenn das Feld **Serviceartikelgruppencode** in der Serviceartikelzeile des Belegs leer ist, weist dies darauf hin, dass der Serviceartikel nicht zu einer Serviceartikelgruppe gehört. In diesem Fall enthält das Fenster **Std.-Serviceartikelgr.-Codes** eine Liste aller Standardservicecodes. Sie sollten einen Code aus der Liste auswählen, um Standardservicezeilen in den Beleg einzufügen. Sie können auch aus einer Liste von Standardservicecodes wählen, die einer bestimmten Serviceartikelgruppe zugeordnet sind. Um die Liste anzuzeigen, wählen Sie den entsprechenden Code im Feld **Serviceartikelgruppencode** im Fenster **Standard-Serviceartikelgruppen-Codes** aus.  

## <a name="to-register-internal-or-public-comments"></a>So erfassen Sie interne oder öffentliche Bemerkungen
Sie können Bemerkungen hinzufügen, die auf Serviceaufträgen und Serviceofferten gedruckt werden, um zusätzliche Informationen bereitzustellen. Sie können bis zu 80 Zeichen, einschließlich Leerzeichen, hinzufügen. Wenn Sie mehr Text eingeben müssen, wählen Sie eine andere Zeile aus. Um eine Bemerkung zu registrieren, wählen Sie eine Zeile und die **Bemerkungen** Aktion aus.  

## <a name="to-delete-invoiced-service-orders"></a>So löschen Sie fakturierte Serviceaufträge  
Aufträge werden automatisch gelöscht, nachdem diese vollständig fakturiert wurden. Beim Buchen einer Rechnung wird ein entsprechender Posten im Fenster **Gebuchte Servicerechnungen** erstellt. Der gebuchte Beleg kann auf der Seite **Gebuchte Servicerechnung** angezeigt werden.  
  
Serviceaufträge werden aber nicht automatisch gelöscht, wenn die Gesamtmenge des Auftrags nicht aus dem eigentlichen Serviceauftrag, sondern im Fenster **Servicerechnung** gebucht wurde. In diesem Fall müssen Sie fakturierte Aufträge, die nicht gelöscht wurden, manuell löschen. Dazu führen Sie die Stapelverarbeitung **Fakturierte Serviceaufträge löschen** aus.  

1. Alternativ wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fakturierte Serviceaufträge löschen** ein. Wählen Sie dann den zugehörigen Link aus. Das Anforderungsfenster des Batchauftrags **Servicebelegprotok. löschen** wird geöffnet.  
2. Um die zu löschenden Aufträge auszuwählen, können Sie Filter in den Feldern **Nr.**, **Debitorennr.** und **Rech. an Deb.-Nr.** festlegen. Felder.  
3. Wählen Sie **OK** aus.  


## <a name="see-also"></a>Siehe auch  
[Servicebuchung](service-service-posting.md)  
[Vorgehensweise: Buchen von Serviceaufträgen](service-how-to-post-service-orders.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Vorgehensweise: Bearbeiten von Serviceaufgaben](service-how-to-work-on-service-tasks.md)  
[Gewusst wie<. Ressourcen zuweisen](service-how-to-allocate-resources.md)  

