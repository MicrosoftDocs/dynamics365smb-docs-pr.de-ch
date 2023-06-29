---
title: "Designdetails\_– Artikeltrackingdesign"
description: 'In diesem Thema wird das Design des Artikeltrackings in Business Central beschrieben, wenn dieses über Produktversionen hinweg ausgereift ist.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item, tracking, tracing'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-design"></a><a name="design-details-item-tracking-design"></a>Designdetails: Artikeltrackingdesign

Artikeltracking in [!INCLUDE[prod_short](includes/prod_short.md)] begann mit [!INCLUDE [navnow_md](includes/navnow_md.md)]. Die Artikeltrackingfunktion befindet sich in einer separaten Objektstruktur mit komplexen Links zu gebuchten Belegen und Lagerposten und ist in das Reservierungssystem integriert, das Reservierung, Auftragstracking und Aktionsnachrichten verwaltet. Weitere Informationen finden Sie unter [Designdetails: Reservierung, Auftragstracking und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md) in den Beschaffungsplanungsdetails.  

Dieses Design enthält Artikeltrackingposten in der Gesamtverfügbarkeitsberechnung im gesamten System, einschliesslich Planungs-, Produktions- und Lagerfunktionen. Serien- und Chargennummern in den Lagerposten werden angewendet, um den einfachen Zugriff auf historische Daten für Artikeltrackingzwecke zu ermöglichen. Mit dem Veröffentlichungszyklus 1 von 2021 enthält das Artikeltracking in [!INCLUDE [prod_short](includes/prod_short.md)] Paketnummern.  

Mit der Hinzufügung der Serien-, Chargen‑ und Paketnummern verarbeitet das Reservierungssystem permanent Artikelattribute sowie periodische Verknüpfungen zwischen Angebot und Nachfrage in Form von Bedarfsverursacherposten und -Reservierungsposten. Ein weitere Eigenschaft der Serien- oder Chargennummern gegenüber herkömmlichen Reservierungsdaten ist die Tatsache, dass diese teilweise oder vollständig gebucht werden können. Daher funktioniert die Tabelle **Reservierungsposten** (T337) jetzt mit einer zugehörigen Tabelle, der Tabelle **Trackingspezifikation** (T336), die das Summieren über aktive und gebuchte Artikeltrackingmengen hinweg verwaltet und anzeigt. Weitere Informationen finden Sie unter [Designdetails: Aktive vs. historische Artikeltrackingposten](design-details-active-versus-historic-item-tracking-entries.md).  

Das folgende Diagramm illustriert das Design von Artikeltrackingfunktionen in [!INCLUDE[prod_short](includes/prod_short.md)].  

![Beispiel für einen Item Tracking Flow.](media/design_details_item_tracking_design.png "Beispiel für den Fluss des Artikeltrackings")  

Das zentrale Buchungsobjekt wird überarbeitet, um die besondere Subklassifikation einer Belegzeile in Form von Serien- oder Chargennummern zu bearbeiten, und bestimmte Beziehungstabellen werden hinzugefügt, um die 1-zu-viele-Relationen zwischen gebuchten Belegen und deren geteilten Lagerposten bzw. Wertposten zu erstellen.  

Codeunit 22, **Lagerposten – Zeile buchen** teilt jetzt die Buchung nach Artikeltrackingnummern, die auf der Belegzeile angegebenen sind. Jede einzelne Artikeltrackingnummer auf der Zeile erstellt ihren eigenen Lagerposten für den Artikel. Dies bedeutet, dass die Verknüpfung von der gebuchten Belegzeile zu den entsprechenden Lagerposten jetzt eine Relation von einem zu mehreren ist. Diese Verknüpfung wird von den folgenden Artikeltracking-Beziehungstabellen verarbeitet.  

|Feld|Description|  
|---------------|---------------------------------------|  
|**Lagerpostenverbindung** (T6507)|Inbezugsetzen gelieferter oder erhaltener Zeilen zu Lagerposten|  
|**Wertpostenverbindung** (T6508)|Inbezugsetzen fakturierter Zeilen zu Wertposten|  

Weitere Informationen finden Sie unter [Designdetails: Artikeltracking-Buchungsstruktur](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Designdetails: Artikeltracking](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
