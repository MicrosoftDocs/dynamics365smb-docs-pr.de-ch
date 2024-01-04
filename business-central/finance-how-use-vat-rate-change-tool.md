---
title: Verwalten von Änderungen des MWST-Satzes
description: 'Erfahren Sie, wie Sie das Tool zur Änderung des MWST-Satzes für Dynamics 365 Business Central verwenden, um die MWST-Sätze auf der Grundlage der lokalen Gesetzgebung zu ändern.'
author: andregu
ms.topic: conceptual
ms.reviewer: bholtorf
ms.workload: na
ms.search.keywords: 'VAT, VAT rate, posting, tax, value-added tax'
ms.search.form: '550,'
ms.date: 06/16/2021
ms.author: andregu
---

# Verwalten von Änderungen des Mehrwertsteuersatzes

Mehrwertsteuersätze können sich je nach lokaler Gesetzgebung ändern. Jede Änderung der Mehrwertsteuer wirkt sich auf Ihre Daten in [!INCLUDE[prod_short](includes/prod_short.md)] aus, unabhängig davon, ob der Mehrwertsteuersatz gesenkt, angehoben oder entfernt wird. Die Mehrwertsteuer ist mit vielen Entitäten in [!INCLUDE[prod_short](includes/prod_short.md)] verbunden, z. B. Kunden, Lieferanten, Artikel, Ressourcen, Artikel Zu-/Abschläge und Fibukonten. Änderungen der Mehrwertsteuersätze erfolgen normalerweise zu einem bestimmten Zeitpunkt. Ab diesem Zeitpunkt müssen Sie die MWST-Einrichtung und Buchungsgruppen usw. geändert haben, um sicherzustellen, dass neue Verkaufsaufträge und Einkaufsbestellungen mit dem neuen Mehrwertsteuersatz erstellt werden.

## Ändern von Mehrwertsteuersätzen

Der optimale Ansatz für die Verwaltung einer Änderung des Mehrwertsteuersatzes besteht darin, offene Bestellungen und andere Belege vor dem Datum der Änderung des Mehrwertsteuersatzes vollständig zu buchen und zu schliessen, um sicherzustellen, dass diese nicht von der Änderung betroffen sind. Dies ist die sauberste Vorgehensweise, die es Ihnen ermöglicht, neue Bestellungen und Belege mit dem neuen Mehrwertsteuersatz zu starten.

Die folgende Methode wird vorgeschlagen, um eine Änderung des Mehrwertsteuersatzes zu verwalten.

1. Buchen und schliessen Sie offene Aufträge, Erfassungsjournale und andere Belege vor dem Umstellungsdatum vollständig. Sie können bis nach dem Umstellungsdatum warten, solange Sie keine neuen Zeilen hinzufügen und sicherstellen, dass das Gültigkeitsdatum vor dem Umstellungsdatum liegt.  
2. Erstellen Sie die neue MwSt-Einrichtung.  
3. Nehmen Sie die MwSt-Umstellung für Entitäten vor (relevante Debitoren, Kreditoren, Artikel usw.).  
4. Am Umstellungsdatum des Mehrwertsteuersatzes erstellen Sie neue Belege, die den neuen Satz verwenden.  


> [!NOTE]  
> Das Tool zum Ändern des MWST-Satzes wird derzeit aktualisiert. Die nachfolgend aufgeführten Funktionen stimmen möglicherweise nicht mit den Funktionen in Ihrer Umgebung überein. Das Update wird vor dem 1. Juli 2020 ausgeführt und ist kein regelmässiges monatliches Update. Stattdessen werden alle Umgebungen automatisch aktualisiert (Hotfix). Wenn dieses Update abgeschlossen ist, wird diese Meldung nicht mehr angezeigt.  

## Das Tool zum Ändern des MWST-Satzes

Das Tool zum Ändern des MWST-Satzes kann die Umrechnung von Mehrwertsteuersätzen für Masterdaten, Erfassungsjournale und Bestellungen in gewissem Umfang unterstützen. Dies ist nützlich, wenn Sie die Mehrwertsteuer für Masterdaten einfacher umrechnen möchten oder Sie über Aufträge verfügen, die Sie nicht vor dem Umstellungsdatum schliessen können und die über einen längeren Zeitraum bearbeitet werden und das Umstellungsdatum des Mehrwertsteuersatzes überschreiten. Das angewendete Tool zum Ändern des MWST-Satzes unterliegt bestimmten Einschränkungen und Einschränkungen.

## Verstehen des Prozesses und der Einschränkungen des Tools zum Ändern des MWST-Satzes

Das Tool zum Ändern des MWST-Satzes führt Mehrwertsteuersatzkonvertierungen für Masterdaten, Erfassungsjournale und Aufträge auf verschiedene Arten aus. Die ausgewählten Masterdaten und die Erfassungsjournale werden von der neuen Produktbuchungsgruppe oder der MWST.-Produktbuchungsgruppe aktualisiert. Wenn eine Bestellung vollständig oder teilweise geliefert wurde, behalten die gelieferten Artikel die aktuelle Produktbuchungsgruppe oder MWST.-Produktbuchungsgruppe. Eine neue Auftragszeile wird für die nicht gelieferten Artikel erstellt und aktualisiert, um aktuelle und neue Produktbuchungsgruppen oder MWST.-Produktbuchungsgruppen aufeinander auszurichten. Darüber hinaus werden Artikelzu-/-abschlagszuweisungen, Konfigurationsvorlagen für Artikel, Reservierungen und Artikeltrackinginformationen entsprechend aktualisiert. 

In Auftragspositionen wird der VK-Preis für alle Zeilen des Typs „Artikel“ und „Ressource“ aktualisiert, wenn Preise inkl. Mehrwertsteuer für den Artikel verwendet werden. Bei anderen Positionstypen kann entschieden werden, ob der VK-Preis aktualisiert werden soll oder nicht.

Es gibt mehrere Elemente, die das Werkzeug nicht konvertiert:

* Verkaufs- oder Einkaufsbestellungen und -rechnungen, in denen Lieferungen gebucht wurden. Diese Belege werden unter Verwendung des aktuellen Mehrwertsteuersatzes gebucht.  
* Belege mit gebuchten Vorauszahlungsrechnungen. Beispielsweise haben Sie Vorauszahlungen auf Rechnungen geleistet oder erhalten, die nicht vollständig erledigt sind, bevor Sie das Mehrwertsteuersatz-Änderungstool verwenden. In diesem Fall gibt es eine Differenz zwischen der MWST., die fällig ist, und der MWST., die in den Vorauszahlungen bezahlt wurde, wenn die Rechnung abgeschlossen wird. Das Mehrwertsteuersatz-Änderungstool überspringt diese Belege, und Sie müssen sie manuell aktualisieren.  
* Verkaufs- oder Einkaufsbestellungen mit Lagerintegration, wenn sie teilweise geliefert oder erhalten werden.  
* Direktlieferungen
* Spezialaufträge 
* Montageaufträge
* Serviceverträge.  
* Gutschriften
* Reklamationen
* Preise für Artikel (Masterdaten)
* Preise für Verkaufspreise (Masterdaten)
* Geschäftsbuchungsgruppen für Debitoren und Kreditoren

### So bereiten Sie Mehrwertsteuersatzänderungen vor

Bevor Sie das Mehrwertsteuersatz-Änderungstool einrichten, müssen Sie die folgenden Vorbereitungen durchführen.

* Wenn Sie Transaktionen haben, die verschiedene Sätze verwenden, müssen sie in verschiedene Gruppen aufgeteilt werden, entweder durch Erstellen neuer Fibukonten für die einzelnen Sätze oder mithilfe von Datenfiltern, um Transaktionen entsprechend dem Satz zu gruppieren.  
* Wenn Sie neue Fibukonten erstellen, müssen Sie auch neue allgemeine Buchungsgruppen erstellen.  
* Um die Anzahl der Belege zu verringern, die konvertiert werden, buchen Sie möglichst viele Belege, und reduzieren Sie nicht gebuchte Belege auf ein Minimum.  
* Sichern von Daten.

### So richten Sie das Mehrwertsteuersatz-Änderungstool ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Einrichtung der MWST-Satzänderung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf den Inforegistern **Masterdaten**, **Buch.-Erfassungsjournale** und **Belege** einen Buchungsgruppenwert aus der Liste der Optionen für erforderliche Felder aus. Für jede Gruppe können Sie wählen, ob Sie MWST-Produktbuchungsgruppen oder allgemeine Produktbuchungsgruppen konvertieren oder beide Werte konvertieren möchten, sofern sie im Masterdatenelement verfügbar sind. Für einige Regionen können Sie auch einen Filter festlegen, um nur eine Teilmenge von Werten zu konvertieren, z. B. Fibukonten. 
3. Wählen Sie auf dem Inforegister **Preise inkl. MwSt** aus, für welche Zeilenarten in Bestellungen Sie VK-Preise aktualisieren möchten. VK-Preise in Zeilen vom Typ „Artikel“ und „Ressource“ werden immer aktualisiert.

### So richten Sie die Produktbuchungsgruppenkonvertierung ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Einrichtung der MWST-Satzänderung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Einrichtung der MWST-Satzänderung** entweder die Option **Umrech. für MWST-Produktbuchungsgruppe** oder **Umrech. für Produktbuchungsgruppe** Aktion.  
3. Geben Sie im Feld **Code ab** die aktuelle Buchungsgruppe ein.  
4. Geben Sie den neuen Standort in dem Feld **Cod zu** ein.  

### So führen Sie eine Umrechnung für die MWST.-Satzänderung aus

Sie verwenden das MwSt.-Satz-Änderungstool, um Änderungen im Standard-MwSt.-Satz zu verwalten. Sie führen MwSt.- und Buchungsgruppenkonvertierungen durch, um Mehrwertsteuersätze zu ändern und für präzise MwSt.-Berichte zu sorgen. Abhängig von Ihrem Setup werden folgende Änderungen vorgenommen:  

* MWST.-Buchungsgruppen und Buchungsgruppen werden konvertiert.  
* Änderungen werden in den Fibuposten, den Debitoren, den Kreditoren, den offenen Belegen, den Erfassungsjournalzeilen usw. implementiert.  

> [!IMPORTANT]  
> Bevor Sie die Umrechnung für MWST-Satzänderungen ausführen, können Sie die Konvertierung testen. Um dies zu tun, führen Sie die Schritte unten aus, stellen Sie aber sicher, dass Sie die Kontrollkästchen **Konvertierung durchführen** und **Tool zum Ändern des MWST-Satzes abgeschlossen** deaktivieren. Während der Testkonvertierung wird das Feld **Konvertiert** in der Tabelle **Protokollposten für MWST-Satzänderung** gelöscht und das Feld **Konvertierungsdatum** in der Tabelle **Protokollposten für MWST-Satzänderung** ist leer. Nach der Umrechnung wählen Sie auf der Registerkarte Start, in der Gruppe Prozess die Option **Änderungsprotokollposten für MWST-Satz** aus, um die Ergebnisse der Umrechnung anzuzeigen. Prüfen Sie jeden Posten, bevor Sie die Umrechnung ausführen. Insbesondere überprüfen Sie Transaktionen, die einen alten MWST-Satz verwenden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **MWST-Satz-Änderung** ein und wählen Sie dann den Link **Einrichtung der MWST-Satzänderung**.  
2. Vergewissern Sie sich, dass Sie bereits die MWST.-Produktbuchungsgruppen-Umrechnung oder die Produktbuchungsgruppen-Umrechnung eingerichtet haben.  
3. Wählen Sie das Kontrollkästchen **Konvertierung durchführen**.  

    > [!IMPORTANT]  
    >  Deaktivieren Sie das Kontrollkästchen **Tool zum Ändern des MWST-Satzes abgeschlossen**. Das Kontrollkästchen wird automatisch aktiviert, wenn die Umrechnung für die MWST.-Satzänderung abgeschlossen ist.  

4. Wählen Sie die Aktion **Konvertieren** aus.  
5. Nachdem die Konvertierung abgeschlossen ist, wählen Sie die Aktion **Änderungsprotokollposten für MWST-Satz**, um die Ergebnisse der Konvertierung anzuzeigen.  

> [!IMPORTANT]  
> Nachdem die Umrechnung abgeschlossen ist, wird das Feld **Konvertiert** in der Tabelle **Protokollposten für MWST-Satzänderung** ausgewählt und das Feld **Konvertierungsdatum** in der Tabelle **Protokollposten für MWST-Satzänderung** wird mit dem Umrechnungsdatum ausgefüllt.  

## Siehe auch 

[MWST einrichten](finance-setup-vat.md)  
[Einrichten von unrealisierter Mehrwertsteuer](finance-setup-unrealized-vat.md)  
[MWST an die Steuerbehörde melden](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Lokale Funktion in Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
