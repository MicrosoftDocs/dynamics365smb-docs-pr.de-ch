---
title: Benutzereinstellungen und Präferenzen in Dynamics 365 Business Central verwalten
description: Verwalten Sie Benutzereinstellungen und Präferenzen in Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 10/01/2020
ms.author: soalex
ms.openlocfilehash: 25b3c8a795c1a3f9d08ae0971da88b78e4d29b25
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752589"
---
# <a name="manage-user-settings-and-preferences"></a>Benutzereinstellungen und Präferenzen verwalten

Als Administrator können Sie Benutzereinstellungen in [!INCLUDE[prod_short](includes/prod_short.md)] vornehmen, ähnlich wie einzelne Benutzer ihre eigenen Einstellungen auf der Seite **Meine Einstellungen** verwalten können.  

## <a name="types-of-user-settings"></a>Typen von Benutzereinstellungen

Die Option *Benutzereinstellungen*, bei der es um den Benutzer als Entität und den Zugriff des Benutzers im System geht, ist nicht mit der Option *Benutzereinrichtung* identisch. Darüber hinaus haben Benutzereinstellungen nichts mit der Personalisierung eines Benutzers zu tun, wie z. B. geringfügige Änderungen an der Benutzeroberfläche. Benutzereinstellungen bestimmen die Einstellungen des Benutzers in verschiedenen Aspekten der Art und Weise, wie sich die Anwendung dem Benutzer präsentiert. Im folgenden Absatz werden die fünf Typen von Benutzereinstellungen und Präferenzen aufgeführt, die von der Person oder zentral vom Administrator festgelegt werden können:

- **Unternehmen**  

  Diese Einstellung bestimmt das Unternehmen, bei dem sich bei der nächsten Anmeldung angemeldet werden soll. Ein Benutzer kann Zugriff auf mehrere Unternehmen haben und in mehreren Unternehmen aktiv sein.

- **Profil (Rollen)**  

  Das Profil beschreibt die Funktion des Benutzers im Unternehmen, z. B. *Verkaufsleiter*, *Buchhalter* oder *Einkäufer*. Das Profil bestimmt dann das Rollencenter des Benutzers, die Startseite, die Benutzern bei der Anmeldung angezeigt wird. Das Profil hat keine Auswirkungen auf die Zugriffsrechte auf Funktionen in [!INCLUDE[prod_short](includes/prod_short.md)].  

- **Gebietsschema-ID (regionale Einstellungen)**  

  Definiert, wie Daten und Zahlen im [!INCLUDE[prod_short](includes/prod_short.md)]-Client angezeigt werden, z. B., ob europäische oder amerikanische Datumsformate verwendet werden sollen oder wie das Dezimalzeichen und Tausendertrennzeichen in Beträgen angezeigt werden sollen. Beim Synchronisieren von [!INCLUDE[prod_short](includes/prod_short.md)]-Benutzern über Microsoft 365 werden die regionalen Einstellungen von Microsoft 365 verwendet, wobei davon ausgegangen wird, dass der Benutzer dieselben Einstellungen in Office-Produkten und [!INCLUDE[prod_short](includes/prod_short.md)] verwenden möchte. Ein Administrator oder Benutzer kann diese Einstellungen manuell in [!INCLUDE[prod_short](includes/prod_short.md)] ändern, diese werden jedoch von Microsoft 365 zurückgesetzt, sobald die nächste Synchronisation durchgeführt wurde.

- **Sprache**  

  Definiert die Anwendungssprache, in der [!INCLUDE[prod_short](includes/prod_short.md)] Text, Beschriftungen und Fehlermeldungen darstellt. Beim Synchronisieren von [!INCLUDE[prod_short](includes/prod_short.md)]-Benutzern über Microsoft 365 werden die Spracheneinstellungen von Microsoft 365 verwendet, wobei davon ausgegangen wird, dass der Benutzer dieselben Einstellungen in Office-Produkten und [!INCLUDE[prod_short](includes/prod_short.md)] verwenden möchte. Ein Administrator oder Benutzer kann diese Einstellungen manuell in [!INCLUDE[prod_short](includes/prod_short.md)] ändern, diese werden jedoch von Microsoft 365 zurückgesetzt, sobald die nächste Synchronisation durchgeführt wurde.

  Wenn die Spracheinstellung von Microsoft 365 einer unterstützten Sprache in [!INCLUDE[prod_short](includes/prod_short.md)] entspricht, wird diese Sprache für den Benutzer ausgewählt.  

  > [!NOTE]
  > Möglicherweise müssen Sie eine Sprach-App für [!INCLUDE[prod_short](includes/prod_short.md)] installieren, um die Sprache ordnungsgemäss anzuzeigen. Daher empfiehlt es sich, die erforderlichen Sprach-Apps zu installieren, bevor sich ein Benutzer zum ersten Mal anmeldet, sodass ihm vom ersten Tag an eine benutzerfreundliche Umgebung zur Verfügung steht. Weitere Informationen finden Sie in der Liste der [unterstützte Sprachen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
- **Zeitzone**  

  Definiert die Zeitzone, in der sich der Benutzer befindet. Derzeit wird diese nicht von Microsoft 365 synchronisiert und muss manuell eingestellt werden.  

> [!NOTE]
> Wenn eine Microsoft 365-Benutzersynchronisierung durchgeführt wird, während Benutzer bei [!INCLUDE[prod_short](includes/prod_short.md)] angemeldet sind, müssen diese Benutzer den Browser aktualisieren oder sich bei [!INCLUDE[prod_short](includes/prod_short.md)] ab- und wieder anmelden, um eine potenziell andere Sprache anzuzeigen, die durch die Synchronisierungsaktion festgelegt wurde.

## <a name="overview-of-all-user-settings"></a>Übersicht über alle Benutzereinstellungen

Administratoren haben die Möglichkeit, diese Einstellungen für Benutzer in jedem Unternehmen festzulegen oder zu ändern. Dies erfolgt auf der Seite **Benutzerpersonalisierungen**. Die Datensätze auf dieser Seite spiegeln die Auswahl des einzelnen Benutzers für die oben genannten Einstellungen wider, ein Datensatz pro Benutzer. Wenn Benutzer Änderungen an ihren Einstellungen auf der Seite **Meine Einstellungen** vornehmen, werden diese Änderungen in der Liste **Benutzerpersonalisierungen** angezeigt. Administratoren können diese Einstellungen auch für Benutzer festlegen, bevor sie sich zum ersten Mal anmelden, sodass Benutzer diese Schritte nicht selbst ausführen müssen und ihnen eine bessere *Erste Schritte*-Erfahrung geboten wird.

> [!NOTE]
> Benutzerpersonalisierungen haben nichts mit den geringfügigen *persönlichen* Änderungen zu tun, die ein Benutzer an der Benutzererfahrung vornehmen kann.

## <a name="to-review-or-make-changes-to-user-settings"></a>So überprüfen oder ändern Sie Benutzereinstellungen

1. Wählen Sie das Symbol ![Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol 'Nach Seite oder Bericht suchen'") aus, geben Sie **Benutzerpersonalisierungen** ein, und wählen Sie dann den zugehörigen Link aus.
2. Dadurch werden die Liste der Benutzer und ihre Einstellungen angezeigt. Klicken Sie zum Ändern der Einstellungen eines Benutzers auf die **Benutzer-ID**, oder wählen Sie **Verwalten** und dann **Bearbeiten** aus.
3. Die Karte **Benutzerpersonalisierung** für die Einstellungen des jeweiligen Benutzers wird angezeigt und die gewünschten Änderungen können vorgenommen werden.  

## <a name="see-also"></a>Siehe auch

[Erste Schritte](product-get-started.md)  
[Verfügbarkeit nach Ländern/Regionen und unterstützte Sprachen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Sprache und Gebiet ändern](about-locale-language.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]