---
title: Importieren von Bankenclearing-Nummern (Schweiz)
description: Bankenclearingnummern sind eindeutige Nummern zur Kennzeichnung der einzelnen Bankagenturen oder Filialen im Bankenstamm. Diese Informationen sind Voraussetzung für elektronische Zahlung. Die Datei kann auf der Website von SIX Interbank Clearing heruntergeladen werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3b2bcbe6baaf833c1f6bd17d26805420a605591e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301031"
---
# <a name="import-swiss-bank-clearing-numbers"></a><span data-ttu-id="3456e-105">Importieren von Schweizer Bankenclearingnummern</span><span class="sxs-lookup"><span data-stu-id="3456e-105">Import Swiss Bank Clearing Numbers</span></span>
<span data-ttu-id="3456e-106">Bankenclearingnummern sind eindeutige Nummern zur Kennzeichnung der einzelnen Bankagenturen oder Filialen im Bankenstamm.</span><span class="sxs-lookup"><span data-stu-id="3456e-106">Bank clearing numbers are unique numbers used to identify each bank agency or branch in the bank directory.</span></span> <span data-ttu-id="3456e-107">Diese Informationen sind Voraussetzung für elektronische Zahlung.</span><span class="sxs-lookup"><span data-stu-id="3456e-107">This information is required for electronic payment.</span></span> <span data-ttu-id="3456e-108">Die Datei kann auf der Website von [SIX Interbank Clearing](https://go.microsoft.com/fwlink/?LinkId=145121) heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="3456e-108">The file can be downloaded from the [SIX Interbank Clearing](https://go.microsoft.com/fwlink/?LinkId=145121) website.</span></span>  

<span data-ttu-id="3456e-109">Die BC-Bankstammdatei – die offizielle Schweizer Bankenclearingnummer-Datei – kann importiert werden, um die Bankenclearingnummer-Informationen im Bankenstamm zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3456e-109">You can import the BC Bank Master file—the official Swiss bank clearing number file—to update the bank clearing number information in the bank directory.</span></span> <span data-ttu-id="3456e-110">Wenn Sie die Bankenclearingnummer-Datei importieren, werden die Daten in die Tabelle **Bankenstamm** importiert, und die vorhandenen Daten werden überschrieben.</span><span class="sxs-lookup"><span data-stu-id="3456e-110">When you import the bank clearing number file, the data is imported to the **Bank Directory** table, and the existing data is overwritten.</span></span> <span data-ttu-id="3456e-111">Nach dem Importieren der Bankenclearingnummer-Datei können Sie die aktualisierte Bankfilialnummer für Debitoren und Kreditoren definieren.</span><span class="sxs-lookup"><span data-stu-id="3456e-111">After importing the bank clearing number file, you can define the updated bank branch number for customers and vendors.</span></span> <span data-ttu-id="3456e-112">Weitere Informationen finden Sie in den Tabellen "Debitor Bankkonto" und "Kreditor Bankkonto".</span><span class="sxs-lookup"><span data-stu-id="3456e-112">For more information, see the Customer Bank Account table and the Vendor Bank Account table.</span></span>  

## <a name="to-import-swiss-bank-clearing-numbers"></a><span data-ttu-id="3456e-113">So importieren Sie Bankenclearingnummern für Schweiz</span><span class="sxs-lookup"><span data-stu-id="3456e-113">To import Swiss bank clearing numbers</span></span>  

1.  <span data-ttu-id="3456e-114">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen"), und öffnen Sie **Bankenstamm**. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="3456e-114">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Directory**, and choose the related link.</span></span>  
2.  <span data-ttu-id="3456e-115">Wählen Sie die Aktion **Bankverzeichnis importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="3456e-115">Choose the **Import Bank Directory** action.</span></span>  
3.  <span data-ttu-id="3456e-116">Aktivieren Sie auf der Seite **Bankenstamm einlesen** auf dem Inforegister **Optionen** das Feld **Clearingnummern automatisch aktualisieren**, um die Bankenclearingnummern automatisch zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3456e-116">On the **Import Bank Directory** page, on the **Options** FastTab, select the **Automatically Update Clearing Numbers** field to update the bank clearing numbers automatically.</span></span>  
4.  <span data-ttu-id="3456e-117">Klicken Sie auf die Schaltfläche **Drucken** oder auf **Seitenansicht**, um die Bankenclearingnummern zu importieren, und suchen Sie anschliessend auf der Seite **Öffnen** die Datei, die Sie von der Website von SIX Interbank Clearing heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="3456e-117">Choose the **Print** button or the **Preview** button to import the bank clearing numbers, and then, on the **Open** page, locate the file that you have downloaded from the SIX Interbank Clearing website.</span></span>
5. <span data-ttu-id="3456e-118">Wählen Sie die Schaltfläche **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="3456e-118">Choose the **Open** button.</span></span>  

    <span data-ttu-id="3456e-119">Falls Sie die Schaltfläche **Drucken** wählen, werden die Inhalte der Datei gedruckt.</span><span class="sxs-lookup"><span data-stu-id="3456e-119">If you choose the **Print** button, the contents of the file will be printed.</span></span> <span data-ttu-id="3456e-120">Falls Sie auf die Schaltfläche **Seitenansicht** klicken, wird die Tabelle **Bankenstamm** aktualisiert und ein Bericht, dessen Clearingnummern geändert wurden, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3456e-120">If you choose the **Preview** button, the **Bank Directory** table will be updated and a report that has clearing numbers that have changed will be displayed.</span></span>  

<span data-ttu-id="3456e-121">Nachfolgend wird beschrieben, wie Bankfilialnummern für Debitorenbankkonten definiert werden. Diese Schritte gelten jedoch auch für die Definition von Bankfilialnummern für Kreditorenbankkonten.</span><span class="sxs-lookup"><span data-stu-id="3456e-121">The following procedure describes how to define bank branch numbers for customer bank accounts, but the same steps also apply for defining bank branch numbers for vendor bank accounts.</span></span>  

## <a name="to-define-bank-branch-numbers-for-customer-bank-accounts"></a><span data-ttu-id="3456e-122">So definieren Sie Bankfilialnummern für Debitorenbankkonten</span><span class="sxs-lookup"><span data-stu-id="3456e-122">To define bank branch numbers for customer bank accounts</span></span>  

1.  <span data-ttu-id="3456e-123">Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und öffnen **Debitoren**. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="3456e-123">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3456e-124">Wählen Sie den Debitor, für den Sie Bankkontoeninformationen erstellen möchten, und wählen die Aktion **Bankkonten**.</span><span class="sxs-lookup"><span data-stu-id="3456e-124">Select the customer for whom you want to create bank account information, and then choose the **Bank Accounts** action.</span></span>  
3.  <span data-ttu-id="3456e-125">Auf der Seite **Debitor Bankkontenliste** wählen Sie das gewünschte Bankkonto aus, und wählen Sie die **Bearbeiten** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="3456e-125">On the **Customer Bank Account List** page, select the required bank account, and then choose the **Edit** action.</span></span>  
4.  <span data-ttu-id="3456e-126">Wählen Sie auf dem Inforegister **Allgemein** im Feld **BLZ**</span><span class="sxs-lookup"><span data-stu-id="3456e-126">On the **General** FastTab, in the **Bank Branch No.**</span></span> <span data-ttu-id="3456e-127">die Nummer der Bankagentur oder -filiale aus.</span><span class="sxs-lookup"><span data-stu-id="3456e-127">field, select the number of the bank agency or branch.</span></span>  
5.  <span data-ttu-id="3456e-128">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="3456e-128">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3456e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3456e-129">See Also</span></span>  
 <span data-ttu-id="3456e-130">[Elektronische Zahlungen (Schweiz)](swiss-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="3456e-130">[Swiss Electronic Payments](swiss-electronic-payments.md) </span></span>  
 [<span data-ttu-id="3456e-131">Bankkonten einrichten</span><span class="sxs-lookup"><span data-stu-id="3456e-131">Set Up Bank Accounts</span></span>](../../bank-how-setup-bank-accounts.md)
