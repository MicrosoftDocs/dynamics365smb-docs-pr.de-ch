---
title: 'Gewusst wie: Einrichten von Intrastat-Berichten| Microsoft Docs'
description: "Erfahren Sie, wie Intrastat-Berichtsfunktinen eingerichtet werden, und wie der Handel mit Unternehmen in anderen EU-Ländern gemeldet wird."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 497f952684cd893bddd954378c02f55f45224f84
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="how-to-set-up-and-report-intrastat"></a>Gewusst wie: Einrichten von Intrastat-Berichten
Alle Unternehmen innerhalb der EU sind verpflichtet, Auskunft über ihre Handelsaktivitäten mit anderen EU-Ländern/-Regionen zu geben. Warenbewegungen müssen jeden Monat dem Statistischen Amt Ihres Landes/Ihrer Region mitgeteilt und die Berichte müssen an die Steuerbehörden übermittelt werden. Dies wird als Intrastat-Berichterstattung bezeichnet. Im Fenster **Intrastat Erfassungsjournal** können Sie regelmässige Intrastat-Berichte ausfüllen.  

## <a name="required-and-optional-setups"></a>Erforderliche und optionale Einrichtung
Bevor Sie das Intrastat Erf.-Journal verwenden können, um Intrastat-Informationen zu berichten, müssen Sie mehrere Dinge einrichten:  

* **Intrastat-Erf.-Journalvorlagen**: Sie müssen die Intrastat-Erf.-Journalvorlagen und Intrastat-Erf.-Journalnamen einrichten, die Sie verwenden. Da Intrastat-Daten monatlich erfasst werden, müssen Sie 12 Intrastat-Erfassungsjournale basierend auf derselben Vorlage erstellen.  
* **Warencodes**: Zoll- und Steuerbehörde haben numerische Codes eingerichtet, die Artikel und Dienstleistungen klassifizieren. Sie geben diese Codes der Artikel an.
* **Transaktionstypencodes**: Länder und Regionen haben unterschiedliche Codes für Intrastat-Transaktionstypen, wie beispielsweise gewöhnlichen Einkauf und Verkauf, den Austausch zurückgegebener Waren und den Austausch nicht zurückgegebener Waren. Einrichtung aller Codes, die sich auf Ihr Land/Ihre Region beziehen. Sie verwenden diese Codes in Einkaufs- und Verkaufsbelegen und wenn Sie Rückgaben verarbeiten.  
* **Transportmethoden**: Es gibt sieben einstellige Codes für Intrastat-Transportmethoden. **1** für See, **2** für Schiene, **3** für Strasse, **4** für Luft, **5** für Post, **7** für feste Installationen und **9** für eigenen Antrieb (z. B. Tranportieren eines Autos, indem dieses gefahren wird). [!INCLUDE[d365fin](includes/d365fin_md.md)] erfordert diese Codes nicht, wir empfehlen jedoch, dass die Beschreibungen eine ähnliche Bedeutung bereitstellen.  

Optional können Sie auch Folgendes angeben:

* **Transaktionsspezifikationen**: Dienen der Ergänzung der Beschreibungen aus den Buchungsarten.  
* **Regionen**: Dienen dazu, Informationen über Länder und Regionen zu ergänzen.  
* **Häfen**: Dienen dazu, die Positionen anzugeben, wo Sie Artikel in andere Länder versenden oder aus anderen Ländern empfangen. Heathrow Airport ist ein Beispiel für einen Hafen. Sie geben Häfen auf Verkaufs- und Einkaufsbelegen des Inforegisters **Aussenhandel** ein. Diese Daten werden auch aus den Lagerposten kopiert, wenn Sie das Intrastat-Erf.-Journal erstellen.  

### <a name="to-set-up-intrastat-templates-and-batches"></a>So richten Sie Intrastat-Buch.-Blattvorlagen und -stapel ein
Die Intrastat-Stapelverarbeitungsaufträge enthalten nur Lagerposten, keine Fibuposten. Sind Fibukonten vorhanden, die in die Intrastat-Berichte einbezogen werden müssen, müssen diese manuell eingegeben werden. Wenn Sie also beispielsweise aus einem anderen Land/einer anderen Region innerhalb der EU einen Computer erwerben, geht der Computer zwar nicht in den Lagerbestand ein, er wird jedoch auf ein Fibukonto gebucht. Diese Postenart muss manuell in das Intrastat-Erf.-Journal eingegeben werden.  

Sie können die Positionen in eine Datei exportieren, die Sie an Ihre Intrastat-Behörden senden. Sie können auch einen Bericht ausdrucken, die Informationen manuell in die Formulare Ihrer Behörden eingeben und dann die Informationen übertragen.

>  [!Note]
> Es empfiehlt sich, für jeden Monat einen Intrastat-Erf.-Journalnamen zu erstellen.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Intrastat Erf.-Journalvorlagen** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Erstellen Sie eine Vorlage für jedes verwendete Intrastat-Formular.  
3. Um Anlagen zu erstellen, wählen Sie die Registerkarte **Navigieren**, und wählen Sie dann **Stapel** aus.  
4. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Erstellen Sie eine Vorlage für jedes verwendete Intrastat-Formular.  

> [!Note]
> Geben Sie im Feld **Statistikperiode** die Statistikperiode als vierstellige Zahl ein, wobei die ersten beiden Ziffern das Jahr und die nächsten beiden Ziffern den Monat darstellen. Für Juni 2017 beispielsweise geben Sie 1706 ein.

### <a name="to-set-up-commodity-codes"></a>Um Warencodes einzurichten:
Alle Artikel, die Sie kaufen oder verkaufen, benötigen einen Warencode.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Warencodes** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Um einem Artikel einem Warencode zuzuordnen, erweitern Sie auf der Seite **Artikelkarte** das Inforegister **Kosten und Buchen** und geben dann den Code in das Feld **Warencode** ein.   

### <a name="to-set-up-transaction-nature-codes"></a>Einrichten von Transaktionsartencodes
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Transaktionscodes** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Wenn Sie häufiger einen bestimmten Transaktionsartencode verwenden, können Sie sich den Standard erstellen. Dazu gehen Sie zur Seite **Intrastat einrichten**, und wählen den Code aus.

### <a name="to-set-up-transport-methods"></a>Einrichten von Transportmethoden
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Transportmethode** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a>Um einzurichten die Intrastat-Berichte erforderlich sein sollte Sie unter
In einigen Ländern wie Spanien und Grossbritannien, verlangen die Behörden, dass Intrastat-Berichte, beispielsweise, die Lieferbedingung für Einkäufe oder einige andere Werte enthalten, wenn Verkaufs- über einem bestimmten Schwellenwert ist. Im Fenster **Intrastat einrichten** können Sie auswählen, um **Einrichtung Checkliste Intrastat** Pflichtfelder im Fenster **Intrastat Erfassungsjournal** festlegen soll.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Intrastateinrichtung** ein, und wählen dann den zugehörigen Link aus.
2. Wählt die **Intrastat-Prüflisten-Einrichtung** Aktion aus.
3. Im Fenster auf **Intrastat-Prüflisten-Einrichtung** in **Feldname**, um den Intrastat-Berichtsfelds auszuwählen, das Sie zwar erforderlich machen möchten. 

## <a name="to-report-intrastat"></a>Erstellen Sie Intrastat-Berichte
Nachdem Sie das Intrastat-Erfassungsjournal ausgefüllt haben, können Sie den Bericht **Checklistenbericht** ausführen, um zu überprüfen, ob alle Daten in dem Erfassungsjournal korrekt sind. Pflichtfelder, die Sie im Fenster **Intrastat-Checklisten-Einrichtung**, die Werte fehlende sind, werden angezeigt in Problemen und in warnendem Infobox im Fenster **Intrastat Erfassungsjournal** festgelegt haben. Anschliessend können Sie einen Intrastat-Bericht als Formular drucken, oder Sie erstellen eine Datei, um diese an die Steuerbehörden in Ihrem Land/Region zu senden.  

### <a name="to-fill-in-intrastat-journals"></a>Intrastat-Erfassungsjournale ausfüllen:  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Intrastat Erf.-Journal** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie auf der Seite **Intrastat Erf.-Journal** das betreffende Erf.-Journal im Feld **Erf.-Journalname** aus und dann **OK**.  
3. Wählen Sie die Aktion **Mahnungszeile vorschlagen**. Die Felder **Startdatum** und **Enddatum** enthalten bereits die Daten, die Sie im Erf.-Journalnamen für die Statistikperiode angegeben haben.  
4. Im Feld **Kosten Zu-/Abschlag %** können Sie einen Prozentsatz (zur Deckung der Transport- und Versicherungskosten) eingeben. Wenn Sie einen Prozentsatz eingeben, ist der Inhalt des Feldes **Statistischer Wert** dementsprechend höher.  
5. Klicken Sie zum Starten des Batchauftrags auf **OK**.  

Der Batchauftrag holt alle Posten innerhalb der Statistikperiode und fügt Sie als Zeilen im Intrastat Erfassungsjournal ein. Sie können diese Positionen bei Bedarf bearbeiten.  

> [!IMPORTANT]  
>  Durch die Stapelverarbeitung werden nur die Posten abgerufen, die einen Länder-/Regionscode enthalten, für den im Fenster **Länder/Regionen** ein Intrastatcode angegeben wurde. Daher ist es wichtig, dass Sie Intrastatcodes für die Länder-/Regionscodes eingeben, für die Sie die Stapelverarbeitung ausführen möchten.  

### <a name="report-intrastat-on-a-form-or-a-file"></a>Melden von Intrastat auf einem Formular oder einer Datei
Um von den Statistikbehörden die für das Intrastat-Formular benötigten Daten zu erhalten, müssen Sie den Bericht **Intrastat – Formular** ausdrucken. Zuvor müssen Sie das Intrastat-Erf.-Journal vorbereiten und ausfüllen. Wenn Sie sowohl Einkaufs- als auch Verkaufstransaktionen haben, müssen Sie für jede Art ein eigenes Formular ausfüllen und daher den Bericht zweimal drucken.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Logistik Intrastat Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie im Fenster **Intrastat-Journal** im Feld Erf.-Journalname das relevante **Erf.-Journal** aus.  
3. Füllen Sie das Erf.-Journal manuell aus, oder klicken Sie auf **Posten holen**, sofern das Journal noch nicht ausgefüllt wurde.  
4. Wählen Sie die **Druck-Intrastat Erf.-Journal** Aktion aus.  
5. Fügen Sie im Inforegister **Intrastat Erf.-Journalzeile** einen **Art**-Filter hinzu, und geben Sie an, ob es sich um einen **Wareneingang** oder **Warenausgang** handelt.  
6. Wählen Sie **Senden an**, um den Bericht zu drucken.  

### <a name="report-intrastat-in-a-file"></a>Intrastat Berichte in einer Datei
Sie können den Intrastat-auch auf einer Datei einreichen. Bevor Sie die Datei erstellen, können Sie einen Testbericht drucken, der dieselben Daten enthält wie die Datei.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Intrastat Erf.-Journal** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie im Fenster **Intrastat-Journal** im Feld Erf.-Journalname das relevante **Erf.-Journal** aus.  
3. Füllen Sie das Erf.-Journal manuell aus, oder klicken Sie auf **Posten holen**, sofern das Journal noch nicht ausgefüllt wurde.  
4. Wählen Sie die Aktion **Aus Datei erstellen** aus.  
5. Klicken Sie im Stapelverarbeitungsfenster auf **OK**.  
6. Wählen Sie **Speichern** aus.  
7. Navigieren Sie zum gewünschten Speicherort für die Datei, und geben Sie den Dateinamen ein. Klicken Sie auf  **Speichern**.

## <a name="reorganize-intrastat-journals"></a>Reorganisieren von Intrastat Buch.-Blättern
Sie müssen für jeden Monat einen Intrastat-Bericht einreichen und für jeden Bericht einen neuen Erf.-Journalnamen erstellen. Deshalb werden Sie irgendwann über eine Vielzahl von Erf.-Journalnamen verfügen. Die Erf.-Journalzeilen werden nicht automatisch gelöscht. Sie werden vielleicht Ihre Erf.-Journalnamen periodisch reorganisieren wollen. Sie tun dies, indem Sie die Erf.-Journalnamen löschen, die Sie nicht länger benötigen. Die Erfassungsjournalzeilen in diesen Erfassungsjournalnamen werden ebenfalls gelöscht.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Logistik Intrastat Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie das Feld **Buch.-Blattname** aus, um die Optionen anzuzeigen.  
3. Wählen Sie die zu löschenden Erf.-Journalnamen aus und wählen Sie **Löschen**.  

## <a name="see-also"></a>Siehe auch
[Finanzmanagement](finance.md)

