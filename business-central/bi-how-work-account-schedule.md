---
title: Finanzberichte mithilfe von Kontenschema bauen
description: "Beschreibt, wie Kontenschema verwendet werden, um unterschiedliche Ansichten und Berichte zum Analysieren von Finanzverhältnisleistungsdaten zu erstellen."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 69034b0eb97b595d0fbf5795e1fac34ecd775afe
ms.contentlocale: de-ch
ms.lasthandoff: 06/11/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Bereiten Sie Finanzberichte mit Kontenschema und Kontengruppen vor
Verwenden von Kontenschema, um die Einblicke in die Finanzdaten zu kommen, die in Ihrem Kontenschema gespeichert werden. Verwenden von Kontenschema zum Analysieren der Werte auf Fibukonten oder zum Vergleichen von Fibuposten mit Finanzbudgetposten. Die Ergebnisse werden in den Diagrammen in Ihrem Rollencenter angezeigt, wie Cashflowplan, und in Berichten, wie Erfolgsrechnung und Bilanzberichte.

Sie rufen diese beiden Berichte beispielsweise mit der Aktion **Finanzverhältnis-Abrechnungen** im Business Manager und Buchhalter Rollen-Centers ab.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] enthält mehrere Beispielkontenschemata, die Sie verwenden können , oder Sie können eigene Zeilen und Spalten einrichten, um die Werte anzugeben und zu vergleichen. So können beispielsweise Kontenschema zur Berechnung von Gewinnmargen für Dimensionen wie beispielsweise Abteilungen oder Debitorengruppen erstellen. Das bedeutet, dass Sie so viele massgeschneiderte Finanzaufstellungen erstellen können, wie Sie möchten.  

Das Einrichten eines Kontenschemas erfordert ein Verständnis für die Finanzdaten im Kontenplan. Sie können beispielsweise die Fibuposten als prozentualen Anteil der Budgetposten sehen. Dazu ist es erforderlich, dass Budgets erstellt werden. Weitere Informationen finden Sie unter [Sachkonto-Budgets erstellen](finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Kontengruppen und Kontenschema
Sie können Kontengruppen dazu verwenden, das Layout Ihrer Finanzberichte zu ändern. Wenn Sie Ihre Kontengruppen im Fenster **Sachkontokategorien** eingerichtet haben und die Aktion **Kontenschemata generieren** auswählen, werden die zugrunde liegenden Kontenschemata für die Kernfinanzberichte aktualisiert. Wenn Sie das nächste Mal einen dieser Berichte wie die Saldoabrechnung ausführen, werden neue Summen und Untereinträge basierend auf Ihren Änderungen hinzugefügt. Weitere Informationen finden Sie unter "Buchhaltungskategorien" unter [Die Fibuposten und den Kontenplan verstehen](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Neue Kontenschemata erstellen:  
 Sie benutzen Kontenschemata zum Analysieren der Werte auf Fibukonten oder zum Vergleichen von Fibuposten mit Finanzbudgetposten. Sie können beispielsweise die Sachposten als prozentualen Anteil der Finanzbudgetposten sehen.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kontenplämne** ein und wählen den zugehörenden Link aus.  
2. Wählen Sie im Fenster **Kontoschemaname** auf der Registerkarte **Neu** die Option Neu aus, um einen neuen Kontenschemanamen zu erstellen.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die **Kontenschema bearbeiten** Aktion aus.
5. Füllen Sie die Felder im Fenster **Kontenschema** aus.  

    Nachdem Sie ein neues  Kontenschema erstellt haben und  neue Zeilen in Ihrem Kontenschema eingerichtet haben, müssen Sie die Spalten einrichten. Sie können diese entweder manuell einrichten oder Ihrem Kontenschema ein vordefiniertes Spaltenlayout zuweisen.
6. Wählen Sie die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.
7. Füllen Sie die Felder im Fenster **Spaltenlayout** aus.

> [!NOTE]  
> Wurde dem Kontenschema kein Standardspaltenlayout zugeordnet, müssen Sie die  Spalten manuell einrichten.

### <a name="to-copy-an-existing-account-schedule"></a>So kopieren Sie ein Kontenschema
Die Kontenschema in der Standardeinstellung von [!INCLUDE[d365fin](includes/d365fin_md.md)] sind die Basis der Standardfinanzberichte, die möglicherweise nicht den Anforderungen Ihres Unternehmens entsprechen. Um Ihre eigenen Finanzberichte schnell erstellen zu können, beginnen Sie, indem Sie ein vorhandenes Kontenschema kopieren.
1. Im Fenster **Kontenschema** können Sie ein Kontenschema wählen und dann die **Kontenschema kopieren** Aktion auswählen.
2. Im Fenster **Kontenplan kopieren** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.

### <a name="to-create-a-column-that-calculates-percentages"></a>Eine Spalte zur Berechnung von Prozentsätzen erstellen:  
Manchmal möchten Sie möglicherweise eine Spalte in ein Kontenschema einfügen, in der Prozentsätze einer Summe berechnet werden. Wenn beispielsweise mehrere Zeilen vorhanden sind, in denen die Verkäufe nach Dimension aufgeschlüsselt sind, empfiehlt sich die Einrichtung einer Spalte, in der für jede Zeile der prozentuale Anteil an den Gesamtverkäufen angegeben ist.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kontenplämne** ein und wählen den zugehörenden Link aus.
2. Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.  
3. Klicken Sie auf der Registerkarte **Kontoschema bearbeiten**in der Gruppe Prozess auf Kontenschema bearbeiten, um eine Kontenschemazeile einzurichten, um die Gesamtsumme zu berechnen, auf denen die Prozentsätze basieren.  
4. Fügen Sie eine Zeile unmittelbar über der ersten Zeile ein, für die Sie einen Prozentsatz anzeigen möchten.  
5. Füllen Sie die Felder in der Zeile wie folgt aus: In dem Feld **Zusammenzählungsart** geben Sie **Festgelegte Basis für Prozent** ein. Geben Sie im Feld **Zusammenzählung** eine Formel für die Summe ein, auf die der Prozentsatz basiert. Wenn beispielsweise Zeile 11 die gesamten Verkäufe enthält, geben Sie **11** ein.  
6. Wählen Sie die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.  
7. Füllen Sie die Felder in der Zeile wie folgt aus: Wählen Sie im Feld **Spaltenart** **Formel** aus. Geben Sie im Feld **Formel** eine Formel für den Betrag ein, für den ein Prozentsatz berechnet werden soll, gefolgt von %. Wenn beispielsweise Spalte N die Bewegung enthält, geben Sie **N%** ein.  
8. Wiederholen Sie Schritt 4 bis 7 für jede Zeilengruppe, die nach Prozentsätzen aufgeschlüsselt werden soll.

## <a name="to-set-up-account-schedules-with-overviews"></a>Kontenschemata mit Matrizen einrichten:  
Sie können eine Kontenschema zum Erstellen eines Vergleichs der in der Finanzbuchhaltung gebuchten Werte mit den Finanzbudgetwerten benutzen.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kontenplämne** ein und wählen den zugehörenden Link aus.
2. Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.  
3. Wählen Sie die **Kontenschema bearbeiten** Aktion aus.  
4. Wählen Sie im Fenster **Kontenplan** den gewünschten Kontenschemanamen im Feld **Name** aus.
5. Wählen Sie die **Konten einfügen** Aktion aus.  
6. Wählen Sie die Konten, die Sie in Ihrer Aufstellung berücksichtigen möchten, und wählen Sie dann **OK**.

    Die Konten sind damit in Ihr Kontenschema eingefügt. Wenn Sie möchten, können Sie auch das Spaltenlayout ändern.  
7. Wählen Sie die Aktion **Übersicht** aus.  
8. Im Inforegister **Dimensionsfilter** legen Sie den gewünschten Budgetfilter fest.  
9. Wählen Sie die Schaltfläche **OK** aus.  

Die Budgetaufstellung kann nun kopiert und in ein Arbeitsblatt eingefügt werden.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Vergleichen von Buchhaltungsperioden mithilfe der Periodenformulare
Ihr Kontenschema kann sich die Ergebnisse von verschiedenen Buchhaltungsperioden, wie diesen Monat mit jenem des Vorjahresmonat vergleichen. Um das zu tun, fügen Sie eine Spalte mit dem Feld **Vergleichsperiodendatumsformel** hinzu und legen Sie dann dieses Feld auf eine Periodenformel fest.  

Eine Buchhaltungsperiode muss nicht dem Kalenderjahr entsprechen, aber jedes Geschäftsjahr muss dieselbe Anzahl von Buchhaltungsperioden aufweisen, selbst wenn jede Periode eine andere Länge haben kann.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet diese Periodenformel, um den Betrag der Vergleichsperiode in Bezug auf die Periode zu berechnen, die Sie im Datumsfilter des Anforderungsfensters im Bericht angegeben haben. Die Vergleichsperiode basiert auf der Periode des Startdatums des Datumsfilters. Für Periodenspezifikationen stehen folgende Abkürzungen zur Verfügung:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Abkürzung</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>P</p></td>
<td><p>Periode</p></td>
</tr>
<tr class="even">
<td><p>EP</p></td>
<td><p>Endperiode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.</p></td>
</tr>
<tr class="odd">
<td><p>LP</p></td>
<td><p>Laufende Periode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.</p></td>
</tr>
<tr class="even">
<td><p>GJ</p></td>
<td><p>Geschäftsjahr. GJ[1..3] bezeichnet beispielsweise das erste Quartal des laufenden Geschäftsjahres.</p></td>
</tr>
</tbody>
</table>

Beispiele für Formeln:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Formel</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;"Leer"&gt;</p></td>
<td><p>Laufende Periode</p></td>
</tr>
<tr class="even">
<td><p>-1P</p></td>
<td><p>Vorperiode</p></td>
</tr>
<tr class="odd">
<td><p>-1GJ[1..EP]</p></td>
<td><p>Das gesamte vorige Geschäftsjahr</p></td>
</tr>
<tr class="even">
<td><p>-1GJ</p></td>
<td><p>Laufende Periode des vorigen Geschäftsjahrs</p></td>
</tr>
<tr class="odd">
<td><p>-1GJ[1..3]</p></td>
<td><p>Das erste Quartal des vorigen Geschäftsjahres</p></td>
</tr>
<tr class="even">
<td><p>-1GJ[1..LP]</p></td>
<td><p>Vom Anfang des vorigen Geschäftsjahres bis zur laufenden Periode des vorigen Geschäftsjahres einschliesslich.</p></td>
</tr>
<tr class="odd">
<td><p>-1GJ[LP..EP]</p></td>
<td><p>Von der laufenden Periode des vorigen Geschäftsjahres bis zur Endperiode des vorigen Geschäftsjahres einschliesslich.</p></td>
</tr>
</tbody>
</table>

Wenn die Berechnung gemäss regulärer Zeitperioden erfolgen soll, muss eine Formel in das Feld **Vergleichsdatumsformel** eingegeben werden.

> [!NOTE]
> Es ist jedoch nicht immer transparent, welche Perioden Sie vergleichen, da Sie einen Datumsfilter in einem Bericht festlegen können, die verschiedene Daten als die Buchhaltungsperioden umfasst, die Daten im Kontenplan angezeigt werden. Beispielsweise können Sie ein Kontenschema erstellen, in dem Sie diese Periode mit derselben Periode des Vorjahrs vergleichen möchten, damit Sie den **Vergleichs-Datums-Perioden-Filter** im Feld *1GJ* festlegen. Dann führen Sie den Bericht am 28. Februar aus und legen die Datumsfilter des Januar und Februar fest. Deshalb vergleicht das Kontenschema Januar und Februar dieses Jahr mit dem Januar des Vorjahrs, die die einzige abgeschlossene Buchhaltungsperiode der zwei für das Vorjahr ist.  


## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

