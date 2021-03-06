---
title: 'Designdetails: Artikeltrackingdesign | Microsoft Docs'
description: Dieses Thema beschreibt den Entwurf hinter dem Artikeltracking in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87c85de9f501e093679512b709841d0027fe17bf
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751344"
---
# <a name="design-details-item-tracking-design"></a>Designdetails: Artikeltrackingdesign
In der ersten Version der Artikeltracking in [!INCLUDE[prod_short](includes/prod_short.md)] 2.60 wurden Seriennummern oder Chargennummern direkt in Lagerposten erfasst. Dieses Design bot vollständige Verfügbarkeitsinformationen und einfaches Tracking von historischen Posten, aber es ermangelte Flexibilität und Funktionen.  

Ab [!INCLUDE[prod_short](includes/prod_short.md)] 3.00, befand sich die Artikeltrackingfunktion in einer separaten Objektstruktur mit verwickelten Links zu den gebuchten Belegen und den Lagerposten. Dieses Design war flexibel und reich an Funktionen, aber Artikeltrackingposten wurden nicht vollständig in Verfügbarkeitsberechnungen einbezogen.  

Seit [!INCLUDE[prod_short](includes/prod_short.md)] 3.60 sind Artikeltrackingfunktionen im Reservierungssystem integriert, das Reservierung, Auftragsnachverfolgung und Aktionsmessaging verarbeitet. Weitere Informationen finden Sie unter „Designdetails: Reservierung, Auftragstracking und Aktionsmeldungen“ in „Designdetails: Beschaffungsplanung“.  

Dieses neueste Design enthält Artikeltrackingposten in der Gesamtverfügbarkeitsberechnung im gesamten System, einschliesslich Planungs-, Produktions- und Lagerfunktionen. Der alte Konzept der Verwendung von Serien- und Chargennummern in den Lagerposten wird erneut eingeführt, um den einfachen Zugriff auf historische Daten für Artikeltrackingzwecke zu ermöglichen. In Verbindung mit Artikeltrackingverbesserungen in [!INCLUDE[prod_short](includes/prod_short.md)] 3.60 wurde das Reservierungssystem auf Nicht-Auftragsnetzwerk-Entitäten erweitert, wie Erfassungsjournale, Rechnungen und Gutschriften.  

Mit der Hinzufügung der Serien- oder Chargennummern verarbeitet das Reservierungssystem permanent Artikelattribute sowie periodische Verknüpfungen zwischen Offerte und Nachfrage in Form von Bedarfsverursacherposten und -Reservierungsposten. Ein weitere Eigenschaft der Serien- oder Chargennummern gegenüber herkömmlichen Reservierungsdaten ist die Tatsache, dass diese teilweise oder vollständig gebucht werden können. Daher funktioniert die Tabelle **Reservierungsposten** (T337) jetzt mit einer zugehörigen Tabelle, der Tabelle **Trackingspezifikation** (T336), die das Summieren über aktive und gebuchte Artikeltrackingmengen hinweg verwaltet und anzeigt. Weitere Informationen finden Sie unter [Designdetails: Aktive vs. historische Artikeltrackingposten](design-details-active-versus-historic-item-tracking-entries.md).  

Das folgende Diagramm illustriert das Design von Artikeltrackingfunktionen in [!INCLUDE[prod_short](includes/prod_short.md)].  

![Beispiel für den Fluss des Artikeltrackings](media/design_details_item_tracking_design.png "Beispiel für den Fluss des Artikeltrackings")  

Das zentrale Buchungsobjekt wird überarbeitet, um die besondere Subklassifikation einer Belegzeile in Form von Serien- oder Chargennummern zu bearbeiten, und bestimmte Beziehungstabellen werden hinzugefügt, um die 1-zu-viele-Relationen zwischen gebuchten Belegen und deren geteilten Lagerposten bzw. Wertposten zu erstellen.  

Codeunit 22, **Lagerposten – Zeile buchen** teilt jetzt die Buchung nach Artikeltrackingnummern, die auf der Belegzeile angegebenen sind. Jede einzelne Artikeltrackingnummer auf der Zeile erstellt ihren eigenen Lagerposten für den Artikel. Dies bedeutet, dass die Verknüpfung von der gebuchten Belegzeile zu den entsprechenden Lagerposten jetzt eine Relation von einem zu mehreren ist. Diese Verknüpfung wird von den folgenden Artikeltracking-Beziehungstabellen verarbeitet.  

|Feld|Description|  
|---------------|---------------------------------------|  
|**Lagerpostenverbindung** (T6507)|Inbezugsetzen gelieferter oder erhaltener Zeilen zu Lagerposten|  
|**Wertpostenverbindung** (T6508)|Inbezugsetzen fakturierter Zeilen zu Wertposten|  

Weitere Informationen finden Sie unter [Designdetails: Artikeltracking-Buchungsstruktur](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Artikeltracking](design-details-item-tracking.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]