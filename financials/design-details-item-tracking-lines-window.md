---
title: 'Designdetails: Fenster Artikeltrackingzeilen | Microsoft Docs'
description: Lesen, wie der Fluss der Serien- und Chargennummern in Ihrem Lager verwaltet wird.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 62070ef4e580a3bd665130c9b017bf164bbe2142
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-item-tracking-lines-window"></a>Designdetails: Artikelverfolgungszeilenfenster
Artikeltrackingdatensätze und Reservierungsdatensätze werden im Reservierungssystem erstellt, und ihre Verfügbarkeit wird dynamisch berechnet. Daten, die in das **Artikeltrackingzeilen**-Fenster eingegeben werden, werden in einer temporären Version der Tabelle **Trackingspezifikation** verwaltet. Wenn das Fenster geschlossen wird, werden die aktiven Daten in der Tabelle **Reservierungsposten** bestätigt und die historischen Daten werden in der Tabelle **Trackingspezifikation** bestimmt. Weitere Informationen finden Sie unter [Designdetails: Aktive vs. historische Artikeltrackingposten](design-details-active-versus-historic-item-tracking-entries.md).  
  
Auswahllisten von den Feldern **Seriennummer** und **Chargennummer** zeigen eine Verfügbarkeit, die sowohl auf der Tabelle **Lagerposten** als auch der Tabelle **Reservierungsposten** basiert, ohne Datumsfilter. Die Matrix der Mengenfelder im Kopf des Fensters **Artikeltrackingzeile** zeigt dynamisch die Mengen und die Summen der Artikeltrackingnummern an, die Sie auf den Zeilen des Fensters eingegeben werden. Die Mengen müssen denen in der Belegzeile entsprechen, was durch eine Null **0** in den Feldern **Undefiniert** in der Kopfzeile des Fensters angezeigt wird.  
  
Um den Fluss der Serien- und Chargennummern durch das Lager zu koordinieren, sind die folgenden Regeln für die Eingabe von Daten im **Artikeltrackingzeilen**-Fenster vorhanden:  
  
* Für eingehende und ausgehende Artikeltrackingzeilen können Sie eine Seriennummer, mit oder ohne Chargennummer, nicht mehrmals in derselben Instanz der **Artikeltrackingzeilen**-Fensters eingeben. Wenn Sie versuchen, eine Kombination von Serien- oder Chargennummern einzugeben, die bereits im Fenster vorhanden ist, dann blockiert eine Fehlermeldung die Dateneingabe.  
* Für eingehende Artikelverfolgungszeilen können Sie den zugehörigen Beleg nicht buchen, wenn sich ein Artikel derselben Variante und mit derselben Seriennummer bereits im Lagerbestand befindet. Wenn Sie versuchen, eine positive Zeile für einen Lagerartikel mit derselben Variante und Seriennummer zu buchen, dann blockiert eine Fehlermeldung die Buchung. Für eingehende und ausgehende Artikeltrackingzeilen auf offenen Belegen können Sie jedoch die gleiche Kombination von Serien- oder Chargennummern haben, die sich auf verschiedene Herkunftsbelegzeilen beziehen, d. h., die in verschiedenen Instanzen des **Artikeltrackingzeilen**-Fensters vorhanden sind, bis der jeweilige Beleg gebucht ist.  
* Wenn der Artikel für die seriennummernspezifische Tracking oder die chargennummernspezifische Tracking eingerichtet ist, können Sie keine ausgehende Belegzeile erstellen, es sei denn, ein Artikel mit der definierten Serien- oder Chargennummer ist im Bestand vorhanden. Wenn Sie versuchen, einen ausgehenden Beleg Artikel mit einer Serien-/Chargennummer zu buchen, die sich nicht im Bestand befindet, dann blockiert eine Fehlermeldung die Buchung.  
  
Die Regeln für die Eingabe von Daten im Fenster **Artikeltrackingzeilen** unterstützen auch die Kopplungsprinzipien, die das Auftragstracking, die Planung und die Reservierung steuern. Weitere Informationen finden Sie unter [Designdetails: Artikeltracking und Planung](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Artikeltracking](design-details-item-tracking.md)
