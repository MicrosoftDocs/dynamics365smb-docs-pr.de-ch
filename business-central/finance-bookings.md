---
title: Fakturieren von Anmeldungen in  Business Central | Microsoft Docs
description: "Erfahren Sie, wie Sie Massenrechnungsstellung von Microsoft Bookings in Business Central vornehmen können."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 357614eb44a312fcc8e078f3d5162fd16be8faa5
ms.contentlocale: de-ch
ms.lasthandoff: 11/22/2018

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a><span data-ttu-id="1c335-103">Massenrechnungen für Microsoft-Anmeldungen in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="1c335-103">Bulk Invoicing for Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="1c335-104">Wenn Ihr Unternehmen die Anmeldungs-App in Office 365 verwendet, können Sie Massenrechnungsstellung für Termine vornehmen.</span><span class="sxs-lookup"><span data-stu-id="1c335-104">If your company uses the Bookings app in Office 365, you can do bulk invoicing for appointments.</span></span> <span data-ttu-id="1c335-105">Die Seite **Nicht in Rechnung gestellte Anmeldungen** in [!INCLUDE[d365fin](includes/d365fin_md.md)] stellt eine Liste der abgeschlossenen Anmeldungen des Mandanten bereit.</span><span class="sxs-lookup"><span data-stu-id="1c335-105">The **Uninvoiced Bookings** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a list of the company's completed bookings.</span></span> <span data-ttu-id="1c335-106">Auf dieser Seite können Sie schnell die Termine auswählen, die Sie verrechnen wollen und Entwurfsrechnungen für die erbrachten Services erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c335-106">In this page you can quickly select the appointments that you want to invoice and create draft invoices for the services provided.</span></span>  

## <a name="connect-to-bookings"></a><span data-ttu-id="1c335-107">Mit Anmeldungen verbinden</span><span class="sxs-lookup"><span data-stu-id="1c335-107">Connect to Bookings</span></span>
<span data-ttu-id="1c335-108">Um Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Anmeldungen zu verbinden, müssen Sie Ihren Anmeldungsmandanten angeben, was mit Anmeldungen zu synchronisieren ist, und wie oft Sie synchronisieren möchten und welche Vorlage zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="1c335-108">To connect your [!INCLUDE[d365fin](includes/d365fin_md.md)] with Bookings, you must specify your Bookings company, what to synchronize with Bookings, how often to synchronize, and which templates to use.</span></span> <span data-ttu-id="1c335-109">Sie richten diese Daten auf der Seite **Anmeldungs-Synchronisierung einrichten** ein, die Sie auf der Seite **Exchange-Synchronisierungs-Einrichtung** starten können, die Sie unter [Suchen](ui-search.md) finden.</span><span class="sxs-lookup"><span data-stu-id="1c335-109">You set up this information in the **Booking Sync. Setup** page, which you can launch from the **Exchange Sync. Setup** page, which you can find through [Search](ui-search.md).</span></span>  

<span data-ttu-id="1c335-110">Wenn Sie beispielsweise Debitoren zwischen Anmeldungen und [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisieren möchten, müssen Sie die Standardvorlage angeben, die sie verwenden möchten, um neue Debitoren basierend auf den [!INCLUDE[d365fin](includes/d365fin_md.md)] Debitoren in Ihrem Anmeldungsmandanten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c335-110">For example, if you want to synchronize customers between Bookings and [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the default template to use to add new customers in [!INCLUDE[d365fin](includes/d365fin_md.md)] based on the customers in your Bookings company.</span></span>  

## <a name="invoice-appointments"></a><span data-ttu-id="1c335-111">Termin fakturieren</span><span class="sxs-lookup"><span data-stu-id="1c335-111">Invoice Appointments</span></span>
<span data-ttu-id="1c335-112">Wenn es Zeit ist, die Rechnungen über die abgeschlossenen Anmeldungen zu senden, wechseln Sie zur Seite **Nicht fakturierte Anmeldungen**.</span><span class="sxs-lookup"><span data-stu-id="1c335-112">When it is time to send invoices for the completed bookings, you go to the **Uninvoiced Bookings** page.</span></span> <span data-ttu-id="1c335-113">Abhängig davon, wie oft die Daten synchronisiert werden, ist die Liste lang oder kurz.</span><span class="sxs-lookup"><span data-stu-id="1c335-113">Depending on how often the information is synchronized, the list is long or short.</span></span> <span data-ttu-id="1c335-114">Sie können Rechnungen für alle Windows-Anmeldungen in der Liste oder für eine Anmeldung nach der anderen erstellen.</span><span class="sxs-lookup"><span data-stu-id="1c335-114">You can create invoices for all bookings in the list or one booking at a time.</span></span> <span data-ttu-id="1c335-115">Sie können eine oder mehrere Posten in der Liste auswählen und nur jene fakturieren.</span><span class="sxs-lookup"><span data-stu-id="1c335-115">You can select one or more entries in the list and invoice those only.</span></span>  

<span data-ttu-id="1c335-116">Die Unterstützung für die Fakturierung von Terminen von Anmeldungen ist schneller und einfacher als der vollere Workflow für die Arbeit mit Verkaufsangeboten, Verkaufsaufträgen und Verkaufsrechnungen.</span><span class="sxs-lookup"><span data-stu-id="1c335-116">The support for invoicing appointments from Bookings is simpler than the fuller workflow of working with sales quotes, sales orders, and sales invoices.</span></span> <span data-ttu-id="1c335-117">Weitere Informationen finden Sie unter [Verkaufsrechnungen](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="1c335-117">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span> <span data-ttu-id="1c335-118">Sie können wählen, Ihre Services mithilfe von [!INCLUDE[d365fin](includes/d365fin_md.md)] zu verkaufen oder wählen, Anmeldungen zu nutzen, abhängig von Ihren Geschäftsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="1c335-118">You can choose to sell your services using [!INCLUDE[d365fin](includes/d365fin_md.md)] or choose to use Bookings, depending on your business needs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1c335-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c335-119">See Also</span></span>
[<span data-ttu-id="1c335-120">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1c335-120">Finance</span></span>](finance.md)  
[<span data-ttu-id="1c335-121">Verkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="1c335-121">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="1c335-122">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="1c335-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="1c335-123">Microsoft-Anmeldungen</span><span class="sxs-lookup"><span data-stu-id="1c335-123">Microsoft Bookings</span></span>](https://products.office.com/en-us/business/scheduling-and-booking-app)  

