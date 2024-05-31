---
title: Allgemeine Anlageninformationen einrichten
description: 'Bevor Sie den Bereich "Anlagenbuchhaltung" verwenden können, müssen Sie die Sachkonten, die Buch.-Blattvorlagen und die Buch.-Blätter und Klassencodes einrichten, die für die Buchung verwendet werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="set-up-general-fixed-assets-information"></a>Allgemeine Anlageninformationen einrichten

Bevor Sie Anlagen verwalten können, müssen Sie die standardmässigen Fibukonten, die Umlageschlüssel und Erfassungsjournalvorlage einrichten, um Anlagen zu buchen und neu zu klassifizieren. Legen Sie ausserdem eine Klassifizierungshierarchie (Klassen und Unterklassen) fest, um Ihre Anlagen zu strukturieren, und legen Sie bei Bedarf die Speicherorte fest, an denen Sie sie speichern.

## <a name="to-set-up-general-behavior-for-fixed-assets-functionality"></a>So richten Sie das allgemeine Verhalten der Anlagenfunktion ein

Legen Sie auf der Seite **Anlagen Einrichtung** das allgemeine Verhalten der Anlagenfunktionalität und seine Belegnummernserien fest.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Anlagen Einrichtung** ein, und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>So richten Sie Anlagenbuchungsgruppen ein

Verwenden von Buchungsgruppen zum Definieren von Anlagengruppen Posten in diesen Buchungsgruppen werden auf die gleichen Fibukonten gebucht.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **FA-Buchungsgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie auf der Seite **Anlagenbuchungsgruppenkarte** die notwendigen Felder aus.

    > [!NOTE]  
    >   Um sicherzustellen, dass Gegenkonten für verschiedene Anlagenbuchungen automatisch eingefügt werden, wenn Sie die Aktion **Anlagengegenkonto einfügen** in den Buch.-Blattzeilen auswählen, führen Sie den nächsten Schritt auf Grundlage der Buchung von Zuschreibungen aus.
4. Geben Sie im Inforegister **Gegenkonto** im Feld **Gegenkto. Zuschreibung** das Sachkonto ein, auf das die Gegenposten für Zuschreibungen gebucht werden sollen.

Weitere Informationen zur Verwendung der Aktion **Anlagengegenkonto einfügen** in den Anlagenerfassungsjournal-Zeilen finden Sie unter [Anlagen neu bewerten](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-journal-templates"></a>So richten Sie Anlagen Erf.-Journalvorlagen ein

Eine Vorlage ist ein vordefiniertes Layout für ein Erfassungsjournal. Eine Vorlage enthält Informationen über Verfolgungscodes, Berichte und Nummernserien. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] erstellt automatisch eine Anlagenerfassungsjournal-Vorlage, wenn Sie zum ersten Mal die Seite **Anlagen-Erf.-Journal** öffnen. Sie können aber auch andere Erfassungsjournalvorlagen einrichten.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anl. Erf.-Journalvorlagen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-set-up-fixed-asset-class-and-subclass-codes"></a>So richten Sie Codes für Anlagenklassen und -unterklassen ein

Im Anlagen können Sie eine Klassifizierungshierarchie festlegen, die zum Gruppieren von Anlagen verwendet werden kann. Die Hierarchie hat zwei Ebenen: Klassen und Unterklassen.

### <a name="fixed-asset-class-codes"></a>Anlagenklassencodes

Anlagenklassen sind die obersten Einträge in der Klassifizierungshierarchie, in der Sie Anlagen gruppieren. Verwenden Sie Klassen zum Beispiel, um Anlagen in materielle und immaterielle Anlagen zu unterteilen. Sie müssen in Ihrer Einrichtung mindestens eine Anlagenklasse erstellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **FA Anlagenklassen** ein und wählen Sie dann den zugehörigen Link.
2. Geben Sie die Codes und die Namen für die Anlagenklassen ein, die Sie erstellen möchten.

### <a name="fixed-asset-subclass-codes"></a>Anlagenunterklassencodes

Anlagenunterklassen sind die Einträge der zweiten Stufe in der Klassifizierungshierarchie, in der Sie Anlagen gruppieren. Jede Unterklasse verweist auf eine Klasse der obersten Ebene. Sie können Anlagenunterklassencodes verwenden, um Anlagen in spezifischere Kategorien einzuteilen, z. B. in Gebäude, Fahrzeuge, Möbel oder Maschinen. Sie müssen in Ihrer Einrichtung mindestens eine Anlagenunterklasse erstellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **FA Anlagensachgruppen** ein, und wählen Sie dann den zugehörigen Link.
2. Geben Sie die Codes und die Namen für die Anlagenunterklassen ein, die Sie erstellen möchten.

## <a name="start-to-register-assets"></a>Mit der Registrierung von Anlagen beginnen

Falls Sie die Anlagen in [!INCLUDE[prod_short](includes/prod_short.md)] zum ersten Mal verwenden, müssen Sie zuerst die Finanzbuchhaltungsregion einrichten, bevor Sie Anlagen einrichten können. Wie dies erfolgt, hängt davon ab, ob Sie Anlagen in die Finanzbuchhaltung integrieren.  

Die folgende Vorgehensweise wird verwendet, wenn Anlagentransaktionen in die Fibu gebucht werden.  

1. Schliessen Sie die grundlegende Einrichtung für das Anlagen ab.  
2. Füllen Sie eine Anlagenkarte für jede bestehende Anlage aus.  
3. Richtet Abschreibungsbücher für verschiedene Abschreibungszwecke ein, z. B. für MWST-Abrechnung und Finanzberichte. Legen Sie für jedes Abschreibungsbuch Grundeinstellungen, wie z. B. die Integration in die Finanzbuchhaltung, fest.

    Aktivieren Sie die Fibu-Integration, indem Sie die folgenden Schritte ausführen. Zuerst stellen Sie sicher, dass die Finanzbuchhaltungsintegration nicht für alle Abschreibungsbücher deaktiviert ist. Dann buchen Sie die Eröffnungsposten und zum Schluss aktivieren Sie die Finanzbuchhaltungsintegration.  
4. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Abschreibungsbücher** ein und wählen Sie dann den zugehörigen Link.  
5. Markieren Sie das entsprechende Abschreibungsbuch und wählen Sie dann die Aktion **Bearbeiten**, um die Seite **Abschreibungsbuch - Karte** zu öffnen.
6. Deaktivieren Sie auf dem Inforegister **Integration** alle Umschalter. Sind mehrere Abschreibungsbücher vorhanden, führen Sie diesen Schritt für jedes durch.  
7. Geben Sie im Anlagen Erf.-Journal die folgenden Zeilen für jede Anlage ein:
   * eine Zeile mit den Anschaffungskosten
   * Eine Zeile mit der kumulierten Abschreibung zum Ende des vorigen Geschäftsjahres.
   * Eine Zeile mit der kumulierten AfA vom Anfang des laufenden Geschäftsjahres bis zu dem Datum, ab dem [!INCLUDE[prod_short](includes/prod_short.md)]mit der Berechnung der Abschreibung beginnen soll.

    Falls Sie andere Anfangssalden haben, zum Beispiel Ab- und Zuschreibung, können Sie diese ebenfalls jetzt eingeben.  
8. Nachdem Sie die Erfassungsjournalzeilen für jede Anlage eingegeben und gebucht haben, aktivieren Sie die Finanzbuchhaltungsintegration in den Abschreibungsbüchern.

Falls die Anlagen nicht in die Finanzbuchhaltung integriert sind, können Sie die Schritte 6 und 8 überspringen.

## <a name="to-set-up-fixed-asset-location-codes-optional"></a>So richten Sie Anlagenstandortcodes ein (optional)

Anlagenstandortcodes legen Bezeichner dafür fest, wo sich eine Anlage befindet, beispielsweise Vertrieb, Empfang, Verwaltung, Produktion oder Lager. Sie können mit ihrer Hilfe den Standort einer Anlage erfassen. Diese Information dient beispielsweise dazu, für Versicherungen anzugeben, in welchem Bereich des Unternehmens oder an welchem Ort sich eine Anlage im Einsatz befindet.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **FA Lagerorte** ein und wählen Sie dann den zugehörigen Link.
2. Geben Sie die Codes und die Namen für die Anlagenstandorte ein, die Sie erstellen möchten.

## <a name="to-set-up-fixed-asset-allocation-keys-optional"></a>So richten Sie Anlagenumlageschlüssel ein (optional)

Verwenden Sie Umlageschlüssel, um Transaktionen verschiedenen Abteilungen oder Projekten zuzuweisen. Sie können z. B. einen Umlageschlüssel einrichten, um die Abschreibungsbeträge von Fahrzeugen zu 35 Prozent auf die Verwaltung und zu 65 Prozent auf den Vertrieb zu verteilen. Weitere Informationen finden Sie unter [Kosten und Einnahmen zuweisen](year-allocate-costs-income.md)

Verteilungsschlüssel gelten für feste Anlagenklassen, nicht für einzelne Anlagen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **FA-Buchungsgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Anlagenbuchungsgruppen** die Aktion **Verteilungen**, und wählen Sie dann eine Buchungsart aus.
3. Füllen Sie auf der Seite **Anlagenverteilungen** die notwendigen Felder aus.
4. Wiederholen Sie Schritt 2 und 3 für alle Buchungsarten, für die Sie Verteilungsschlüssel einrichten wollen.

## <a name="to-set-up-fixed-asset-journal-batches-optional"></a>So richten Sie Anlagenerfassungsjournal-Batches ein (optional)

Sie können mehrere Erfassungsjournalnamen erstellen, d. h. mehrere individuelle Erfassungsjournale für jede Erfassungsjournalvorlage. Sie können z. B. für jeden Mitarbeiter ein eigenes Erfassungsjournal benutzen, dass die Initialien des Mitarbeiters im Namen verwendet. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md).  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anl. Erf.-Journalvorlagen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die entsprechende Buch.-Blattvorlage und dann die Aktion **Buch.-Blattnamen** aus.
3. Füllen Sie auf der Seite **Anlagen Erf.-Journalnamen** die notwendigen Felder aus.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates-optional"></a>So richten Sie Vorlagen für Anlagenneuklassifizierungs-Erfassungsjournale ein (optional)

Verwenden Sie spezifische Erfassungsjournale zum Übertragen, Aufteilen oder Zusammenfassen von Anlagen. [!INCLUDE[prod_short](includes/prod_short.md)] erstellt automatisch eine Erfassungsjournalvorlage für die Anlagenneuklassifizierung, wenn Sie zum ersten Mal die Seite **Anlagenneuklassifizierungs-Erf.-Journal** öffnen. Sie können aber auch andere Neuklassifizierungs-Erfassungsjournal-Vorlagen einrichten. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md).  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **FA Reclass. Erfassungen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches-optional"></a>So richten Sie Anlagenneuklassfizierungs-Erfassungsjournal-Batches ein (optional)

Sie können mehrere Erfassungsjournalnamen erstellen, d. h. mehrere individuelle Erfassungsjournale für jede Umbuch. Erfassungsjournalvorlage. Sie können z. B. für jeden Mitarbeiter ein eigenes Erfassungsjournal benutzen, das die Initialien des Mitarbeiters im Namen verwendet. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **FA Reclass. Erfassungen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die entsprechende Buch.-Blattvorlage und dann die Aktion **Buch.-Blattnamen** aus.
3. Füllen Sie auf der Seite **Anlagen Umbuch. Erf.-Journalnamen** die notwendigen Felder aus.

## <a name="see-also"></a>Siehe auch

[Anlagen einrichten](fa-setup.md)  
[Anlagen – Übersicht](fa-manage.md)  
[Finanzen](finance.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
