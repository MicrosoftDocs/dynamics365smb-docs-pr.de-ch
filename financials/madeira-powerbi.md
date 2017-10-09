---
title: "Dynamics 365 for Financials und für Power BI Inhaltspakete| Microsoft Docs"
description: Nutzen Sie Einblicke in Ihre Finanzdaten mit Power BI und dem Financials-Inhaltspaket.
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d165efbb6a157c6f95f8f59e6aa0d9b7100daa91
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivieren Sie Ihre Geschäftsdaten für Power BI
Einblicke in Ihre [!INCLUDE[d365fin](includes/d365fin_md.md)]-Daten zu erhalten ist mit Power BI und dem [!INCLUDE[d365fin](includes/d365fin_md.md)] Financials-Inhaltspaket sehr einfach.. Power BI ruft die Daten ab und dann erstellt ein Standarddashboard und Berichte auf Grundlage der Daten.  

Microsoft hat folgende Inhaltspakete veröffentlicht:

| App | Description |
| --- | --- |
| Microsoft Dynamics 365 for Financials | Gewährt ein Dashboard mit Schlüsselfinanzdaten im Zeitverlauf, z.B. Umsatz von Ausgaben, Deckungsbeiträgen % und Geldumlauf.|
| Microsoft Dynamics 365 for Financials - CRM | Gewährt ein Dashboard mit Schlüsseldaten zu Verkaufschancen und Kontakten.  |
| Microsoft Dynamics 365 for Financials - Sales | Gewährt ein Dashboard mit Schlüsseldaten zu Verkaufschancen und Bestand. |

## <a name="using-the-dashboards"></a>Dashboards nutzen
Jedes Inhaltspaket enthält Berichte, die Sie aufrufen können in:

* Wählen Sie eine Darstellung im Dashboard, um einen der Berichte anzuzeigen.  
* Filtern Sie den Bericht oder fügen Sie Felder hinzu, die Sie überwachen möchten.  
* Heften Sie diese benutzerdefinierte Ansicht an das Dashboard an, um sie weiter zu verfolgen.  
  Sie können Daten auch manuell aktualisieren, und Sie können einen Aktualisierungsplan einrichten. Weitere Informationen finden Sie unter [Konfigurieren der geplanten Aktualisierung](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Das Inhaltspaket ist vorkonfiguriert, um mit Umsatzdaten und Finanzdaten aus dem Demounternehmen zu arbeiten, das Sie erhalten, wenn Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden. Wenn Sie die Apps in Power BI einrichten und Sie Ihre eigenen Daten verbinden, gehen einige Berichte möglicherweise nicht, da sie auf Daten beruhen, die Ihr Mandant nicht verfügt. In diesen Fällen können Sie den Bericht von Ihrem Dashboard einfach entfernen.  

> [!NOTE]  
>   Sie können eigene Berichte und Dashboards in Power BI auf Grundlage Ihrer Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen. Weitere Informationen finden Sie unter [Verbindung von Geschäftsdaten an Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="accessing-included365finincludesd365finmdmd-in-power-bi"></a>Auf [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI zugreifen
Um Ihre [!INCLUDE[d365fin](includes/d365fin_md.md)]-Daten in Power BI anzuzeigen, müssen Sie Folgendes haben:  

* Zugriff auf [!INCLUDE[d365fin](includes/d365fin_md.md)] Weitere Informationen finden Sie unter [Financials](http://go.microsoft.com/fwlink/?LinkID=759714).  
* Zugriff auf Power BI Weitere Informationen finden Sie unter [Power BI](https://powerbi.microsoft.com).

Auf der Power BI-Website finden Sie zusätzliche Informationen zum [Verbinden mit den Services mit Inhaltspaketen für Power BI](http://go.microsoft.com/fwlink/?LinkID=760850).  

Um auf die Daten [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI auf der Verbindungsseite zuzugreifen, müssen Sie die folgenden Informationen angeben:

| Feld | Description |
| --- | --- |
| **OData-Feed-URL** |Die OData-URL, damit Power BI auf die Daten von Ihrem Mandanten zugreifen kann z.B. https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('My%2Business'). |
| **Authentifizierungsmethode** |Wählen Sie **Standard** aus. |
| **Benutzername** |Ihr Name, wie er in Ihrem Konto in [!INCLUDE[d365fin](includes/d365fin_md.md)] angezeigt wird wie *John Smith*.. |
| **Kennwort** |Dies ist der Webdienst-Zugriffsschlüssel für Ihr Benutzerkonto in [!INCLUDE[d365fin](includes/d365fin_md.md)] |

Das bedeutet, dass Sie drei Informationen aus [!INCLUDE[d365fin](includes/d365fin_md.md)] benötigen: die *OData-URL* und den *Webdienst-Zugriffsschlüssel* für Ihr Benutzerkonto.  

### <a name="getting-the-url"></a>Abrufen der URL
Wenn Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] zu Power BI hinzufügen, müssen Sie eine URL angeben, über die Power BI Daten von Ihrem Mandanten abrufen kann. Auf der Verbindungsseite wird die URL als **OData-Feed URL** bezeichnet und muss folgendes Format aufweisen:

         https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
In diesem Beispiel ist *mybusiness* der Name des [!INCLUDE[d365fin](includes/d365fin_md.md)]-Dienstes und *CRONUS US* ist der Name des Demounternehmens, wobei *%20* das Leerzeichen im Namen darstellt.   
Um die URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] abzurufen, suchen Sie das Fenster **Webdienste** und öffnen es. Dieses Fenster führt die Webdienste auf, die aktuell verfügbar sind, und Sie können den Link aus dem **OData URL**-Feld für einen der OData-Webdienste kopieren.  

### <a name="getting-the-user-name-and-the-web-service-access-key"></a>Ermitteln des Benutzernamens und der Webdiensttastenkombination
Um Daten aus [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI zu nutzen, müssen Sie im Fenster **Mit Financials verbinden** einen Benutzernamen und ein Kennwort angeben. Der Benutzername ist Ihr Name wie er für Ihr Konto in [!INCLUDE[d365fin](includes/d365fin_md.md)] angezeigt wird, sodass Power BI sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden kann. Das Kennwort ist der Webdienst-Zugriffsschlüssel, den Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] für Ihr Benutzerkonto angelegt haben.  

Um diese Informationen in [!INCLUDE[d365fin](includes/d365fin_md.md)]zu finden, suchen Sie nach dem Fenster **Benutzer**  und öffnen Sie die Karte für Ihr Benutzerkonto. Im Feld Inforegister **Allgemein** kopieren Sie den Inhalt des Feldes **Benutzername** und im Inforegister **Webdienstzugriff** kopieren Sie den Inhalt des Felds **Webdienst-Zugriffsschlüssel**. Wenn das Feld **Webdienstzugriffsschlüssel**leer ist, wählen Sie im Menüband **Webdienst-Zugriffsschlüssel ändern**, wählen Sie **Schlüssel läuft nie ab** und klicken Sie anschließend auf die Schaltfläche OK. Anschließend können Sie den Schlüssel kopieren.  

## <a name="getting-data-from-included365finincludesd365finmdmd"></a>Abrufen von Daten aus [!INCLUDE[d365fin](includes/d365fin_md.md)]
Das [!INCLUDE[d365fin](includes/d365fin_md.md)]-Dashboard zeigt die Berichte an, die Sie normalerweise verwenden, um Ihr Geschäft zu verfolgen. Die Daten werden von Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)]-Mandanten über Webdienste zum Lesen von Livedaten abgerufen. In [!INCLUDE[d365fin](includes/d365fin_md.md)], listet das **Webdienste** Fenster die Webdienste an, die eingerichtet wurden.

> [!NOTE]  
>   Wenn Sie den Namen dieser Webdienste ändern, werden die Daten nicht in Power BI angezeigt.  
Wenn Sie weitere Daten in Power BI verwenden möchten, müssen Sie die Tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] suchen, sie als Webdienste verfügbar machen und diese dann dem Inhaltspaket hinzufügen. Dies ist ein erweitertes Szenario. Wir empfehlen, dass Sie mit den Daten beginnen, die bereits in Power BI verfügbar sind.  

## <a name="troubleshooting"></a>Problembehebung
Das Power BI-Dashboard beruht auf den veröffentlichten Webdiensten, die oben erwähnten werden. Es enthält Daten vom Demomandanten oder von Ihrem eigenen Unternehmen wenn Sie Daten aus der aktuellen Finanzlösung importieren. Wenn etwas schief geht, stellt dieser Abschnitt eine Problemumgehung für die häufigsten Probleme bereit.  

**Parameterprüfung fehlgeschlagen. Prüfen Sie, ob alle Parameter gültig sind**  
Wenn Sie diesen Fehler erhalten nachdem Sie die [!INCLUDE[d365fin](includes/d365fin_md.md)]-URL eingegeben, vergewissern Sie sich, dass die folgenden Anforderungen erfüllt sind:  

* Die URL folgt diesem Muster:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Löschen Sie den Text nach Mandantennamen in den Klammern  
* Stellen Sie sicher, dass am Ende der URL kein Schrägstrich steht.  
* Stellen Sie sicher, dass es sich um eine sichere Verbindung handelt (URL beginnt mit *https*).  

**"Anmeldung fehlgeschlagen"**  
Wenn Sie einen Anmeldung fehlgeschlagen-Fehler erhalten, wenn Sie mit Ihren [!INCLUDE[d365fin](includes/d365fin_md.md)]-Anmeldedaten am Dashboard angemeldet sind, kann dies durch eines der folgenden Probleme verursacht werden:

* Das Konto, das Sie verwenden, hat keine Berechtigungen, um die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Daten aus Ihrem Konto zu lesen.

    Prüfen Sie Ihr Benutzerkonto in [!INCLUDE[d365fin](includes/d365fin_md.md)] und vergewissern Sie sich, ob Sie den richtigen Webdienst-Zugriffsschlüssel und das passende Kennwort verwendet haben, und Versuchen Sie es dann erneut.  
* Die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Instanz mit der Sie eine Verbindung herstellen wollen hat kein gültiges SSL-Zertifikat. In diesem Fall wir eine detailliertere Fehlermeldung angezeigt ("Vertrauenswürdiges SSL-Beziehung kann nicht erstellt werden").

    > [!NOTE]  
>   Selbstsignierte Zertifikate werden nicht unterstützt.  

**"Oops"**  
Wenn Sie ein Oops "-Fehlerdialogfeld" erhalten, nachdem Sie das Authentifizierungsdialogfeld abgeschlossen haben, wird dieses am häufigsten durch ein Problem mit der Verbindung zu den Daten für das Inhaltspaket verursacht.

* Vergewissern Sie sich, dass die URL dem Muster folgt, das oben angegeben wurde:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')`  
* Ein häufiger Fehler ist, das gesamte URL für einen bestimmten Webdienst angegeben wird:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')/powerbifinance`
* Oder Sie vergessen den Unternehmensnamen anzugeben:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/`

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Geschäftsdaten aus anderen Finanzsystemen migrieren](upload-data.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-how-use-financials-data-source-powerbi.md)Financials als Power BI Datenquelle nutzen  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-how-use-financials-data-source-powerapps.md)Financials als Power BI Datenquelle nutzen  
[Anwendung [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] in Microsoft-Fluss](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

