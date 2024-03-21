---
title: Anlagenabschreibung einrichten
description: Es gibt verschiedene Methoden der Abschreibung. In Business Central definieren Sie die Abschreibungsmethode für eine Anlage auf der Seite **Anlagekarte**.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: write down
ms.date: 06/28/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Richten Sie eine neue Anlagenabschreibung ein

Sie können unterschiedliche Abschreibungsmethoden für Bilanzen und Steuern verwenden. Viele Grossunternehmen verwenden die lineare Abschreibung in ihren Bilanzen, da dies im Allgemeinen höhere Gewinne anzeigt. Für Einkommenssteuerzwecke verwenden viele Unternehmen jedoch eine beschleunigte Abschreibungsmethode, wie z. B. die degressive Abschreibung. Sie definieren die Abschreibungsmethode einer Anlage mit dem Feld **Abschreibungsmethode** auf der Seite **Anlagenkarte**. Weitere Informationen zu den verschiedenen Methoden finden Sie unter [Abschreibungsmethoden](fa-depreciation-methods.md).

Sie definieren Abschreibungsbücher, in denen Sie die verschiedenen Arten, wie die Abschreibungen für unterschiedliche Typen von Anlagen berechnet werden müssen, definieren. In jedem Abschreibungsbuch werden individuelle Abschreibungsbedingungen festgelegt. Es ist zum Beispiel möglich, dass eine Anlage in einem Buch über einen Zeitraum von drei Jahren abgeschrieben wird und in einem anderen über fünf Jahre.

Nachdem Sie die erforderlichen AfA-Bücher erstellt haben, müssen Sie jeder Anlage mindestens ein AfA-Buch zuweisen. Ein Abschreibungsbuch, das einer Anlage zugewiesen ist, wird als Anlagen-Abschreibungsbuch bezeichnet. Sie können beliebig viele Abschreibungsbücher für eine Anlage einrichten.  

## So erstellen Sie ein Anlagen-Abschreibungsbuch

In einem Abschreibungsbuch können Sie festlegen, wie eine Anlage abgeschrieben wird. Sie können mehrere Abschreibungsbücher einrichten, um die verschiedenen Abschreibungsarten zu erleichtern.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Abschreibungsbücher** ein und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Abschreibungsbuch Liste** wählen Sie die Aktion **Neu** aus.
3. Füllen Sie im Inforegister **Abschreibungsbuchkarte** die Seite nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hinweis: Sie können Anlagentransaktionen auf der Seite **Anlagen Fibu Erf.-Journal** oder auf der Seite **Anlagen Erf.-Journal** erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind. Führen Sie den nächsten Schritt aus, um festzulegen, welche Art von Erf.-Journal für die verschiedenen Anlagenaktivitäten standardmässig verwendet wird.
4. Aktivieren Sie im Inforregister **Integration** das Kontrollkästchen für jede Anlagenaktivität, deren Transaktionen Sie mithilfe der Seite **Anlagen Fibu Erf.-Journal** buchen möchten.
5. Wiederholen Sie die Schritte 2 bis 4 für jede Abschreibungs- oder Buchungsmethode, die Sie den Anlagen als Abschreibungsbuch zuweisen möchten.

> [!IMPORTANT]
> Wählen Sie das Feld **Period. Abschreibung runden** zum Runden der berechneten periodischen Abschreibungsbeträge auf ganze Zahlen. Zum Beispiel, wenn Ihr Unternehmen auch die Rechnungsrundung auf ganze Zahlen auf der Seite **Fibu Einrichtung** verwendet, kann das Runden von Abschreibungsbeträgen auf ganze Zahlen zur Transparenz beitragen.

Wenn Sie beispielsweise ein Anlagevermögen veräussern, in dem im Abschreibungsbuch keine Rundung angegeben ist, die Einrichtung der Finanzbuchhaltung Ihres Unternehmens jedoch eine Rundung erfordert, wird bei der Veräusserung des Anlagevermögens die Fehlermeldung angezeigt, dass ein Betrag in einem Posten gerundet werden muss.  

## So verknüpfen Sie ein Abschreibungsbuch mit einer Anlage

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Anlage aus, für die Sie ein Anlagen-Abschreibungsbuch einrichten möchten.
3. Füllen Sie im Inforegister **AfA-Buch** die Felder nach Bedarf aus.
4. Wenn Sie mehrere AfA-Bücher der Anlage zuweisen müssen, wählen Sie die Aktion **Weitere AfA-Bücher hinzufügen** aus.
5. Alternativ wählen Sie die Aktion **AfA-Bücher** aus , um eine oder mehrere Anlagen-AfA-Bücher anzugeben.

    > [!NOTE]  
    >   Hinweis: Wenn Sie die manuelle Abschreibungsmethode verwenden, müssen Sie die Abschreibung manuell im Anlagen Fibu Erf.-Journal eingeben. Die Funktion **AfA berechnen** berücksichtigt keine Anlagen mit der AfA-Methode "Manuell". Sie können diese Methode für Anlagen verwenden, die nicht abgeschrieben werden, wie z. B. Land.

    > [!NOTE]  
    > Wenn Sie die benutzerdefinierte Abschreibungsmethode verwenden, müssen Sie das Abschreibungsbuch auf eine andere Weise zuordnen. Für weitere Informationen siehe [Benutzerdefinierte Abschreibungsmethode festlegen](fa-how-setup-user-defined-depreciation-method.md).

## So weisen Sie ein Abschreibungsbuch mehreren Anlagen mit einer Stapelverarbeitung zu

Falls Sie ein AfA-Buch mit mehreren Anlagen verknüpfen möchten, können Sie die Stapelverarbeitung **Anlagen-AfA-Buch erstellen** verwenden, um die Anwendung die erforderlichen AfA-Bücher automatisch erstellen zu lassen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Anlage aus, die Sie einrichten möchten und der ein AfA-Buch zugewiesen werden soll, und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Wählen Sie auf der Seite **Abschreibungsbuch - Karte** die Aktion **Anlagen-Abschreibungsbücher erstellen** aus.
4. Füllen Sie auf der Seite **Anlagen-Abschreibungsbuch erstellen** das Fenster **Abschreibungsbuch** aus.
5. Klicken Sie im Feld **Kopieren von Anl.-Nr.** auf den AssistButton, und wählen Sie dann die Nummer der Anlage, die Sie als Basis für neue Abschreibungsbücher verwenden möchten.

    Wenn Sie dieses Feld ausfüllen, enthalten die Abschreibungsfelder in den neuen Anlagen-Abschreibungsbüchern die gleichen Informationen wie die entsprechenden Felder im Anlagen-Abschreibungsbuch, aus dem Sie kopieren. Lassen Sie dieses Feld leer, wenn Sie neue Anlagen-Abschreibungsbücher mit leeren Abschreibungsfeldern erstellen möchten.  
6. Im Inforegister **Anlage** können Sie einen Filter setzen, um die Anlagen auszuwählen, für die Sie Anlagen-AfA-Bücher erstellen wollen.
7. Wählen Sie die Schaltfläche **OK** aus.

## So richten Sie Abschreibungsbuchungsarten ein:

Für jedes AfA-Buch müssen Sie festlegen, wie die verschiedenen Buchungsarten in [!INCLUDE[prod_short](includes/prod_short.md)] verarbeitet werden sollen. Beispielsweise ob Buchungen Soll- oder Habenposten sein sollen und ob die Buchungsart in der AfA-Grundlage enthalten sein soll.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Abschreibungsbücher** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das AfA-Buch aus, die Sie einrichten möchten und wählen Sie dann die Aktion **Anlagenbuchungsart Einr.** aus.
3. Füllen Sie auf der Seite **Anlagenbuchungsgruppenkarte einrichten** die notwendigen Felder aus.

    > [!NOTE]  
    >   Sie können auf der Seite **Anlagenbuchungsart Einr.** keine Zeilen löschen oder einfügen. Sie können nur die bestehenden Zeilen ändern.

Es wird empfohlen, die Einrichtung von AfA-Büchern, für die bereits Posten gebucht wurden, nicht zu ändern. Änderungen haben keinen Einfluss auf Posten, die bereits gebucht wurden, da andernfalls die Statistik für das Abschreibungsbuch verfälscht würde.

## So richten Sie Standardvorlagen und -Standardstapelverarbeitungen für Anlagen-Abschreibung ein

Sie können für jedes Abschreibungsbuch Vorgaben für Vorlagen und Erfassungsjournalen definieren. Sie nutzen diese Standards, um Zeilen aus einem Buch.-Blatt in ein anderes zu kopieren, wenn die Batchaufträge **AfA berechnen** oder **Anlagen indexieren** Buch.-Blattzeilen erstellen oder wenn Anschaffungskosten im Versicherungs Buch.-Blatt doppelt vorhanden sind.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Abschreibungsbücher** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das AfA-Buch aus, für das Sie die Standardbuch.-Blätter festlegen möchten und wählen Sie dann die Aktion **Anlagen Buch.-Blatt Einr.** aus.  
3. Falls Sie eine Standardeinrichtung für jeden einzelnen Benutzer definieren möchten, wählen Sie die Seite **Benutzer-ID** aus, um über das Fenster **Benutzer** auszuwählen.  
4. Wählen Sie in den anderen Feldern die Erf.-Journalvorlage oder den Erf.-Journalnamen, die standardmässig verwendet werden müssen.  

## Geschäftsjahr 365 Tage Feld Abschreibung

Wenn der Batchauftrag Abschreibung berechnen die Abschreibungen berechnet, verwendet der Batchauftrag normalerweise ein standardisiertes Jahr mit 360 Tagen, wobei jeder der 12 Monate 30 Tage hat.

Wenn Sie dieses Feld markieren, verwendet der Batchauftrag „Abschreibung berechnen“ stattdessen das Kalenderjahr mit 365 Tagen, wobei jeder Monat mit der gleichen Anzahl von Tagen wie im Kalender berechnet wird. Die einzige Ausnahme ist der Februar in Schaltjahren, den der Batchauftrag so behandelt, als hätte er 28 Tage und nicht 29. Aus diesem Grund besitzen alle Jahre (auch Schaltjahre) 365 Tage.

## Siehe auch 

[Anlagen einrichten](fa-setup.md)  
[Anlagen](fa-manage.md)  
[Finanzen](finance.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
