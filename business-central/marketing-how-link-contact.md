---
title: Kontakte mit Debitoren, Kreditoren und Bankkonten verknüpfen| Microsoft Docs
description: Beschreibt, wie Sie einen Kontakt mit einem Debitor, Kreditor oder einem Bankkonto aus dem gleichen Unternehmen verknüpfen, sodass Sie allgemeine Daten synchronisieren können.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.openlocfilehash: 3db94f55657b08e06a4691b2bd78791da4f26bf5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238336"
---
# <a name="link-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="694b8-103">Synchronisation von Kontakten mit Debitoren, Kreditoren und Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="694b8-103">Link Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="694b8-104">Wenn Sie Kontakt und entweder einen Debitor, Kreditor oder ein Bankkonto für das gleiche Unternehmen haben, können Sie die beiden Einheiten verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="694b8-104">If you have contact and either a customer, vendor, or bank account for the same company, you can link the two entities.</span></span> <span data-ttu-id="694b8-105">Das Verknüpfen der beiden Einheiten ermöglicht Ihnen gemeinsame Daten zu synchronisieren, sodass diese an beiden Stellen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="694b8-105">Linking the two entities enables you to synchronize data that is common so that it is the same in both places.</span></span>

## <a name="link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a><span data-ttu-id="694b8-106">Verknüpfen eines Kontakts mit einem vorhanden Debitor, Kreditor oder Bankkonto</span><span class="sxs-lookup"><span data-stu-id="694b8-106">Link a Contact to an Existing Customer, Vendor, or Bank Account</span></span>
1. <span data-ttu-id="694b8-107">Öffnen Sie den Kontakt, den Sie verknüpfen möchten.</span><span class="sxs-lookup"><span data-stu-id="694b8-107">Open the contact that you want to link.</span></span>
2. <span data-ttu-id="694b8-108">Wählen Sie die Aktion **Mit vorhandenem verknüpfen** aus, und wählen Sie dann **Debirot**, **Kreditor** oder **Bank**.</span><span class="sxs-lookup"><span data-stu-id="694b8-108">Choose the **Link with existing** action, and then choose **Customer**, **Vendor**, or **Bank**.</span></span>
3. <span data-ttu-id="694b8-109">Wählen Sie den Debitor, Kreditor oder das Bankkonto für die Verknüpfung aus.</span><span class="sxs-lookup"><span data-stu-id="694b8-109">Select the customer, vendor, or bank account to link to.</span></span>

   <span data-ttu-id="694b8-110">Legen Sie im Feld **Felder übernehmen von** fest, welche Felder im Konfliktfall Priorität haben sollen.</span><span class="sxs-lookup"><span data-stu-id="694b8-110">In the **Current Master Fields**, you specify which fields should prioritize in case of conflicting information in fields common to the contact and customer, vendor, or account.</span></span> <span data-ttu-id="694b8-111">Wenn sich z. B. der Verkäufercode im Kontakt von dem des Kredtors unterscheidet, können Sie entscheiden, dass die gültige Information aus dem Kontakt übernommen werden soll, indem Sie **Kontakt** auswählen.</span><span class="sxs-lookup"><span data-stu-id="694b8-111">For example, if the salesperson code is different in the contact than the customer, you can decide, by selecting **Contact**, to use the information in the contact.</span></span>

## <a name="see-also"></a><span data-ttu-id="694b8-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="694b8-112">See Also</span></span>
[<span data-ttu-id="694b8-113">Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten</span><span class="sxs-lookup"><span data-stu-id="694b8-113">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="694b8-114">Erstellen und Verwalten von Kontakten</span><span class="sxs-lookup"><span data-stu-id="694b8-114">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="694b8-115">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="694b8-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
