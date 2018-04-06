---
title: 'Designdetails: Ausgleich von Bedarf und Vorrat | Microsoft Docs'
description: "Das Kernstück des Planungssystems beinhaltet den Augleich von Bedarf und Vorrat durch das Vorschlagen von Aktionen zur Revidierung der Beschaffungsaufträge bei fehlendem Ausgleich. Dieses findet pro Kombination von Variante und Lagerort statt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 51555bbfbd7fec6ca46bc1b2e6b02382288a41bc
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-balancing-supply-with-demand"></a>Designdetails: Ausgleich von Bedarf und Vorrat
Das Kernstück des Planungssystems beinhaltet den Augleich von Bedarf und Vorrat durch das Vorschlagen von Aktionen zur Revidierung der Beschaffungsaufträge bei fehlendem Ausgleich. Dieses findet pro Kombination von Variante und Lagerort statt.  
  
Stellen Sie sich vor, dass jedes Lagerprofil eine Zeichenfolge aus den Bedarfsereignissen (sortiert nach Datum und Priorität) und eine entsprechende Zeichenfolge von Vorratsereignissen enthält. Jedes Ereignis verweist zurück auf seinen Herkunftsartstyp und seine Identifizierung. Die Regeln für den Ausgleich des Artikels sind einfach. Zu jedem Zeitpunkt des Vorgangs können vier Instanzen des Abgleichs von Bedarf und Vorrat auftreten:  
  
1. Kein Bedarf oder Vorrat für den Artikel => die Planung ist abgeschlossen (oder soll nicht beginnen).  
2. Bedarf existiert, aber es ist kein Vorrat vorhanden=> Vorrat soll vorgeschlagen werden.  
3. Vorrat existiert, aber es ist kein Bedarf vorhanden=> Vorrat soll storniert werden.  
4. Bedarf und Vorrat sind vorhanden => Fragen sollten gestellt und beantwortet werden, bevor das System sicherstellen kann, dass der Bedarf befriedigt wird und der Vorrat ausreicht.  
  
     Wenn das Timing des Vorrats nicht geeignet ist, kann der Vorrat möglicherweise wie folgt umgeplant werden:  
  
    1.  Wenn der Vorrat vor dem Bedarf platziert wird, kann der Vorrat vielleicht umgeplant werden, so dass der Bestand so niedrig wie möglich ist.  
    2.  Wenn das Angebot später gesetzt wird, kann das Angebot möglicherweise umgeplant werden. Andernfalls schlägt das System einen neuen Vorrat vor.  
    3.  Wenn der Vorrat den Bedarf an dem Datum erfüllt, kann das Planungssystem fortfahren, zu untersuchen, ob die Menge des Vorrats den bedarf decken kann.  
  
     Sobald die Zeitplanung erfolgt ist, kann die entsprechende bereitzustellende Menge wie folgt berechnet werden:  
  
    1.  Wenn die Vorratsmenge kleiner als der Bedarf ist, ist es möglich, dass die Vorratsmenge erhöht werden kann (oder nicht, wenn Sie durch eine Höchstmengenrichtlinie begrenzt ist).  
    2.  Wenn die Vorratsmenge grösser als der Bedarf ist, ist es möglich, dass die Vorratsmenge reduziert werden kann (oder nicht, wenn Sie durch eine Mindestmengenrichtlinie begrenzt ist).  
  
     An dieser Stelle besteht eine von zwei Situationen:  
  
    1.  Der aktuelle Bedarf kann abgedeckt werden, in welchem Fall er geschlossen werden kann und die Planung für den folgenden Bedarf begonnen werden kann.  
    2.  Das Vorrat hat sein Maximum erreicht, ein Teil der Bedarfsmenge wurde nicht abgedeckt. In diesem Fall kann das Planungssystem den aktuellen Vorrat schliessen und mit dem nächsten fortfahren.  
  
 Der Vorgang beginnt von vorn mit dem folgenden Bedarf und dem folgenden Vorrat oder umgekehrt. Der aktuelle Vorrat kann möglicherweise auch diesen nächsten Bedarf abdecken, oder der aktuelle Bedarf wurde noch nicht vollständig abgedeckt.  
  
## <a name="rules-concerning-actions-for-supply-events"></a>Regeln im Hinblick auf Aktionen für Vorratsereignisse  
Wenn das Planungssystem eine top-down Berechnung ausführt, in der der Vorrat den Bedarf erfüllen muss, gilt der Bedarf als entnommen, d.h. es liegt ausserhalb des Steuererung des Planungssystems. Jedoch kann die Vorratsseite verwaltet werden. Daher wird vom Planungssystem vorgeschlagen, neue Beschaffungsaufträge zu erstellen, bestehenden neu zu planen und/oder die Bestellmenge zu ändern. Wenn ein vorhandener Beschaffungsauftrag überflüssig wird, schlägt das System dem Benutzer vor, ihn zu stornieren.  
  
Wenn der Benutzer einen vorhandenen Beschaffungsauftrag aus den Planungsvorschlägen ausschliessen möchte, kann er angeben, dass keine Planungsflexibilität besteht (Planungsflexibilität = Keine). Dann wird überschüssiger Vorrat aus diesem Auftrag verwendet, um Bedarf zu decken, aber keine Aktion wird vorgeschlagen.  
  
Im Allgemeinen haben alle Vorräte eine Planungsflexibilität, die durch den Zustand der einzelnen vorgeschlagenen Aktionen eingeschränkt ist.  
  
-   **Neuplanung Aus**: Das Datum eines vorhandenen Beschaffungsauftrags kann ausgeplant werden, um das Fälligkeitsdatum des Bedarfs zu erfüllen, es sei denn:  
  
    -   Es stellt den Lagerbestand dar (immer mit Tag Null).  
    -   Es enthält einen Auftrag-zu-Auftrag-Link zu einem anderen Bedarf.  
    -   Es liegt ausserhalb des durch den Zeitrahmen definierten, neu geplanten Fensters.  
    -   Es gibt einen näheren Bestand, der verwendet werden könnte.  
    -   Andererseits entscheidet sich der Benutzer möglicherweise zu einer Neuplanung, weil  
    -   Der Beschaffungsauftrag wurde bereits an einem früheren Datum mit einem anderen Bedarf verbunden.  
    -   Das erforderliche Neuplanung ist so minimal, dass der Benutzer sie als geringfügig ansehen wird.  
  
-   **Neuplanung Ein**: Das Datum eines vorhandenen Beschaffungsauftrags kann eingeplant werden, ausgenommen unter den folgenden Bedingungen:  
  
    -   Es wird direkt mit einem anderen Bedarf verknüpft.  
    -   Es liegt ausserhalb des durch den Zeitrahmen definierten, neu geplanten Fensters.  
  
> [!NOTE]  
>  Wenn ein Artikel unter Verwendung eines Minimalbestands geplant wird, kann der Beschaffungsauftrag immer bei Bedarf geplant werden. Dies ist häufig in den vorwärtsgeplanten Beschaffungsaufträgen, die durch einen Minimalbestand gestartet werden.  
  
-   **Zugangs-Menge**: Die Menge eines vorhandenen Beschaffungsauftrags kann erhöht werden, damit der Bedarf erfüllt werden kann, es sei denn, der Beschaffungsauftrag ist direkt mit einem Bedarf durch einen Auftrag-zu-Auftrag-Link verknüpft.  
  
> [!NOTE]  
>  Obwohl es möglich ist, den Beschaffungsauftrag zu erhöhen, kann dies durch eine maximale Auftragsgrösse eingeschränkt sein.  
  
-   **Menge reduzieren**: Ein vorhandener Beschaffungsauftrag mit einem Überschuss im Vergleich zu einem vorhandenen Bedarf kann reduziert werden, damit der Bedarf erfüllt werden kann.  
  
> [!NOTE]  
>  Obwohl die Menge verringert werden kann, ist möglicherweise immer noch Überschuss im Vergleich zum Bedarf vorhanden, und zwar aufgrund einer Mindestauftragsmenge oder eines Auftragsvielfachen.  
  
-   **Abbrechen**: Als spezieller Vorfall der Mengenverminderungsaktion könnte der Beschaffungsauftrag storniert werden, wenn er bis auf Null verringert wurde.  
-   **Neu**: Wenn kein Beschaffungsauftrag existiert oder jedoch ein existierender, der nicht geändert werden kann, um der erforderlichen Menge im angeforderten Fälligkeitsdatum zu genügen, wird ein neuer Beschaffungsauftrag vorgeschlagen.  
  
## <a name="determining-the-supply-quantity"></a>Bestimmen der Vorratsmenge  
Durch den Benutzer definierte Planungsparameter steuern die vorgeschlagene Menge eines jeden Beschaffungsauftrags.  
  
Wenn das Planungssystem die Menge eines neuen Beschaffungsauftrags oder die Mengenänderung in bestehenden Aufträgen berechnet, kann sich die vorgeschlagene Menge von der tatsächlich benötigten unterscheiden.  
  
Wenn ein Maximalbestand oder eine feste Auftragsmenge ausgewählt werden, wird die vorgeschlagene Menge erhöht, um diese feste Menge oder den Maximalbestand zu erfüllen. Wenn ein Wiederbeschaffungsverfahren einen Minimalbestand verwendet, wird die Menge mindestens so erhöht, dass der Minimalbestand erreicht wird.  
  
 Die vorgeschlagene Menge kann in dieser Sequenz geändert werden:  
  
1. Bis zur maximalen Auftragsmenge (falls vorhanden).  
2. Aufwärts bis zur Mindestbestellmenge.  
3. Aufwärts bis zum nächsten Losgrössenrundungsfaktor. (Im Falle fehlerhafter Einstellungen verstösst dies möglicherweise gegen die maximale Auftragsmenge.)  
  
## <a name="order-tracking-links-during-planning"></a>Bedarfsverursacherverknüpfungen bei der Planung  
Hinsichtlich des Auftragstracking während der Planung ist es wichtig zu erwähnen, dass das Planungssystem die dynamisch erstellten Auftragstrackingverknüpfungen für die Artikel-/Varianten-/Lagerortkombinationen neu anordnet.  
  
Hierfür gibt es zwei Gründe:  
  
-   Das Planungssystem muss in der Lage sein, seine Vorschläge zu begründen; dass der Gesamtbedarf gedeckt wurde und dass keine Beschaffungsaufträge überflüssig sind.  
-   Dynamisch erstellte Auftragstrackinglinks müssen regelmässig nachjustiert werden.  
  
Im Laufe der Zeit geraten dynamische Bedarfsverursacherverknüpfungen aus der Balance, da das gesamte Bedarfsverursachernetzwerk erst dann wiederhergestellt wird, wenn ein Bedarf- oder Vorratsereignis tatsächlich geschlossen ist.  
  
Vor dem Ausgleich des Vorrats nach Bedarf löscht das Programm alle vorhandenen Auftragstrackinglinks. Dann während des Ausgleichsvorgangs, wenn ein Bedarfs- oder Zubehörereignis abgeschlossen wird, werden neue Bedarfsverursacherverknüpfungen zwischen Bedarf und Offerte erstellt.  
  
> [!NOTE]  
>  Selbst wenn der Artikel nicht für die dynamische Auftragstracking eingerichtet wurde, erstellt das Planungssystem Auftragsverfolgungslinks wie oben erläutert.  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)   
[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)
