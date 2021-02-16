---
title: Buchen Sie Zahlungsanzeige-Erweiterung | Microsoft Docs
description: Beschreibt das Senden der Zahlungsanzeigeerweiterung, die das Buchen und das Neuversenden der Zahlungsanzeige aus dem Zahlungsausgangs Erf.-Journal und den Kreditorenposten zulassen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3ae8d131b714b0d7ffb60727d1a991cd6e4ab692
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757081"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="c0e3f-103">Rimesseavis senden</span><span class="sxs-lookup"><span data-stu-id="c0e3f-103">Send Remittance Advice</span></span>

<span data-ttu-id="c0e3f-104">Wenn Zahlungsanzeigen verwendet werden, um Kreditoren über die Zahlungen zu benachrichtigen, die erstellt werden, können Sie Zahlungsanzeige als Massenvorgang aus dem Zahlungsausgangs-Erf.-Journal buchen und erneut senden, nachdem die Zahlungen von Kreditorenposten getätigt werden, indem Sie Belegsendeprofile verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0e3f-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="c0e3f-105">Diese Funktionalität wird nur in Business Central online und lokal in folgenden Ländern unterstützt: Grossbritannien, USA, Kanada, Australien Neuseeland, und Südafrika.</span><span class="sxs-lookup"><span data-stu-id="c0e3f-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="c0e3f-106">Sie können Zahlungsanzeigen auf zwei verschiedene Arten senden:</span><span class="sxs-lookup"><span data-stu-id="c0e3f-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="c0e3f-107">Auf der Seite **Zahlungsausgangs Erf.-Journal** wählen Sie **Zugehörig**, **Zahlungen**, **Überweisungsbescheid senden**, um den Überweisungsbescheid für eine oder mehrere Zahlungsausgangs Erfassungsjournalzeilen per E-Mail zu senden.</span><span class="sxs-lookup"><span data-stu-id="c0e3f-107">In the **Payment Journal** page, choose **Related**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="c0e3f-108">Wählen Sie auf der Seite **Kreditorenposten** **Aktionen**, **Funktionen**, **Überweisungsbescheid senden** aus, um einen Überweisungsbescheid per E-Mail zu senden, nachdem die Kreditorenzahlungen für einen von mehreren Kreditorenposten gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="c0e3f-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="c0e3f-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0e3f-109">See Also</span></span>

[<span data-ttu-id="c0e3f-110">Zahlungsvorschlag</span><span class="sxs-lookup"><span data-stu-id="c0e3f-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="c0e3f-111">[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c0e3f-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="c0e3f-112">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c0e3f-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c0e3f-113">Senden von Belegen über E-Mail</span><span class="sxs-lookup"><span data-stu-id="c0e3f-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
