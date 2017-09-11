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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c27c63ae26f2f97dd15d31978b967f6a08dd55b7
ms.contentlocale: de-ch
ms.lasthandoff: 09/11/2017


---
# <a name="logging-changes-in-dynamics-365-for-financials"></a><span data-ttu-id="bead4-103">Änderungen in Dynamics 365 for Financials protokollieren</span><span class="sxs-lookup"><span data-stu-id="bead4-103">Logging Changes in Dynamics 365 for Financials</span></span>
<span data-ttu-id="bead4-104">Sie können die Änderungsanmeldung aktivieren, sodass [!INCLUDE[d365fin](includes/d365fin_md.md)] Sie den Verlauf der Aktivitäten sehen.</span><span class="sxs-lookup"><span data-stu-id="bead4-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="bead4-105">Die Protokollierung basiert auf den erfolgten Änderungen, die an den Daten in den Tabellen vorgenommen wurden, die Sie verfolgen.</span><span class="sxs-lookup"><span data-stu-id="bead4-105">The log is based on changes that are made to data in the tables that you track.</span></span> <span data-ttu-id="bead4-106">Im Änderungsprotokoll sind Posten chronologisch bestellt und zeigt Änderungen an, die in den Feldern der angegebenen Tabellen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="bead4-106">In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="bead4-107">Das Änderungsprotokoll erfasst alle Änderungen, die auf der Tabelle vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="bead4-107">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="bead4-108">Arbeiten mit dem Änderungsprotokoll</span><span class="sxs-lookup"><span data-stu-id="bead4-108">Working with the change log</span></span>
<span data-ttu-id="bead4-109">Ein verbreitetes Problem in einem Finanzsystem ist die Lokalisierung von Fehlern und Änderungen von Daten.</span><span class="sxs-lookup"><span data-stu-id="bead4-109">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="bead4-110">Es könnte alles sein – von einer falschen Kundentelefonnummer bis hin zu einer falschen Buchung in der Finanzbuchhaltung.</span><span class="sxs-lookup"><span data-stu-id="bead4-110">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="bead4-111">Die Änderungsprotokollfunktion ermöglicht die Verfolgung aller direkten Änderungen, die von einem Benutzer an den Daten in der Datenbank vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="bead4-111">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="bead4-112">Sie müssen jede Tabelle und jedes Feld festlegen, die/das die Anwendung protokollieren soll, und dann das Änderungsprotokoll aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bead4-112">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="bead4-113">Sie verwenden das Fenster **Änderungsprotokoll einrichten** zum Aktivieren bzw. Deaktivieren des Änderungsprotokolls.</span><span class="sxs-lookup"><span data-stu-id="bead4-113">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="bead4-114">Wenn Sie das Änderungsprotokoll aktivieren bzw. deaktivieren, wird diese Aktivität protokolliert, sodass Sie immer sehen, welcher Anwender die Protokollierung an- bzw. abgeschaltet hat.</span><span class="sxs-lookup"><span data-stu-id="bead4-114">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="bead4-115">Dies kann nicht abgeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="bead4-115">This cannot be turned off.</span></span>  

<span data-ttu-id="bead4-116">Im Fenster **Änderungsprotokoll einrichten** können Sie definieren, wenn Sie die Aktion **Tabellen** aktivieren, angeben, welche Tabellen und welche Änderungen Sie verfolgen wollen.</span><span class="sxs-lookup"><span data-stu-id="bead4-116">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="bead4-117"> verfolgt auch mehrere Systemtabellen.</span><span class="sxs-lookup"><span data-stu-id="bead4-117"> also tracks a number of system tables.</span></span>

<span data-ttu-id="bead4-118">Wenn Sie das Änderungsprotokoll eingerichtet und aktiviert haben und jemand Daten verändert hat, protokolliert die Anwendung die Änderung in einem **Änderungsprotokollposten**.</span><span class="sxs-lookup"><span data-stu-id="bead4-118">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="bead4-119">Wenn Sie Posten löschen möchten, können Sie die im Fenster **Änderungsprotokollposten löschen** tun, an dem Sie Filter auf Basis Datum und Zeit festlegen können.</span><span class="sxs-lookup"><span data-stu-id="bead4-119">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bead4-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bead4-120">See Also</span></span>
[<span data-ttu-id="bead4-121">Ändern von grundlegenden Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bead4-121">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="bead4-122">Sortieren</span><span class="sxs-lookup"><span data-stu-id="bead4-122">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="bead4-123">Seite oder Bericht suchen verwenden</span><span class="sxs-lookup"><span data-stu-id="bead4-123">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="bead4-124">[Vorgehensweise: Verwalten Sie Benutzer und Berechtigungen](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="bead4-124">[How to: Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="bead4-125">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bead4-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

