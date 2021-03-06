---
title: Terminberechnung für Verkäufe  | Microsoft Docs
description: Die Anwendung berechnet automatisch das Datum, an dem Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum im Lagerbestand vorhanden ist. Dies ist das Datum, an dem Sie erwarten können, dass Artikel, die an einem bestimmten Datum bestellt wurden, zur Kommissionierung verfügbar sind.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 26782d211d205bb5414c5bd423ccf240f70f197e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748482"
---
# <a name="date-calculation-for-sales"></a>Terminberechnung für Verkäufe
[!INCLUDE[prod_short](includes/prod_short.md)] berechnet automatisch das frühestmögliche Datum, an dem ein Artikel in einer Verkaufsauftragszeile geliefert werden kann.

Wenn der Debitor ein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel für die Kommissionierung zur Verfügung stehen müssen, damit dieser Liefertermin eingehalten werden kann.

Falls der Debitor kein bestimmtes Lieferdatum wünscht, wird das Datum berechnet, an dem die Artikel geliefert werden können, ausgehend von dem Datum, an dem die Artikel für die Kommissionierung zur Verfügung stehen.

## <a name="calculating-a-requested-delivery-date"></a>So berechnen Sie ein gewünschtes Wareneingangsdatum:
Wenn Sie in einer Verkaufszeile ein gewünschtes Lieferdatum eingeben, wird dieses Datum zum Ausgangspunkt für die folgenden Berechnungen.

- Gewünschtes Lieferdatum - Transportzeit = Geplantes Warenausgangsdatum
- Geplantes Warenausgangsdatum - Ausgeh. Lagerdurchlaufzeit = Warenausgangsdatum

Falls die Artikel am Lieferdatum zur Kommissionierung zur Verfügung stehen, kann der Verkaufsvorgang fortgesetzt werden. Anderenfalls wird eine Warnmeldung wegen fehlenden Bestands angezeigt.

> [!Note]
> Falls Ihr Prozess auf einer Rückwärtsberechnung basiert, beispielsweise bei Verwendung des gewünschten Lieferdatums zum Ermitteln des geplanten Warenausgangsdatums, empfiehlt sich die Verwendung von Datumsformeln mit fester Dauer, wie etwa „5D“ für fünf Tage oder „1W“ für eine Woche. Datumsformeln ohne feste Dauer, wie etwa „LW“ für laufende Woche oder „LM“ für laufender Monat können zu fehlerhaften Datumsberechnungen führen. Weitere Informationen über Datumsformeln finden Sie unter [Arbeiten mit Datumsangaben und Uhrzeiten in Kalendern](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>So berechnen Sie das frühestmögliche Lieferdatum:
Wenn Sie kein angefordertes Lieferdatum auf der Verkaufsauftragszeile angeben oder das angeforderte Lieferdatum nicht eingehalten werden kann, wird das früheste Datum, an dem die Artikel verfügbar sind, berechnet. Dieses Datum wird dann im Feld Versanddatum auf der Zeile eingegeben, und das Datum, an dem Sie planen, die Artikel zu liefern, sowie das Datum, an dem Sie an den Kunden ausgeliefert werden, werden anhand der nachfolgenden Formeln berechnet.

- Warenausgangsdatum + Ausgeh. Lagerdurchlaufzeit = Geplantes Warenausgangsdatum
- Geplantes Warenausgangsdatum + Transportzeit = Geplantes Lieferdatum


## <a name="see-also"></a>Siehe auch  
 [Terminberechnung für Einkäufe](purchasing-date-calculation-for-purchases.md)   
 [Lieferterminzusagen-Daten berechnen](sales-how-to-calculate-order-promising-dates.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]