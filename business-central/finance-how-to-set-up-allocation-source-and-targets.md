---
title: 'Vorgehensweise: Einrichten von Zuteilungsquellen und -zielen | Microsoft Docs'
description: Jede Zuordnung besteht aus einer Zuordnungsquelle und einer oder mehreren Zuordnungszielen. Die Zuordnungsquelle definiert, welche Kosten zugeordnet werden. Die Zuordnungsziele bestimmen, wie die Kosten zugeordnet werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 2e8040816ed5089188f06f76b2cd8f027ba83766
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "929782"
---
# <a name="set-up-allocation-source-and-targets"></a>Richten Sie die Zuteilungsquelle und Ziele ein
Jede Zuordnung besteht aus einer Zuordnungsquelle und einer oder mehreren Zuordnungszielen. Die Zuordnungsquelle definiert, welche Kosten zugeordnet werden. Die Zuordnungsziele bestimmen, wie die Kosten zugeordnet werden.  

## <a name="to-set-up-cost-allocations"></a>So richten Sie Kostenzuordnungen ein  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kostenumlage** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie auf der Seite **Kostenumlage** die Aktion **Bearbeiten** aus.  
3.  Geben Sie eine ID für die Zuordnungsquelle in das Feld **ID** ein.  
4.  Definieren Sie eine **Ebene** als Zahl zwischen 1 und 99 im Feld . Die Verteilungsbuchung richtet sich nach der Reihenfolge der Stufen.  
5.  Geben Sie eine Kostenart ein, um festzulegen, welche Kostenarten im Feld **Kostenartbereich** zugeordnet werden. Wenn alle Kosten für eine Kostenart zugeordnet werden, wird kein Bereich definiert.  
6.  Geben Sie eine Kostenstelle zusammen mit den zuzuordnenden Kosten im Feld **Kostenstellencode** ein.  
7.  Geben Sie eine Kostenstelle zusammen mit den zuzuordnenden Kosten im Feld **Kostenstellencode** ein. Am häufigsten bleibt das Feld leer, da Kostenobjekte selten anderen Kostenträgern zugeordnet werden.  
8.  Geben Sie im Feld **Für Kostenart gutschreiben** eine Kostenart ein. Die Kosten, die zugeteilt werden, werden der ursprünglichen Kostenart gutgeschrieben. Die Kreditbuchung wird auf Kostenart gebucht, die hier angegeben ist.  
9. Definieren Sie im Inforegister **Zeilen** die Verteilungsziele. Geben Sie auf der ersten Zeile unter **Zielkostenart** eine Kostenart ein. So definieren Sie, unter welcher Kostenart die Zuordnung gebucht wird.  
10. Geben Sie in der ersten Zeile das erste Zuordnungsziel in das Feld **Zielkostenstelle** oder **Zielkostenobjekt** ein. Diese beiden Felder definieren, auf welche Kostenstelle oder welchen Kostenträger die Zuordnung gebucht wird. Sie können eines dieses Felder ausfüllen, aber nicht beide.  
11. Wiederholen Sie dieselben Schritte in der zweiten Zeile, um zusätzliche Zuordnungsziele einzurichten.  
12. Nach dem Einrichten der Zuordnungsziele und -quellen wählen Sie auf der Registerkarte Start in der Gruppe Prozess die Aktion **Umlageschlüssel berechnen** aus, um die gesamten Aktienwerte zu berechnen.  

> [!NOTE]  
>  Aktivieren Sie das Kontrollkästchen **Gesperrt**, um die Verteilungseinrichtung zu deaktivieren.  

## <a name="see-also"></a>Siehe auch  
[Kostenrechnung](finance-manage-cost-accounting.md)  
 [Setzen von Filtern für dynamische Zuteilungsgrundlagen](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Szenario-Beispiel: Definieren von statischen Umlagen basierend auf dem Verteilungsverhältnis](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)   
 [Szenario-Beispiel: Definieren von dynamischen Zuteilungen auf der Basis der verkauften Artikel](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Definieren und Zuweisen von Kosten](finance-define-and-allocate-costs.md)   
 [Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
