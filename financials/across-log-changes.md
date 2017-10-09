---
title: "Benutzer-Aktivität in einem Änderungsprotokoll nachverfolgen | Microsoft Docs"
Description: "Sie können ein Benutzerprotokoll aktivieren, sodass Sie Aufzeichnungen über sämtliche Änderungen haben, die an den Daten in verfolgten Tabellen vorgenommen werden."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c27c63ae26f2f97dd15d31978b967f6a08dd55b7
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="logging-changes-in-dynamics-365-for-financials"></a><span data-ttu-id="a84c8-103">Änderungen in Dynamics 365 for Financials protokollieren</span><span class="sxs-lookup"><span data-stu-id="a84c8-103">Logging Changes in Dynamics 365 for Financials</span></span>
<span data-ttu-id="a84c8-104">Sie können die Änderungsanmeldung aktivieren, sodass [!INCLUDE[d365fin](includes/d365fin_md.md)] Sie den Verlauf der Aktivitäten sehen.</span><span class="sxs-lookup"><span data-stu-id="a84c8-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="a84c8-105">Das Protokoll basiert auf Änderungen, die an den Daten in den von Ihnen verfolgten Tabellen vorgenommen werden. Im Änderungsprotokoll sind Posten chronologisch bestellt und zeigt Änderungen an, die in den Feldern der angegebenen Tabellen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="a84c8-105">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="a84c8-106">Das Änderungsprotokoll erfasst alle Änderungen, die auf der Tabelle vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="a84c8-106">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="a84c8-107">Arbeiten mit dem Änderungsprotokoll</span><span class="sxs-lookup"><span data-stu-id="a84c8-107">Working with the change log</span></span>
<span data-ttu-id="a84c8-108">Ein verbreitetes Problem in einem Finanzsystem ist die Lokalisierung von Fehlern und Änderungen von Daten.</span><span class="sxs-lookup"><span data-stu-id="a84c8-108">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="a84c8-109">Es könnte alles sein – von einer falschen Kundentelefonnummer bis hin zu einer falschen Buchung in der Finanzbuchhaltung.</span><span class="sxs-lookup"><span data-stu-id="a84c8-109">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="a84c8-110">Die Änderungsprotokollfunktion ermöglicht die Verfolgung aller direkten Änderungen, die von einem Benutzer an den Daten in der Datenbank vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="a84c8-110">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="a84c8-111">Sie müssen jede Tabelle und jedes Feld festlegen, die/das die Anwendung protokollieren soll, und dann das Änderungsprotokoll aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a84c8-111">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="a84c8-112">Sie verwenden das Fenster **Änderungsprotokoll einrichten** zum Aktivieren bzw. Deaktivieren des Änderungsprotokolls.</span><span class="sxs-lookup"><span data-stu-id="a84c8-112">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="a84c8-113">Wenn Sie das Änderungsprotokoll aktivieren bzw. deaktivieren, wird diese Aktivität protokolliert, sodass Sie immer sehen, welcher Anwender die Protokollierung an- bzw. abgeschaltet hat.</span><span class="sxs-lookup"><span data-stu-id="a84c8-113">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="a84c8-114">Dies kann nicht abgeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a84c8-114">This cannot be turned off.</span></span>  

<span data-ttu-id="a84c8-115">Wenn Sie im Fenster **Änderungsprotokoll Einrichtung** die Aktion **Tabellen** wählen, können Sie angeben, welche Tabellen auf Änderungen verfolgt werden sollen, und welche Änderungen verfolgt werden sollen. [!INCLUDE[d365fin](includes/d365fin_md.md)] verfolgt auch mehrere Systemtabellen.</span><span class="sxs-lookup"><span data-stu-id="a84c8-115">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="a84c8-116">Wenn Sie das Änderungsprotokoll eingerichtet und aktiviert haben und jemand Daten verändert hat, protokolliert die Anwendung die Änderung in einem **Änderungsprotokollposten**.</span><span class="sxs-lookup"><span data-stu-id="a84c8-116">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="a84c8-117">Wenn Sie Posten löschen möchten, können Sie die im Fenster **Änderungsprotokollposten löschen** tun, an dem Sie Filter auf Basis Datum und Zeit festlegen können.</span><span class="sxs-lookup"><span data-stu-id="a84c8-117">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a84c8-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a84c8-118">See Also</span></span>
[<span data-ttu-id="a84c8-119">Ändern von grundlegenden Einstellungen</span><span class="sxs-lookup"><span data-stu-id="a84c8-119">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="a84c8-120">Sortieren</span><span class="sxs-lookup"><span data-stu-id="a84c8-120">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="a84c8-121">Seite oder Bericht suchen verwenden</span><span class="sxs-lookup"><span data-stu-id="a84c8-121">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="a84c8-122">[Vorgehensweise: Verwalten Sie Benutzer und Berechtigungen](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="a84c8-122">[How to: Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="a84c8-123">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a84c8-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

