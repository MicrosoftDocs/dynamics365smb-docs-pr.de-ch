---
title: Finanzielle Prozesse festlegen
description: Informieren Sie sich über die Aufgaben, die erforderlich sind, um die Finanzen in Ihrem Unternehmen so festzulegen, dass sie allen Anforderungen der Buchhaltung, der Rechnungsprüfung oder der Buchführung entsprechen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: 87d5ede3d1cbd94178a614cd7929da9c8e43600a
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532202"
---
# <a name="setting-up-finance"></a>Finance einrichten
Bevor Sie mit der Geschäftstätigkeit beginnen können, müssen Sie Regeln und Standardeinstellungen für die Verwaltung der Finanzprozesse für dieses Unternehmen festlegen. Richten Sie zunächst den Kern der Buchhaltungsdatensätze des Mandanten ein, den Kontenplan. Anschliessend werden Buchungsgruppen eingerichtet, um das Zuordnen von standardmässigen Fibukontobuchungskonten zu Debitoren, Kreditoren und Artikeln effizienter zu gestalten.

Einige Finanzeinrichtungen können automatisch mit Hilfe der Anleitung für die unterstützte Einrichtung durchgeführt werden, andere müssen manuell durchgeführt werden. Weitere Informationen finden Sie unter [Vorbereitungen für das Ausführen von Geschäften](ui-get-ready-business.md). Auf der Seite **Fibuposten-Einrichtung** geben Sie an, wie verschiedene finanzbuchhalterische Sachverhalte in Ihrem Unternehmen gehandhabt werden sollen. Zum Beispiel verwenden Sie diese Seite, um Einzelheiten zur Rechnungsrundung, zum Währungscode, zur Mandantenwährung, zu Adressformaten und zur Berichtswährung zu hinterlegen. Weitere Informationen finden Sie unter [Die Fibuposten und der Kontenplan verstehen](finance-general-ledger.md).  

Sie können Dimensionen verwenden, um jeder Transaktion unterschiedliche Arten von Informationen hinzuzufügen. Sie können die grundlegenden Dimensionen Ihres Mandanten festlegen, wie *Projekte* und *Abteilungen*. Später können Sie weitere Dimensionen hinzufügen, wenn Sie sie benötigen, und Sie können temporäre Dimensionen für die Verwendung für einen begrenzten Zeitraum einrichten, beispielsweise in Verbindung mit einer Verkaufskampagne. Weitere Informationen finden Sie unter [Arbeiten mit Dimensionen](finance-dimensions.md)

Zwar müssen viele der Einrichtungsaufgaben ausgeführt werden, bevor Sie mit der Erfassung von Finanztransaktionen beginnen können, die meisten Einstellungen können jedoch zu einem späteren Zeitpunkt geändert werden. So müssen beispielsweise Intercompanybuchungen und Konsolidierungen nur eingerichtet werden, wenn Sie mit mehreren Mandanten arbeiten. Einige Einrichtungsaufgaben, wie das Angeben der Zeitraums, in dem das Buchen erlaubt ist, müssen möglicherweise in regelmässigen Abständen wiederholt werden.  

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert

| Bis | Siehe |
| --- | --- |
|Anzeigen oder Bearbeiten der Liste der Fibukonten, auf die alle Fibuposten gebucht werden|[Einrichten oder Ändern des Kontenplans](finance-setup-chart-accounts.md)|
| Geben Sie an, wie Sie von Kunden bezahlt werden möchten und wie Sie Ihre Lieferanten bezahlen möchten. |[Einrichten von Zahlungsformen](finance-payment-methods.md) |
| Definieren Sie Zahlungsbedingungen zum Verwalten von Fälligkeitsdaten sowie zum Berechnen von möglichem Skonto.|[Zahlungsbedingungen einrichten](finance-payment-terms.md) |
| Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Fibukonten. |[Buchungsgruppen einrichten](finance-posting-groups.md)|
|Erstellen Sie Kontenschema und definieren hiermit Kontengruppen, um den Inhalt aus Finanzdiagrammen und Berichte, wie die Bilanz- und Erfolgsrechnung-Berichte, zu definieren.|[Bereiten Sie Finanzberichte mit Kontenschema und Kontengruppen vor](bi-how-work-account-schedule.md)|
|Einrichtung einer Toleranz, mit der das System eine Rechnung schliesst, selbst wenn die Zahlung einschliesslich aller Rabatte nicht vollständig den Betrag der Rechnung abdeckt.|[Arbeiten mit Zahlungstoleranzen und Skontotoleranzen](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Einrichten von Finanzzeiträumen |[Arbeiten mit Buchhaltungsperioden und Geschäftsjahren](finance-accounting-periods-and-fiscal-years.md) |
|Richten Sie Erinnerungsbedingungen ein, um überfällige Zahlungen einzutreiben.|[Einrichten von Mahnmethoden, Bestimmungen und Mahntext](finance-setup-reminders.md)|
| Definieren Sie, wie Sie Dienstleistungssteuerbeträge erstellen, die Sie für Verkäufe an das Finanzamt eingetrieben haben. |[Mehrwertsteuer (MWST) einrichten](finance-setup-vat.md)|
|Vorbereitung für das Bearbeiten nicht vereinnahmter MWST in Verbindung mit Einnahmen- und Ausgabenrechnungs-Methoden.|[Einrichten unrealisierter MWST. für Einnahmen- und Ausgabenrechnung](finance-setup-unrealized-vat.md)|
|Definieren Sie die Fremdwährungen, mit denen Sie handeln oder Transaktionen melden.|[Einrichten von Währungen](finance-set-up-currencies.md)|
| Einrichten Ihrer Verkaufs- und Einkaufsfunktionen, um Zahlungen in Fremdwährungen abzuwickeln.|[Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definieren Sie eine oder mehrere Währungen, so dass Beträge automatisch in Mandantenwährung sowie in Berichtswährung für jeden Fibuposten und weitere Posten gebucht werden.|[Einrichten einer zusätzlichen Berichtswährung](finance-how-setup-additional-currencies.md)|
|Passen Sie in regelmässigen Abständen weitere Währungsentsprechungen an, um schwankende Wechselkurse wieder gutzumachen.|[Währungswechselkurse aktualisieren](finance-how-update-currencies.md)|
|Mehrere Zinssätze werden für verschiedene Perioden für gestundete Zahlungen in den Geschäftstransaktionen verwendet.|[Dient zum Einrichten mehrerer Zinssätze](finance-how-to-set-up-multiple-interest-rates.md)|
|Gegebenenfalls müssen Rechnungsbeträge automatisch beim Erstellen von Rechnungen gerundet werden.|[Einrichten der Rechnungsrundung](finance-set-up-invoice-rounding.md)|
| Fügen Sie dem bestehenden Kontenplan neue Konten hinzu. |[Einrichten des Kontenplans](finance-setup-chart-accounts.md) |
| Einrichten Business Intelligence (BI)- Diagrammen, um Cashflow zu analysieren. |[Aufstellungs-Cashflow-Analyse](finance-setup-cash-flow-analyses.md) |
|Aktivierung der Rechnungstellung für einen Debitoren, der nicht im System eingerichtet ist.|[Bargelddebitoren einrichten](finance-how-to-set-up-cash-customers.md)|
| Einrichtung von Intrastat-Berichten und Übermitteln des Berichts an eine Behörde | [Einrichten und Berichten von Intrastat](finance-how-setup-report-intrastat.md)|
|Stellen Sie sicher, dass ein Posten eines Fibu Erf.-Journal beim Buchen des Erf.-Journals auf verschiedene Konten verteilt wird, und zwar nach Anzahl, Prozent oder Betrag.|[Verwenden von Umlageschlüsseln in Fibu Erf.-Journals](ui-how-use-allocation-keys-general-journals.md)|
|Einrichten von Buchungsspurcodes und Ursachencodes, mit denen Sie Audit-Trails verfolgen können|[Buchungsspurcodes und Ursachencodes für Audit Trails einrichten](finance-setup-trail-codes.md)|
|Geben Sie Standardberichte an, die für verschiedene Dokumenttypen verwendet werden sollen.|[Berichtsauswahl in Business Central](across-report-selections.md)|

> [!TIP]
> Abhängig von Ihrem geografischen Standort können einige Seiten Felder enthalten, die in den hier aufgeführten Artikeln nicht beschrieben sind, da sie für lokale Funktionen oder Anpassungen gelten. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)  
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Analysieren von Cashflow in Ihren Mandanten](finance-analyze-cash-flow.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
