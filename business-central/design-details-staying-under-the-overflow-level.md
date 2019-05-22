---
title: 'Designdetails: Unter dem Überlaufmenge bleiben | Microsoft Docs'
description: Wenn die Funktionen Auffüllen auf Maximalbestand Feste Bestellmenge verwendet werden, konzentriert sich das Planungssystem nur auf den voraussichtlichen Lagerbestand in dem vorgegebenen Zeitrahmen. Dies bedeutet, dass das Planungssystem möglicherweise überflüssigen Vorrat vorschlägt, wenn negativer Bedarfs- oder positive Vorratsänderungen ausserhalb gegebenen Zeitrahmens auftreten.
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
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 250de9bf843dac7bfca08d8f3a9dcd4ea44586df
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240064"
---
# <a name="design-details-staying-under-the-overflow-level"></a>Designdetails: Unter dem Überlauflevel bleiben
Wenn die Funktionen Auffüllen auf Maximalbestand Feste Bestellmenge verwendet werden, konzentriert sich das Planungssystem nur auf den voraussichtlichen Lagerbestand in dem vorgegebenen Zeitrahmen. Dies bedeutet, dass das Planungssystem möglicherweise überflüssigen Vorrat vorschlägt, wenn negativer Bedarfs- oder positive Vorratsänderungen ausserhalb gegebenen Zeitrahmens auftreten. Wenn aus diesem Grund ein überflüssiger Vorrat vorgeschlagen wird, berechnet das Planungssystem die zu reduzierende oder zu löschende Vorratsmenge, um überflüssigen Vorrat zu vermeiden. Diese Menge wird als "Überlaufmenge" bezeichnet. Diese Menge wird als "Überlauflevel" bezeichnet. Der Überlauf wird als Planungszeile mit einer **Menge ändern** oder **Abbrechen** Operation und der folgenden Warnmeldung mitgeteilt:  

*Achtung: Der voraussichtliche Lagerbestand [xx] ist höher als das Überlauflevel [xx] am Fälligkeitsdatum [xx].*  

![Lagerüberlaufmenge](media/supplyplanning_2_overflow1_new.png "Lagerüberlaufmenge")  

##  <a name="calculating-the-overflow-level"></a>Berechnung des Überlauflevels  
Das Überlauflevel wird auf verschiedene Arten abhängig vom Planungssetup berechnet.  

### <a name="maximum-qty-reordering-policy"></a>Auffüllen auf Maximalbestand. Wiederbeschaffungsverfahren  
Überlauflevel = Maximalbestand  

> [!NOTE]  
>  Wenn eine Auftragsmindestmenge existiert, wird sie wie folgt hinzugefügt: Überlauflevel-= Maximalbestand-+ Auftragsmindestmenge.  

### <a name="fixed-reorder-qty-reordering-policy"></a>Nachbestellungsrichtlinie Feste Bestellmenge  
Überlauflevel = Bestellmenge + Minimalbestand  

> [!NOTE]  
>  Wenn die Mindestauftragsgrösse höher als der Minimalbestand ist, dann werden folgende Ersetzungen vorgenommen: Überlauflevel-= Bestellmenge + Mindestauftragsgrösse  

### <a name="order-multiple"></a>Losgrössenrundungsfaktor  
Wenn ein Auftragsvielfaches vorhanden ist, reguliert dieses den Überlauflevel für die Wiederbeschaffungsverfahren Höchstmenge und Feste Nachbestellmenge.  

##  <a name="creating-the-planning-line-with-overflow-warning"></a>Erstellen der Planungszeile mit Überlaufwarnmeldung  
Wenn eine vorhandene Lieferung dazu führt, dass der voraussichtliche Lagerbestand höher ist, als das Überlauflevel am Ende eines Zeitrahmens höher, wird eine Planungszeile erstellt. Um vor einem möglichen überflüssigen Vorrat zu warnen, hat die Planungszeile eine Warnmeldung, das Feld **Ereignismeldung akzeptieren** ist nicht aktiviert, und die Ereignismeldung ist entweder "Abbrechen" oder "Menge ändern".  

### <a name="calculating-the-planning-line-quantity"></a>Berechnen der Planungszeilenmenge  
Planungszeilen-Menge = Netzstrom-Menge - (voraussichtlicher Lagerbestand - Überlauflevel)  

> [!NOTE]  
>  Wie bei allen Hinweiszeilen werden alle Max./Min.-Auftragsmengen oder Auftragsvielfache ignoriert.  

### <a name="defining-the-action-message-type"></a>Definieren des Aktionsmeldungstyps  

-   Wenn die Planungszeilenmenge höher als 0 ist, ist die Aktionsmeldung „Menge ändern“.  
-   Wenn die Planungszeilenmenge gleich oder niedriger als 0 ist, ist die Aktionsmeldung „Stornieren“.  

### <a name="composing-the-warning-message"></a>Verfassen der Warnmeldung  
Im Falle eines Überlaufs zeigt die Seite  **Planungselement ohne Nachverfolgung** eine Warnmeldung mit den folgenden Informationen an:  

-   Der voraussichtliche Lagerbestand, der die Warnung ausgelöst hat.  
-   Der berechnete Überlauflevel  
-   Das Fälligkeitsdatum des Vorratsereignisses.  

Beispiel: "Der voraussichtliche Lagerbestand 120 übersteigt das Überlauflevel 60 am 28.01.11"  

## <a name="scenario"></a>Szenario  
In diesem Szenario ändert ein Debitor einen Verkaufsauftrag von 70 zu 40 Stück zwischen zwei Planungen. Die Überlauffunktion reduziert den Einkauf, der für die anfängliche Verkaufsmenge vorgeschlagen worden war.  

### <a name="item-setup"></a>Artikeleinrichtung  

|Wiederbeschaffungsverfahren|Auffüllen auf Maximalbestand|  
|-----------------------|------------------|  
|Maximale Losgrösse|100|  
|Minimalbestand|50|  
|Lagerbestand|80|  

### <a name="situation-before-sales-decrease"></a>Situation vor Vertriebsabgang  

|Ereignis|"Menge ändern"|Voraussichtlicher Lagerbestand|  
|-----------|-----------------|-------------------------|  
|Tag eins|keine|80|  
|Verkauf|-70|10|  
|Ende des Zeitrahmens|keine|10|  
|Neue Bestellung vorschlagen|+90|100|  

### <a name="situation-after-sales-decrease"></a>Situation nach Vertriebsabgang  

|Ändern|"Menge ändern"|Voraussichtlicher Lagerbestand|  
|------------|-----------------|-------------------------|  
|Tag eins|keine|80|  
|Verkauf|-40|40|  
|Einkauf|+90|130|  
|Ende des Zeitrahmens|keine|130|  
|Vorschlagen, den Einkauf zu vermindern<br /><br /> Auftrag von 90 bis 60|-30|100|  

### <a name="resulting-planning-lines"></a>Planzeilen erstellen  
 Eine Planungszeile (Warnen) wird erstellt, um den Einkauf mit 30 von 90 auf 60 zu verringern, um den voraussichtlichen Lagerstatus auf 100 entsprechend dem Überlauflevel festzuhalten.  

![Planung entsprechender Überlaufmenge](media/nav_app_supply_planning_2_overflow2.png "Planung entsprechender Überlaufmenge")  

> [!NOTE]  
>  Ohne die Sammelfunktion werden keine Warnmeldungen erstellt, wenn der voraussichtliche Lagerbestand über Maximalbestand ist. Dies kann einen überflüssigen Vorrat von 30 verursachen.  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md)   
[Designdetails: Planungsparameter](design-details-planning-parameters.md)   
[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)
