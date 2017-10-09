---
title: "Vorgehensweise: Buchen von Serviceaufträgen | Microsoft Docs"
description: "Nachdem Sie einen Serviceauftrag erstellt und eventuelle Änderungen vorgenommen haben, können Sie den Serviceauftrag buchen. Der Serviceauftrag muss mindestens eine Serviceartikelzeile und eine Servicezeile enthalten, bevor Sie den Auftrag buchen können. Sollte der Auftrag mehr als eine Serviceauftragszeile umfassen, bucht die Anwendung alle Zeilen in einem Durchgang."
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
ms.openlocfilehash: 7cafdcb9f6002d0732ee86b643b784d96e8c2aa1
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-service-orders-and-credit-memos"></a>Vorgehensweise: Buchen von Serviceaufträgen und Gutschriften
Nachdem Sie einen Serviceauftrag erstellt und eventuelle Änderungen vorgenommen haben, können Sie den Serviceauftrag buchen. Der Serviceauftrag muss mindestens eine Serviceartikelzeile und eine Servicezeile enthalten, bevor Sie den Auftrag buchen können. Sollte der Auftrag mehr als eine Serviceauftragszeile umfassen, bucht die Anwendung alle Zeilen in einem Durchgang.  

Wenn Sie eine große Anzahl an Serviceaufträgen haben, können Sie Zeit sparen, wenn Sie diese mit einer Stapelverarbeitung buchen. Sie können diese Stapelverarbeitung aus jedem Serviceauftrag ausführen.

> [!Tip]
> Bevor Sie einen Servicebeleg buchen, ist es vorteilhaft, die **Bericht testen** Aktion zu nutzen, um jeden Fehler oder fehlende Informationen zu prüfen. Wenn es Fehler gibt, müssen Sie das jeweilige Problem lösen. Sie können einen neuen Testbericht ausdrucken, um die Behebung zu bestätigen, und den Beleg dann buchen.
  
## <a name="to-post-a-service-order"></a>So buchen Sie einen Serviceauftrag    
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceaufträge** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie den relevanten Serviceauftrag.  
3. Auf der Seite **Serviceauftrag** wählen Sie eine der folgenden Aktionen aus.  
  
    |**Aktion**|**Ergebnis**|  
    |------------------|----------------|  
    |**Testbericht** | Überprüft alle Teile des Belegs und zeigt das Ergebnis in einem Bericht an. Wenn der Bericht Fehler oder fehlende Informationen angibt, müssen Sie das jeweilige Problem beheben. Sie können dann einen neuen Testbericht drucken.|  
    |**Buchen** | Bucht den Auftrag, ohne einen Lieferschein oder eine Rechnung zu drucken.|  
    |**Buchen und Drucken** | Bucht den Auftrag und druckt einen Lieferschein (wenn Sie den Auftrag liefern, ohne ihn zu fakturieren) oder eine Rechnung (wenn Sie den Auftrag fakturieren).|  
    |**Stapelbuchen** | Bucht mehrere Serviceaufträge einmal gleichzeitig.|  
  
4. Wenn Sie den Auftrag buchen, müssen Sie auswählen, wie Sie den Auftrag buchen möchten. Sie haben folgende Optionen:  
  
    |**Buchungsoption**|**Ergebnis**|  
    |------------------------|----------------|  
    |**Liefern** | Bucht die Lieferung der Artikel.|  
    |**Fakturieren** | Fakturiert Artikel, die bereits geliefert wurden.|  
    |**Liefern und fakturieren** | Fakturiert und liefert die Artikel.|  
    |**Liefern und verbrauchen** | Bucht die Lieferung und den Verbrauch für den Auftrag. Darüber hinaus werden die relevanten Mengen in den Servicezeilen des Auftrags und in den Servicelieferungsbelegen aktualisiert, die im Vorfeld für die Zeile gebucht wurden.|  
  
Sie können den Verbrauch nur buchen, wenn die Zeile eine Menge enthält, die geliefert, jedoch nicht fakturiert oder verbraucht wurde.  
  
Beim Buchen des Auftrags werden die entsprechenden Posten und gebuchten Belege erstellt. Die relevanten Felder werden im Serviceauftragsbeleg aktualisiert.  

## <a name="to-batch-post-service-orders"></a>So buchen Sie Serviceaufträge per Batchauftrag
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceaufträge** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Stapelbuchen** aus.  
3.  Sie können einen Filter setzen, um bestimmte Serviceauftragsnummern oder ein Intervall von Auftragsnummern auszuwählen.  
4.  Klicken Sie zum Starten des Batchauftrags auf **OK**.  

## <a name="to-post-a-service-credit-memo"></a>So buchen Sie Servicegutschriften  
Wenn Sie eine Servicegutschrift erstellt und ausgefüllt haben, können Sie diese Gutschrift buchen. Wenn beim Buchen Fehler oder fehlende Informationen in der Gutschrift vorhanden sind, wird der Vorgang durch eine Fehlermeldung unterbrochen.  
   
1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Servicevertragsgutschriften** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Erstellen Sie eine neue Servicegutschrift. Wählen Sie auf der Registerkarte **Start** in der Gruppe **Neu** die Option **Neu** aus.  
3. Füllen Sie die erforderlichen Felder aus.  
4. Wählen Sie auf der Registerkarte **Aktionen** in der Gruppe **Buchen** die Option **Buchen** aus. Wenn Sie die Gutschrift gleichzeitig buchen und drucken möchten, wählen Sie stattdessen auf **Buchen und drucken**.  
5. Um Gutschriften vor dem Buchen zu prüfen, aktivieren Sie **Testbericht**. Wenn Sie den Bericht ausführen, werden die Buchungsdaten, die im Beleg angegeben wurden, und weitere Daten überprüft.  
6. Bucht mehrere Servicegutschriften gleichzeitig. führen Sie die Stapelverarbeitung **Servicegutschriften stapelbuchen** aus. Das kann vorteilhaft sein, wenn Sie sehr viele Gutschriften buchen müssen.  
  
> [!NOTE]  
>  Es ist wichtig, alle notwendigen Informationen für die Gutschriften einzugeben, bevor für diese die Stapelbuchung erfolgt. Andernfalls werden Sie möglicherweise nicht gebucht. Sind die Buchungen durch den Batchauftrag abgeschlossen, zeigt eine Meldung an, wie viele der Servicegutschriften gebucht worden sind.  

## <a name="to-post-consumption-from-a-service-order"></a>So buchen Sie den Verbrauch von Serviceaufträgen aus  
Im folgenden Verfahren wird beschrieben, wie die Artikel, Ressourcenzeiten und/oder Kosten für eine bestimmte Servicearbeit gebucht werden, die Sie dem Debitor nicht in Rechnung stellen. Der Verbrauch von Artikeln, Stunden oder Kosten kann nur für eine gebuchte Lieferung gebucht werden, für die keine Rechnungen und kein Verbrauch gebucht wurde.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceaufträge** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie den Serviceauftrag, für den der Verbrauch gebucht werden soll.  
3. Wählen Sie den Serviceartikel aus. Wählen Sie **Aktionen** , **Auftrag**, und klicken Sie anschließend auf **Servicezeilen**.  
4. Suchen Sie nach den entsprechenden Posten, und geben Sie im Feld **Mge. zu verbrauchen** die Mengen an, für die Sie den Verbrauch buchen. Die Menge kann nicht größer als die bereits gelieferte Menge und die nicht fakturierte Restmenge nach einer teilweisen Fakturierung dieser Lieferung sein.  
  
    > [!NOTE]  
    >  Füllen Sie die Felder **Projektnr.**, **Projektaufgabennr.** und **Projektzeilenart** für die Servicezeile aus, um den Verbrauch in Bezug auf eine Aufgabe zu erfassen.  
  
5. Wählen Sie die zu buchenden Zeilen aus, und wählen Sie dann die Aktion **Buchen** aus. Wählen Sie auf der daraufhin angezeigten Seite die Option **Liefern und Verbrauchen**.  
  
Der Service wird als teilweise oder vollständig verbraucht gebucht (abhängig vom Wert im Feld **Mge. zu verbrauchen**) und die entsprechenden Posten werden erstellt. Darüber hinaus aktualisiert die Anwendung die zuvor gebuchten Servicelieferungsbelege chronologisch mit den verbrauchten Mengen. Die entsprechenden Mengen werden in den Servicezeilen des Auftrags aktualisiert.  

## <a name="to-post-shipments-from-service-orders"></a>So buchen Sie Lieferungen von Serviceaufträgen aus  
Nachdem Sie die Details eines Service angegeben haben, können Sie die Mengen für verwendete Artikel, Zeitaufwand und angefallene Kosten anpassen und buchen. Daraufhin werden die erforderlichen Änderungen durch [!INCLUDE[d365fin](includes/d365fin_md.md)] vorgenommen, sodass der neue Lagerbestand und der aktuelle Status der jeweiligen Auftragsabwicklung widergespiegelt werden.  
  
Der folgende Ablauf zeigt, wie man Lieferung der Servicezeilenartikel in Lagerplätzen bucht, die nicht so eingerichtet wurden, dass ein Lagerdurchlauf erforderlich ist.  

1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceauftrag** ein. Wählen Sie dann den zugehörigen Link aus. 2. Wählen Sie im Fenster für den ausgewählten Serviceauftrag **Aktionen**, **Auftrag**, **Servicezeilen** aus.  
3. Suchen Sie im Fenster **Servicezeilen** nach den entsprechenden Posten, und geben Sie die zu buchende Menge in das Feld **Zu liefern Menge** ein.  
  
   > [!NOTE]  
   >  Der Wert für die zu liefernde Menge hängt davon ab, ob Sie die Lieferung teilweise oder insgesamt buchen möchten. Bei einer Gesamtlieferung muss der Wert im Feld **Zu liefernde Menge** dem Wert im Feld **Menge** entsprechen. Wenn Sie eine teilweise Lieferung buchen, müssen Sie die anfänglich zu liefernde Menge angeben. Wenn bereits ein Teil des Service auf dem Auftrag geliefert wurde, geben Sie diesen Wert im Feld **Menge geliefert** an. Die maximale Menge, die Sie in das Feld **Zu liefern** eingeben können, ist die Anzahl der Einheiten, die noch nicht geliefert wurden.  
  
4. Wählen Sie **Aktionen**, **Buchen** und dann nochmals **Buchen** aus. Wählen Sie im daraufhin angezeigten Fenster die Option **Lieferung** aus.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)]Die Anwendung erstellt die Posten (Garantieposten, Artikelposten, Serviceposten oder Sachposten), erzeugt den gebuchten Servicelieferungsbeleg und aktualisiert die entsprechenden Felder in den Serviceauftragszeilen.  
  
Wenn der Lagerort so eingerichtet wurde, dass ein Lagerdurchlauf erforderlich ist, dann erfolgt die Lieferung und Umlagerung der Servicezeilenartikel auf die gleichen Weise wie für andere Herkunftsbelege. Der einzige Unterschied besteht darin, dass Servicezeilenartikel extern oder intern verbraucht werden können und daher zwei unterschiedliche Freigabefunktionen benötigen.  
  
Informationen über die Artikellieferung für Herkunftsbelege in den erweiterten Lagerkonfigurationen, finden Sie unter [Artikel für Lager-Lieferung auswählen](warehouse-pick-items.md).  

## <a name="to-undo-posted-consumption"></a>So machen Sie einen gebuchten Verbrauch rückgängig  
Sie können den Verbrauch der Serviceaufträge kündigen. Beispielsweise, da er versehentlich gebucht wurde.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"), geben **Gebuchte Servicelieferungen** ein und wählen dann den zugehörigen Link aus.  
2. Öffnen Sie die gebuchte Servicelieferung, für die der fehlerhafte Verbrauch gebucht wurde.  
3. Wählen Sie **Aktionen**, **Versand** und dann **Service-Versandzeilen**.  
4. Wählen Sie die Zeilen, die den falschen Verbrauch enthalten aus, und wählen die **Verbrauch stornieren** Aktion aus.  
  
 Für den Ausgleich wird eine Servicelieferungszeile mit negativen Werten in den Mengenfeldern für die ausgewählten Zeilen eingefügt.  
  
> [!NOTE]  
>  Sie können Dienstverbrauch nicht rückgängig machen, wenn:  

>    * Der Serviceauftrag geschlossen wurde.  
>    * Er für im Modul "Projekte" gebucht wurde und Projektposten zugeordnet sind.  
  
## <a name="to-post-service-lines"></a>So buchen Sie Servicezeilen  
Wenn Sie für längere Zeit mit einem Serviceauftrag arbeiten müssen, ohne diesen zu buchen, möchten Sie ggf. schon einige der Zeilen buchen, die damit verknüpft sind, z. B. um das Lager auf dem aktuellen Stand zu halten. Sie können buchen, indem Sie die relevanten Mengen in den zu buchenden Zeilen angeben. Sie können die Zeilen einzeln oder mehrere Zeilen gleichzeitig buchen.  
  
Die folgende Vorgehensweise beschreibt, wie die Lieferungsbuchung direkt aus einem Serviceauftrag heraus für Lagerorte ohne Lagerkosteneinrichtung erfolgt. Wenn der Lagerort so eingerichtet wurde, dass ein Lagerdurchlauf erforderlich ist, dann erfolgt die Lieferungsbuchung in einem anderen Logistikbeleg, abhängig von der Einrichtung des Lagerorts.
  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceaufträge** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie den relevanten Serviceauftrag, und wählen Sie die **Servicezeilen** Aktion aus.  
4. Füllen Sie in den Zeilen, die Sie buchen möchten, die Felder **Zu liefernde Menge**, **Zu fakturierende Menge** und**Mge. zu verbrauchen** aus, je nachdem, wie Sie die Zeilen buchen möchten.  
5. Wählen Sie die Aktion **Buchen** aus.
  
## <a name="see-also"></a>Siehe auch  
[Buchen in der Serviceverwaltung](service-service-posting.md)  
[Vorgehensweise: Erstellen eines Serviceauftrags](service-how-to-create-service-orders.md)  

