---
title: So finden Sie gebuchte Belege ohne eingehende Belege
description: 'Sie können nach Fibuposten für gebuchte Einkaufs- und Verkaufsrechnungen suchen, für die es keine elektronischen Belege gibt, wie z.B. importierte Rechnungen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
---
# So finden Sie gebuchte Belege ohne zugehörige eingehende Belege

Auf den Seiten **Kontenplan** und **Fibuposten** können Sie eine Suchfunktion verwenden, um Fibuposten für gebuchte Kauf- und Verkaufsbelege zu finden, die keine eingehenden Datensätze haben, und diese dann zentral mit bestehenden Datensätzen verknüpfen oder neue mit angehängten Belegdateien erstellen.

## So finden Sie gebuchte Belege ohne zugehörige eingehende Belege

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie eine Zeile für ein Fibukonto aus, für dessen Fibuposten Sie gebuchte Einkaufs- und Verkaufsbelege abrufen möchten, zu denen keine eingehenden Belege vorhanden sind, und wählen Sie dann die Aktion **Gebuchte Belege ohne eingehenden Beleg**.
3. Alternativ wählen Sie die Aktion **Posten** aus.
4. Wählen Sie auf der Seite **Fibuposten** die Aktion **Gebuchte Belege ohne eingehende Belege** aus.

Daraufhin wird die Seite **Gebuchte Belege ohne eingehenden Beleg** geöffnet, das die gebuchten Einkaufs- und Verkaufsbelege ohne zugehörige eingehende Belege enthält, die von Fibuposten auf dem Fibukonto dargestellt werden, für das Sie das Fenster geöffnet haben. Die Seite kann maximal 1000 Zeilen anzeigen. Standardmässig enthält das Feld **Datumsfilter** daher einen Filter, der die Anzeige auf Einträge beschränkt, deren Buchungsdatum zwischen dem Beginn der Buchhaltungsperiode und dem Arbeitsdatum liegt.

## So verknüpfen Sie gefundene Belege mit vorhandenen eingehenden Belegen

1. Wählen Sie auf der Seite **Gebuchte Belege ohne eingehenden Beleg** die Zeile für einen gebuchten Beleg aus, den Sie mit einem vorhandenen eingehenden Beleg verknüpfen möchten, und wählen Sie dann die Aktion **Eingehenden Beleg auswählen** aus.
2. Wählen Sie auf der Seite **Eingehende Belege** den eingehenden Beleg aus, den Sie der gefundenen Buchung zuordnen möchten, und klicken Sie anschliessend auf die Schaltfläche **OK**.
3. Auf der Seite **Gebuchte Belege ohne eingehenden Beleg** wird der gewählte eingehende Beleg nun mit dem gebuchten Beleg verknüpft und in der Infobox **Eingehende Belegdateien** angezeigt.

Wenn auf der Seite **Eingehende Belege** kein entsprechender Datensatz vorhanden ist, können Sie ihn erstellen. Weitere Informationen finden Sie unter [So geht's: Eingehende Belege erstellen](across-how-create-income-document-records.md).

## Siehe verwandte [Microsoft Schulungen](/training/modules/incoming-documents-dynamics-365-business-central/)

## Siehe auch 

[Erstellen von Datensätzen für eingehende Belege](across-how-create-income-document-records.md)
[Verwenden Sie OCR, um PDF- und Bilddateien in elektronische Belege zu verwandeln](across-how-use-ocr-pdf-images-files.md)
[Erstellen Sie Datensätze für eingehende Belege direkt aus Belegen und Einträgen](across-how-connect-disconnect-income-document-records.md)
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
