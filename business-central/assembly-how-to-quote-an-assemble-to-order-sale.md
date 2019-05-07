---
title: 'Vorgehensweise: Offerte eines Auftragsmontageverkaufs | Microsoft Docs'
description: Sie können Montageverwaltung verwenden, um einen Montageartikel auf Anforderung eines Debitors während des Vertriebsprozesses anzupassen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: b69433a365e6c67f31863f8289cddb21d0f7f4b7
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "936498"
---
# <a name="quote-an-assemble-to-order-sale"></a>Offerte eines Auftragsmontageverkaufs
Sie können Montageverwaltung verwenden, um einen Montageartikel auf Anforderung eines Debitors während des Vertriebsprozesses anzupassen. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  

Wie beim Verkauf beliebiger Artikel können Sie auch eine Verkaufsofferte für einen angepassten Montageartikel erstellen, bevor Sie dieses in einen Verkaufsauftrag umwandeln. Dieser Prozess beinhaltet einige zusätzliche Schritte, wenn Sie ihn mit dem Erstellen einer regulären Verkaufsofferte vergleichen; er verwendet eine Variation eines verknüpften Montageauftrags, eine Montageofferte.

> [!NOTE]  
>  Wie alle Arten von Angeboten, werden die Mengen in Montageangeboten nicht für die Verfügbarkeit, in der Planung oder für Reservierungen verwendet.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>So erstellen Sie eine Verkaufsofferte für einen Auftragsmontageartikel:  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkaufsofferten** ein, und wählen dann den zugehörigen Link aus.  
2.  Erstellen Sie eine Verkaufsoffertenzeile mit einer Zeile für einen Montageartikel. Weitere Informationen finden Sie unter [Verkaufsofferten machen](sales-how-make-offers.md).  
3.  Geben Sie im Feld **Menge für Auftragsmontage** die vollständige Menge ein.

    > [!NOTE]  
    >  Sie sollten keine Teilmenge eingeben. Daher müssen Sie die gleiche Menge eingeben, die Sie im Feld **Menge** auf der Verkaufsoffertenzeile eingegeben haben.  

4.  Wählen Sie auf dem Inforegister **Zeilen** **Zeile** aus, wählen Sie **Auftragsmontage**, und klicken Sie anschliessend auf **Auftragsmontagezeilen**. Alternativ wählen Sie das Feld **Menge für Auftragsmontage** aus.  
5.  Prüfen und ändern Sie bei Bedarf auf der Seite **Auftragsmontagezeilen** die Auftragsmontagezeilen anhand der Offerte, die der Debitor anfragt. Wenn Sie weitere Informationen wünschen, wählen Sie die Aktion **Dokument anzeigen**, um den vollständigen Rahmenoffertenauftrag zu öffnen. Sie können den Inhalt der meisten Felder nicht ändern, und Sie können nicht buchen.  
6.  Wenn Sie die Montageauftragszeilen entsprechend der Offerte angepasst haben, schliessen Sie die Seite **Auftragsmontagezeilen**, um zur Seite **Verkaufsofferte** zurückzukehren.  
7.  Wenn der Kunde die Offerte annimmt, erstellen Sie einen Verkaufsauftrag für den offerierten Montageartikel. Weitere Informationen finden Sie unter [Verkaufsofferten machen](sales-how-make-offers.md). Die verknüpfte Montageofferte und alle eventuellen Anpassungen werden mit dem neuen Verkaufsauftrag verknüpft, um die Montage des/der zu verkaufenden Artikel vorzubereiten.  

## <a name="see-also"></a>Siehe auch  
[Montageverwaltung](assembly-assemble-items.md)  
[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
