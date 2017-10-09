---
title: 'So gehts: Buchen der Lagerkosten in die Fibu | Microsoft Docs'
description: Beschreibt, wie physischen Produkte verwaltet werden, die Sie im Lagerbestand in Ihrem Lager verwalten.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 07/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 41c967c323f4bc156733575cf96925d2b64ddafe
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reconcile-inventory-costs-with-the-general-ledger"></a>Vorgehensweise: Abstimmen der Lagerregulierung mit der Fibu
Wenn Sie Lagertransaktionen buchen, z. B. Verkaufslieferungen, Einkaufsrechnungen oder Lagerregulierungen, werden die veränderten Artikelkosten in den Artikelwerteinträgen aufgezeichnet. Um diese Änderung des Lagerwerts in Ihren Finanzbüchern wiederzugeben, werden die Lagerkosten automatisch zu den entsprechenden Lagerkonten in der Finanzbuchhaltung gebucht. Für jede Lagertransaktion, die Sie buchen, werden die entsprechenden Werte im Fibuposten im Lagerkonto, im Korrekturkonto und im Lagerverbrauchskonto gebucht.

Die automatische Lagerbuchung wird durch das Feld **Automatische Lagerbuchung** im Fenster **Lagereinrichtung** definiert.

Selbst wenn Lagerkosten automatisch in die Finanzbuchhaltung gebucht werden, ist es immer noch notwendig sicherzustellen, dass die Kosten für Waren zur zugehörigen ausgehenden Transaktion weitergeleitet werden, insbesondere in Situationen, in denen Sie Waren verkaufen, bevor Sie den Kauf dieser Waren in Rechnung stellen. Dies wird als Kostenanpassung bezeichnet. Artikelkosten werden automatisch angepasst, wenn Sie Artikeltransaktionen buchen, Sie können jedoch auch Artikelpreise manuell anpassen. Weitere Informationen finden Sie unter [So geht's: Artikelkosten anpassen](inventory-how-adjust-item-costs.md).

## <a name="to-post-inventory-costs-manually"></a>Lagerkosten manuell buchen
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Lagerregulierung buchen** ein und wählen dann den zugehörigen Link aus.
2. Sie buchen eine Lagerkosten manuell im Fibuposten, indem Sie den Batchauftrag ausführen. Wenn Sie diesen Batchauftrag ausführen, werden auf Basis der Wertposten Fibuposten erstellt. Sie können die Posten buchen, damit diese pro Buchungsgruppe zusammengefasst werden.

> [!NOTE]  
> Beim Ausführen dieses Batchauftrages könnten Sie auf Fehler treffen, die ihre Ursache in fehlender Einrichtung oder nicht kompatibler Dimensionseinrichtung haben. Wenn die Stapelverarbeitung auf Fehler in der Dimensionseinrichtung stösst, setzt sie diese Fehler ausser Kraft und verwendet die Dimensionen des Wertpostens. Bei allen anderen Fehlern überspringt der Batchauftrag das Buchen der Wertposten und listet sie am Ende des Berichts im Abschnitt “Übersprungene Artikel” auf. Sollen diese Artikel gebucht werden, müssen Sie die Fehler beheben.

Wenn Sie eine Liste der Fehler anzeigen möchten, bevor Sie den Batchauftrag ausführen, führen Sie den Bericht **Lagereinstandspreise buchen - Test** aus. In dem Testbericht werden alle gefundenen Fehler aufgelistet, die während der Testbuchung aufgetreten sind. Sie können die Fehler dann beheben und die Stapelverarbeitung zum Buchen der Lagerregulierung ausführen, ohne dass irgendwelche Posten übersprungen werden.

Wenn Sie sich nur einen Überblick verschaffen möchten, welche Werte in der Finanzbuchhaltung gebucht werden können, das Buchen selbst aber nicht vornehmen möchten, können Sie die Stapelverarbeitung **Lagerregulierung buchen** ausführen, ohne dass die Werte tatsächlich in der Finanzbuchhaltung gebucht werden. Dazu müssen Sie auf der Anforderungsseite das Häkchen im Feld **Buchen** entfernen. In diesem Fall wird, wenn Sie der Batchauftrag ausführen, nur der Bericht erzeugt, der die Werte enthält, die im Fibuposten bereit stehen, aber nicht gebucht sind.

## <a name="to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger"></a>Überprüfen der Abstimmung zwischen den Lagerposten und der Fibu
Das Fenster **Lager – Sachpostenabstimmung** ermöglicht Folgendes:

- Gibt Aufschluss über Abstimmungsdifferenzen. Hierzu werden die in der Finanzbuchhaltung erfassten Werte mit den in den Inventurposten erfassten Werten verglichen.
- Zeigt nicht abgestimmte Einstandsbeträge in den Wertposten der Inventurposten so an, als seien sie entsprechenden lagerbezogenen Konten in der Finanzbuchhaltung zugeordnet, und vergleicht sie mit den tatsächlich erfassten Summen auf den gleichen Konten in der Finanzbuchhaltung.
- Spiegelt die Struktur der doppelten Buchführung aus der Finanzbuchhaltung wider, indem die Daten entsprechend dargestellt werden. So besitzt beispielsweise ein Lagerverbrauchsposten einen entsprechenden Lagerposten.
- Ermöglicht das Anzeigen der zugrunde liegenden Einstandsbeträge mittels Drilldown-Navigation.
- Beinhaltet Filter zum Eingrenzen der Analyse anhand von Datum, Artikel und Lagerort.
- Gibt Aufschluss über die Gründe für Abstimmungsdifferenzen in Form von Informationsmeldungen.


In der Spalte **Name** (am äußerst linken Rand des Gitters) werden die verschiedenen Fibukontoarten angezeigt, die mit Lagerbestand verknüpft sind.

Die Spalten **Lagerbestand**, **Lager (Interim)** und **Aktiviert Lager** enthalten die fakturierten, nicht fakturierten und WIP-Summen jeder Fibukontoart. Diese werden aus Wertposten berechnet, d.h., sie werden auf die Fibukontoarten übertragen, auf denen sie sich nach dem Buchen in die Finanzbuchhaltung befinden.

Die Spalte **Gesamt** enthält die (fett formatierte) Summe der Wertpostenbeträge in den drei Lagerbestandsspalten.

Die Spalte **Fibu gesamt** enthält die (fett formatierten) Beträge für die einzelnen, in der Fibu vorhandenen Fibukontoarten. Diese Werte werden auf der Grundlage von Fibuposten berechnet, stellen also die Lagerkosten dar, die bereits in die Finanzbuchhaltung gebucht wurden.

Die Spalte **Differenz** enthält die Differenz zwischen **Fibu gesamt** und **Gesamt**.

Am oberen Rand des Fensters **Lager - Sachpostenabstimmung** können Sie mithilfe von Filtern beispielsweise die Periode eingrenzen, für die Sie Informationen ermitteln möchten.

Wenn Sie ein Häkchen in das Kontrollkästchen **Warnung anzeigen** setzen und wenn es Abweichungen zwischen den Lagerbestandssummen und den Werten in der Fibu gesamt gibt, werden im Feld **Warnung** des Gitters Meldungen angezeigt, in denen die jeweilige Abweichung beschrieben wird. Wenn Sie das Feld "Warnung" auswählen, werden weitere Informationen zum Inhalt der Warnung angezeigt.

Wenn Sie alle entsprechenden Filter eingegeben haben, wählhen Sie die Aktion **Matrix anzeigen**. Die Daten werden berechnet, und das Matrixfenster wird geöffnet.

In der äusserst linken Spalte des Gitters werden die verschiedenen Kontoarten der Finanzbuchhaltung angezeigt, die mit dem Lagerbestand verknüpft sind. Für jede dieser Kontoarten werden im Gitter die fakturierten, nicht fakturierten (Interims-) und WIP-Lagerbestandssummen angezeigt. Diese Summen wurden aus den Wertposten berechnet.

In den nächsten Spalten werden für dieselben Kontoarten die Summen angezeigt, die aus den Fibuposten berechnet wurden.

Wählen Sie in einem der Summenfelder den Betrag, damit die Lagerberichtsposten angezeigt werden, mit denen die Summen berechnet wurden. Für Lagerbestandssummen sind die Lagerberichtsposten die Summen der Wertposten für die Artikel. Für die Werte in Fibu gesamt sind die Lagerberichtsposten die Summen aus den Fibuposten.

## <a name="see-also"></a>Siehe auch  
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)    
[Arbeiten mit [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

