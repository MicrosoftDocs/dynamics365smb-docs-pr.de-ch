---
title: 'Vorgehensweise: Erstellen von Lagerplatzinhalten | Microsoft Docs'
description: "Nachdem Sie Ihre Lagerplätze eingerichtet haben, können Sie die Lagerplatzinhalte einrichten. Mit anderen Worten: Sie können die Artikel einrichten, die Sie in jedem beliebigen Lagerplatz lagern möchten, und Sie können die Regeln festlegen, die befolgt werden sollen, wenn sie den Lagerplatz mit einem bestimmten Artikel füllt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ec7a0c7c34e164b6ca6c8e65938a8c5e53e65514
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-bin-contents"></a>Lagerplatzinhalt erstellen
Nachdem Sie Ihre Lagerplätze eingerichtet haben, können Sie die Lagerplatzinhalte einrichten. Mit anderen Worten: Sie können die Artikel einrichten, die Sie in jedem beliebigen Lagerplatz lagern möchten, und Sie können die Regeln festlegen, die befolgt werden sollen, wenn sie den Lagerplatz mit einem bestimmten Artikel füllt. Sie können dies im Fenster **Lagerplatzinhalt** oder automatisch mit dem Fenster **Erstellen Sie Lagerplatzinhalt-Vorschlag erstellen** manuell tun.

## <a name="to-create-bin-content-manually"></a>So erstellen Sie Lagerplatzinhalt manuell  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplätze** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Lagerort aus, an dem Sie Lagerplatzinhalte einrichten möchten, und wählen Sie dann die Aktion **Lagerplätze** aus.  
3.  Wählen Sie den Lagerplatz aus, an dem Sie Lagerplatzinhalte einrichten möchten, und wählen Sie dann die Aktion **Inhalte** aus.  
4.  Füllen Sie für jeden Artikel, den Sie in dem Lagerplatz lagern möchten, eine Zeile im Fenster **Lagerplatzinhalt** mit den relevanten Informationen aus. Einige der Felder sind bereits mit Informationen über den Lagerplatz ausgefüllt.  
5.  Füllen Sie als Erstes das Feld **Artikelnr.** aus und dann, wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, die anderen Felder, wie z. B. **Einheitencode**, **Max. Menge** und **Min. Menge** aus.  

Wählen Sie bei Bedarf das Feld **Fix** aus. Wenn der Lagerplatz als Standardlagerplatz für den Artikel verwendet werden soll, wählen das Feld **Standardlagerplatz**.  

Wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden und die richtigen Dimensionsinformationen auf der Artikelkarte zu jeder Einheit des Artikels eingegeben haben (Länge, Breite, Höhe und Gewicht), wird die maximale Menge, die Sie in das Fenster **Lagerplatzinhalt** eingegeben haben, gegen die physische Kapazität des Lagerplatzes geprüft. Dann werden die minimale und maximale Menge verwendet, wenn die Lagerplatzauffüllung berechnet und Einlagerungen vorgeschlagen werden.  

Wenn Sie das Feld **Fest** wählen, legen Sie diesen Lagerplatz für diesen Artikel fest. Das bedeutet, dass [!INCLUDE[d365fin](includes/d365fin_md.md)] versuchen wird, diesen Artikel in den Lagerplatz einzulagern, wenn dort Platz ist. Sie wird an dieser Festlegung sogar dann festhalten, wenn die Menge im Lagerplatz 0 ist. Andere Artikel können in den Lagerplatz eingelagert werden, obwohl ein bestimmter Artikel als Standard für den Lagerplatz festgelegt wurde. Andere Artikel können in den Lagerplatz eingelagert werden, obwohl ein bestimmter Artikel dem Lagerplatz fest zugewiesen wurde.  

> [!NOTE]  
>  Im Fenster **Lagerplatzinh. Erst.-Vorschlag** können Sie mehrere Lagerplatzinhalte gleichzeitig einrichten.  

## <a name="to-create-bin-content-with-a-worksheet"></a>So erstellen Sie Lagerplatzinhalt in einem Vorschlag  
Wenn Sie Ihre Lagerplätze erzeugt haben, können Sie den Lagerplatzinhalt, den Sie in jedem Lagerplatz haben möchten, im Lagerplatzinhalt Erstellungsvorschlag generieren.

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"), geben **Lagerplatzinh. Erst.-Vorschlag** ein und wählen dann den zugehörigen Link aus.  
2.  Klicken Sie im Kopf des Vorschlags in das Feld **Name** und wählen Sie den Vorschlag des Lagerortes, für den Sie Lagerplatzinhalte erstellen möchten.  
3.  Wählen Sie im Feld **Lagerplatzcode** den Code des Lagerplatzes, für den Sie den Lagerplatzinhalt definieren möchten.   

    Wenn Sie in diesem Lagerort die gesteuerte Einlagerung und Kommissionierung verwenden, werden automatisch die Felder ausgefüllt, die mit diesem speziellen Lagerplatz verknüpft sind, wie z. B. **Lagerplatzartencode**, **Lagerklassencode** und **Lagerplatzpriorität**. Dies sind Informationen, die Sie berücksichtigen müssen, wenn Sie den Lagerplatzinhalt definieren.  
4.  Wählen Sie den Artikel, den Sie dem Lagerplatz zuordnen möchten, und füllen Sie die Felder aus, die sich auf den Lagerplatzinhalt beziehen. Wenn Sie die gesteuerte Einlagerung und Kommissionierung nutzen und die Funktion **Lagerplatz-Auffüllung berechnen** verwenden möchten, füllen Sie die Felder **Max. Menge** und **Min. Menge** aus.  

    Wenn Sie diesen Lagerplatz für den Artikel als bevorzugten Lagerplatz einrichten möchten, auch wenn die Menge am Lagerplatz **0** ist und alle anderen Einlagerungskriterien gleich sind, aktivieren Sie das Feld **Fix**.  
5.  Wiederholen Sie die Schritte 3 bis 4 für jeden Artikel, den Sie einem Lagerplatz zuordnen möchten.  
6.  Wählen Sie auf Aktion **Drucken** aus, um sich eine Seitenansicht der Lagerplatzinhalte anzusehen, die Sie im Vorschlag eingegeben haben, oder um diese zu drucken. Überprüfen Sie den Lagerplatzinhalt so lange, bis Sie mit dem Ergebnis zufrieden sind.  
7.  Wenn Sie bereit sind, wählen Sie die **Lagerplatzinhalt erstellen** Aktion aus.  

In diesem Vorschlag können Sie mit einer Anzahl Lagerplatzinhaltszeilen für mehrere Lagerplätze arbeiten und dadurch einen guten Überblick darüber erhalten, was Sie in die verschiedenen Lagerplätze in einer vorgegebenen Zone, einem Gang oder Regal einlagern.  

## <a name="see-also"></a>Siehe auch
[Lagerplatzauffüllung berechnen](warehouse-how-to-calculate-bin-replenishment.md)    
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

