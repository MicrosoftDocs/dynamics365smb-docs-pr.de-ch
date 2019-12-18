---
title: Verwalten von Debitoren, die Dynamics 365 Sales verwenden| Microsoft Docs
description: Sie können Dynamics 365 Sales aus Business Central nutzen, um Daten zu verknüpfen und eine nahtlose Integration und Synchronisation der führenden Prozesse sicherzustellen.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 33b2931e14cb7e41cc3e71c327d2237cd8308466
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878211"
---
# <a name="using-dynamics-365-sales-from-business-central"></a>Verwenden von Dynamics 365 Sales von Business Central
Wenn Sie Dynamics 365 Sales for Customer Engagement verwenden, können Sie nahtlose Integration in den Interessent-zu-Geld-Prozess nutzen, indem Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] für Backend-Aktivitäten wie Auftragsverarbeitung, Lagerbestandsverwaltung und Finanzbearbeitung verwenden.

Bevor Sie die Integrationsfunktionen verwenden können, müssen Sie die Verbindung einrichten und Benutzer in [!INCLUDE[crm_md](includes/crm_md.md)] definieren. Weitere Informationen finden Sie unter [Integrieren in Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> In diesen Schritten wird die Integration von Onlineversionen von [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] beschrieben. Informationen zur lokalen Konfiguration finden Sie unter [Dynamics 365 Sales für die Integration vor Ort vorbereiten](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Die Integration der Anwendungen ermöglicht den Zugriff auf Daten in Sales von [!INCLUDE[d365fin](includes/d365fin_md.md)] aus und in einigen Fällen auch umgekehrt. Sie können mit Datentypen, die bei beiden Diensten gleich sind, arbeiten und diese synchronisieren. Dazu zählen etwa Debitoren, Kontakte und Verkaufsinformationen. Ausserdem können Sie die Daten an beiden Anwendungen auf dem aktuellen Stand halten.  

Beispielsweise kann ein Verkäufer in Sales die Preislisten verwenden aus [!INCLUDE[d365fin](includes/d365fin_md.md)] wenn Sie einen Verkaufsauftrag erstellen. Wenn Artikel in der Verkaufsauftragszeile in Sales hinzugefügt werden, sind sie in der Lage, den Lagerbestand (Verfügbarkeit) des Artikels anzuzeigen von [!INCLUDE[d365fin](includes/d365fin_md.md)].

Andererseits können Auftragsbearbeiter in [!INCLUDE[d365fin](includes/d365fin_md.md)] Verkaufsaufträge verarbeiten, die automatisch oder manuell vom Vertrieb übertragen werden. Beispielsweise können sie Verkaufsauftragszeilen für Artikel oder Ressourcen erstellen und buchen, die in Sales als einzutragende Produkten eingegeben wurden. Weitere Informationen finden Sie im Abschnitt [Verarbeiten von Verkaufsauftragsdaten](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] integriert nur mit Dynamics 365 Sales. Andere Dynamics 365, die den Standardworkflow oder das Datenmodell in Sales ändern, zum Beispiel, Project Service Automation, können die Integration zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Sales unterbrechen.

### <a name="coupling-records"></a>Kopplungsdatensätze
Mit dem Leitfaden für das unterstütze Setup können Sie die zu synchronisierenden Daten auswählen. Später können Sie die Synchronisierung für bestimmte Datensätze einrichten. Dies wird als *Kopplung* bezeichnet. Beispielsweise können Sie ein bestimmtes Konto in Sales mit einem bestimmten Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] koppeln. In diesem Abschnitt wird beschrieben, was berücksichtigt werden sollte, wenn Sie Datensätze koppeln.

Wenn Sie Konten in Sales als Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] anzeigen möchten, müssen Sie die beiden Arten von Datensätzen koppeln. Dazu verwenden Sie auf der Listenseite **Debitoren** in [!INCLUDE[d365fin](includes/d365fin_md.md)] die **Kopplung einrichten**-Aktion. Dann legen Sie fest, welche [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitoren den Konten in Sales zugewiesen werden.

Sie können auch ein Konto in Sales erstellen (und koppeln), das zum Beispiel auf einem Debitorendatensatz in [!INCLUDE[d365fin](includes/d365fin_md.md)] basiert, wenn Sie **Konto in Dynamics 365 Sales erstellen** verwenden, oder umgekehrt mithilfe von **Debitor erstellen in [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

Wenn Sie eine Kopplung zwischen zwei Datensätzen einrichten, können Sie manuell anfordern, dass der aktuelle Datensatz, beispielsweise einen Debitor, sofort durch Kontodaten aus Sales (oder aus [!INCLUDE[d365fin](includes/d365fin_md.md)]) mithilfe der **Jetzt synchronisieren**-Aktion überschrieben werden. Die **Jetzt synchronisieren**-Aktion, die fragt, ob Sales oder [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensatzdaten überschrieben werden sollen.

In einigen Fällen müssen Sie projektspezifische Datenbestände vor anderen Datensätzen koppeln, wie in der folgenden Tabelle dargestellt.

|Daten|Was zuerst koppeln|
|-----|----|
|Debitoren und Konten|Verkäufer mit Sales-Benutzern koppeln|
|Artikel und Ressourcen|Masseinheiten mit Sales-Einheitengruppe koppeln|
|Artikel und Ressourcenpreise|Debitorenpreisgruppen mit Verkaufspreisen koppeln|

> [!NOTE]  
> Wenn Ihre Preise oder Debitoren Fremdwährungen verwenden, stellen Sie sicher, dass Sie Währungen mit Sales-Transaktionswährungen koppeln.

In Sales hängen Verkaufsaufträge von Informationen wie Debitoren, Masseinheiten, Währungen, Debitorenpreisgruppen, Artikeln und/oder Ressourcen ab. Damit Verkaufsaufträge arbeiten, müssen Sie Debitoren, Masseinheiten, Währungen, Debitorenpreisgruppen, Artikel und/oder Ressourcen koppeln.

### <a name="fully-synchronizing-records"></a>Datensätze vollständig synchronisieren
Am Ende des Leitfaden für das unterstützte Setup können Sie die Aktion **Vollständige Synchronisierung ausführen** auswählen, um die Synchronisierung aller Datensätze mit allen [!INCLUDE[d365fin](includes/d365fin_md.md)] Datensätzen mit allen verknüpften Einträgen in Sales zu starten. Auf der Seite **Dynamics 365 Sales vollständige Synchronisierung prüfen** wählen Sie die Aktion **Starten** aus. Vollständige Synchronisierung kann einige Zeit dauern, aber Sie können in [!INCLUDE[d365fin](includes/d365fin_md.md)] weiterarbeiten, während sie im Hintergrund ausgeführt wird.

Um den Status aus einzelnen Projekte in einer vollständigen Synchronisierung zu prüfen, wählen Sie auf der Seite **Dynamics 365 Sales vollständigen Synchronisierung prüfen** einen Datensatz, um Details anzeigen. Um den Status der Synchronisierung zu aktualisieren, aktualisieren Sie die Seite.

Auf der Seite **Microsoft Dynamics 365-Verbindungseinrichtung** können Sie Details über sämtliche Synchronisierungen sehen. Von hier können Sie die Seite **Integrationstabellenzuordnungen** auch öffnen, um Details über die Tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] und Sales zu finden, die synchronisiert werden müssen.

## <a name="handling-sales-order-data"></a>Bearbeiten von Verkaufsauftragsdaten
Verkaufsaufträge, die Verkäufer in [!INCLUDE[crm_md](includes/crm_md.md)] einreichen, werden automatisch zu [!INCLUDE[d365fin](includes/d365fin_md.md)] übertragen, wenn Sie das Kontrollkästchen **Verkaufsaufträge automatisch erstellen** auf der Seite **Microsoft Dynamics 365-Verbindungseinrichtung** auswählen.
Alternativ können Sie eingereichte Verkaufsaufträge aus [!INCLUDE[crm_md](includes/crm_md.md)] mithilfe der Aktion **Erstellen in [!INCLUDE[d365fin](includes/d365fin_md.md)]**, die auf der Seite **Verkaufsaufträge - Dynamics 365 for Sales** verfügbar ist, manuell konvertieren.
In solchen Verkaufsaufträgen wird das **Name** Feld im ursprünglichen Auftrag dem Feld **Externe Belegnummer** im Verkaufsauftrag in [!INCLUDE[d365fin](includes/d365fin_md.md)] übertragen und zugeordnet.

Dies kann auch gehen, wenn der ursprüngliche Verkaufsauftrag geschriebene Produkte enthält, d.h. Artikel oder Ressourcen sind nicht in beiden Apps erfasst worden. In diesem Fall müssen Sie die Felder**Geschriebenen Produkttyp** und die **Geschriebene Produktnummer** ausfüllen auf der Seite **Debitoren & Verkauf Einr.**, damit solche nicht-registrierte Produktverkäufe in einem angegebenen Artikel/einer Ressourcennummer für Finanzanalyse zugeordnet werden.

Wenn die Artikelbeschreibung des ursprünglichen Verkaufsauftrags lang ist, wird eine zusätzliche Verkaufsauftragszeile der Art **Bemerkung** erstellt, um den Text in dem Verkaufsauftrag in [!INCLUDE[d365fin](includes/d365fin_md.md)]festzuhalten.

Aktualisierungen der Verkaufsauftrags-Kopffeldern, wie "Letztes Lieferdatum" oder "Gewünschtes Lieferdatum", die der VERKAUFSAUFTRAG-AUFTRAG-**Integrationstabellenzuordnung** zugeordnet sind, werden in regelmässigen Abständen mit [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert. Arbeitsgänge wie das Freigeben eines Verkaufsauftrags und die Lieferung oder Fakturierung eines Verkaufsauftrags werden auf der Verkaufsauftragszeitachse in [!INCLUDE[crm_md](includes/crm_md.md)] gebucht. Weitere Informationen finden Sie unter [Einführung in die Aktivitätsfeeds](/dynamics365/customer-engagement/developer/introduction-activity-feeds).

> [!NOTE]  
> Periodische Synchronisation basierend auf der SALESORDER-ORDER-**Integrationstabellenzuordnung** funktioniert nur, wenn die Verkaufsauftragsintegration aktiviert ist. Weitere Informationen finden Sie unter [Verbinden mit Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md) Nur Verkaufsaufträge, die aus übermittelten Verkaufsaufträgen in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt wurden, werden synchronisiert. Weitere Informationen finden Sie unter [Integration für Vertriebsauftragsverarbeitung aktivieren](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Bearbeiten von Verkaufsangebotsdaten
Verkaufsofferten, die in [!INCLUDE[crm_md](includes/crm_md.md)] aktiviert werden, werden automatisch zu [!INCLUDE[d365fin](includes/d365fin_md.md)] übertragen, wenn Sie das Kontrollkästchen **Automatisches Verarbeiten von Angeboten** auf der Seite **Microsoft Dynamics 365-Verbindungseinrichtung** auswählen.
Alternativ können Sie aktivierte Verkaufsofferten aus [!INCLUDE[crm_md](includes/crm_md.md)] mithilfe der Aktion **Prozess in [!INCLUDE[d365fin](includes/d365fin_md.md)]** auf der Seite **Verkaufsofferte - Dynamics 365 Sales** verwenden.
In solchen Verkaufsofferten wird das **Name**-Feld in der ursprünglichen Offerte dem Feld **Externe Belegnummer** im Verkaufsauftrag in [!INCLUDE[d365fin](includes/d365fin_md.md)] übertragen und zugeordnet. Auch wird das Feld **Gültig bis** beim Offerte übertragen und dem Feld **Offerte gültig bis** auf der Verkaufsofferte in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet.  

Verkaufsofferten unterliegen vielen Überarbeitungen, bis sie abgeschlossen werden. Manuelle und automatische Verarbeitung von Verkaufsangeboten in [!INCLUDE[d365fin](includes/d365fin_md.md)] stellt sicher, dass vorherige Versionen von Verkaufsanfragen archiviert werden, bevor neue Überarbeitungen von Verkaufsanfragen von [!INCLUDE[crm_md](includes/crm_md.md)] verarbeitet werden.

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Behandlung der gebuchten Verkaufsrechnungen, Debitoren-Zahlungen und Statistiken
Nach der Erfüllung eines Verkaufsauftrags, werden dafür Rechnungen erstellt. Wenn Sie Aufträge fakturieren, können Sie gebuchte Verkaufsrechnung übertragen an [!INCLUDE[crm_md](includes/crm_md.md)], wenn Sie das Kontrollkästchen**Rechnung erstellen in [!INCLUDE[crm_md](includes/crm_md.md)]** auf der Seite **Gebuchte Verkaufsrechnungen** auswählen. Gebuchte Rechnungen werden an [!INCLUDE[crm_md](includes/crm_md.md)] mit dem Status **Fakturiert** übertragen.

Sobald Sie die Zahlung des Debitors für die Verkaufsrechnung in [!INCLUDE[d365fin](includes/d365fin_md.md)] erhalten, wird der Verkaufsrechnungsstatus auf **Bezahlt** mit dem **Statusgrund** auf **Teilweise** festgelegt, wenn teilweise bezahlt oder auf **Komplett** festgelegt, wenn vollständig bezahlt, wenn Sie die Aktion **Kontostatistik aktualisieren** auf der Debitorenseite in [!INCLUDE[d365fin](includes/d365fin_md.md)] auswählen. Die Funktion **Kontostatistik aktualisieren** aktualisiert auch Werte wie **Saldo** und **Gesamtverkäufe** in der **Infobox [!INCLUDE[d365fin](includes/d365fin_md.md)] Kontostatistik** in [!INCLUDE[crm_md](includes/crm_md.md)]. Alternativ können Sie geplante Aufträge (Debitoren-Statistik und POSTEDSALESINV-INV) automatisch für beide Vorgänge im Hintergrund ausführen.

## <a name="see-also"></a>Siehe auch
[Integration mit Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Marketing & Vertrieb](marketing-relationship-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funktionen, die angezeigt werden ändern](ui-experiences.md)  
[Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)    
[Überblick über Sales und Verkaufs-Hub](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
