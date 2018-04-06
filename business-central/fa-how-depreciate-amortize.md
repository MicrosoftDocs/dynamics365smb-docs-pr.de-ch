---
title: Anlagen abschreiben oder amortisieren| Microsoft Docs
description: "Sie müssen festlegen, wie Sie jede Ihrer Anlagen abschreiben oder amortisieren."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8d2d583ca649488f9a506362386a511743ed661b
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="depreciate-or-amortize-fixed-assets"></a>Anlagen abschreiben oder amortisieren
Abschreibung wird verwendet, um die Anschaffungskosten von Anlagen, wie z. B. Maschinen und Ausrüstung, über die Nutzungsdauer zu verteilen. Sie müssen für jede Anlage definieren, wie diese abgeschrieben wird.  

 Es gibt zwei Wege, Abschreibungen zu buchen:  

* Automatisch durch Ausführen der Stapelverarbeitung **Abschreibungen berechnen**  
* Manuell, unter Verwendung des Anlagen Fibu Erf.-Journals.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] kann tägliche Abschreibungen berechnen, sodass Sie Abschreibungen für beliebige Perioden berechnen können. Sie können damit das aktuelle operative Ergebnis beispielsweise auf monatlicher, quartalsweiser oder jährlicher Basis analysieren. Die Berechnungen verwendet ein standardisiertes Jahr mit 360 Tagen und einen standardisierten Monat mit 30 Tagen. Weitere Informationen finden Sie unter [AfA-Methoden](fa-depreciation-methods.md).  

Falls eine Anlage von verschiedenen Abteilungen verwendet wird, kann die Abschreibung automatisch entsprechend einer benutzerdefinierten Tabelle auf diese Abteilungen verteilt werden.  

Sie können falsche AfA-Posten aus einem AfA-Buch mit Hilfe der Stapelverarbeitung **Anlagenposten stornieren** stornieren. Danach können Sie die korrekten Beträge buchen, indem Sie die Stapelverarbeitung **AfA berechnen** erneut ausführen. Wenn Sie Fehler korrigieren, werden diese als Anlagenstornoposten gebucht.  

Die Indexierung wird verwendet, um die Werte allgemeinen Preisänderungen anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um die AfA-Beträge neu zu berechnen.  

## <a name="to-calculate-depreciation-automatically"></a>So berechnen Sie Abschreibung automatisch
Einmal monatlich oder in beliebigen anderen Intervallen können Sie die Stapelverarbeitung **AfA berechnen** ausführen. Der Stapelverarbeitungsjob ignoriert Anlagen, die verkauft wurden, auf der Anlagenkarte gesperrt oder inaktiv sind, und Anlagen, die die Abschreibung-Methode "Manuell" verwenden.  

1. Wählen Sie in das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **AfA berechnen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die Schaltfläche **OK** aus.  

    Die Stapelverarbeitung berechnet die Abschreibung und erstellt Zeilen im Anlagen Fibu Erf.-Journal.  
4. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.  

    Im Fenster **Anlagen-Fibu Buch.-Blatt** können Sie im Feld **Anzahl AfA-Tage** sehen, wie viele AfA-Tage berechnet wurden.  
5. Wählen Sie die Aktion **Buchen** aus.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>So buchen Sie eine Abschreibung aus dem Anlagen Fibu Erf.-Journal
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.  
2. Erstellen Sie eine ursprüngliche Erf.-Journalzeile und füllen Sie die notwendigen Felder aus.  
3. Wählen Sie im Feld **Anlagenbuchungsart** die **AfA**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Erf.-Journalzeile wird für das Gegenkonto erstellt, das für die Abschreibungsbuchung eingerichtet ist. Weitere Informationen finden Sie im Abschnitt "So richten Sie Anlagenbuchungsgruppen ein" in [ Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).  
5. Wählen Sie auf der Registerkarte **Start** die Option **Buchen** aus, um das Erfassungsjournal zu buchen.  

Falls Sie Anlagenverteilungsschlüssel eingerichtet haben, um Beträge auf verschiedene Kostenstellen und/oder Kostenträger zu verteilen, werden die Beträge während der Buchung zugeordnet. Weitere Informationen finden Sie unter [Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).  

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>So berechnen Sie Verteilungen in Anlagen Fibu Erf.-Journalen
Falls eine Anlage von verschiedenen Abteilungen verwendet wird, kann die Abschreibung automatisch, entsprechend einer benutzerdefinierten Tabelle, auf diese Abteilungen verteilt werden.  

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.  
2. Erstellen Sie eine ursprüngliche Zeile und füllen Sie die notwendigen Felder aus.
3. Wählen Sie im Feld **Anlagenbuchungsart** die **Verteilung**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Erf.-Journalzeile wird für das Gegenkonto erstellt, das für die Buchung einer Verteilung eingerichtet wird.  
5. Wählen Sie auf der Registerkarte **Start** die Option **Buchen** aus, um das Erfassungsjournal zu buchen.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Kopiervorgänge zum Vorbereiten von Buchungen in mehrere AfA-Bücher verwenden
Ausfüllen der Zeilen in einem Erf.-Journal für die Erfung auf ein Abschreibungsbuch und anschliessendes Kopieren der Zeilen in ein anderes Erf.-Journal, von wo aus sie auf ein anderes Abschreibungsbuch gebucht werden können Weitere Informationen finden Sie im Abschnitt "So buchen Sie Posten auf verschiedene AfA-Bücher".

1. Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen]das Symbol (media/ui-search/search_small.png "")Nach Seite oder Bericht suchen und geben **AfA-Buchliste** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie das entsprechende AfA-Buch aus und aktivieren Sie dann das Kontrollkästchen **Teil des Kopiervorgangs**.  

> [!IMPORTANT]  
>   Wenn Sie das Feld **Kopiervorgang aktivieren** aktiviert haben, dürfen Sie im Erfassungsjournal keine Nummernserien verwenden. Der Grund dafür ist, dass die Nummernserie für das Anlagen Fibu Erf.-Journal nicht der Nummernserie im Anlagen Erf.-Journal entspricht.  

## <a name="to-post-entries-to-different-depreciation-books"></a>So buchen Sie Posten auf verschiedene AfA-Bücher
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.  
2. Aktivieren Sie im Buch.-Blatt, das Sie zum Buchen der AfA verwenden möchten, das Kontrollkästchen **Kopiervorgang aktivieren**.  
3. Füllen Sie die verbleibenden Felder je nach Bedarf aus.  
4. Wählen Sie die Aktion **Buchen** aus.  
5. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.  

    > [!NOTE]  
    >   Das Fenster **Anlagen Buch.-Blatt** enthält neue Zeilen für verschiedene AfA-Bücher entsprechend der Verdopplungsliste.  
6. Prüfen oder bearbeiten Sie die Zeilen, und wählen Sie dann die Aktion **Buchen** aus.  

    > [!NOTE]  
    >   Eine andere Art, einen Posten in ein anderes Buch zu kopieren, ist es, einen Abschreibungsbuchcode in dem Feld **In Abschreibungsbuch kopieren** anzugeben, wenn Sie eine Erfassungsjournalzeile ausfüllen.  

Sie können mit Hilfe der Stapelverarbeitung **AfA-Buch kopieren** Posten von einem AfA-Buch in ein anderes AfA-Buch kopieren. Die Stapelverarbeitung erstellt Buch.-Blattzeilen in dem Buch.-Blatt, das Sie in dem Fenster **Anlagen Buch.-Blatt Einr.** für das AfA-Buch angegeben haben, aus dem Sie kopieren möchten. Weitere Informationen finden Sie in der folgenden Prozedur.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>So kopieren Sie Anlagenposten zwischen AfA-Büchern
1. Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen]das Symbol (media/ui-search/search_small.png "")Nach Seite oder Bericht suchen und geben **AfA-Buchliste** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie die entsprechende AfA-Buch - Karte und wählen Sie dann die Aktion **AfA-Buch kopieren**.  
3. Füllen Sie im Fenster **AfA-Buch kopieren** die Felder nach Bedarf aus.  
4. Wählen Sie die Schaltfläche **OK** aus.  

Die kopierten Zeilen werden entweder in einem Anlagen Fibu Erf.-Journal oder im Anlagen Erf.-Journal erstellt. Dies hängt davon ab, ob das Abschreibungsbuch, das Sie kopieren, in der Fibuposten aktiviert wurde.  

## <a name="see-also"></a>Siehe auch
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

