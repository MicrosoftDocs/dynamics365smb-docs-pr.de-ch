---
title: Anlagen anschaffen| Microsoft Docs
description: "Sie können Anlagen einrichten, ein Abschreibungsbuch zuweisen und Anlagen-Anschaffungskosten aufzeichnen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 9f2dcd6328c86117a927aeaeaeba075c421db046
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="acquire-fixed-assets"></a>Erworbene Anlagen
Sie müssen für jede Anlage eine Karte mit den entsprechenden Informationen über die Anlage einrichten. Sie können Gebäude oder Produktionseinrichtungen als Hauptanlage mit einer Komponentenliste einrichten und sie unterschiedlich gruppieren, z. B. nach Klasse, Abteilung oder Standort. Vor der Anschaffung muss für jede Anlage ein Abschreibungsbuch eingerichtet und zugewiesen werden.

Wenn eine Anlage eingerichtet und ein Abschreibungsbuch zugewiesen ist, müssen Sie die Anlage erwerben. Um eine Anlage zu erwerben, erfassen Sie seine Anschaffungskosten im entsprechenden Sachkonto, Bankkonto oder Kreditor, indem Sie eine Anschaffungstransaktion im Fenster **Anlagen Fibu Buch.-Blatt** buchen. Sie können das Fenster **Unterstützte Anlagenanschaffung** verwenden, um die erforderlichen Fibu Buch.-Blattzeilen automatisch zu erstellen und zu buchen.

Der Restwert ist der verbleibende Wert einer Anlage, die nicht mehr verwendet werden kann. Sie können den Restbetrag zusammen mit den Anschaffungskosten buchen. Weitere Informationen finden Sie unter [Anlagen abschreiben oder amortisieren](fa-how-depreciate-amortize.md).

Die Indexierung wird verwendet, um die Werte allgemeinen Preisänderungen anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um die Anschaffungskosten zu Wiederbeschaffungskosten zu ermitteln.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a>So erstellen Sie eine Anlage und erwerben diese automatisch
Nachfolgend wird beschrieben, wie eine Anlage erstellt und erhalten wird, indem Sie das Fenster **Unterstützte Anlagenanschaffung** verwenden, um die entsprechenden Fibu Buch.-Blattzeilen zu erstellen und zu buchen. Sie können die Buch.-Blattzeilen auch manuell erstellen und buchen. Weitere Informationen finden Sie im Abschnitt "Wie Anlagenanschaffungen mit dem Anlagen Fibu Erf.-Journal manuell gebucht werden".

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie dann bei Bedarf die Felder im Inforegister **Allgemein** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Füllen Sie im Inforegister **AfA-Buch** die Felder nach Bedarf aus. Dieser Schritt weist eine Anlage einem Abschreibungsbuch zu.  
4. Wenn Sie mehrere AfA-Bücher der Anlage zuweisen müssen, wählen Sie die Aktion **Weitere AfA-Bücher hinzufügen** aus. Weitere Informationen finden Sie im Abschnitt "So weisen Sie ein Abschreibungsbuch einer Anlage zu" [ Einrichten von Anlagen-Abschreibungsbüchern](fa-how-setup-depreciation.md).

    Wenn alle Felder, die benötigt werden, um eine Anlage zu erwerben, ausgefüllt sind, erscheint oben auf der Seite die Benachrichtigung **Sie sind bereit, die Anlage zu erwerben**.
5. Wählen Sie Aktion **Erwerben** in der Benachrichtigung aus.
6. Befolgen Sie die Schritte im Fenster **Unterstützte Anlagenanschaffung** Fenster, um die automatische Beschaffung der Anlage abzuschliessen.

> [!NOTE]  
>   Sie können Anchaffungskosten auch als auch Habenbeträge buchen. In diesem Fall sollten Sie daran denken, dass der Wert im Feld **Anschaffungskosten inklusive MwSt** mit einem Minuszeichen eingegeben werden muss, um eine Gutschrift anzugeben.

Wenn Sie **Fertigstellen** auswählen, wird das Feld **Buchwert** im Fenster **Anlagenkarte** ausgefüllt und gibt an, dass die Anlage zu den angegebenen Anschaffungskosten erworben wurde.  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>So richten Sie Komponentenlisten für Hauptanlagen ein
Sie können Ihre Anlagen in Hauptanlagen und deren Komponenten gliedern. Sie können dies z. B. für eine Produktionsanlage verwenden, die aus vielen Teilen besteht, die auf diese Weise gruppiert werden sollen.  

Sowohl für die Hauptanlage als auch für die Unteranlagen müssen Anlagenkarten eingerichtet werden. Nachdem Sie eine Komponentenübersicht eingerichtet haben, füllt [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch die Felder **Hauptanlage/Komponente** und **Komponente/Hauptanlage** auf den Anlagenkarten aus.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Anlage, die die Hauptanlage ist, und wählen die Aktion **Hauptanl. Unteranlagen** aus.
3. Im Fenster **Unteranlagen** wählen Sie **Anlagennr.** aus und wählen Sie die Anlage aus, die Sie als Komponente der Hauptanlage hinzufügen möchten.
4. Schliessen Sie das Fenster.
5. Wiederholen Sie die Schritte 3 und 4 für jede Unteranlage, die Sie hinzufügen möchten.
6. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
7. Aktivieren Sie das Kontrollkästchen **Buchen auf Hauptanl. erlaubt**.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a>So buchen Sie eine Anlagenanschaffungen mit dem Anlagen Fibu Erf.-Journal manuell
Nachfolgend wird beschrieben, wie eine Anlage manuell erworben wird, indem Zeilen im Fenster **Anlagen Fibu Buch.-Blatt** erstellt und gebucht werden. Sie können eine Anlage auch automatisch erwerben, indem Sie das Fenster **Unterstützte Anlagenanschaffung** verwenden. Weitere Informationen finden Sie unter Schritt 5 im Abschnitt "So erstellen Sie eine Anlage und erwerben diese automatisch".

> [!NOTE]  
>   Sie können Anchaffungskosten auch als auch Habenbeträge buchen. In diesem Fall sollten Sie daran denken, dass der Wert im Feld **Betrag** mit einem Minuszeichen eingegeben werden muss, um eine Gutschrift anzugeben.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.
2. Im Fenster **Anlagen Fibu Buch.-Blatt** wählen Sie im Feld **Anlagenbuchungsart** die **Anschaffungskosten** aus.
3. Füllen Sie die verbleibenden Felder je nach Bedarf aus.
4. Wählen Sie die Aktion **Buchen** aus.  

> [!TIP]  
>   Wenn Sie bei der Buchung von Anschaffungskosten im Anlagen Fibu Erf.-Journal das Feld **Versicherungsnr.** ausfüllen, bucht [!INCLUDE[d365fin](includes/d365fin_md.md)] die Anwendung die Anschaffungskosten der Anlage auch für die Versicherungsposten. Weitere Informationen finden Sie unter [Versichern von Anlagen](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>So stornieren Sie eine Anschaffungskostenbuchung für eine Anlage
Wenn Ihnen beim Buchen von Anschaffungskosten ein Fehler unterläuft, können Sie den Posten mithilfe der Stapelverarbeitung **Anlagenposten storn.** entfernen und anschliessend den korrekten Anschaffungsposten buchen. Die fehlerhaften Posten werden in das Fenster **Anlagenstornoposten** übertragen.

Wenn Sie also beispielsweise eine Anschaffung mit dem falschen Datum gebucht haben, müssen Sie sie so schnell wie möglich korrigieren, da das Anlagenbuchungsdatum für viele kritische Berechnungen verwendet wird.

> [!IMPORTANT]  
>   Sie können die Funktion **Transaktion stornieren** nicht für Anlagenposten verwenden.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Anlageneintrag stornieren** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie die Schaltfläche **OK**, um den Batchauftrag zu starten.
4. Wenn der falsche Posten oder die falschen Posten storniert wurden, können Sie mit dem Buchen der korrekten Anschaffungskosten fortfahren.

Um Posten für mehrere Anlagen gleichzeitig abzubrechen, verwenden Sie die Stapelverarbeitung **Anlagenposten stornieren**.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>So buchen Sie den Restbetrag zusammen mit den Anschaffungskosten
Sie können den Restwert zusammen mit den Anschaffungskosten aus einem Anlagen Fibu Erf.-Journal buchen.    

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Anlageneintrag stornieren** ein. Wählen Sie dann den zugehörigen Link aus.
2. Erstellen Sie eine Anschaffungs-Erf.-Journalzeile. Weitere Informationen finden Sie im Abschnitt "Wie Anlagenanschaffungen mit dem Anlagen Fibu Erf.-Journal manuell gebucht werden".
3. Geben Sie im Feld **Restwert** in der Rechnungszeile den Restwertbetrag als Haben (mit einem Minuszeichen) ein.
4. Wählen Sie die Aktion **Buchen** aus.

> [!NOTE]  
>   Die Buchungsart R**estwert** steht nur im Fenster **Anlagen Buch.-Blatt** zur Verfügung. Sie ist im Fenster **Anlagen Fibu Buch.-Blatt** nicht verfügbar, weil der Restbetrag nie in der Finanzbuchhaltung gebucht wird.

## <a name="see-also"></a>Siehe auch
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Erste Schritte](product-get-started.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

