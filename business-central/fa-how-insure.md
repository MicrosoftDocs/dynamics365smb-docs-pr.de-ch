---
title: Anlagen versichern
description: 'Sie können eine oder mehrere Anlagen einer Richtlinie zuordnen, indem Sie von der Seite **Versicherungsjournal** aus in das Sachkonto der Versicherung buchen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="insure-fixed-assets"></a>Anlagen versichern

Verwenden Sie die Seite  **Versicherungskarte**, um eine Versicherungspolice für ein oder mehrere Anlagegüter abzuschließen. Sie können einer Versicherungspolice ein Anlagevermögen oder einer Versicherungspolice mehrere Anlagevermögen zuordnen.

Sie ordnen einer Anlage einer Versicherungspolice zu, indem Sie sie im Versicherungsposten auf der Seite **Versicherungs Erf.-Journal** buchen.

Zudem können Sie eine Anlage einer Versicherungspolice zuzuordnen und Versicherungsposten erstellen, wenn Sie deren Anschaffungskosten buchen. Sie buchen Anschaffungskosten aus dem Anlagenjournal mit ausgefülltem Feld  **Versicherungsnr.** . Sie müssen den Schalter  **Automatische Versicherungsbuchung**  auf der Seite  **Anlageneinrichtung**  aktivieren. Weitere Informationen finden Sie unter  [Erwerben eines Anlagevermögens mithilfe eines Anlagevermögen-Fibujournals](fa-how-acquire.md#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

Wenn die Option  **Automatische Versicherungsbuchung** auf der Seite  **Anlageneinrichtung** nicht aktiviert ist, werden beim Buchen von Anschaffungen aus dem Anlagenjournal Zeilen auf der Seite  **Versicherungsjournal**  erstellt. Sie müssen diese Zeilen manuell buchen.

> [!WARNING]  
> Wenn Sie die Option  **Automatische Versicherungsbuchung**  auf der Seite  **Anlageneinrichtung**  nicht aktivieren, sollte Ihr Versicherungsjournal auf einer Journalvorlage ohne Nummernserie basieren. Der Grund dafür ist, dass die eingefügten Belegnummern aus der Anl. Erf.-Journalzeile andernfalls einen Konflikt mit der Nummernserie des Versicherungs Erf.-Journals verursachen. Weitere Informationen über Erf.-Journalvorlagen und Erf.-Journalstapel finden Sie unter [Einrichten allgemeiner Anlagen-Informationen](fa-how-setup-general.md).

Nachdem Sie einer Versicherungspolice ein Anlagevermögen zugewiesen haben, enthält das Feld  **Versichert**  auf der Anlagenkarte den Eintrag  **Ja**. Wenn Sie das Anlagevermögen verkaufen, wird der Schalter automatisch deaktiviert.

## <a name="to-create-or-modify-an-insurance-card"></a>So erstellen oder ändern Sie eine Versicherungskarte

Wenn Sie Informationen über Änderungen in der Deckungssumme erhalten, müssen Sie diese in der **Versicherungskarte**aktualisieren, um sicherzustellen, dass die Versicherungsdeckung korrekt angezeigt wird.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Versicherung** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** aus, um eine neue Karte für eine Versicherungspolice zu erstellen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Alternativ wählen Sie die Versicherungspolice, die Sie ändern möchten, und wählen die Aktion **Bearbeiten** aus.

## <a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a>So verknüpfen Sie eine Anlage mit einer Versicherungspolice durch Buchen aus einem Versicherungs Erf.-Journal

Sie verknüpfen eine Anlage mit einer Versicherungspolice, indem Sie sie in den Versicherungsposten buchen.  

Nachfolgend wird beschrieben, wie Sie eine Versicherungs Erf.-Journalzeile manuell erstellen. Wenn auf der Seite  **Anlageneinrichtung**  der Schalter  **Automatische Versicherungsbuchung**  aktiviert ist, werden beim Buchen von Anschaffungskosten automatisch Versicherungsjournalzeilen erstellt. In diesem Fall müssen Sie nur das Erf.-Journal buchen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Vers. Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie das relevante Erf.-Journal und füllen Sie die Erf.-Journalzeilen nach Bedarf aus.  
3. Um mehrere Anlagen einer Versicherungspolice zuzuweisen, können Sie Erfassungsjournalzeilen mit dem gleichen Wert im Feld **Versicherungsnr.** und unterschiedliche Werte im Feld **Anlagennr.**  
4. Wählen Sie die Aktion **Buchen** aus.  

    > [!NOTE]  
    > Die Posten aus dem Versicherungs Erfassungsjournal werden nur auf die Versicherungsposten gebucht.  

## <a name="to-update-the-insurance-value-of-a-fixed-asset"></a>So aktualisieren Sie den Versicherungswert einer Anlage

Sie können die Stapelverarbeitung **Indexiere Versicherung** verwenden, um den Wert der versicherten Anlagen zu aktualisieren.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Versicherung indexieren** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder je nach Bedarf aus.

    > [!NOTE]  
    >   Im Feld **Indexzahl** wird eine Senkung um 5 % beispielsweise als "95" eingegeben, während eine Steigerung von 2 % als "102" eingegeben wird.  
3. Wählen Sie die Schaltfläche **OK** aus.  

   Die Stapelverarbeitung berechnet den neuen Betrag als Prozentsatz des gesamten versicherten Wertes auf der Seite **Versicherungsstatistik** und erstellt dann eine Zeile im Vers. Erf.-Journal.  
4. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Vers. Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.  
5. Öffnen Sie das relevante Versicherungs Erf.-Journal, prüfen Sie die erstellten Posten und buchen Sie diese dann auf die Versicherungsposten.  

## <a name="to-monitor-insurance-coverage"></a>So überwachen Sie die Versicherungsdeckung

[!INCLUDE[prod_short](includes/prod_short.md)] bietet dedizierte Berichte und Statistikseiten, die dazu verwendet werden können, Versicherungspolicen zu analysieren und zu überprüfen, ob Ihre Anlagen über- oder unterversichert sind.  

### <a name="overview-of-insurance-policies"></a>Übersicht der Versicherungspolicen

Gibt einen Überblicks über die Versicherungspolicen durch Drucken des Berichts **Versicherung-Liste**. Der Bericht zeigt die einzelnen Policen und die wichtigsten Felder der Versicherungskarten an.  

### <a name="insurance-coverage"></a>Versicherungsschutz

Um zu sehen, welche Versicherungspolicen welche Anlagen in welcher Höhe abdecken, können Sie den Bericht **Versicherung – Vers. Summe** ausdrucken oder anzeigen.  

#### <a name="overunder-coverage"></a>Über-/Unterdeckung

Ob Anlagevermögen über- oder unterversichert ist, können Sie auf folgende Arten prüfen:  

* Die Seite **Versicherungsstatistik**. Ein positiver Betrag in dem Feld **Über-/Unterversichert** bedeutet, dass die Anlage überversichert ist. Ein negativer Betrag bedeutet, dass das Anlagegut unterversichert ist.  
* Die Seite **Anlagenstatistik**. Wählen Sie das Feld **Versicherte Summe**, um die Seite **Versicherungsposten** anzuzeigen.  
* Der Bericht **Unter-/Überversicherung**.  
* Der Bericht **Versicherungsanalyse**.  

### <a name="uninsured-fixed-assets"></a>Nicht versicherte Sachanlagen

Um zu überprüfen, ob Sie vergessen haben, einer Versicherungspolice ein Anlagevermögen zuzuordnen, können Sie den Bericht  **Versicherung – Nicht versicherte Anlagevermögen**  ausdrucken oder in der Vorschau anzeigen. In diesem Bericht werden Anlagegüter angezeigt, für die keine Beträge im Versicherungsdeckungsbuch gebucht wurden.  

## <a name="to-view-insurance-coverage-ledger-entries"></a>So zeigen Sie Versicherungsposten an

Sie können Ihre vorgenommenen Einträge im Versicherungsdeckungsbuch einsehen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Versicherung** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die entsprechende Versicherungspolice aus, und wählen Sie dann die Aktion **Versicherungsposten**.  

## <a name="to-view-the-total-insurance-value-of-fixed-assets"></a>So zeigen Sie den gesamten Versicherungswert von Anlagen an:

Auf einer Matrixseite werden die pro Versicherungsvertrag erfassten Versicherungswerte pro Anlagevermögen angezeigt, die sich aus gebuchten versicherungsrelevanten Beträgen ergeben.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Versicherung** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die entsprechende Versicherungspolice aus, und wählen Sie dann die Aktion **Versicherte Summe pro Anlage**.  
3. Füllen Sie die Felder je nach Bedarf aus.  
4. Wählen Sie die Aktion **Matrix anzeigen** aus.  
5. Um die zu Grunde liegenden Versicherungsposten anzuzeigen, aktivieren Sie einen Wert in der Matrix.  

## <a name="to-correct-insurance-coverage-entries"></a>So korrigieren Sie Versicherungsposten

Wurde eine Anlage einer falschen Versicherung zugeordnet, können Sie dies durch die Erstellung von zwei Umgliederungsbuchungen aus dem Versicherungsjournal korrigieren.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Vers. Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine Buch.-Blattzeile für die Anlage und die korrekte Versicherungspolice, in der der Wert im Feld **Betrag** positiv ist.  
3. Erstellen Sie eine weitere Buch.-Blattzeile für die Anlage und die inkorrekte Versicherungspolice, in der der Wert im Feld **Betrag** negativ ist.  
4. Wählen Sie die Aktion **Buchen** aus.  

In der zweiten Zeile wird das Anlagevermögen aus der fehlerhaften Versicherungspolice herausgerechnet. In der ersten Zeile des Journals wird das Anlagegut der richtigen Versicherungspolice zugeordnet.  

## <a name="see-also"></a>Siehe auch

[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
