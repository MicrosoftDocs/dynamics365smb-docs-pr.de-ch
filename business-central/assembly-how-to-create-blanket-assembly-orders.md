---
title: 'Vorgehensweise: Erstellen von Montageaufträgen| Microsoft Docs'
description: Erstellen Sie Rahmenaufträge für benutzerdefinierte Montageartikel, bevor Sie die tatsächlichen Verkaufsaufträge in regelmässigen Abständen entsprechend der Rahmenbestellung erstellen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: eea8c80f1f1796ad0d552b6e832565b400f4cce7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304153"
---
# <a name="create-blanket-assembly-orders"></a>Erstellen von Montagerahmenaufträgen
Sie können Montageverwaltung verwenden, um einen Montageartikel auf Anforderung eines Debitors während des Vertriebsprozesses anzupassen. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  

 Wie für jedem anderen Artikel, können Sie auch Rahmenaufträge für benutzerdefinierte Montageartikel erstellen, bevor Sie die tatsächlichen Verkaufsaufträge in regelmässigen Abständen entsprechend der Rahmenbestellung erstellen. Dieser Prozess beinhaltet im Vergleich zum Erstellen eines regulären Rahmenauftrag einige zusätzliche Schritte; er verwendet eine Variation eines verknüpften Montageauftrags, einen Montagerahmenauftrag.

> [!NOTE]  
>  Wie bei allen Rahmenaufträgen werden Mengen in Montagerahmenaufträgen nur prognostiziert und sind nicht operativ, bis sie in tatsächliche Montageaufträge umgewandelt werden. Daher sind die Bestellungsfunktionen, wie Verfügbarkeitsberechnung, Reservierung, Artikeltracking auf Montagerahmenaufträgen nicht aktiv.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>So erstellen Sie einen Montagerahmenauftrag für einen Auftrags\-\-montageartikel:  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Leere Verkaufsaufträge** ein, und wählen dann den zugehörigen Link aus.  
2. Erstellen Sie einen neune Rahmenauftrag mit einer Zeile für einen Montageartikel. Weitere Informationen hierzu finden Sie unter [Rahmenaufträge erstellen](sales-how-to-create-blanket-sales-orders.md).  
3. Geben Sie im Feld **Menge für Montageauftrag** auf dem Montagerahmenauftrag die vollständige Menge ein.

    > [!NOTE]  
    >  Sie sollten keine Rahmenauftragsvereinbarungen für eine Teilmenge erstellen. Daher müssen Sie die gleiche Menge eingeben, die Sie im Feld **Menge** auf der Rahmenauftragszeile eingegeben haben.  

4. Wählen Sie auf dem Inforegister Zeilen die Option **Auftragsmontage** aus, und wählen Sie dann **Auftragsmontagezeilen**. Wählen Sie das Feld **Menge für Auftragsmontage** aus.  
5. Prüfen und ändern Sie bei Bedarf im Fenster **Auftragsmontagezeilen** die Auftragsmontagezeilen entsprechend der Rahmenauftragsvereinbarung, die Sie mit dem Debitor getroffen haben. Wenn Sie weitere Informationen wünschen, wählen Sie die Aktion **Beleg anzeigen**, um den vollständigen Rahmenangebotsauftrag zu öffnen. Sie können den Inhalt der meisten Felder nicht ändern, und Sie können nicht buchen.  
6. Wenn Sie die Montageauftragszeilen entsprechend der Rahmenauftragsvereinbarung angepasst haben, schliessen Sie das Fenster **Auftragsmontagezeilen**, um zum Fenster **Rahmenauftrag** zurückzukehren.  
7. Wenn der Kunde anfragt, einen Verkaufsauftrag basierend auf dem vereinbarten Rahmenauftrag zu erstellen, erstellen Sie einen Verkaufsauftrag für die vereinbarten Montageartikel oder Artikel. Weitere Informationen hierzu finden Sie unter [Rahmenaufträge erstellen](sales-how-to-create-blanket-sales-orders.md).

Der verknüpfte Montagerahmenauftrag und alle eventuellen Anpassungen werden mit dem neuen Verkaufsauftrag verknüpft, um die Montage des/der zu verkaufenden Artikel vorzubereiten.  

## <a name="see-also"></a>Siehe auch
[Erstellen von Rahmenaufträgen](sales-how-to-create-blanket-sales-orders.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
