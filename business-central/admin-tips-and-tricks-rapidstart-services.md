---
title: Tipps und Tricks – RapidStart Services | Microsoft Docs
description: Wenn Sie Unternehmen mit RapidStart Services konfigurieren, gibt es einige Tipps und Tricks, die Sie für eine reibungslose Implementierung nutzen können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e9506697eacfb4bd411266078e4245e59a11353
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922431"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Tipps und Tricks: RapidStart Services

Wenn Sie Unternehmen mit RapidStart Services konfigurieren, gibt es einige Tipps und Tricks, die Sie für eine reibungslose Implementierung nutzen können.  

## <a name="take-advantage-of-configuration-templates"></a>Konfigurationsvorlagen nutzen

Mit Konfigurationsvorlagen können Sie Ihren Implementierungsprozess optimieren. Sie können damit ähnliche Debitoren in Segmente einbinden und dann ein Implementierungsprotokoll entwickeln, das alle Debitoren in einem Segment in ähnlicher Weise behandelt. Auf diese Art können Sie bei jedem Segment eine bestimmte Vorkonfiguration anwenden und mit einer schnelle Implementierung fortfahren.  

## <a name="configuration-questionnaires"></a>Konfigurationsfragebögen

Um das Ausfüllen eines Konfigurationsfragebogens zu unterstützen, erwägen Sie, Standardantworten zu definieren, um auf bewährte Methoden hinzuweisen.  

## <a name="batch-creation-of-journal-lines"></a>Stapelerstellung von Erfassungsjournalzeilen

Es wird empfohlen, die Datenmigrationswerkzeuge für die Migration von Blatteinträgen zu verwenden. Bei der Erstellung von Erfassungsjournalzeilen mit der Stapelverarbeitung steht andernfalls nur ein begrenzter Bereich zur Verfügung, und es werden nur Verzugsfelder in einem Erfassungsjournal generiert. Der Rest des Erfassungsjournals muss anschliessend manuell ausgefüllt werden werden.  

## <a name="migrating-transactions"></a>Migrierung von Transaktionen

Es wird empfohlen, Eröffnungssalden in der folgenden Reihenfolge in mehreren Schritten zu migrieren. <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. Migrieren Sie die Eröffnungssalden des Fibukontos, ohne die untergeordneten Konten des Fibukontos zu verwenden. Verwenden Sie bestimmte Ausgleichskonten für Eröffnungssalden, wobei pro untergeordnetes Sachkonto eines eingerichtet werden sollte. Richten Sie für direkte Buchungen Ausgleichskonten ein.  
2. Migrieren Sie offene Debitorenposten.  <!--work on these-->
3. Migrieren Sie offene Lagerposten.  
4. Migrieren Sie offene Anlagenposten.  

## <a name="make-each-package-manageable"></a>Machen Sie jedes Paket überschaubar

Wenn Sie Konfigurationspakete zum Migrieren von Daten verwenden, teilen Sie die Daten zur Erleichterung der Portabilität in separate Pakete auf. Wenn Sie beispielsweise die Posten von 20 Jahren migrieren möchten, kann der Import viele Stunden und Tage dauern. Teilen Sie die Daten stattdessen auf, damit die einzelnen Pakete überschaubarer werden. Derzeit gibt es keine festen Regel, welche Paketgrösse am besten geeignet ist. Wenn Sie jedoch Probleme beim Importieren oder Exportieren eines Pakets feststellen, versuchen Sie es erneut mit einem kleineren Paket und warten Sie ab, ob dies hilfreich ist.  

## <a name="see-also"></a>Siehe auch

[Mandanten mit RapidStart Services einrichten](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]