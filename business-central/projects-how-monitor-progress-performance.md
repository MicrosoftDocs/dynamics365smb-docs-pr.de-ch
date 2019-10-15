---
title: Eine WIP-Methode definieren und den Projekt-Status überwachen | Microsoft Docs
description: Beschreibt, wie Sie eine Umlaufbestand-Methode (WIP) erstellen und WIP berechnen können, um den finanziellen Wert von Projekten zu beurteilen, während sie ausgeführt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a11e2064467ffa168603aed74c24f4bb972ea10d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312834"
---
# <a name="monitor-job-progress-and-performance"></a>Überwachen des Status und der Leistung
Im Laufe eines Projekts werden Material sowie Ressourcen und andere Aufwendungen verbraucht und müssen auf das Projekt gebucht werden. Umlaufbestand (WIP) ist eine Funktion, mit der Sie den finanziellen Wert im Fibuposten schätzen können, solange die Projekte noch nicht abgeschlossen sind. In vielen Fällen werden die Aufwendungen für ein Projekt vor der Fakturierung des Projekts gebucht. Wurden ausschliesslich Aufwendungen gebucht, ergibt sich eine inkorrekte Finanzauswertung. Weitere Informationen finden Sie unter [WIP-Methode verstehen](projects-understanding-wip.md).

Zum Überwachen des Werts im Fibuposten können Sie die WIP berechnen und den Wert im Fibuposten buchen.

Die WIP-Berechnung kann auf der Grundlage der folgenden Optionen erfolgen:

* Einstandswert
* Verkaufswert
* Realisierbare Kosten
* Prozentsatz der Fertigung
* Bei Abschluss

Soll das Ergebnis unter Verwendung einer anderen Methode angezeigt werden, können Sie die Methode ändern und die WIP-Berechnung erneut ausführen. Dieser Schritt lässt sich beliebig oft wiederholen. Die WIP wird lediglich berechnet; sie wird nicht in der Finanzbuchhaltung gebucht. Nach Ausführung der WIP-Berechnung kann das Ergebnis in die Fibuposten gebucht werden.

## <a name="to-create-a-job-wip-method"></a>WIP-Methode für Projekt erstellen
Sie können eine WIP-Methode für das Projekt erstellen, die den Bedarf Ihrer Organisation wiedergibt. Nachdem Sie diese erstellt haben, können Sie diese als die standardmässige Projekt-WIP-Berechnungsmethode festlegen, die in Ihrer Organisation verwendet wird.  

> [!NOTE]
> Nachdem Sie Ihre neue Methode verwendet haben, um WIP-Posten zu erstellen, können Sie die Methode nicht löschen oder ändern.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Job-WIP-Methode** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Schliessen Sie die Seite.   
4. Um diese neue Methode zum Standard zu machen, wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Job einrichten** ein, und wählen dann den zugehörigen Link aus.  
5. Wählen Sie im Feld **WIP-Standardmethode** die Methode aus der Liste aus.

## <a name="to-define-a-wip-method-for-a-job"></a>Eine WIP-Methode für ein Projekt definieren
Wenn Sie ein neues Projekt erstellen, müssen Sie auswählen, welche WIP-Methode angewendet werden soll. In einigen Fällen kann die WIP-Methode, die Sie verwenden können, bereits als Standard eingerichtet sein.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus. Weitere Informationen finden Sie unter  [Projekte erstellen](projects-how-create-jobs.md).  
3. Wählen Sie auf der Seite **Projektkarte** im Feld **WIP-Methode** eine WIP-Methode aus der Liste aus. Wenn eine standardmässige Methode festgelegt wurde, können Sie sofern erforderlich eine andere Option aktivieren.  

## <a name="to-calculate-wip"></a>So berechnen Sie die WIP
Bestimmen den WIP-Betrag, der im Rahmen der Berichterstellung am Periodenende auf Bilanzkonten gebucht werden muss Dazu verwenden Sie die Stapelverarbeitung **WIP berechnen Projekt**.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Job berechnet WIP** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **WIP berechnen** aus.
3. Geben Sie auf der Seite **WIP für Projekt berechnen** die notwendigen Felder ein.
4. Wählen Sie die Schaltfläche **OK** aus.  

> [!NOTE]  
>   Die Stapelverarbeitung berechnet nur den WIP. Er wird nicht auf das Fibukonto gebucht. Dazu müssen Sie die Stapelverarbeitung **WIP nach Sachposten Projekt** ausführen, nachdem Sie den WIP berechnet haben. Weitere Informationen finden Sie in der folgenden Prozedur.

## <a name="to-post-wip"></a>Zu buchender WIP
Wenn Sie den WIP berechnet haben, können Sie ihn zur Erstellung von Periodenendberichten auf Bilanzkonten buchen. Dazu verwenden Sie die Stapelverarbeitung **WIP auf Fibuposten buchen**.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Job bucht WIP auf Buch.Blatt** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie auf der Seite **WIP nach Sachkonten Projekt buchen** aus und füllen Sie die Felder wie erforderlich aus.  
3. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-view-job-usage-estimates-and-post-updates"></a>So zeigen Sie Projektverbrauchschätzungen und Buchungsaktualisierungen an.
Der Projektverbrauch kann bis zum Projektabschluss in einem einzigen Schritt angezeigt werden. Verwenden Sie hierzu die Stapelverarbeitung **Restverbrauch für Projekt berechnen** für alle Aufgaben bis zum Projektende (einschliesslich).  

Auf diese Weise können Sie die ursprüngliche Planung mit den tatsächlichen Ergebnissen vergleichen und ggf. Änderungen vornehmen oder neue Posten hinzufügen. Beispiel: Sie haben für ein Projekt eine Dauer von zehn Stunden geplant, aktueller Stand sind jedoch 15 Stunden. Sie können die fünf zusätzlichen Stunden entweder der bestehenden Erf.-Journalzeile hinzufügen oder eine neue Erf.-Journalzeile erstellen, um die fünf Stunden als Überstunden (anderer Arbeitstyp) zu melden. Die angemessenen Kosten und der Preis werden berechnet und dann können Sie sie in das Protokoll buchen.  

> [!NOTE]  
>   Artikeleinträge erstellen Lagerposten und reduzieren die Lagerbestandmenge. Durch die Stapelverarbeitung **Lagerregulierung buchen** werden die Kosten aus dem Lagerbestand in die Finanzbuchhaltung gebucht. Aus Posten für Ressourcen werden Ressourcenposten erstellt.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Job Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie ein Buch.-Blatt des entsprechenden Projekts, und wählen Sie dann die Aktion **Verbleibender Verbrauch berechnen** aus.  
3. Geben Sie auf der Seite **Restverbrauch für Projekt berechnen** die Belegnummer und das Erfassungsdatum ein, das in das Erf.-Journal eingefügt werden soll und wählen Sie dann die Schaltfläche **OK**.  
4. Aktualisieren Sie das Erf.-Journal mit sämtlichen Änderungen, die möglicherweise erforderlich sind.  
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-view-job-ledger-entries"></a>Projektbuchungsposten anzeigen
Alle projektbezogenen Posten werden in Projektjournalen aufgezeichnet und fortlaufend nummeriert, beginnend mit 1. Aus den Projektjournalen können Sie eine Übersicht über alle Projektposten erhalten.    

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Job-Register** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Projektposten** aus.

Auf der Seite **Projektposten** können Sie die Posten überprüfen, die einem Projekt zugeordnet sind.  

## <a name="see-also"></a>Siehe auch
[Verwalten von Projekten](projects-manage-projects.md)
[Verwalten der Lagerkosten](finance-manage-inventory-costs.md)   
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
