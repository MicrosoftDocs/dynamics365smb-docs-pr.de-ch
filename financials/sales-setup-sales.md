---
title: "Überblick der Aufgaben zum konfigurieren von Verkaufsprozessen | Microsoft Docs"
description: "Gliedert die Aufgaben, um Regeln und Werte einzurichten, um Ihre Vertriebsrichtlinien und Arbeitsgänge zu definieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 06/01/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 75ed584feda066a6c412f861bd624646c4c31085
ms.contentlocale: de-ch
ms.lasthandoff: 09/11/2017

---
# <a name="setting-up-sales"></a><span data-ttu-id="b0761-103">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="b0761-103">Setting Up Sales</span></span>
<span data-ttu-id="b0761-104">Bevor Sie Verkaufsprozesse verwalten können, müssen die Regeln und Werte konfiguriert werden, die die Vertriebsrichtlinien des Mandanten definieren.</span><span class="sxs-lookup"><span data-stu-id="b0761-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="b0761-105">Zuerst muss die allgemeine Einrichtung definiert werden, z. B. welche Verkaufsbelege erforderlich sind und wie deren Werte gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="b0761-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="b0761-106">Diese allgemeinen Einstellungen werden in der Regel einmalig bei der Erstimplementierung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0761-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="b0761-107">Eine separate Reihe von Aufgaben, die mit der Erfassung neuer Kreditoren im Zusammenhang stehen, dient dazu, alle Sonderpreis oder Rabattvereinbarungen zu speichern, die Sie mit einzelnen Kreditoren haben.</span><span class="sxs-lookup"><span data-stu-id="b0761-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="b0761-108">Einrichten von finanzbezogenen Verkäufen wie Zahlungsformen und Währungen werden im Finanzsetupabschnitt behandelt.</span><span class="sxs-lookup"><span data-stu-id="b0761-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="b0761-109">Weitere Informationen finden Sie unter [Einrichten von Finanzen](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="b0761-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="b0761-110">An</span><span class="sxs-lookup"><span data-stu-id="b0761-110">To</span></span> | <span data-ttu-id="b0761-111">Informationen</span><span class="sxs-lookup"><span data-stu-id="b0761-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="b0761-112">Erstellen Sie eine Debitorenkarte für jeden Debitor, an den Sie verkaufen.</span><span class="sxs-lookup"><span data-stu-id="b0761-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="b0761-113">Vorgehensweise: Einen neuen Debitor registrieren</span><span class="sxs-lookup"><span data-stu-id="b0761-113">How to: Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="b0761-114">Aktivieren Sie Debitoren, um über Paypal zu bezahlen, indem Sie das Paypal-Logo in Verkaufsbelegen auswählen.</span><span class="sxs-lookup"><span data-stu-id="b0761-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="b0761-115">Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Paypal</span><span class="sxs-lookup"><span data-stu-id="b0761-115">How to: Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="b0761-116">Geben Sie die verschiedenen Rabatte und alternativen Preise ein, die Sie den Debitoren abhängig von Artikel, Mengen und/oder Datum gewähren.</span><span class="sxs-lookup"><span data-stu-id="b0761-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="b0761-117">Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="b0761-117">How to: Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="b0761-118">Einrichten von Verkäufer, sodass Sie diese den Debitorenkontakten zuweisen können oder die Leistung des Verkaufspersonals messen können und als Basis für die Berechnung von Verkaufsprovisionen oder der Prämie zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="b0761-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="b0761-119">Gewusst wie: Verkäufer einrichten</span><span class="sxs-lookup"><span data-stu-id="b0761-119">How to: Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="b0761-120">Geben Sie für einzelne Debitoren oder für alle Debitoren an, wie Verkaufsbelege standardmäßig gesendet werden, wenn Sie die Aktion **Buchen und senden** auswählen.</span><span class="sxs-lookup"><span data-stu-id="b0761-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="b0761-121">Vorgehensweise: Einrichten von Belegsendeprofilen</span><span class="sxs-lookup"><span data-stu-id="b0761-121">How to: Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="b0761-122">Legen Sie die E-Mail a, um eine Zusammenfassung der Informationen des Verkaufsbelegs zu erhalten, der gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0761-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="b0761-123">[Vorgehensweise: Senden von Belegen über E-Mail](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="b0761-123">[How to: Send Documents by Email](ui-how-send-documents-email.md).</span></span> |

## <a name="see-also"></a><span data-ttu-id="b0761-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0761-124">See Also</span></span>
[<span data-ttu-id="b0761-125">Verkauf</span><span class="sxs-lookup"><span data-stu-id="b0761-125">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="b0761-126">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b0761-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

