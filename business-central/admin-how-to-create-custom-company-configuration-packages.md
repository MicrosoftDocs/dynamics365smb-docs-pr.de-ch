---
title: 'Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete | Microsoft Docs'
description: "Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können. Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind."
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
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 868972e4d53d858834ba5985a3de3ffa1d4dcc6b
ms.contentlocale: de-ch
ms.lasthandoff: 11/22/2018

---
# <a name="create-custom-company-configuration-packages"></a>Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete
Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können. Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind.  

Im Allgemeinen erstellen Sie ein Konfigurationspaket pro Funktionsbereich, zum Beispiel ein Paket für Ihre Fertigungsfunktionen. Dadurch können Sie nach Bedarf neue Bereiche in einem Mandanten anwenden und einrichten.  

Ein anderer Ansatz wäre die Erstellung eines Pakets, das die Tabellen enthält, die die Einrichtung definieren, etwa wie folgt:  

-   Anlagen Einrichtung  
-   Fibu Einrichtung  
-   Lager Einrichtung  
-   Produktion Einrichtung  
-   Kreditoren und Einkauf Einr.  
-   Marketing & Vertrieb Einr.  
-   Service Einrichtung  
-   Debitoren und Verkauf Einr.  
-   Logistik Einrichtung  
-   Buchungsmatrix Einrichtung  
-   MWST-Buchungsmatrix  
-   Lagerbuchungseinrichtung  

Um eine vollständige Liste von Tabellen-Einrichtungen zu sehen, wählen Sie das Symbol ![Glühlampe, mit der die Funktion Wie möchten Sie weiter verfahren geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") und geben Sie **Einrichtung** ein und wählen dann den zugehörigen Link aus.  

## <a name="to-create-a-custom-company-configuration-package"></a>Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete  
1.  Erstellen Sie in der Liste eine neue [!INCLUDE[d365fin](includes/d365fin_md.md)] ***NICHT MÖGLICHER Link, um für das Erstellen eines neuen Tenants" zu helfen***.   
2.  Erstellen Sie einen neuen Mandanten für die Branchen- oder die Lösungsvorlage. Weitere Informationen zum Erstellen einer Vorlage finden Sie unter [Vorgehensweise: Ein neues Unternehmen  erstellen](admin-how-to-create-a-new-company.md).  
3.  Richten Sie den neuen Mandanten so ein, wie Sie ihn benötigen. Füllen Sie alle erforderlichen Einrichtungstabellen aus.  
4.  Öffnen des neuen Mandanten
5. Öffnen Sie das Fenster **Konfigurationsvorschlag**.  
6.  Fügen Sie die Tabellen hinzu, die Sie zu einem anderen Mandanten auf dem Arbeitsblatt übertragen möchten. Weisen Sie die Arbeitsblattzeilen dem Paket zu.  
7.  Erstellen Sie einen Fragebogen für die am häufigsten verwendeten Einrichtungstabellen.  
8.  Erstellen Sie Konfigurationsvorlagen, um es zu erleichtern, Stammdaten, beispielsweise Debitoren oder Artikel, zu erstellen.  
9.  Exportieren Sie Ihr Paket als eine .rapidstart-Datei.  

## <a name="see-also"></a>Siehe auch  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)

