---
title: Abschreibungsmethoden| Microsoft Docs
description: Erhalten von Informationen zu den unterschiedlichen Methoden, um Anlagen abzuschreiben.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a1278b344efef1df243d4f82e9d463f8faf9a259
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920811"
---
# <a name="depreciation-methods"></a>Abschreibungsmethoden
Es gibt acht verfügbare Abschreibungsmethoden:  

* Linear  
* Degressiv 1  
* Degressiv 2  
* Degr1/Linear  
* Degr2/Linear  
* Tabelle  
* Manuell  

  > [!NOTE]  
  >   Sie können diese Methode für Anlagen verwenden, die nicht abgeschrieben werden z. B. Land. Sie müssen die Abschreibung im Anlagen Fibu Erf.-Journal eingeben. Die Stapelverarbeitung **Abschreibung berechnen** berücksichtigt keine Anlagen mit dieser Abschreibungs-Methode.  
* US-Halbjahresregel  

  > [!NOTE]  
  >    Wenn diese Methode verwendet wird, wird eine Anlage jedes Jahr mit dem gleichen Betrag abgeschrieben.  

## <a name="straight-line-depreciation"></a>Lineare Abschreibung
Wenn Sie die Methode "Linear" verwenden, müssen Sie eine der folgenden Optionen im Anlagen-Abschreibungsbuch angeben:  

* Die Nutzungsdauer (in Jahren oder Monaten) oder das Enddatum der Nutzungsdauer.  
* Einen festen jährlichen Prozentsatz  
* Einen festen jährlichen Betrag  
* Abschreibungsperiode  

### <a name="depreciation-period"></a>Abschreibungsperiode
Falls Sie eine Abschreibung Periode angeben (Anzahl der Abschreibung Jahre, Anzahl der Abschreibung Monate oder das Enddatum der Nutzungsdauer), verwendet die Anwendung die folgende Formel, um den Abschreibung Betrag zu berechnen:  

*AfA Betrag = ((Buchwert – Restwert) x Anzahl AfA Tage) / Verbleibende AfA Tage*  

Die verbleibenden Abschreibungstage werden als die Gesamtzahl der Abschreibungstage minus der Anzahl der Tage zwischen dem Startdatum Normal-Abschreibung und dem letzten Anlagen-Buchungsdatum berechnet.  

Der Buchwert kann durch gebuchte Zuschreibungen, AfA, Sonderabschreibungsbeträge oder benutzerdef. Abschr.beträge reduziert werden; abhängig davon, ob das Feld **In AfA-Berechnung enthalten** deaktiviert ist und ob das Feld **Teil d. Buchwerts** auf der Seite **Anlagenbuchungsart Einr.** aktiviert ist. Diese Berechnung stellt sicher, dass die Anlage zum angegebenen Enddatum vollständig abgeschrieben ist.  

### <a name="fixed-yearly-percentage"></a>Fester jährlicher Prozentsatz
Wenn Sie einen festen jährlichen Prozentsatz angeben, verwendet die Anwendung die folgende Formel für die Berechnung des Abschreibungssatzes.  

Abschreibungsbetrag = (Linear % x Abschreibungsbasis x Anzahl Abschreibungstage) / (100 x 360)  

### <a name="fixed-yearly-amount"></a>Fester jährlicher Betrag
Wenn Sie einen festen jährlichen Betrag angeben, verwendet die Anwendung die folgende Formel, um den Abschreibungssatz zu berechnen:  

Abschreibungsbetrag = (Fester Abschreibungsbetrag x Anzahl Abschreibungstage) / 360  

### <a name="example---straight-line-depreciation"></a>Beispiel – Lineare Abschreibung
Eine Anlage hat Anschaffungskosten von MW 100.000. Die erwartete Lebensdauer ist 8 Jahre. Die Stapelverarbeitung **AfA berechnen** wird zweimal jährlich ausgeführt.  

Für dieses Beispiel sieht der Anlagenposten folgendermassen aus:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01.01.10 |Anschaffungskosten |* |100,000.00 |100,000.00 |
| 30.06.10 |Abschreibungen |180 |-6.250,00 |93,750.00 |
| 31.12.10 |Abschreibungen |180 |-6.250,00 |87,500.00 |
| 30.06.11 |Abschreibungen |180 |-6.250,00 |81,250.00 |
| 31.12.11 |Abschreibungen |180 |-6.250,00 |75,000.00 |
| 30.06.17 |Abschreibungen |180 |-6.250,00 |6,250.00 |
| 31.12.17 |Abschreibungen |180 |-6.250,00 |0 |

* Startdatum Normal-Abschreibung  

## <a name="declining-balance-1-depreciation"></a>Abschreibungsmethode "1 % degressiv"
Hierbei handelt es sich um eine beschleunigte Abschreibungsmethode, bei der der grösste Teil der Kosten einer Anlage in den ersten Jahren der Nutzungsdauer abgeschrieben wird. Wenn Sie diese Methode verwenden, müssen Sie einen festen jährlichen Prozentsatz eingeben.  

Die folgende Formel zur Berechnung des Abschreibung-Betrages ist:  

*AfA Betrag = (Degressive AfA % * Anzahl AfA Tage * AfA Basis) / (100 *360)*  

Die Abschreibungsbasis wird als der Buchwert minus der gebuchten Abschreibung seit dem Startdatum des aktuellen Geschäftsjahres berechnet.  

Der gebuchte Abschreibungsbetrag kann Posten mit verschiedenen Buchungsarten enthalten (erhöhte Abschreibung, Sonder-Abschreibung und benutzerdefinierte Abschreibung), die seit dem Startdatum des aktuellen Geschäftsjahrs gebucht worden sind. Diese Buchungsarten sind in dem gebuchten Abschreibung Betrag enthalten, wenn Häkchen in den Feldern **Abschreibungsart** und **Teil d. Buchwerts** auf der Seite **Anlagenbuchungsart Einr.** gesetzt sind.  

### <a name="example---declining-balance-1-depreciation"></a>Beispiel – Abschreibungsmethode "1 % degressiv"
Eine Anlage hat Anschaffungskosten von MW 100.000. Das Feld **Degressive AfA %** hat den Wert 25. Die Stapelverarbeitung **AfA berechnen** wird zweimal jährlich ausgeführt.  

Die nachstehende Tabelle zeigt, wie die Anlagenposten-Einträge aussehen.  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01.01.10 |Anschaffungskosten |* |100,000.00 |100,000.00 |
| 30.06.10 |Abschreibungen |180 |-12.500,00 |87,500.00 |
| 31.12.10 |Abschreibungen |180 |-12.500,00 |75,000.00 |
| 30.06.11 |Abschreibungen |180 |-9.375,00 |65,625.00 |
| 31.12.11 |Abschreibungen |180 |-9.375,00 |56,250.00 |
| 30.06.12 |Abschreibungen |180 |-7.031,25 |49,218.75 |
| 31.12.12 |Abschreibungen |180 |-7.031,25 |42,187.50 |
| 30.06.13 |Abschreibungen |180 |-5.273,44 |36,914.06 |
| 31.12.13 |Abschreibungen |180 |-5.273,44 |31,640.62 |
| 30.06.14 |Abschreibungen |180 |-3.955,08 |27,685.54 |
| 31.12.14 |Abschreibungen |180 |-3.955,08 |23,730.46 |

* Startdatum Normal-Abschreibung  

    Berechnungsmethode:  

    *1. Jahr: 25 % von 100.000 = 25.000 = 12.500 + 12.500*

    *2. Jahr: 25 % von 75.000 = 18.750 = 9.375 +9.375*

    *3. Jahr: 25 % von 56.250 = 14.062,50 = 7.031,25 +7.031,25*

    Die Berechnung erfolgt bis der Buchwert gleich dem endgültigen Rundungsbetrag oder dem von Ihnen angegebenen Restwert ist.   

## <a name="declining-balance-2-depreciation"></a>Abschreibungsmethode "2 % degressiv"
Die Methoden Degressiv 1 und Degressiv 2 berechnen den gleichen Gesamt Abschreibung-Betrag für jedes Jahr. Falls Sie die Stapelverarbeitung **AfA berechnen** mehr als einmal jährlich ausführen, resultiert die Methode "Degressiv 1" in gleichen AfA Beträgen für die einzelnen Perioden. Die Methode "Degressiv 2" hat in diesem Fall fallende Beträge in den einzelnen Perioden zur Folge.  

### <a name="example---declining-balance-2-depreciation"></a>Beispiel – Abschreibungsmethode "2 % degressiv"
Eine Anlage hat Anschaffungskosten von MW 100.000. Das Feld **Degressive AfA %** hat den Wert 25. Die Stapelverarbeitung **AfA berechnen** wird zweimal jährlich ausgeführt. Die Anlagenposten sehen folgendermassen aus:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01.01.10 |Anschaffungskosten |* |100,000.00 |100,000.00 |
| 30.06.10 |Abschreibungen |180 |-13.397,46 |86,602.54 |
| 31.12.10 |Abschreibungen |180 |-11.602,54 |75,000.00 |
| 30.06.11 |Abschreibungen |180 |-10.048,09 |64,951.91 |
| 31.12.11 |Abschreibungen |180 |-8.701,91 |56,250.00 |

* Startdatum Normal-Abschreibung  

Berechnungsmethode:  

* BW = Buchwert  
* AT = Anzahl Abschreibungstage  
* DAP = Degressive AfA Prozent  
* B = DAP/100  
* T = AT/360  

Die Formel zur Berechnung des Abschreibungsbetrages ist:  

*DA = BV x (1 – (1 –P)<sup>D<sup>*  

Die Abschreibungswerte lauten:  

| Datum | Berechnung |
| --- | --- |
| 30.06.10 |AB = 100.000,00 x (1 - (1 - 0,25)<sup>0,5<sup>) = 13.397,46 |
| 31.12.10 |AB = 86.602,54 x (1 - (1 - 0,25)<sup>0,5<sup>) = 11.602,54 |
| 30.06.11 |AB = 75.000,00 x (1 - (1 - 0,25)<sup>0,5<sup>) = 10.048,09 |
| 31.12.11 |AB = 64.951,91 x (1 - (1 - 0,25)<sup>0,5<sup>) = 8.701,91 |

## <a name="db1sl-depreciation"></a>Degressiv/Lineare Abschreibung 1
"Degr1/Linear" ist eine abgekürzte Kombination von "Degressiv 1" und "Linear". Die Berechnung erfolgt bis der Buchwert gleich dem endgültigen Rundungsbetrag oder dem von Ihnen angegebenen Restwert ist.  

Die Stapelverarbeitung **AfA berechnen** berechnet einen linearen Betrag und einen degressiven Betrag. Nur der grössere dieser beiden Beträge wird in das Buch.-Blatt übertragen.  

Die Anwendung kann die degressiven Berechnungen unter der Verwendung von verschiedenen Prozentsätzen durchführen.  

Wenn Sie diese Methode verwenden, müssen Sie die geschätzte Nutzungsdauer und einen degressiven Prozentsatz auf der Seite **Anlagen-Abschreibungsbücher** eingeben.  

### <a name="example---db1-sl-depreciation"></a>Beispiel – Degressiv-Lineare Abschreibung 1
Eine Anlage hat Anschaffungskosten von MW 100.000. Im Fenster **Anlagen-Abschreibungsbücher** enthält die Seite **Degressive Abschreibung %** den Wert 25 und das Feld **Nutzungsdauer i. Jahren** den Wert 8. Die Stapelverarbeitung **AfA berechnen** wird zweimal jährlich ausgeführt.  

Die Anlagenposten sehen folgendermassen aus:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01.01.10 |Anschaffungskosten |* |100,000.00 |100,000.00 |
| 30.06.10 |Abschreibungen |180 |-12.500,00 |87,500.00 |
| 31.12.10 |Abschreibungen |180 |-12.500,00 |75,000.00 |
| 30.06.11 |Abschreibungen |180 |-9.375,00 |65,625.00 |
| 31.12.11 |Abschreibungen |180 |-9.375,00 |56,250.00 |
| 30.06.12 |Abschreibungen |180 |-7.031,25 |49,218.75 |
| 31.12.12 |Abschreibungen |180 |-7.031,25 |42,187.50 |
| 30.06.13 |Abschreibungen |180 |-5.273,44 |36,914.06 |
| 31.12.13 |Abschreibungen |180 |-5.273,44 |31,640.62 |
| 30.06.14 |Abschreibungen |180 |-3.955,08 |27,685.54 |
| 31.12.14 |Abschreibungen |180 |-3.955,08 |23,730.46 |
| 30.06.15 |Abschreibungen |180 |-3.955,08 |19.775,38 Linear |
| 31.12.15 |Abschreibungen |180 |-3.955,08 |15.820,30 Linear |
| 30.06.16 |Abschreibungen |180 |-3.955,08 |11.865,22 Linear |
| 31.12.16 |Abschreibungen |180 |-3.955,07 |7.910,15 Linear |
| 30.06.17 |Abschreibungen |180 |-3.955,08 |3.955,07 Linear |
| 31.12.17 |Abschreibungen |180 |-3.955,07 |0,00 Linear |

* Startdatum Normal-Abschreibung  

"Linear" nach dem Buchwert bedeutet, dass die lineare Abschreibung verwendet worden ist.  

Berechnungsmethode:  

Jahr:  

*Degressiv Betrag: 25% von 100.000 = 25.000=12.500+12.500*  

*Linear Betrag = 100.000/8=12.500=6.250+6.250*  

Es wird der degressive Betrag verwendet, da es sich um den grösseren Betrag handelt.  

Jahr (2015):  

*Degressiv Betrag: 25% von 23,730.46 = 4,943.85=2,471.92+2,471.92*  

*Linearer Betrag = 23,730.46/3 = 7,910.15 = 3,995.07 + 3,995.08*  

Es wird der lineare Betrag verwendet, da es sich um den grösseren Betrag handelt.  

## <a name="user-defined-depreciation"></a>Benutzerdefinierte Abschreibung
Die Anwendung hat Funktionen, mit denen Sie benutzerdefinierte Abschreibungsmethoden definieren können.  

Mit einer benutzerdefinierten Methode können Sie die Seite **Abschreibungstabellen** verwenden, in dem Sie einen Abschreibung Prozentsatz für jede Periode angeben müssen (Monat, Quartal, Jahr oder Buchhaltungsperiode).  

Die Formel zur Berechnung des Abschreibungsbetrages ist:  

Abschreibungsbetrag = (Abschreibung % x Anzahl Abschreibungstage x Abschreibungsbasis) / (100 x 360)  

### <a name="depreciation-based-on-number-of-units"></a>Abschreibung basierend auf der Stückzahl
Diese benutzerdefinierte Methode kann auch verwendet werden, um eine Abschreibung nach der produzierten Stückzahl durchzuführen, zum Beispiel für Produktionsmaschinen, die eine von der Stückzahl abhängige Lebensdauer haben. Auf der Seite **Abschreibungstabellen** können Sie die Stückzahl eingeben, die innerhalb einer Periode (Monat, Quartal, Jahr oder Buchhaltungsperiode) produziert werden kann.  

### <a name="to-set-up-user-defined-depreciation-methods"></a>So richten Sie benutzerdefinierte Abschreibungsmethoden ein
Auf der Seite **Abschreibungstabelle** können Sie benutzerdefinierte Abschreibungsmethoden einrichten. Beispielsweise können Sie die Abschreibung basierend auf der Stückzahl einrichten.  

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Abschreibungstabellen** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Abschreibung-Tabelle Übersicht** wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie auf der Seite **Abschreibungstabelle - Karte** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="example---user-defined-depreciation"></a>Beispiel - Benutzerdefinierte Abschreibung
Sie verwenden eine Abschreibungsmethode, die es Ihnen erlaubt, Anlagen für steuerliche Zwecke schneller abzuschreiben.  

Sie könnten für steuerliche Zwecke die folgenden Sätze für eine Anlage mit einer Lebensdauer von drei Jahren verwenden:  

* Jahr 1: 25 %  
* Jahr 2: 38 %  
* Jahr 3: 37 %  

Die Anschaffungskosten betragen MW 100.000 und die Lebensdauer für die Abschreibung ist fünf Jahre. Die Abschreibung wird manuell berechnet.  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01.01.10 |Anschaffungskosten |* |100,000.00 |100,000.00 |
| 31.12.10 |Abschreibungen |360 |-25.000,00 |75,000.00 |
| 31.12.11 |Abschreibungen |360 |-38.000,00 |37,000.00 |
| 31.12.12 |Abschreibungen |360 |-37.000,00 |0 |
| 31.12.13 |Abschreibungen |Keine |Keine |0 |
| 31.12.14 |Abschreibungen |Keine |Keine |0 |

* Startdatum Normal-Abschreibung  

Wenn Sie eine benutzerdefinierte Methode verwenden, müssen die Seiten **Startdatum Benutzerdef. Abschreibung** und **Startdatum Normal-Abschreibung** im Fenster **Anlagen-Abschreibungsbücher** ausgefüllt werden. Das Feld **Startdatum Benutzerdef. Abschreibung** und der Inhalt des Felds **Periodenlänge** auf der Seite **Abschreibungstabellen** werden verwendet, um die Zeitintervalle für Abschreibungsberechnungen festzulegen. Damit wird sichergestellt, dass die Anwendung den angegebenen Prozentsatz für sämtliche Anlagen am gleichen Tag verwendet. Das Feld **Startdatum Normal-Abschreibung** wird verwendet, um die Anzahl der Abschreibungstage zu berechnen.  

Im vorherigen Beispiel enthalten die Felder **Startdatum Benutzerdef. AfA** und **Startdatum Normal-AfA** beide den Wert "01/01/01". Hätte das Feld **Startdatum Benutzerdef. AfA** jedoch den Wert "01/01/10" und das Feld **Startdatum Normal-AfA** den Wert "01/04/11" enthalten, wäre das Ergebnis folgendermassen ausgefallen:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01.01.10 |Anschaffungskosten |* |100,000.00 |100,000.00 |
| 31.12.10 |Abschreibungen |270 |-18.750,00 |81,250.00 |
| 31.12.11 |Abschreibungen |360 |-38.000,00 |42,250.00 |
| 31.12.12 |Abschreibungen |360 |-37.000,00 |6,250.00 |
| 31.12.13 |Abschreibungen |90 |-6.250,00 |0 |
| 31.12.14 |Abschreibungen |Keine |Keine |0 |

* Startdatum Normal-Abschreibung  

## <a name="half-year-convention-depreciation"></a>Abschreibung 1 unter Verwendung der US-Halbjahresregel
Die US-Halbjahresregel wird nur dann angewendet, wenn Sie ein Häkchen auf der Seite **US-Halbjahresregel verwenden** im **Anlagen-Abschreibungsbuch** gesetzt haben.  

Diese Abschreibung-Methode kann im Zusammenhang mit folgenden Abschreibungsmethoden in der Anwendung verwendet werden:  

* Linear  
* Degressiv 1  
* Degr1/Linear  

Wenn die Halbjahresregel angewendet wird, hat eine Anlage sechs AfA Monate in dem ersten Geschäftsjahr der Abschreibung, unabhängig vom Inhalt des Feldes **Abschreibungsdatum** .  

> [!NOTE]  
>   Die Nutzungsdauer einer Anlage, die nach dem ersten Geschäftsjahr verbleibt, enthält immer ein halbes Jahr, wenn die US-Halbjahresregel verwendet wird. Damit die Halbjahresregel korrekt angewendet wird, muss dass Feld **Enddatum d. Nutzungsdauer** auf der Seite **Anlagen-Abschreibungsbuch** immer ein Datum enthalten, das genau sechs Monate vor dem Enddatum des Geschäftsjahres liegt, in dem die Anlage vollständig abgeschrieben ist.  

### <a name="example---half-year-convention-depreciation"></a>Beispiel – Abschreibung 1 unter Verwendung der US-Halbjahresregel
Eine Anlage hat Anschaffungskosten von MW 100.000. Das **Startdatum Normal-AfA** ist der 01.03.10. Die erwartete Lebensdauer ist fünf Jahre, daher muss das Feld **Enddatum d. Nutzungsdauer** den Wert 30.06.15 enthalten. Die Stapelverarbeitung **Abschreibung berechnen** wird jährlich ausgeführt. Dieses Beispiel basiert auf einem Kalenderjahr als Geschäftsjahr.  

Die Anlagenposten sehen folgendermassen aus:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01.03.10 |Anschaffungskosten |* |100,000.00 |100,000.00 |
| 31.12.10 |Abschreibungen |270 |-10.000,00 |90,000.00 |
| 31.12.11 |Abschreibungen |360 |-20.000,00 |70,000.00 |
| 31.12.12 |Abschreibungen |360 |-20.000,00 |50,000.00 |
| 31.12.13 |Abschreibungen |360 |-20.000,00 |30,000.00 |
| 31.12.14 |Abschreibungen |360 |-20.000,00 |10,000.00 |
| 31.12.15 |Abschreibungen |180 |-10.000,00 |0.00 |

* Startdatum Normal-Abschreibung  

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Beispiel – Degressiv/Lineare Abschreibung 1 unter Verwendung der US-Halbjahresregel
Eine Anlage hat Anschaffungskosten von MW 100.000. Das **Startdatum Normal-AfA** ist der 01.11.10. Die erwartete Lebensdauer ist fünf Jahre, daher muss das Feld **Enddatum d. Nutzungsdauer** den Wert 30.06.15 enthalten. Auf der Seite **Anlagen-Abschreibungsbücher** enthält das Feld **Degressive Abschreibung %** den Wert 40. Die Stapelverarbeitung **Abschreibung berechnen** wird jährlich ausgeführt. Dieses Beispiel basiert auf einem Kalenderjahr als Geschäftsjahr.  

Die Anlagenposten sehen folgendermassen aus:  

| Datum | Anlagenbuchungsart | Tage | Betrag | Buchwert |
| --- | --- | --- | --- | --- |
| 01.11.10 |Anschaffungskosten |* |100,000.00 |100,000.00 |
| 31.12.10 |Abschreibungen |60 |-20.000,00 |80,000.00 |
| 31.12.11 |Abschreibungen |360 |-32.000,00 |48,000.00 |
| 31.12.12 |Abschreibungen |360 |-19.200,00 |28,800.00 |
| 31.12.13 |Abschreibungen |360 |-11.520,00 |17,280.00 |
| 31.12.14 |Abschreibungen |360 |-11.520,00 |5.760,00 Linear |
| 31.12.15 |Abschreibungen |180 |  -5.760,00 |0,00 Linear |

* Startdatum Normal-Abschreibung  

"Linear" nach dem Buchwert bedeutet, dass die lineare Abschreibung verwendet worden ist.  

Berechnungsmethode:  

Jahr:  

*Degressiver Betrag = Betrag des gesamten Jahres = 40% von 100,000 = 40,000. Daher für ein halbes Jahr 40,000 / 2 = 20,000*  

*Linearer Betrag = 100,000% von 5 = 20.000. Daher für ein halbes Jahr 20.000 / 2 = 10.000* B  

Es wird der degressive Betrag verwendet, da es sich um den grösseren Betrag handelt.  

Jahr (2004):  

*Degressiver Betrag = 40% von 17,280.00 = 6,912.00*  

*Linearer Betrag = 28,800 / 1.5 = 11,520.00*  

Es wird der lineare Betrag verwendet, da es sich um den grösseren Betrag handelt.  

## <a name="duplicating-entries-to-more-depreciation-books"></a>Kopieren von Posten in weitere AfA-Bücher
Falls Sie über 3 Abschreibungsbücher B1, B2 und B3 verfügen und Sie Posten aus B1 in B2 und B3 kopieren möchten, können Sie ein Häkchen in dem Feld **Kopien ermöglichen** in der Abschreibungsbuchkarte von B2 und B3 setzen. Dies kann hilfreich sein, wenn das Abschreibungsbuch B1 in die Fibuposten integriert ist und das Anlagen-Fibu Erf.-Journal verwendet, während die Abschreibungsbücher B2 und B3 nicht in der Fibuposten integriert sind und das Anlagen Erf.-Journal verwenden.  

Wenn Sie einen Posten in B1 im Anlagen-Fibu Erf.-Journal erstellen und dann ein Häkchen in dem Feld **Kopiervorgang aktivieren** gesetzt haben, kopiert die Anwendung den Posten in die Bücher B2 und B3 im Anlagen Erf.-Journal, wenn Sie den Posten buchen.  

> [!NOTE]  
>   Es ist nicht möglich in dem gleichen Erf.-Journal und der gleichen Erf.-Journalvorlage zu kopieren, aus der Sie kopieren. Wenn Sie Posten im Fibu Erf.-Journal buchen, können Sie diese über eine weitere Stapelverarbeitung in ein Anlagen Erf.-Journal oder ein Anlagen Fibu Erf.-Journal kopieren.  

> [!NOTE]  
>   Es ist nicht möglich, im Anlagen Fibu Erf.-Journal und im Anl. Erf.-Jrn. dieselbe Nummernserie zu verwenden. Wenn Sie im Anlagen Fibu Erf.-Journal Posten buchen, müssen Sie das Feld **Belegnr.** leer lassen. Wenn Sie in das Feld eine Nummer eingeben, wird die Nummer im Anlagen Erf.-Journal dupliziert. Sie müssen die Belegnummer manuell ändern, bevor Sie das Erf.-Journal buchen können.  

## <a name="see-also"></a>Siehe auch
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Erste Schritte](product-get-started.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
