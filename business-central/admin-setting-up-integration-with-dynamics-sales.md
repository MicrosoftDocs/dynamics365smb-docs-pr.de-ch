---
title: Einrichten des Benutzerkontos für die Integration in Dynamics 365 for Sales | Microsoft Docs
description: Erfahren Sie, wie die Benutzerkonten eingerichtet werden, die die Apps zum Austausch von Daten verwenden, und die Mitarbeiter nutzen, um auf Daten in den Apps zuzugreifen und diese Daten zu synchronisieren.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 3163389cb0818133fba9ab8c55b8d0cf662130f1
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620967"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Einrichten des Benutzerkontos für die Integration in Dynamics 365 for Sales
Dieser Artikel bietet eine Übersicht darüber, wie die Benutzerkonten eingerichtet werden, die erforderlich sind, um [!INCLUDE[d365fin](includes/d365fin_md.md)] in [!INCLUDE[crm_md](includes/crm_md.md)] zu integrieren.  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-admininstrator-user-account-in-sales"></a>Einrichten des Admininstratorbenutzerkontos im Verkauf
Sie müssen Ihr Administratorbenutzerkonto für [!INCLUDE[d365fin](includes/d365fin_md.md)] als Benutzer in [!INCLUDE[crm_md](includes/crm_md.md)] hinzufügen und dann den Benutzer zum Administrator in [!INCLUDE[crm_md](includes/crm_md.md)] befördern. Das Administratorbenutzerkonto muss auch die Rolle des Systemanpassers und mindestens eine andere nicht administrative Benutzerrolle, z. B. Vertriebsmanager, in [!INCLUDE[crm_md](includes/crm_md.md)] haben.

## <a name="setting-up-the-user-account-for-the-integration"></a>Einrichten des Benutzerkontos für die Integration
Sie müssen ein spezifisches Benutzerkonto in Ihrem Office 365-Abonnement erstellen, das sowohl [!INCLUDE[d365fin](includes/d365fin_md.md)] als auch [!INCLUDE[crm_md](includes/crm_md.md)] verwenden können, um Daten zu synchronisieren. Dieses Benutzerkonto muss in der Lage sein, sich bei [!INCLUDE[crm_md](includes/crm_md.md)] anzumelden, was bedeutet, dass dieser Benutzer eine Lizenz für [!INCLUDE[crm_md](includes/crm_md.md)] benötigt und mindestens eine Sicherheitsrolle in [!INCLUDE[crm_md](includes/crm_md.md)] zugewiesen werden muss, wie [ hier](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account) beschrieben. Weitere Informationen darüber, wie Benutzer in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt werden, finden Sie unter [Verwalten von Sicherheit, Benutzern und Teams](http://go.microsoft.com/fwlink/?LinkID=616518). Nachdem die Verbindung eingerichtet ist, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] dem Benutzerkonto die Sicherheitsrollen zuweisen, die sie benötigen in [!INCLUDE[d365fin](includes/d365fin_md.md)] und dieses Konto kann auf [ nicht interaktiven Zugriffsmodus](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) festgelegt werden in [!INCLUDE[crm_md](includes/crm_md.md)]

![Der Leitfaden für das unterstützte Setup zeigt den Ort, an dem die Anmeldeinformationen für die Synchronisierung eingegeben werden](media/sync-user-setup.png "Assistentenseite für die Visualisierung des unterstützten Setups zeigt den Ort, an dem die Anmeldeinformationen für die Synchronisierung eingegeben werden")

> [!IMPORTANT]  
> Verwenden Sie nicht das Administratorkonto für [!INCLUDE[crm_md](includes/crm_md.md)] für die Synchronisierung. Dadurch wird die Synchronisierung unterbrochen.
> Um die konstante Synchronisierung zu vermeiden, werden auch Änderungen an den Daten, die durch das Integrationsbenutzerkonto vorgenommen werden, nicht synchronisiert. <!--What changes would this account make?--> Nachdem die Verbindung hergestellt wurde, empfehlen wir, den Zugriffsmodus für das Benutzerkonto für die Integration auf einen nicht interaktiven Modus in [!INCLUDE[crm_md](includes/crm_md.md)] festzulegen. Weitere Informationen finden Sie unter [Erstellen eines nicht interaktiven Benutzerkontos](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Einrichten von Konten für Verkäufer
Sie müssen Benutzerkonten in [!INCLUDE[crm_md](includes/crm_md.md)] für die Verkäufer von [!INCLUDE[d365fin](includes/d365fin_md.md)]. Um das zu vereinfachen, bietet das Microsoft 365 Admin Center eine Excel-Vorlage, die Sie verwenden können. Wählen Sie auf der Seite **Aktive Benutzer** die Option **Mehr** und dann **Mehrere Benutzer importieren** aus. Wählen Sie **CSV-Datei nur mit Kopfzeilen herunterladen** aus und geben Sie dann die Informationen für die Verkäufer ein. Um ein Beispiel anzusehen, wählen Sie **CSV-Datei mit Kopfzeilen und Beispielbenutzerinformationen herunterladen** aus. Nachdem Sie die Informationen über die Benutzer eingeben, besteht der nächste Schritt im Importvorgang darin, den Benutzern Lizenzen zu dem Dynamics 365 Customer Engagement-Plan zuzuweisen.  

Nachdem Sie die Benutzer importiert und ihnen Lizenzen für Dynamics 365 Customer Engagement zugewiesen haben, müssen Sie die Benutzer der Rolle **Verkäufer** in [!INCLUDE[crm_md](includes/crm_md.md)] zuweisen.

![Koppeln von Verkäufern mit Benutzern in Dynamics 365 for Sales](media/couple-salespeople.png "Visualisierung des Koppelns von Verkäufern mit Benutzern in Dynamics 365 for Sales")

## <a name="see-also"></a>Siehe auch  
[Integrieren in Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
