---
title: Info zu Fertigungsaufträgen | Microsoft Docs
description: Fertigungsaufträge werden dazu verwendet, die Umwandlung von Einkaufsmaterialien in Produktionsartikel zu verwalten. Fertigungsaufträge (Arbeits- oder Werkaufträge) leiten Arbeit durch verschiedene Einrichtungen (Arbeitsplätze oder Arbeitsplatzgruppen) im Fertigungsbereich.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cc62673e83fa0a748164af57bf0a075ca325dde4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925019"
---
# <a name="about-production-orders"></a>Info zu Fertigungsaufträgen
Fertigungsaufträge werden dazu verwendet, die Umwandlung von Einkaufsmaterialien in Produktionsartikel zu verwalten. Fertigungsaufträge (Arbeits- oder Werkaufträge) leiten Arbeit durch verschiedene Einrichtungen (Arbeitsplätze oder Arbeitsplatzgruppen) im Fertigungsbereich.  

Bevor sie mit der Produktion fortfahren, führen die meisten Unternehmen eine Beschaffungsplanung aus, in der Regel einmal wöchentlich, um zu berechnen wie viele Fertigungsaufträge und Einkaufsbestellungen auszuführen sind, um den Verkaufsbedarf diese Woche zu erfüllen. Einkaufsbestellungen liefern die Komponenten, die nach der Fertigungsstückliste erforderlich sind, um die Endartikel zu fertigen.

Fertigungsaufträge sind die zentralen Komponenten der Fertigungsfunktionen der Anwendung und enthält die folgenden Informationen:  

-   Produkte, die für die Fertigung geplant sind  
-   Materialien, die für die geplanten Fertigungsaufträge erforderlich sind  
-   Produkte, die soeben gefertigt wurden  
-   Materialien, die bereits ausgewählt wurden  
-   Produkte, die früher gefertigt wurden  
-   Materialien, die in früheren Fertigungsvorgängen verwendet wurden  

Fertigungsaufträge sind die Ausgangspunkte für:  

-   Planen der zukünftigen Fertigung  
-   Überwachen der aktuellen Fertigung  
-   Tracking der abgeschlossenen Fertigung  

## <a name="production-order-creation"></a>Fertigungsauftrag erstellen  
Fertigungsaufträge können auftragsweise manuell aus den Seiten **Fertigungsauftrag** , **Verkaufsauftragsplanung** und/oder **Auftragsplanung** erstellt werden. Mehrere Aufträge werden aus der Seite **Planungsvorschlag** erstellt.  

Für die Erstellung eines Fertigungsauftrags werden Informationen aus folgenden Quellen verwendet:  

- Arti&kel  
- Operationspläne
- Arbeitspläne  
- Arbeitsplätze  
- Arbeitsplatzgruppen  

## <a name="limitations-on-production-order-creation"></a>Einschränkungen für das Erstellen von Fertigungsaufträgen  
Ein Fertigungsauftrag wird automatisch reserviert und zu seinem Ursprung verfolgt, wenn:  

-   Er aus dem **Planungsvorschlag** erstellt wurde  
-   Wurde mit der Auftragsfunktion auf der Seite **Verkaufsauftragsplanung** erstellt  
-   Wurde aus der Seite **Auftragsplanung** erstellt  
-   Die Funktion **Neu planen** für Fertigungsaufträge verwendet wird  

Weitere Informationen finden Sie unter [Titel-Beziehungen zwischen Bedarf und Vorrat nachverfolgen](production-how-track-demand-supply.md).

Fertigungsaufträge, die auf andere Weise erstellt wurden, werden nicht automatisch reserviert und verfolgt.   

## <a name="production-order-status"></a>Fertigungsauftragsstatus (FA-Status)  
Über den Fertigungsauftragsstatus wird gesteuert, wie sich der Fertigungsauftrag in der Anwendung sich verhält. Form und Inhalt der Produktion werden durch den Status des Auftrags festgelegt. Je nach Status werden die Fertigungsaufträge auf verschiedenen Seiten angezeigt. Sie können den Status eines Fertigungsauftrags nicht manuell ändern; Sie müssen die Funktion **Status ändern** verwenden.  

### <a name="simulated-production-order"></a>Simulierter Fertigungsauftrag  
Ein simulierter Fertigungsauftrag zeichnet sich durch folgende Eigenschaften aus:  

- Wie sein Name schon ausdrückt, ist er eine Simulation, und sein Hauptzweck besteht in der Offertenerstellung und Kalkulation (Bewertung) - beispielsweise wenn die Abteilung für Forschung und Entwicklung eine Kostenschätzung für einen vorgeschlagenen Artikel benötigt. Ein simulierter Fertigungsauftrag fungiert als Beispiel eines Fertigungsauftrages.  
- Er hat keinerlei Auswirkungen auf die Planung von Aufträgen. Simulierte Fertigungsaufträge werden weder von einer  Planung (Prod.-Programmplanung und Nettobedarf) berücksichtigt, noch wirken sie sich auf eine Planung aus. Ausserdem kann ein simulierter Fertigungsauftrag nicht als Vorlage verwendet werden, weil er gelöscht wird, sobald Sie seinen Status geändert haben.  

### <a name="planned-production-order"></a>Geplanter Fertigungsauftrag  
Ein geplanter Fertigungsauftrag (FA) zeichnet sich durch folgende Eigenschaften aus:  

- Sie können einen geplanten FA automatisch aus einem Verkaufsauftrag erstellen.  
- Ein geplanter Fertigungsauftrag ist wie ein freigegebener Fertigungsauftrag und stellt Informationen für die Kapazitätsplanung bereit, indem er die Kapazitätsanforderungen nach Arbeitsplatz oder Arbeitsplatzgruppe zeigt.  
- Ein geplanter Fertigungsauftrag entspricht der besten Schätzung der zukünftigen Auslastung des Arbeitsplatzes oder der Arbeitsplatzgruppe auf Basis der verfügbaren Informationen. Üblicherweise wird ein geplanter FA aus den Planungsinformationen generiert, er kann aber auch manuell erstellt werden. Da ein geplanter FA während der Generierung späterer Planungsschritte gelöscht wird, ist eine manuelle Erstellung nicht empfehlenswert.  
- Die Generierung eines geplanten FA ergibt eine vorgeschlagene "voraussichtliche Auftragsfreigabe", die die Menge, das Freigabedatum und das Fälligkeitsdatum enthält. Die Logik des Planungssystems basiert auf der Beschaffungsmethode, den Wiederbeschaffungsverfahren und den Auftragsmodifikationen, die im Planungsvorgang für den Nettobedarf festgelegt wurden.  
- Wenn Sie die Auswirkungen eines geplanten FA wissen möchten, sehen Sie sich auf dem Arbeitsplan des geplanten FA die Auslastung für jeden Arbeitsplatz oder jede Arbeitsplatzgruppe an.  

### <a name="firm-planned-production-order"></a>Fest geplanter Fertigungsauftrag  
Ein fest geplanter Fertigungsauftrag (FA) zeichnet sich durch folgende Eigenschaften aus:  

- Sie können einen fest geplanten FA automatisch aus einem Verkaufsauftrag erstellen.  
- Ein fest geplanter FA fungiert im Planungsschema für einige zukünftige Projekte, die für die Fertigung freigegeben wurden, als Platzhalter.  
- Ein fest geplanter FA kann aus Planungsinformationen generiert oder manuell aus Verkaufsaufträgen erstellt werden. Er wird im weiteren Verlauf der Planung nicht gelöscht.  
- Die Generierung eines fest geplanten FA ergibt eine vorgeschlagene "voraussichtliche Auftragsfreigabe", die die Menge, das Freigabedatum und das Fälligkeitsdatum enthält. Die Logik des Planungssystems basiert auf der Beschaffungsmethode, den Wiederbeschaffungsverfahren und den Auftragsmodifikationen, die im Planungsvorgang für den Nettobedarf festgelegt wurden.  
- Wenn Sie die Auswirkungen eines fest geplanten FA wissen möchten, sehen Sie sich auf dem Arbeitsplan des fest geplanten FA die Auslastung für jeden Arbeitsplatz oder jede Arbeitsplatzgruppe an.  

### <a name="released-production-order"></a>Freigegebener Fertigungsauftrag  
Ein freigegebener Fertigungsauftrag (FA) zeichnet sich durch folgende Eigenschaften aus:  

- Sie können einen freigegebenen FA automatisch aus einem Verkaufsauftrag erstellen.  
- Wenn ein Fertigungsauftrag freigegeben wurde, heisst dies nicht notwendigerweise, dass Materialien kommissioniert wurden oder das Projekt physisch zu seinem ersten Arbeitsgang verschoben wurde.  
- In einem Unternehmen mit Auftragsfertigung kann es üblich sein, einen freigegebenen FA unmittelbar nach Eingang eines Verkaufsauftrags zu erstellen.  
- Der tatsächliche Materialverbrauch und die tatsächlichen Istmeldungen können mit einem freigegebenen FA erfasst werden. Ausserdem kann automatisches Buchen von Verbrauch und Istmeldungen nur für freigegebene Fertigungsaufträge erfolgen.  

### <a name="finished-production-order"></a>Beendeter Fertigungsauftrag  
Ein beendeter Fertigungsauftrag (FA) zeichnet sich durch folgende Eigenschaften aus:  

- Ein beendeter FA ist üblicherweise ein FA, dessen Artikel gefertigt ist.  
- Das Beenden eines Fertigungsauftrages ist eine wichtige Aufgabe beim Abschliessen der Gesamtkostenbewertung des Artikels, der gefertigt wird. Durch Beenden eines Fertigungsauftrages kann die Bewertung angepasst und abgestimmt werden.  
- Beendete Fertigungsaufträge werden für die Erstellung von statistischen Berichten sowie als Unterstützung für die Möglichkeit verwendet, eine Rückverfolgung zu anderen Aufträgen (z. B. Verkaufsaufträge, Fertigungsaufträge und Einkaufsbestellungen) auszuführen. Die Möglichkeit, eine Rückverfolgung zu einem beendeten FA auszuführen, versetzt Sie in die Lage, die genaue Historie nachzuvollziehen.  
- Ein beendeter FA kann nicht geändert werden.  

## <a name="production-order-execution"></a>Fertigungsauftrag ausführen  
Sobald ein Fertigungsauftrag erstellt und geplant worden ist, muss er für den Fertigungsbereich freigegeben werden, damit er ausgeführt wird. Während des Ausführens des Auftrags erfassen Sie Folgendes:  

- Die Materialien, die kommissioniert oder verbraucht wurden  
- Die Zeit, die für das Abarbeiten des Auftrags benötigt wurde  
- Die Menge des gefertigten übergeordneten Artikels  

Diese Informationen können manuell oder über automatische Berichterstellung erfasst werden, entsprechend der Artikeleinrichtung im Feld .  

### <a name="material-consumption"></a>Materialverbrauch  
Die Anwendung bietet verschiedene Optionen, wie ein Produktionsbetrieb den Materialverbrauch erfassen kann. Beispielsweise kann es vorteilhaft sein, den Materialverbrauch manuell zu erfassen, weil häufig Komponenten ersetzt werden oder der Ausschuss grösser ist als erwartet.  

Der Verbrauch von Materialien kann über das FA-Verbrauchs Erf.-Journal verarbeitet werden, kann aber auch automatisch durch die Anwendung erfasst werden (wird als automatische Berichterstellung bezeichnet). Es gibt folgende Berichterstellungsmethoden:  

-   Manuell  
-   Vorwärts  
-   Rückwärts  

Die manuelle Verbrauchsberichterstellung verwendet "FA-Verbrauchs Erf.-Journal", um die Materialkommissionierung anzugeben.  

Bei der Verbrauchsberichterstellung vom Typ "Vorwärts" wird davon ausgegangen, dass die erwarteten Mengen aller Materialien für den gesamten Auftrag bei der Freigabe eines Fertigungsauftrags verbraucht werden, sofern keine Verbindungscodes verwendet werden. Bei Verwendung von Verbindungscodes werden die Materialien, die nach dem Beginn des Fertigungsschrittes verbraucht werden, im "FA-Istmeldungs Erf.-Journal" erfasst. Soll der gesamte Fertigungsauftrag vorwärts gebucht werden, müssen die beiden folgenden Bedingungen erfüllt sein:  

- Für jeden Artikel in der Produktionsstückliste der obersten Ebene muss auf seiner Artikelkarte die Buchungsmethode "Vorwärts" ausgewählt sein.  
- Aus der Produktionsstückliste müssen alle Verbindungscodes entfernt worden sein.  

Bei der Verbrauchsberichterstellung vom Typ "Rückwärts" werden die tatsächlichen Mengen aller kommissionierten oder verbrauchten Materialien erfasst, sobald sich der Status eines Fertigungsauftrags in *Beendet* geändert hat und sofern keine Verbindungscodes verwendet werden. Bei Verwendung von Verbindungscodes werden die Materialien verbraucht, nachdem eine Menge des übergeordneten Artikels für den Fertigungsschritt im "FA-Istmeldungs Erf.-Journal" erfasst wurde.  

Wird der Fertigungsauftrag aktualisiert, wird die Buchungsmethode von der Artikelkarte kopiert. Da die Buchungsmethode für jede Komponente eines Fertigungsauftrags steuert, wie und wann der Verbrauch erfasst wird, sollten Sie wissen, dass Sie die Buchungsmethode für bestimmte Artikel direkt auf dem "Fertigungsauftrag" ändern können.  

#### <a name="automatic-consumption-posting-flushing"></a>Automatisches Buchen des Verbrauchs  
Der Vorteil der automatischen Buchung besteht darin, dass sie die Dateneingabe erheblich verringert. Durch die Möglichkeit, einen Arbeitsgang automatisch zu buchen, kann der gesamte Erfassungsprozess für Verbrauch und fertige Artikel automatisiert werden. Der Nachteil des automatischen Buchens besteht darin, dass Ausschuss möglicherweise nicht richtig oder sogar gar nicht erfasst wird. Die Methoden zur automatischen Berichterstellung:  

- "Vorwärts"-Buchen des gesamten Auftrags  
- "Vorwärts"-Buchen pro Arbeitsgang  
- "Rückwärts"-Buchen pro Arbeitsgang  
- "Rückwärts"-Buchen des gesamten Auftrags  

#### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Automatisches Berichtswesen - "Vorwärts"-Buchen des gesamten Auftrags  
Wenn Sie den Fertigungsauftrag zu Beginn des Projekts mit der Methode "Vorwärts" buchen, verhält sich die Anwendung ähnlich wie bei einem manuellen Verbrauch. Der Hauptunterschied besteht darin, dass der Verbrauch automatisch auftritt.  

- Der gesamte Inhalt der Fertigungsstückliste wird zu dem Zeitpunkt verbraucht und dem Lagerbestand entnommen, zu dem der freigegebene Fertigungsauftrag aktualisiert wird.  
- Die Verbrauchsmenge entspricht der Menge pro Stück, die in der Fertigungsstückliste angegeben ist, multipliziert mit der Anzahl der übergeordneten Artikel, die gefertigt werden.  
- Es ist nicht erforderlich, irgendwelche Informationen im FA-Verbrauchs Erf.-Journal zu erfassen, wenn für alle Artikel festgelegt ist, dass sie gebucht werden müssen.  
- Wenn Artikel aus dem Lagerbestand verbraucht werden, spielt es keine Rolle, wann die Einträge in das FA-Istmeldungs Erf.-Journal vorgenommen werden, weil sich das FA-Istmeldungs Erf.-Journal nicht auf diesen Modus des Buchens des Verbrauchs auswirkt.  
- Es können keine Verbindungscodes festgelegt werden.  

Das "Vorwärts"-Buchen eines gesamten Auftrags ist für Fertigungsumgebungen mit folgenden Eigenschaften geeignet:  

-   Es gibt nur wenige Defekte.  
-   Es gibt nur wenige Arbeitsgänge.  
-   Es gibt einen hohen Komponentenverbrauch in frühen Arbeitsgängen.  

#### <a name="automatic-reporting---forward-flushing-by-operation"></a>Automatisches Berichtswesen - "Vorwärts"-Buchen pro Arbeitsgang  
Buchen pro Arbeitsgang versetzt Sie in die Lage, den Lagerbestand zu aktualisieren, während ein bestimmter Arbeitsgang aus dem Arbeitsplan des übergeordneten Artikels ausgeführt wird. Die Materialien sind mit dem Arbeitsplan über Verbindungscodes verknüpft, die den Verbindungscodes entsprechen, die auf Komponenten in der Fertigungsstückliste angewendet werden.  

Die Buchung erfolgt, wenn der Arbeitsgang gestartet wurde, der denselben Verbindungscode hat. Gestartet bedeutet, dass mindestens eine Aktivität im FA-Istmeldungs Erf.-Journal des Arbeitsgangs erfasst wurde. Diese Aktivität kann z. B. lediglich darin bestehen, dass eine Rüstzeit eingegeben wird.  

Die Mengenangabe für die Buchung ergibt sich aus der Menge pro Stück, die in der Fertigungsstückliste angegeben ist, multipliziert mit der Anzahl der übergeordneten Artikel, die gefertigt werden (erwartete Menge).  

Diese Methode ist am besten geeignet, wenn es viele Arbeitsgänge gibt und bestimmte Komponenten erst spät im Fertigungsablauf benötigt werden. Tatsächlich kann es sein, dass bei einer JIT-Einrichtung (Just-in-Time) die Artikel noch nicht einmal verfügbar sind, wenn die Neuplanung des Fertigungsauftrags gestartet wird.  

Materialien können im Verlauf von Arbeitsgängen verbraucht werden, indem Verbindungscodes verwendet werden. Einige Komponenten werden möglicherweise erst bei den Endmontagearbeitsgängen benötigt und sollten bis dahin nicht aus dem Lager entnommen werden.  

#### <a name="automatic-reporting---back-flushing-by-operation"></a>Automatisches Berichtswesen - "Rückwärts"-Buchen pro Arbeitsgang  
Beim "Rückwärts"-Buchen pro Arbeitsgang wird der Verbrauch erfasst, nachdem der Arbeitsgang im FA-Istmeldungs Erf.-Journal gebucht wurde.  

Der Vorteil dieser Methode liegt darin, dass die Anzahl der übergeordneten Teile, die im Arbeitsgang fertig gestellt wurden, bekannt ist.  

Material in der Fertigungsstückliste ist über Verbindungscodes mit den Arbeitsplandatensätzen verbunden. Die "Rückwärts"-Buchung erfolgt, wenn ein Arbeitsgang mit einem bestimmten Verbindungscode zusammen mit einem fertigen Teil gebucht wird.  

Die Mengenangabe für die Buchung ergibt sich aus der Menge pro Stück, die in der Fertigungsstückliste angegeben ist, multipliziert mit der Zahl der übergeordneten Artikel, die für diesen Arbeitsgang als fertig gestellte Menge gebucht wurden. Diese Mengenangabe kann von der erwarteten Menge unterscheiden.  

#### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Automatisches Berichtswesen - "Rückwärts"-Buchen des gesamten Auftrags  
Bei dieser Berichterstellungsmethode werden keine Verbindungscodes berücksichtigt.  

Komponenten werden erst entnommen, wenn sich der Status des freigegebenen Fertigungsauftrags in *Beendet* geändert hat. Die Mengenangabe für die Buchung ergibt sich aus der Menge pro Stück, die in der Fertigungsstückliste angegeben ist, multipliziert mit der Zahl der übergeordneten Artikel, die fertig gestellt und in den Lagerbestand übernommen wurden.  

Soll ein gesamter Fertigungsauftrag nach der Methode "Rückwärts" gebucht werden, ist die gleiche Einrichtung wie für die Buchungsmethode "Vorwärts" erforderlich: Die Berichterstellungsmethode muss auf jeder Artikelkarte auf "Rückwärts" festgelegt sein, damit alle Artikel in der übergeordneten Stückliste bei der Berichterstellung berücksichtigt werden. Ausserdem müssen alle Verbindungscodes aus der Produktionsstückliste entfernt worden sein.  

### <a name="production-output"></a>Fertig produzierte Artikel (Istmeldungen)  
Die Anwendung gibt Ihnen die Möglichkeit nachzuverfolgen, wie viel Zeit für das Abarbeiten eines Fertigungsauftrags benötigt wurde, zusätzlich zur Aufzeichnung der produzierten Menge. Mit diesen Informationen können Sie die Fertigungskosten genauer bestimmen. Ausserdem kann es sein, dass Hersteller, die ein standardmässiges Kostenrechnungssystem verwenden, die tatsächlichen Informationen erfassen möchten, damit sie genauere Standards entwickeln können.  

Die Istmeldung kann über das FA-Istmeldungs Erf.-Journal verarbeitet, können aber auch automatisch erfasst werden. Beim Berechnen kopiert die Anwendung die Buchungsmethode von der Arbeitsplatz- oder Arbeitsplatzgruppenkarte in den FA-Arbeitsplan kopiert. Wie beim Materialverbrauch gibt es auch für Istmeldungen drei Berichterstellungsmethoden:  

- "Manuell"  
- Vorwärts  
- "Rückwärts"  

Bei der manuellen Methode wird das FA-Verb. Erfassungsjournal verwendet, um die benötigte Zeit und die gefertigte Menge anzugeben.  

Bei der Methode "Vorwärts" wird die Soll-Menge (und die Zeit) erfasst, die automatisch bei der Freigabe eines Fertigungsauftrags erfasst wird. Verbindungscodes spielen beim "Vorwärts"-Buchen der Soll-Menge (Istmeldungen) keine Rolle.  

Bei der Methode "Rückwärts" wird die Soll-Menge (und die Zeit) erfasst, die automatisch am Ende eines Fertigungsauftrags erfasst wird. Verbindungscodes spielen beim "Rückwärts"-Buchen der Soll-Menge (Istmeldungen) keine Rolle.  

### <a name="posting-consumption-and-output"></a>Verbrauch und Istmeldungen buchen  
Sie können sowohl für Verbrauch als auch für Istmeldungen beliebige Kombinationen aus automatischem Buchen und manuell erfassten Informationen verwenden. Beispielsweise kann es sein, dass Sie Komponenten automatisch mit der Methode "Vorwärts" buchen, Ausschuss aber weiterhin mit dem FA-Verbrauchs Erf.-Journal erfassen möchten. In gleicher Weise möchten Sie möglicherweise Istmeldungen automatisch erfassen, aber das FA-Istmeldungs Erf.-Journal dazu verwenden, Ausschuss des übergeordneten Artikels oder zusätzlich für den Auftrag benötigte Zeit zu erfassen.  

Wenn Sie Verbrauch und Istmeldungen manuell eingeben, müssen Sie die Reihenfolge festlegen, in der diese Informationen erfasst werden sollen. Sie können den Verbrauch zuerst erfassen und zum Eingeben der Istmeldungen eine Schnellmethode verwenden, die auf der erwarteten Menge für die Istmeldungen basiert. Sie können aber auch zuerst die Istmeldungen mit der Funktion **Arbeitsplan auflösen** eingeben. Anschliessend müssen Sie den Verbrauch anhand der tatsächlichen Mengen der Istmeldungen erfassen.  

### <a name="production-journal"></a>Produktions Erfassungsjournal  
Im Produktions Erf.-Journal werden die Funktionen des FA-Verbrauchs Erf.-Journals und des FA-Istmeldungs Erf.-Journals in einem Erfassungsjournal kombiniert, auf das direkt vom freigegebenen Fertigungsauftrag aus zugegriffen werden kann.  

Der Sinn des Produktions Erf.-Journal besteht darin, eine einzelne Oberfläche bereitzustellen, über die Sie den Verbrauch und die Istmeldungen eines Fertigungsauftrags erfassen können.  

Das Produktions Erf.-Journal hat eine einfache Ansicht und bietet Ihnen folgende Möglichkeiten:  

- Einfaches Erfassen von Istmeldungen und Verbrauch hinsichtlich eines Fertigungsauftrags  
- Verbinden der Komponenten mit Arbeitsgängen  
- Verbinden der tatsächlichen Arbeitsgangsdaten mit den Standardschätzungen in den Arbeitsplanzeilen des Fertigungsauftrags und in den Komponentenzeilen  
- Buchen und Drucken einer Übersicht der registrierten Arbeitsgangsdaten für den Fertigungsauftrag  

Das Produktions Erf.-Journal erfüllt viele derselben Funktionen wie das FA-Verbrauchs Erf.-Journal und das FA-Istmeldungs Erf.-Journal. Dimensionen, Artikeltracking und Lagerplatzinhalte werden auf dieselbe Weise verwaltet wie auf dem FA-Verbrauchs Erf.-Journal und dem FA-Istmeldungs Erf.-Journal.  

In den folgende Punkten unterscheidet sich das Produktions Erf.-Journal aber vom FA-Verbrauchs Erf.-Journal und FA-Istmeldungs Erf.-Journal:  

- Es wird direkt aus einer Zeile eines freigegebenen Fertigungsauftrags aufgerufen und mit den relevanten Daten voreingestellt.  
- Es versetzt Sie in die Lage, über einen Buchungsmethodenfilter auf dem Erf.-Journal zu definieren, welche Arten von Komponenten bearbeitet werden sollen.  
- Mengen und Zeiten, die bereits für den Auftrag gebucht wurden, werden im unteren Bereich des Erf.-Journals als Posten angezeigt.  
- Felder, für die Dateneingaben unwichtig sind, sind leer und nicht editierbar.  
- Der Benutzer kann einrichten, wie fertig gestellte Mengen im Erf.-Journal voreingestellt werden - beispielsweise kann er festlegen, dass die "Fertig gestellte Menge" für den letzten Arbeitsgang gleich Null sein muss.  
- Sollten Sie versuchen, das Erf.-Journal zu beenden, ohne die vorgenommenen Buchungen gespeichert zu haben, wird eine Bestätigungsmeldung angezeigt, die Ihnen den Verbleib im Erf.-Journal ermöglicht.  
- Arbeitsgänge und Komponenten werden zusammen in einer logischen Struktur angezeigt, die einen Überblick über den Fertigungsprozess bereitstellt.  

Im Produktions Erf.-Journal werden Verbrauchsmengen als negative Lagerposten, fertig gestellte Mengen als positive Posten und benötigte Zeiten als Kapazitätsposten gebucht.  

## <a name="see-also"></a>Siehe auch
[Bearbeitungen](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbesttand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
