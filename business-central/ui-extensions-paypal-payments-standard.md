---
title: Nutzung der Paypal-Zahlungs-Standard-Erweiterung| Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Debitoren zu aktivieren, um Zahlungen mit Paypal zu leisten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ac0ee9bb3287542484478daf23877d3e3bebf5f7
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392088"
---
# <a name="the-paypal-payments-standard-extension"></a><span data-ttu-id="41fea-103">Die PayPal Payments Standard-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="41fea-103">The PayPal Payments Standard Extension</span></span>
<span data-ttu-id="41fea-104">Debitoren erfordern regelmässig höheren Debitorenservice, sowohl in Bezug auf Produktqualität wie auch in Bezug auf Lieferungs- und Zahlungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="41fea-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="41fea-105">Mit dem Paypal-Zahlungsstandard-Service erhöhen Sie Ihren Kundenservice.</span><span class="sxs-lookup"><span data-stu-id="41fea-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="41fea-106">Als Alternative zu Zahlungen per Banktransfer oder Kreditkarten können Sie Ihren Debitoren anbieten, über Paypal zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="41fea-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="41fea-107">Wenn Sie eine Verkaufsrechnung oder einen Verkaufsauftrag per E-Mail versenden, hat es einen Paypal-Link im E-Mail-Text und im angefügten PDF-Dokument.</span><span class="sxs-lookup"><span data-stu-id="41fea-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="41fea-108">Wenn der Debitor den Link auswählt, erscheint die Service-Seite für Ihr Paypal-Konto mit den Zahlungsdetails für den Verkauf.</span><span class="sxs-lookup"><span data-stu-id="41fea-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="41fea-109">Der Kunde kann die Rechnung wie jede andere PayPal-Zahlung bezahlen.</span><span class="sxs-lookup"><span data-stu-id="41fea-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="41fea-110">Der Paypal-Zahlungsstandard-Service hat folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="41fea-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="41fea-111">Debitorenzahlungen sind schneller auf Ihrem Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="41fea-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="41fea-112">Debitoren haben mehr Arten, Rechnungen zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="41fea-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="41fea-113">Paypal bietet einen vertrauenswürdigen Zahlungsservice an, den Debitoren gegenüber der Eingabe von Kreditkarteninformationen auf der Websites bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="41fea-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="41fea-114">Paypal bietet mehrere Arten zur Zahlungsabwicklung an, einschliesslich Kreditkartenverarbeitung, Paypal-Konten und andere Quellen.</span><span class="sxs-lookup"><span data-stu-id="41fea-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="41fea-115">Der Paypal-Link kann automatisch allen Verkaufsbelegen oder manuell vom Benutzer hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="41fea-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="41fea-116">Der Paypal-Zahlungsstandard-Service kostet keine Monatsgebühren oder Gebühren für die Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="41fea-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="41fea-117">Da dies eine Erweiterung ist, können Sie den Paypal-Zahlungsstandard-Service einfach aktivieren wenn und wenn Ihr Geschäft sie benötigt.</span><span class="sxs-lookup"><span data-stu-id="41fea-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="41fea-118">Weitere Informationen finden Sie unter [Aktivieren Sie Debitoren-Zahlung durch Paypal](sales-how-enable-payment-service-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="41fea-118">For more information, see [Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="41fea-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41fea-119">See Also</span></span>
<span data-ttu-id="41fea-120">[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="41fea-120">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="41fea-121">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="41fea-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="41fea-122">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="41fea-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]