---
title: 'Designdetails: Fibu-Erf.-Journal-Buchungszeile - Überblick | Microsoft Docs'
description: Diese Dokumentation stellt einen detaillierten technischen Einblick in die Urheberrechtshinweise und Prinzipien bereit, die verwendet werden, um die Finanzbuchhaltungs-Buchungsfunktion in Business Central neu zu gestalten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 337f1e679ba2f0b1fcfc0ceb8b3f0ea45ca86ecc
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "935650"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="66abd-103">Designdetails: Fibu Erf.-Journal-Beitrags-Zeile</span><span class="sxs-lookup"><span data-stu-id="66abd-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="66abd-104">Diese Dokumentation stellt einen detaillierten technischen Einblick in die Urheberrechtshinweise und Prinzipien bereit, die verwendet werden, um die Fibu-Erf.-Journal-Buchungsfunktion in [!INCLUDE[d365fin](includes/d365fin_md.md)] neu zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="66abd-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="66abd-105">Die Neukonstruktion macht Codeunit 12 einfacher und einfacher zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="66abd-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="66abd-106">Die Dokumentation beginnt mit der Beschreibung der konzeptionellen Übersichten der Neugestaltung.</span><span class="sxs-lookup"><span data-stu-id="66abd-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="66abd-107">Dann wird die technische Architektur erklärt, um die Änderungen zu zeigen, die sich aus der Neugestaltung ergeben.</span><span class="sxs-lookup"><span data-stu-id="66abd-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="66abd-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="66abd-108">In This Section</span></span>  
[<span data-ttu-id="66abd-109">Fibu-Buchungszeile - Überblick</span><span class="sxs-lookup"><span data-stu-id="66abd-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="66abd-110">Designdetails: Buchungs-Schnittstellenstruktur</span><span class="sxs-lookup"><span data-stu-id="66abd-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="66abd-111">Designdetails: Buchungs-Modul-Struktur</span><span class="sxs-lookup"><span data-stu-id="66abd-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="66abd-112">Codeunit 12 Änderungen: Zuordnen der globalen Variablen für Fibu Erf.-Journal-Beitrags-Zeile</span><span class="sxs-lookup"><span data-stu-id="66abd-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="66abd-113">Codeunit 12 Änderungen: Änderungen in Fibu Erf.-Journal-Beitrags-Verfahren</span><span class="sxs-lookup"><span data-stu-id="66abd-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="66abd-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66abd-114">See Also</span></span>  
<span data-ttu-id="66abd-115">[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)A</span><span class="sxs-lookup"><span data-stu-id="66abd-115">[Working with General Journals](ui-work-general-journals.md)</span></span>
