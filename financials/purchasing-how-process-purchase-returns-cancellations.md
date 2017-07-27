---
title: "Einkaufsrücklieferung verwenden, um Stornierungen zu verarbeiten| Microsoft Docs"
description: "Erklärt, wie Sie eine Einkaufsgutschrift erstellen und buchemn, wenn Sie Artikel an einen Kreditor zurückgeben möchten oder eingekaufte Services stornieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 06/21/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 887add30a1ec72b7de961e03161bfc34826980fc
ms.contentlocale: de-ch
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-process-purchase-returns-or-cancellations"></a>Vorgehensweise: Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen
Wenn Sie Artikel an Ihren Kreditor zurückschicken oder Dienstleistungen löschen wollen, die Sie eingekauft haben, können Sie eine Einkaufsgutschrift erstellen und buchen, die die angeforderte Änderung im Hinblick auf die ursprünglichen Einkaufsrechnung angibt. Um korrekte Einkaufsrechnungsinformationen zu berücksichtigen, können Sie die Einkaufsgutschrift aus der gebuchten Einkaufsrechnung erstellen oder eine Kopierfunktion verwenden.

> [!NOTE]  
>   Wenn eine gebuchte Einkaufsrechnung noch nicht bezahlt wurde, können Sie die **Korrigieren** oder **Abbrechen**-Funktionen auf der gebuchten Einkaufsrechnung verwenden, um die entsprechenden Transaktionen automatisch zu stornieren. Diese Funktionen arbeiten nur für nicht geleistete Rechnungen, und sie unterstützen nicht Teil-Reklamationen oder Kündigungen. Weitere Informationen finden Sie unter [Vorgehensweise: Ändern oder löschen von unbezahlten Einkaufsrechnungen]](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Normalerweise erstellen Sie eine Einkaufsgutschrift als Antworten auf eine Gutschrift, die Ihnen von einem Kreditor gesendet wird. Die Einkaufsgutschrift fungiert als Ihre interne Dokumentation für den Gutschriftsprozess für Buchhaltungszwecke.

Die Änderung mögen mit allen Produkten auf der Rechnung der ursprünglichen Einkaufsrechnung oder nur mit einigen der Produkte, verknüpft werden. Entsprechend können Sie die erhaltenen Artikel teilweise zurückgeben oder Teil-Vergütung von erhaltenen Services. In diesem Fall müssen Sie die kopierte Einkaufsrechnung bearbeiten.

Zusätzlich zur ursprünglich gebuchten Einkaufsrechnung können Sie die Einkaufsgutschrift für andere Einkaufsbelege übernehmen, beispielsweise einer anderen gebuchten Einkaufsrechnung, da der Kreditor auch die Artikel zurücksendet, die mit dieser Rechnung geliefert werden.

Die Gutschriftsbuchung stellt auch jegliche Artikel Zu-/Abschläge wieder her, die dem gebuchten Beleg zugewiesen wurden, sodass die Wertposten des Artikels wieder identisch sind, wie bevor der Artikel Zu-/Abschlag zugewiesen wurde.

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Eine neue Einkaufsgutschrift aus einer gebuchte Einkaufsrechnung erstellen
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie das Feld **Gebuchte Einkaufsrechnung**, um das Fenster **Korrekturgutschrift erstellen** zu öffnen, und wählen Sie die gebuchte Einkaufsrechnung aus, die Sie stornieren möchten.

    Die meisten Felder im Einkaufsgutschriftskopf werden mit den Informationen aus der gebuchten Einkaufsrechnung ausgefüllt. Sie können alle Felder bearbeiten, zum Beispiel mit neuen Daten, die die Rückholvereinbarung wiedergeben.
3. Bearbeiten Sie Informationen über die Zeilen entsprechend der Vereinbarung, wie die Anzahl der zurückzuerstattenden Artikel oder der gutzuschreibende Betrag.
4. Wählen Sie die Aktion **Posten ausgleichen...** aus.
5. Im Fenster **Kreditorenposten zuweisen** wählen Sie die Zeile mit dem gebuchten Einkaufsbeleg, die Sie der Einkaufsgutschrift zuordnen möchten, und wählen Sie dann **Zuweisungs-ID festlegen** aus. Die Nummer der Einkaufsgutschrift wird im Feld **Zuweisungs-ID** eingefügt.
6. Geben Sie in jeder Zeile im Feld **Anzuwendender Betrag** den Betrag ein, den Sie ausgleichen möchten, wenn dieser kleiner ist als der ursprüngliche Betrag.

    Im unteren Bereich des Fensters **Kreditposten ausgleichen** können Sie den Gesamtbetrag sehen, um alle beteiligten Posten zu stornieren, nämlich wenn der Wert im Feld **Saldo** Null ist.
7. Wählen Sie die Schaltfläche **OK** aus. Wenn Sie die Einkaufsgutschrift buchen, wird sie für die angegebenen Einkaufsbelege angewandt.

    Nachdem Sie die erforderlichen Einkaufsgutschriftszeilen erstellt oder bearbeitet haben, und der Ausgleich einzelner oder mehrerer Posten angegeben wird, können Sie fortfahren, die Einkaufsgutschrift zu buchen.
8. Wählen Sie die Aktion **Buchen** aus.

Die gebuchten Einkaufsrechnungen, auf die Sie die Gutschrift anzuwenden, werden jetzt umgekehrt. Wenn Sie bereits die ursprüngliche Rechnung bezahlt haben, sollte der Lieferant die Zahlung jetzt an Sie jetzt zurückerstatten. Wenn die Gutschrift nur für einen Teil des Produkts auf der ursprünglichen Rechnung gilt, können Sie nur den Restbetrag auf der Rechnung der ursprünglichen Einkaufsrechnung bezahlen, um sie zu schließen.

Die Einkaufsgutschrift wird entfernt und durch einen neuen Beleg in der Liste der gebuchten Einkaufsgutschriften ersetzt.

## <a name="to-create-a-purchase-credit-memo-from-scratch"></a>So erstellen Sie eine Einkaufsgutschrift von Grund auf
1. Alternativ wählen Sie  das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufskreditor-Memo** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie **Neu**, um eine neue leere Einkaufsgutschrift zu öffnen.
3. Geben Sie im Feld **Kreditor** den Namen eines vorhandenen Kreditors ein.
4. Wählen Sie die **Beleg kopieren**-Aktion aus.
5. Wählen Sie im Fenster **Einkaufsdokument kopieren** im Feld **Dokumenttyp** **Rechnung buchen** aus.
6. Wählen Sie das Feld **Belegnummer**, um das Fenster **Gebuchte Verkaufsrechnung.** zu öffnen, und wählen Sie dann die gebuchte Einkaufsrechnung aus, die die Zeile enthält, die Sie stornieren möchten.
7. Wählen Sie das Kontrollkästchen **Zeilen neu berechnen**, wenn die kopierten gebuchten Einkaufsrechnungszeilen, mit einzelnen Änderungen im Artikelpreis und im Einstandspreis, aktualisiert werden sollen, da die Rechnung gebucht wurde.
8. Wählen Sie die Schaltfläche **OK** aus. Die kopierten Rechnungszeilen werden in die Einkaufsgutschrift eingefügt.
9. Schließen Sie die Einkaufsgutschrift ab, so wie dies unter "Eine neue Einkaufsgutschrift aus einer gebuchte Einkaufsrechnung erstellen" in diesem Thema erklärt ist.

## <a name="see-also"></a>Siehe auch
[Einkauf](purchasing-manage-purchasing.md)  
[Vorgehensweise: Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Vorgehensweise: Ändern oder Löschen einer unbezahlten Einkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

