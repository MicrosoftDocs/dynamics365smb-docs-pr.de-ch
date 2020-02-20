---
title: Eingeben von Daten in Business Central | Microsoft Docs
description: Informationen zu allgemeinen Funktionen, die Ihnen dabei helfen, Daten in die Felder einzugeben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/27/2020
ms.author: sgroespe
ms.openlocfilehash: 6a57af4a29e2b355dfe3f261a5d83fade992551d
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992110"
---
# <a name="entering-data"></a>Eingeben von Daten

Es gibt eine Vielzahl allgemeiner Funktionen, die Ihnen dabei helfen, die Daten einfacher, schneller und genaueren einzugeben. Die allgemeinen Funktionen für die Eingabe von Daten werden alle in diesem Artikel beschrieben.  

Die Beispiele in diesen Artikel verwendet die Demodaten.

## <a name="keyboard-shortcuts"></a>Tastenkombinationen

Es gibt mehrere Tastenkombinationen, mit denen Sie ohne Maus arbeiten und Ihre Dateneingabe beschleunigen können, insbesondere bei Posten im grossen Umfangs und wiederkehrenden Tippaufgaben.

Weitere Informationen zu diesen Tastenkombinationen finden Sie unter [Tastenkombinationen](keyboard-shortcuts.md). Einige der Tastenkombinationen werden in diesem erläutert Artikel.

## <a name="QuickEntry"></a>Beschleunigende der Dateneingabe mithilfe der Schnelleingabe

Die Schnelleingabe ist eine Funktion für die Dateneingabe bei Verwendung der Tastatur. Schnelleingabe funktioniert bei Feldern (wie in Kartenseiten) und in Listen (Zeilen und Spalten). Sie ist bei der Durchführung wiederkehrende Tippaufgaben hilfreich, die mehrere Datensätze nacheinander erfordern, wie ein Stapel von Verkaufsaufträgen oder der Registrierung neuer Artikel.

Sie sind möglicherweise bereits mit der Anwendung die TAB-TASTE vertraut, um von einem Feld einer Seite zum nächsten bearbeitbaren Feld zu navigieren. Der Nachteil der Anwendung von TAB ist, dass sie stets fortlaufend zum nächsten Feld navigiert. <!-- even if the field is non-editable or seldom filled it in.-->Mit Schnelleintrag können Sie den Pfad ändern. Mit Schnelleintrag verwenden Sie ENTER, um nur durch diejenigen Felder zu navigieren, an den Sie interessiert sind, und Sie überspringen die nicht-bearbeitbaren Felder und Felder, die Sie üblicherweise nicht ausfüllen. Sie haben dieses Verhalten möglicherweise bereits auf einigen Seiten bemerkt. Der Grund ist, dass die Anwendung bereits festlegt, welche Felder eingeschlossen werden, wenn die Eingabetaste gedrückt wird und welche Felder übersprungen werden. Sie können die Schnelleingabe anpassen, indem Sie den Arbeitsbereich personalisieren und optimieren, wie Sie Daten auf jeder Seite eingeben.

### <a name="how-quick-entry-works"></a>So funktioniert die Schnelleingabe

Jedes Feld kann als *in Schnelleingabe enthalten* oder *aus Schnelleingabe ausgeschlossen* markiert werden. Felder, die in der Schnelleingabe enthalten sind, sind im Pfad enthalten, wenn Sie ENTER drücken; Felder, die aus der Schnelleingabe ausgeschlossen sind, nicht.

Wenn Sie die Dateneingabe in einem Feld beendet haben, drücken Sie einfach ENTER, um die Änderungen zu bestätigen und zum nächsten Feld zu wechseln. Wenn Sie die Richtung umkehren und zum vorherigen Feld gehen möchten, drücken SHIFT+ENTER. Weitere Informationen zu diesen Tastenkombinationen unter [Tastenkombinationen der Schnelleingabe für Felder](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Tipps und Tricks
Es folgen einige nützliche Informationen zur Anwendung der Schnelleingabe.

- Sie ist für alle bearbeitbaren Felder verfügbar.
- Sie funktioniert auch über Spalten und Zeilen hinweg.
- Sie verhindert nicht den Zugriff auf andere Elemente einer Seite wie Aktionen. Auf diese kann noch mit TAB und SHIFT+TAB zugegriffen werden.  
- Inforegister müssen nicht erweitert werden, damit die Schnelleingabe funktioniert. Wenn sich das nächste Feld der Schnelleingabe in einem reduzierten Inforegister befindet, wird das Inforegister automatisch mit Fokus auf dem festgelegten Feld erweitert.
- Schnelleingabe funktioniert ungeachtet davon, ob Felder erforderlich sind. Daher ist es vorteilhaft, sicherzustellen, dass erforderliche Felder in der Schnelleingabe enthalten sind.
- Standardmässig sind die meisten Felder automatisch im der Schnelleingabe enthalten. Daher wird die Aufgabe höchstwahrscheinlich zunächst darin bestehen, Felder aus der Schnelleingabe auszuschliessen.

### <a name="to-change-quick-entry-fields"></a>Um Felder der Schnelleingabe zu ändern

Um zu ändern, welche Felder einer Seite in die Schnelleingabe eingeschlossen oder daraus ausgeschlossen werden, verwenden Sie die Personalisierung.

1. Beginnen Sie mit der Personalisierung, indem Sie das Symbol ![Einstellungen](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollencenter") und dann die Aktion **Personalisieren** auswählen.
2. Wählen Sie ein Feld, das Sie ändern möchten, oder wählen Sie in Listen die entsprechende Spaltenüberschrift und dann entweder **In Schnelleingabe einschliessen** oder **Aus Schnellausgabe ausschliessen** aus.

Weitere Informationen zur Personalisierung finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Pflichtfelder

Wenn Sie Daten auf Seiten in eingeben, werden bestimmte Felder mit einem roten Sternchen markiert. Das rote Sternchen bedeutet, dass das Feld ausgefüllt werden muss, um einen bestimmten Prozess, der das Feld verwendet, abzuschliessen (Beispiel: Buchung einer Transaktion, die den Wert in dem Feld verwendet).  

Selbst wenn das Feld ein rotes Sternchen enthält, sind Sie nicht gezwungen, das Feld auszufüllen, bevor Sie mit anderen Feldern fortfahren oder die Seite schliessen. Das rote Sternchen dient nur als Erinnerung, dass Sie am Beenden eines bestimmten Prozesses gehindert werden.  

## <a name="finding-data-as-you-type"></a>Suchen von Daten bei der Eingabe

 Wenn Sie mit der Eingabe von Zeichen in einem Feld beginnen, wird eine Dropdownliste mit möglichen Feldwerten angezeigt. Die Anzeige der Dropdownliste ändert sich bei Eingabe weiterer Zeichen, und Sie können den korrekten Wert auswählen, wenn dieser angezeigt wird.  

 Viele Felder haben eine Schaltfläche mit einem nach unten zeigenden Pfeil, den Sie auswählen können. Durch Klicken auf diesen Pfeil wird eine Liste der Daten angezeigt, die in das Feld eingegeben werden können. Die Schaltfläche bietet abhängig vom Feldtyp zwei Funktionen:  

-   Lookup – Zeigt Informationen aus einer anderen Tabelle an, die im Feld eingegeben werden können. Es kann jeweils ein Datenelement ausgewählt werden.  

-   Dropdown – Zeigt die Optionen an, die für das Feld verfügbar sind. Sie können nur eine der Optionen auswählen.  

## <a name="copying-and-pasting-faq-fields-and-lines"></a>FAQ Felder und Zeilen kopieren und einfügen

Sie können eine oder mehrere Zeilen aus einer Liste oder einem einzelnen Feld auf einer Seite kopieren und die kopierten Daten dann auf der gleichen Seite, einer andere Seite oder einem externen Beleg (wie Microsoft Excel und Outlook-E-Mail) einfügen. Kurz gesagt, zum Kopieren drücken Sie CTRL+C (cmd+C in Mac Os) auf Ihrer Tastatur. Zum Einfügen drücken Sie CTRL+V (cmd+V in Mac Os).

Um das Feld in einer Liste in der gleichen Spalte der Zeile darüber zu kopieren, und es in die aktuelle Zeile einzufügen, drücken Sie einfach F8.

Weitere Informationen finden Sie unter [FAQ zum Kopieren und Einfügen](ui-copy-paste.md).

## <a name="filtering-line-items"></a>Filtern von Positionsartikel

Um mit dem Filtern zu beginnen, wählen Sie ![Filterbereichssymbol](media/open-filter-pane-icon.png "Filterbereichssymbol") in der Liste oben aus, oder drücken Sie auf Shift+F3, um den Filterbereich zu öffnen. Sie arbeiten mit Filterbereich, wie in jeder anderen Liste. Weitere Informationen finden Sie unter [Filterung](ui-enter-criteria-filters.md#Filtering).

Filterung ist besonders dann von Nutzen, wenn längere Belege anzeigt und analysiert werden. Stellen Sie sich beispielsweise vor, dass Sie eine gebuchte Verkaufsrechnung öffnen und filtern, dass alle Positionsartikel mit einem Einzelrabatt von 5 % haben, oder Sie filtern, dass nur Fahrradzubehör mit "Pro" im Namen angezeigt wird.

## <a name="Focus"></a>Fokussieren auf Positionsartikel

Wenn Sie an Belegen arbeiten, die einen Zeilenartikelteil enthalten, z. B. eine Kundenauftrags- oder Rechnungsseite, können Sie die Ansicht so ändern, dass nur die Werbebuchungen angezeigt werden. Der Zeilenartikelbereich wird dann so erweitert, dass er fast den gesamten Arbeitsbereich einnimmt und andere Teile der Seite mit Ausnahme des Aktionsbereichs oben verbirgt. Damit erhalten Sie einen besseren Überblick über die Positionsartikel und mehr Platz, um daran zu arbeiten.

Dies ist besonders nützlich, wenn Sie mit grossen Positionsartikellisten arbeiten und eine schnelle Dateneingabe erforderlich ist. Ein anderer Vorteil besteht darin, dass auch erweiterte Filterungsfunktion, wie auf anderen Listen, bereitgestellt werden, sodass Durchsuchen und Suchen nach Belegpositionen sogar einfacher wird.

### <a name="switching-the-focus-on-and-off"></a>Den Fokus zwischen An- und Ausschalten wechseln

Um sich auf Zeilenartikel zu konzentrieren, wählen Sie irgendeine Stelle im Bereich des Zeilenartikelteils aus und wählen Sie dann das ![Fokusmodussymbol](media/focus-mode.png "Fokusmodus-Symbol") in der oberen rechten Ecke aus, oder drücken Sie Ctrl+Shift+F12.

Um zur Normalansicht zurückzukehren, wählen Sie das ![Fokusmodussymbol](media/focus-mode.png "Fokusmodus-Symbol") aus, oder drücken Sie Ctrl+Shift+F12 erneut.

## <a name="multitasking-across-multiple-pages"></a>Multitasking über mehrere Seiten
Wenn Sie an mehreren Aufgaben gleichzeitig arbeiten oder Unterbrechungen der aktuellen Aufgabe verwalten, z. B. einen eingehenden Anruf entgegennehmen, können Sie eine Karten- oder Belegseite in einem neuen Fenster öffnen. Auf diese Weise können Sie ein Fenster für eine laufende Aufgabe geöffnet lassen, während Sie eine andere Aufgabe in einem oder mehreren anderen Fenstern starten oder abschliessen.

Um die aktuelle Karte oder den aktuellen Beleg in einem neuen Fenster zu öffnen, wählen Sie ![Neues Fenster öffnen](media/open-new-window-icon.png "Symbol „Neues Fenster öffnen“") öffnen in der oberen rechten Ecke, oder drücken Sie Alt + Shift+W.

> [!NOTE]
> Wenn Sie andere Seiten von einer Karte oder einem Beleg aus öffnen, die bzw. der in einem neuen Fenster geöffnet wird, werden diese Seiten in einem neuen Fenster geöffnet, auch wenn nicht ![Neues Fenster öffnen](media/open-new-window-icon.png "Symbol „Neues Fenster öffnen“") wählen.

> [!NOTE]
> Wenn Sie im Safari-Browser arbeiten, kann ein Popupblocker dazu führen, dass das neue Fenster nicht geöffnet wird. In diesem Fall geben Sie die Produkt-URL als zulässige Website an. Weitere Informationen finden Sie unter [Ändern Sie die Einstellungen in Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Das Gleiche kann in anderen Browsern wie Firefox passieren. Weitere Informationen finden Sie unter [Popupblocker-Einstellungen in Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400).  

## <a name="entering-quantities-by-calculation"></a>Eingeben von Mengen durch Berechnung

Beim Eingeben von Zahlen in die Mengenfelder, beispielsweise in das Feld **Menge** in einer Artikel Erf.-Journalzeile, kann anstelle der Summenmenge die Formel eingegeben werden.  

### <a name="examples"></a>Beispiele  

-   Bei Eingabe von 19+19 wird im Feld als Wert 38 angezeigt.  

-   Bei Eingabe von 41-9 wird im Feld als Wert 32 angezeigt.  

-   Bei Eingabe von 12*4 wird im Feld als Wert 48 angezeigt.  

-   Bei Eingabe von 12/4 wird im Feld als Wert 3 angezeigt.  

## <a name="entering-negative-numbers"></a>Eingeben von negativen Zahlen

Sie können negative Zahlen auf zwei Arten eingeben. Die Zahl. -20,5 kann so eingegeben werden:  

-   -20.5  

    Oder
-   20.5-  

 In beiden Fällen wird der Betrag als -20,5 erfasst.  

 Wenn das letzte Zeichen des Ausdrucks **+** oder **-** ist, wird der gesamte Ausdruck mit diesem Vorzeichen erfasst. Ein Beispiel, **10-20+** ergibt 10 und nicht -10.  

## <a name="entering-dates-and-times"></a>Daten und Zeit eingeben

Datums- und Uhrzeitwerte können in alle Felder eingegeben werden, die speziell für Datumswerte vorgesehen sind (Datumsfelder). Datumswerte können mit oder ohne Trennzeichen eingegeben werden.

> [!NOTE]  
> Wie Sie Daten und Uhrzeiten eingeben, hängt von Ihren Einstellungen in Ihrer**Region** ab. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Eingeben von Datumswerten

Für Datumsfelder können Sie die Datenauswahl verwenden, mit der Sie ein Datum aus einem Kalender auswählen können, oder Sie können Datumswerte manuell eingeben. Dieser Abschnitt bietet eine kurze Übersicht über die Dateneingabe. Weitere Informationen finden Sie unter [Arbeiten mit Datumsangaben und Uhrzeiten in Kalendern](ui-enter-date-ranges.md).

Für manuelle Eingaben von Datumsangaben können zwei-, vier-, sechs- oder achtstellige Werte eingegeben werden:  

-   Wenn Sie nur zwei Ziffern eingeben, wird dies als Tagesangabe interpretiert, es gilt also der Monat und das Jahr des Arbeitsdatums.  

-   Wenn Sie vier Ziffern eingeben, wird dies als Tages- und Monatsangabe interpretiert, es gilt also das Jahr des Arbeitsdatums.  

-   Wenn Sie ein Datum zwischen dem 01.01.1930 und dem 31.12.2029 eingeben wollen, können Sie das Jahr zweistellig eingeben; ansonsten sollten Sie das Jahr vierstellig angeben.  

Sie können auch einen Wochentag gefolgt von einer Kalenderwoche (und optional einer Jahresangabe) für das Datum verwenden. So steht beispielsweise "mo25" oder "Mo25" für den Montag in der 25. Kalenderwoche.  

Anstatt ein bestimmtes Datum direkt einzugeben, können Sie auch einen dieser Codes verwenden.  

|Code|Ergebnis|  
|--------------|----------------|  
|h|Dies gibt das heutige Datum (das Systemdatum des Computers) an.|  
|p|Dies gibt eine Buchhaltungsperiode an, wobei P die erste Buchhaltungsperiode bezeichnet, P2 die zweite Buchhaltungsperiode angibt usw. |
|a|Dies gibt das Arbeitsdatum an, das in der Anwendung eingerichtet wird. Um das Arbeitsdatum zu ändern, siehe [Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md). Die Verwendung des Arbeitsdatums ist hilfreich, wenn eine Vielzahl von Transaktionen zu einem Datum ausgeführt werden müssen, das vom Systemdatum abweicht.|
|a|Gibt an, dass das Datum nach A ein Abschlussdatum ist, beispielsweise A31.12.01.|  

## <a name="entering-times"></a>Eingeben von Uhrzeiten

Beim Eingeben von Uhrzeiten kann zwischen den Zeiteinheiten ein beliebiges Trennzeichen (oder auch kein Trennzeichen) verwendet werden. Die Angabe von Minuten, Sekunden oder AM/PM ist nicht erforderlich.  

In der folgenden Tabelle finden Sie eine Liste über die Möglichkeiten zum Angeben von Uhrzeiten sowie die Interpretation der jeweiligen Angabe.  

|Eingabe|Interpretation|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5,50|05:30:05,5|  
|053005050|05:30:05.05|  

 Sie müssen für jede Zeiteinheit, die Sie eintragen, zwei Zeichen eingeben, wenn Sie kein Trennzeichen verwenden.  

## <a name="entering-datetimes"></a>Datums-/Uhrzeitangaben eingeben

Wenn Sie eine Datum-/Zeiteingabe eingeben, müssen Sie zwischen dem Datum und der Zeiteingabe einen Leerschritt einfügen.  

In der folgenden Tabelle finden Sie eine Liste über die Möglichkeiten zum Eingeben von Datums-/Uhrzeitangaben sowie die Interpretation der jeweiligen Angabe.  

|Eingabe|Interpretation|  
|---------------|------------------------|  
|`131202` 132455|13.12.02 13:24:55|  
|1-12-02 10|01.12.02 10:00:00|  
|1.12.02 5|01.12.02 05:00:00|  
|1.12.02|01.12.02 00:00:00|  
|11 12|11.aktueller Monat.aktuelles Jahr 12:00:00|  
|1112 12|11.12.aktuelles Jahr 12:00:00|  
|h für heute|heutiges Datum 00:00:00|  
|t Zeit|heutiges Datum aktuelle Zeit|  
|h 10:30|heutiges Datum 10:30:00|  
|h 3:3:3|heutiges Datum 03:03:03|  
|a oder Arbeitsdatum|das Arbeitsdatum 00:00:00|  
|"m" oder "Montag"|Montag der aktuellen Woche 00:00:00|  
|"d" oder "Dienstag"|Dienstag der aktuellen Woche 00:00:00|  
|"mi" oder "Mittwoch"|Mittwoch der aktuellen Woche 00:00:00|  
|"do" oder "Donnerstag"|Donnerstag der aktuellen Woche 00:00:00|  
|"f" oder "Freitag"|Freitag der aktuellen Woche 00:00:00|  
|"s" oder "Sonnabend"|Samstag der aktuellen Woche 00:00:00|  
|"so" oder "Sonntag"|Sonntag der aktuellen Woche 00:00:00|  
|di 10:30|Dienstag der aktuellen Woche 10:30:00|  
|d 3:3:3|Dienstag der aktuellen Woche 03:03:03|  

## <a name="entering-duration"></a>Eingeben von Terminen
Sie können Zeitdauern als Zahl gefolgt von der entsprechenden Einheit eingeben.  

Hier folgen einige Beispiele.  

|Termine|Masseinheit**|  
|------------------|-------------------------|  
|2h|2 Stunden|  
|6h 30m|6 Stunden 30 Minuten|  
|6,5h|6 Stunden 30 Minuten|  
|90m|1 Stunde 30 Minuten|  
|2d 6h 30m|2 Tage 6 Stunden 30 Minuten|  
|2d 6h 30m 56s 600ms|2 Tage 6 Stunden 30 Minuten 56 Sekunden 600 Millisekunden|  

 Sie haben auch die Möglichkeit, eine Zahl einzugeben, die dann automatisch in einen Zeitraum umgewandelt wird. Die Zahl, welche Sie eingeben, wird entsprechend der Vorgabeeinheit, die Sie für das Dauer-Feld definiert haben, konvertiert.  

 Geben Sie zum Ermitteln der Einheit, die für ein Feld vom Typ "Dauer" verwendet wird, eine Zahl ein. Am Ergebnis können Sie ablesen, in welche Einheit diese konvertiert wird.  

 Die Zahl 5 wird in 5 h konvertiert, wenn Stunden als Einheit angegeben wurden.  

## <a name="see-also"></a>Siehe auch  
 [Sortieren, Durchsuchen und Filtern von Listen](ui-enter-criteria-filters.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
