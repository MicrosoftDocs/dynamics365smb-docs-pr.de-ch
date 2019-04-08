---
title: Einrichten von Prozessen in Financials | Microsoft Docs
description: Informationen zu Aufgaben, Finanzen in Ihrem Unternehmen einzurichten, um Ihrer Buchhaltung, oder Buchhaltungsanforderungen Prüfungen zu entsprechen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 12/19/2018
ms.author: sgroespe
ms.openlocfilehash: 377e7f8eb3cb78adf68e3f4167a215d8f027f972
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "819879"
---
# <a name="setting-up-finance"></a>Finance einrichten
Damit Sie sich rasch zurechtfinden, enthält [!INCLUDE[d365fin](includes/d365fin_md.md)]  Standardkonfigurationen für die meisten Finanzprozesse. Wenn Sie die Konfiguration ändern müssen, um Ihrem Geschäft zu entsprechen, tun Sie es. Sei können vom Rollencenter auf eine unterstützte Einrichtung zugreifen, die Sie beispielsweise dabei unterstützt, Salestax abhängig von Ihrem Standort einzurichten.  

Es gibt jedoch mehrere Elemente, die Sie selber einrichten müssen. Wenn Sie Dimensionen als Grundlage für Business Intelligence verwenden möchten.  

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

| An | Informationen |
| --- | --- |
| Wählen Sie aus, wie Sie Ihre Kreditoren bezahlen. |[Zahlungsformen definieren](finance-payment-methods.md) |
| Buchungsgruppenzuordnungseinheiten nach Debitoren, Kreditoren, Artikel, Ressourcen und Einkaufs- und Verkaufsbelegen mit Fibukonten. |[Buchungsgruppen einrichten](finance-posting-groups.md)|
|Erstellen Sie Kontenschema und definieren hiermit Kontengruppen, um den Inhalt aus Finanzdiagrammen und Berichte, wie die Bilanz- und Erfolgsrechnung-Berichte, zu definieren.|[Bereiten Sie Finanzberichte mit Kontenschema und Kontengruppen vor](bi-how-work-account-schedule.md)|
|Einrichtung einer Toleranz, mit der das System eine Rechnung schliesst, selbst wenn die Zahlung einschliesslich aller Rabatte nicht vollständig den Betrag der Rechnung abdeckt.|[Mit Zahlungstoleranzen und Skontotoleranzen arbeiten](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Einrichten von Finanzzeiträumen |[Ein neues Geschäftsjahres eröffnen](finance-how-open-new-fiscal-year.md) |
| Definieren Sie, wie Sie Dienstleistungssteuerbeträge erstellen, die Sie für Verkäufe an das Finanzamt eingetrieben haben. |[Methoden für die Berechnung und Buchung der Salestax einrichten](finance-setup-vat.md)|
|Vorbereitung für das Bearbeiten nicht vereinnahmter MWST in Verbindung mit Einnahmen- und Ausgabenrechnungs-Methoden.|[Einrichten unrealisierter MWST. für Einnahmen- und Ausgabenrechnung](finance-setup-unrealized-vat.md)|
| Einrichten Ihrer Verkaufs- und Einkaufsfunktionen, um Zahlungen in Fremdwährungen abzuwickeln.|[Anwendung von Kreditorenposten in unterschiedlichen Währungen aktivieren](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definieren Sie eine oder mehrere Währungen, so dass Beträge automatisch in Mandantenwährung sowie in Berichtswährung für jeden Fibuposten und weitere Posten gebucht werden.|[Einrichten einer zusätzlichen Berichtswährung](finance-how-setup-additional-currencies.md)|
|Passen Sie in regelmäßigen Abständen weitere Währungsentsprechungen an, um schwankende Wechselkurse wieder gutzumachen.|[Währungswechselkurse aktualisieren](finance-how-update-currencies.md)|
|Mehrere Zinssätze werden für verschiedene Perioden für gestundete Zahlungen in den Geschäftstransaktionen verwendet.|[Dient zum Einrichten mehrerer Zinssätze.](finance-how-to-set-up-multiple-interest-rates.md)|
|Gegebenenfalls müssen Rechnungsbeträge automatisch beim Erstellen von Rechnungen gerundet werden.|[Einrichten der Rechnungsrundung](finance-set-up-invoice-rounding.md)|
| Fügen Sie dem bestehenden Kontenplan neue Konten hinzu. |[Einrichten des Kontenplans](finance-setup-chart-accounts.md) |
| Einrichten Business Intelligence (BI)- Diagrammen, um Cashflow zu analysieren. |[Aufstellungs-Cashflow-Analyse](finance-setup-cash-flow-analyses.md) |
|Aktivierung der Rechnungstellung für einen Debitoren, der nicht im System eingerichtet ist.|[Bargelddebitoren einrichten](finance-how-to-set-up-cash-customers.md)|
| Einrichtung von Intrastat-Berichten und Übermitteln des Berichts an eine Behörde | [Einrichten und Berichten von Intrastat](finance-how-setup-report-intrastat.md)|
|Konsolidierten Rohbilanzberichts für das Buchhalter Rollen-Center vorbereiten, um eine finanzielle Übersicht in mehreren Mandanten zu erhalten.|[Konsolidieren von Finanzdaten aus mehreren Unternehmen](finance-consolidated-company-reporting.md)|
|Stellen Sie sicher, dass ein Posten eines Fibu Erf.-Journal beim Buchen des Erf.-Journals auf verschiedene Konten verteilt wird, und zwar nach Anzahl, Prozent oder Betrag.|[Verwenden von Umlageschlüsseln in Fibu Buch.-Blättern](ui-how-use-allocation-keys-general-journals.md)|

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Geschäftsdaten aus anderen Finanzsystemen migrieren](across-import-data-configuration-packages.md)  
[Analysieren von Cashflow in Ihren Mandanten](finance-analyze-cash-flow.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
