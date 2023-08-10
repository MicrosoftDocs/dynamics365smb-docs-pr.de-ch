---
title: 'Gewusst wie: Drucken von ESR-Rechnungen [CH]'
description: 'In diesem Thema wird erläutert, wie Sie Zahlungsscheinrechnungen und -gutschriften für einen Einzahlungsschein mit Referenznummer (ESR) drucken können:'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '3010531, 3010532'
ms.date: 06/21/2021
ms.author: edupont
---
# <a name="print-esr-invoices-in-the-swiss-version"></a>ESR-Rechnungen drucken in der Schweizer Version

Zum Drucken von Einzahlungsscheinen mit Referenznummer (ESR) stehen folgende Methoden zur Auswahl:  

- Als Teil der Verkaufsrechnung ESR.  
- Als separaten Beleg, dem ESR-Coupon.  

Der Bericht "Verkauf ESR Rechnung" entspricht der Verkaufsrechnung mit beigefügtem zusätzlichem ESR-Abschnitt. Indem Sie den Verkauf ESR-Couponsbericht verwenden, können Sie den blauen Einzahlungsbeleg drucken.  

> [!NOTE]  
> Sie müssen bei der Installation des ESR-Zahlungsmoduls einen Drucker und Einstellungen auswählen, damit der Einzahlungsbeleg korrekt gedruckt wird. Weitere Informationen finden Sie unter Druckerauswahl – Tabelle.  

Im folgenden Verfahren wird das Drucken von ESR-Verkaufsrechnungen beschrieben, dieselben Schritte gelten jedoch auch für ESR-Abschnitte.  

## <a name="to-print-esr-invoices"></a>So drucken Sie ESR-Rechnungen

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../media/ui-search/search_small.png "Tell me-Funktion") Geben Sie **ESR Rechnung** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie im Stapelverarbeitungsauftrag **Verkauf ESR Rechnung** die Felder auf dem Inforegister **Optionen** wie in der folgenden Tabelle beschrieben aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Anzahl Kopien**|Geben Sie die gewünschte Anzahl der Berichtskopien ein.|  
    |**ESR-Bank**|Wählen Sie die ESR-Bankleitzahl aus, die in dem Bericht gedruckt werden soll.<br /><br /> Wenn der Wert in diesem Feld \<Blank\> und der ESR-Zahlungsformcode nicht auf der Seite **ESR-Einrichtung** definiert ist, wird die ESR-Hauptbank, die auf der Seite **ESR-Einrichtung** ausgewählt wird, gedruckt.|  
    |**Aktivität protokollieren**|Gibt an, ob die Aktivitäten, die Sie mit Ihren Kontakten haben, protokolliert werden.|  
    |**ESR-System**|Wählen Sie das ESR-System aus, über das Sie neue ESR-Coupons an Kunden schicken können. Wählen Sie **Gemäss ESR-Bank**, um das ESR-System der im Feld **ESR-Bank** angegebenen Bank zu verwenden.|  

3. Wählen Sie die Schaltfläche **Drucken** aus, um den Bericht zu drucken, oder die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.  

Sie können den Bericht "Verkauf ESR Rechnung" oder "Verkauf ESR Abschnitt" auch erneut drucken.  

## <a name="see-also"></a>Siehe auch
 [Elektronische Zahlungen mit ESR (Schweiz)](swiss-electronic-payments-using-esr.md)   
 [Importieren von ESR-Zahlungen](how-to-import-esr-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
