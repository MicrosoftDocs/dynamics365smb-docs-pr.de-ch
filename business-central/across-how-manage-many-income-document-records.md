---
title: Definieren, welche eingehenden Belege Sie sehen möchten| Microsoft Docs
description: Regulieren der Standardansicht aus eingehenden Belege, wie Erechnungen, um die Übersicht verarbeiteten und nicht verarbeiteten Datensätzen zu verbessern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5401b8049e13d594f3429c97cfff915fc944c733
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305586"
---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="28cf9-103">Mehrere eingehende Belegdatensätze verwalten</span><span class="sxs-lookup"><span data-stu-id="28cf9-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="28cf9-104">Wenn Sie eingehende Belegdatensätze verarbeiten, erhöht sich die Anzahl der Zeilen auf der Seite **Eingehende Belege** möglicherweise so, dass Sie die Übersicht verlieren.</span><span class="sxs-lookup"><span data-stu-id="28cf9-104">As you create or process incoming document records, the number of lines on the **Incoming Documents** page may grow to an extent where you lose overview.</span></span> <span data-ttu-id="28cf9-105">Daher können Sie eingehende Belegdatensätze auf "Verarbeitet" festlegen, um sie aus der Standardansicht zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="28cf9-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="28cf9-106">Wenn Sie die Aktion **Alle anzeigen** auswählen, können Sie sowohl verarbeitete als auch nicht verarbeitete Datensätze anzeigen.</span><span class="sxs-lookup"><span data-stu-id="28cf9-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="28cf9-107">Sie können in eingehenden Belegdatensätzen, die auf "Verarbeitet" gesetzt wurden, keine Informationen bearbeiten, Dateien hinzufügen oder andere Prozesse ausführen.</span><span class="sxs-lookup"><span data-stu-id="28cf9-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="28cf9-108">Sie müssen sie zuerst auf "Nicht verarbeitet" festlegen.</span><span class="sxs-lookup"><span data-stu-id="28cf9-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="28cf9-109">Das Kontrollkästchen **Verarbeitet** ist automatisch bei eingehenden Belegdatensätzen aktiviert, die verarbeitet wurden, aber Sie können das Kontrollkästchen auch manuell aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="28cf9-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="28cf9-110">Abhängig von Ihrem Geschäftsprozess wird ein Datensatz möglicherweise verarbeitet, wenn ein zugehöriger Beleg dafür erstellt oder eine Datei angehängt wurde.</span><span class="sxs-lookup"><span data-stu-id="28cf9-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="28cf9-111">Wenn Sie die Seite **Eingehende Belege** innerhalb der Aktion **Meine eingehenden Belege** im Rollencenter öffnen, werden nur nicht verarbeitete Belege standardmässig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28cf9-111">When you open the **Incoming Documents** page with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="28cf9-112">Dies wird in diesem Thema als "Standardansicht" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="28cf9-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="28cf9-113">So entfernen Sie eingehende Belegdatensätze aus der Standardansicht</span><span class="sxs-lookup"><span data-stu-id="28cf9-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="28cf9-114">Auf der Seite **Eingehende Belege** wählen Sie eine oder mehrere Zeilen für eingehende Belegdatensätze, die Sie von der Standardansicht entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="28cf9-114">On the **Incoming Documents** page, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="28cf9-115">Wählen Sie die Aktion **Auf "Verarbeitet" setzen** aus.</span><span class="sxs-lookup"><span data-stu-id="28cf9-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="28cf9-116">Die eingehenden Belegdatensätze werden aus der Standardansicht entfernt, und das Kontrollkästchen **Verarbeitet** wird in den Zeilen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="28cf9-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="28cf9-117">Sie können diese Aktion für einzelne Datensätze auf der Seite **Eingehende Belegkarte** durchführen.</span><span class="sxs-lookup"><span data-stu-id="28cf9-117">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="28cf9-118">So zeigen Sie alle eingehende Belegdatensätze an</span><span class="sxs-lookup"><span data-stu-id="28cf9-118">To view all incoming document records</span></span>
1. <span data-ttu-id="28cf9-119">Wählen Sie auf der Seite **Eingehende Belege** die Aktion **Alle anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="28cf9-119">On the **Incoming Documents** page, choose the **Show All** action.</span></span>

<span data-ttu-id="28cf9-120">Alle eingehenden Belegdatensätze einschliesslich derer, bei denen das Kontrollkästchen **Verarbeitet** nicht aktiviert ist, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28cf9-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="28cf9-121">So fügen Sie eingehende Belegdatensätze der Standardansicht hinzu</span><span class="sxs-lookup"><span data-stu-id="28cf9-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="28cf9-122">Wählen Sie auf der Seite **Eingehende Belege** die Aktion **Alle anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="28cf9-122">On the **Incoming Documents** page, choose the **Show All** action.</span></span>
2. <span data-ttu-id="28cf9-123">Wählen Sie eine oder mehrere Zeilen für eingehende Belegdatensätzeaus, die in der Standardansicht angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="28cf9-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="28cf9-124">Wählen Sie die Aktion **Auf "Nicht verarbeitet" setzen** aus.</span><span class="sxs-lookup"><span data-stu-id="28cf9-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="28cf9-125">Sie können diese Aktion für einzelne Datensätze auf der Seite **Eingehende Belegkarte** durchführen.</span><span class="sxs-lookup"><span data-stu-id="28cf9-125">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="28cf9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28cf9-126">See Also</span></span>
[<span data-ttu-id="28cf9-127">Eingehende Belege verarbeiten</span><span class="sxs-lookup"><span data-stu-id="28cf9-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="28cf9-128">Eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="28cf9-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="28cf9-129">Einkauf</span><span class="sxs-lookup"><span data-stu-id="28cf9-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="28cf9-130">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="28cf9-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
