---
title: Bankkonten abstimmen und Zahlungen zuweisen
description: 'Zeigt Aufgaben, um Ihre Bank, Verkaufs- und Kreditorensammelkonte, Beitragszahlungseingänge oder Kosten auszugleichen und gleicht Zahlungen automatisch aus.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1291, 1293, 1294'
ms.date: 07/25/2024
ms.service: dynamics-365-business-central
---

# <a name="apply-payments-automatically-and-reconciling-bank-accounts"></a>Zahlungen automatisch ausführen und Bankkonten abgleichen
Sie müssen Ihre Bank, Debitoren- und Kreditorensammelkonten routinemässig abstimmen, indem Sie die Zahlungen, die in Ihrem Bankkonto aufgezeichnet sind, mit ihren entsprechenden offenen (unbezahlten) Rechnungen und Gutschriften oder anderen offenen Posten im [!INCLUDE[prod_short](includes/prod_short.md)]ausgleichen.  

Diese Aufgabe können Sie dann auf der Seite **Zahlungs-Abstimmungs-Erf.-Journal** ausführen, z. B., indem Sie eine Bankkontoauszugsdatei oder einen Feed importieren, um die Zahlungen schnell zu erfassen. Die Zahlungen werden angewendet, um Debitoren- oder Kreditorenposten zu öffnen, indem passender Zahlungstext und Zahlungsinformationen verknüpft werden. Sie können auch automatische Anwendungen überprüfen und ändern, bevor Sie das Erfassungsjournal buchen. Sie können die offenen Bankkontoposten für ausgeglichenen Posten schließen, wenn Sie das Erfassungsjournal buchen. Das bedeutet, dass das Bankkonto automatisch abgestimmt wird, wenn alle Zahlungen ausgeglichen werden.

Auf der Seite **Zahlungsausgleichsvorschriften** können Sie priorisierte Regeln einrichten, die steuern, wie der Zahlungstext automatisch mit den Posteninformationen abgeglichen wird.

Sie können auch, Bankkonten abstimmen ohne Zahlungen gleichzeitig anzuwenden. Sie führen diese Arbeiten auf der Seite **Bankkonto Abstimmen** aus. Weitere Informationen finden Sie unter [Abstimmen von Bankkonten](bank-how-reconcile-bank-accounts-separately.md).

Um den Import von Bankkontoauszügen als Bankfeed zu aktivieren, müssen Sie den Bank-Feed-Service Envestnet Yodlee anlegen und aktivieren und dann Ihr Bankkonto mit den entsprechenden Online Bankkonten verbinden. Weitere Informationen finden Sie unter [Einrichten des Envestnet Yodlee Bank-Feed-Dienstes](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Sie können Kontoauszugsdateien auch im durch Kommas oder Semikolons getrennten Format (.CSV) importieren. Verwenden Sie die unterstützte Einrichtung **Richten Sie ein Bankauszugs-Dateiimportformat ein** zum Definieren von Importformaten für Kontoauszüge und Anhängen des Formats an ein Bankkonto. Sie können diese Formate dann verwenden, wenn Sie Kontoauszüge in die Seite **Bankkontenabgleich** importieren.

Alternativ können Sie mit der AMC Banking 365 Fundamentals-Erweiterung eine Kontoauszugsdatei von jedem Format in einen Datenstrom konvertieren, den Sie in [!INCLUDE[prod_short](includes/prod_short.md)] importieren können. Weitere Informationen finden Sie unter [Verwenden der AMC Banking 365-Grundlagenerweiterung](ui-extensions-amc-banking.md).  

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben..  

| Bis | Informationen |
| --- | --- |
| Zahlungen verwenden, um Debitoren- oder Kreditorenposten zu öffnen, indem Sie einen Bankkontoauszug importieren und das Bankkonto anschliessend abstimmen, nachdem Sie alle Zahlungen ausgeglichen haben. |[Zahlungen mit automatischem Ausgleich abstimmen](receivables-how-reconcile-payments-auto-application.md) |
| Gleichen Sie manuell Zahlungen aus, indem Sie detaillierte Informationen über zugeordnete Daten und Vorschläge für offene Kandidatenposten anzeigen, mit denen Zahlungen ausgeglichen werden sollen. |[Überprüfen oder Ausgleichen von Zahlungen nach automatischer Anwendung](receivables-how-review-apply-payments-auto-application.md) |
| Lösen Sie Zahlungen auf, die nicht automatisch in die entsprechenden offenen Posten übernommen werden können. Beispielsweise weil die Beträge abweichen oder weil ein verwandter Posten vorhanden. |[Zahlungen abstimmen, die nicht automatisch ausgeglichen werden können](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Verknüpfen Sie Text auf Zahlungen mit bestimmten Debitoren-, Kreditoren- oder Fibukonten, um solche wiederkehrenden Zahlungseingänge oder Ausgaben immer auf diesen Konten als Zahlungen ohne zugehörige Belege zu buchen, wenn keine entsprechenden Belege vorhanden sind. |[Zuordnen von Text auf sich wiederholenden Zahlungen an Konten für automatische Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Richten Sie die Regeln ein, um zu steuern, wie Zahlungen/Banktransaktionen automatisch mit ihren entsprechenden offenen Fibuposten ausgeglichen werden, wenn Sie die Funktion **Automatisch anwenden** auf der Seite **Zahlungsabstimmungserf.-Journal** verwenden.|[Regeln für die automatische Anwendung von Zahlungen einrichten](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-also"></a>Siehe auch
[Bankkonten abstimmen](bank-how-reconcile-bank-accounts-separately.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
