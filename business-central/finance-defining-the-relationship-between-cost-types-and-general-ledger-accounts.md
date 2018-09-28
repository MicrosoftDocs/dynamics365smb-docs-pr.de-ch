---
title: Definieren der Beziehung zwischen Kostenarten und Fibukonten | Microsoft Docs
description: Lernen, wie die beiden Felder definiert werden, die die Beziehung zwischen Kostenart und Fibukonto festlegen
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7709edb214804f52ee9b495c43b5302e2a23bd6b
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definieren der Beziehung zwischen Kostenarten und Sachkonten
Das Verbindung zwischen der Kostenart und dem Fibukonto wird in der Kostenart und im Fibukonto erstellt.  

* Das Feld **Fibukontenbereich** in der Tabelle **Kostenart** bestimmt, welche Fibukonten zu einer Kostenart gehören.  
* Das **Kostenartennummer** Feld im Kontenplan bestimmt, zu welcher Kostenart ein Fibukonto gehört.  

Diese beiden Felder werden automatisch ausgefüllt, wenn Sie die **Kostenarten aus Kontenplan abrufen**-Funktion verwenden.  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Beziehung zwischen Fibukonten und Kostenarten  
Zwischen Fibukonten und Kostenarten besteht eine n:1-Beziehung. Mehrere Fibukonten können zu einer Kostenart gehören, aber jedes Fibukonto gehört nur zu einer Kostenart. In der folgenden Tabelle werden die Details der Beziehung beschrieben.  

|Verbindungen|**Fibukontobereich**|**Kostenartnr.**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Ein Fibukonto für jede Kostenart|Ein Fibukonto|Eine Kostenart|  
|Mehrere Fibukonten für eine Kostenart|Fibukontobereich, z. B. 7110 ... 7193 für jedes Fibukonto|Für jedes Fibukonto im Bereich gibt es nur eine Kostenart|  
|Kostenarten ohne entsprechende Fibukonten|<Empty>||  
|Fibukonten, deren Posten nicht übertragen werden||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Kostenarten ohne Beziehung zum Fibukonto  
Eine Kostenart hat möglicherweise keine Beziehung zu Fibukonten, wenn eine der folgenden Bedingungen zutrifft:  

* Konten für die betriebliche Buchhaltung, wie Berech. Zinsen und Abschreibungen, entnehmen nur Kosten aus der betrieblichen Buchhaltung.  
* Helfende Kostenarten, wie Kostenarten 9901, 9902 und 9903 in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank, werden als Haben- und Sollbeträge für Zuordnungen verwendet.  
* Das helfende Konto, 9920 in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank, enthält tatsächliche Zugänge, die die Differenz zwischen Kosten und Ausgaben des Fibukontos anzeigen.  

## <a name="see-also"></a>Siehe auch  
[Kostenrechnung](finance-manage-cost-accounting.md)  
[Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md)   
[Informationen zur Kostenrechnung](finance-about-cost-accounting.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

