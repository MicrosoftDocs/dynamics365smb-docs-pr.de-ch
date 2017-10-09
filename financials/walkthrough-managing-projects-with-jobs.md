---
title: 'Exemplarische Vorgehensweise: Verwalten von Projekten | Microsoft Docs'
description: "In dieser exemplarischen Vorgehensweise erhalten Sie eine Einführung in die Projektmanagementfunktionen in \"Projekte\". Mit Projekten können Sie den Verbrauch der Ressourcen Ihres Unternehmens planen und die verschiedenen Kosten im Zusammenhang mit dem Einsatz von Ressourcen für ein bestimmtes Projekt verfolgen. Projekte beinhalten den Verbrauch von Mitarbeiterstunden, Maschinenstunden, Bestandsposten und andere Verbrauchsarten, die während des Projekts verfolgt werden können."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b6a61a9c5d2b8c7b3d197780c580c8bcf957560e
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-managing-projects-with-jobs"></a>Exemplarische Vorgehensweise: Verwalten von Projekten
In dieser exemplarischen Vorgehensweise erhalten Sie eine Einführung in die Projektmanagementfunktionen in "Projekte". Mit Projekten können Sie den Verbrauch der Ressourcen Ihres Unternehmens planen und die verschiedenen Kosten im Zusammenhang mit dem Einsatz von Ressourcen für ein bestimmtes Projekt verfolgen. Projekte beinhalten den Verbrauch von Mitarbeiterstunden, Maschinenstunden, Bestandsposten und andere Verbrauchsarten, die während des Projekts verfolgt werden können.  

 In dieser exemplarischen Vorgehensweise werden die Einrichtung eines neuen Projekts sowie einige allgemeine Aufgaben wie das Verwenden von Festpreisen, Anwenden von Teilzahlungen, Buchen von Projektrechnungen und Kopieren von Projekten erläutert.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise  
 In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

### <a name="setting-up-a-job"></a>Einrichten eines Projekts  
 Wenn die Budgetstruktur für Projekte eingerichtet ist, ist ein Projekt einfach zu erstellen. Diese exemplarische Vorgehensweise umfasst folgende Verfahren:  

-   Einrichten von Projektaufgabenzeilen und Planungszeilen  
-   Erstellen projektspezifischer Preise für Artikel, Ressourcen und Sachkonten  
-   Fakturieren eines Projekts  

### <a name="handling-fixed-prices"></a>Verwenden von Festpreisen  
 In Projekten können Festpreise und die vorab mit Kunden vereinbarten Preise für Services oder Waren verwendet werden. In dieser exemplarischen Vorgehensweise können Sie Folgendes durchführen:  

-   Erfahren Sie, wie Vertrags- und Rechnungswerte ermittelt werden.  
-   Einplanen zusätzlicher, nicht fakturierter Arbeit im Plan  

### <a name="copying-a-job"></a>Kopieren eines Projekts  
 In diesem Teil der exemplarischen Vorgehensweise wird gezeigt, wie Sie ein Projekt ganz oder teilweise kopieren, um den manuellen Dateneingabeaufwand zu reduzieren und die Genauigkeit zu verbessern. Dazu zählen folgende Aufgaben:  

-   Kopieren eines Projektteils in ein neues Projekt  
-   Kopieren projektspezifischer Preise  
-   Kopieren von Planungszeilen  

### <a name="making-payment-by-installment"></a>Anwenden von Teilzahlungen  
 Wenn ein grosses, kostspieliges Projekt über einen langen Zeitraum läuft, schliesst der Kunde häufig mit dem Unternehmen eine Teilzahlungsvereinbarung ab. In diesem Szenario wird gezeigt, wie Sie Teilzahlungen und Versicherungen einrichten:  

-   Erstellen von Teilzahlungen für ein Projekt  
-   Fakturieren von Teilzahlungen  
-   Abrechnen des Verbrauchs in einem Projekt, das für Teilzahlungen eingerichtet ist.  

## <a name="roles"></a>Rollen  
 Diese exemplarische Vorgehensweise umfasst Aufgaben für folgende Rollen:  

-   Projekt-Manager  
-   Projektteammitglied  

## <a name="prerequisites"></a>Voraussetzungen  
 Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

-   Installieren Sie die Demodatenbank "CRONUS AG".
-   Erstellen Sie wie im folgenden Abschnitt beschrieben einige Beispieldaten.  

## <a name="story"></a>Hintergrund  
Diese exemplarische Vorgehensweise in CRONUS Internationl Ltd, ein Design- und Beratungsunternehmen, das neue Infrastrukturen anpasst, wie Konferenzräume mit Möblen, Zubehör und Lagereinheiten. Der Grossteil der Arbeiten ist projektorientierter Natur. Prakash ist Projekt-Manager bei Cronus. Er verwendet das Projektmodul, da er sich damit einen Überblick über die einzelnen laufenden Projekte verschaffen kann, die CRONUS gestartet hat, wie auch über die abgeschlossenen Projekte. In der Regel ist er es, der die Geschäfte mit Debitoren einrichtet und die Kerndaten des Projekts, d.h. Aufgaben- und Planungszeilen sowie Preise, in [!INCLUDE[d365fin](includes/d365fin_md.md)] erfasst. Er findet, dass erstellen, verwalten, und Informationen prüfen einfach ist. Auch ist Bernhard schätzt die Art, wie [!INCLUDE[d365fin](includes/d365fin_md.md)] das Kopieren von Projekten sowie von Teilzahlungen ausführt.

 Katrin, ein Projektteammitglied, das Bernard unterstellt ist, ist für die tägliche Überwachung des Projekts zuständig. Sie gibt ihre eigene Arbeit zusätzlich zu der Arbeit ein, die von Technikern für jede Aufgabe ausgeführt wird. Sie speichert die Artikel, die sie verwendet haben und die Kosten, die sie verursacht haben.  

## <a name="preparing-sample-data"></a>Vorbereiten der Beispieldaten  
 Um sich für diese exemplarische Vorgehensweise vorzubereiten, müssen Sie Katrin als neue Ressource hinzufügen.  

### <a name="to-prepare-the-sample-data"></a>So bereiten Sie die Beispieldaten vor  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Ressourcen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die **Neu** Aktion aus, um eine neue Ressourcenkarte zu erstellen.  
3.  Geben Sie auf dem Inforegister **Allgemein** die folgenden Informationen ein:  

    - **Nr.**: **Katrin**  
    - **Name**: **Katrin**  
    - **Art**: **Person**  

4.  Wählen Sie im Feld **Basiseinheitencode** die Option **Neu**, um das Fenster **Ressourceneinheit** zu öffnen. Wählen Sie im Feld **Code** die Option **Stunde** aus. Wählen Sie die Schaltfläche **OK** aus.  
5.  Geben Sie auf dem Inforegister **Fakturierung** die folgenden Informationen ein:  

    -   **EK-Preis**: **5**  
    -   **Kosten %**: **4**  
    -   **Einstandspreis**: **10**  
    -   **Produktbuchungsgruppe**: **Services**  
    -   **MWST.-Produktbuchungsgruppe**: **MWST16**  

6.  Klicken Sie auf die Schaltfläche **OK**, um die Änderungen zu speichern.  

 Im folgenden Verfahren erstellen Sie eine Projektbuchungsblatt für Katrin, um deren Verbrauch zu buchen.  

### <a name="to-create-a-job-journal-batch"></a>So erstellen Sie einen Projekt Erfassungsjournalnamen  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen]Symbol (media/ui-search/search_small.png "")Nach Seite oder Bericht suchen und geben **Projektbuch** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie im Fenster **Projekt Erfassungsjournal** das Feld **Erfassungsjournalname** aus. Das Fenster **Projekt Erfassungsjournalnamen** wird geöffnet.  
3.  Wählen Sie auf der Registerkarte Start die Option **Neu** aus, um eine neue Zeile mit folgender Information zu erstellen.  

    -   **Name**: **Katrin**  
    -   **Beschreibung**: **Katrin**  
    -   **Nummernserie**: **PRJ-BCHBL**  

4.  Wählen Sie die Schaltfläche **OK**, um alle geöffneten Fenster zu schliessen.  

## <a name="setting-up-a-job"></a>Einrichten eines Projekts  
 In diesem Szenario hat CRONUS einen Vertrag mit einem Kunden, Progressive Home Furnishings, für den Entwurf eines Konferenz- und Speisesaals abgeschlossen. Der Kunde hat seinen Sitz in den USA, und für das Projekt ist spezielle Software erforderlich. Der Projektmanager trifft eine Vereinbarung mit dem Kunden und erstellt ein Projekt für den Vertrag.  

### <a name="to-set-up-a-job"></a>So richten Sie ein Projekt ein  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die **Neu** Aktion aus, um eine neue Ressourcenkarte zu erstellen.  
3.  Geben Sie auf dem Inforegister **Allgemein** die folgenden Informationen ein:  

    -   **Beschreibung**: **Beratung zur Einrichtung des Konferenzraums**  
    -   **Rech. an Deb.-Nr.**: **01445544**  

4.  Geben Sie auf dem Inforegister **Buchung** die folgenden Informationen ein:  

    -   **Status**: **Bestellung**  
    -   **Projektbuchungsgruppe**: **Einrichten**  
    -   **WIP-Methode**: **Einstandswert**  

5.  Geben Sie auf dem Inforegister **Dauer** das heutige Datum in die Felder **Startdatum** und **Enddatum** ein. Diese Datumsangaben werden bei der Fakturierung des Projekts zur Währungsumrechnung verwendet.  
6.  Stellen Sie auf dem Inforegister **Aussenhandel** sicher, dass der Währungscode auf **USD** festgelegt ist. Wenn Sie im Feld **Währungscode Rechnung** die Option "USD" auswählen, wird das Projekt in US-Doller fakturiert und nur in der lokalen Währung von Cronus geplant.  

 Sie können die Preise für Debitoren auf Pro-Projekt-Basis je nach den getroffenen Vereinbarungen anpassen. Im folgenden Verfahren gibt der Projekt-Manager Kosten für Katrins Zeit an, setzt den Preis für die benötigte Software fest und fügt in den Reisekosten hinzu, dass der Debitor zugestimmt hat, zu zahlen.  

### <a name="to-customize-pricing"></a>Preise anpassen  

1.  Von der Projektkarte wählen Sie die **Ressource** Aktion aus.  
2.  Geben Sie im Fenster **Res.-VK-Preise Projekt** die folgenden Informationen ein:  

    -   **Code**: **Katrin**  
    -   **VK-Preis**: **20**  

3.  Wählen Sie die Schaltfläche **OK**, um das Fenster zu schliessen.  
4.  Wählen Sie die Aktion **Artikel** aus.  
5.  Geben Sie im Fenster **Projektartikelpreise** die folgenden Informationen und den folgenden angepassten Preis ein:  

    1.  **Artikelnr.**: **80201 (Grafikprogramm)**  
    2.  **VK-Preis**: **200**  

6.  Wählen Sie die Schaltfläche **OK**, um das Fenster zu schließen.  
7.  Wählen Sie die **Fibukonto** Aktion aus.  
8.  Geben Sie im Fenster **Projekt-Fibukontopreise** die folgenden Werte sowie die Reisekosten ein, für die Sie mit dem Debitor vereinbart haben, dass er sie zuzüglich 25 % übernimmt.  

    1.  **Fibukonto**: **8430 (Reisekosten)**  
    2.  **Einstandspreis**: **1,25**  

9. Wählen Sie die Schaltfläche **OK**, um das Fenster zu schliessen.  

 Die letzten Schritte beim Einrichten eines Projekts bestehen darin, die Projektaufgaben und die Planungszeilen hinzufügen, die Teil jedes Projekts sind. Die Planungszeilen bestimmen, welche Posten dem Kunden in Rechnung gestellt werden.  

### <a name="to-add-job-tasks"></a>So fügen Sie Projektaufgaben hinzu  

1.  Auf der Karte **Projekt** für das neue Projekt, wählen Sie die **Projektaufgabenzeilen** Aktion aus.  
2.  In der folgenden Tabelle werden die Informationen beschrieben, die Sie in die Felder eingeben müssen.  

    |Projektaufgabennr.|Description|Projektaufgabenart|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Beratung zur Einrichtung des Raums|Von-Summe|  
    |1010|Beratungsgespräch mit dem Kunden|Buchen|  
    |1020|Entwicklung|Buchen|  
    |1090|Beratung insgesamt|Bis-Summe|  

3.  Um zu zeigen, dass einige Aufgaben Unterkategorien anderer Aufgaben sind, wählen Sie auf der Registerkarte **Aktionen** in der Gruppe **Funktion** die Option **Projektaufgaben einrücken**.  

 Eine Planungszeile kann von einer der folgenden Arten sein:  

-   **Plan**: Dem Plan hinzugefügt, aber noch nicht fakturiert.  
-   **Vertrag**: Fakturiert, aber nicht dem Plan hinzugefügt.  
-   **Plan und Vertrag**: Fakturiert und dem Plan hinzugefügt.  

 In dieser exemplarischen Vorgehensweise verwendet der Projektmanager **Plan und Vertrag**. Er erstellt drei Planungszeilen für die Aufgabe 1010 und zwei Planungszeilen für die Aufgabe 1020.  

### <a name="to-create-planning-lines"></a>So erstellen Sie Planungszeilen  

1.  Wählen Sie die Zeile 1010 und wählen Sie dann die Aktion **Projektplanzeilen** aus. Geben Sie die folgenden Informationen ein:  

     **Zeile 1**  

    -   **Zeilenart**: **Plan und Vertrag**  
    -   **Planungsdatum**: **(heutiges Datum)**  
    -   **Art**: **Ressource**  
    -   **Nr.**: **Katrin**  
    -   **Menge**: **40**  

     **Zeile 2**  

    -   **Zeilenart**: **Plan und Vertrag**  
    -   **Planungsdatum**: **(heutiges Datum)**  
    -   **Art**: **Ressource**  
    -   **Nr.**: **Thorsten**  
    -   **Menge**: **40**  

     **Zeile 3**  

    -   **Zeilenart**: **Plan und Vertrag**  
    -   **Planungsdatum**: **(heutiges Datum)**  
    -   **Art**: **Fibukonto**  
    -   **Nr.**: **8430 (Reise)**  
    -   **Menge**: **2**  
    -   **Einstandspreis**: **400**  

2.  Wählen Sie die Schaltfläche **OK**, um das Fenster zu schliessen. Die Summen werden im Fenster **Projektaufgabenzeilen** aktualisiert.  
3.  Wählen Sie die Zeile 1020 und wählen Sie dann die Aktion **Projektplanzeilen** aus. Geben Sie die folgenden Informationen ein:  

     **Zeile 1**  

    -   **Zeilenart**: **Plan und Vertrag**  
    -   **Planungsdatum**: **(heutiges Datum)**  
    -   **Art**: **Ressource**  
    -   **Nr.**: **Katrin**  
    -   **Menge**: **80**  

     **Zeile 2**  

    -   **Zeilenart**: **Plan und Vertrag**  
    -   **Planungsdatum**: **(heutiges Datum)**  
    -   **Art**: **Artikel**  
    -   **Nr.**: **80201 (Grafikprogramm)**  
    -   **Menge**: **1**  

4.  Wählen Sie die Schaltfläche **OK**, um das Fenster zu schliessen. Die Summen werden im Fenster **Projektaufgabenzeilen** aktualisiert.  

## <a name="calculating-remaining-usage"></a>Berechnen des Restverbrauchs  
 Katrin, das Teamprojektmitglied, arbeitet seit einiger Zeit an dem Projekt und möchte ihre Stunden und ihren Verbrauch für das Projekt erfassen. Sie hat nicht mehr gearbeitet, als vorab mit dem Kunden vereinbart wurde. Sie verwendet den Batchauftrag **Restverbrauch berechnen**, um den Restverbrauch für das Projekt in einem Projektbuchhaltungsblatt zu berechnen. Mithilfe der Stapelverarbeitung wird für jede Projektaufgabe die Differenz zwischen dem geplanten Verbrauch von Artikeln, Ressourcen und Aufwandssachposten und dem in Projektposten gebuchten tatsächlichen Verbrauch berechnet. Der Restverbrauch wird dann im Projektbuchungsblatt angezeigt, von dem aus sie eine Buchung vornehmen kann.  

### <a name="to-calculate-remaining-usage"></a>So berechnen Sie den Restverbrauch  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen]Symbol (media/ui-search/search_small.png "")Nach Seite oder Bericht suchen und geben **Projektbuch** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Öffnen Sie im Fenster **Projekt Erfassungsjournal** im Feld **Erfassungsjournalname** die Liste **Projekt Erfassungsjournalnamen**. Wählen Sie den Projekt-Erfassungsjournalnamen **Katrin** aus.  
3.  Wächlen Sie im Aktionsbereich **Restverbrauch**.  
4.  Wählen Sie im Fenster **Restverbrauch für Projekt berechnen** im Inforegister **Projektaufgabe** das Feld **Projektnr.** aus, und wählen die Jobnummer des entsprechenden Projekts, üblicherweise Projekt J00010.  
5.  Geben Sie auf dem Inforegister **Optionen** die Nummer **PW00001** in das Feld **Belegnr.** ein. Dadurch wird das zukünftige Tracking der Buchung vereinfacht.  
6.  Geben Sie als Buchungsdatum das heutige Datum ein.  
7.  Wählen Sie die Schaltfläche **OK** aus. Dadurch werden alle Projekt-Buchungsblattzeilen generiert, die von den von Bernard erstellten Planungszeilen für das Projektbuchhaltungsblatt abgeleitet wurden.  
8.  Wählen Sie die Schaltfläche **OK** im Bestätigungsfenster. Die generierten Zeilen werden dem Projekt-Erfassungsjournal hinzugefügt.  
9. Stellen Sie sicher, dass für alle Belegnummern J00001 angezeigt wird. Klicken Sie auf Aktionen, zeigen Sie auf **Buchen**, und klicken Sie dann auf Buchen. Wählen Sie **Ja**, um die Buchung zu bestätigen.  
10. Die Zeilen werden gebucht. Wählen Sie die Schaltfläche **OK**, um die Fenster zu schliessen.  

## <a name="creating-and-posting-a-job-sales-invoice"></a>Erstellen und Buchen einer Projektverkaufsrechnung  
 Als Nächstes kann Katrin eine neue Rechnung für das gesamte Projekt oder für Teil eines Projekts erstellen. Die Rechnung kann auch an eine andere Rechnung für denselben Kunden und dasselbe Projekt angefügt werden. In diesem Fall fakturiert Sie das gesamte Projekt, da es jetzt abgeschlossen ist.  

### <a name="to-create-a-job-sales-invoice"></a>So erstellen Sie eine Projektverkaufsrechnung  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie das Projekt aus, das Sie zuvor erstellt haben, und wählen die **Projektverkaufsrechnung erstellen** Aktion aus.  
3.  Löschen Sie im Inforegister **Projektaufgabe** in **Projektaufgabennr.** alle Filter, um das Projekt zu fakturieren. Wählen Sie im Feld **Projektnr.** das entsprechende Projekt aus.  
4.  Geben Sie im Inforegister **Optionen** das Buchungsdatum ein, und definieren Sie, ob eine Rechnung pro Aufgabe oder eine einzige Rechnung für alle Aufgaben erstellt werden soll.  
5.  Wählen Sie die Schaltfläche **OK**, um die Rechnung zu erstellen, und wählen Sie dann die Schaltfläche **OK** im Bestätigungsfenster.  

 Nachdem Katrin die Rechnung erstellt hat, kann sie von **Verkauf und Marketing** unter **Auftragsabwicklung** darauf zugreifen und sie weiter bearbeiten.  

### <a name="to-post-a-new-sales-invoice"></a>So buchen Sie eine neue Verkaufsrechnung  

1.  Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsrechnung** ein und wählen den zugehörenden Link aus.  
2.  Wählen Sie die Rechnung für die Debitorennummer 01445544. Die aus den Planungszeilen erfassten Informationen werden angezeigt.  
3.  Wählen Sie die Aktion **Buchen** aus. Wählen Sie **Ja**, um die Buchung zu bestätigen.  

### <a name="to-view-the-posted-invoice"></a>So zeigen Sie die gebuchte Rechnung an  

1.  Öffnen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Projektplanzeilen** aus.  
2.  Wählen Sie eine der fakturierten Planungszeilen aus, und wählen Sie auf der Registerkarte Start in der Gruppe Prozess die Option **Verkaufsrechnung/Gutschrift** aus.
3. Im Fenster **Projektrechnungen** wählen Sie die Aktion **Verkaufsrechnungen/Gutschrift** aus.  

 Katrin hat eine Frage zu den Preisen, Kosten und Gewinnen für dieses spezielle Projekt, daher greift sie über das Fenster **Statistik** auf die Informationen zu.  

### <a name="to-open-the-statistics-window"></a>So öffnen Sie das Fenster "Statistik"  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Statistik** aus. Sie können detaillierte Informationen über die Projektverkaufspreise, Kosten und Gewinne in lokalen und fremden Währungen anzeigen.  
3.  Wählen Sie die Schaltfläche **Schliessen**, um das Fenster **Projektstatistik** zu schliessen.  

## <a name="handling-fixed-prices"></a>Verwenden von Festpreisen  
 CRONUS wurde abgeschlossen, um Konferenzräume einzurichten. Als Projekt-Manager benötigt Bernard einen umfassenden Überblick über die erforderlichen Aufgaben für das Projekt sowie die zugehörigen budgetierten und angefallenen Kosten für jede Aufgabe. Zudem möchte er den vertraglich vereinbarten Verkaufsbetrag für das Projekt und den bisher fakturierten Betrag ermitteln. Er hat mit dem Kunden Festpreise für das Projekt vereinbart.  

### <a name="to-manage-fixed-pricing-in-jobs"></a>So verwalten Sie Festpreise in Projekten  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Projektnummer **Guildford**, und wählen Sie die **Projektaufgabenzeilen** Aktion aus.  
3.  Wählen Sie die Zeile 1120 aus, klicken Sie im Feld **Plan (Einstandsbetrag)** mit der rechten Maustaste auf den Betrag, und wählen Sie **DrillDown** aus.  

     Beim Überprüfen der Projektplanungszeilen stellt Bernard fest, dass er Katrin in dieser Phase des Projekts für 30 Stunden benötigt. Er vereinbart einen Festpreis mit dem Kunden.  

4.  Im Fenster **Projekt Buch,-Blatt** wählen Sie die Zeile 1120 und wählen die Aktion **Buchen** aus.  
5.  Wählen Sie auf der Registerkarte Start die Option **Neu** aus, um eine neue Zeile mit folgender Information zu erstellen.  

    -   **Zeilenart**: **Plan und Vertrag**  
    -   **Art**: **Ressource**  
    -   **Nr.**: **Katrin**  
    -   **Menge**: **30**  

7.  Wählen Sie die Schaltfläche **OK**, um das Fenster zu schliessen.  
8.  Klicken Sie mit der rechten Maustaste im Feld **Plan (Einstandsbetrag)**, und wählen Sie erneut **Drilldown** im Fenster **Projektaufgabenzeilen** aus. Zeigen Sie die Änderungen am Plan an. Die 30 Stunden wurden dem Plan hinzugefügt.  
9. Wählen Sie die Schaltfläche **OK**, um die Fenster zu schliessen.  

 Nachdem Katrin dem Plan für diese Aufgabenzeile hinzugefügt wurde, arbeitet sie 25 Stunden an dem Projekt. Sie trägt diese Stunden in das Projektbuchungsblatt ein.  

### <a name="to-enter-hours-in-the-job-journal"></a>So erfassen Sie Stunden im Projekt Erf.-Journal  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen]Symbol (media/ui-search/search_small.png "")Nach Seite oder Bericht suchen und geben **Projektbuch** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Geben Sie in einer neuen Zeile die folgenden Informationen ein:  

    -   **Zeilenart**: **(leer)**  
    -   **Buchungsdatum**: **(heutiges Datum)**  
    -   **Belegnr.**: **J00002**  
    -   **Projektnr.**: **Bäderwelt**  
    -   **Projektaufgabennr.**: **1120**  
    -   **Art**: **Ressource**  
    -   **Nr.**: **Katrin**  
    -   **Menge**: **25**  

3.  Wählen Sie die Aktion **Buchen** aus.  

     Einige Tage später arbeitet Katrin weitere 10 Stunden an dem Projekt. Sie hat jetzt insgesamt 35 Stunden an dem Projekt gearbeitet. Da Sie nur 30 Stunden mit dem Kunden vereinbart haben, werden dem Kunden nur fünf dieser Stunden in Rechnung gestellt. Katrin fügt manuell die fünf zusätzlichen Stunden hinzu, in denen sie den Plan bearbeitete.  

4.  Wählen Sie im Fenster Projekt **Erf.-Journal**auf der Registerkarte Start die Option **Restverbrauch berechnen**.  
5.  Geben Sie im Fenster **Restverbrauch für Projekt berechnen** die folgenden Informationen auf dem Inforegister **Optionen** ein:  

    -   **Belegnr.**: **J00003**  
    -   **Buchungsdatum**: **(heutiges Datum)**  

6.  Geben Sie auf dem Inforegister **Projektaufgabe** die folgenden Informationen ein:  

    -   **Projektnr.**: **Bäderwelt**  
    -   **Projektaufgabennr.**: **1120**  

     Klicken Sie auf die Schaltfläche **OK**, um die Berechnung auszuführen. Es gibt fünf Arbeitsstunden, die für Katrin bleiben. Das Feld **Zeilenart** ist leer; dies gibt an, dass nur der Verbrauch gebucht werden muss, da die Arbeit bereits geplant wurde.  

7.  Erstellen Sie im **Projekt Erfassungsjournal** eine neue Zeile mit den folgenden Informationen. Prüfen Sie, ob beide Projektnummern Folgenummern derer, die Sie bereits verwendet haben:  

    -   **Zeilenart**: **Plan**  
    -   **Projektnr.**: **Bäderwelt**  
    -   **Projektaufgabennr.**: **1120**  
    -   **Art**: **Ressource**  
    -   **Nr.**: **Katrin**  
    -   **Menge**: **5**  

     Durch die Verwendung der Zeilenart **Plan** werden die geplanten Kosten und der Preis aktualisiert, ohne die dem Kunden in Rechnung gestellten Einstandsbeträge und Preise aus dem Vertrag zu aktualisieren.  

8.  Wählen Sie die Aktion **Buchen** aus. Wählen Sie die Schaltfläche **OK**, um das Fenster zu schließen.  
9. Öffnen Sie die Liste **Projekte**.  
10. Wählen Sie das GUILDFORD Projekte und wählen Sie dann die Aktion **Projektplanzeilen** aus.  
11. Wählen Sie die Zeile 1120 aus, und klicken Sie im Feld **Plan (Einstandsbetrag)** mit der rechten Maustaste auf den Betrag. Wählen Sie **DrillDown** aus, um die Informationen anzuzeigen.  

     Sie können sehen, dass die Änderungen automatisch in der Zeile für die Projektaufgabennummer 1120 eingegeben wurden. Im Einstandsbetrag der geplanten Arbeit sind fünf zusätzliche Arbeitsstunden von Katrin dem Plan hinzugefügt worden.  

12. Klicken Sie auf die Schaltfläche **Schliessen**, um das Fenster zu schliessen.  
13. Klicken Sie mit der rechten Maustaste auf den Betrag im Feld **Vertrag (Einstandsbetrag)**, und wählen Sie dann **DrillDown** aus, um die Informationen anzuzeigen.  

     Im Einstandsbetrag des Vertrags werden nur die ursprünglich im Vertrag festgesetzten 30 Stunden angezeigt, da dies mit dem Kunden vereinbart wurde.  

## <a name="copying-jobs"></a>Kopieren von Projekten  
 Bernard hat mit einem Kunden, Blütenhaus GmbH, einen Vertrag über die Einrichtung von zehn Konferenzräumen abgeschlossen. Da die Vereinbarung ähnelt einem früheren Projekt. Daher spart es Zeit, dieses frühere Projekt zu kopieren.  

 Im Fenster **Projekt kopieren** können Sie das zu kopierende Projekt und die gewünschten Aufgabenzeilen auswählen. Sie können auch festlegen, ob die Projektposten aus dem Quellprojekt (dabei werden Planungszeilen basierend auf dem tatsächlichen Verbrauch erstellt) oder die Planungszeilen des Quellprojekts (dabei werden die ursprünglichen Planungszeilen in das neue Projekt kopiert) kopiert werden sollen. Danach können Sie die für das neue Projekt relevanten Planungszeilen- oder Projektpostenarten auswählen und in den Kopiervorgang einschliessen. Zum Schluss wählen Sie das Zielprojekt aus, und Sie legen fest, ob Preise und Mengen ebenfalls kopiert werden sollen.  

### <a name="to-copy-a-job"></a>So kopieren Sie ein Projekt  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die **Neu** Aktion aus, um eine neue Ressourcenkarte zu erstellen. Geben Sie die folgenden Informationen ein:  

    -   **Beschreibung**: **Zehn Konferenzräume einrichten**  
    -   **Rech. an Deb.-Nr.**: **20000**  

3.  Wählen Sie die Aktion **Von Workflowvorlage kopieren** aus.  
4.  Geben Sie im Fenster **Projektaufgaben kopieren** Folgendes ein:  

    -   **Projektnr.**: **Bäderwelt**  
    -   **Projektaufgabennr. von**: **1000**  
    -   **Herkunft**: **Projektplanzeilen**  
    -   **Inkl. Planzeilenart**: **Plan+Vertrag**  
    -   **Zu Projekt-Nr.** **Guildford-Einstellung bis zu 10 Konferenzräume**  
    -   Aktivieren Sie die Felder **Dimensionen kopieren** und **Menge kopieren**.  

5.  Wählen Sie die Schaltfläche **OK**, um das Projekt zu kopieren, und wählen Sie dann die Schaltfläche **OK**, um das Bestätigungsfenster zu schliessen.  

     Indem Sie Preise, Projektaufgabenzeilen und Projektplanungszeilen für die beiden Projekte vergleichen, können Sie sehen, dass die Informationen erfolgreich kopiert wurden.  

## <a name="making-payments-by-installments"></a>Anwenden von Teilzahlungen  
 CRONUS hat gerade ein großes Projekt an Land gezogen, das über ein Jahr laufen wird. Da viele Ressourcen erforderlich sind, richtet der Projektmanager den Vertrag so ein, dass der Kunde eine Teilzahlung im Voraus, eine Teilzahlung nach der Hälfte des Projekts und schliesslich die endgültige Zahlung nach Abschluss des Projekts leistet.  

### <a name="to-set-up-a-new-account"></a>So richten Sie ein neues Konto ein  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Kontenplan** ein und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie im Fenster **Kontenplan** auf der Registerkarte Start die Option **Neu**, um eine neue Karte zu erstellen.  
3.  Geben Sie auf der Karte **Neues Fibukonto** die folgenden Informationen ein:  

    -   **Nr.**: **6630**  
    -   **Name**: **Projektbezahlung**  

4.  Wählen Sie auf dem Inforegister **Buchung** im Feld **Produktbuchungsgruppe** die Option **SONST** aus. Wählen Sie die Schaltfläche **OK**, um das Fenster zu schliessen.  
5.  Wählen sie im Fenster **Kontenplan** die Option **Nr. - 6630 Projektbezahlung** und auf der Registerkarte Start in der Gruppe Vorgang die Option **Einrückung des Kontenplans**aus. Wählen Sie **Ja** aus, um den Vorgang zu bestätigen.  

 In den folgenden Verfahren wird gezeigt, wie Sie ein neues Projekt erstellen, die Preisgestaltung festlegen und dann Teilzahlungen einrichten. In den Projektaufgabenzeilen können Sie spezifische Zeilen für die Teilzahlungen erstellen. Alle für das Projekt ausgeführten Arbeiten werden dem Plan hinzugefügt und in den Verbrauchszeilen erfasst. Für jede Zahlungsaufgabenzeile der Planungszeilen kann die Zeilenart auf "Vertrag" festgelegt werden, wodurch die Fakturierung für den Debitor erfolgt. Geben Sie für die Anzahlung eine neue Zeile ein. In der Verbrauchsaufgabenzeile können Sie die Informationen für die in diesem Projekt verwendeten Artikel und Ressourcen eingeben, z. B. Mitarbeiterstunden und für das Projekt verbrauchte Artikel. Der Plan wird dadurch entsprechend erhöht.  

### <a name="to-make-a-payment-by-installment"></a>So wenden Sie eine Teilzahlung an  

1.  Erstellen Sie ein neues Projekt.  
2.  Geben Sie auf der neuen Karte **Projekt** die folgenden Informationen ein:  

    -   **Beschreibung**: **Neugestaltung des Empfangsbereichs**  
    -   **Rech. an Deb.-Nr.**: **30000**  
    -   **Projektbuchungsgruppe**: **Einrichten**  
    -   **WIP-Methode**: **Einstandswert**  

3.  Von der Projektkarte wählen Sie die **Ressource** Aktion aus. Geben Sie die folgenden Informationen ein:  

    -   **Code**: **Katrin**  
    -   **VK-Preis**: **10**  

     Wählen Sie die Schaltfläche **OK**, um das Fenster zu schließen.  

4.  Wählen Sie auf der Registerkarte **Projekt** die Option **Projektplanzeilen** aus.  

     In der folgenden Tabelle werden die Zeilen, die Sie erstellen, beschrieben.  

    |Zeile|Projektaufgabennr.|Description|Projektaufgabenart|  
    |----------|------------------|---------------------------------------|-------------------|  
    |1|1000|Zahlung - Anzahlung|Buchen|  
    |2|2000|Verbrauch|Buchen|  
    |3|3000|Zahlung - Hälfte|Buchen|  
    |4|4000|Zahlung - Abschluss|Buchen|  

5.  Im Fenster **Projekt Buch,-Blatt** wählen Sie die Zeile 1000 und wählen die Aktion **Buchen** aus.  
6.  Erstellen Sie eine Planungszeile mit den folgenden Informationen:  

    -   **Zeilenart**: **Vertrag**  
    -   **Planungsdatum**: **(heutiges Datum)**  
    -   **Art**: **Fibukonto**  
    -   **Nr.**: **6630**  
    -   **Menge**: **1**  
    -   **VK-Preis**: **5000**  

     Wählen Sie die Schaltfläche **OK**, um das Fenster zu schliessen.  

7.  Wählen Sie im Fenster **Projektaufgabenzeilen** die option **Aufgabe 2000** aus, und öffnen Sie seine **Projektplanzeilen**.  

     In der folgenden Tabelle wird die Planung, die Sie erstellen, beschrieben.  

    |Linie|Zeilenart|Planungsdatum|Typ|Nr.|Menge|  
    |----------|---------------|-------------------|----------|---------|--------------|  
    |1|Plan|(heutiges Datum)|Ressource|Katrin|120|  
    |2|Plan|(heutiges Datum)|Artikel|70104|10|  

     Wählen Sie die Schaltfläche **OK**, um das Fenster zu schliessen. Im Fenster **Projektaufgabenzeilen** können Sie sehen, dass die Planbeträge aktualisiert wurden.  

8.  Wählen Sie im Fenster **Projektaufgabenzeilen** die **Aufgabe 3000** aus.  
9. Erstellen Sie eine Planungszeile mit den folgenden Informationen:  

    -   **Zeilenart**: **Vertrag**  
    -   **Planungsdatum**: **ein zukünftigen Datum**  
    -   **Art**: **Fibukonto**  
    -   **Nr.**: **6630**  
    -   **Menge**: **1**  
    -   **VK-Preis**: **5000**  

     Wählen Sie die Schaltfläche **OK**, um das Fenster zu schliessen.  

10. Erstellen Sie eine ähnliche Planungszeile für Projektaufgabe 4000.  

 Nachdem die Aufgaben- und Planungszeilen erfasst wurden, erstellt Bernard eine Rechnung für die erste Zahlung. Er verwendet dazu die Projektaufgabenzeilen, um sicherzustellen, dass die Rechnung nur die Zeilen für die erste Zahlung enthält. Der Verkaufsauftrag kann über die Planungszeilen oder die Aufgabenzeilen geöffnet werden.  

### <a name="to-create-an-invoice"></a>So erstellen Sie eine Rechnung  

1.  Im Fenster **Projekt Buch,-Blatt** wählen Sie die Zeile 1000 und wählen die Aktion **Verkaufsrechung erstellen** aus.  
2.  Legen Sie im Fenster **Verkaufsrechnung erstellen** das heutige Datum als Buchungsdatum fest, geben Sie **" Nach Aufgabe** an, und wählen Sie die Schaltfläche **OK**, um eine Rechnung mit den Standardinformationen zu erstellen. Klicken Sie auf **OK**, um das Bestätigungsfenster zu schliessen.  
3.  Wählen Sie die Aktion **Verkaufsrechnung/Gutschrift**. Auf der Verkaufsrechnung können Sie sehen, dass die Rechnung nur die Anzahlung enthält. Diese Rechnung kann jetzt wie vereinbart an den Kunden gesendet werden.  

## <a name="next-steps"></a>Nächste Schritte  
 In dieser exemplarischen Vorgehensweise wurden Sie durch mehrere der grundlegenden Schritte für die Arbeit mit Projekten in [!INCLUDE[d365fin](includes/d365fin_md.md)] geführt. Sie haben gelernt, wie ein neues Projekt erstellt, ein Projekt kopiert und Zahlungen verarbeitet werden. Sie haben auch eine Demonstration gesehen, wie Stunden verfolgt und Rechnungen erstellt werden.  

## <a name="see-also"></a>Siehe auch  
 [Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)   
 [Richten Sie Ihr Projektmanagement ein.](projects-setup-projects.md)   
 [Verwendung von Ressourcen](projects-how-use-resources.md)   
 [So gehts: Überwachen des Status und der Leistung](projects-how-monitor-progress-performance.md)   
 [Vorgehensweise: Fakturieren](projects-how-invoice-jobs.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

