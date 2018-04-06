---
title: Lohntransaktionen importieren| Microsoft Docs
description: Um Gehalt zu verwalten, importieren Sie buchen und finanzieller Transaktionen von Ihrem Gehaltsabrechnungsanbieter auf den Fibuposten, mithilfe einer Gehaltsabrechnungserweiterung wie Ceridian oder Quickbooks.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 06/16/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 45ac64abac2a604eb4f669dd3c246b59f05f4d31
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="import-payroll-transactions"></a><span data-ttu-id="e28dd-103">Lohntransaktionen importieren</span><span class="sxs-lookup"><span data-stu-id="e28dd-103">Import Payroll Transactions</span></span>
<span data-ttu-id="e28dd-104">Um Gehaltszahlungen und verwandte Transaktionen zu berücksichtigen, müssen Sie die Gehaltstransaktionen importieren und finanzielle Transaktionen buchen, die durch Ihr Gehaltsabrechnungsanbieter in die Finanzbuchhaltung gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="e28dd-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="e28dd-105">Dazu importieren Sie zuerst eine Datei, die Sie vom Gehaltsabrechnungsanbieter erhalten in das Fenster **Fibur Buch.Blatt**.</span><span class="sxs-lookup"><span data-stu-id="e28dd-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="e28dd-106">Anschliessend ordnen Sie die externen Konten in der Gehaltsabrechnungsdatei den jeweiligen Sachkonten zu.</span><span class="sxs-lookup"><span data-stu-id="e28dd-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="e28dd-107">Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen entsprechend der Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="e28dd-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e28dd-108">Um diese Funktionalität nutzen zu können, muss für den Gehaltsabrechnungsimport eine Erweiterung eingerichtet und aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="e28dd-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="e28dd-109">Die Ceridian-Gehaltsliste und die Quickbooks-Gehaltsabrechnungsdatei-Importerweiterungen werden in [!INCLUDE[d365fin](includes/d365fin_md.md)] vorinstalliert.</span><span class="sxs-lookup"><span data-stu-id="e28dd-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e28dd-110">Weitere Informationen finden Sie unter [Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-extensions.md) mithilfe der Erweiterungen .</span><span class="sxs-lookup"><span data-stu-id="e28dd-110">For more information, see [Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="e28dd-111">Um eine Lohndatei zu importieren</span><span class="sxs-lookup"><span data-stu-id="e28dd-111">To import a payroll file</span></span>
1. <span data-ttu-id="e28dd-112">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="e28dd-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="e28dd-113">Wählen Sie im relevanten Fibu Buch.-Blattname die Aktion **Gehaltsabrechnungstransaktionen importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e28dd-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="e28dd-114">Ein unterstützter Einrichtungsleitfaden wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e28dd-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="e28dd-115">Befolgen Sie die Schritte im Fenster **Gehaltsabrechnungstransaktionen importieren**.</span><span class="sxs-lookup"><span data-stu-id="e28dd-115">Follow the steps in the **Import Payroll Transactions** window.</span></span>

    > [!TIP]  
>   <span data-ttu-id="e28dd-116">Im Schritt zum Zuordnen der externen Lohn- und Gehaltsabrechnungsdatensätze zu den Sachkonten, erinnert sich das Programm an die Zuordnungen, die Sie erstellen, das nächste Mal, wenn dieselben Daten importiert werden.</span><span class="sxs-lookup"><span data-stu-id="e28dd-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="e28dd-117">Das spart Zeit, weil Sie nicht jedes Mal manuell das Feld **Kontonr.** im Fibu-Erf.-Journal ausfüllen müssen, wenn Sie wiederkehrende Gehaltsabrechnungstransaktionen importiert haben.</span><span class="sxs-lookup"><span data-stu-id="e28dd-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="e28dd-118">Wenn Sie die Schaltfläche **OK** im unterstützten Einrichtungsleitfaden auswählen, wird das Fenster **Fibu Buch.-Blatt** mit den Zeilen ausgefüllt, die die Transaktionen darstellen, die die Gehaltsabrechnungsdatei enthält und dabei werden die relevanten Konten in den Feldern **Sachkonto** vorausgefüllt, gemäss den Zuordnungen, die Sie im Leitfaden vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="e28dd-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** window is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="e28dd-119">Bearbeiten oder buchen Sie die Erf.-Journalzeilen für andere Fibupostenstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="e28dd-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="e28dd-120">Weitere Informationen finden Sie unter [Transaktionen direkt im Fibuposten buchen](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="e28dd-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="e28dd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e28dd-121">See Also</span></span>
[<span data-ttu-id="e28dd-122">Finanzen</span><span class="sxs-lookup"><span data-stu-id="e28dd-122">Finance</span></span>](finance.md)  
<span data-ttu-id="e28dd-123">[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzenb](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e28dd-123">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="e28dd-124">[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)A</span><span class="sxs-lookup"><span data-stu-id="e28dd-124">[Working with General Journals](ui-work-general-journals.md)</span></span>  

