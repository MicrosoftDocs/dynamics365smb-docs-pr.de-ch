---
title: Dfinieren und Zuweisen von Kosten | Microsoft Docs
description: "Kostenumlagen verschieben Kosten und Einnahmen zwischen Kostenarten, Kostenstellen und Kostenträgern. Sie können so viele Zuteilungen wie notwendig definieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7bdddcadf3fb7dceb762354e8fa527158782b676
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="defining-and-allocating-costs"></a>Definieren und Zuweisen von Kosten
Kostenumlagen verschieben Kosten und Einnahmen zwischen Kostenarten, Kostenstellen und Kostenträgern. Sie können so viele Zuteilungen wie notwendig definieren. Jede Zuteilung besteht aus:  

-   Eine Verteilungsquelle.  
-   Mindestens einem Zuteilungsziel.  

Die Zuteilungsquelle gibt an, welche Kosten zugeordnet werden müssen, und die Zuteilungsziele bestimmen, wo die Kosten zugeordnet werden müssen. Beispielsweise kann eine Zuteilungsquelle die Kosten für die Kostenart "Strom und Heizung" sein. Sie ordnen alle Strom- und Heizkosten drei Kostenstellen zu: Werkstatt, Produktion und Verkauf. Diese Kostenstellen sind Ihre Zuteilungsziele.  

Für jede Zuteilungsquelle legen Sie eine Zuteilungsebene, eine Gültigkeitsdauer und eine Variante als Gruppen-ID fest. Sie können einen Batchauftrag verwenden, um Filter festzulegen und Zuteilungsdefinitionen auszuwählen und dann automatisch Kostenumlagen auszuführen.  

Für jedes Zuteilungsziel definieren Sie eine Zuteilungsgrundlage. Die Zuteilungsgrundlage kann entweder statisch oder dynamisch sein.  

-   Die statische Zuteilungsgrundlagen basieren auf einem definierten Wert, zum Beispiel Quadratmeter oder ein eingerichtetes Verteilungsverhältnis, wie 5:2:4.  
-   Die dynamische Zuteilung basiert auf veränderbaren Werten, wie z. B. die Anzahl der Mitarbeiter in einer Kostenstelle oder die Verkaufseinnahmen eines Kostenträgers in einem bestimmten Zeitraum.  

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

|Bis|Informationen|  
|--------|---------|  
|Richten Sie die Zuteilungsquelle und ihre Ziele ein.|[Richten Sie die Zuteilungsquelle und Ziele ein](finance-how-to-set-up-allocation-source-and-targets.md)|  
|Richten Sie verschiedene Filter für dynamische Zuteilungsgrundlagen ein.|[Setzen von Filtern für dynamische Zuteilungsgrundlagen](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|Sehen Sie sich ein Beispiel für das Definieren einer statischen Umlage an.|[Szenario-Beispiel: Definieren von statischen Umlagen basierend auf dem Verteilungsverhältnis](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|Sehen Sie sich ein Beispiel für das Definieren einer dynamischen Zuteilung an.|[Szenario-Beispiel: Definieren von dynamischen Zuteilungen auf der Basis der verkauften Artikel](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a>Siehe auch  
 [Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md)   
 [Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md)   
 [Kostenrechnung](finance-manage-cost-accounting.md)   
 [Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md)   
 [Informationen zur Kostenrechnung](finance-about-cost-accounting.md)

