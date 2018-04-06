---
title: Deaktivieren des Artikelpreistracking
description: "Wenn ein Artikel im Lager nicht nachverfolgt wird, müssen die Artikelpreise nicht nachverfolgt werden, und es muss kein Lagerposten erstellt werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: f094cc748d263c2ec2d1cfcc18c69b65029246b2
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="deactivate-item-cost-tracking"></a>Deaktivieren des Artikelpreistrackings
Wenn ein Artikel im Lager nicht nachverfolgt wird, müssen die Artikelpreise nicht nachverfolgt werden, und es muss kein Lagerposten erstellt werden.  

Sie können das Artikelpreistracking für einen Artikel deaktivieren. Im Allgemeinen sollte das Artikelpreistracking für Verbrauchsartikel (z. B. Altpapierprodukte) und Dienste, die als Produkte gelten (z. B. feste Parkgebühren), deaktiviert werden. Das Artikelpreistracking sollte für Artikel deaktiviert werden, bei denen die Verfolgung zu falschen Rückschlüssen führen würde. Für Artikel, für die das Artikelpreistracking deaktiviert wurde, sind folgende Funktionen bzw. Systeme nicht verfügbar: Reservierung, Verfügbarkeitsprüfung, Artikelverfolgung und Materialplanungssysteme.  

## <a name="to-deactivate-item-cost-tracking"></a>So deaktivieren Sie das Artikelpreistracking  

1.  Wählen Sie ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die entsprechende Elemente und wählen Sie dann die Aktion **Bearbeiten** aus.  
3.  Aktivieren Sie auf dem Inforegister **Allgemein** das Kontrollkästchen **Keine Lagerführung**.  

    Wenn eine Transaktion für diesen Artikel gebucht wird, wird kein Lagerposten erstellt. Weitere Informationen erhalten Sie in der Tabelle "Lagerposten".  

    > [!NOTE]  
    >  Das Kontrollkästchen **Keine Lagerführung** kann nicht für einen Artikel aktiviert werden, für den bereits Lagerposten gebucht wurden.  

4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
 [Lagerverwaltung (Schweiz)](swiss-inventory-management.md)   
 [Sperren von Lagerartikeln für Verkäufe oder Einkäufe](how-to-block-inventory-items-for-sales-or-purchases.md)

