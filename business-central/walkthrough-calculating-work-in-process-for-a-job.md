---
title: "Exemplarische Vorgehensweise\_– den Umlaufbestand für ein Projekt berechnen"
description: 'Erfahren Sie, wie Sie den Verbrauch von Mitarbeiterstunden, Maschinenstunden, Bestandsposten und andere Verbrauchsarten während des Projekts verfolgen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 12/13/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="walkthrough-calculating-work-in-process-for-a-project"></a>Exemplarische Vorgehensweise: den Umlaufbestand für ein Projekt berechnen

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Mit Projekten können Sie den Verbrauch der Ressourcen Ihres Unternehmens planen und die verschiedenen Kosten im Zusammenhang mit dem Verbrauch von Ressourcen für ein bestimmtes Projekt verfolgen. Projekte beinhalten den Verbrauch von Mitarbeiterstunden, Maschinenstunden, Bestandsposten und andere Verbrauchsarten, die während des Projekts verfolgt werden müssen. Wenn ein Projekt über einen langen Zeitraum läuft, müssen diese Kosten möglicherweise noch während des Projekts in ein Konto für Umlaufbestand (WIP) in der Bilanz übertragen werden. So können Sie die Kosten und den Umsatz wie erforderlich in den Erfolgsrechnungskonten deklarieren.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise

 In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

-   Berechnen der WIP  
-   Auswählen einer WIP-Berechnungsmethode  
-   Ausschliessen von Teilen eines Projekts von der WIP.  
-   Buchen der WIP auf das Sachkonto  
-   Stornieren einer WIP-Buchung  

 In jedem Schritt des Prozesses wird der Wert berechnet, und die Projekttransaktionen werden in das Fibukonto übertragen. Die Berechnungs- und Buchungsschritte erfolgen getrennt voneinander, sodass Sie die Daten überprüfen und vor dem Buchen in die Finanzbuchhaltung Änderungen vornehmen können. Sie müssen daher nach der Stapelverarbeitung für die Berechnung und vor der Stapelverarbeitung für die Buchung sicherstellen, dass alle Informationen korrekt sind.  

## <a name="roles"></a>Rollen

 In dieser exemplarischen Vorgehensweise wird die Rolle eines Projektteammitglieds (Katrin) verwendet.  

## <a name="prerequisites"></a>Voraussetzungen

 Bevor Sie die Aufgaben in dieser Demonstration ausführen, muss [!INCLUDE[prod_short](includes/prod_short.md)] auf dem Computer installiert sein.  

## <a name="story"></a>Hintergrund

 Im Mittelpunkt dieser exemplarischen Vorgehensweise steht die CRONUS AG, ein Design- und Beratungsunternehmen, das neue Infrastrukturen schafft und anpasst, wie Konferenzräume und Büros mit Möbeln, Zubehör und Lagereinheiten. Ein Grossteil der Arbeit bei CRONUS ist projektorientiert, und Katrin, ein Projektteammitglied, verwendet Projekte, um einen Überblick über die einzelnen laufenden Projekte zu erhalten, die CRONUS gestartet hat, und auch über die Projekte, die abgeschlossen sind. Einige der Projekte können auf sehr lange Zeit angelegt sein und sich über Monate erstrecken. Katrin kann ein Unf.-Arbeit-Konto verwenden, um die unfertige Arbeit zu erfassen und die Kosten während des Projekts zu verfolgen.  

## <a name="calculating-wip"></a>Berechnen der WIP

 CRONUS hat ein Projekt mit langer Laufzeit übernommen, das sich nun über mehrere Berichtszeiträume erstreckt. Tricia, ein Projektteammitglied, berechnet den Umlaufbestand (WIP), um sicherzustellen, dass die Finanzaufstellung des Unternehmens korrekt ist.  

 Bei diesem Verfahren wählt Tricia eine bestimmte Gruppe von Aufgaben aus, die in die WIP-Berechnung einbezogen werden. Katrin kann diese Zeilen auf der Seite **Projektaufgabenzeilen** in der Spalte **WIP-Summe** angeben.  

 Die drei Optionen werden in der folgenden Tabelle beschrieben.  

|Feld|Description|  
|-------------------------------------|---------------------------------------|  
|**\<blank\>**|Lassen Sie dieses Feld leer, wenn die Projektaufgabe ein Teil einer Gruppe von Aufgaben ist.|  
|**Summe**|Definiert den Bereich oder die Gruppe von Aufgaben, die in der WIP- und Umsatzrealisierungsberechnung berücksichtigt sind. Innerhalb der Gruppe ist jede Projektaufgabe, deren **Projektaufgabenart** auf **Buchen** festgelegt ist, in der WIP-Summe enthalten, es sei denn, das Feld **WIP-Summe** ist auf **Ausschliesslich** festgelegt.|  
|**Ausschliesslich**|Gilt nur für eine Aufgabe der **Projektaufgabenart** **Buchen**. Die Aufgabe wird nicht einbezogen, wenn WIP und Umsatzrealisierung berechnet werden.|  

 In der folgenden exemplarischen Vorgehensweise wendet Tricia das Einstandswertverfahren, die Unternehmensnorm an, um die WIP zu berechnen. Katrin gibt an, welcher Teil des Projekts in die WIP-Berechnung einbezogen werden soll, indem Sie die WIP-Summenwerte den verschiedenen Projektaufgabenzeilen zuweist.  

### <a name="to-calculate-wip"></a>So berechnen Sie die WIP

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Projekt** ein und wählen Sie dann den zugehörigen Link aus.  
2. In der Liste **Projekte** wählen Sie das Projekt **Landsberg** aus, und wählen Sie die **Bearbeiten**-Aktion aus. Die Projektkarte wird im Bearbeitungsmodus geöffnet.  

     Die WIP kann basierend auf Einstandswert, Verkaufswert, Vertriebskosten, Prozentsatz der Fertigung oder bei Abschluss berechnet werden. In diesem Beispiel verwendet CRONUS das Einstandswertverfahren.  

3. Wählen Sie im Inforegister **Buchen** das Feld **WIP-Methode** und dann **Einstandswert** aus.  
4. Wählen Sie die Aktion **Projektaufgabenzeilen** aus, und legen Sie die folgenden Werte im Feld **WIP-Summe** fest.  

     Die Werte werden in der folgenden Tabelle beschrieben.  

    |Projektaufgabennr.|Feld "WIP-Summe"|  
    |------------------|----------------------|  
    |1130|Ausschliesslich|  
    |1190|Summe|  
    |1210|Ausschliesslich|  
    |1310|Ausschliesslich|  

5. Wählen Sie die **RIF** Aktion aus, und wählen Sie die **WIP berechnen** Aktion aus.  
6. Auf der Seite **WIP berechnen Projekt** wählen Sie ein Projekt aus, für das Sie den WIP berechnen möchten. Wählen Sie im Inforegister **Projekt** die Option **Landsberg** im Feld **Nr.** aus Feld  
7. Das **Buchungsdatum** liegt nach dem Arbeitsdatum. Bestätigen Sie, dass das Datum korrekt ist.
8. Geben Sie im Feld **Belegnr.** den Wert **1** ein. Dieses erstellt ein Dokument, das Sie später für die Verfolgbarkeit verwenden können.  
9. Wählen Sie die Schaltfläche **OK**, um den Batchauftrag zu starten. Eine Meldung wird angezeigt. Klicken Sie zum Fortfahren auf die Schaltfläche **OK**. Schliessen Sie die Seite **Projektaufgabenzeilen**.  

    > [!NOTE]  
    >  Die Benachrichtigung weist darauf hin, dass Warnungen im Zusammenhang mit der WIP-Berechnung vorliegen. Im folgenden Verfahren werden Sie die Warnungen überprüfen.  

10. Erweitern Sie auf der Seite **Projektkarte** das Inforegister **WIP und Umsatzrealisierung**, um die berechneten Werte anzuzeigen. Sie können auch das **WIP-Buchungsdatum** und die im Sachkonto gebuchten Werte anzeigen, soweit vorhanden.  

 Beachten Sie, dass der Wert für **Deaktivierter Einstandsbetrag** 215,60 in der Spalte **Zu buchen** ist. Dieses spiegelt die Gesamtkosten von zwei Artikeln in der Projektaufgabengruppe 1110 – 1130 wieder. Der dritte Artikel wurde auf **Ausschliesslich** gesetzt und ist daher nicht in die WIP-Berechnung einbezogen.  

### <a name="to-review-wip-warnings"></a>WIP-Warnungen überprüfen

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Projekt – WIP-Cockpit** ein, und wählen Sie dann den entsprechenden Link aus.  
2.  Wählen Sie das entsprechende Projekt **Landsberg** und dann die Aktion **Warnung anzeigen** aus.  
3.  Überprüfen Sie auf der Seite **Projekt-WIP-Warnungen** die Warnung, die dem Projekt zugeordnet ist.  

 Nach dem Ende der Buchhaltungsperiode muss Katrin die WIP erneut berechnen, um die bis zu diesem Zeitpunkt abgeschlossene Arbeit einzubeziehen.  

### <a name="to-recalculate-wip"></a>So berechnen Sie die WIP neu

1. Wählen Sie auf der Seite **Projektkarte** die Aktion **WIP-Posten** aus, um die WIP-Berechnung anzuzeigen.  

     Auf der Seite **WIP-Projektposten** werden die zuletzt für ein Projekt berechneten WIP-Posten angezeigt. Dies ist auch dann der Fall, wenn der WIP noch nicht auf das Fibukonto gebucht wurde.  

2. Sie können zur erneuten Berechnung von WIP den Schritten in dem Verfahren folgen, das erläutert, wie WIP berechnet wird. Bei jeder Berechnung der WIP wird ein Posten auf der Seite **WIP-Projektposten** erstellt.  
3. Schliessen Sie die Seite.  

> [!NOTE]  
> WIP und Anerkennung werden berechnet, jedoch nicht im Fibukonto gebucht. Führen Sie dazu den Stapelauftrag **WIP nach Sachkonten Projekt** aus, nachdem Sie die WIP und Umsatzrealisierung berechnet haben.

## <a name="posting-wip-to-general-ledger"></a>Den WIP auf das Sachkonto buchen

 Nachdem Katrin die WIP für dieses Projekt berechnet hat, kann sie sie auf die Finanzbuchhaltung buchen.  

### <a name="to-post-wip-to-general-ledger"></a>So buchen Sie die WIP auf das Sachkonto

1. Wählen Sie in der Liste **Projekte** das Projekt **Landsberg** aus.  
2. Wählen Sie die **RIF** Aktion aus, und wählen Sie die **WIP auf Sachkonto buchen** Aktion aus.  
3. Wählen Sie auf der Seite **WIP nach Sachkonten Projekt** auf dem Inforegister **Projekt** die Option **Landsberg** im Feld **Nr.** aus Feld  
4. Geben Sie auf dem Inforegister **Optionen** im Feld **Stornobelegnr.** den Wert **1** ein.  
5. Wählen Sie die Schaltfläche **OK**, um WIP auf den Fibuposten zu buchen.  
6. Klicken Sie auf **OK**, um die Bestätigungsseite zu schliessen.  

     Nachdem Sie die Buchung abgeschlossen haben, können Sie die Buchungsdaten auf der Seite **WIP-Fibuposten** anzeigen.  

7.  In der Liste **Projekte** wählen Sie das Projekt **Landsberg** und anschliessend die Aktion **WIP Fibukonto-Eintrag** aus.  

     Auf der Seite **WIP-Projekt-Fibuposten** stellen Sie sicher, dass die WIP auf das Fibukonto gebucht wurde.  

8. Schliessen Sie die Seite.  
9. Öffnen Sie die Seite **Projektkarte** für das Projekt **Landsberg**.  
10. Beachten Sie, dass im Inforegister **WIP und Umsatzrealisierung** in der Spalte **Gebucht** das Feld **Deaktivierter Einstandsbetrag auf Sachkonten** jetzt ausgefüllt ist, was angibt, dass diese WIP in der Finanzbuchhaltung erfolgreich gebucht wurde.  
11. Wählen Sie die Schaltfläche **OK**, um die Karte zu schliessen.  

## <a name="reversing-a-wip-posting"></a>Eine WIP-Buchung stornieren

 Katrin stellt fest, dass die Projektaufgaben, die aus der WIP-Berechnung ausgeschlossen wurden, in WIP berechnet worden sein sollten. Tricia kann die falschen Buchungen stornieren, ohne neue WIP-Posten buchen zu müssen.  

### <a name="to-reverse-a-wip-posting"></a>So stornieren Sie eine WIP-Buchung

1. Wählen Sie in der Liste **Projekte** das Projekt **Landsberg** aus.  
2. Wählen Sie die **RIF** Aktion aus, und wählen Sie die **WIP auf Sachkonto buchen** Aktion aus.  
3. Wählen Sie auf der Seite **WIP nach Sachkonten Projekt** auf dem Inforegister **Projekt** die Option **Landsberg** im Feld **Nr.** aus Feld  
4. Geben Sie auf dem Inforegister **Optionen** im Feld **Stornobelegnr.** den Wert **1** ein.  
5. Geben Sie in dem Feld **Stornobuchungsdatum** das ursprüngliche Buchungsdatum an. Dies sollte dasselbe Datum sein, das Sie für die erste Berechnung von WIP verwendet haben.  
6. Aktivieren Sie das Kontrollkästchen **Nur stornieren**. Dadurch wird der zuvor gebuchte WIP storniert, der neue WIP wird jedoch nicht auf das Sachkonto gebucht.  
7. Wählen Sie die Schaltfläche **OK**, um den Stapelauftrag auszuführen, und wählen Sie dann die Schaltfläche **OK**, um die Bestätigungsseite zu schliessen.  
8. Öffnen Sie die Seite **Projektkarte** für **Landsberg**.  
9. Überprüfen Sie im Inforegister **WIP und Umsatzrealisierung**, dass keine gebuchten WIP-Posten vorhanden sind.  
10. Schliessen Sie diese Seite.  
11. Wählen Sie in der Liste **Projekte** das Projekt **Landsberg**, wählen Sie die Aktion **WIP** und dann die Aktion **WIP Fibukonto-Eintrag** aus. In den WIP-Posten ist das Kontrollkästchen **Storniert** aktiviert.  
12. Schliessen Sie diese Seite.  
13. Öffnen Sie **Projektaufgabenzeilen** für das Projekt, schliessen Sie die in die WIP-Berechnung einzubeziehenden Teile des Projekts ein, und berechnen und buchen Sie dann den neuen Wert auf das Fibukonto.  

    > [!NOTE]  
    >  Gesetzt den Fall, Katrin hat WIP für ein Projekt mit falschen Datumsangaben berechnet und gebucht. Nach der zuvor erläuterten Methode kann Tricia die falschen Buchungen stornieren, die Datumsangaben korrigieren und erneut auf den Fibuposten buchen.  

## <a name="next-steps"></a>Nächste Schritte

 In dieser exemplarischen Vorgehensweise wurden die Schritte zum Berechnen der unfertigen Arbeit (WIP) in [!INCLUDE[prod_short](includes/prod_short.md)] erläutert. Bei grösseren Projekten kann es hilfreich sein, die Kosten periodisch in ein WIP-Konto zu übertragen, während das Projekt fertig gestellt wird. In dieser exemplarischen Vorgehensweise wurde gezeigt, wie Sie Aufgabenzeilen von einer Berechnung ausschliessen. Zudem wurden Fälle vorgestellt, in denen eine Neuberechnung erforderlich ist. Die und zum Schluss, zeigt dieser exemplarischen Vorgehensweise, wie die WIP auf das Sachkonto gebucht wird. Ein Beispiel zum Stornieren einer WIP-Buchung in der Finanzbuchhaltung wurde ebenfalls berücksichtigt.  

## <a name="see-also"></a>Siehe auch

 [Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  
 [Exemplarische Vorgehensweise: Verwalten von Projekten](walkthrough-managing-projects-with-jobs.md)  
 [Verständnis - WIP-Methoden](projects-understanding-wip.md)  
 [Überwachen von Status und Leistung](projects-how-monitor-progress-performance.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
