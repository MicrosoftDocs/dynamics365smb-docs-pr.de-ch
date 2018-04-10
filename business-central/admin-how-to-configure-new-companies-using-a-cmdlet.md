---
title: 'Vorgehensweise: Konfigurieren neuer Unternehmen per Cmdlet | Microsoft Docs'
description: "In einigen Szenarien können Sie ein Konfigurationspaket laden und importieren, ohne Ihre Benutzer mit einzubeziehen oder die RapidStart Services-Benutzeroberfläche zu verwenden. Dies können Sie tun, indem Sie ein Windows PowerShell cmdlet  verwenden."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 9d248f2f8676c392451ae4a6f99932145f354f5b
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a>Vorgehensweise: Konfigurieren neuer Unternehmen per Cmdlet
In einigen Szenarien können Sie ein Konfigurationspaket laden und importieren, ohne Ihre Benutzer mit einzubeziehen oder die RapidStart Services-Benutzeroberfläche zu verwenden. Dies können Sie tun, indem Sie ein Windows PowerShell cmdlet  verwenden. Szenarien, in denen dies hilfreich sein kann, sind etwa:  

- Ausführen des Dateniports in mehre  [!INCLUDE[d365fin](includes/d365fin_md.md)] Installationsarbeiten.
- Konfigurieren von zusätzlichen Anwendungsbereichen für mehrere Kunden.  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a>Ein Konfigurationspaket unter Verwendung eines Cmdlets bereitstellen  

1. Bereiten Sie ein RapidStart-Dienstepaket vor. Beispielsweise können Sie ein Paket erstellen, um bestimmte Werte und Namen der Tabelle und der Felder zu importieren und diese Werte einzufügen.  
2. Setzen Sie das Paket auf einen Computer, auf dem Sie das Cmdlet ausführen.  
3. [!INCLUDE[d365fin](includes/d365fin_md.md)] Verwaltungsshell öffnen.  
4. Geben Sie **Invoke-NAVCodeUnit** ein, und geben Sie Daten wie im folgenden Beispiel an.  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
Das Cmdlet importiert das Paket in jedes Unternehmen. Benutzer können sofort beginnen, eine neue Funktionalität zu verwenden.  

## <a name="see-also"></a>Siehe auch  
[So konfigurieren Sie einen neuen Mandanten.](admin-how-to-configure-new-companies.md)  
[Übernehmen von Konfiguration in neue Mandanten](admin-apply-configuration-to-new-companies.md)  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)  
[Microsoft Dynamics NAV Windows PowerShell-Cmdlets](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

