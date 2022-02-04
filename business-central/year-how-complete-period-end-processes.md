---
title: Optionale Aktivitäten für Abschlussperioden
description: In diesem Thema werden die optionalen Vorgänge und Aktivitäten Abschlussbuchhaltungsperioden in  Business Central dargelegt.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Überblick zu Aufgaben, Buchhaltungsperioden zu schliessen

[!INCLUDE[prod_short](includes/prod_short.md)] zwingt Sie nicht, Perioden zu schliessen, aber es gibt viele Aktivitäten am Periodenende (Monatsende), die Sie ausführen können. Dieses Thema zeigt eine Übersicht von optionalen Vorgängen und Aktivitäten für Perioden, die bereitstehen.  

## <a name="general-ledger"></a>Fibuposten

* Geben Sie systemweite und benutzerspezifische Buchungsperioden an.  

    Dies gibt die Daten an, zwischen denen Buchungen zulässig sind. Je nach Geschäftsanforderungen empfiehlt es sich, die Buchungsdatumsbereiche für Benutzer zu Beginn des Periodenabschlusses einzugrenzen. Weitere Informationen finden Sie unter [Abschliessen von Buchhaltungsperioden](finance-how-specify-posting-periods.md).  
* Führen Sie alle notwendigen Sachpostenregulierungen durch.  
* Aktualisieren und buchen Sie wiederkehrende Erfassungsjournale.  
  <!--* Process Consolidations-->
* Führen Sie ein Kontenschema wie folgt aus:  
  * Öffnen Sie die Seite **Kontenschema** und klicken Sie auf **Drucken**.  

## <a name="sales-and-receivables"></a>Debitoren und Verkauf

* Alle Aufträge, Rechnungen, Gutschriften und Reklamationen werden gebucht.  
* Buchen Sie alle Barzahlungseingangs-Buch.-Blätter.  
* Aktualisieren und buchen Sie wiederkehrende Erfassungsjournale, die sich auf Debitoren und Verkauf beziehen.  
* Stimmen Sie die Debitoren mit der Finanzbuchhaltung ab.  
* Führen Sie die Stapelverarbeitung **Fakturierte Aufträge löschen** aus.  

## <a name="purchases-and-payables"></a>Kreditoren und Einkauf

* Alle Aufträge, Rechnungen, Gutschriften und Reklamationen für Kreditoren werden gebucht.  
* Buchen Sie das Zahlungsausgangs Buch.-Blatt.  
* Aktualisieren und buchen Sie wiederkehrende Buch.-Blätter, die sich auf Kreditoren und Einkäufe beziehen.  
* Führen Sie den Bericht **Kreditor - Saldenrückblick** aus, und stimmen Sie die Kreditoren mit der Finanzbuchhaltung ab.  
* Führen Sie die Stapelverarbeitung **Erledigte fakturierte Bestellungen löschen** aus.  

## <a name="fixed-assets"></a>Anlagevermögen

* Alle Wartungskosten wurden über die Anlagen-Buch.-Blätter oder Rechnungen gebucht.
* Buchen Sie Regulierungen.
* Buchen Sie die Zuschreibung.
* Buchen Sie die Abschreibung.
* Aktualisieren und buchen Sie das Erf.-Journal für wiederkehrende Anlagen

## <a name="intercompany"></a>Intercompany

* Verarbeiten von Intercompanytransaktionen

## <a name="calculate-and-process-sales-tax"></a>Berechnen und erfassen Sie die Salestax.

* Schliessen Sie Steuer-Abrechnungen ab.  

## <a name="see-also"></a>Siehe auch

[Beenden von Jahresabschluss und Perioden](year-close-years-periods.md)  
[Schliessen der Bücher](year-close-books.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]