---
title: Beleg-Layouts Debitoren oder Kreditoren zuweisen
description: 'Verwenden Sie Beleglayouts, um das Aussehen und Format von Belegen wie Rechnungen und Bestellungen zu steuern, die Sie an Debitoren und Kreditoren senden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '21, 9650'
ms.date: 07/05/2024
ms.service: dynamics-365-business-central
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Beleglayouts für Debitoren und Kreditoren definieren

Beleglayouts verwenden Berichtslayouts, um das Aussehen und Format von Belegen zu definieren, die Sie an Debitor und Kreditor senden. Business Central bietet Standardlayouts, aber Sie können auch angepasste Layouts für jeden Ihrer Geschäftspartner erstellen. Weitere Informationen finden Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md). Sie wählen Standard- und angepasste Beleglayouts aus Debitor- und Kreditorenkarten aus, indem Sie die Aktion **Dokumentenlayouts** wählen. Der Wert im Feld **Verwendung** definiert den Prozess, für den das Beleg-Layout verwendet wird. Für Debitor können Sie zum Beispiel **Erinnerung**, **Versand** und **Bestätigung** als Beleglayout verwenden.

Beleglayouts können Ihnen auch Zeit sparen, wenn Sie Belege per E-Mail an Debitor- oder Kreditor-Kontakte senden. Für jedes Layout, das Sie dem Debitor oder Kontakt zuweisen, können Sie eine oder mehrere E-Mail-Adressen angeben. So können Sie beispielsweise eine Rechnung an die Kontakte im Einkauf und im Lager des Debitors senden. Das Hinzufügen von Kontakt-E-Mail-Adressen ist ganz einfach. Auf der Seite  **Dokumentlayouts**  können Sie mit der Aktion  **Auswählen „E-Mail aus Kontakten“**  aus einer Liste der Kontakt-E-Mail-Adressen auswählen, die Sie für den Kunden oder Lieferanten registriert haben. Sie können E-Mail-Adressen auch manuell hinzufügen. Wenn Sie mehrere Adressen eingeben, trennen Sie diese mit einem Semikolon und fügen Sie keine Leerzeichen zwischen den Adressen ein.

Bevor Sie festlegen können, welches Beleglayout für welche Prozesse verwendet werden soll und an welchen Kontakt der Beleg gesendet werden soll, müssen Sie alle verfügbaren Berichte (Belege) von der Seite **Berichtsauswahl** laden. Sie können die Belege schnell laden, indem Sie die Aktion **Kopieren aus Berichtsauswahl** auf der Seite **Dokumentlayouts** verwenden.

Die Schritte in den folgenden Abschnitten beschreiben, wie Sie die Layouts für Verkaufsbelege auf der Seite **Kundenkarte** definieren. Für Kreditor sind die Schritte auf der Seite **Lieferantenkarte** die gleichen.

## <a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer"></a>So laden Sie die Standardbeleg-Layouts für Verkaufsbelege für einen Debitor

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Seite **Kundenkarte** für den Debitor, und wählen Sie dann die Aktion **Dokumentenlayouts**.
3. Auf der Seite **Beleglayouts** wählen Sie die Aktion **Aus Berichtsauswahl kopieren** aus.

Auf der Seite **Beleglayouts** werden alle Layouts angezeigt, die für Verkaufsbelege verfügbar sind. 

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>So wählen Sie ein benutzerdefiniertes Berichtslayout aus, das für das Verkaufsbeleglayout verwendet werden soll

Die folgenden Schritte setzen voraus, dass Sie bereits einen benutzerdefinierten Bericht Layout für den Dokumenttyp haben. Wenn Sie noch keinen benutzerdefinierten Bericht Layout haben, müssen Sie zuerst einen erstellen. Weitere Informationen finden Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Seite **Kundenkarte** für den Debitor, und wählen Sie dann die Aktion **Dokumentenlayouts**.
3. Auf der Seite **Beleglayouts** in der Zeile für ein Berichtslayout, für das Sie ein benutzerdefiniertes Layout verwenden möchten, wählen Sie das Feld **Benutzerdefinierte Layoutbeschreibung** aus.

   > [!TIP]
   > Standardmäßig ist das benutzerdefinierte Beschreibungsfeld Layout ausgeblendet. Wenn das Feld nicht verfügbar ist, können Sie die Seite personalisieren, um es hinzuzufügen. Um die Seite zu personalisieren, wählen Sie das Symbol :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="„Einstellungen“."::: Symbol und wählen Sie dann  **Personalisieren**. Weitere Informationen zum Personalisieren von Seiten finden Sie unter  [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

1. Wählen Sie auf der Seite **Benutzerdefinierte Berichtslayouts** das Dokumentenlayout aus, das Sie für die Art des Verkaufsbelegs verwenden möchten. Weitere Informationen finden Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).

## <a name="to-specify-which-contact-receives-which-document-layout-for-a-customer"></a>So legen Sie fest, welcher Kontakt welches Dokument erhält Layout für einen Kunden

Um Zeit zu sparen, wenn Sie Belege per E-Mail an Debitor- und Kreditor-Kontakte senden, geben Sie deren E-Mail-Adressen in den Beleglayouts an. So können Sie z.B. Kontoauszüge immer an die Debitor-Kontakte und Verkaufsaufträge an die Einkäufer bzw. Verkäufer/Einkäufer senden.

1. Auf der Seite **Beleglayouts** in der Zeile für ein Berichtslayout, das Sie an einen bestimmten Kontakt für den Debitor senden möchten, wählen Sie die Aktion **E-Mail aus Kontakten auswählen** aus.
2. Wählen Sie auf der Seite **Kontakte** einen oder mehrere Kontakte aus, und wählen Sie dann **OK**.

## <a name="see-also"></a>Siehe auch

[Benutzerdefinierte Berichtslayouts aktualisieren](ui-update-report-layouts.md)  
[Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md)  
[Importieren und Exportieren eines benutzerdefinierten Berichts- oder Beleglayouts](ui-how-import-and-export-report-layout.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
