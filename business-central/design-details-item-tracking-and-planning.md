---
title: 'Designdetails: Artikeltracking und -planung | Microsoft Docs'
description: 'Da sie im Reservierungssystem gespeichert werden, werden Artikeltrackingnummern vollständig mit Auftragstrackingdatensätzen abgestimmt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
---
# Designdetails: Artikeltracking und Planung
Da sie im Reservierungssystem gespeichert werden, werden Artikeltrackingnummern vollständig mit Auftragstrackingdatensätzen abgestimmt. Dies bedeutet, dass Artikel mit Auftragstrackingdatensätzen Artikeltrackingnummern zugeordnet werden können. Andererseits können Artikel, die Artikeltrackingnummern haben, zu Auftragstrackingdatensätzen werden. Weitere Informationen finden Sie unter [Designdetails: Artikeltrackingdesign](design-details-item-tracking-design.md).

Weitere Informationen zu den integrierten Systemen finden Sie unter [Designdetails: Reservierungen, Auftragstracking und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md).

Da das Auftragstracking sich nur auf bestimmte Artikelausgleiche bezieht, gilt die Koordination mit Artikeltrackingnummern nur für Artikel, die zur Verwendung einem bestimmten Artikeltracking eingerichtet wurden. Dies wird durch die Felder **Seriennr.-spezifische Verf.** und **Chargennr.-spezifische Verf.** auf der Artikelkarte festgelegt, die Folgendes angeben:

- Der Artikel muss eine Seriennummer oder Chargennummer tragen, wenn er gebucht wird.
- Der Artikel muss dieselbe Seriennummer oder Chargennummer anwenden, wenn er als ausgehend gebucht wird.

In Anlehnung an Standardofferte/nachfrage-Ausgleichsprinzipien gleichen das Planungssystem und die zugehörige Auftragstrackingfunktion nur den Bedarf ab und verlangen Artikeltrackingnummern, wenn der jeweilige Artikel ein spezifisches Artikeltracking benutzt. In allen anderen Fällen ignorieren die Planungs- und die Artikeltrackingfunktionen Artikeltrackingnummern, wenn sie das Prinzip Vorrat zur Nachfragedeckung oder Nachfragedeckung für den Vorrat anwenden. Weitere Informationen finden Sie unter [Designdetails: Reservierung, Auftragstracking und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md).

Wenn beispielsweise das Auftragstracking für einen bestimmten Artikel aktiv ist, bedeutet dies, dass Datensätze für den Artikel bereits in der Tabelle **Reservierungsposten** vorhanden sind, die der Kern des Reservierungssystems ist, bevor die Artikeltrackingnummern definiert sind. Daher gelten die folgenden Kopplungseinschränkungen für die Artikeltrackingnummern, um ein Bedarfsverursachertracking durchzuführen.

- Bedarf mit einer Seriennummer oder einer Chargennummer kann nur Vorrat mit derselben Seriennummer oder Chargennummer abdecken.
- Bedarf ohne Seriennummer oder Chargennummer kann Vorrat mit oder ohne Seriennummer oder Chargennummer abdecken.

Abgesehen von ihren Auswirkungen auf das dynamische Auftragstracking beeinflussen die Artikeltrackingkopplungseinschränkungen das Planungssystem nicht erheblich.

Auf der Zugangsseite wird eine Serien- oder Chargennummer normalerweise nicht direkt vor dem Buchen eines Auftrags eingegeben, wie z. B. eine Einkaufslieferung in das Lager. Wenn eine Serien- oder Chargennummer auf der Bedarfsseite, etwa auf einem Verkaufsauftrag, eingegeben wird, ist diese Serien- oder Chargennummer bereits im Lagerbestand. Entsprechend sind Artikeltrackingnummern in der Regel kein Problem in der Beschaffungsplanung.

Für Artikel, die ein bestimmtes Artikeltracking verwenden, müssen alle Bedarfe mit Serien- oder Chargennummern durch entsprechenden Vorrat abgeglichen werden. In den meisten Fällen ist es nicht sinnvoll, eine bestimmte Serien- oder Chargennummer neu zu sortieren; daher wird die Planung von Einkaufs- oder Produktionsvorräten wahrscheinlich nicht beeinflusst. Wenn Artikel aus einem Lagerort in einen anderen übertragen werden, ist es jedoch wahrscheinlich, dass die Übertragung spezifisch für eine bestimmte Charge ist, sodass Planungsübertragungsvorräte durch die spezifische Kopplungseinschränkung beeinflusst werden.

Weitere Informationen finden Sie unter [Designdetails: Übertragung in der Planung](design-details-transfers-in-planning.md)

## Ausgleich von Bedarf und Vorrat
Wenn ein Artikel ein bestimmtes Artikeltracking erfordert, dann wird ein Auftragstrackinglink aus allen Trackingbedarfen des Artikels zu allen entsprechenden Artikeltrackingvorräten erstellt, mit der einzigen Einschränkung, dass der Vorrat vor dem Bedarf kommen muss. Wenn unter diesen Umständen kein Artikeltrackingzubehör gefunden werden kann, das dem trackingspezifischen Bedarf des Artikels entspricht, wird sofort neuer Trackingvorrat ohne Berücksichtigung der Bestellmenge, Planungsparameter oder Neuplanung für vorhandenen Bedarf derselben Serien- oder Chargennummer erstellt.

Wenn Artikeltrackingnummern auf der Bedarfsseite oder auf der Vorratsseite zugewiesen werden, ohne dass ein bestimmtes Artikeltracking erforderlich ist, dann wird ein Auftragstrackinglink von dem Bedarf zu diesem dem Vorrat erstellt, basierend auf dem passendsten Timing und der geeignetsten Menge, wie im normalen Ausgleichsverfahren. Die angegebene Artikeltrackingnummer geht in den Auftragstrackingdatensatz in der gleichen Weise ein, wie eine angegebene Artikeltrackingmenge ein Ende des Auftragstrackinglinks definiert. Das bedeutet, dass die Artikeltrackingnummer, die eingetragen wird, beibehalten wird, während sie auch Teil des Bedarfsverursacherdatensatzes ist.

Wenn Artikeltrackingnummern auf der Bedarfsseite zugeordnet werden, ohne dass ein bestimmtes Artikeltracking erforderlich ist, wird dieser Vorrat als vom Planungssystem korrigiert betrachtet. Grössenanpassungen oder Neuplanungen werden nicht für diesen Vorrat vorgeschlagen, doch wird dieser berücksichtigt, wenn das Planungssystem versucht, dem Bruttobedarf zu genügen.

Weitere Informationen finden Sie unter [Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)  

## Siehe auch  
[Designdetails: Artikeltrackingdesign](design-details-item-tracking-design.md)  
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)  
[Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]