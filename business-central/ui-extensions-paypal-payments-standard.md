---
title: Nutzung der Paypal-Zahlungs-Standard-Erweiterung| Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Debitoren zu aktivieren, um Zahlungen mit Paypal zu leisten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 6aa3eec4afc365789b1fd85d64781593156ba068
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "819683"
---
# <a name="the-paypal-payments-standard-extension"></a><span data-ttu-id="897b7-103">Die PayPal Payments Standard-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="897b7-103">The PayPal Payments Standard Extension</span></span>
<span data-ttu-id="897b7-104">Debitoren erfordern regelmässig höheren Debitorenservice, sowohl in Bezug auf Produktqualität wie auch in Bezug auf Lieferungs- und Zahlungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="897b7-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="897b7-105">Mit dem Paypal-Zahlungsstandard-Service erhöhen Sie Ihren Kundenservice.</span><span class="sxs-lookup"><span data-stu-id="897b7-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="897b7-106">Als Alternative zu Zahlungen per Banktransfer oder Kreditkarten können Sie Ihren Debitoren anbieten, über Paypal zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="897b7-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="897b7-107">Wenn Sie eine Verkaufsrechnung oder einen Verkaufsauftrag per E-Mail versenden, hat es einen Paypal-Link im E-Mail-Text und im angefügten PDF-Dokument.</span><span class="sxs-lookup"><span data-stu-id="897b7-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="897b7-108">Wenn der Debitor den Link auswählt, erscheint die Service-Seite für Ihr Paypal-Konto mit den Zahlungsdetails für den Verkauf.</span><span class="sxs-lookup"><span data-stu-id="897b7-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="897b7-109">Der Kunde kann die Rechnung wie jede andere PayPal-Zahlung bezahlen.</span><span class="sxs-lookup"><span data-stu-id="897b7-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="897b7-110">Der Paypal-Zahlungsstandard-Service hat folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="897b7-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="897b7-111">Debitorenzahlungen sind schneller auf Ihrem Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="897b7-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="897b7-112">Debitoren haben mehr Arten, Rechnungen zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="897b7-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="897b7-113">Paypal bietet einen vertrauenswürdigen Zahlungsservice an, den Debitoren gegenüber der Eingabe von Kreditkarteninformationen auf der Websites bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="897b7-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="897b7-114">Paypal bietet mehrere Arten zur Zahlungsabwicklung an, einschließlich Kreditkartenverarbeitung, Paypal-Konten und andere Quellen.</span><span class="sxs-lookup"><span data-stu-id="897b7-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="897b7-115">Der Paypal-Link kann automatisch allen Verkaufsbelegen oder manuell vom Benutzer hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="897b7-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="897b7-116">Der Paypal-Zahlungsstandard-Service kostet keine Monatsgebühren oder Gebühren für die Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="897b7-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="897b7-117">Da dies eine Erweiterung ist, können Sie den Paypal-Zahlungsstandard-Service einfach aktivieren wenn und wenn Ihr Geschäft sie benötigt.</span><span class="sxs-lookup"><span data-stu-id="897b7-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="897b7-118">Weitere Informationen finden Sie unter [Aktivieren Sie Debitoren-Zahlung durch Paypal](sales-how-enable-payment-service-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="897b7-118">For more information, see [Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="897b7-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="897b7-119">See Also</span></span>
<span data-ttu-id="897b7-120">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzenb](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="897b7-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="897b7-121">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="897b7-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="897b7-122">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="897b7-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
