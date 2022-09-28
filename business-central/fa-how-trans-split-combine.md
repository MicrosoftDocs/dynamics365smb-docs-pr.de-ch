---
title: Anlagen umbuchen
description: Beschreibt, wie eine Anlage umgelagert wird, um sie mit anderen Anlagen aufzusplitten oder zu kombinieren.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5638, 5636, 5640, 5637
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 00565ae00664005c9b968eb3e34e4cb7e6130966
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531527"
---
# <a name="transfer-split-or-combine-fixed-assets"></a>Übertragen, Teilen oder Kombinieren von Anlagen.

Das Anlagen-Erfassungsjournal wird zum Transferieren, Aufteilen und/oder Zusammenfassen von Anlagen verwendet. Sie können die Ergebnisse der Anlagenumbuchung mit dem Bericht **Anlagenspiegel** anzeigen oder ausdrucken.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>So übertragen Sie eine Anlage an eine andere Kostenstelle.

Es kann erforderlich sein, Anlagen an andere Kostenstellen zu transferieren, wenn Sie z. B. eine Anlage in der Bauzeit in der Produktion aufstellen und nach der Fertigstellung in die Verwaltung transferieren.  

1. Richten Sie eine neue Anlage ein. Geben Sie die neue Abteilung als Dimension ein.  
2. Weisen Sie der neuen Anlage ein Anlagen-Abschreibungsbuch zu. Weitere Informationen finden Sie unter [Anschaffen von Anlagen](fa-how-acquire.md).
3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen UmErfassungsjournale** ein und wählen Sie dann den zugehörigen Link.
4. Erstellen Sie eine Erf.-Journalzeile, in der das Feld **Anlagennr.** die ursprüngliche Anlage enthält und das Feld **Neue Anlagennr.** die neue Anlage, die verschoben werden soll. Füllen Sie die anderen Felder aus entsprechend aus.  
5. Wählen Sie die Aktion **Umbuchen** aus.

    Es werden zwei Zeilen im Anlagen Fibu Erf.-Journal unter Verwendung der Vorlage und dem Erf.-Journalnamen, die Sie auf der Seite **Anlagen Erf.-Journal Einr.** für das gewählte Abschreibungsbuch angegeben haben, erstellt. Weitere Informationen finden Sie unter [Anlagen-Abschreibungsbücher automatisch einrichten](fa-how-setup-depreciation.md).
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen Fibu Erfassungsjournale** ein, und wählen Sie dann den zugehörigen Link.    
7. Auf der Seite **Anlagen Fibu Erf.-Journal** wählen Sie die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 4 und 5 ausgeführt haben.

Falls Sie Anschaffungskosten für eine Anlage gebucht haben, können Sie das Anlagen Umlagerungserfassungsjournal verwenden, um die Anschaffungskosten auf mehrere Anlagen aufzusplitten.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>So teilen Sie eine Anlage in drei Anlagen
Sie können eine Anlage in mehrere Anlagen aufteilen, zum Beispiel wenn Sie eine Anlage auf drei verschiedene Abteilungen verteilen müssen. In diesem Fall können Sie z. B. 25 Prozent der Anschaffungskosten und der Abschreibung der ursprünglichen Anlage auf die zweite Anlage buchen und 45 Prozent auf die dritte Anlage. Die restlichen 30 Prozent verbleiben bei der ursprünglichen Anlage.

1. Richten Sie zwei neue Anlagen ein. Geben Sie die relevanten Abteilungen als Dimensionen ein.  
2. Weisen Sie den zwei neuen Anlagen Anlagen-AfA-Bücher zu. Weitere Informationen finden Sie unter [Anschaffen von Anlagen](fa-how-acquire.md).
3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen UmErfassungsjournale** ein und wählen Sie dann den zugehörigen Link.
4. Erstellen Sie zwei Umlagerungs Buch.-Blattzeilen, eine für jede neue Anlage.
5. Wählen Sie in der ersten Zeile die zweiten Anlage im Feld **Neue Anlagennr.** und 25 im Feld **Buchen Sie Anschaffungskosten um %** Feld ein.
6. Wählen Sie in der ersten Zeile die zweiten Anlage im Feld **Neue Anlagennr.** und 40 im Feld **Buchen Sie Anschaffungskosten um %** Feld ein.
7. In beiden Zeilen aktivieren Sie die Kontrollkästchen **Anschaffung umbuchen** und **Normal-AfA umbuchen**.  
8. Wählen Sie die Aktion **Umbuchen** aus.  

    Es werden zwei Zeilen im Anlagen Fibu Erf.-Journal unter Verwendung der Vorlage und dem Erf.-Journalnamen, die Sie auf der Seite **Anlagen Erf.-Journal Einr.** für das gewählte Abschreibungsbuch angegeben haben, erstellt. Weitere Informationen finden Sie unter [Anlagen-Abschreibungsbücher automatisch einrichten](fa-how-setup-depreciation.md).    
9. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anlagen Fibu Erfassungsjournale** ein, und wählen Sie dann den zugehörigen Link.
10. Auf der Seite **Anlagen Fibu Erf.-Journal** wählen Sie die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 4 und 8 ausgeführt haben.

## <a name="to-combine-two-fixed-assets-into-one"></a>So fassen Sie zwei Anlagen in einer zusammen

Sie können mehrere Anlage in einer Anlagen zusammenfassen, wenn Sie zum Beispiel verteilte Anlagen in eine Abteilung verschieben. Wenn Sie Anschaffungskosten und Abschreibung für die Anlagen, die verschoben werden sollen, gebucht haben, werden diese Werte in einer einzelnen Anlage zusammengefasst.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anlagen UmErfassungsjournale** ein und wählen Sie dann den zugehörigen Link.
2. Erstellt das Umlagerungs-Erf.-Journal, in dem das **Anlagennr.** Feld die urspr. Anlage enthält, und das Feld **Neue Anlagennr.** die neue Anlage enthält, mit der sie kombiniert werden soll.
3. Lassen Sie das Feld **Anschaffung % umbuchen** leer, um die gesamten Anschaffungskosten zu verschieben/zusammenzufassen.  
4. Aktivieren Sie die Kontrollkästchen **Anschaffung umbuchen** und **Normal-AfA umbuchen**.
5. Wählen Sie die Aktion **Umbuchen** aus.

    Es werden zwei Zeilen im Anlagen Fibu Erf.-Journal unter Verwendung der Vorlage und dem Erf.-Journalnamen, die Sie auf der Seite **Anlagen Erf.-Journal Einr.** für das gewählte Abschreibungsbuch angegeben haben, erstellt. Weitere Informationen finden Sie unter [Anlagen-Abschreibungsbücher automatisch einrichten](fa-how-setup-depreciation.md).   
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anlagen-Fibu Erfassungsjournale** ein, und wählen Sie dann den zugehörigen Link.
7. Auf der Seite **Anlagen Fibu Erf.-Journal** wählen Sie die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 2 und 5 ausgeführt haben.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>So zeigen Sie geänderte Abschreibungsbuch-Werte aufgrund von Anlagenumbuchung an

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anlagenspiegel 02** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder je nach Bedarf aus.
3. Klicken Sie auf die Schaltfläche **Drucken** oder **Vorschau**.  

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/reclassify-fixed-assets/)

## <a name="see-also"></a>Siehe auch 

[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
