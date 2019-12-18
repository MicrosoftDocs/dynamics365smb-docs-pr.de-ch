---
title: Benutzerberechtigungen zuweisen oder bearbeiten | Microsoft Docs
description: Beschreibt, wie Office 365-Benutzern Business Central hinzugefügt wird und vergibt dann Berechtigungen, Zugriffsrechte und Sicherheitseinstellungen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 12/03/2019
ms.author: sgroespe
ms.openlocfilehash: 1d0b7b7363df88e52631b4ba6e2f495be13f7397
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896171"
---
# <a name="create-users-according-to-licenses"></a>Benutzer nach Lizenzen anlegen
Im Folgenden wird beschrieben, wie Sie als Administrator Benutzer anlegen und definieren, wer sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden darf und welche Grundrechte verschiedene Benutzertypen entsprechend den Lizenzen haben.

Wenn Benutzer unter [!INCLUDE[d365fin](includes/d365fin_md.md)] angelegt werden, können Sie den Benutzern über Berechtigungssätze spezifische Berechtigungen zuweisen und Benutzer in Benutzergruppen organisieren, um die Berechtigungsverwaltung zu erleichtern. Weitere Informationen finden Sie unter [Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).  

> [!NOTE]
> Der Prozess der Verwaltung von Benutzern und Lizenzen variiert je nachdem, ob Ihre Lösung online oder vor Ort bereitgestellt wird. Beispielsweise können Sie in Online-Bereitstellungen einen Benutzer nur dann deaktivieren und aktivieren, wenn er zu [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzugefügt wurde. In lokalen Implementierungen können Sie Benutzer erstellen, bearbeiten und löschen.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Verwalten von Benutzern und Lizenzen in Online-Bereitstellungen
Bei [!INCLUDE[d365fin](includes/d365fin_md.md)] online wird die Anzahl der Benutzer durch das Abonnement definiert und Ihrem Mandaten im Microsoft Partner Center, typischerweise von Ihrem Microsoft-Partner, hinzugefügt. Weitere Informationen finden Sie unter [Neukunden hinzufügen](https://docs.microsoft.com/partner-center/add-a-new-customer) und [Kundenabonnements anlegen, aussetzen oder kündigen](https://docs.microsoft.com/partner-center/create-a-new-subscription) in der Microsoft Partner Center Hilfe.

Um zu definieren, wer sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden darf, müssen die Produktlizenzen den Benutzern entsprechend den Rollen zugeordnet werden, die sie bei [!INCLUDE[d365fin](includes/d365fin_md.md)] übernehmen werden. Dies kann auf folgende Weise geschehen:
- Der Office 365-Administrator Ihres Unternehmens kann dies im [Microsoft 365 Administrationscenter](https://admin.microsoft.com) tun. Weitere Informationen finden Sie unter [Benutzer einzeln oder in grossen Mengen zu Office 365](https://aka.ms/CreateOffice365Users) hinzufügen.  
- Ein Microsoft-Partner kann Lizenzen im Microsoft 365 Administrationscenter oder im Microsoft Partner Center vergeben. Weitere Informationen finden Sie unter [Benutzerverwaltung für Kundenkonten](https://docs.microsoft.com/partner-center/assign-licenses-to-users) in der Hilfe zum Microsoft Partner Center.

Weitere Informationen finden Sie unter [Administration von Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) in der Hilfe für Entwickler und ITPro.

Wenn Benutzer mit einer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Lizenz in Office 365 erstellt werden, können sie auf die Seite **Benutzer** in [!INCLUDE[d365fin](includes/d365fin_md.md)] mithilfe der Aktion **Neue Benutzer von Office 365 abrufen** importiert werden.

### <a name="to-add-a-user-in-business-central"></a>Hinzufügen eines Benutzers in Business Central
Um Benutzer aus dem Microsoft 365 Administrationscenter online auf [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzuzufügen, verwenden Sie eine spezielle Importfunktion.  
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neue Benutzer von Office 365 abrufen** aus.

Jeder neue Benutzer, der für Ihr Office 365-Abonnement erstellt wurde, wird auf der Seite **Benutzer** hinzugefügt. Den Benutzern werden Berechtigungssätze entsprechend der dem Benutzer unter Office 365 zugewiesenen Lizenz zugewiesen. Anschliessend können Sie den Benutzern detailliertere Berechtigungen zuweisen und sie zur einfachen Berechtigungsverwaltung in Benutzergruppen organisieren. Weitere Informationen finden Sie unter [Zuordnen von Berechtigungssätzen zu Benutzern](ui-define-granular-permissions.md#to-assign-permission-sets-to-users).

> [!NOTE]
> Wenn Sie einen externen Buchhalter verwenden, um Ihre Bücher und Finanzberichterstattung zu verwalten, können Sie ihn/sie in Ihr Business Central einladen, damit er/sie mit Ihnen an Ihren Steuerdaten zu arbeiten. Weitere Informationen finden Sie unter [Ihren externen Buchhalter in Ihr Business Central einladen](finance-accounting.md#inviteaccountant)

### <a name="to-remove-a-users-access-to-the-system"></a>So entfernen Sie den Zugriff eines Benutzers auf das System
In Online-Bereitstellungen können Sie den Zugriff eines Benutzers auf das System entfernen, indem Sie das Feld **Status** auf **Deaktiviert** setzen. Alle Referenzen auf den Benutzer bleiben erhalten, aber der Benutzer kann sich nicht mehr am System anmelden und aktive Sitzungen für den Benutzer werden beendet.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Seite **Benutzerkarte** für den jeweiligen Benutzer, und wählen Sie dann im Feld **Status** **Deaktiviert**.
3. Um dem Benutzer erneut Zugriff zu gewähren, ändern Sie das Feld **Zustand** auf **aktiviert**.

Zusätzlich zur Deaktivierung eines Benutzers können Sie die Zuweisung der Lizenz zu einem Benutzer im Microsoft 365 Admin Center aufheben. Der Benutzer kann sich dann nicht mehr anmelden. Weitere Informationen finden Sie unter [Lizenzen von Benutzern aufheben](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>So ändern Sie die zugewiesene Lizenz für einen Benutzer
Manchmal kann es erforderlich sein, die Lizenz zu ändern, die einem Benutzer zugeordnet ist. Wenn Sie sich beispielsweise für die Verwendung des Service Management Moduls entscheiden und daher alle Essential-Lizenzen auf Premium aktualisieren müssen. Oder wenn sich die Verantwortung eines Benutzers geändert hat und Sie eine Team Member-Lizenz durch Essential ersetzen müssen.

1. Ändern Sie die Lizenz im Microsoft 365 Admin Center. Weitere Informationen finden Sie unter [Benutzer einzeln oder in grossen Mengen zu Office 365](https://aka.ms/CreateOffice365Users) hinzufügen.
2. Melden Sie sich als Administrator bei [!INCLUDE[d365fin](includes/d365fin_md.md)] an.
3. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.
4. Wählen Sie auf der Seite **Benutzer** die Aktion **Alle Benutzergruppen aktualisieren** aus.

Die Benutzer werden in eine eigene Benutzergruppe verschoben und die Berechtigungsgruppen werden aktualisiert. Weitere Informationen finden Sie unter [Berechtigungen über Benutzergruppen verwalten](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Allen regulären Benutzern in einer Lösung muss die gleiche Lizenz, Essential oder Premium, zugewiesen werden.
> Informationen zur Lizenzierung finden Sie unter [Microsoft Dynamics 365 Business Central Lizenzleitfaden](https://aka.ms/BusinessCentralLicensing).

### <a name="synchronization-with-office-365"></a>Synchronisierung mit Office 365
Wenn einem Benutzer in Office 365 eine Lizenz zugewiesen ist, gibt es zwei Möglichkeiten, den Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu erstellen. Das System führt dies automatisch aus, wenn sich der Benutzer zum ersten Mal anmeldet, oder der Administrator kann den Benutzer durch Auswahl der Aktion **Benutzer von Office 365 abrufen** auf der Seite **Benutzer** hinzufügen.

In beiden Fällen werden einige zusätzliche Einstellungen automatisch vorgenommen. Diese sind in der zweiten und dritten Spalte der Tabelle unten aufgeführt.

Wenn Sie den Benutzer in Office 365 danach ändern und Sie die Änderungen mit [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisieren müssen, können Sie unterschiedliche Aktionen auf der Seite **Benutzer** verwenden, abhängig davon, was genau Sie synchronisieren möchten. Diese sind in den letzten drei Spalten in der Tabelle unten aufgeführt.

|Was passiert, wenn:|Erste Anmeldung|Benutzer abrufen von Office 365|Benutzer aktualisieren von Office 365|Standardbenutzergruppen des Benutzers wiederherstellen|Benutzergruppen aktualisieren|
|-|-|-|-|-|-|
|Umfang:|Aktueller Benutzer|Neue Benutzer in Office 365|Mehrere ausgewählte Benutzer|Einzelner ausgewählter Benutzer (ausser aktuellem)|Mehrere ausgewählte Benutzer|
|Erstellen Sie den neuen Benutzer und weisen Sie ihm einen SUPER-Berechtigungssatz zu.<br /><br />Plattform|**X**|**X**| | | |
|Aktualisieren Sie den Benutzerdatensatz basierend auf den tatsächlichen Informationen in Office 365: Status, vollständiger Name, Kontakt-E-Mail, Authentifizierungs-E-Mail.<br /><br />Codeunit "Azure AD   Graph-Benutzer".UpdateUserFromAzureGraph|**X**|**X**|**X**|**X**| |
|Synchronisieren Sie Benutzerpläne (Lizenzen) mit Lizenzen und Rollen, die in Office 365 zugewiesen sind.<br /><br />Codeunit "Azure AD   Graph-Benutzer".UpdateUserPlans|**X**|**X**| |**X**|**X**|
|Fügen Sie den Benutzer gemäss den aktuellen Benutzerplänen zu Benutzergruppen hinzu. Widerrufen Sie den SUPER-Berechtigungssatz. (Mindestens ein SUPER wird benötigt. Widerrufen Sie nicht von [Administratoren](/dynamics365/business-central/dev-itpro/administration/tenant-administration) aus.)<br /><br />Codeunit "Berechtigungsmanager". AddUserToDefaultUserGroups|**X**|**X**| |**X**<br /><br />Überschreiben: Entfernen Sie den Benutzer aus anderen Gruppen. Entfernen Sie manuell zugewiesene Berechtigungssätze.|**X**<br /><br />Additiv: Behalten Sie die aktuelle Mitgliedschaft in der Benutzergruppe und die zugewiesenen Berechtigungssätze intakt. Fügen Sie Benutzer nur bei Bedarf zu Gruppen hinzu.|

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Verwalten von Benutzern und Lizenzen in lokalen Bereitstellungen
Bei lokalen Implementierungen vor Ort wird in der Lizenzdatei (.flf) eine Anzahl von lizenzierten Benutzern angegeben. Wenn der Administrator oder Microsoft-Partner die Lizenzdatei hochlädt, kann der Administrator festlegen, welche Benutzer sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden können.

Bei lokalen Implementierungen erstellt, bearbeitet und löscht der Administrator Benutzer direkt von der Seite **Benutzer**.

### <a name="to-edit-or-delete-a-user-on-premises"></a>So bearbeiten oder löschen Sie einen Benutzer vor Ort
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Benutzer aus, und wählen Sie anschliessend die Aktion **Bearbeiten** aus.
3. Füllen Sie auf der Seite **Benutzerkarte** die Informationen nach Bedarf aus.    
4. Um einen Benutzer zu löschen, wählen Sie den Benutzer, den Sie löschen möchten, und wählen die Aktion **Löschen** aus.

> [!NOTE]
> Für lokale Bereitstellungen von [!INCLUDE[d365fin](includes/d365fin_md.md)] kann der Administrator zwischen verschiedenen Autorisierungsmechanismen für Benutzer auswählen. Wenn Sie einen Benutzer erstellen, stellen Sie je nach Anmeldeinformationstyp in der aktuellen [!INCLUDE[server](includes/server.md)]-Instanz verschiedene Informationen bereit.<br /><br />
> Weitere Informationen finden Sie unter [Authentifizierungs- und Anmeldeinformationstypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) im Abschnitt Verwaltung des Entwicklers und des ITPro-Inhalts für. [!INCLUDE[d365fin](includes/d365fin_md.md)]

## <a name="see-also"></a>Siehe auch
[Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  
[Profile verwalten](admin-users-profiles-roles.md)  
[Funktionen, die angezeigt werden ändern](ui-experiences.md)  
[Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Verwaltung](admin-setup-and-administration.md)  
[Hinzufügen von Benutzern zu Office 365 for Business](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Central-Lizenzierungshandbuch](https://aka.ms/BusinessCentralLicensing)  
[Sicherheit und Schutz in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) in Developer und IT-pro Help
