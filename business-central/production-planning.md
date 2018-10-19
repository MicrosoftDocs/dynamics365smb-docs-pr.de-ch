---
title: Lieferkettenplanung | Microsoft Docs
description: "Vorbereiten eines ausführlichen ausführbaren Plan und der Montageplan für Verkäufe und Produktionsbedarf."
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 24a2cec78c97d52716c1548f062fa6346bddc5f6
ms.contentlocale: de-ch
ms.lasthandoff: 09/28/2018

---
# <a name="planning"></a>Planung
Die Produktionsschritte, die ausgeführt werden müssen, um das Ausgangsmaterial zu Fertigerzeugnissen zu verarbeiten, müssen – abhängig von Volumen und Art der Produkte – täglich oder wöchentlich geplant werden. [!INCLUDE[d365fin](includes/d365fin_md.md)] verfügt über Features zum Erfüllen des erwarteten und tatsächlichen Bedarfs von Verkauf und Produktion sowie über Verteilungsplanungsfeatures, die die Verwendung von Lagerhaltungsdaten und Umlagerungen zwischen Lagerorten ermöglichen.

> [!NOTE]
> Dieses Thema beschreibt die Planung für Unternehmen, die mit der Fertigung oder Montageverwaltung zu tun haben, wenn die resultierenden Beschaffungsaufträge entweder Produktion, Montage, Umlagerung oder Einkaufsbestellungen sein können. Die Hauptschnittstelle für diese Planungsarbeiten ist das Fenster **Planungsvorschlag**

> [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt auch Beschaffungsplanung für Grosshandelsmandanten, in denen Beschaffungsaufträge und die resultierende Umlagerung nur Einkaufsbestellungen sein können. Die für diese Hauptschnittstelle Planungsarbeiten ist das **Bestellvorschlag** Fenster, die indirekt in diesem Thema beschrieben wird, während die meisten Planungsfunktionalität auf beide Vorschläge gehört.

Bevor Sie Produktionsaufträge planen und ausführen können, müssen Sie die Fertigungskapazitäten konfigurieren, wie Erstellung von Betriebskalendern, Arbeitsplänen, Produktionsstücklisten und Maschinencentren. Weitere Informationen finden Sie unter [Einrichten von Produktion](production-configure-production-processes.md).

Planung kann als die Vorbereitung der erforderlichen Beschaffungsaufträge in den Montage- oder Fertigungsabteilungen zur Erfüllung des Bedarfs angesehen werden. Weitere Informationen finden Sie unter [Montageverwaltung](assembly-assemble-items.md) und [Produktion](production-manage-manufacturing.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.   

|**Bis**|**Siehe**|  
|------------|-------------|  
|Erhalten einer kurzen Einführung, wie das Planungssystem verwendet werden kann, um Nachfrage zu erkennen und zu priorisieren und einen ausgewogenen Beschaffungsplan vorzuschlagen,.|[Info zu Planungsfunktionen](production-about-planning-functionality.md)|
|Erläutert, wie das Planungssystem arbeitet und wie die Algorithmen angepasst werden, um Planungsbedingungen in verschiedenen Umgebungen zu erfüllen.|[Designdetails: Vorratsplanung](design-details-supply-planning.md)|
|Erhalten von Informationen zur Planungslogikabweichung zwischen dem Bedarf an Lagerplätzen gemäss den Einstellungen der Lagerhaltungsdaten und dem Bedarf ohne Lagerortcodes|Siehe [Planung mit/ohne Lagerortcodes](production-planning-with-without-locations.md).|
|Prognostizieren den Fertigungsbedarf, der durch erwartete Verkaufs- und Fertigungskomponenten dargestellt wird.|[Bedarfsplanung erstellen](production-how-to-create-a-forecast.md)|  
|Automatisches exaktes Erstellen von Fertigungsaufträgen auf der Grundlage von Aufträgen, um den exakten Bedarf der Auftragszeile abzudecken|[Fertigungsaufträge aus Verkaufsaufträgen zu erstellen:](production-how-to-create-production-orders-from-sales-orders.md)|
|Direktes Erstellen eines Projektfertigungsauftrags auf der Grundlage eines mehrzeiligen Auftrags, bei dem es sich um Fertigungsprojekt handelt|[Projektaufträge planen](production-how-to-plan-project-orders.md)|
|Manuelles Planen für Verkaufs- oder Fertigungsbedarf pro einzelner Operationsplanebene mithilfe des Fensters **Auftragsplanung**|[Planung der Bestellung eines neuen Bedarfs von Auftrag](production-how-to-plan-for-new-demand.md)|
|Verwenden Sie das Fenster **Planungsvorschlag**, um die Felder Prod.-Programmplanung und Nettobedarfsoptionen auszuführen, einen oder ausführlichen Beschaffungsplans auf hoher Ebene in allen Artikelebenen automatisch zu erstellen.|[Führen Sie eine vollständige Planung, Prod.-Programmplanung oder Nettobedarf aus](production-how-to-run-mps-and-mrp.md)|
|Ausführen des Bestellvorschlags zum automatischen Erstellen eines ausführlichen Beschaffungsplans, um den Bedarf für Artikel zu decken, die ausschliesslich per Einkauf oder Umlagerung beschafft werden|**Bestellvorsch.-Namen**|  
|Initiieren oder Aktualisieren eines Fertigungsauftrags in Form grobterminierter Arbeitsgänge im Produktionsplan|[Neugestaltungs- oder direkt Aktualisierung von Fertigungsaufträgen](production-how-to-replan-refresh-production-orders.md)|
|Berechnen Sie Arbeits- oder Arbeitsplatzkalender aufgrund von Planungsänderungen.|"Berechnen eines Arbeitsplatzgruppenkalender-Abschnitt in [Richten Sie Betriebskalender ein](production-how-to-create-work-center-calendars.md)|
|Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist|[Nachverfolgen von Beziehungen zwischen Bedarf und Vorrat.](production-how-track-demand-supply.md)|
|Anzeigen des voraussichtlich verfügbaren Lagerbestands eines Artikels in verschiedenen Ansichten und Anzeigen des beeinflussenden Bruttobedarfs sowie der beeinflussenden geplanten Auftragseingänge und anderer Ereignisse im Laufe der Zeit|[Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)|  
|Wählen Sie Planungsaktivitäten wie ändern oder hinzufügen von Planungsvorschlagszeilen, in einer grafischen Ansicht des Beschaffungsplans aus.|[Ändern von Planungsvorschlägen in einer grafischen Ansicht](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a>Siehe auch
[Produktion einrichten](production-configure-production-processes.md)  
[Bearbeitungen](production-manage-manufacturing.md)    
[Lagerbesttand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

