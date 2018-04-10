---
title: 'Vorgehensweise: Elektronische Belege empfangen und konvertieren | Microsoft Docs'
description: "-Sie können elektronische Belege direkt aus den Handelspartnern oder einem OCR-Dienst erhalten."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ed2da1942b0a17a3a7a2af6d00ddbd883acf4e0f
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="receive-and-convert-electronic-documents"></a>Vorgehensweise: Elektronische Belege empfangen und konvertieren
Die generische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt das Empfangen von elektronischen Rechnungen und Gutschriften im PEPPOL-Format, das von den wichtigsten Anbietern von Belegaustauschdiensten unterstützt wird. Um beispielsweise eine Rechnung von einem Kreditor in Form eines elektronischen PEPPOL-Belegs zu erhalten, verarbeiten Sie den Beleg im Fenster Eingehende Belege, um diesen in eine Einkaufsrechnung oder Fibu Erf.-Journalzeile in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu konvertieren.

 Zusätzlich zur Empfangen von elektronischen Belegen direkt von Handelspartnern können Sie elektronische Belege von einem OCR-Dienst erhalten, der Ihre PDF- oder Bilddateien in elektronische Belege umgewandelt hat.  

 Bevor Sie elektronische Belege durch den Belegaustauschdienst empfangen können, müssen Sie verschiedene Stammdaten (wie Firmendaten, Kreditoren, Artikel und Einheiten) einrichten. Diese werden verwendet, um Geschäftspartner und Artikel zu identifizieren, wenn Daten in Elementen im Eingangsbeleg zu Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertiert werden. Weitere Informationen finden Sie unter [Belegaustausch-Dienst](across-how-to-set-up-a-document-exchange-service.md).  

 Bevor Sie elektronische Belege vom OCR-Dienst empfangen können, müssen Sie die vorkonfigurierte Serviceverbindung einrichten und aktivieren. Weitere Informationen finden Sie unter [Eingehende Belege einrichten](across-how-setup-income-documents.md).  

 Der Verkehr von elektronischen Belegen in und aus [!INCLUDE[d365fin](includes/d365fin_md.md)] wird durch die Funktion Aufgabenwarteschlange verwaltet. Bevor Sie elektronische Belege empfangen können, muss die betreffende Projektwarteschlange gestartet werden.  

 Sie können die Konvertierung von elektronischen Belegen entweder manuell beginnen, wie in diesem Verfahren beschrieben, oder Sie können einen Workflow aktivieren, der elektronische Belege automatisch konvertiert, wenn sie eintreffen. Die generische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält die Workflowvorlage *Eingehenden elektronischen Beleg über OCR bis Einkaufsrechnung öffnen – Workflow*, die in einen Workflow kopiert und aktiviert werden kann. Weitere Informationen finden Sie unter [Workflow](across-workflow.md).  

> [!NOTE]  
>  Wenn Sie die aus dem OCR-Service erhalten elektronischen Belege in die Belege oder Erfassungsjournalzeilen in [!INCLUDE[d365fin](includes/d365fin_md.md)] umwandeln, dann werden mehrere Zeilen im Herkunftsbeleg in einer Zeile summiert. Die einzelne Zeile hat den Typ "Fibukonto" und die Felder **Beschreibung** und Fibukonto **Nr.** sind leer. Felder sind leer. Der Wert im Feld **Betrag** entspricht dem Gesamtbetrag ohne MWST aller Zeilen im Herkunftsbeleg.  
>   
>  Um sicherzustellen dass **Beschreibung** und **Nr.** Felder ausgefüllt sind, können Sie die Schaltfläche **Text zu Konto zuordnen** im Fenster **Eingehende Belege** auswählen. Hiermit legen Sie fest, dass ein bestimmter Rechnungstext immer einem bestimmten Soll- oder Habenkonto in der Fibuposten zugeordnet wird. Dadurch wird das Feld **Beschreibung** in Belegen oder Erfassungsjournalzeilen, die aus einem elektronischen Beleg für diesen Kreditor oder Debitor erstellt werden, mit dem entsprechenden Text ausgefüllt, und das Feld Fibukonto **Nr.** Feld mit dem fraglichen Konto ergänzt.  
>   
>  Anstelle der Zuordnung zu einem Fibukonto können Sie auch ein Bankkonto zuordnen. Dies ist beispielsweise für elektronische Belege für Ausgaben nützlich, die bereits bezahlt wurden, für die Sie jedoch eine Fibu Erf.-Journalzeile erstellen möchten, die auf ein Bankkonto buchen kann.  

 Die folgenden Schritte zeigen, wie Sie eine Kreditorenrechnungen empfangen und in eine Einkaufsrechnung in [!INCLUDE[d365fin](includes/d365fin_md.md)] konvertieren können. Der Vorgang ist derselbe wie beim Konvertieren einer Kreditorenrechnung in eine Fibu Erf.-Journalzeile.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>So empfangen Sie eine elektronische Rechnung und konvertieren sie in eine Einkaufsrechnung:  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.  

2.  Wählen Sie die Zeile für den Eingangsbeleg aus, der die neue eingehende elektronische Rechnung darstellt, und wählen Sie dann auf der Registerkarte **Start** in der Gruppe **Verwalten** die Option **Bearbeiten** aus.  

     Im Fenster **Eingehende Dokumentenkarte**  wird die entsprechende XML-Datei angehängt, und die meisten Felder werden mit den Informationen aus der elektronischen Rechnung ausgefüllt. Weitere Informationen finden Sie unter [So gehts: Eingehende Dokumente erstellen](across-how-create-income-document-records.md).  

3.  Wählen Sie im Feld **Datenaustauschart** die Option **PEPPOL - Rechnung** oder **OCR - Rechnung** aus, je nachdem, woher der elektronische Beleg stammt.  

4.  Um Text in der Kreditorenrechnung einem bestimmten Sollkonto zuzuordnen, wählen Sie auf der Registerkarte **Aktion**  in der Gruppe **Allgemein** die Option **Text zu Konto zuordnen**, und füllen Sie dann das **Kontozurodnungs**fenster aus.  

5.  Wählen Sie auf der Registerkarte **Aktionen** in der Gruppe **Allgemein** die Option **Beleg erstellen**.  

     Eine Einkaufsrechnung wird in [!INCLUDE[d365fin](includes/d365fin_md.md)] basierend auf den Daten im elektronischen Beleg erstellt.  

     Überprüfungsfehler, die üblicherweise mit falschen oder fehlenden Stammdaten in [!INCLUDE[d365fin](includes/d365fin_md.md)] zusammenhängen, werden im Inforegister **Fehlermeldungen** angezeigt.  

## <a name="see-also"></a>Siehe auch  
[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Eingehende Belege](across-income-documents.md)  
[Einrichten des Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Daten elektronisch austauschen](across-data-exchange.md)   
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
