---
title: Änderungen prüfen | Microsoft Docs
description: Sie können ein Benutzerprotokoll aktivieren, sodass Sie Aufzeichnungen über sämtliche Änderungen haben, die an den Daten in verfolgten Tabellen vorgenommen werden. Sie können Aktivitäten auch mit bestimmten Arten von Aktivitätsprotokollen verfolgen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 43aea054ce4e66e9108f408d96c2eb491351b382
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304961"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="826eb-104">Protokollieren von Änderungen in Business Central</span><span class="sxs-lookup"><span data-stu-id="826eb-104">Auditing Changes in Business Central</span></span>

<span data-ttu-id="826eb-105">Sie können die Änderungsanmeldung aktivieren, sodass [!INCLUDE[d365fin](includes/d365fin_md.md)] Sie den Verlauf der Aktivitäten sehen.</span><span class="sxs-lookup"><span data-stu-id="826eb-105">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="826eb-106">Das Protokoll basiert auf Änderungen, die an den Daten in den von Ihnen verfolgten Tabellen vorgenommen werden. Im **Änderungsprotokoll** sind Posten chronologisch bestellt und zeigt Änderungen an, die in den Feldern der angegebenen Tabellen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="826eb-106">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="826eb-107">Das Änderungsprotokoll erfasst alle Änderungen, die auf der Tabelle vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="826eb-107">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="826eb-108">Die Konfiguration eines Benutzers in **Änderungsprotokollposten** ist nicht sichtbar, bis die Sitzung des Benutzers neu gestartet wird, was in folgenden Fällen geschieht:</span><span class="sxs-lookup"><span data-stu-id="826eb-108">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="826eb-109">Die Sitzung war abgelaufen und wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="826eb-109">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="826eb-110">Der Benutzer hat ein anderes Unternehmen oder Rollencenter ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="826eb-110">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="826eb-111">Der Benutzer hat sich an- und wieder angemeldet.</span><span class="sxs-lookup"><span data-stu-id="826eb-111">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="826eb-112">Arbeiten mit dem Änderungsprotokoll</span><span class="sxs-lookup"><span data-stu-id="826eb-112">Working with the Change Log</span></span>

<span data-ttu-id="826eb-113">Ein verbreitetes Problem in einem Finanzsystem ist die Lokalisierung von Fehlern und Änderungen von Daten.</span><span class="sxs-lookup"><span data-stu-id="826eb-113">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="826eb-114">Es könnte alles sein – von einer falschen Kundentelefonnummer bis hin zu einer falschen Buchung in der Finanzbuchhaltung.</span><span class="sxs-lookup"><span data-stu-id="826eb-114">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="826eb-115">Die Änderungsprotokollfunktion ermöglicht die Verfolgung aller direkten Änderungen, die von einem Benutzer an den Daten in der Datenbank vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="826eb-115">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="826eb-116">Sie müssen jede Tabelle und jedes Feld festlegen, die/das die Anwendung protokollieren soll, und dann das Änderungsprotokoll aktivieren.</span><span class="sxs-lookup"><span data-stu-id="826eb-116">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="826eb-117">Sie verwenden die Seite **Änderungsprotokoll einrichten** zum Aktivieren bzw. Deaktivieren des Änderungsprotokolls.</span><span class="sxs-lookup"><span data-stu-id="826eb-117">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="826eb-118">Wenn Sie das Änderungsprotokoll aktivieren bzw. deaktivieren, wird diese Aktivität protokolliert, sodass Sie immer sehen, welcher Anwender die Protokollierung an- bzw. abgeschaltet hat.</span><span class="sxs-lookup"><span data-stu-id="826eb-118">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="826eb-119">Wenn Sie auf der Seite **Änderungsprotokoll Einrichtung** die Aktion **Tabellen** wählen, können Sie angeben, welche Tabellen auf Änderungen verfolgt werden sollen, und welche Änderungen verfolgt werden sollen. [!INCLUDE[d365fin](includes/d365fin_md.md)] verfolgt auch mehrere Systemtabellen.</span><span class="sxs-lookup"><span data-stu-id="826eb-119">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="826eb-120">Wenn Sie das Änderungsprotokoll eingerichtet und aktiviert haben und jemand Daten verändert hat, protokolliert die Anwendung die Änderung in einem **Änderungsprotokollposten**.</span><span class="sxs-lookup"><span data-stu-id="826eb-120">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="826eb-121">Wenn Sie Posten löschen möchten, können Sie dies auf der Seite **Änderungsprotokollposten löschen** tun, an dem Sie Filter auf Basis Datum und Zeit festlegen können.</span><span class="sxs-lookup"><span data-stu-id="826eb-121">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="working-with-activity-logs"></a><span data-ttu-id="826eb-122">Arbeiten mit Aktivitätsprotokollen</span><span class="sxs-lookup"><span data-stu-id="826eb-122">Working with Activity Logs</span></span>

<span data-ttu-id="826eb-123">Von einigen Seiten in [!INCLUDE [prodshort](includes/prodshort.md)] können Sie ein Aktivitätsprotokoll anzeigen, in dem der Status und alle Fehler von Dateien angezeigt werden, aus denen Sie exportieren oder in die Sie importieren [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="826eb-123">From some pages in [!INCLUDE [prodshort](includes/prodshort.md)], you can view an activity log that shows the status and any errors from files that you export from or import into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

<span data-ttu-id="826eb-124">Die Informationen werden auf der Seite **Aktivitätsprotokoll** angezeigt, entsprechend dem Kontext, aus dem sie geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="826eb-124">The information is displayed in the **Activity Log** page, according to the context that it is opened from.</span></span> <span data-ttu-id="826eb-125">Sie können das Fenster beispielsweise von den Seiten **Belegaustauschservice einrichten**, **eingehende Belege**, **Gebuchte Verkaufsrechnung**, und **Gebuchte Verkaufsgutschrift**.</span><span class="sxs-lookup"><span data-stu-id="826eb-125">You can open the window from the **Document Exchange Service Setup**, **Incoming Document**, **Posted Sales Invoice**, and **Posted Sales Credit Memo** pages, for example.</span></span> <span data-ttu-id="826eb-126">Sie können die Liste der Protokolleinträge leeren oder die Liste der Einträge löschen, die älter als 7 Tage sind.</span><span class="sxs-lookup"><span data-stu-id="826eb-126">You can empty the list of log entries, or just clear the list of entries older than 7 days.</span></span>  

## <a name="see-also"></a><span data-ttu-id="826eb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="826eb-127">See Also</span></span>
[<span data-ttu-id="826eb-128">Ändern von grundlegenden Einstellungen</span><span class="sxs-lookup"><span data-stu-id="826eb-128">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="826eb-129">Sortieren</span><span class="sxs-lookup"><span data-stu-id="826eb-129">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="826eb-130">Suchen von Seiten und Informationen mit Wie möchten Sie weiter verfahren</span><span class="sxs-lookup"><span data-stu-id="826eb-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="826eb-131">[Benutzer und ihre Berechtigungen verwalten](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="826eb-131">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="826eb-132">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="826eb-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
