---
title: Verwenden Sie die Daten, um eine App zu erstellen| Microsoft Docs
description: Sie können Daten aus Business Central zur Verfügung stellen und eine OData URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe von Power Apps zu erstellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5d2e6b75978d9aced7636b41623365f3d98ed3aa
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754506"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Verknüpfung mit Business Central, um eine Geschäfts-App mithilfe von Power Apps zu erstellen

Sie können die [!INCLUDE[prod_short](includes/prod_short.md)] Daten als Datenquelle in Power Apps bereitstellen.  

> [!NOTE]  
> Sie müssen ein gültiges Konto bei [!INCLUDE[prod_short](includes/prod_short.md)] und Power Apps haben.  

## <a name="to-add-prod_short-as-a-data-source-in-power-apps"></a>So fügen Sie [!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power Apps hinzu

1. In Ihrem Browser navigieren und zu [powerapps.microsoft.com](https://powerapps.microsoft.com/) gehen und sich dann anmelden.
2. Wählen Sie auf der Homepage im Abschnitt **Beginn von Daten** die Kachel **Andere Datenquellen** aus.  

    Dadurch wird Power Apps Studio geöffnet. Bei der ersten Anmeldung müssen Sie das Land/die Region angeben.  
3. In der Liste der verfügbaren Verbindungscodes wählen Sie **Business Central** und dann die Schaltfläche **Erstellen** aus.

    Power Apps PowerApps verbinden sich mit Ihrem [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe der Anmeldeinformationen, mit denen Sie sich anmelden. Wenn Sie KEIN Administrator Ihrer [!INCLUDE[prod_short](includes/prod_short.md)] sind, müssen Sie sich möglicherweise bei einem anderen Konto anmelden.  

4. Power Apps zeigt eine Liste der *Umgebungen und Unternehmungen* an, die in [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar sind. Wählen Sie die Umgebung und das Unternehmen aus, in der sich die Daten befinden, zu denen Sie eine Verbindung herstellen möchten, z. B. *PRODUKTION - Mein Unternehmen*.  

5. Als Nächstes wird eine Liste der Tabellen angezeigt, die als Teil der API für Ihre Umgebung bereitgestellt werden. Wählen Sie die Tabelle aus, zu der Sie eine Verbindung herstellen möchten, und wählen Sie dann **Verbinden** aus.

Diese sogenannten Tabellen werden von [!INCLUDE[prod_short](includes/prod_short.md)] Connector für Power Apps als Endpunkte bereitgestellt.  

> [!NOTE]
> Wenn Sie Daten aus anderen Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] in Ihre Anwendung aufnehmen möchten, müssen Sie mit einem Entwickler zusammenarbeiten, um eine benutzerdefinierte API in [!INCLUDE[prod_short](includes/prod_short.md)] zu definieren und diese benutzerdefinierte API dann über einen benutzerdefinierten Konnektor in Power Apps zu verwenden. Weitere Informationen finden Sie unter [Erstellen Sie einen benutzerdefinierten Connector von Grund auf neu](/connectors/custom-connectors/define-blank).  

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Daten verbunden und sind bereit, Ihre Power App zu erstellen. Sie können zusätzliche Bildschirme hinzufügen und an weitere Daten von Ihrem  [!INCLUDE[prod_short](includes/prod_short.md)] anschliessen. Weitere Informationen finden Sie unter [Erstellen einer Canvas-App aus einem Beispiel in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Wenn Sie Ihre App entworfen und erstellt haben, können Sie diese mit Ihre Kollegen teilen. Weitere Informationen finden Sie unter [Speichern und veröffentlichen Sie eine Canvas-App in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal verbinden möchten, müssen Sie den **Business Central (lokal)** Connector in Schritt 3 auswählen.  

## <a name="see-also"></a>Siehe auch

[Erstellen Sie eine Canvas-App aus einer Vorlage in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Erste Schritte mit dem Entwickeln von Verbindungs-Apps für Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]