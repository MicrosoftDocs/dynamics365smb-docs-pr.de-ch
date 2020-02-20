---
title: Abschreibungsmethoden einrichten| Microsoft Docs
description: Sie geben in einem Abschreibungsbuch an, wie Sie Anlagen abschreiben oder anzeigen möchten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 01/29/2020
ms.author: sgroespe
ms.openlocfilehash: 4f11ac5080c8601ce8ae46178bf5c1ed8bb646e1
ms.sourcegitcommit: 1c286468697d403b9e925186c2c05e724d612b88
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 01/31/2020
ms.locfileid: "2999585"
---
# <a name="set-up-fixed-asset-depreciation"></a>Richten Sie eine neue Anlagenabschreibung ein
 Sie können unterschiedliche Abschreibungsmethoden für Bilanzen und Steuern verwenden. Viele Grossunternehmen verwenden die lineare Abschreibung in ihren Bilanzen, da dies im Allgemeinen höhere Gewinne anzeigt. Für Einkommenssteuerzwecke verwenden viele Unternehmen jedoch eine beschleunigte Abschreibungsmethode, wie z. B. die degressive Abschreibung. Sie definieren die Abschreibungsmethode einer Anlage mit dem Feld **Abschreibungsmethode** auf der Seite **Anlagenkarte**. Weitere Informationen zu den verschiedenen Methoden finden Sie unter [Abschreibungsmethoden](fa-depreciation-methods.md).

 In Abschreibungsbüchern definieren Sie die verschiedenen Arten, wie die Abschreibungen für Ihr unterschiedliches Anlagen berechnet werden müssen. In jedem Buch können Sie individuelle Abschreibungsbedingungen angeben. Es ist zum Beispiel möglich, dass eine Anlage in einem Buch über einen Zeitraum von drei Jahren abgeschrieben wird und in einem anderen über fünf Jahre.

 Nachdem Sie die erforderlichen AfA-Bücher erstellt haben, müssen Sie jeder Anlage mindestens ein AfA-Buch zuweisen. Ein Abschreibungsbuch, das einer Anlage zugewiesen ist, wird als Anlagen-Abschreibungsbuch bezeichnet. Sie können beliebig viele Abschreibungsbücher für eine Anlage einrichten. 

## <a name="to-create-a-depreciation-book"></a>So erstellen Sie ein Anlagen-Abschreibungsbuch
In einem Abschreibungsbuch können Sie festlegen, wie eine Anlage abgeschrieben wird. Sie können mehrere Abschreibungsbücher einrichten, um die verschiedenen Abschreibungsarten zu erleichtern.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Abschreibungsbücher** ein, und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Abschreibungsbuch Liste** wählen Sie die Aktion **Neu** aus.
3. Füllen Sie im Inforegister **Abschreibungsbuchkarte** die Seite nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Hinweis: Sie können Anlagentransaktionen auf der Seite **Anlagen Fibu Erf.-Journal** oder auf der Seite **Anlagen Erf.-Journal** erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind. Führen Sie den nächsten Schritt aus, um festzulegen, welche Art von Erf.-Journal für die verschiedenen Anlagenaktivitäten standardmässig verwendet wird.
4. Aktivieren Sie im Inforregister **Integration** das Kontrollkästchen für jede Anlagenaktivität, deren Transaktionen Sie mithilfe der Seite **Anlagen Fibu Erf.-Journal** buchen möchten.
5. Wiederholen Sie die Schritte 2 bis 4 für jede Abschreibungs- oder Buchungsmethode, die Sie den Anlagen als Abschreibungsbuch zuweisen möchten.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>So verknüpfen Sie ein Abschreibungsbuch mit einer Anlage
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Anlagen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Anlage aus, für die Sie ein Anlagen-Abschreibungsbuch einrichten möchten.
3. Füllen Sie im Inforegister **AfA-Buch** die Felder nach Bedarf aus.
4. Wenn Sie mehrere AfA-Bücher der Anlage zuweisen müssen, wählen Sie die Aktion **Weitere AfA-Bücher hinzufügen** aus.
5. Alternativ wählen Sie die Aktion **AfA-Bücher** aus , um eine oder mehrere Anlagen-AfA-Bücher anzugeben.

    > [!NOTE]  
    >   Hinweis: Wenn Sie die manuelle Abschreibungsmethode verwenden, müssen Sie die Abschreibung manuell im Anlagen Fibu Erf.-Journal eingeben. Die Funktion **AfA berechnen** berücksichtigt keine Anlagen mit der AfA-Methode "Manuell". Sie können diese Methode für Anlagen verwenden, die nicht abgeschrieben werden, wie z. B. Land.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>So weisen Sie ein Abschreibungsbuch mehreren Anlagen mit einer Stapelverarbeitung zu
Falls Sie ein AfA-Buch mit mehreren Anlagen verknüpfen möchten, können Sie die Stapelverarbeitung **Anlagen-AfA-Buch erstellen** verwenden, um die Anwendung die erforderlichen AfA-Bücher automatisch erstellen zu lassen.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Anlagen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Anlage aus, die Sie einrichten möchten und der ein AfA-Buch zugewiesen werden soll, und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Wählen Sie auf der Seite **Abschreibungsbuch - Karte** die Aktion **Anlagen-Abschreibungsbücher erstellen** aus.
4. Füllen Sie auf der Seite **Anlagen-Abschreibungsbuch erstellen** das Fenster **Abschreibungsbuch** aus.
5. Klicken Sie im Feld **Kopieren von Anl.-Nr.** auf den AssistButton, und wählen Sie dann die Nummer der Anlage, die Sie als Basis für neue Abschreibungsbücher verwenden möchten.

    Wenn Sie dieses Feld ausfüllen, enthalten die Abschreibungsfelder in den neuen Anlagen-Abschreibungsbüchern die gleichen Informationen wie die entsprechenden Felder im Anlagen-Abschreibungsbuch, aus dem Sie kopieren. Lassen Sie dieses Feld leer, wenn Sie neue Anlagen-Abschreibungsbücher mit leeren Abschreibungsfeldern erstellen möchten.  
6. Im Inforegister **Anlage** können Sie einen Filter setzen, um die Anlagen auszuwählen, für die Sie Anlagen-AfA-Bücher erstellen wollen.
7. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-set-up-depreciation-posting-types"></a>So richten Sie Abschreibungsbuchungsarten ein:
Für jedes AfA-Buch müssen Sie festlegen, wie die verschiedenen Buchungsarten in [!INCLUDE[d365fin](includes/d365fin_md.md)] verarbeitet werden sollen. Beispielsweise ob Buchungen Soll- oder Habenposten sein sollen und ob die Buchungsart in der AfA-Grundlage enthalten sein soll.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Abschreibungsbücher** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das AfA-Buch aus, die Sie einrichten möchten und wählen Sie dann die Aktion **Anlagenbuchungsart Einr.** aus.
3. Füllen Sie auf der Seite **Anlagenbuchungsgruppenkarte einrichten** die notwendigen Felder aus.

    > [!NOTE]  
    >   Sie können auf der Seite **Anlagenbuchungsart Einr.** keine Zeilen löschen oder einfügen. Sie können nur die bestehenden Zeilen ändern.

Es wird empfohlen, die Einrichtung von AfA-Büchern, für die bereits Posten gebucht wurden, nicht zu ändern. Änderungen haben keinen Einfluss auf Posten, die bereits gebucht wurden, da andernfalls die Statistik für das Abschreibungsbuch verfälscht würde.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>So richten Sie Standardvorlagen und -Standardstapelverarbeitungen für Anlagen-Abschreibung ein
Sie können für jedes Abschreibungsbuch Vorgaben für Vorlagen und Erfassungsjournalen definieren. Sie nutzen diese Standards, um Zeilen aus einem Buch.-Blatt in ein anderes zu kopieren, wenn die Batchaufträge **AfA berechnen** oder **Anlagen indexieren** Buch.-Blattzeilen erstellen oder wenn Anschaffungskosten im Versicherungs Buch.-Blatt doppelt vorhanden sind.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Abschreibungsbücher** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das AfA-Buch aus, für das Sie die Standardbuch.-Blätter festlegen möchten und wählen Sie dann die Aktion **Anlagen Buch.-Blatt Einr.** aus.  
3. Falls Sie eine Standardeinrichtung für jeden einzelnen Benutzer definieren möchten, wählen Sie die Seite **Benutzer-ID** aus, um über das Fenster **Benutzer** auszuwählen.  
4. Wählen Sie in den anderen Feldern die Erf.-Journalvorlage oder den Erf.-Journalnamen, die standardmässig verwendet werden müssen.  

## <a name="see-also"></a>Siehe auch
[Anlagen einrichten](fa-setup.md)  
[Anlagen](fa-manage.md)  
[Finanzen](finance.md)  
[Erste Schritte](product-get-started.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
