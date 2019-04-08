---
title: Verwaltung von Personalisierung als Administrator in Business Central | Microsoft Docs
description: Erfahren Sie, wie Sie die Benutzeroberfläche anpassen, damit diese Ihren Bedürfnissen entspricht.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: ad3b4cf3be7031ab1c7c4699bed6020fe09bd2d1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "819486"
---
# <a name="managing-personalization-as-an-administrator"></a>Personalisierung als Administrator verwalten
<!--NAV in the Web client--> Benutzer können ihren Arbeitsbereich personalisieren, um ihren Bedürfnissen zu entsprechen. Als Administrator können Sie Anpassungen steuern und verwalten, indem Sie die Möglichkeit deaktivieren, dass Benutzer Seiten anpassen und sämtliche Seitenanpassungen löschen, die Benutzer vorgenommen haben.

## <a name="disable-personalization-for-a-profile"></a>Personalisierung für ein Profil deaktivieren
Sie können verhindern, dass alle Benutzer, die zu einem bestimmten Profil gehören, ihre Seiten personalisieren können.
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Profilliste** ein, und wählen dann den zugehörigen Link aus.
2.  Wählen Sie das Profil in der Liste aus, das Sie ändern möchten.
3. Aktivieren Sie das Kontrollkästchen **Anpassung deaktivieren**, und klicken Sie dann auf die Schaltfläche **OK**.

## <a name="clear-user-personalizations"></a>Benutzerpersonalisierung deaktivieren

Die Löschung der Seitenanpassung ändert die Seite oder erstellt das ursprüngliche Layout wieder. Es gibt zwei Möglichkeiten, die Anpassungen zu löschen, die Benutzer auf Seiten vorgenommen haben: mit der Seite **Benutzeranpassung löschen** und mithilfe der Anwendung der Seite **Benutzeranpassungskarte**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Benutzeranpassungen löschen mithilfe der Seite Benutzeranpassungen löschen

Die Seite **Benutzeranpassung löschen** gibt Ihnen die Möglichkeit, die Personalisierung für eine Seite oder pro Benutzer zu löschen.

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzeranpassung löschen** ein, und wählen dann den zugehörigen Link aus.

    Die Seite führt alle Seiten auf, die angepasst wurden, und den Benutzer, dem sie gehören.

    >[!NOTE]
    > Ein Häkchen in den Spalten **Vorgänger-Anpassung** bedeutet, dass die Personalisierung in einem vorherigen Version von, die erforderlich war [!INCLUDE[d365fin](includes/d365fin_md.md)]die Anpassung, Bearb die unterscheidet, als sie jetzt zu konfigurieren. Benutzer, die versuchen, diese Seiten zu personalisieren, können dies nicht tun, es sei denn, sie entsperren die Seite. Weitere Informationen finden Sie unter [Warum eine Seite zum Personalisieren gesperrt ist](ui-personalization-locked.md).

2. Wählen Sie den Posten, den Sie löschen möchten, und wählen die Aktion **Löschen** aus.

    Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Benutzeranpassungen löschen mithilfe der Seite Benutzeranpassungskarte.

Die Seite **Benutzeranpassungskarte** gibt Ihnen die Möglichkeit, die Personalisierung für alle Seiten für eijnen bestimmten Benutzer zu löschen. Dazu müssen Sie die Schreibberechtigung für Tabelle 2000000072 **Profil** haben.

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzeranpassung** ein, und wählen dann den zugehörigen Link aus.

    Die Seite **Benutzeranpassung** führt alle Benutzer auf, die möglicherweise eine personalisierte Seite haben. Wenn Sie einen Benutzer in der Liste nicht finden können, bedeutet dies, dass sie keine personalisierten Seiten haben.

2. Wählen den Benutzer aus der Liste aus und wählen Sie dann die Aktion **Bearbeiten** aus.

3.  Wählen Sie auf der Registerkarte **Aktionen** **Personalisierte Seiten löschen** aus.

    Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.

## <a name="see-also"></a>Siehe auch
[Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Sie können auswählen, welche Funktionen angezeigt werden](ui-experiences.md)  
