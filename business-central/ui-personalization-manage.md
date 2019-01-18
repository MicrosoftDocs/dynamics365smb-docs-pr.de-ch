---
title: Verwaltung von Personalisierung als Administrator in Business Central | Microsoft Docs
description: "Erfahren Sie, wie Sie die Benutzeroberfläche anpassen, damit diese Ihren Bedürfnissen entspricht."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 15d7e4aac7989f95f7becc8aa8ed96381a7dc2de
ms.contentlocale: de-ch
ms.lasthandoff: 11/22/2018

---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="997ed-103">Personalisierung als Administrator verwalten</span><span class="sxs-lookup"><span data-stu-id="997ed-103">Managing Personalization as an Administrator</span></span>
<span data-ttu-id="997ed-104"><!--NAV in the Web client--> Benutzer können ihren Arbeitsbereich personalisieren, um ihren Bedürfnissen zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="997ed-104"><!--NAV in the Web client--> Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="997ed-105">Als Administrator können Sie Anpassungen steuern und verwalten, indem Sie die Möglichkeit deaktivieren, dass Benutzer Seiten anpassen und sämtliche Seitenanpassungen löschen, die Benutzer vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="997ed-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span>

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="997ed-106">Personalisierung für ein Profil deaktivieren</span><span class="sxs-lookup"><span data-stu-id="997ed-106">Disable personalization for a profile</span></span>
<span data-ttu-id="997ed-107">Sie können verhindern, dass alle Benutzer, die zu einem bestimmten Profil gehören, ihre Seiten personalisieren können.</span><span class="sxs-lookup"><span data-stu-id="997ed-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="997ed-108">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Profile** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="997ed-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2.  <span data-ttu-id="997ed-109">Wählen Sie das Profil aus, das Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="997ed-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="997ed-110">Aktivieren Sie das Kontrollkästchen **Anpassung deaktivieren**, und klicken Sie dann auf die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="997ed-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="997ed-111">Benutzerpersonalisierung deaktivieren</span><span class="sxs-lookup"><span data-stu-id="997ed-111">Clear user personalizations</span></span>

<span data-ttu-id="997ed-112">Die Löschung der Seitenanpassung ändert die Seite oder erstellt das ursprüngliche Layout wieder.</span><span class="sxs-lookup"><span data-stu-id="997ed-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="997ed-113">Es gibt zwei Möglichkeiten, die Anpassungen zu löschen, die Benutzer auf Seiten vorgenommen haben: mit der Seite **Benutzeranpassung löschen** und mithilfe der Anwendung der Seite **Benutzeranpassungskarte**.</span><span class="sxs-lookup"><span data-stu-id="997ed-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="997ed-114">Benutzeranpassungen löschen mithilfe der Seite Benutzeranpassungen löschen</span><span class="sxs-lookup"><span data-stu-id="997ed-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="997ed-115">Die Seite **Benutzeranpassung löschen** gibt Ihnen die Möglichkeit, die Personalisierung für eine Seite oder pro Benutzer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="997ed-115">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1.  <span data-ttu-id="997ed-116">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzeranpassung löschen** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="997ed-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="997ed-117">Die Seite führt alle Seiten auf, die angepasst wurden, und den Benutzer, dem sie gehören.</span><span class="sxs-lookup"><span data-stu-id="997ed-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="997ed-118">Ein Häkchen in den Spalten **Vorgänger-Anpassung** bedeutet, dass die Personalisierung in einem vorherigen Version von, die erforderlich war [!INCLUDE[d365fin](includes/d365fin_md.md)]die Anpassung, Bearb die unterscheidet, als sie jetzt zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="997ed-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="997ed-119">Benutzer, die versuchen, diese Seiten zu personalisieren, können dies nicht tun, es sei denn, sie entsperren die Seite.</span><span class="sxs-lookup"><span data-stu-id="997ed-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="997ed-120">Weitere Informationen finden Sie unter [Warum eine Seite zum Personalisieren gesperrt ist](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="997ed-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="997ed-121">Wählen Sie den Posten, den Sie löschen möchten, und wählen die Aktion **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="997ed-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="997ed-122">Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="997ed-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="997ed-123">Benutzeranpassungen löschen mithilfe der Seite Benutzeranpassungskarte.</span><span class="sxs-lookup"><span data-stu-id="997ed-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="997ed-124">Die Seite **Benutzeranpassungskarte** gibt Ihnen die Möglichkeit, die Personalisierung für alle Seiten für eijnen bestimmten Benutzer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="997ed-124">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="997ed-125">Dazu müssen Sie die Schreibberechtigung für Tabelle 2000000072 **Profil** haben.</span><span class="sxs-lookup"><span data-stu-id="997ed-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="997ed-126">Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzeranpassung** ein, und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="997ed-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="997ed-127">Die Seite **Benutzeranpassung** führt alle Benutzer auf, die möglicherweise eine personalisierte Seite haben.</span><span class="sxs-lookup"><span data-stu-id="997ed-127">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="997ed-128">Wenn Sie einen Benutzer in der Liste nicht finden können, bedeutet dies, dass sie keine personalisierten Seiten haben.</span><span class="sxs-lookup"><span data-stu-id="997ed-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="997ed-129">Wählen den Benutzer aus der Liste aus und wählen Sie dann die Aktion **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="997ed-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="997ed-130">Wählen Sie auf der Registerkarte **Aktionen** **Personalisierte Seiten löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="997ed-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="997ed-131">Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="997ed-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="997ed-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="997ed-132">See Also</span></span>
[<span data-ttu-id="997ed-133">Personalisieren Ihres Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="997ed-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="997ed-134">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="997ed-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="997ed-135">Ändern von grundlegenden Einstellungen</span><span class="sxs-lookup"><span data-stu-id="997ed-135">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="997ed-136">Sie können auswählen, welche Funktionen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="997ed-136">Changing Which Features are Displayed</span></span>](ui-experiences.md)  

