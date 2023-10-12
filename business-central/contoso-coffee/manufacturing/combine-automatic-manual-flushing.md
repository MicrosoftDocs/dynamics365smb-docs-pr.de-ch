---
title: Automatisches und manuelles Buchen kombinieren
description: 'Exemplarische Vorgehensweise für einen Produktionsplaner bei Contoso Coffee, der automatisches und manuelles Buchen kombinieren möchte.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Vorgehensweise: Automatisches und manuelles Buchen kombinieren

In diesem Artikel führen wir Sie durch die Schritte zur Verwendung der Demodaten von Contoso Coffee beim Buchen.  

## Szenario

Sie sind der Produktionsplaner bei Contoso Coffee. Sie müssen einen neuen Produktionsauftrag für zehn Einheiten des Artikels SP-SCM1004, AutoDrip erstellen. Einige Komponenten und Vorgänge werden basierend auf unterschiedlichen Bedingungen mit der Methode „Vorwärts“, andere mit der Methode „Rückwärts“ gebucht.

## Schritte

> [Note!] Denken Sie daran, den Bestand zu bereinigen, indem Sie Artikel Erf.-Journale mit Erfassungen der Anfangssalden buchen.

1. Erstellen Sie einen fest geplanten Fertigungsauftrag für fünf Einheiten des Artikels **SP-SCM1004, AutoDrip** am Standort *MAIN*. Eine Anleitung finden Sie unter [Vorgehensweise: Neuen fest geplanten Fertigungsauftrag erstellen und ändern](create-firm-planned-production-order-change.md).  

2. Geben Sie den Fertigungsauftrag frei.

    1. Wählen Sie die Aktion **Status ändern** aus.  

    2. Legen Sie auf der angezeigten Seite das Feld **Neuer Status** auf *Freigegeben* fest, und wählen Sie dann die Schaltfläche **Ja** aus.  

        Es wird eine Meldung mit einer Statusleiste angezeigt, die auf den automatischen Verbrauch hinweist. Auf diese folgt eine Bestätigungsmeldung, dass der Auftrag geändert in den Status *Freigegeben* geändert wird.  

    3. Wählen Sie die Schaltfläche **OK** aus, um die Bestätigungsmeldung zu schliessen.

3. Überprüfen Sie die Artikel- und Kapazitätsposten für den Produktionsauftrag.

    1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Freigegebener Fertigungsauftrag** ein, und wählen Sie dann den zugehörigen Link.  

    2. Öffnen Sie den Produktionsauftrag mit den 5 Einheiten der AutoDrip-Kaffeemaschine.  

    3. Wählen Sie die Aktion **Lagerposten** aus.  

        Der Artikel **SP-BOM1305 Schraube Hex M3, Zink** wird sofort mit der gesamten erwarteten Menge gebucht. Schliessen Sie die Seite **Lagerposten**.  

    4. Wählen Sie die Aktion **Kapazitätsposten** aus.  Beachten Sie, dass zum Zeitpunkt der Auftragsfreigabe auch ein Eintrag für Karosseriemontagevorgänge abgeschlossen wurde. Wählen Sie das Fenster **Kapazitätsposten** aus.

    Sie können Komponentenartikel mithilfe des FA-Verb. Erf.- oder Produktions Erf.-Journals manuell buchen. Mit der manuellen Buchung können Sie die Menge vor dem Buchen anpassen. Wenn beispielsweise zusätzliche Mengen benötigt werden, um Rohstoffe mit geringer Qualität abzudecken.
4. Buchen Sie Komponenten manuell.  
    1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Verbrauchs Erf.-Journal** ein, und wählen Sie dann den zugehörigen Link.  

    2. Wählen Sie die Aktion **Verbrauch berechnen** aus.  

    3. Definieren Sie auf Anforderungsseite **Verbrauch berechnen**, im Inforegister **Produktionsauftrag** FastTab, einen Filter für den spezifischen Auftrag im Feld **Auftragsnr.** , und wählen Sie dann die Schaltfläche **OK** aus. Nachdem die Anforderungsseite für die Stapelverarbeitung geschlossen wurde, wird die Seite **FA-Verb. Erf.-Journal** mit den Komponenten gefüllt, die manuell verbraucht werden müssen.

    4. Wählen Sie die Aktion **Buchen** aus. Schliessen Sie das FA-Verb. Erf.-Journal.

5. Registrieren Sie die Ausgabe für die elektrische Verkabelung manuell.  

    Sie müssen die Felder **Rüstzeit** und **Bearbeitungszeit** ausfüllen. Sie können auch die tatsächlich produzierte Menge und den Ausschuss angeben. Geben Sie *3* als fertig gestellte Menge ein, und buchen Sie die Ausgabe.

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Erfassung Erf.-Journal** ein und wählen Sie dann den zugehörigen Link.  

    2. Erstellen Sie eine neue Erfassungsjournalzeile auf der Seite **Ausgabejournal**.  

    3. Geben Sie im Feld **Auftragsnr.** den Auftrag ein.  

    4. Wählen Sie die Aktion **Arbeitsplan auflösen** aus.  

        Die Seite **Erfassungsjournalzeile** wird nur für die elektrische Verkabelung mit der Arbeitsgangzeile gefüllt.

    5. Legen Sie das Feld **Bearbeitungszeit** auf *10* fest.  

    6. Ändern Sie das Feld **Menge** in *5* bis *3* fest.

    7. Wählen Sie **Buchen** aus.  
    8. Schliessen Sie das FA-Istmeldungs Erf.-Journal.

6. Überprüfen Sie die Lagerposten für den Produktionsauftrag.

    1. Wählen Sie auf der Seite für den Fertigungsauftrag die Aktion **Lagerposten** aus.  

    Der Artikel **SP-BOM1302, Bedienfeldanzeige** wird, basierend auf der Isteffektivität, mit der Menge *3* gebucht, während **SP-BOM1303, Knopf** mit der gesamten erwarteten Menge gebucht wird. Schliessen Sie die Seite **Lagerposten**.

7. Beenden Sie den Fertigungsauftrag.  

    1. Wählen Sie die Aktion **Status ändern** aus.
    2. Legen Sie auf der angezeigten Seite das Feld **Neuer Status** auf *Beendet* fest, und wählen Sie dann die Schaltfläche **Ja** aus.  

        Es wird eine Meldung mit einer Statusleiste angezeigt, die den automatischen Verbrauch widerspiegelt. Auf diese folgt eine Bestätigungsmeldung, dass der Auftrag geändert in einen Auftrag mit dem Status *Beendet* geändert wird. Der beendete Fertigungsauftrag hat dieselbe Nummer wie im Status *Freigegeben*.
    3. Wählen Sie die Schaltfläche **OK** aus, um die Bestätigungsmeldung zu schliessen.

8. Überprüfen Sie die Artikel- und Kapazitätsposten für den Produktionsauftrag erneut.

    1. Wählen Sie die Aktion **Kapazitätsposten** aus.  

        Der Eintrag für Verpackungsvorgänge wurde im Moment der Auftragsfreigabe abgeschlossen. Die produzierte (Ausgabe-)Menge ist *5*, unabhängig von der Ausgabe des vorherigen Schritts. Schliessen Sie die Seite **Kapazitätsposten**.

    2. Wählen Sie die Aktion **Lagerposten** aus.  

        Die Menge im Lagerposten vom Typ *Ausgabe* ist gleich der fertig gestellten Menge im Kapazitätsposten. Die verbrauchte Menge von **SP-BOM1301, Gehäuse AutoDrip**, und **SP-BOM1304, Thermoskanne aus Edelstahl** ist für beide 5, da die erwartete Ausgabe und die tatsächliche Ausgabe identisch sind. 

    3. Schliessen Sie die Seite **Lagerposten**.  

Das war's zum Thema manuelles und automatisches Buchen von Komponenten.

## Siehe auch

[Komponenten nach Vorgangsausgabe buchen](../../production-how-to-flush-components-according-to-operation-output.md)  
[Einführung in Contoso Coffee Demo Data](contoso-coffee-manufacturing-intro.md)  
