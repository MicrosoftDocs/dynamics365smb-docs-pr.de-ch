---
title: Einrichten der Lagerwertberechnung und der Kostenrechnung | Microsoft Docs
description: In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.
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
ms.openlocfilehash: 184c7651fe8db60b55bd161bb5dc870df1ed01c5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241952"
---
# <a name="setting-up-inventory-valuation-and-costing"></a>Einrichten der Lagerwertberechnung und der Kostenrechnung
Um sicherzustellen, dass Lagerregulierungen ordnungsgemäss aufgezeichnet werden, müssen Sie verschiedene Felder und Seiten einrichten, bevor Sie Artikeltransaktionen durchführen können.

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

|**Bis**|**Siehe**|  
|------------|-------------|  
|Festlegen einer Lagerabgangsmethode für jeden Artikel, um zu steuern, wie dessen eingehende Kosten zum Ermitteln des Lagerwerts und der Kosten für verkaufte Waren verwendet werden sollen|[Neue Artikel registrieren](inventory-how-register-new-items.md)|  
|Sicherstellen, dass Kosten beim Buchen einer Lagertransaktion automatisch in die Finanzbuchhaltung gebucht werden|Wählen Sie auf der Seite **Lagereinrichtung** das Feld **Automatische Lagerbuchung**.|  
|Sicherstellen, dass die Soll-Kosten in die Finanzbuchhaltung gebucht werden, um in den Interimsfibukonten vor der eigentlichen Buchung eine Schätzung der fälligen Beträge und der Kosten der gehandelten Waren anzuzeigen|Wählen Sie auf der Seite **Lagereinrichtung** das Feld **Soll-Kosten buchen**.|  
|Einrichten der automatischen Regulierung von Kostenänderungen beim Buchen von Lagertransaktionen|[Artikelpreise justieren](inventory-how-adjust-item-costs.md)|  
|Festlegen, ob der durchschnittliche Einstandspreis nur pro Artikel oder pro Artikel für alle Lagerhaltungsdaten sowie für jede Variante des Artikels berechnet werden soll|Wählen Sie auf der Seite **Lagereinrichtung** das Feld **Einst.-Pr.(durchschn.)Ber.-Art**.|  
|Auswählen des gewünschten Zeitraums für die Berechnung der gewichteten Durchschnittskosten von Artikeln, für die die Durchschnittskostenmethode verwendet wird|Wählen Sie auf der Seite **Lagereinrichtung** das Feld **Durchschnittskostenperiode**.|  
|Definieren der Lagerbuchungsperioden zum Steuern des Lagerwerts im Zeitverlauf durch Sperren der Buchung von Transaktionen in geschlossenen Lagerbuchungsperioden|[Arbeiten mit Lagerbuchungsperioden](finance-how-to-work-with-inventory-periods.md)|  
|Sicherstellen, dass Verkaufsreklamationen mit der ursprünglichen ausgehenden Transaktion ausgeglichen werden, um den Lagerwert zu erhalten.|Das Feld **Einst.-Pr.-Rückverfolg. notw.** auf der Seite **Debitoren & Verkauf**|  
|Sicherstellen, dass Einkaufsreklamationen mit der ursprünglichen eingehenden Transaktion ausgeglichen werden, um den Lagerwert zu erhalten.|Das Feld **Einst.-Pr.-Rückverfolg. notw.** auf der Seite **Kreditoren & Einkauf**|
|Einrichten der Rundungsregeln, die beim Regulieren oder Vorschlagen von Artikelpreisen sowie beim Regulieren oder Vorschlagen von Einstandspreisen angewendet werden|**Rundungsmethode**|  

## <a name="see-also"></a>Siehe auch  
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Arbeiten mit  Business Central](ui-work-product.md)  
[Finanzen](finance.md)  
