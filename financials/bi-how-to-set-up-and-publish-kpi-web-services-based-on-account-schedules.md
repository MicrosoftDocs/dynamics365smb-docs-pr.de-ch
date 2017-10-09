---
title: "Vorgehensweise: Einrichten und Veröffentlichen von KPI-Webdiensten auf der Basis von Kontenschema | Microsoft Docs"
description: Im Fenster **Kontoplan KPI Web-Service einrichten** richten Sie ein, wie die Kontenschema-KPI-Daten angezeigt werden, und auf welchen spezifischen Kontenschema die KPIs basieren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f91a9813b07b0868043a4a2a3ed0b3f838536
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Vorgehensweise: Einrichten und Veröffentlichen von KPI-Webdienste auf der Basis von Kontenschema
Im Fenster **Kontoplan KPI Web-Service einrichten**  richten Sie ein, wie die Kontenschema-KPI-Daten angezeigt werden, und auf welchen spezifischen Kontenschema die KPIs basieren. Wenn Sie die Schaltfläche **Webdienst veröffentlichen** wählen, werden die angegebenen Kontenschema-KPI-Daten der Liste der veröffentlichten Webdienste im Fenster **Web-Dienste** hinzugefügt.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>So richten Sie einen KPI-Webdienst ein und veröffentlichen ihn, der auf Kontenschemata basiert  

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Kontensalden KPI Webservice einrichten** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Füllen Sie im Inforegister **Allgemein** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Anfang Geplante Werte**|Geben Sie an, zu welchem Zeitpunkt prognostizierte Werte in der Grafik des Kontenschema-KPIs angezeigt werden.<br /><br /> Die prognostizierten Werte werden aus dem Fibupostenbudget abgerufen, das Sie im Feld **Sachkostenbudgetname** auswählen. **Hinweis:**Um KPIs zu erhalten, die die prognostizierten Zahlen nach einem bestimmten Datum und die tatsächlichen Zahlen vor dem Datum anzeigen, können Sie das Feld **Buchungen zulassen ab** im Fenster **Fibukonto einrichten** ändern. Weitere Informationen finden Sie unter Einrichten von Gruppenbuchungen |  
    |**Finanzbudgetname**|Geben Sie den Namen des Finanzbudgetpostens an, das prognostizierte Werte für den Webdienst des Kontenschema-KPIs bereitstellt.|  
    |**Periode**|Geben Sie die Periode an, auf dem der Kontenschema-KPI-Webservice basiert.|  
    |**Anzeigen nach**|Geben Sie an, in welchem Zeitintervall der Kontenschema KPI gezeigt wird.|  
    |**Webdienstname**|Geben Sie den Namen des Kontenschema-KPIs an.<br /><br /> Dieser Name wird im Feld **Servicename** im Fenster **Webservice** angezeigt.|  

    Fahren Sie fort, ein oder mehrere Kontenschema anzugeben, die Sie als KPI-Webdienst gemäss der Einrichtung veröffentlichen möchten, die Sie in der vorhergegangenen Tabelle vorgenommen haben.  

3.  Füllen Sie im Inforegister **Kontenschema** die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Kontenschemaname**|Geben Sie das Kontenschema, auf dem der Kontenschema-KPI-Webservice basiert.|  
    |**Kontenschemabeschreibung**|Geben Sie die Beschreibung des Kontenschemas an, auf dem der KPI-Webservice basiert.|  

4.  Wiederholen Sie Schritt 3 für alle Kontenschema, auf denen der Webdienst des Kontenschema-KPI basieren soll.  
5.  Um das ausgewählte Kontenschema einzusehen oder zu bearbeiten, wählen Sie auf dem Inforegister **Kontenschema** **Kontenschema bearbeiten**.  
6.  Um die Daten der Kontenschemas-KPIs anzuzeigen, die Sie eingerichtet haben, wählen Sie auf der Registerkarte Navigieren, in der Gruppe **Allgemein Kontoschema KPI Webservice**.  
7.  Veröffentlichen Sie den Kontenplan KPI Webdienst. Wählen Sie die Aktion **Webdient veröffentlichen**. Der Webdienst wird der Liste der veröffentlichten Webdienste im Fenster **Webservices** hinzugefügt.  

    > [!NOTE]  
    >  Sie können auch den KPI-Webdienst veröffentlichen, indem Sie im Feld **Webdienst-Setup für KPI-Kontenschema** aus dem Seitenobjekt **Webdienste** verweisen. Weitere Informationen finden Sie unter [So gehts: Veröffentlichen eines Webservice](https://msdn.microsoft.com/en-us/library/dd338978.aspx) auf MSDN.  

## <a name="see-also"></a>Siehe auch  
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

