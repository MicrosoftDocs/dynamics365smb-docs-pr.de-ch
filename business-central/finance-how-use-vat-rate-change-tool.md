---
title: Verwenden des Mehrwertsteuersatz-Änderungstools | Microsoft-Dokumentation
description: Das MWST-Satz-Änderungstool verwenden
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/06/2020
ms.author: andregu
ms.openlocfilehash: 0fe23bb6b1d4ce6fbf73a1978a66f6d47b8e78fe
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992268"
---
# <a name="use-the-vat-rate-change-tool"></a>Das MWST-Satz-Änderungstool verwenden

## <a name="understanding-the-vat-rate-conversion-process"></a>Verstehen des Prozesses der Umrechnung für die MWST.-Satzänderung  
Die das MWST-Änderungstool führt MWST-Konvertierungen für Masterdaten, Erfassungsjournale und Aufträge auf verschiedene Arten aus. Die ausgewählten Masterdaten und die Erfassungsjournale werden von der neuen Produktbuchungsgruppe oder der MWST.-Produktbuchungsgruppe aktualisiert. Wenn eine Bestellung vollständig oder teilweise geliefert wurde, behalten die gelieferten Artikel die aktuelle Produktbuchungsgruppe oder MWST.-Produktbuchungsgruppe. Eine neue Auftragszeile wird für die nicht gelieferten Artikel erstellt und aktualisiert, um aktuelle und neue Produktbuchungsgruppen oder MWST.-Produktbuchungsgruppen aufeinander auszurichten. Darüber hinaus werden Artikelzu-/-abschlagszuweisungen, Reservierungen und Artikeltrackinginformationen entsprechend aktualisiert.  

Es gibt mehrere Elemente, die das Werkzeug nicht konvertiert:

* Verkaufs- oder Einkaufsbestellungen und -rechnungen, in denen Lieferungen gebucht wurden. Diese Belege werden unter Verwendung des aktuellen Mehrwertsteuersatzes gebucht.  
* Belege mit gebuchten Vorauszahlungsrechnungen. Beispielsweise haben Sie Vorauszahlungen auf Rechnungen geleistet oder erhalten, die nicht vollständig erledigt sind, bevor Sie das Mehrwertsteuersatz-Änderungstool verwenden. In diesem Fall gibt es eine Differenz zwischen der MWST., die fällig ist, und der MWST., die in den Vorauszahlungen bezahlt wurde, wenn die Rechnung abgeschlossen wird. Das Mehrwertsteuersatz-Änderungstool überspringt diese Belege, und Sie müssen sie manuell aktualisieren.  
* Direktlieferungen oder Spezialaufträge.  
* Verkaufs- oder Einkaufsbestellungen mit Lagerintegration, wenn sie teilweise geliefert oder erhalten werden.  
* Serviceverträge.  

### <a name="to-prepare-vat-rate-change-conversions"></a>So bereiten Sie Mehrwertsteuersatzänderungen vor  
Bevor Sie das Mehrwertsteuersatz-Änderungstool einrichten, müssen Sie die folgenden Vorbereitungen durchführen.

* Wenn Sie Transaktionen haben, die verschiedene Sätze verwenden, müssen sie in verschiedene Gruppen aufgeteilt werden, entweder durch Erstellen neuer Fibukonten für die einzelnen Sätze oder mithilfe von Datenfiltern, um Transaktionen entsprechend dem Satz zu gruppieren.  
* Wenn Sie neue Fibukonten erstellen, müssen Sie auch neue allgemeine Buchungsgruppen erstellen.  
* Um die Anzahl der Belege zu verringern, die konvertiert werden, buchen Sie möglichst viele Belege, und reduzieren Sie nicht gebuchte Belege auf ein Minimum.  
* Sichern von Daten.

### <a name="to-set-up-the-vat-rate-change-tool"></a>So richten Sie das Mehrwertsteuersatz-Änderungstool ein  
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Einrichtung der MWST-Satzänderung** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf den Inforegistern **Masterdaten**, **Buch.-Erfassungsjournale** und **Belege** einen Buchungsgruppenwert aus der Liste der Optionen für erforderliche Felder aus. Für jede Gruppe können Sie wählen, ob Sie MWST-Produktbuchungsgruppen oder allgemeine Produktbuchungsgruppen konvertieren oder beide Werte konvertieren möchten, sofern sie im Masterdatenelement verfügbar sind. Für einige Regionen können Sie auch einen Filter festlegen, um nur eine Teilmenge von Werten zu konvertieren, z. B. Fibukonten. 

### <a name="to-set-up-product-posting-group-conversion"></a>So richten Sie die Produktbuchungsgruppenkonvertierung ein  
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Einrichtung der MWST-Satzänderung** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Einrichtung der MWST-Satzänderung** entweder die Option **Umrech. für MWST-Produktbuchungsgruppe** oder **Umrech. für Produktbuchungsgruppe** Aktion.  
3. Geben Sie im Feld **Code ab** die aktuelle Buchungsgruppe ein.  
4. Geben Sie den neuen Standort in dem Feld **Cod zu** ein.  

### <a name="to-perform-vat-rate-change-conversion"></a>So führen Sie eine Umrechnung für die MWST.-Satzänderung aus  
Sie verwenden das MwSt.-Satz-Änderungstool, um Änderungen im Standard-MwSt.-Satz zu verwalten. Sie führen MwSt.- und Buchungsgruppenkonvertierungen durch, um Mehrwertsteuersätze zu ändern und für präzise MwSt.-Berichte zu sorgen. Abhängig von Ihrem Setup werden folgende Änderungen vorgenommen:  

* MWST.-Buchungsgruppen und Buchungsgruppen werden konvertiert.  
* Änderungen werden in den Fibuposten, den Debitoren, den Kreditoren, den offenen Belegen, den Erfassungsjournalzeilen usw. implementiert.  

> [!IMPORTANT]  
>  Bevor Sie die Umrechnung für MWST-Satzänderungen ausführen, können Sie die Konvertierung testen. Um dies zu tun, führen Sie die Schritte unten aus, stellen Sie aber sicher, dass Sie die Kontrollkästchen **Konvertierung durchführen** und **Tool zum Ändern des MWST-Satzes abgeschlossen** deaktivieren. Während der Testkonvertierung wird das Feld **Konvertiert** in der Tabelle **Protokollposten für MWST-Satzänderung** gelöscht und das Feld **Konvertierungsdatum** in der Tabelle **Protokollposten für MWST-Satzänderung** ist leer. Nach der Umrechnung wählen Sie auf der Registerkarte Start, in der Gruppe Prozess die Option **Änderungsprotokollposten für MWST-Satz** aus, um die Ergebnisse der Umrechnung anzuzeigen. Prüfen Sie jeden Posten, bevor Sie die Umrechnung ausführen. Insbesondere überprüfen Sie Transaktionen, die einen alten MWST-Satz verwenden.     

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Änderung des MWST-Satzes** ein und wählen Sie dann den Link **Einrichtung der MWST-Satzänderung**.  
2. Vergewissern Sie sich, dass Sie bereits die MWST.-Produktbuchungsgruppen-Umrechnung oder die Produktbuchungsgruppen-Umrechnung eingerichtet haben.  
3. Wählen Sie das Kontrollkästchen **Konvertierung durchführen**.  

    > [!IMPORTANT]  
    >  Deaktivieren Sie das Kontrollkästchen **Tool zum Ändern des MWST-Satzes abgeschlossen**. Das Kontrollkästchen wird automatisch aktiviert, wenn die Umrechnung für die MWST.-Satzänderung abgeschlossen ist.  

4. Wählen Sie die Aktion **Konvertieren** aus.  
5. Nachdem die Konvertierung abgeschlossen ist, wählen Sie die Aktion **Änderungsprotokollposten für MWST-Satz**, um die Ergebnisse der Konvertierung anzuzeigen.  

> [!IMPORTANT]  
>  Nachdem die Umrechnung abgeschlossen ist, wird das Feld **Konvertiert** in der Tabelle **Protokollposten für MWST-Satzänderung** ausgewählt und das Feld **Konvertierungsdatum** in der Tabelle **Protokollposten für MWST-Satzänderung** wird mit dem Umrechnungsdatum ausgefüllt.  
## <a name="see-also"></a>Siehe auch  
[Mehrwertsteuer einrichten](finance-setup-vat.md)  
[Einrichten von unrealisierter Mehrwertsteuer](finance-setup-unrealized-vat.md)      
[MWST an die Steuerbehörde melden](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Lokale Funktion in Business Central](about-localization.md)
