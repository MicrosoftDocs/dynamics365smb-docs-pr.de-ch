---
title: "Vorgehensweise: Verknüpfung von Datensätzen zu externen Informationen oder Programmen | Microsoft Docs"
description: "Fügen Sie einem Dokument oder einer Website einen Link zu einem bestimmten Datensatz hinzu, beispielsweise zu einer Debitorenkarte oder einem Dokument."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 8927d2ca670b3faa38cd03ea10ae524e595721ad
ms.contentlocale: de-ch
ms.lasthandoff: 11/26/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a>Hinzufügen von Links zu Websites, Belegen oder Programmen auf Datensätze
An einem bestimmten Datensatz, beispielsweise einem Debitoren Beleg oder Verkaufsauftrag, können Sie einen Link einem externen Beleg, einer Website oder einer Anwendung hinzufügen. Möglicherweise möchten Sie einen Link einrichten, durch den eine neue leere E-Mail an einen bestimmten Empfänger geöffnet wird, wenn darauf geklickt wird. Die Kartenseite für einige Einträge wie Debitoren- und Kreditorenkarten beinhalten ein Feld mit der Bezeichnung **Homepage**, in dem eine URL eingegeben werden kann. Wenn Sie andere Links einbeziehen möchten, können Sie die Methode verwenden, die in diesem Artikel beschrieben wird.

Ein anderes Beispiel könnte sein, wenn Sie gedruckte Rechnungen von Kreditoren erhalten. Sie können diese durchsuchen und als .pdf Datei auf einer SharePoint-Site speichern. Anschliessend kann eine Einkaufsrechnung in  [!INCLUDE[d365fin_md](includes/d365fin_md.md)] mit der entsprechenden Rechnung im SharePoint Server verknüpft werden. Zudem besteht die Möglichkeit, eine Artikelkarte mit der entsprechenden Seite im Onlinekatalog des Kreditors zu verknüpfen.

## <a name="to-add-a-link-on-a-record"></a>Um einen Link aus einem Datensatz zu entfernen:   

1.  Öffnen Sie den Datensatz, dem Sie den Link zuordnen möchten (beispielsweise Debitorenkarte oder Verkaufsauftrag). Wenn Sie den Link einer bestimmten Zeile (beispielsweise eine Erf.-Journalzeile) zuordnen möchten, wählen Sie die Zeile aus.  

2.  Wählen Sie die **Links** Aktion aus, um die **Links** Seiten zu öffnen, die alle aktuellen und Links anzeigt, die dem Datensatz hinzugefügt werden.

3. Um neue Benutzer zu erstellen, wählen Sie **+Neu**.

4.  Geben Sie im Feld **Link Adresse** ein

    -   Um eine Datei auf dem Computer oder dem Netzwerk zu verknüpfen, geben Sie den vollständigen Pfad und den Dateinamen, wie **C:My Documentsinvoice1.doc** ein.
    -   Um auf die Website zu verknüpfen, geben Sie die Internetadresse (URL), wie **www.microsoft.com** ein.
    -   Um auf die Website zu verknüpfen, geben Sie die Internetadresse (URL), wie **www.microsoft.com** ein.
    -   Um eine Anwendung zu verknüpfen, Sie geben eine bestimmte Zeichenfolge ein, um die Anwendung zu öffnen. Zum Beispiel, um OneNote mit einer bestimmten Seite zu öffnen, geben Sie **onenote:///C:\Eigene Dateien\test.one** ein. Um Outlook mit einer neuen leeren E-Mail an en bestimmtes Alias zu öffnen, geben Sie **mailto:testalias** ein.  

5.  Geben Sie in das Feld **Beschreibung** Informationen zu dem Link ein.  

6.  Klicken Sie auf die Schaltfläche **Speichern**.  

## <a name="to-delete-a-link-from-a-record"></a>So entfernen Sie einen Link aus einem Datensatz:  

Um einen Link auf der Seite **Links** zu deaktivieren, können Sie auf **…** und anschliessend **Löschen** auswählen.

Wenn Sie einen einzelnen Datensatz (z. B. eine Verkaufszeile, einen Verkaufsauftrag oder eine Debitorenkarte) löschen, werden alle Links gelöscht, die dem Datensatz zugeordnet sind. Wenn Datensätze dagegen mit einer Stapelverarbeitung gelöscht werden wie **Verrechneter Verkaufsauftrag löschen** Stapelverarbeitung, dann wird der Link in der Datenbank gespeichert. Wenn Sie diese Links aus der Datenbank löschen möchten, führen Sie die Codeunit **Nicht verbundene Datensatzverknüpfungen löschen** aus. Wählen Sie dazu das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben **Nicht verbundene Datensatzverknüpfungen löschen** ein, und wählen dann den zugehörigen Link aus.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Siehe auch  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

