---
title: So erstellen Sie Erf.-Journal-Eröffnungssalden | Microsoft Docs
description: Business Central enthält mehrere Stapelverarbeitungsaufträge, die bereitgestellt werden, um die Übertragung von vorhandenen Kontosalden auf einen neu konfigurierten Mandanten zu unterstützen. Sie können diese Daten mithilfe von Buch.-Blatt-Buchungen einfach übertragen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8ffb5b8b90d0fdd4f3e1bd90271db8568c05d41e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753981"
---
# <a name="create-journal-opening-balances"></a>So erstellen Sie Erf.-Journal-Eröffnungssalden

[!INCLUDE[prod_short](includes/prod_short.md)] enthält mehrere Stapelverarbeitungsaufträge, die bereitgestellt werden, um die Übertragung von vorhandenen Kontosalden auf einen neu konfigurierten Mandanten zu unterstützen. Sie können diese Daten auf das Debitor Erf.-Journal, das Kreditor Erf.-Journal, das Artikel Erf.-Journal und das Hauptbuch Erf.-Journal übertragen.

Der erste Schritt besteht darin, ein Konfigurationspaket zu erstellen, das die Einrichtungstabellen für alle Erfassungsjournale enthält. Nachfolgend wird davon ausgegangen, dass dieser Schritt abgeschlossen ist. Weitere Informationen finden Sie unter [Unternehmenskonfiguration einrichten](admin-set-up-company-configuration.md). Das Verfahren beschreibt die folgenden Schritte, die das Übernehmen des Pakets, das von einem Partner bereitgestellt wird, enthalten.  

Bevor Sie den Buchungsvorgang starten, prüfen Sie, ob Sie die Verwaltungsrollencenterseite verwenden, da sie den korrekten Kontext für Ihre Konfigurationsarbeit bereitstellt. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>So übernehmen Sie die Posten in einem Erfassungsjournal für einen neuen Mandanten.

1. Konfigurieren Sie einen neuen Mandanten und wenden Sie ein Konfigurationspaket darauf an. Weitere Informationen finden Sie unter [So konfigurieren Sie einen Mandanten mit dem RapidStart-Assistenten](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Der neue Mandant enthält keine Informationen über Erfassungsjournal-Eröffnungssalden.  

2. Öffnen Sie das Konfigurationsarbeitsblatt, und importieren Sie vorhandene Daten zu Debitoren, Kreditoren, Artikeln, Kreditoren und dem Fibukonto. Weitere Informationen finden Sie unter [Gewusst wie: Kundendaten zusammenführen](admin-migrate-customer-data.md).  

    Jetzt haben Sie die Masterdaten eingerichtet. Als Nächstes fügen Sie die Eröffnungssalden hinzu. In den folgenden Schritten wird beschrieben, wie Sie Erfassungsjournalzeilen für Fibukonten erstellen. Gleiches gilt jedoch für die Erstellung von Erfassungsjournalzeilen für Debitoren, Kreditoren und Artikel.  
3. Wählen Sie beispielsweise die Aktion **Erfassungsjournalzeilen erstellen** aus.  
4. Füllen Sie das Inforegister **Optionen** entsprechend aus und legen Sie nach Bedarf Filter fest. Geben Sie beispielsweise im Feld **Erfassungsjournalvorlage** einen Namen ein.  
5. Wählen Sie die Schaltfläche **OK** aus. Die Datensätze stehen jetzt im Erf.-Journal, die Beträge sind jedoch leer.  
6. Exportieren Sie die Erfassungsjournal-Tabelle in Excel und geben Sie die Buchung und die Gegenkontoinformationen aus den Stammdaten manuell ein.
7. Importieren Sie die Tabelleninformationen in den neuen Mandanten und gleichen Sie sie aus. Die Erfassungspositionen sind für die Buchung bereit.  
8. Wählen Sie im Konfigurationsarbeitsblatt die Erf.-Journalzeile, und wählen Sie in der Registerkarte Aktionen in der Gruppe Anzeigen die Option **Datenbank-Daten** aus.  
9. Überprüfen Sie die Informationen und wählen Sie dann die Schaltfläche **Buchen** aus.  
10. Wiederholen Sie die Schritte, um verschiedene Salden zu importieren und zu buchen.  

> [!TIP]
> Sie können dieselben Stapeljobs verwenden, um Eröffnungssalden hinzuzufügen, wenn Sie einen neuen Debitor oder Kreditor registrieren, mit dem Sie zuvor Geschäfte gemacht haben, bei dem Sie jedoch nicht registriert sind [!INCLUDE [prod_short](includes/prod_short.md)]. Suchen Sie einfach nach der entsprechenden Aufgabe und wählen Sie dann den entsprechenden Link.

## <a name="see-also"></a>Siehe auch

[Konfigurationen für neue Mandanten übernehmen](admin-apply-configuration-to-new-companies.md)  
[Mandanten mit RapidStart Services einrichten](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]