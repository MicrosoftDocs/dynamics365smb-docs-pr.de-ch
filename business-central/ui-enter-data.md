---
title: Wie Sie Daten in die Felder ein| Microsoft Docs
description: "Es gibt eine Vielzahl an allgemeinen Funktionen, die Ihnen dabei helfen, Daten schnell und einfach einzugeben. Die allgemeinen Funktionen für die Eingabe von Daten werden in diesem Thema beschrieben."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 4354e28522d359cf9fa6178c4a1919831dcc52db
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---

# <a name="entering-data"></a>Eingeben von Daten
Es gibt eine Vielzahl an allgemeinen Funktionen, die Ihnen dabei helfen, Daten schnell und einfach einzugeben. Die allgemeinen Funktionen für die Eingabe von Daten werden alle in diesem Artikel beschrieben.  

Die Beispiele in diesen Artikel verwendet die Demodaten.

## <a name="mandatory-fields"></a>Pflichtfelder
Wenn Sie Daten auf Seiten in eingeben, werden bestimmte Felder mit einem roten Sternchen markiert. Das rote Sternchen bedeutet, dass das Feld ausgefüllt werden muss, um einen bestimmten Prozess, der das Feld verwendet, abzuschliessen (Beispiel: Buchung einer Transaktion, die den Wert in dem Feld verwendet).  

Selbst wenn das Feld ein rotes Sternchen enthält, sind Sie nicht gezwungen, das Feld auszufüllen, bevor Sie mit anderen Feldern fortfahren oder die Seite schliessen. Das rote Sternchen dient nur als Erinnerung, dass Sie am Beenden eines bestimmten Prozesses gehindert werden.  


## <a name="finding-data-as-you-type"></a>Suchen von Daten bei der Eingabe  
 Wenn Sie mit der Eingabe von Zeichen in einem Feld beginnen, wird eine Dropdownliste mit möglichen Feldwerten angezeigt. Die Anzeige der Dropdownliste ändert sich bei Eingabe weiterer Zeichen, und Sie können den korrekten Wert auswählen, wenn dieser angezeigt wird.  

 Viele Felder haben eine Schaltfläche mit einem nach unten zeigenden Pfeil, den Sie auswählen können. Durch Klicken auf diesen Pfeil wird eine Liste der Daten angezeigt, die in das Feld eingegeben werden können. Die Schaltfläche bietet abhängig vom Feldtyp zwei Funktionen:  

-   Lookup – Zeigt Informationen aus einer anderen Tabelle an, die im Feld eingegeben werden können. Es kann jeweils ein Datenelement ausgewählt werden.  

-   Dropdown – Zeigt die Optionen an, die für das Feld verfügbar sind. Sie können nur eine der Optionen auswählen.  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards in the **Items** page, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a>Eingeben von Mengen durch Berechnung  
 Beim Eingeben von Zahlen in die Mengenfelder, beispielsweise in das Feld **Menge** in einer Artikel Erfassungsjournalzeile, kann anstelle der Summenmenge die Formel eingegeben werden.  

## <a name="examples"></a>Beispiele  

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
> Wie Sie Daten und Uhrzeiten eingeben, hängt von Ihren Einstellungen in Ihrer**Region** ab. Weitere Informationen finden Sie unter [Ändern von Grundeinstellungen](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Datumswerte eingeben  
 In einem Datumsfeld können zwei-, vier-, sechs- oder achtstellige Werte eingegeben werden:  

-   Wenn Sie nur zwei Ziffern eingeben, wird dies als Tagesangabe interpretiert, es gilt also der Monat und das Jahr des Arbeitsdatums.  

-   Wenn Sie vier Ziffern eingeben, wird dies als Tages- und Monatsangabe interpretiert, es gilt also das Jahr des Arbeitsdatums.  

-   Wenn Sie ein Datum zwischen dem 01.01.1930 und dem 31.12.2029 eingeben wollen, können Sie das Jahr zweistellig eingeben; ansonsten sollten Sie das Jahr vierstellig angeben.  

 Sie können auch einen Wochentag gefolgt von einer Kalenderwoche (und optional einer Jahresangabe) für das Datum verwenden (z. B. steht mo25 oder Mo25 für den Montag in der 25. Kalenderwoche).  

 Anstatt ein bestimmtes Datum direkt einzugeben, können Sie auch einen der zwei folgenden Codes verwenden.  

|Code|Ergebnis|  
|--------------|----------------|  
|h|Dies ist das heutige Datum (das Systemdatum des Computers).|  
|a|Dies ist das Arbeitsdatum, die in der Anwendung eingerichtet wird. Um das Arbeitsdatum zu ändern, siehe [Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md). Das Arbeitsdatum ist nützlich, wenn Sie viele Transaktionen unter einem anderen als dem aktuellen Systemdatum durchführen müssen.|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a>Uhrzeiten eingeben  
 Beim Eingeben von Uhrzeiten kann zwischen den Zeiteinheiten ein beliebiges Trennzeichen (oder auch kein Trennzeichen) verwendet werden. Die Angabe von Minuten, Sekunden oder AM/PM ist nicht erforderlich.  

 In der folgenden Tabelle finden Sie eine Liste über die Möglichkeiten zum Angeben von Uhrzeiten sowie die Interpretation der jeweiligen Angabe.  

|Eingabe|Interpretation|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5,50|05:30:050,5|  
|053005050|05:30:05.05|  

 Sie müssen für jede Zeiteinheit, die Sie eintragen, zwei Zeichen eingeben, wenn Sie kein Trennzeichen verwenden.  

## <a name="entering-datetimes"></a>Datums-/Uhrzeitangaben eingeben  
 Wenn Sie eine Datum-/Zeiteingabe eingeben, müssen Sie zwischen dem Datum und der Zeiteingabe einen Leerschritt einfügen.  

 In der folgenden Tabelle finden Sie eine Liste über die Möglichkeiten zum Eingeben von Datums-/Uhrzeitangaben sowie die Interpretation der jeweiligen Angabe.  

|Posten|Interpretation|  
|---------------|------------------------|  
|131202 132455|13-12-02 13:24:55|  
|1-12-02 10|01-12-02 10:00:00|  
|1.12.02 5|01-12-02 05:00:00|  
|1.12.02|01-12-02 00:00:00|  
|11 12|11-aktueller Monat-aktuelles Jahr 12:00:00|  
|1112 12|11-12-aktuelles Jahr 12:00:00|  
|h für heute|heutiges Datum 00:00:00|  
|h Zeit|heutiges Datum aktuelle Zeit|  
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

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a>Datumsformeln verwenden  
 Bei einer Datumsformel handelt es sich um eine verkürzte Kombination aus Buchstaben und Zahlen, die zum Berechnen von Datumswerten verwendet wird. Datumsformeln können in verschiedenen Datumsberechnungsfeldern sowie in Felder vom Typ "Wiederholungsrate" (in wiederkehrenden Erf.-Journalen) eingeben werden.  

> [!NOTE]  
>  In allen Formelfeldern wird automatisch ein Tag aufgenommen, um den heutigen Tag als den Tag abzudecken, an dem die Periode beginnt. Wenn Sie beispielsweise "1W" eingeben, ist die Periode tatsächlich acht Tage, da der heutige Tag enthalten ist. Um eine Periode von sieben Tagen (tatsächlich eine Woche) einschliesslich des Periodenstartdatums anzugeben, müssen Sie "6D" oder "1W-1D" eingeben.  

 Nachfolgend einige Beispiele wie Datumsformeln eingesetzt werden können:  

-   Die Datumsformel im Feld "Wiederholungsrate" in wiederkehrenden Journalen bestimmt, wie oft der Posten in der Journalzeile gebucht werden wird.  

-   Die Datumsformel in dem Feld "Toleranzperiode" für eine Mahnstufe bestimmt die Zeit, die vom Fälligkeitsdatum (oder vom Datum der letzten Mahnung) an vergehen muss, bevor eine Mahnung erstellt wird.  

-   Anhand der Datumsformel im Feld Fälligkeitsformel wird die Berechnung des Fälligkeitsdatums auf der Mahnung bestimmt.  

 Die Datumsberechnungsformel kann maximal 20 Zeichen (Buchstaben und Zahlen) enthalten. Für die Berechnungszeiträume können die folgenden Abkürzungen verwendet werden.  

|||  
|-|-|  
|L|Laufend|  
|T|Tag(e)|  
|W|Woche(n)|  
|M|Monat(e)|  
|Q|Quartal(e)|  
|J|Jahr(e)|  

 Datumsformeln können auf drei Arten erstellt werden.  

 Das folgende Beispiel zeigt das aktuelle Datum plus eine Zeiteinheit.  

|||  
|-|-|  
|LW|Laufende Woche|  
|LM|Laufender Monat|  

 Das folgende Beispiel zeigt eine Zahl plus eine Zeiteinheit. Eine Zahl darf nicht grösser sein als 9999.  

|||  
|-|-|  
|10T|10 Tage von heute an|  
|2W|2 Wochen von heute an|  

 Das folgende Beispiel zeigt eine Zeiteinheit plus eine Zahl.  

|||  
|-|-|  
|T10|Am 10. des Monats|  
|WT4|Am 4. Tag einer Woche (Donnerstag)|  

 Das folgende Beispiel zeigt, wie Sie diese drei Formulare nach Bedarf kombinieren können.  

|||  
|-|-|  
|LM+10T|Laufender Monat plus 10 Tage|  

 Das folgende Beispiel zeigt, wie Sie ein Minuszeichen verwenden können, um anzugeben, dass es sich um ein Datum in der Vergangenheit handelt.  

|||  
|-|-|  
|-1J|Heute vor einem Jahr|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a>Siehe auch  
 [Ermitteln, filternd und Sortieren von Daten](ui-enter-criteria-filters.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

