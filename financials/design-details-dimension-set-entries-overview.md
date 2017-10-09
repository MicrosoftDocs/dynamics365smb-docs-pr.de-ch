---
title: "Dimensionssatzposten Übersicht | Microsoft Docs"
description: In diesem Thema wird beschrieben, wie Dimensionssatzposten in  [!INCLUDE[d365fin](includes/d365fin_md.md)].gespeichert und gebucht werden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 53c85ecbb42db92e95921203d24781bcb82f942d
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="dimension-set-entries-overview"></a>Dimensionssatz-Eintrags-Übersicht
In diesem Thema wird beschrieben, wie Dimensionssatzposten in [!INCLUDE[d365fin](includes/d365fin_md.md)] gespeichert und gebucht werden.  
  
## <a name="dimension-sets"></a>Dimensionssätze  
Ein Dimensionssatz ist eine eindeutige Kombination von Dimensionswerten. Er wird als Dimensionssatzposten in die Datenbank gespeichert. Jeder Dimensionssatzposten stellt einen einzelnen Dimensionswert dar. Der Dimensionssatz wird durch eine allgemeine Dimensionssatz-ID identifiziert, die jedem Dimensionssatzposten zugewiesen wird, der zum Dimensionssatz gehört.  
  
Im folgenden Beispiel wird ein Dimensionssatz gezeigt, der drei Dimensionssatzposten aufweist. Der Dimensionssatz wird durch eine Dimensionssatz-ID, nämlich 108, identifiziert.  
  
|Dimensionssatz-ID|Dimensionscode|Dimensionswertcode|Dimensionswertname|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|BEREICH|70|Nordamerika|  
|108|UNTERNEHMENSGRUPPE|HOME|Start|  
|108|KOSTENSTELLE|VERKAUF|Verkauf|  
  
## <a name="dimension-set-entries"></a>Dimensionssatzposten  
Dimensionssätze werden in der Tabelle als **Dimensionssatzposten** mit derselben Dimensionssatz-ID gespeichert.  
  
![Dimensions-Postenübersicht](media/dimensionentrynav7.png "DimensionEntryNAV7")  
  
Wenn Sie eine neue Erfassungsjournalzeile, einen Belegkopf oder eine Belegzeile erstellen, können Sie eine Kombination von Dimensionswerten angeben. Anstatt jeden Dimensionswert explizit in der Datenbank zu speichern, wird eine Dimensionssatz-ID der Erfassungsjournalzeile, dem Belegkopf oder der Belegzeile zugewiesen, um den Dimensionssatz anzugeben.  
  
Wenn Sie das Fenster **Dimensionssatzeinträge bearbeiten**bearbeiten und schließen, wird eine Prüfung ausgeführt, um festzustellen, ob die Kombination aus Dimensionswerten als Dimensionssatz in der Tabelle existiert. Wenn die Kombination in der Tabelle auftritt, wird die entsprechende Dimensionssatz-ID der Erfassungsjournalzeile, dem Belegkopf oder der Belegzeile zugeordnet. Andernfalls wird ein neuer Dimensionssatz der Tabelle hinzugefügt, und die neue Dimensionssatz-ID wird der Erfassungsjournalzeile, dem Belegkopf oder der Belegzeile zugeordnet.  
  
## <a name="performance-improvement"></a>Leistungsverbesserung  
Durch das einmalige Speichern von Dimensionssätzen in der Datenbank wird Datenbankplatz beibehalten und die Gesamtleistung verbessert.  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Suche nach Dimensionskombinationen](design-details-searching-for-dimension-combinations.md)   
[Designdetails: Tabellenstruktur](design-details-table-structure.md)   
[Designdetails: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md)   
[Designdetails: Codebeispiele von geänderten Mustern in Änderungen](design-details-code-examples-of-changed-patterns-in-modifications.md)   
[Designdetails: Dimensionssatzposten](design-details-dimension-set-entries.md)   

