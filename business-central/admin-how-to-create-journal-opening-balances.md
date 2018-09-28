---
title: "So erstellen Sie Erf.-Journal-Eröffnungssalden | Microsoft Docs"
description: "Business Central enthält mehrere Stapelverarbeitungsaufträge, die bereitgestellt werden, um die Übertragung von vorhandenen Kontosalden auf einen neu konfigurierten Mandanten zu unterstützen. Sie können diese Daten mithilfe von Buch.-Blatt-Buchungen einfach übertragen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fc8e8f34220643b7cd3fd357aea3807641cee911
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a>So erstellen Sie Erf.-Journal-Eröffnungssalden
[!INCLUDE[d365fin](includes/d365fin_md.md)] enthält mehrere Stapelverarbeitungsaufträge, die bereitgestellt werden, um die Übertragung von vorhandenen Kontosalden auf einen neu konfigurierten Mandanten zu unterstützen. Sie können diese Daten auf das Debitor Erf.-Journal, das Kreditor Erf.-Journal, das Artikel Erf.-Journal und das Hauptbuch Erf.-Journal übertragen.

Der erste Schritt besteht darin, ein Konfigurationspaket zu erstellen, das die Einrichtungstabellen für alle Erfassungsjournale enthält. Nachfolgend wird davon ausgegangen, dass dieser Schritt abgeschlossen ist. Weitere Informationen finden Sie unter [Unternehmenskonfiguration einrichten](admin-set-up-company-configuration.md). Das Verfahren beschreibt die folgenden Schritte, die das Übernehmen des Pakets, das von einem Partner bereitgestellt wird, enthalten.  

Bevor Sie den Buchungsvorgang starten, prüfen Sie, ob Sie in der RapidStart Service-Implementierungs-Rollencenterseite sind, da sie den korrekten Kontext für Ihre Konfigurationsarbeit bereitstellt. Weitere Informationen finden Sie unter [Ändern von Grundeinstellungen](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>So übernehmen Sie die Posten in einem Erfassungsjournal für einen neuen Mandanten.  
1. Konfigurieren Sie einen neuen Mandanten und wenden Sie ein Konfigurationspaket darauf an. Weitere Informationen finden Sie unter [Vorgehensweise: Konfigurieren Sie einen Mandanten mit dem RapidStart-Assistenten](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Der neue Mandant enthält keine Informationen über Erfassungsjournal-Eröffnungssalden.  

2. Öffnen Sie das Konfigurationsarbeitsblatt, und importieren Sie vorhandene Daten zu Debitoren, Kreditoren, Artikeln, Kreditoren und dem Fibukonto. Weitere Informationen finden Sie unter [Gewusst wie: Kundendaten zusammenführen](admin-migrate-customer-data.md).  
3. Wählen Sie die Aktion **Erfassungsjournalzeilen erstellen** aus.  
4. Füllen Sie das Inforegister **Optionen** entsprechend aus und legen Sie nach Bedarf Filter fest. Geben Sie beispielsweise im Feld **Erfassungsjournalvorlage** einen Namen ein.  
5. Wählen Sie die Schaltfläche **OK** aus. Die Datensätze stehen jetzt im Erf.-Journal, die Beträge sind jedoch leer.  
6. Exportieren Sie die Erfassungsjournal-Tabelle in Excel und geben Sie die Buchung und die Gegenkontoinformationen aus den Stammdaten manuell ein.
7. Importieren Sie die Tabelleninformationen in den neuen Mandanten und gleichen Sie sie aus. Die Erfassungspositionen sind für die Buchung bereit.  
8. Wählen Sie im Konfigurationsarbeitsblatt die Erf.-Journalzeile, und wählen Sie in der Registerkarte Aktionen in der Gruppe Anzeigen die Option **Datenbank-Daten** aus.  
9. Überprüfen Sie die Informationen und wählen Sie dann die Schaltfläche **Buchen** aus.  
10. Wiederholen Sie die Schritte, um verschiedene Salden zu importieren und zu buchen.  

## <a name="see-also"></a>Siehe auch  
[Übernehmen von Konfiguration in neue Mandanten](admin-apply-configuration-to-new-companies.md)  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)

