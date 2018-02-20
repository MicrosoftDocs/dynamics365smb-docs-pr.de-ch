---
title: "Einrichten von Beleg-spezifischen Inhalten und Dateianhängen für E-Mails | Microsoft Docs"
description: "Sie können Inhalt definieren, um in den Text eine E-Mail beispielsweise ein Paypal-Link einzufügen. Bestellanforderungen können auch Belege an eine E-Mail-Nachricht angehängt werden."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 03/30/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: dc22f7e06cf0686238cf1b6ab43951f3943e38a3
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="send-documents-by-email"></a>Senden von Belegen über E-Mail
Um die Inhalte von Geschäftsbelegen Ihren Geschäftspartnern rasch zu kommunizieren, wie beispielsweise Zahlungsinformationen auf Verkaufsbelegen an Debitoren, können Sie die Berichtslayoutfunktion verwenden, um dokumentspezifischen Inhalt zu definieren, der automatisch in E-Mail-Texte eingefügt wird. Weitere Informationen finden Sie unter [Berichte- und Dokumentenlayouts verwalten](ui-manage-report-layouts.md).

Um E-Mails aus [!INCLUDE[d365fin](includes/d365fin_md.md)] zu aktivieren starten Sie die die unterstützte Einrichtung **E-Mail einrichten** auf der Homepage.

Sie können praktisch alle Belegarten als Dateianhänge in E-Mails direkt im Fenster senden, das den Beleg anzeigt. Zusätzlich zum Dateianhang können Sie belegspezifische E-Mail-Texte mit Kerninformationen aus dem Beleg einrichten, der vom Standardtext gefolgt wird, der den E-Mail-Empfänger grüsst und den fraglichen Beleg vorstellt. Um Ihren Debitoren anzubieten, für Verkäufe unter Verwendung eines Zahlungsservice wie Paypal elektronisch zu bezahlen, können Sie die Paypal-Informationen und -Links auch in den E-Mail-Text einfügen.

Von allen unterstützten Belegen initiieren Sie das Übermitteln per E-Mail, indem Sie **Senden** auf gebuchten Belegen oder **Buchen und Senden** auf nicht-gebuchten Belegen auswählen.

Wenn das Feld **E-Mail** Im Fenster **Dokument senden an** auf **JA festgelegt wurde (Aufforderung für Einstellungen)**, dann wird das Fenster **Senden per E-Mail** geöffnet und mit der Kontaktperson im Feld **Zu** ergänzt und das Dokument als PDF-Datei angehängt. Geben Sie im Feld **Text** entweder den Text manuell ein oder Sie können definieren, dass das Feld mit einem belegspezifischen E-Mail-Text ausgefüllt wird, den Sie eingerichtet haben.

Nachfolgend wird beschrieben, wie der Bericht **Verkaufsrechnung** für belegspezifische E-Mail-Texte verwendet wird, wenn Sie gebuchte Verkaufsrechnungen senden.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Einen belegspezifischen E-Mail-Text für Verkaufsrechnungen einrichten
1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Berichtauswahl Verkäufe** ein. Wählen Sie dann den zugehörigen Link aus.
2. Im Fenster **Berichts-Auswahl - Verkauf** unter **Verwendung** wählen Sie **Rechnung**.
3. In einer neuen Zeile im Feld **Berichts-ID** wählen Sie beispielsweise Standardbericht 1306.
4. Wählen Sie das Kontrollkästchen **Für E-Mail-Text verwenden**.
5. Wählen Sie das Feld **E-Mail-Text-Layout-Code** und wählen Sie ein Layout aus der Liste aus.

    Berichtslayouts definieren das Format und den Inhalt des E-Mail-Texts, einschliesslich den Standardtext, der den Kernbeleginformationen im E-Mail-Text vorangeht. Sie können alle verfügbaren Berichtslayouts sehen, wenn Sie die Schaltfläche **Aus vollständiger Liste auswählen** in der Liste auswählen.
6. Um das Layout anzusehen oder zu bearbeiten, auf dem der E-Mail-Text basiert, gehen Sie zum Fenster **Benutzerdefinierte Berichtslayouts** und wählen die Aktion **Layout bearbeiten** aus.
7. Um Ihren Debitoren anzubieten, für Verkäufe unter Verwendung eines Zahlungsservice wie Paypal elektronisch zu bezahlen, können Sie die Paypal-Informationen und -Links auch in den E-Mail-Text einfügen. Weitere Informationen finden Sie unter [Aktivieren Sie Debitoren-Zahlung durch Paypal](sales-how-enable-payment-service-extensions.md)
8. Wählen Sie die Schaltfläche **OK** aus.

Wenn Sie jetzt beispielsweise die Aktion **Senden** im Fenster **Gebuchte Verkaufsrechnung** auswählen, enthält der E-Mail-Text die Beleginformationen 1306 des Berichts, der vom formatierten Standardtext entsprechend dem Berichtslayout stammt, das Sie in Schritt 5 ausgewählt haben.

Nachfolgend wird beschrieben, wie eine gebuchte Verkaufsrechnung als E-Mail mit dem Beleg gesendet wird, der als PDF-Datei angehängt ist und einen belegspezifischen E-Mail-Text enthält.

## <a name="to-send-documents-by-email"></a>Senden von Belegen über E-Mail
1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Verkaufsrechnung** ein und wählen den zugehörenden Link aus.
2. Wählen Sie die relevante gebuchte Verkaufsrechnung aus und wählen Sie die Aktion **Senden**. Das Fenster **Dokument senden an** wird geöffnet.
3. Wählen Sie im Feld **E-Mail** **Ja (Aufforderung für Einstellung)** aus. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).
4. Wählen Sie die Schaltfläche **OK** aus. Das Fenster **E-Mails senden** wird geöffnet.
5. Im Feld **Zu** geben Sie eine gültige E-Mail-Adresse ein. Der Standardwert ist die E-Mail-Adresse des Debitors.
6. Geben Sie im Feld **Betreff** einen beschreibenden Betreff ein. Der Standardwert ist der Debitorennamen und die Rechnungsnummer.
7. Im Feld **Anhang** wird die generierte Rechnung standardmässig als PDF_Datei angehängt. Wählen Sie die Suchschaltfläche, um die Datei zu öffnen oder eine andere Datei anzufügen.
8. Geben Sie im **Nachrichtentext**-Feld eine kurze Mitteilung an den Empfänger ein.

    Wenn ein dokumentspezifischer E-Mail-Text im Fenster **Berichts-Auswahl - Verkauf** eingerichtet wird, wird das Feld **Text** automatisch ausgefüllt. Weitere Informationen finden Sie unter “Einrichten eines dokumentspezifischen E-Mail-Texts für Verkaufsrechnungen” im betreffenden Abschnitt zu diesem Thema.
9. Wählen Sie die Schaltfläche **OK**, um die E-Mail zu senden.

> [!NOTE]  
>   Wenn Sie die E-Mail-Einstellungen nicht jedes Mal ändern wollen, wenn Sie ein Dokument per E-Mail senden, können Sie die Option **Ja** (Standardeinstellungen verwenden) im Feld **E-Mail** im Fenster **Dokument senden** an auswählen. In diesem Fall wird das Fenster **E-Mail senden** nicht geöffnet. Siehe dazu auch Schritt 4. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).

## <a name="see-also"></a>Siehe auch
[Verwaltung von Berichts- und Beleg-Layouts](ui-manage-report-layouts.md)  
[E-Mail einrichten](madeira-how-setup-email.md)  
[Verkaufsrechnung](sales-how-invoice-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

