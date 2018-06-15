---
title: Business Central und Power BI Inhaltspakete verbinden | Microsoft Docs
description: Nutzen Sie Einblicke in Business Central mit Power BI und dem Business Central-Inhaltspaket.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/03/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 0196bff5dedb878884fd3d6e0208022faa968dfd
ms.contentlocale: de-ch
ms.lasthandoff: 05/17/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a><span data-ttu-id="ad7d1-103">Power BI mit den Dynamics 365 Business Central-Inhaltspaketen verbinden</span><span class="sxs-lookup"><span data-stu-id="ad7d1-103">Connecting Power BI to Dynamics 365 Business Central Content Packs</span></span>
<span data-ttu-id="ad7d1-104">Einblicke in Ihre Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Daten zu erhalten ist mit Power BI und dem Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Inhaltspaket sehr einfach.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="ad7d1-105">Power BI ruft die Daten ab und erstellt ein Standarddashboard und Berichte auf Grundlage der Daten.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

<span data-ttu-id="ad7d1-106">Sie müssen ein gültiges Konto mit Dynamics 365 und Power BI haben.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="ad7d1-107">Zudem müssen Sie [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) herunterladen, wenn Sie Ihre eigenen Power BI-Berichte erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) if you wish to create your own Power BI reports.</span></span> <span data-ttu-id="ad7d1-108">Power BI Inhaltpakete benötigen Berechtigungen für die Tabellen, aus denen Daten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="ad7d1-109">Weitere Einzelheiten auf den Anforderungen werden im Folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="ad7d1-110">So stellen Sie die Verbindung her</span><span class="sxs-lookup"><span data-stu-id="ad7d1-110">How to Connect</span></span>
1. <span data-ttu-id="ad7d1-111">Wählen Sie **Daten abrufen** am unteren Rand des linken Navigationsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="ad7d1-112">![Navigieren, um die Daten zu erhalten](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="ad7d1-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>

<span data-ttu-id="ad7d1-113">Sie können auch aus Dynamics 365 Business Edition heraus beginnen.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-113">You may also get starting from within Dynamics 365 Business Edition.</span></span> <span data-ttu-id="ad7d1-114">Im Rollencenter navigieren Sie zu **Berichtsauswahl** im Power BI-Rollencenterteil.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-114">From the role center, navigate to **Report Selection** in the Power BI Role Center part.</span></span> <span data-ttu-id="ad7d1-115">Wählen Sie entweder **Service** oder **Mein Unternehmen** im Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-115">Select either **Service** or **My Organization** from the ribbon.</span></span> <span data-ttu-id="ad7d1-116">Wenn eine dieser Aktionen ausgewählt wird, gelangen Sie zu der jeweiligen Dienstgalerie in Power BI oder zu der Dienstbibliothek in Power BI, die zudem so gefiltert ist, dass nur Inhaltspakete zu [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-116">When either of these actions are selected, you will be taken to either the Organization gallery in Power BI or to the services library in Power BI, which will also be filtered to only display content packs related to [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span>

2. <span data-ttu-id="ad7d1-117">Im Feld **Dienste** wählen Sie **Abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-117">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="ad7d1-118">Dadurch wird ein Fenster mit **AppSource** und **Apps für Power BI Apps** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-118">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="ad7d1-119">![Wählen Sie Inhaltspakete von Onlinediensten aus](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="ad7d1-119">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="ad7d1-120">Wählen Sie **Apps** auf der Registerkarte **Apps für Power BI Apps**, wählen Sie das Feld **Microsoft Dynamics 365 Business Central** Inhaltspakete, die Sie verwenden möchten, und wählen Sie dann **jetzt abrufen**.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-120">Select **Apps** from the **Apps for Power BI apps** tab, choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="ad7d1-121">![Wählen Sie Dynamics 365 Business Central und wählen Sie "Jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="ad7d1-121">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="ad7d1-122">Wenn Sie dazu aufgefordert werden, geben Sie in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] den Namen des *Unternehmens* ein.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-122">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="ad7d1-123">Dies ist nicht der Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-123">This is not the display name.</span></span> <span data-ttu-id="ad7d1-124">Der Name des Unternehmens kann auf der Seite „Unternehmen“ innerhalb Ihrer [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]- Instanz gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-124">The company name can be found on the 'Companies' page within your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] instance.</span></span> 
<span data-ttu-id="ad7d1-125">![Wählen Sie Dynamics 365 Business Central und wählen Sie jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="ad7d1-125">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="ad7d1-126">Sobald verbunden, werden ein Dashboard, ein Bericht und ein Datensatz automatisch in Ihren Power BI Arbeitsbereich geladen.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-126">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="ad7d1-127">Wenn abgeschlossen, werden die Kacheln die Daten aus Ihrem [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-Unternehmen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-127">When completed, the tiles will update with data from your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] company.</span></span>
<span data-ttu-id="ad7d1-128">![Wählen Sie Dynamics 365 Business Central und wählen Sie jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="ad7d1-128">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="ad7d1-129">Was jetzt?</span><span class="sxs-lookup"><span data-stu-id="ad7d1-129">What Now?</span></span>

- <span data-ttu-id="ad7d1-130">Versuchen Sie im [Erstellen eine Frage im Q&A-Feld](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) im oberen Bereich des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-130">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>
- <span data-ttu-id="ad7d1-131">[Ändern Sie die Kacheln](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) im Dashboard.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-131">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="ad7d1-132">[Wählen Sie eine Kachel aus](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles), um den zu Grunde liegenden Bericht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-132">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="ad7d1-133">Während Ihr Dataset täglich aktualisiert wird, können Sie den Aktualisierungsplan ändern oder ihn mithilfe von **jetzt aktualisieren** bei Bedarf aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-133">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="ad7d1-134">Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-134">System Requirements</span></span>
<span data-ttu-id="ad7d1-135">Um die Daten [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] in Power BI zu importieren, müssen Sie Berechtigungen für den Webdiensten haben, um die Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-135">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="ad7d1-136">Die Web Services, die für jedes Inhaltspakete erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="ad7d1-136">The web services required for each content pack include:</span></span>

## <a name="role-center-reports"></a><span data-ttu-id="ad7d1-137">Rollencenterberichte</span><span class="sxs-lookup"><span data-stu-id="ad7d1-137">Role Center Reports</span></span>

<span data-ttu-id="ad7d1-138">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-138">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="ad7d1-139">Verkaufschancen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-139">Sales Opportunities</span></span>
- <span data-ttu-id="ad7d1-140">Excel-Vorlage zur Unternehmensansicht</span><span class="sxs-lookup"><span data-stu-id="ad7d1-140">Excel Template View Company</span></span>
- <span data-ttu-id="ad7d1-141">Power BI-Berichtsbeschrifungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-141">Power BI Report Labels</span></span>

<span data-ttu-id="ad7d1-142">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-142">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="ad7d1-143">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="ad7d1-143">PowerBIFinance</span></span>
- <span data-ttu-id="ad7d1-144">Excel-Vorlage zur Unternehmensansicht</span><span class="sxs-lookup"><span data-stu-id="ad7d1-144">Excel Template View Company</span></span>
- <span data-ttu-id="ad7d1-145">Power BI-Berichtsbeschrifungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-145">Power BI Report Labels</span></span>

<span data-ttu-id="ad7d1-146">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-146">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="ad7d1-147">Projektliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-147">Job List</span></span>
- <span data-ttu-id="ad7d1-148">Projektplanzeilen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-148">Job Planning Lines</span></span>
- <span data-ttu-id="ad7d1-149">Projektaufgabenzeilen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-149">Job Task Lines</span></span>
- <span data-ttu-id="ad7d1-150">Power BI-Berichtsbeschrifungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-150">Power BI Report Labels</span></span>
- <span data-ttu-id="ad7d1-151">Excel-Vorlage zur Unternehmensansicht</span><span class="sxs-lookup"><span data-stu-id="ad7d1-151">Excel Template View Company</span></span>

<span data-ttu-id="ad7d1-152">**Microsoft Dynamics 365 Business Central – Sales**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-152">**Microsoft Dynamics 365 Business Central - Sales**</span></span>
- <span data-ttu-id="ad7d1-153">Verkaufsdashboard</span><span class="sxs-lookup"><span data-stu-id="ad7d1-153">Sales Dashboard</span></span>
- <span data-ttu-id="ad7d1-154">Excel-Vorlage zur Unternehmensansicht</span><span class="sxs-lookup"><span data-stu-id="ad7d1-154">Excel Template View Company</span></span>
- <span data-ttu-id="ad7d1-155">Power BI-Berichtsbeschrifungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-155">Power BI Report Labels</span></span>

## <a name="list-page-reports"></a><span data-ttu-id="ad7d1-156">Berichte für Listenseite</span><span class="sxs-lookup"><span data-stu-id="ad7d1-156">List Page Reports</span></span> 

<span data-ttu-id="ad7d1-157">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-157">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="ad7d1-158">Artikel-Statistik nach Debitor</span><span class="sxs-lookup"><span data-stu-id="ad7d1-158">Item Sales by Customer</span></span>
- <span data-ttu-id="ad7d1-159">Power BI - Artikeleinkaufsliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-159">Power BI Item Purchase List</span></span>
- <span data-ttu-id="ad7d1-160">Power BI - Artikelverkaufsliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-160">Power BI Item Sales List</span></span>
- <span data-ttu-id="ad7d1-161">Verkaufsdashboard</span><span class="sxs-lookup"><span data-stu-id="ad7d1-161">Sales Dashboard</span></span>
- <span data-ttu-id="ad7d1-162">Power BI - Debitorenliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-162">Power BI Customer List</span></span>
- <span data-ttu-id="ad7d1-163">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ad7d1-163">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="ad7d1-164">Power BI-Berichtsbeschrifungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-164">Power BI Report Labels</span></span> 

<span data-ttu-id="ad7d1-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span></span>
- <span data-ttu-id="ad7d1-166">Power BI - Betrag im Hauptbuch - Liste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-166">Power BI GL Amount List</span></span>
- <span data-ttu-id="ad7d1-167">Power BI - Hauptbuch - Budgetierter Betrag</span><span class="sxs-lookup"><span data-stu-id="ad7d1-167">Power BI GL Budgeted Amount</span></span>
- <span data-ttu-id="ad7d1-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ad7d1-168">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="ad7d1-169">Power BI-Berichtsbeschrifungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-169">Power BI Report Labels</span></span>

<span data-ttu-id="ad7d1-170">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-170">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="ad7d1-171">Artikel-Statistik nach Debitor</span><span class="sxs-lookup"><span data-stu-id="ad7d1-171">Item Sales by Customer</span></span>
- <span data-ttu-id="ad7d1-172">Power BI - Artikeleinkaufsliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-172">Power BI Item Purchase List</span></span>
- <span data-ttu-id="ad7d1-173">Power BI - Artikelverkaufsliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-173">Power BI Item Sales List</span></span>
- <span data-ttu-id="ad7d1-174">Verkaufsdashboard</span><span class="sxs-lookup"><span data-stu-id="ad7d1-174">Sales Dashboard</span></span>
- <span data-ttu-id="ad7d1-175">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ad7d1-175">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="ad7d1-176">Power BI-Berichtsbeschrifungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-176">Power BI Report Labels</span></span>

<span data-ttu-id="ad7d1-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span></span>
- <span data-ttu-id="ad7d1-178">Power BI - Projektliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-178">Power BI Jobs List</span></span>
- <span data-ttu-id="ad7d1-179">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ad7d1-179">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="ad7d1-180">Power BI-Berichtsbeschrifungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-180">Power BI Report Labels</span></span>

<span data-ttu-id="ad7d1-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span></span>
- <span data-ttu-id="ad7d1-182">Power BI - Einkaufsliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-182">Power BI Purchase List</span></span>
- <span data-ttu-id="ad7d1-183">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ad7d1-183">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="ad7d1-184">Power BI-Berichtsbeschrifungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-184">Power BI Report Labels</span></span>

<span data-ttu-id="ad7d1-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span></span>
- <span data-ttu-id="ad7d1-186">Power BI - Verkaufsliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-186">Power BI Sales List</span></span>
- <span data-ttu-id="ad7d1-187">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ad7d1-187">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="ad7d1-188">Power BI-Berichtsbeschrifungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-188">Power BI Report Labels</span></span>


<span data-ttu-id="ad7d1-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="ad7d1-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="ad7d1-190">Power BI - Artikeleinkaufsliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-190">Power BI Item Purchase List</span></span>
- <span data-ttu-id="ad7d1-191">Power BI - Artikelverkaufsliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-191">Power BI Item Sales List</span></span>
- <span data-ttu-id="ad7d1-192">Power BI - Kreditorenliste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-192">Power BI Vendor List</span></span>
- <span data-ttu-id="ad7d1-193">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ad7d1-193">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="ad7d1-194">Power BI-Berichtsbeschrifungen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-194">Power BI Report Labels</span></span>

## <a name="web-services"></a><span data-ttu-id="ad7d1-195">Webdienste</span><span class="sxs-lookup"><span data-stu-id="ad7d1-195">Web Services</span></span>
<span data-ttu-id="ad7d1-196">Eine einfache Methode, die Webdienste zu finden ist, in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] nach Webdiensten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-196">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="ad7d1-197">In der Liste stellen Sie sicher, dass das Veröffentlichungsfeld für die oben aufgeführten Webdienste markiert wird.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-197">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ad7d1-198">Problembehebung</span><span class="sxs-lookup"><span data-stu-id="ad7d1-198">Troubleshooting</span></span>
<span data-ttu-id="ad7d1-199">Das Power BI-Dashboard beruht auf den veröffentlichten Webdiensten, die oben erwähnten werden. Es enthält Daten vom Demomandanten oder von Ihrem eigenen Unternehmen wenn Sie Daten aus der aktuellen Finanzlösung importieren.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-199">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="ad7d1-200">Wenn etwas schief geht, stellt dieser Abschnitt eine Problemumgehung für die häufigsten Probleme bereit.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-200">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="ad7d1-201">Ungültiger Unternehmensnamen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-201">Incorrect Company Name</span></span>  
<span data-ttu-id="ad7d1-202">Ein häufiger Fehler ist, den Unternehmensanzeigenamen anstelle des Unternehmensnamens einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-202">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="ad7d1-203">Unternehmensnamensuche für **Unternehmen** zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-203">To find the company name search for **Companies**.</span></span> <span data-ttu-id="ad7d1-204">Verwenden Sie das Feld **Name**, wenn Sie den Unternehmensnamen eingeben.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-204">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="ad7d1-205">Falscher Benutzername und Kennwort</span><span class="sxs-lookup"><span data-stu-id="ad7d1-205">Incorrect User Name and Password</span></span>  
<span data-ttu-id="ad7d1-206">Der Benutzername und das Kennwort, die zum Verbinden verwendet werden, sind dieselben, die verwendet werden, um die Verbindung mit Ihrem  Microsoft Office 365 Konto herzustellen.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-206">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="ad7d1-207">Die Inhaltspakete erfordern, dass Sie ein Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Konto haben.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-207">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="ad7d1-208">Nachdem Sie Ihre Anmeldeinformationen eingeben haben, erkennen wir sämtliche Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Tenants, auf die Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-208">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="ad7d1-209">Wenn Sie kein lizenziertes oder Probe-Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Konto haben, erhalten Sie eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-209">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="ad7d1-210">Der Schlüssel glich keinen Zeilen in der Tabelle</span><span class="sxs-lookup"><span data-stu-id="ad7d1-210">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="ad7d1-211">Wenn Sie einen nicht gültigen Unternehmensnamen während des Verbindungsvorgangs eingeben, erhalten Sie möglicherweise die Fehlermeldung, "der Schlüssel entsprach keinen Zeilen in der Tabelle".</span><span class="sxs-lookup"><span data-stu-id="ad7d1-211">If you enter a non-valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="ad7d1-212">Geben Sie den korrekten Unternehmensnamen an und versuchen Sie die Verbindung erneut.</span><span class="sxs-lookup"><span data-stu-id="ad7d1-212">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad7d1-213">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad7d1-213">See Also</span></span>
[<span data-ttu-id="ad7d1-214">Erste Schritte mit Power BI</span><span class="sxs-lookup"><span data-stu-id="ad7d1-214">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[<span data-ttu-id="ad7d1-215">Power BI - Grundmodelle</span><span class="sxs-lookup"><span data-stu-id="ad7d1-215">Power BI - Basic Concepts</span></span>](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[<span data-ttu-id="ad7d1-216">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="ad7d1-216">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="ad7d1-217">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="ad7d1-217">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="ad7d1-218">Geschäftsdaten aus anderen Finanzsystemen migrieren</span><span class="sxs-lookup"><span data-stu-id="ad7d1-218">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="ad7d1-219">[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="ad7d1-219">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="ad7d1-220">Finanzen</span><span class="sxs-lookup"><span data-stu-id="ad7d1-220">Finance</span></span>](finance.md)  
<span data-ttu-id="ad7d1-221">[Einrichtungs-Berichterstellugn für [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="ad7d1-221">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

