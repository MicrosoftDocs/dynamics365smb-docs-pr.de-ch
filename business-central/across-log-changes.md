---
title: "Benutzer-Aktivität in einem Änderungsprotokoll nachverfolgen | Microsoft Docs"
description: "Sie können ein Benutzerprotokoll aktivieren, sodass Sie Aufzeichnungen über sämtliche Änderungen haben, die an den Daten in verfolgten Tabellen vorgenommen werden."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 11/14/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 59afb06e9d43bdadc5ceacf563a9e6faf7439b7b
ms.openlocfilehash: bc56e07a540c24f53b88651ad2b2ff5e1e56a571
ms.contentlocale: de-ch
ms.lasthandoff: 12/05/2018

---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="876f1-103">Protokollieren von Änderungen in Business Central</span><span class="sxs-lookup"><span data-stu-id="876f1-103">Auditing Changes in Business Central</span></span>

<span data-ttu-id="876f1-104">Sie können die Änderungsanmeldung aktivieren, sodass [!INCLUDE[d365fin](includes/d365fin_md.md)] Sie den Verlauf der Aktivitäten sehen.</span><span class="sxs-lookup"><span data-stu-id="876f1-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="876f1-105">Das Protokoll basiert auf Änderungen, die an den Daten in den von Ihnen verfolgten Tabellen vorgenommen werden. Im **Änderungsprotokoll** sind Posten chronologisch bestellt und zeigt Änderungen an, die in den Feldern der angegebenen Tabellen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="876f1-105">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="876f1-106">Das Änderungsprotokoll erfasst alle Änderungen, die auf der Tabelle vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="876f1-106">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="876f1-107">Die Konfiguration eines Benutzers in **Änderungsprotokollposten** ist nicht sichtbar, bis die Sitzung des Benutzers neu gestartet wird, was in folgenden Fällen geschieht:</span><span class="sxs-lookup"><span data-stu-id="876f1-107">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="876f1-108">Die Sitzung war abgelaufen und wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="876f1-108">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="876f1-109">Der Benutzer hat ein anderes Unternehmen oder Rollencenter ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="876f1-109">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="876f1-110">Der Benutzer hat sich an- und wieder angemeldet.</span><span class="sxs-lookup"><span data-stu-id="876f1-110">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="876f1-111">Arbeiten mit dem Änderungsprotokoll</span><span class="sxs-lookup"><span data-stu-id="876f1-111">Working with the Change Log</span></span>

<span data-ttu-id="876f1-112">Ein verbreitetes Problem in einem Finanzsystem ist die Lokalisierung von Fehlern und Änderungen von Daten.</span><span class="sxs-lookup"><span data-stu-id="876f1-112">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="876f1-113">Es könnte alles sein – von einer falschen Kundentelefonnummer bis hin zu einer falschen Buchung in der Finanzbuchhaltung.</span><span class="sxs-lookup"><span data-stu-id="876f1-113">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="876f1-114">Die Änderungsprotokollfunktion ermöglicht die Verfolgung aller direkten Änderungen, die von einem Benutzer an den Daten in der Datenbank vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="876f1-114">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="876f1-115">Sie müssen jede Tabelle und jedes Feld festlegen, die/das die Anwendung protokollieren soll, und dann das Änderungsprotokoll aktivieren.</span><span class="sxs-lookup"><span data-stu-id="876f1-115">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="876f1-116">Sie verwenden die Seite **Änderungsprotokoll einrichten** zum Aktivieren bzw. Deaktivieren des Änderungsprotokolls.</span><span class="sxs-lookup"><span data-stu-id="876f1-116">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="876f1-117">Wenn Sie das Änderungsprotokoll aktivieren bzw. deaktivieren, wird diese Aktivität protokolliert, sodass Sie immer sehen, welcher Anwender die Protokollierung an- bzw. abgeschaltet hat.</span><span class="sxs-lookup"><span data-stu-id="876f1-117">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="876f1-118">Wenn Sie auf der Seite **Änderungsprotokoll Einrichtung** die Aktion **Tabellen** wählen, können Sie angeben, welche Tabellen auf Änderungen verfolgt werden sollen, und welche Änderungen verfolgt werden sollen. [!INCLUDE[d365fin](includes/d365fin_md.md)] verfolgt auch mehrere Systemtabellen.</span><span class="sxs-lookup"><span data-stu-id="876f1-118">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="876f1-119">Wenn Sie das Änderungsprotokoll eingerichtet und aktiviert haben und jemand Daten verändert hat, protokolliert die Anwendung die Änderung in einem **Änderungsprotokollposten**.</span><span class="sxs-lookup"><span data-stu-id="876f1-119">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="876f1-120">Wenn Sie Posten löschen möchten, können Sie dies auf der Seite **Änderungsprotokollposten löschen** tun, an dem Sie Filter auf Basis Datum und Zeit festlegen können.</span><span class="sxs-lookup"><span data-stu-id="876f1-120">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="876f1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="876f1-121">See Also</span></span>
[<span data-ttu-id="876f1-122">Ändern von grundlegenden Einstellungen</span><span class="sxs-lookup"><span data-stu-id="876f1-122">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="876f1-123">Sortieren</span><span class="sxs-lookup"><span data-stu-id="876f1-123">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="876f1-124">Seite oder Bericht suchen verwenden</span><span class="sxs-lookup"><span data-stu-id="876f1-124">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="876f1-125">[Benutzer und ihre Berechtigungen verwalten](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="876f1-125">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="876f1-126">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="876f1-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

