---
title: 'Designdetails: Fibu-Erf.-Journal-Buchungszeile - Überblick | Microsoft Docs'
description: Diese Dokumentation stellt einen detaillierten technischen Einblick in die Urheberrechtshinweise und Prinzipien bereit, die verwendet werden, um die Finanzbuchhaltungs-Buchungsfunktion in Business Central neu zu gestalten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3ea2ea8a4ef5bbdff70346022ee226fd5e26748d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777837"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="273e7-103">Designdetails: Fibu Erf.-Journal-Beitrags-Zeile</span><span class="sxs-lookup"><span data-stu-id="273e7-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="273e7-104">Diese Dokumentation stellt einen detaillierten technischen Einblick in die Urheberrechtshinweise und Prinzipien bereit, die verwendet werden, um die Fibu-Erf.-Journal-Buchungsfunktion in [!INCLUDE[prod_short](includes/prod_short.md)] neu zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="273e7-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="273e7-105">Die Neukonstruktion macht Codeunit 12 einfacher und einfacher zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="273e7-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="273e7-106">Die Dokumentation beginnt mit der Beschreibung der konzeptionellen Übersichten der Neugestaltung.</span><span class="sxs-lookup"><span data-stu-id="273e7-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="273e7-107">Dann wird die technische Architektur erklärt, um die Änderungen zu zeigen, die sich aus der Neugestaltung ergeben.</span><span class="sxs-lookup"><span data-stu-id="273e7-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="273e7-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="273e7-108">In This Section</span></span>  
[<span data-ttu-id="273e7-109">Fibu-Buchungszeile - Überblick</span><span class="sxs-lookup"><span data-stu-id="273e7-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="273e7-110">Designdetails: Buchungs-Schnittstellenstruktur</span><span class="sxs-lookup"><span data-stu-id="273e7-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="273e7-111">Designdetails: Buchungs-Modul-Struktur</span><span class="sxs-lookup"><span data-stu-id="273e7-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="273e7-112">Codeunit 12 Änderungen: Zuordnen der globalen Variablen für Fibu Erf.-Journal-Beitrags-Zeile</span><span class="sxs-lookup"><span data-stu-id="273e7-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="273e7-113">Codeunit 12 Änderungen: Änderungen in Fibu Erf.-Journal-Beitrags-Verfahren</span><span class="sxs-lookup"><span data-stu-id="273e7-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="273e7-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="273e7-114">See Also</span></span>  
[<span data-ttu-id="273e7-115">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="273e7-115">Working with General Journals</span></span>](ui-work-general-journals.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]