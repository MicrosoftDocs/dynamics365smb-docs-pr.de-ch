---
title: "Fügen Sie Ihren externen Buchhalter Ihrem Financials hinzu | Microsoft Docs"
description: "Erfahren Sie, wie Sie den externen Buchhalter zu Ihrem Dynamics 365 for Financials einladen können."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b7efbb724f322d371e9e1b725612cb4eb0b3ceb2
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a><span data-ttu-id="a5e51-103">Externen Buchhalter einladen zu Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="a5e51-103">Inviting Your External Accountant to Your [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="a5e51-104">Wenn Sie eines externen Buchhalter verwenden, um Ihre Buch und Berichte zu verwalten, können Sie sie für Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] einladen, damit sie mit Ihnen an Ihren steuerlichen Daten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a5e51-104">If you use an external accountant to manage your books and financial reporting, you can invite them to your [!INCLUDE[d365fin](includes/d365fin_md.md)] so they can work with you on your fiscal data.</span></span>

<span data-ttu-id="a5e51-105">Sobald Ihr Buchhalter zu den verwendeten [!INCLUDE[d365fin](includes/d365fin_md.md)] Zugriff hat, können sie das Rollencenter **Buchhalter** verwenden, das Zugriff auf den relevantsten Fenstern für ihre Arbeit gibt.</span><span class="sxs-lookup"><span data-stu-id="a5e51-105">Once your accountant has gained access to your [!INCLUDE[d365fin](includes/d365fin_md.md)], they can use the **Accountant** Role Center that gives easy access to the most relevant windows for their work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a5e51-106">Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a5e51-106">This functionality requires that the experience is set to **Suite**.</span></span> <span data-ttu-id="a5e51-107">Weitere Informationen finden Sie unter [Anpassen Ihrer Financials Experience](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="a5e51-107">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a><span data-ttu-id="a5e51-108">Ihren Buchhalter einladen zu Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="a5e51-108">Invite Your Accountant to Your [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="a5e51-109">In der neuesten Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] machen wir es Ihnen ganz einfach, Ihren externen Buchhalter einzuladen.</span><span class="sxs-lookup"><span data-stu-id="a5e51-109">In the latest version of [!INCLUDE[d365fin](includes/d365fin_md.md)], we have made it easy for you to invite your external accountant.</span></span> <span data-ttu-id="a5e51-110">Öffnen Sie einfach das Fenster **Benutzer** und wählen Sie im Band die Aktion **Externen Buchhalter einladen**.</span><span class="sxs-lookup"><span data-stu-id="a5e51-110">Simply open the **Users** window, and then choose the **Invite External Accountant** action in the ribbon.</span></span> <span data-ttu-id="a5e51-111">Es wird eine E-Mail für Sie vorbereitet. Sie tragen einfach nur die E-Mail-Adresse Ihres Buchhalters ein und senden die Einladung ab.</span><span class="sxs-lookup"><span data-stu-id="a5e51-111">An email is made ready for you, just add your accountant's work email, and send the invitation.</span></span>  

![Ihren Buchhalter einladen](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  <span data-ttu-id="a5e51-113">Dies setzt voraus, dass Sie SMPT-E-Mail eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="a5e51-113">This requires that you have set up SMTP email.</span></span> <span data-ttu-id="a5e51-114">Dies können Sie selbst machen, oder Ihren [!INCLUDE[d365fin](includes/d365fin_md.md)]-Partner darum bitten.</span><span class="sxs-lookup"><span data-stu-id="a5e51-114">You can do this yourself or ask your [!INCLUDE[d365fin](includes/d365fin_md.md)] partner.</span></span> <span data-ttu-id="a5e51-115">Zudem müssen als [!INCLUDE[d365fin](includes/d365fin_md.md)] Benutzeradministrator, nicht als der Geschäftsinhaber oder andere Benutzer angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="a5e51-115">Also, you must be logged in to [!INCLUDE[d365fin](includes/d365fin_md.md)] as a user administrator, not as the business owner or other users.</span></span>  

### <a name="separate-license"></a><span data-ttu-id="a5e51-116">Lizenzen trennen</span><span class="sxs-lookup"><span data-stu-id="a5e51-116">Separate License</span></span>
<span data-ttu-id="a5e51-117">Hinter den Kulissen wird der Buchhalter Ihrem Active Directory-Mandanten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a5e51-117">Behind the scenes, the accountant is added to your Active Directory tenant.</span></span> <span data-ttu-id="a5e51-118">Ihr Administrator kann überprüfen, ob der Buchhalter die Einladung akzeptiert und der richtigen Lizenz hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a5e51-118">Your administrator can verify that the accountant accepts the invitation and is assigned the correct license.</span></span> <span data-ttu-id="a5e51-119">Die Schritte dazu hängen von der Art des Kontos ab, das Sie verwendet haben, als Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmeldeten.</span><span class="sxs-lookup"><span data-stu-id="a5e51-119">The steps for doing this depends on the type of account that you used when you signed up for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a5e51-120">Dieses Thema basiert auf Grundlage von Dimensionswertcodes von einem Office 365-Konto, welches Microsoft Azure Active Directory verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5e51-120">This topic is based on the use of an Office 365 account, which uses Microsoft Azure Active Directory.</span></span>  

<span data-ttu-id="a5e51-121">Wenn Sie Ihr Abonnement von [!INCLUDE[d365fin](includes/d365fin_md.md)] nicht mehr aktiviert haben die Evaluationsunternehmung nicht mehr verwenden, haben Sie einen Azure Active Directory Tenant.</span><span class="sxs-lookup"><span data-stu-id="a5e51-121">If you have activated your subscription of [!INCLUDE[d365fin](includes/d365fin_md.md)] and are no longer using the evaluation company, you have an Azure Active Directory tenant.</span></span> <span data-ttu-id="a5e51-122">Der Administrator oder [!INCLUDE[d365fin](includes/d365fin_md.md)] Partner verwaltet diesen Tenant in [Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="a5e51-122">Your administrator or [!INCLUDE[d365fin](includes/d365fin_md.md)] partner manages this tenant in the [Azure portal](https://portal.azure.com).</span></span> <span data-ttu-id="a5e51-123">Dieses ist, woher neue Benutzer hinzugefügt werden und Lizenzen angewendet und entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a5e51-123">This is where new users are added and licenses are applied and removed.</span></span> <span data-ttu-id="a5e51-124">Weitere Informationen finden Sie unter [Microsoft Azure-Portalübersicht](https://docs.microsoft.com/en-us/azure/azure-portal-overview).</span><span class="sxs-lookup"><span data-stu-id="a5e51-124">For more information, see the [Microsoft Azure portal overview](https://docs.microsoft.com/en-us/azure/azure-portal-overview).</span></span>  

<span data-ttu-id="a5e51-125">Einer der Lizenztypen für [!INCLUDE[d365fin](includes/d365fin_md.md)] ist *Externer Buchhalter*.</span><span class="sxs-lookup"><span data-stu-id="a5e51-125">One of the license types for [!INCLUDE[d365fin](includes/d365fin_md.md)] is the *External Accountant* license.</span></span> <span data-ttu-id="a5e51-126">Dieser Lizenztyp ist für Benutzer wie externe Buchhalter gedacht.</span><span class="sxs-lookup"><span data-stu-id="a5e51-126">This license type is intended for use by users such as external accountants.</span></span> <span data-ttu-id="a5e51-127">Das bedeutet, dass Sie einen zusätzlichen Arbeitsplatz in den aktuellen Active Directory nicht kaufen oder eine der vorhandenen Benutzerkonten auf [!INCLUDE[d365fin](includes/d365fin_md.md)] Ihrem externen Buchhalter verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="a5e51-127">This means that you do not have to buy an extra seat in your current Active Directory or use one of your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts on your external accountant.</span></span> <span data-ttu-id="a5e51-128">Wenn beispielsweise Ihr aktuelles Office 365 Abonnement 10 Benutzer umfasst für [!INCLUDE[d365fin](includes/d365fin_md.md)] und Sie 10 *Volle Benutzer*-Lizenzen verwenden, kann der Administrator den externen Buchhalter als Gastbenutzer in Azure hinzufügen und diesem Benutzer die *Externer Buchhalter*-Lizenz ohen zusätzliche Kosten zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a5e51-128">For example, if your current Office 365 subscription includes 10 users for [!INCLUDE[d365fin](includes/d365fin_md.md)], and you are currently using 10 *Full User* licenses, your administrator can simply add your external accountant as a guest user in the Azure portal and assign this user the *External Accountant* license at no additional cost.</span></span> <span data-ttu-id="a5e51-129">Sie können jedoch einen Benutzer mit der *Externer Buchhalter*-Lizenz haben.</span><span class="sxs-lookup"><span data-stu-id="a5e51-129">However, you can only have one user with the *External Accountant* license.</span></span> <span data-ttu-id="a5e51-130">Wenn Sie mehrere Benutzer hinzufügen möchten, müssen Sie das Office 365 Abonnement entsprechend aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a5e51-130">If you want to add more users, you must update your Office 365 subscription accordingly.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5e51-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5e51-131">See Also</span></span>
[<span data-ttu-id="a5e51-132">Finanzen</span><span class="sxs-lookup"><span data-stu-id="a5e51-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="a5e51-133">Vorgehensweise: Richten Sie E-Mail Nachricht manuell oder mit der unterstützten Einrichtung ein</span><span class="sxs-lookup"><span data-stu-id="a5e51-133">How to: Set Up Email Manually or Using the Assisted Setup</span></span>](madeira-how-setup-email.md)  
[<span data-ttu-id="a5e51-134">Buchhalter Experiences in Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="a5e51-134">Accountant Experiences in Dynamics 365 for Financials</span></span>](finance-accounting.md)  
[<span data-ttu-id="a5e51-135">Financials for Accounts in Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a5e51-135">Financials for Accountants on Microsoft.com</span></span>](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
