---
title: "Suche nach Belegen ohne Dateianhänge| Microsoft Docs"
Description: "Sie können nach Fibuposten für gebuchte Einkaufs- und Verkaufsbelege suchen, die keine eingehenden  elektronische Belege haben, wie importierte Rechnungen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 263146eca72e4c83b4ad6887a84844e7aa15dd87
ms.contentlocale: de-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-find-posted-documents-without-incoming-document-records"></a>So wird's gemacht: Gebuchte Belege ohne Eingangsbelege finden
In den Fenstern **Kontenplan** und **Sachposten** können Sie eine Suchfunktion verwenden, um Sachposten für gebuchte Einkaufs- und Verkaufsbelege zu finden, für die keine eingehende Belegdatensätze vorhanden sind, und dann zentral eine Verknüpfung zu vorhandenen Datensätzen herstellen oder neue mit angefügten Belegdateien erstellen.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>So finden Sie gebuchte Belege ohne zugehörige Eingangsbelege
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben **Kontenplan** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie eine Zeile für ein Fibukonto aus, für dessen Fibuposten Sie gebuchte Einkaufs- und Verkaufsbelege abrufen möchten, zu denen keine Eingangsbelege vorhanden sind, und wählen Sie dann die Aktion **Gebuchte Belege ohne Eingangsbeleg**.
3. Alternativ wählen Sie die Aktion **Ledger Entries** aus.
4. Wählen Sie im Fenster **Sachposten** die Aktion **Gebuchte Belege ohne Eingangsbelege** aus.

Daraufhin wird das Fenster **Gebuchte Belege ohne Eingangsbeleg** geöffnet, dass die gebuchten Einkaufs- und Verkaufsbelege ohne zugehörige Eingangsbelege enthält, die von Fibuposten auf dem Fibukonto dargestellt werden, für das Sie das Fenster geöffnet haben. Das Fenster kann maximal 1000 Zeilen anzeigen. Standardmäßig enthält das Feld **Datumsfilter** daher einen Filter, der die Anzeige auf Einträge beschränkt, deren Buchungsdatum zwischen dem Beginn der Buchhaltungsperiode und dem Arbeitsdatum liegt.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>So verknüpfen Sie gefundene Belege mit vorhandenen Eingangsbelegen
1. Wählen Sie im Fenster **Gebuchte Belege ohne Eingangsbeleg** die Zeile für einen gebuchten Beleg aus, den Sie mit einem vorhandenen Eingangsbeleg verknüpfen möchten, und wählen Sie dann die Aktion **Eingehenden Beleg auswählen** aus.
2. Wählen Sie im Fenster **Eingehende Belege** den Eingangsbeleg aus, den Sie der gefundenen Buchung zuordnen möchten, und klicken Sie anschließend auf die Schaltfläche **OK**.
3. Im Fenster **Gebuchte Belege ohne Eingangsbeleg** wird der gewählte Eingangsbeleg nun mit dem gebuchten Beleg verknüpft und in der InfoBox **Eingehende Belegdateien** angezeigt.

Wenn das Fenster **Eingehende Belege** keinen relevanten Eingangsbeleg-Datensatz enthält, können Sie einen erstellen. Weitere Informationen finden Sie unter [So gehts: Eingehende Belege erstellen](across-how-create-income-document-records.md).

## <a name="see-also"></a>Siehe auch
[Eingehende Dokumente verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

