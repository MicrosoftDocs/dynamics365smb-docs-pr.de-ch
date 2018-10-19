---
title: Servicebuchung | Microsoft Docs
description: "Mit der Funktion \"Servicebuchung\" können Sie Belege effizient verarbeiten und damit eine erfolgreiche Debitorenservicepolitik sicherstellen. Sie können Belege erstellen und gebuchte Belege aktualisieren und Posten sowohl im Servicebereich als auch in anderen Modulen erstellen, um eine ordnungsgemässe Aktualisierung sicherzustellen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 75f0fd760978b0efc4ab86b8d17a815280a09799
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="service-posting"></a>Servicebuchung
Mit der Funktion "Servicebuchung" können Sie Belege effizient verarbeiten und damit eine erfolgreiche Debitorenservicepolitik sicherstellen. Sie können Belege erstellen und gebuchte Belege aktualisieren und Posten sowohl im Servicebereich als auch in anderen Modulen erstellen, um eine ordnungsgemässe Aktualisierung sicherzustellen.  

> [!NOTE]  
>  Nachfolgend wird die Servicebuchung erläutert, unabhängig davon, wie Artikel physisch im Lager bearbeitet werden.  
>   
>  An einem Standort, der nicht so eingerichtet wurde, dass ein Lagerdurchlauf erforderlich ist, führen Sie die Buchungsaktionen direkt im Fenster **Servicezeilen**  aus. An Standorten, die Lagerdurchlaufzeiten vorsehen, buchen Sie die beschriebenen Aktionen, ausser "Liefern" und "Verbrauchen", indirekt durch je nach Einrichtung verschiedene Lagerlieferfunktionen. Weitere Informationen finden Sie unter [Entnahme von Artikeln mit Kommissionierungen](warehouse-how-to-pick-items-with-inventory-picks.md).  

## <a name="ship"></a>Lieferung  
Mit der Option "Liefern" können Sie die relevanten Artikel und Zeiten erfassen, die nach Abschluss des Service in den Zeilen eines Serviceauftrags eingegeben wurden. Eine gebuchte Lieferung wird erstellt, und das Lagermodul sowie weitere Module in [!INCLUDE[d365fin](includes/d365fin_md.md)] werden aktualisiert, um die Artikel zu erfassen, die aus dem Lager entnommen und an den Kunden gesendet wurden. Im Einzelnen werden Lagerposten, Wertposten, Serviceposten und Garantieposten erstellt.  

Wenn der Lagerort so eingerichtet wurde, dass ein Lagerdurchlauf erforderlich ist, dann erfolgt die Lieferung und Umlagerung der Servicezeilenartikel auf die gleichen Weise wie für andere Herkunftsbelege. Der einzige Unterschied besteht darin, dass Servicezeilenartikel extern oder intern verbraucht werden können, wozu zwei unterschiedliche Freigabefunktionen benötigt werden.

## <a name="invoice"></a>Fakturieren  
Zum Erstellen einer Rechnung an den Debitor, dem Sie den Service in Rechnung stellen möchten, müssen Sie die Option "Rechnung" verwenden. Normalerweise ist die Differenz zwischen der gelieferten Menge, die mit der Funktion **Warenausgang buchen** erfasst wurde, und der verbrauchten Menge, die mit der Funktion **Verbrauch buchen** erfasst wurde, Gegenstand der Rechnung. Sie können nicht fakturieren, was Sie nicht geliefert haben. Wenn Sie die Funktion **Rechnungen buchen** ausführen, wird eine gebuchte Servicerechnung erstellt, und die zuvor gebuchten Belege werden aktualisiert, damit sie dieselben Mengen wie in der ausgegebenen Rechnung enthalten. Wie bei anderen Buchungsverfahren werden die relevanten Posten einschliesslich Sachposten generiert.  

## <a name="ship-and-invoice"></a>Liefern und fakturieren  
Mit der Option "Liefern und fakturieren" können Sie gleichzeitig eine Rechnung und eine Servicelieferung erstellen.  

## <a name="ship-and-consume"></a>Liefern und verbrauchen  
Mit der Option "Liefern und Verbrauchen" können Artikel, Einstandspreise oder Stunden erfasst und gebucht werden, die für den Service aufgewendet wurden, die dem Debitor jedoch nicht in Rechnung gestellt werden können. Es wird keine Rechnung ausgegeben, aber Sie können eine Servicelieferung und einen Serviceverbrauch gleichzeitig ausgeben, um zu berücksichtigen, dass dem Debitor einige Artikel oder Stunden kostenlos zur Verfügung gestellt wurden. Die entsprechenden Posten werden ebenfalls erstellt, um den Verbrauch zu erfassen.  

> [!NOTE]  
>  Im Rahmen des Servicebuchungsverfahrens können Sie auch eine teilweise Buchung vornehmen. Sie können eine Teillieferung oder eine Teilrechnung erstellen, indem Sie vor dem Buchen die Felder **Zu liefernde Menge** und/oder **Zu fakturierende Menge** der einzelnen Servicezeilen der Serviceaufträge ausfüllen. Beachten Sie, dass Sie keine Rechnung für etwas erstellen können, das Sie nicht geliefert haben. Dies bedeutet, dass Sie eine Lieferung bereits erfasst haben müssen oder Lieferung und Rechnung zur gleichen Zeit erstellen müssen.  

Nach Abschluss des Buchungsvorgangs können Sie die gebuchten Servicebelege in den entsprechenden Fenstern **Gebuchte Servicelieferung** und **Gebuchte Servicerechnung** anzeigen. Die erstellten gebuchten Posten können in unterschiedlichen Fenstern angezeigt werden, die gebuchte Posten enthalten, wie z. B. **Fibuposten**, **Lagerposten**, **Lagerplatzposten**, **Serviceposten**, **Projektposten** und **Garantieposten**.  

## <a name="to-view-information-about-a-posted-service-document"></a>So zeigen Sie zusätzliche Informationen zu einem gebuchten Servicebeleg an  
Wenn Sie eine Servicerechnung, eine Servicelieferung oder eine Servicegutschrift buchen, werden die Informationen im Beleg in das Fenster **Gebuchte Servicerechnung**, **Gebuchte Dienstlieferung** bzw. **Gebuchte Servicegutschrift** übertragen. In diesen Fenstern können keine Einträge eingegeben, geändert oder gelöscht werden. Sie können aus diesen Fenstern einen Lieferschein, eine Rechnung oder eine Gutschrift drucken.  

Die folgende Vorgehensweise verwendet eine gebuchte Servicerechnung als Beispiel, Sie können jedoch dieselben Schritte auf gebuchte Servicelieferungen und gebuchte Gutschriften anwenden.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Gebuchte Servicerechnung** ein, und wählen dann den zugehörigen Link aus.  
2. Öffnen Sie die gebuchte Servicerechnung, die Sie anzeigen möchten.  
3. Um eine Übersicht über die gebuchte Rechnung zu erhalten, wählen Sie die **Statistik** Aktion.  

    Das Fenster **Serviceauftragsstatistik** wird geöffnet. In dem jeweiligen Fenster werden Informationen wie Menge, Betrag, MWST., Kosten, Deckungsbeitrag und Kreditlimit des Debitors für den gebuchten Beleg angezeigt.

## <a name="see-also"></a>Siehe auch  
[Buchen von Serviceaufträgen](service-how-to-post-service-orders.md)   
[Erstellen von Serviceaufträgen](service-how-to-create-service-orders.md)

