---
title: Pflichtfeld, um Arbeitsgänge abzuschliessen | Microsoft Docs
description: Erhalten von Informationen zu den Feldern, die mit einem roten Sternchen gekennzeichnet werden, das angibt, dass sie benötigt werden und ausgefüllt werden müssen, um Arbeitsgänge benötigt.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: solsen
ms.openlocfilehash: feb0b6f8c90b55363e6eb4ef4f7c17afe4cbaaa3
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195449"
---
# <a name="detecting-mandatory-fields"></a><span data-ttu-id="105a3-103">Pflichtfelder erkennen</span><span class="sxs-lookup"><span data-stu-id="105a3-103">Detecting Mandatory Fields</span></span>
<span data-ttu-id="105a3-104">Wenn Sie Daten auf Seiten in  [!INCLUDE[d365fin](includes/d365fin_md.md)] eingeben, werden bestimmte Felder mit einem roten Sternchen markiert.</span><span class="sxs-lookup"><span data-stu-id="105a3-104">When you enter data on pages in [!INCLUDE[d365fin](includes/d365fin_md.md)], certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="105a3-105">Das rote Sternchen bedeutet, dass das Feld ausgefüllt werden muss, um einen bestimmten Prozess, der das Feld verwendet, abzuschliessen (Beispiel: Buchung einer Transaktion, die den Wert in dem Feld verwendet).</span><span class="sxs-lookup"><span data-stu-id="105a3-105">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>

<span data-ttu-id="105a3-106">Selbst wenn das Feld ein rotes Sternchen enthält, sind Sie nicht gezwungen, das Feld auszufüllen, bevor Sie mit anderen Feldern fortfahren oder die Seite schliessen.</span><span class="sxs-lookup"><span data-stu-id="105a3-106">Even though the field contains a red asterisk, you are not forced to fill in the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="105a3-107">Das rote Sternchen dient nur als Erinnerung, dass Sie am Beenden eines bestimmten Prozesses gehindert werden.</span><span class="sxs-lookup"><span data-stu-id="105a3-107">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>

## <a name="examples"></a><span data-ttu-id="105a3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="105a3-108">Examples</span></span>
<span data-ttu-id="105a3-109">Auf der Seite **Debitorenkarte** wird im Feld **Name** und in den drei **Salestax Gebietscodes** das rote Sternchen angezeigt, um anzugeben, dass Sie eine Verkaufstransaktion für den Debitor nur dann buchen können, wenn diese ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="105a3-109">On the **Customer Card** page, the red asterisk appears in the **Name** field, in the **Tax Area Code** field, and in the posting group fields to indicate that you cannot post a sales transaction for the customer unless the fields are filled.</span></span>

<span data-ttu-id="105a3-110">Auf der Seite **Artikelkarte** wird das rote Sternchen auf **Beschreibung** und den Basiseinheitencode Feldern angezeigt, um anzugeben, dass Sie den Artikel in einer Belegzeile (beispielsweise in einem Verkaufsauftrag) nur dann eingeben können, wenn auch diese Felder ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="105a3-110">On the **Item Card** page, the red asterisk appears in the **Description** field to indicate that you cannot enter the item on a document line, such as a sales order, unless this field is filled.</span></span>

## <a name="see-also"></a><span data-ttu-id="105a3-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="105a3-111">See Also</span></span>
<span data-ttu-id="105a3-112">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="105a3-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
