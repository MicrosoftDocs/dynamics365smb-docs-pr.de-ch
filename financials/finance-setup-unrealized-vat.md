---
title: Einrichten von unrealisierter Mehrwertsteuer | Microsoft Docs
description: "Wenn Sie Einnahmen- und Ausgabenrechnung verwenden, können Sie angeben, wie Sie unrealisierte MWST. für Verkäufe und Einkäufe behandeln möchten."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 09/08/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 9a51b767006911a26e4e3a7abd55fbbeda05e0bc
ms.contentlocale: de-ch
ms.lasthandoff: 12/14/2017

---

# <a name="how-to-set-up-unrealized-vat-for-cash-based-accounting"></a>Vorgehensweise: Einrichten unrealisierter MWST für Einnahmen- und Ausgabenrechnung
Wenn Sie Einnahmen- und Ausgabenrechnungs-Methoden ausgleichen, können Sie in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] festlegen, wie unrealisierte MwSt. zu behandeln ist.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Verwenden von Fibukonten für unrealisierte MWST
Sie können festlegen, dass MWST.-Beträge beim Buchen einer Rechnung berechnet und auf ein temporäres Fibukonto gebucht werden und dass die Beträge erst dann auf das korrekte Fibukonto gebucht und in die MWST.-Abrechnungen einbezogen werden sollen, wenn die eigentliche Zahlung der Rechnung gebucht wird. Bevor Sie dies tun können, müssen Sie die MWST.-Buchungsmatrix ausfüllen.

Um die Konten für unrealisierte MWST. zu verwenden, führen Sie diese Schritte aus:
1. Wählen Sie ![Nach Seite oder Bericht suchen]Symbol (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Finanzbuchhaltung einrichen** eingeben. 
2. Auf der Seite **Finanzbuchhaltung Einrichtung** im Inforegister **Allgemein**, wählen Sie **Mehr anzeigen** und wählen Sie dann das Kontrollkästchen **Unrealisierte MwSt.** aus.
3. Schließen Sie die Seite.
4. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus**![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **MwSt Buchung einrichten** ein und wählen Sie dann den entsprechenden Link aus. 
5. Auf der Seite **MwSt.-Buchung einrichten** wählen Sie die MwSt.-Buchungsgruppe aus, und wählen Sie dann **Bearbeiten** aus. 
6. Im Feld **Unrealisierte MwSt-Art** wählen Sie eine Option aus, um zu bestimmen, wie Zahlungen auf dem Rechnungsbetrag (ohne MwSt.) und den MwSt.-Betrag selbst aufgeteilt wird und wie MwSt.-Beträge vom Konto "Unreal. MwSt." auf das realisierte MwSt.-Konto gebucht werden. Die Optionen werden in der folgenden Tabelle beschrieben.

| Option | Description |
| --- | --- |
| Leer | Wählen Sie diese Option, wenn Sie die Funktion "Unrealisierte MWST." nicht verwenden möchten. |
| Prozent | Zahlungen decken sowohl MwSt und den Rechnungsbetrag im Verhältnis zur prozentualen Zahlung des zu begleichenden Gesamtbetrags. Der gezahlte Steuerbetrag wird vom unrealisierten MwSt-Konto auf das realisierte MwSt-Konto gebucht. |
| Erster | Zahlungen decken zuerst die MwSt und dann den Rechnungsbetrag. In diesem Fall entspricht der vom Konto für die vereinnahmte Mehrwertsteuer auf das Konto für die realisierte Mehrwertsteuer transferierte Betrag dem Zahlungsbetrag (bis die Mehrwertsteuer vollständig beglichen ist). |
| Letzter | Zahlungen decken zuerst den Rechnungsbetrag und dann die MWST. In diesem Fall wird erst dann ein Betrag vom Konto für die unrealisierte Mehrwertsteuer auf das Konto für die realisierte Mehrwertsteuer transferiert, wenn der Zahlungsbetrag (ohne Mehrwertsteuer) vollständig beglichen ist. |
| Erste (ganz bezahlt) | Zahlungen decken zuerst die MwSt. (wie die  _Erste_ Option), aber es werden erst dann Beträge auf das Steuerkonto transferiert, wenn die MwSt. vollständig gezahlt wurde. |
| Letzte (ganz bezahlt) | Zahlungen decken zuerst den Rechnungsbetrag (wie unter der Option _Letzte_), aber es werden erst dann Beträge auf das Steuerkonto transferiert, wenn die MwSt. vollständig beglichen wurde. |

6. Geben Sie im Feld  **Unreal. Umsatzsteuerkonto** die entsprechende unrealisierte MwSt ein.

    > [!NOTE]  
>   Der MwSt-Betrag wird auf dieses Steuerkonto gebucht, wo er verbleibt, bis die Zahlung des Debitors gebucht wird. Der Betrag wird dann auf das Fibuposten für Umsatzsteuer transferiert.
7. Geben Sie im Feld **Unreal. Vorsteuerkonto** die entsprechende Fibukontonummer ein.

    > [!NOTE]  
>   Der MwSt-Betrag wird auf dieses Steuerkonto gebucht, wo er verbleibt, bis die Zahlung des Debitors gebucht wird. Der Betrag wird dann auf das Sachkonto für Mehrwertsteuerkäufe transferiert.

## <a name="see-also"></a>Siehe auch
[ Mehrwertsteuer einrichten ](finance-setup-vat.md)
