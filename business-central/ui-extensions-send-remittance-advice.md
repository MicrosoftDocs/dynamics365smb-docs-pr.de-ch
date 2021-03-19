---
title: Buchen Sie Zahlungsanzeige-Erweiterung | Microsoft Docs
description: Beschreibt das Senden der Zahlungsanzeigeerweiterung, die das Buchen und das Neuversenden der Zahlungsanzeige aus dem Zahlungsausgangs Erf.-Journal und den Kreditorenposten zulassen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e0868a5919f82af9d19dbd692c8d27577e64b6b0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376976"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="b8797-103">Rimesseavis senden</span><span class="sxs-lookup"><span data-stu-id="b8797-103">Send Remittance Advice</span></span>

<span data-ttu-id="b8797-104">Wenn Zahlungsanzeigen verwendet werden, um Kreditoren über die Zahlungen zu benachrichtigen, die erstellt werden, können Sie Zahlungsanzeige als Massenvorgang aus dem Zahlungsausgangs-Erf.-Journal buchen und erneut senden, nachdem die Zahlungen von Kreditorenposten getätigt werden, indem Sie Belegsendeprofile verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8797-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="b8797-105">Diese Funktionalität wird nur in Business Central online und lokal in folgenden Ländern unterstützt: Grossbritannien, USA, Kanada, Australien Neuseeland, und Südafrika.</span><span class="sxs-lookup"><span data-stu-id="b8797-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="b8797-106">Sie können Zahlungsanzeigen auf zwei verschiedene Arten senden:</span><span class="sxs-lookup"><span data-stu-id="b8797-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="b8797-107">Auf der Seite **Zahlungsausgangs Erf.-Journal** wählen Sie **Zugehörig**, **Zahlungen**, **Überweisungsbescheid senden**, um den Überweisungsbescheid für eine oder mehrere Zahlungsausgangs Erfassungsjournalzeilen per E-Mail zu senden.</span><span class="sxs-lookup"><span data-stu-id="b8797-107">In the **Payment Journal** page, choose **Related**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="b8797-108">Wählen Sie auf der Seite **Kreditorenposten** **Aktionen**, **Funktionen**, **Überweisungsbescheid senden** aus, um einen Überweisungsbescheid per E-Mail zu senden, nachdem die Kreditorenzahlungen für einen von mehreren Kreditorenposten gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="b8797-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="b8797-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8797-109">See Also</span></span>

[<span data-ttu-id="b8797-110">Zahlungsvorschlag</span><span class="sxs-lookup"><span data-stu-id="b8797-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="b8797-111">[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="b8797-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="b8797-112">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b8797-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b8797-113">Senden von Belegen über E-Mail</span><span class="sxs-lookup"><span data-stu-id="b8797-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]