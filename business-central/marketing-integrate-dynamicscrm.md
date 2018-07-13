---
title: Verwalten von Kunden, die Dynamics 365 for Sales nutzen| Microsoft Docs
description: "Sie können Dynamics 365 for Sales aus  Business Central. nutzen, um Daten zu verknüpfen und eine nahtlose Integration und Synchronisation der führenden Prozesse sicherzustellen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 07/02/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 046a42582dc66368fded90a4bb45add71a95d979
ms.openlocfilehash: 33987f37c170af9982b86baf20f0c3e0682de2cd
ms.contentlocale: de-ch
ms.lasthandoff: 07/02/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a>Die erstellten Debitoren und Verkäufe in Dynamics 365 for Sales verwalten
Wenn Sie Dynamics 365 for Sales (Sales) für Customer Engagement verwenden, können Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] für Prozesse und Finanzen verwenden und eine nahtlose Integration in bargeldlose Prozesse haben.

Wenn Ihre Anwendung für die Integration mit Sales eingerichtet ist, haben Sie Zugriff auf Umsatzdaten von [!INCLUDE[d365fin](includes/d365fin_md.md)] und in einigen Fällen auch umgekehrt. Mit dieser Integration können Sie mit Datentypen, die von beiden Diensten verwendet werden, arbeiten und diese synchronisieren. Dazu zählen etwa Debitoren, Kontakte und Verkaufsinformationen. Ausserdem können Sie die Daten an beiden Lagerorten auf dem aktuellen Stand halten.  

Beispielsweise kann der Verkäufer in Sales die Preislisten aus [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, wenn sie einen Verkaufsauftrag erstellen. Wenn Artikel in der Verkaufsauftragszeile in Sales hinzugefügt werden, sind sie auch in der Lage, den Lagerbestand (Verfügbarkeit) des Artikels anzuzeigen von [!INCLUDE[d365fin](includes/d365fin_md.md)].

Andererseits können Auftragsbearbeiter in [!INCLUDE[d365fin](includes/d365fin_md.md)] die speziellen Eigenschaften aus automatisch oder manuell übertragenen Verkaufsaufträgen von Sales behandeln, wie Verkaufsaufträge für Artikel oder Ressourcen, die in Sales als geschriebene Produkte eingegeben wurden, erstellen und verbuchen. Weitere Informationen finden Sie im Abschnitt "Behandlungs-der speziellen Verkaufsauftrags-Daten".

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] integriert nur mit Dynamics 365 for Sales. Auf andere Anwendungen oder Lösungen in Dynamics 365, die den Standardworkflow oder das Datenmodell in Sales ändern, zum Beispiel, Project Service Automation, können die Integration zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Sales unterbrechen.

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Standard-Sales-Entitätszuordnungen für die Synchronisierung
Sales-Einheiten, wie beispielsweise Konten, werden mit den entsprechenden [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensatztypen, wie beispielsweise Debitoren, integriert. Um mit -Sales-Daten zu arbeiten, richten Sie Kopplungen zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätzen und Sales-Einheitendatensätzen ein. Beispielsweise richten Sie eine Kopplung zwischen einem bestimmten Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] und einem entsprechenden Konto in Sales ein.

In der folgenden Tabelle sind die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensatztypen (Tabellen) und entsprechende Sales-Entitäten aufgeführt, die sofort synchronisiert werden können.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|Verkauf|Synchronisierungsrichtung|Standardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Verkäufer/Einkäufer|Benutzer|Sales -> Business Central|Vertriebskontaktfilter: **Status** ist **Nein**, **Benutzer lizenziert** **Ja** ist, Integrationsbenutzer Modus ist **Nein**|
|Debitor|Konto|Business Central -> Sales and Sales -> Business Central|Sales-Kontenfilter: **Verhältnisart** ist **Kunde** und **Status** ist **Aktiv**.|
|Kontakt|Kontakt|Business Central -> Sales and Sales -> Business Central|Business Central Kontaktfilter: **Art** ist **Person** und der Kontakt wird einem Unternehmen zugewiesen. Sales Kontaktfilter: Kontakt wird einem Unternehmen zugeordnet und die übergeordnete Kundenart ist **Konto**.|
|Währung|Transaktionswährung|Business Central -> Sales| |
|Masseinheit|Einheiten-Gruppe|Business Central -> Sales| |
|Option|Produkt|Business Central -> Sales and Sales -> Business Central|Vertriebskontaktfilter: **Produkt-Typ** ist **Verkaufs-Lager**|
|Ressource|Produkt|Business Central -> Sales and Sales -> Business Central|Vertriebskontaktfilter: **Produkt-Typ** ist **Service**|
|Debitorenpreisgruppe|VK-Preisliste|Business Central -> Sales| |
|Verkaufspreis|Produkt-Preisliste|Business Central -> Sales|Zentraler Kontaktfilter des Geschäfts: **Verkaufscode** ist nicht leer ist **Verkaufsart** ist **Debitorenpreisgruppe**|
|Verkaufschance|Verkaufschance|Business Central -> Sales and Sales -> Business Central| |
|Verkaufsrechnungskopf|Fakturieren|Business Central -> Sales| |
|Verkaufsrechnungszeile|Rechnungsprodukt|Business Central -> Sales| |

Die Verkaufseinheiten und [!INCLUDE[d365fin](includes/d365fin_md.md)] Tabellen aus, die synchronisiert werden, wird durch Tabellenzuordnungsposten in Tabelle 5335, **Integrationstabellenzuordnung** definiert. Sie können die Zuordnungen anzeigen und Filter aus der Seite 5335 **Integrations-Tabellenzuordnung** einrichten. Die Zuordnung zwischen den Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätzen und den Feldern in Sales-Entitäten wird durch Feldzuordnungseinträge in Tabelle 5336 **Integration Feldzuordnung** und zusätzliche Zuordnungslogik definiert.

### <a name="field-mapping-for-the-sales-account-option"></a>Feld-Zuordnung für die Verkaufskonto-Option
Drei Tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] werden den Options-Feldern in der **Konto** Einheit zugeordnet.   

Die Datensätze in der Tabelle, die sich nicht auf die Optionen beziehen, die in der Tabelle vorhanden sind, werden übersprungen. während der Synchronisierung. Das bedeutet, dass das Feld **Option** in Sales leer ist.

Die folgende Tabelle zeigt Zuordnungen der zentralen Tabellen des Geschäfts für das Feld **Option** **Konto** in der Masseinheit an.

|Tisch|Optionsfeld in der Konto-Einheit in Sales|
|----------------------|-------------------------------------------|
|Zahlungsbedingungen|Zahlungsbedingungen|
|Lieferbedingung|Adresse 1: Frachtbedingungen|
|Spediteur|Adresse 1: Versandmethode|

### <a name="synchronization-rules"></a>Synchronisierungsregeln
Die folgende Tabelle beschreibt Regeln, die die Synchronisierung zwischen Business Central Tabellen und Sales-Einheiten steuern.

> [!NOTE]  
> Änderungen an den Daten in Sales, die durch das Sales-Verbindungskonto ausgeführt werden, werden ausgelassen. Die Änderungen werden nicht synchronisiert. Daher wird empfohlen, dass Sie keine Änderungen an Daten mithilfe des Sales-Verbindungskontos vornehmen.

|Tisch|Regel|
|-----|----|
|Debitoren|Bevor ein Kunde mit einem Konto synchronisiert werden kann, muss der Vertriebsmitarbeiter, der dem Kunde zugewiesen ist, mit einem Benutzer in Sales gekoppelt werden. Wenn Sie das Kunden Dynamics 365 for Sales Synchronisierungsprojekt ausführen und wenn Sie es so einrichten, dass neue Datensätze erstellt werden, achten Sie darauf, dass Sie Vertriebsmitarbeiter mit Sales-Benutzern synchronisieren, bevor Sie Kunden mit Sales-Konten synchronisieren. <br /> <br />Das Kunden - Dynamics 365 for Sales Synchronisierungsprojekt synchronisiert nur Sales-Konten, die die Verhältnisart Kunde haben.|
|Kontakte|Nur Kontakte in Sales, die mit einem Konto verknüpft sind, werden in Business Central erstellt. Der Verkäufer-Codewert definiert den Besitzer der gekoppelten Einheit im Verkauf.|
|Währungen|Währungen werden an Transaktionswährungen in Sales basierend auf ISO-Codes gekoppelt. Nur Währungen, die einen Standard-ISO-Code haben, werden mit Transaktionswährungen gekoppelt und synchronisiert.|
|Einheiten|Masseinheiten werden mit Einheitengruppen in Sales synchronisiert. Es kann nur eine Einheit in der Einheitengruppe definiert sein.|
|Arti&kel|Wenn Artikel mit Sales-Produkten synchronisiert werden, erstellt Business Central automatisch eine Preisliste in Sales. Um Synchronisationsfehler zu vermeiden, sollten Sie diese Preisliste nicht manuell ändern.|
|Verkäufer|Verkäufer werden zu den Systembenutzern in Sales gekoppelt. Der Benutzer muss aktiviert werden und lizenziert werden und darf nicht der integrierte Benutzer sein. Die Notiz, dass dies die erste Tabelle ist, die synchronisiert werden muss, weil sie Debitoren, Kontakten, Verkaufschancen und in den Verkaufsrechnungen verwendet wird.|
|Ressourcen|Ressourcen sind mit Verkaufsprodukten synchronisiert, die Produkttyp Service haben.|
|Debitorenpreisgruppen|Debitorenpreisgruppen werden mit Verkaufspreislisten synchronisiert.|
|Verkaufspreise|Verkaufspreise, die Verkaufsart Debitorenpreisgruppe haben und einen definierten Verkaufscode haben, werden mit Verkaufspreislistenzeilen synchronisiert|
|Verkaufschancen|Chancen werden mit Verkaufschancen synchronisiert. Der Verkäufer-Codewert definiert den Besitzer der gekoppelten Einheit im Verkauf.|
|Gebuchte Verkaufsrechnungen|Gebuchte Verkaufsrechnungen werden mit Verkaufsrechnungen synchronisiert. Bevor eine Rechnung synchronisiert werden kann, ist es besser, alle anderen Einheiten, die in der Rechnung teilnehmen können, von Verkäufer zu Preislisten zu synchronisieren. Der Verkäufer-Codewert im Rechnungskopf definiert den Besitzer der gekoppelten Einheit im Verkauf.|

## <a name="setting-up-the-connection"></a>Einrichten der Verbindung
Von der Startseite können Sie auf das unterstützte Setup für **Microsoft Dynamics 365 Verbindungseinrichtung** zugreifen, das Ihnen hilft, den Link einzurichten. Sobald das getan wird, haben Sie eine nahtlose Kopplung Sales-Datensätze mit [!INCLUDE[d365fin](includes/d365fin_md.md)] Datensätzen.  

> [!NOTE]  
>   Das folgende berücksichtigt die unterstützte Einrichtung, aber Sie können dieselben Aufgaben im Fenster **Sales-Verbindungseinrichtung** manuell ausführen.

Im unterstützten Einrichtungshandbuch können Sie auswählen, welche Daten zwischen den beiden Services zu synchronisieren sind. Sie können auch festlegen, dass Sie die vorhandene Lösung in die bestehende Sales-Lösung importieren möchten. In diesem Fall müssen Anmeldeinformationen für ein Administratorkonto angeben.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Richten Sie das Benutzerkonto für das Importieren der Lösung ein
Um eine vorhandene Sales-Lösung zu importieren, verwendet das Einrichtungshandbuch ein Verwaltungskonto. Dieses Konto muss ein gültiger Benutzer in Sales mit den folgenden Sicherheitsrollen sein:

* Systemadministrator  
* Lösungsanpasser  

Weitere Informationen finden Sie unter [Benutzer erstellen und Microsoft Dynamics 365 (online) Sicherheitsrollen zuweisen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) u[Benutzer und Berechtigungen verwalten](ui-how-users-permissions.md).  

Dieses Konto wird nur bei der Einrichtung verwendet. Sobald die Lösung in [!INCLUDE[d365fin](includes/d365fin_md.md)] importiert wurde, wird das Konto nicht mehr erforderlich.

### <a name="setting-up-the-user-account-for-synchronization"></a>Den Benutzer für die Synchronisierung einrichten
Die Integration beruht auf einem freigegebenen Benutzerkonto. In Ihrem Office 365 Abonnement müssen Sie einen dedizierten Benutzer erstellen, der für die Synchronisierung zwischen den beiden Services verwendet wird. Dieses Konto muss bereits ein gültiger Benutzer in Sales sein, aber Sie müssen keine Sicherheitsrollen zum Konto zuordnen, da die Einrichtungshilfe dies für Sie konfigurieren wird. Sie müssen dieses Benutzerkonto einmal oder mehrere Male bei der Einrichtung festlegen, abhängig davon, wie viele Synchronisierungen Sie aktivieren möchten. Weitere Informationen finden Sie unter [Benutzer erstellen in Microsoft Dynamics 365 (online) und  Sicherheitsrollen zuweisen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Wenn Sie die *Artikelverfügbarkeit* aktivieren, muss das Integrationsbenutzerkonto einen Webdienst-Zugangsschlüssel haben. Dies basiert auf zwei Schritten auf der [!INCLUDE[d365fin](includes/d365fin_md.md)] Seite für das Benutzerkonto, Sie müssen Sie die Schaltfläche **Webdienstschlüssel ändern** auswählen und bei der Sales-Verbindungseinrichtung müssen Sie den Benutzer als OData-Webdienstbenutzer angeben.

Wenn Sie *Verkaufsauftragsintegration* aktivieren, müssen Sie einen Benutzer festlegen, der diese Synchronisierung verarbeiten kann - der Integrationsbenutzer oder ein anderes Benutzerkonto.

### <a name="coupling-records"></a>Kopplungsdatensätze
Im unterstützten Einrichtungshandbuch können Sie auswählen, welche Daten zwischen den beiden Services zu synchronisieren sind. Später können Sie die Synchronisierung für bestimmte Arten von Daten einrichten. Dieses wird als *Koppeln* betrachtet und der entsprechende Abschnitt bietet Empfehlungen für das, was Sie berücksichtigen müssen.

Wenn Sie Konten in Sales als Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] anzeigen möchten, müssen Sie die beiden Arten von Datensätzen koppeln. Dies ist nicht sehr kompliziert - öffnen Sie das Fenster **Debitorenliste** in [!INCLUDE[d365fin](includes/d365fin_md.md)], es gibt eine Aktion im Menüband, um diese Daten mit Sales zu koppeln. Dann legen Sie fest, welche [!INCLUDE[d365fin](includes/d365fin_md.md)] Debitoren den Konten in Sales entsprechen.

In bestimmten Bereichen beruht die Funktionalität auf Sie bestimmten Datensätze vor anderen Datensätzen, wie in der folgenden Liste angezeigt:

* Kunden und Konten  
  * Koppelt Verkäufer mit Sales Benutzern zuerst  
* Artikel und Ressourcen  
  * Koppelt Masseinheiten mit Sales Einheitengruppe zuerst  
* Artikel und Ressourcenpreise  
  * Koppelt Kundenpreisgruppen mit Sales-Preisen zuerst  

> [!NOTE]  
>   Wenn Sie Verkaufspreise in Fremdwährungen verwenden, stellen Sie sicher, dass Sie Währungen mit Sales-Transaktionswährungen koppeln.

In Sales hängen Verkaufsaufträge von zusätzlichen Informationen wie Debitoren, Masseinheiten, Währungen, Debitorenpreisgruppen, Artikeln und/oder Ressourcen ab. Damit Verkaufsaufträg nahtlos arbeiten, müssen Sie Debitoren, Masseinheiten, Währungen, Debitorenpreisgruppen, Artikel und/oder Ressourcen zuerst koppeln.

### <a name="synchronizing-records-fully"></a>Datensätze vollständig synchronisieren
Am Ende der unterstützen Einrichtung können Sie die Aktion **Vollständige Synchronisierung ausführen** auswählen, um die Synchronisierung aller Datensätze mit allen [!INCLUDE[d365fin](includes/d365fin_md.md)] Datensätzen mit allen verknüpften Einträgen in den verbundenen Sales-Lösung zu starten. Im Fenster **Überprüfung vollständige CRM-Synchronisierung** wählen Sie die Aktion **Starten** aus. Die Synchronisierung beginnt dann, Aufgaben entsprechend der Abhängigkeiten auszuführen. Beispielsweise werden Währungsdatensätze vor Debitorendatensätze synchronisiert. Die vollständige Synchronisierung wird möglicherweise viel Zeit in Anspruch nehmen und läuft im Hintergrund, damit Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] weiter arbeiten können.

Um den Status aus einzelnen Projekte in einer vollständigen Synchronisierung sicherzustellen, blättern Sie im **Projektwarteschlangenposten-Status** nach unten zum Feld **Um Int. Tabellen-Projekt-Status** oder **Von Int. Tabellen-Projekt-Status** im Fenster **CRM Full Synch. Prüfen**.

Im Fenster **Microsoft Dynamics 365 Verbindungseinrichtung** können Sie Details über sämtliche Synchronisierungen sehen. Von hier können Sie das Fenster **Integrationstabellenzuordnungen** auch öffnen, um Details über die Tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] und in der Sales-Lösung finden, die synchronisiert werden müssen.

## <a name="handling-special-sales-order-data"></a>Auflösen von bestimmten Verkaufsauftrags-Daten
Verkaufsaufträge in Sales werden automatisch übertragen in [!INCLUDE[d365fin](includes/d365fin_md.md)], wenn Sie das Kontrollkästchen **Automatisches Erstellen von Verkaufsaufträgen** im Fenster **Microsoft Dynamics 365 Verbindungseinrichtung** auswählen. In solchen Verkaufsaufträgen wird das **Name** Feld im ursprünglichen Auftrag dem Feld **Externe Belegnummer** im Verkaufsauftrag in [!INCLUDE[d365fin](includes/d365fin_md.md)] übertragen und zugeordnet.

Dies kann auch gehen, wenn der ursprüngliche Verkaufsaufttag geschriebene Produkte enthält, d.h. Artikel oder Ressourcen sind nicht in beiden Produkten erfasst worden. In diesem Fall müssen Sie die Felder**Geschriebenen Produkttyp** und die **Geschriebene Produktnummer** ausfüllen im Fenster **Debitoren & Verkauf Einr.**, damit solche nicht-registrierte Produktverkäufe in einem angegebenen Artikel/einer Ressourcennummer für Finanzanalyse zugeordnet werden.

Wenn die Artikelbeschreibung des ursprünglichen Verkaufsauftrag sehr lang ist, wird eine zusätzliche Verkaufsauftragszeile der Art Bemerkung erstellt, um den Text in dem Verkaufsauftrag festzuhalten[!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Siehe auch
[Marketing & Vertrieb](marketing-relationship-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Sie können auswählen, welche Funktionen angezeigt werden](ui-experiences.md)  
[Benutzer und ihre Berechtigungen verwalten.](ui-how-users-permissions.md)    
[Holen Sie Ihre Organisation und Benutzer zu Dynamics 365 (Online) an Bord](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

