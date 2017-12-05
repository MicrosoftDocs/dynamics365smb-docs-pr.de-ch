---
title: QuickBooks-Migrations-Erweiterung verwenden | Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Debitoren, Kreditoren, Artikel und Konten aus QuickBooks-Online auf Dynamics 365 zu migrieren
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 05/24/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: e73db91a37fd5aee249de032d231df2c5e36b4ba
ms.contentlocale: de-ch
ms.lasthandoff: 11/10/2017

---

# <a name="the-quickbooks-online-data-migration-extension-for-dynamics-365-business-edition"></a>Die QuickBooks-Online-Datenmigrations-Erweiterung für Dynamics 365 Business edition
Diese Erweiterung ist im unterstützten Einrichtungshandbuch **Datenmigration** enthalten, um Ihnen zu helfen, wichtige Geschäftsdaten von QuickBooks in Online zu [!INCLUDE[d365fin](includes/d365fin_md.md)]migrieren. Dies ist beispielsweise dann nützlich, wenn Ihr Unternehmen wächst und Sie sich entschieden haben, Ihre Geschäftsführungs-App zu aktualisieren, indem Sie mit [!INCLUDE[d365fin](includes/d365fin_md.md)]  verwenden.

## <a name="what-data-can-i-import-from-quickbooks-online"></a>Welche Daten kann ich von QuickBooks online importieren?
Sie können die folgenden Daten aus QuickBooks online importieren [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

* Debitoren
* Kreditoren
* Arti&kel
* Kontenplan
* Saldovortragtransaktion im Fibuposten
* Verfügbare Mengen für Lagerartikel
* Offene Belege für Debitoren und Kreditoren, wie beispielsweise Rechnungen, Gutschriften und Zahlungen

Es migrieren nur Gesamtbeträge auf Einkaufs- und Verkaufsbelegen. Wir aktualisieren keine teilweise bezahlten Beträge. Wenn ein Debitor 300 von insgesamt 500 Dollar einer Verkaufsrechnung bezahlt hat, migrieren wir die vollständigen 500. Wenn Sie Teilzahlungen erhalten, müssen Sie diese manuell aktualisieren, entweder, vor oder nach dem Sie Daten migrieren. Es ist empfehlenswert, ausstehende Transaktionen anzuwenden, bevor Sie migrieren, das ist einfacher danach.

> [!NOTE]  
>   Wir migrieren keine Einkaufsbestellungen oder Verkaufsaufträge.

## <a name="before-you-start"></a>Bevor Sie beginnen
Ein wichtiger Teil des Migrationsvorgangs ist es, Konten anzugeben, um Transaktionen zu migrieren. Es ist empfehlenswert, diese Zuordnung zu planen, bevor Sie Daten migrieren. Beispielsweise die Konten, die Sie für Transaktionen buchen:  

* Der Verkauf von Artikeln oder Services an einen Kunden.
* Der Kauf von Waren oder Dienste von einem Kreditor.  
* Änderungen im Fibuposten.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] erfordert, dass Sachkonten die Kontonummern haben, die ihm zugeordnet werden. Überprüfen Sie, ob Sie Kontonummern Ihren Konten in QuickBooks online zugeordnet werden.

Wenn Transaktionen in QuickBooks online Steuerbeträge haben, müssen Sie eine MwSt einrichten für Ihre Steuerzuständigkeiten in, [!INCLUDE[d365fin](includes/d365fin_md.md)] bevor Sie Buchungen durchführen können.

## <a name="how-do-i-start-using-the-extension"></a>Wie beginne ich, die Erweiterung zu nutzen?
Erste Schritte sind einfach. Sie müssen nur das unterstütze Einrichtungshandbuch **Datenmigration** ausführen. So geht es:

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "") Symbol **Unterstützte Einrichtung** und geben **Geschäftsdaten migrieren** ein.
2. Befolgen Sie die Anweisungen für jeden Schritt im unterstützten Anleitungshandbuch.

## <a name="what-do-i-do-after-i-migrate-data"></a>Was tue ich, nachdem ich Daten migriert habe?
Nachdem Sie Daten migriert haben, haben die Transaktionen den Status **Nicht gebucht**, sodass Sie sie überprüfen und Korrekturen vornehmen können. Um die Transaktionen zu überprüfen, wechseln Sie zur Seite in der Sie normalerweise suchen müssen. Beispielsweise um nicht gebuchten Verkaufsrechnungen zu überprüfen, gehen Sie zu der Seite **Verkaufsrechnungen**. Um Zahlungsausgangs Buch.-Blätter zu überprüfen, wechseln Sie zur Seite **Zlg.-Ausg. Buch.-Blätter**.   

Es gibt mehrere Dinge, die Sie durchführen sollten:

* Wenn die Transaktionen in QuickBooks online Markup oder Rabattbeträge aufweisen, müssen Sie die Beträge zu den verwandten Transaktionen manuell hinzufügen, [!INCLUDE[d365fin](includes/d365fin_md.md)] bevor Sie diese buchen.
* Wenn Sie MWST verwenden, können Sie eine Geschäftsbuchungsgruppe und eine Produktbuchungsgruppe "Buchungsmatrix Einrichtung" hinzufügen, sodass Sie MWST-Beträge buchen können.
* Prüfen Sie die Startkapitale für Konten im Fibuposten. QuickBooks online speichert nicht den aktuellen Saldo für alle Konten, daher müssen Sie möglicherweise Startkapitale korrigieren.

## <a name="see-also"></a>Siehe auch
[Geschäftsdaten aus anderen Finanzsystemen migrieren](upload-data.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzenb](ui-extensions.md)  

