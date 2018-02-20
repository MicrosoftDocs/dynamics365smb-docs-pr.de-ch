---
title: 'Vorgehensweise: Offerte eines Auftragsmontageverkaufs | Microsoft Docs'
description: "Sie können Montageverwaltung verwenden, um einen Montageartikel auf Anforderung eines Debitors während des Vertriebsprozesses anzupassen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4b91b8a0ee359c1dc8dc4507cade6b635dace644
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="quote-an-assemble-to-order-sale"></a>Offerte eines Auftragsmontageverkaufs
Sie können Montageverwaltung verwenden, um einen Montageartikel auf Anforderung eines Debitors während des Vertriebsprozesses anzupassen. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  

Wie beim Verkauf beliebiger Artikel können Sie auch eine Verkaufsofferte für einen angepassten Montageartikel erstellen, bevor Sie dieses in einen Verkaufsauftrag umwandeln. Dieser Prozess beinhaltet einige zusätzliche Schritte, wenn Sie ihn mit dem Erstellen einer regulären Verkaufsofferte vergleichen; er verwendet eine Variation eines verknüpften Montageauftrags, eine Montageofferte.

> [!NOTE]  
>  Wie alle Arten von Angeboten, werden die Mengen in Montageangeboten nicht für die Verfügbarkeit, in der Planung oder für Reservierungen verwendet.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>So erstellen Sie eine Verkaufsofferte für einen Auftragsmontageartikel:  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Verkaufsofferte** ein und wählen dann den zugehörigen Link aus.  
2.  Erstellen Sie eine Verkaufsoffertenzeile mit einer Zeile für einen Montageartikel. Weitere Informationen finden Sie unter  [Angebot erstellen](sales-how-make-offers.md).  
3.  Geben Sie im Feld **Menge für Auftragsmontage** die vollständige Menge ein.

    > [!NOTE]  
    >  Sie sollten keine Teilmenge eingeben. Daher müssen Sie die gleiche Menge eingeben, die Sie im Feld **Menge** auf der Verkaufsoffertenzeile eingegeben haben.  

4.  Wählen Sie auf dem Inforegister **Zeilen** **Zeile** aus, wählen Sie **Auftragsmontage**, und klicken Sie anschliessend auf **Auftragsmontagezeilen**. Alternativ wählen Sie das Feld **Menge für Auftragsmontage** aus.  
5.  Prüfen und ändern Sie bei Bedarf im Fenster **Auftragsmontagezeilen** die Auftragsmontagezeilen anhand der Offerte, das der Debitor anfragt. Wenn Sie weitere Informationen wünschen, wählen Sie die Aktion **Dokument anzeigen**, um den vollständigen Rahmenoffertenauftrag zu öffnen. Sie können den Inhalt der meisten Felder nicht ändern, und Sie können nicht buchen.  
6.  Wenn Sie die Montageauftragszeilen entsprechend der Offerte angepasst haben, schliessen Sie das Fenster **Auftragsmontagezeilen**, um zum Fenster **Verkaufsofferte** zurückzukehren.  
7.  Wenn der Kunde die Offerte annimmt, erstellen Sie einen Verkaufsauftrag für den offerierten Montageartikel. Weitere Informationen finden Sie unter  [Angebot erstellen](sales-how-make-offers.md). Die verknüpfte Montageofferte und alle eventuellen Anpassungen werden mit dem neuen Verkaufsauftrag verknüpft, um die Montage des/der zu verkaufenden Artikel vorzubereiten.  

## <a name="see-also"></a>Siehe auch  
[Montageverwaltung](assembly-assemble-items.md)  
[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

