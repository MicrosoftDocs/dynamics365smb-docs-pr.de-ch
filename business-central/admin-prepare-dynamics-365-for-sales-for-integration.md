---
title: Integration in Dynamics 365 Sales| Microsoft Docs
description: Erfahren Sie, wie Sie Dynamics 365 Business Central für die Integration mit Dynamics 365 Sales vorbereiten.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 692c3d10ba8bc72b3993d4f05cc9dcaee7dabc8c
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035695"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integration mit Dynamics 365 Sales
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Die Rolle des Verkäufers wird häufig als eine der am meisten nach aussen gerichteten Tätigkeiten in einem Unternehmen angesehen. Es kann jedoch für Verkäufer hilfreich sein, einen Blick in das Innere des Unternehmens zu werfen und zu erfahren, was am anderen Ende passiert. Durch die Integration von [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] können Sie Ihren Verkäufern diese Einblicke ermöglichen, indem Sie es ihnen ermöglichen, diese Informationen in [!INCLUDE[prod_short](includes/prod_short.md)] abzurufen, während sie in [!INCLUDE[crm_md](includes/crm_md.md)] arbeiten. Bei der Vorbereitung einer Verkaufsofferte kann es zum Beispiel hilfreich sein, zu wissen, ob ausreichend Lagerbestand vorhanden ist, um die Bestellung zu erfüllen. Weitere Informationen finden Sie unter [Verwenden von Dynamics 365 Sales von Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Dieses Thema beschreibt den Prozess der Integration der Online-Versionen von [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] bis [!INCLUDE[prod_short](includes/cds_long_md.md)]. Informationen zur lokalen Konfiguration finden Sie unter [Dynamics 365 Sales für die lokale Integration vorbereiten](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-dataverse"></a>Integrieren über Dataverse
[!INCLUDE[prod_short](includes/prod_short.md)] lässt sich auch mit der [!INCLUDE[prod_short](includes/cds_long_md.md)] integrieren, was die Verbindung und Synchronisierung von Daten mit anderen Dynamics 365-Anwendungen wie [!INCLUDE[crm_md](includes/crm_md.md)] oder sogar selbst erstellten Anwendungen erleichtert. Wenn Sie zum ersten Mal integrieren, empfehlen wir Ihnen, dies über [!INCLUDE[prod_short](includes/cds_long_md.md)] zu tun. Weitere Informationen finden Sie unter [Integration mit Dataverse](admin-common-data-service.md).

Wenn Sie bereits [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[prod_short](includes/prod_short.md)] integriert haben, können Sie die Datensynchronisation mit Ihrem Setup fortsetzen. Wenn Sie jedoch Ihre [!INCLUDE[crm_md](includes/crm_md.md)]-Integration aktualisieren oder ausschalten, müssen Sie, um sie wieder einzuschalten, eine Verbindung über [!INCLUDE[prod_short](includes/cds_long_md.md)] herstellen. Weitere Informationen finden Sie unter [Aktualisierung einer Integration mit Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Eine erneute Verbindung über [!INCLUDE[prod_short](includes/cds_long_md.md)] wendet die Standard-Synchronisationseinstellungen an und überschreibt alle Ihre Konfigurationen. Es werden zum Beispiel die Standard-Tabellenzuordnungen angewendet.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Integrationseinstellungen, die spezifisch für eine [!INCLUDE[crm_md](includes/crm_md.md)]-Integration sind
Die Integration mit [!INCLUDE[prod_short](includes/prod_short.md)] geschieht durch [!INCLUDE[prod_short](includes/cds_long_md.md)], und es gibt eine Menge Standardeinstellungen und Tabellen, die durch die Integration bereitgestellt werden. Zusätzlich zu den Standardeinstellungen gibt es einige, die spezifisch für [!INCLUDE[crm_md](includes/crm_md.md)] sind. In den folgenden Abschnitten werden diese aufgelistet.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Berechtigungen und Sicherheitsrollen für Benutzerkonten im Vertrieb
Wenn Sie die Integrationslösung installieren, werden die Berechtigungen für das Integrationsbenutzerkonto konfiguriert. Wenn diese Berechtigungen geändert werden, müssen Sie sie möglicherweise zurücksetzen. Sie können dies tun, indem Sie die Integrationslösung neu installieren, indem Sie **Integrationslösung neu installieren** auf der Seite **Dynamics 365 Verbindungseinrichtung** wählen. Die folgenden Sicherheitsrollen werden eingesetzt:

* Dynamics 365 Business Central Integrations-Administrator
* Dynamics 365 Business Central Integration Benutzer
* Dynamics 365 Business Central Benutzer der Produktverfügbarkeit

### <a name="connection-settings-in-the-setup-guide"></a>Verbindungseinstellungen im Einrichtungshandbuch

Sie können eine unterstützte Setup-Anleitung verwenden, um die Verbindung schnell einzurichten und erweiterte Funktionen wie die Kopplung zwischen Datensätzen festzulegen.

1. Wählen Sie **Einrichtung und Erweiterungen** und dann **Unterstütztes Setup** aus.
2. Wählen Sie **Dynamics 365 Sales verbindung einrichten**, um den Leitfaden zur unterstützten Einrichtung zu starten.
3. Füllen Sie die Felder je nach Bedarf aus.
4. Optional gibt es erweiterte Einstellungen, die die Sicherheit erhöhen und zusätzliche Funktionen ermöglichen, wie z.B. die Bearbeitung von Kundenaufträgen und die Anzeige von Lagerbeständen. Die erweiterten Einstellungen werden in der folgenden Tabelle beschrieben.  

| Feld | Beschreibung |
|--|--|
| **Import Dynamics 365 Sales Lösung** | Aktivieren Sie dies, um die in Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] einzurichten und zu konfigurieren. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
| **Artikelverfügbarkeits-Webdienst veröffentlichen** | Ermöglichen Sie es Personen, die [!INCLUDE[crm_md](includes/crm_md.md)] verwenden, die Verfügbarkeit von Artikeln (Produkten) im Lager in [!INCLUDE[prod_short](includes/prod_short.md)] anzuzeigen. Dies erfordert ein Benutzerkonto [!INCLUDE[prod_short](includes/prod_short.md)] mit einem Webdienst-Zugriffsschlüssel. Das Zuordnen des Schlüssels ist ein Vorgang mit zwei Schritten. Im Benutzerkonto in [!INCLUDE[prod_short](includes/prod_short.md)] müssen Sie die Aktion **Webdienstschlüssel ändern** auswählen. Im Leitfaden für das unterstützte Setup zum Einrichten der Dynamics 365 Sales Verbindung müssen Sie die Dynamics 365 Business Central-OData-Webdienst-URL festlegen und Benutzeranmeldeinformationen für [!INCLUDE[prod_short](includes/prod_short.md)] zum Aufrufen des Diensts bereitstellen. Weitere Informationen finden Sie unter [Odata-Webservice](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
| **Business Central-OData-Webdienst-URL** | Wenn Sie den Webdienst für die Anzeige der Verfügbarkeit von Artikeln aktivieren, wird Ihnen die URL für den OData Webdienst zur Verfügung gestellt. |
| **Business Central-OData-Webdienst-Benutzername** | Der Name des Benutzerkontos [!INCLUDE[prod_short](includes/prod_short.md)], das [!INCLUDE[crm_md](includes/crm_md.md)] verwendet, um Informationen über die Verfügbarkeit von Artikeln in [!INCLUDE[prod_short](includes/prod_short.md)] über den OData-Webdienst abzurufen. |
| **Business Central-OData-Webdienst-Zugriffsschlüssel** | Der Zugriffsschlüssel für das Benutzerkonto, das [!INCLUDE[crm_md](includes/crm_md.md)] benutzt, um Informationen über die Verfügbarkeit von [!INCLUDE[prod_short](includes/prod_short.md)] über den OData-Webdienst zu erhalten. Der Schlüssel wird dem Benutzer zugewiesen, der im Feld **Business Central-OData-Webdienst-Benutzername** gewählt wurde. Um den Schlüssel zu erhalten, wählen Sie die Schaltfläche **Wert suchen** neben dem Benutzernamen, wählen Sie den Benutzer aus, wählen Sie **Verwalten** und dann **Bearbeiten** aus. In der Benutzerkarte wählen Sie **Aktionen**, **Authentifizierung** und dann **Webdienstschlüssel ändern**. |
| **Verkaufsauftragsintegration aktivieren** | Wenn Personen Verkaufsaufträge in [!INCLUDE[crm_md](includes/crm_md.md)] erstellen und Aufträge in [!INCLUDE[prod_short](includes/prod_short.md)] erfüllen, wird dies in den Prozess in [!INCLUDE[crm_md](includes/crm_md.md)] integriert. Weitere Informationen finden Sie unter [Integration für Vertriebsauftragsverarbeitung aktivieren](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Dazu ist es erforderlich, dass Sie Anmeldeinformationen für ein Administratorbenutzerkonto in [!INCLUDE[crm_md](includes/crm_md.md)] zur Verfügung stellen. Weitere Informationen finden Sie im Abschnitt [Verarbeiten von Verkaufsauftragsdaten](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
| **CDS-Verbindung aktivieren** | Aktivieren Sie die Verbindung mit [!INCLUDE[prod_short](includes/cds_long_md.md)]. |
| **Dynamics 365-SDK-Version** | Dies ist nur relevant, wenn Sie eine lokale Version von [!INCLUDE[crm_md](includes/crm_md.md)] integrieren. Das ist das Dynamics 365 Software Development Kit (wird auch als Xrm bezeichnet), das Sie verwenden, um eine Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] herzustellen. Die Version muss mit der SDK-Version kompatibel sein, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird, und der Version von [!INCLUDE[crm_md](includes/crm_md.md)] entsprechen oder neuer sein. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Verbindungseinstellungen auf der Seite Microsoft Dynamics 365 Verbindungsaufbau

Geben Sie die folgenden Informationen über die Verbindung von [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[prod_short](includes/prod_short.md)] ein.

| Feld | Beschreibung |
|--|--|
| **Dynamics 365 Sales URL** | Die URL Ihrer [!INCLUDE[crm_md](includes/crm_md.md)]-Instanz. Dies ermöglicht es Benutzern, entsprechende Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] von Datensätzen in [!INCLUDE[crm_md](includes/crm_md.md)] zu öffnen, wie z.B. ein Konto oder ein Produkt. Die [!INCLUDE[prod_short](includes/prod_short.md)]-Datensätze werden in [!INCLUDE[prod_short](includes/prod_short.md)] geöffnet. |
|**Dynamics 365 Sales URL**|Die URL Ihrer [!INCLUDE[crm_md](includes/crm_md.md)]-Instanz. Dies ermöglicht es Benutzern, entsprechende Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] von Datensätzen in [!INCLUDE[crm_md](includes/crm_md.md)] zu öffnen, wie z.B. ein Konto oder ein Produkt. Die [!INCLUDE[prod_short](includes/prod_short.md)]-Datensätze werden in [!INCLUDE[prod_short](includes/prod_short.md)] geöffnet.|
|**Artikelverfügbarkeits-Webdienst aktiviert**|Ermöglichen Sie es Personen, die [!INCLUDE[crm_md](includes/crm_md.md)] verwenden, die Verfügbarkeit von Artikeln (Produkten) im Lager in [!INCLUDE[prod_short](includes/prod_short.md)] anzuzeigen. Wenn Sie dies aktivieren, müssen Sie auch einen Benutzernamen und einen Zugriffsschlüssel für [!INCLUDE[crm_md](includes/crm_md.md)] angeben, um den OData-Webdienst nach der Verfügbarkeit von Artikeln (Produkten ) abzufragen. Weitere Informationen finden Sie unter [Odata-Webservice](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**Dynamics 365 Business Central-OData-Webdienst-URL**|Wenn Sie den Artikelverfügbarkeits-Webdienst aktivieren, wird Ihnen die URL für den OData-Webdienst bereitgestellt. Legen Sie für dieses Feld die URL der zu verwendenden [!INCLUDE[prod_short](includes/prod_short.md)]-Instanz fest.<br /><br /> Um das Feld zur Standard-URL für [!INCLUDE[prod_short](includes/prod_short.md)] zurückzusetzen, wählen Sie die Aktion **Webclient-URL zurücksetzen** aus.<br /><br /> Dieses Feld ist nur relevant, wenn die [!INCLUDE[prod_short](includes/prod_short.md)]-Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] installiert ist.|
|**Dynamics 365 Business Central-OData-Webdienst-Benutzername**|Der Name des Benutzerkontos, den [!INCLUDE[crm_md](includes/crm_md.md)] verwendet, um Informationen über die Artikelverfügbarkeit aus [!INCLUDE[prod_short](includes/prod_short.md)] über den OData-Webdienst abzurufen.|
|**Dynamics 365 Business Central-OData-Webdienst-Zugriffsschlüssel**|Der Zugriffsschlüssel des Benutzerkontos, das [!INCLUDE[crm_md](includes/crm_md.md)] verwendet, um Informationen über Artikelverfügbarkeit aus [!INCLUDE[prod_short](includes/prod_short.md)] über den OData-Webdienst abzurufen. Der Schlüssel wird dem Benutzer zugeordnet, der im Feld **Dynamics 365 Business Central-OData-Webdienst-Benutzername** ausgewählt ist. Um den Schlüssel zu erhalten, wählen Sie die Schaltfläche **Wert suchen** neben dem Benutzernamen, wählen Sie den Benutzer aus, wählen Sie **Verwalten** und dann **Bearbeiten** aus. In der Benutzerkarte wählen Sie **Aktionen**, **Authentifizierung** und dann **Webdienstschlüssel ändern**.|
|**Dynamics 365-SDK-Version**|Wenn Sie eine Integration in einer lokale Version von [!INCLUDE[crm_md](includes/crm_md.md)] durchführen, verwenden Sie dieses Dynamics 365 Software Development Kit (wird auch als Xrm bezeichnet), um [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] zu verbinden. Die Version, die Sie auswählen, muss mit der SDK-Version kompatibel sein, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird. Diese Version gleicht der Version, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird oder ist neuer.|-->

Zusätzlich zu den oben genannten Einstellungen geben Sie folgende Einstellungen für [!INCLUDE[crm_md](includes/crm_md.md)] ein.

| Feld | Beschreibung |
|--|--|
| **Auftragsintegration ist aktiviert** | Ermöglichen Sie es Benutzern, Verkaufsaufträge und aktivierte Offerten in [!INCLUDE[crm_md](includes/crm_md.md)] zu senden und sie dann in [!INCLUDE[prod_short](includes/prod_short.md)] anzuzeigen und zu bearbeiten. Dies integriert den Prozess in [!INCLUDE[crm_md](includes/crm_md.md)]. Weitere Informationen finden Sie unter [Integration für Vertriebsauftragsverarbeitung aktivieren](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Verkaufsaufträge automatisch erstellen** | Erstellen Sie einen Verkaufsauftrag in [!INCLUDE[prod_short](includes/prod_short.md)], wenn ein Benutzer einen in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt und sendet. |
| **Verkaufsofferten automatisch verarbeiten** | Verarbeiten Sie eine Verkaufsofferte in [!INCLUDE[prod_short](includes/prod_short.md)], wenn ein Benutzer eine in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt und aktiviert. |

<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Standard-Sales-Entitätszuordnungen für die Synchronisierung

Entitäten in [!INCLUDE[crm_md](includes/crm_md.md)], wie z.B. Bestellungen, werden mit äquivalenten Typen von Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] integriert, wie z.B. Debitorenaufträge. Um mit [!INCLUDE[crm_md](includes/crm_md.md)]-Daten zu arbeiten, richten Sie Verknüpfungen, auch Kopplungen genannt, zwischen Tabellen in [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] ein.

Die folgende Tabelle zeigt die standardmässige Zuordnung zwischen Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[prod_short](includes/prod_short.md)], die [!INCLUDE[crm_md](includes/crm_md.md)] bietet.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synchronisierungsrichtung | Standardfilter |
|--|--|--|--|
| Masseinheit | Einheiten-Gruppe | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Artikel | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Vertriebskontaktfilter: **Produkt-Typ** ist **Verkaufs-Lager** |
| Ressource | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Vertriebskontaktfilter: **Produkt-Typ** ist **Service** |
| Debitorenpreisgruppe | VK-Preisliste | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkaufspreis | Produkt-Preisliste | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] Kontaktfilter: **Verkaufscode** ist nicht leer, **Verkaufsart** ist **Debitorenpreisgruppe** |
| Verkaufschance | Verkaufschance | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Verkaufsrechnungskopf | Fakturieren | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkaufsrechnungszeile | Rechnungsprodukt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkaufsauftrags-Kopf | Verkaufsauftrag | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)]Verkaufskopffilter: **Dokumentart** ist Auftrag. **Status** ist freigegeben |
| Hinweise zu Verkaufsaufträgen | Hinweise zu Verkaufsaufträgen | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

### <a name="synchronization-rules"></a>Synchronisierungsregeln

Die folgende Tabelle listet die Regeln auf, die die Synchronisation zwischen [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] steuern. Diese kommen zu den für Dataverse definierten Regeln hinzu, die ebenfalls gelten. Weitere Informationen finden Sie unter [Standard-Entitätszuordnung für die Synchronisation](/dynamics365/business-central/admin-synchronizing-business-central-and-sales?branch=master-cds-crm#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Änderungen an Daten, die vom Integrationsbenutzerkonto vorgenommen wurden, werden nicht synchronisiert. Daher empfiehlt es sich, bei der Nutzung dieses Kontos keine Daten zu ändern. Weitere Informationen finden Sie unter [Einrichten des Benutzerkontos für die Integration in Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tabelle|Regel|
|-----|----|
|Masseinheiten|Masseinheiten werden mit Einheitengruppen in [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert. Es kann nur eine Einheit in der Einheitengruppe definiert sein.|
|Artikel|Wenn Artikel mit [!INCLUDE[crm_md](includes/crm_md.md)]-Produkten synchronisiert werden, erstellt [!INCLUDE[prod_short](includes/prod_short.md)] automatisch eine Preisliste in [!INCLUDE[crm_md](includes/crm_md.md)]. Um Synchronisationsfehler zu vermeiden, sollten Sie diese Preisliste nicht manuell ändern.|
|Ressourcen|Ressourcen werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Produkten synchronisiert, die den Produkttyp-Service haben.|
|Debitorenpreisgruppen|Debitorenpreisgruppen werden mit Verkaufspreislisten synchronisiert.|
|Verkaufspreise|Verkaufspreise, die Verkaufsart Debitorenpreisgruppe haben und einen definierten Verkaufscode haben werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Preislistenzeilen synchronisiert|
|Verkaufschancen|Chancen werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Chancen synchronisiert. Der Verkäufer-Codewert definiert den Besitzer der gekoppelten Tabelle in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Gebuchte Verkaufsrechnungen|Gebuchte Verkaufsrechnungen werden mit Verkaufsrechnungen synchronisiert. Bevor eine Rechnung synchronisiert werden kann, ist es besser, alle anderen Tabellen, die in der Rechnung teilnehmen können, von Verkäufer zu Preislisten zu synchronisieren. Der Verkäufer-Codewert im Rechnungskopf definiert den Besitzer der gekoppelten Tabelle im Verkauf.|
|Verkaufsaufträge|Wenn die Verkaufsauftragsintegration aktiviert ist, werden Verkaufsaufträge in [!INCLUDE[prod_short](includes/prod_short.md)], die aus übermittelten Verkaufsaufträgen in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt werden, mit Verkaufsaufträgen in INCLUDE SALES synchronisiert, wenn sie freigegeben werden. Vor dem Synchronisieren von Aufträgen wird empfohlen, zunächst alle an dem Auftrag beteiligten Tabellen zu synchronisieren, z. B. Verkäufer und Preislisten. Das Verkäufer-Codefeld im Auftragskopf definiert den Besitzer der gekoppelten Tabelle in [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Synchronisierungsaufträge für eine Vertriebsintegration

Die Jobs werden in der folgenden Reihenfolge ausgeführt, um Kopplungsabhängigkeiten zwischen Tabellen zu vermeiden. Bei Dataverse sind zusätzliche Aufträge verfügbar. Weitere Informationen finden Sie unter [Projektwarteschlangen nutzen, um Aufgaben zu planen](/dynamics365/business-central/admin-job-queues-schedule-tasks)

1. UNITOFMEASURE - Dynamics 365 Sales Synchronisierungsauftrag  
2. RESSOURCE-PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag  
3. ARTIKEL - PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag  
4. CUSTPRCGRP-PRICE- Synchronisierungsauftrag „Dynamics 365 Sales“.
5. SALESPRC-PRODPRICE - Synchronisierungsauftrag „Dynamics 365 Sales“.
6. POSTEDSALESINV-INV - Dynamics 365 Sales-Synchronisierungsauftrag.

### <a name="default-synchronization-job-queue-entries"></a>Standardmässige Synchronisierungsprojektwarteschlangenposten

Die folgende Tabelle beschreibt die Standardsynchronisierungsjobs für Sales.  

|Aufgabenwarteschlangenposten|Beschreibung|Richtung|Integrationstabellenzuordnung|Standard-Synchronisationsfrequenz (Minuten)|Standard-Inaktivitätsruhezustand (Minuten)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|UNITOFMEASURE - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Einheitsgruppen mit [!INCLUDE[prod_short](includes/prod_short.md)]-Masseinheiten.|Von [!INCLUDE[prod_short](includes/prod_short.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|MASSEINHEIT|30|720<br> (12 Std.)|
|RESSOURCE-PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produkte mit [!INCLUDE[prod_short](includes/prod_short.md)]-Ressourcen.|Von [!INCLUDE[prod_short](includes/prod_short.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE – PRODUKT|30|720<br> (12 Std.)|
|ARTIKEL - PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produkte mit [!INCLUDE[prod_short](includes/prod_short.md)]-Artikeln.|Von [!INCLUDE[prod_short](includes/prod_short.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL/PRODUKT|30|1440<br> (24 Std.)|
|CUSTPRCGRP-PREIS - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Verkaufspreislisten mit [!INCLUDE[prod_short](includes/prod_short.md)]-Debitorenpreisgruppen.| |DEBITORENPREISGRUPPEN – VERKAUFSPREISLISTEN|30|1440<br> (24 Std.)|
|SALESPRC-PRODUCTPRICE - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produktpreise mit [!INCLUDE[prod_short](includes/prod_short.md)]-Verkaufspreisen.||PRODUKTPREIS – VERKAUFSPREIS|30|1440<br> (24 Std.)|
|POSTEDSALESINV-INV - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Rechnungen mit gebuchten [!INCLUDE[prod_short](includes/prod_short.md)]-Verkaufsrechnungen.|Von [!INCLUDE[prod_short](includes/prod_short.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|RECHNUNGEN – GEBUCHTE VERKAUFSRECHNUNGEN|30|1440<br> (24 Std.)|
|Debitorenstatistik - Dynamics 365 Sales Synchronisierungsauftrag|Aktualisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Konten mit den neuesten [!INCLUDE[prod_short](includes/prod_short.md)]-Debitorendaten. In [!INCLUDE[crm_md](includes/crm_md.md)] erscheinen diese Informationen im **Business Central-Kontostatistik**-Schnellansichtsformular von Konten, die mit [!INCLUDE[prod_short](includes/prod_short.md)]-Debitoren gekoppelt werden.<br /><br /> Diese Daten können auch manuell für jeden Debitorendatensatz aktualisiert werden. Weitere Informationen finden Sie unter [Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Hinweis:** Dieser Projektwarteschlangeneintrag ist nur relevant, wenn die [!INCLUDE[prod_short](includes/prod_short.md)]-Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] installiert ist. |Nicht anwendbar|Nicht anwendbar|30|Nicht anwendbar| 

## <a name="connecting-business-central-on-premises-versions-earlier-than-version-16"></a>Die lokalen Business Central Versionen vor Version 16 verbinden
Das Microsoft Power Platform Team hat [angekündigt](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse), dass der Office365-Authentifizierungstyp nicht mehr unterstützt wird. Wenn Sie die lokale Version von [!INCLUDE[prod_short](includes/prod_short.md)] verwenden, die älter als Version 16 ist, müssen Sie den OAuth-Authentifizierungstyp verwenden, um eine Verbindung online zu [!INCLUDE[crm_md](includes/crm_md.md)] herzustellen. Die Schritte in diesem Abschnitt beschreiben, wie die Verbindung hergestellt wird.

### <a name="requirements"></a>Anforderungen
Sie müssen ein Microsoft Azure Abonnement haben. Ein Testkonto funktioniert für die Registrierung von Anträgen.

### <a name="to-connect-a-version-of-business-central-earlier-than-version-16"></a>zum verbinden der lokalen Business Central Versionen vor Version 16
1. Importieren Sie Microsoft Dynamics 365 Business Central Integrationslösung in Ihre [!INCLUDE[crm_md](includes/crm_md.md)] Umgebung. Die Integrationslösung ist im Ordner CrmCustomization auf Ihrer Business Central-Installations-DVD verfügbar. Es gibt mehrere Versionen der Lösung, z. B. DynamicsNAVIntegrationSolution_v8 oder DynamicsNAVIntegrationSolution_v9 oder DynamicsNAVIntegrationSolution_v91. Die Lösung, die Sie importieren sollten, hängt von der Version von [!INCLUDE[crm_md](includes/crm_md.md)] ab, mit der Sie sich verbinden. [!INCLUDE[crm_md](includes/crm_md.md)] online erfordert die DynamicsNAVIntegrationSolution_v91 Integrationslösung.
2. Erstellen Sie einen nicht interaktiven Integrationsbenutzer in Ihrer [!INCLUDE[crm_md](includes/crm_md.md)] Umgebung, und weisen Sie dem Benutzer die folgenden Sicherheitsrollen zu. Weitere Informationen finden Sie unter [Erstellen eines nicht interaktiven Benutzerkontos](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central Integrations-Administrator
   * Dynamics 365 Business Central Integration Benutzer

   > [!Important]
   > Dieser Benutzer darf nicht über die Sicherheitsrolle des Systemadministrators verfügen. Sie können das Systemadministratorkonto auch nicht als Integrationsbenutzer verwenden.

3.  Im Azure Portal erstellen Sie eine App-Registrierung für [!INCLUDE[prod_short](includes/prod_short.md)]. Weitere Informationen zu den Schritten finden Sie unter [Registrieren Sie eine Anwendung in Azure Active Directory](/business-central/dev-itpro/administration/register-app-azure?branch=live#register-an-application-in-azure-active-directory). Die Einstellungen, für die eine Verbindung hergestellt werden soll mit [!INCLUDE[crm_md](includes/crm_md.md)] sind die delegierten Berechtigungen. In der folgenden Tabelle sind die Mindestberechtigungen beschrieben.

   |API/Berechtigungsname |Art  |Beschreibung  |
   |---------|---------|---------|
   |Financials.ReadWrite.All     |Stellvertretend|Für [!INCLUDE[prod_short](includes/prod_short.md)] erforderlich.    |
   |user_impersonation     |Stellvertretend|Für [!INCLUDE[crm_md](includes/crm_md.md)] erforderlich.|
   
4. In [!INCLUDE[prod_short](includes/prod_short.md)] suchen Sie nach **Microsoft Dynamics 365 Verbindung einrichten** und wählen Sie dann den entsprechenden Link. 
5. Auf der Seite **Microsoft Dynamics 365 Verbindung einrichten** im Feld **Authentifizierungsart** wählen Sie im Feld die Option für OAuth. 
6. Wählen Sie die CRM SDK-Version aus, die der in Schritt 1 importierten Lösungsversion entspricht.
7. In dem Feld **Serveradresse** geben Sie die URL Ihrer [!INCLUDE[crm_md](includes/crm_md.md)] Umgebung ein und geben Sie dann den Benutzernamen und das Kennwort für den Integrationsbenutzer ein.
8. In dem Feld **Verbindungszeichenfolge** geben Sie im Feld die ID der App-Registrierung an. Dieses Feld enthält zwei Token, in denen die ID Ihrer Anwendung angegeben werden soll.

   |Token           |Beschreibung  |
   |----------------|-------------|
   |**appId**       |Stellen Sie die Anwendungs-ID ein.      |
   |**Umleitungs-URL** |Stellen Sie die Anwendungs-ID ein, fügen Sie jedoch den **App: //** Präfix hinzu.         |

    **Beispiel** Das folgende Beispiel zeigt eine Verbindungszeichenfolge.

    ```
    AuthType=OAuth;Username=jsmith@contoso.onmicrosoft.com;Password=****;Url=https://contosotest.crm.dynamics.com;AppId=<your AppId>;RedirectUri=app://<your AppId>;TokenCacheStorePath=;LoginPrompt=Auto
    ```
9. Aktivieren Sie die Verbindung.

> [!Note]
> Wenn Sie eine lokale Instanz mit [!INCLUDE[crm_md](includes/crm_md.md)] mit einem bestimmten Authentifizierungstyp konfigurieren möchten, füllen Sie die Felder im Inforegister **Authentifizierungstyp-Details** aus. Weitere Informationen finden Sie unter [Verwenden der Verbindungszeichenfolgen in XRM-Tooling zum herstellen einer Verbindung mit Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Dieser Schritt ist nicht erforderlich, wenn sie eine Verbindung mit einer Onlineversion von [!INCLUDE[prod_short](includes/prod_short.md)] herstellen.

## <a name="see-also"></a>Siehe auch

[Einrichten des Benutzerkontos für die Integration in [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Richten Sie eine Verbindung mit [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md) ein  
[Synchronisieren von Business Central und [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Vorbereiten der Integration in Dynamics 365 Sales für die lokale Integration](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]