---
title: Importieren der Gehalts-Daten mithilfe der Ceridian-Gehaltsabrechnungserweiterung
description: Mit der Ceridian-Gehaltsabrechnungserweiterung können Sie die Importgehaltsabrechnungstransaktionen Services Ceridian HR/Payroll (USA) und Ceridian PowerPay (Kanada) importieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f2129d26cab8de999ae6ae1e80943ee4066ab50f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787441"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="5ee53-103">Die Ceridian-Gehaltsabrechnungserweiterung</span><span class="sxs-lookup"><span data-stu-id="5ee53-103">The Ceridian Payroll Extension</span></span>

<span data-ttu-id="5ee53-104">Um Gehaltszahlungen und verwandte Transaktionen zu berücksichtigen, müssen Sie die Gehaltstransaktionen importieren und finanzielle Transaktionen buchen, die durch Ihr Gehaltsabrechnungsanbieter in die Finanzbuchhaltung gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="5ee53-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="5ee53-105">Dazu importieren Sie zuerst eine Datei, die Sie vom Gehaltsabrechnungsanbieter erhalten in die Seite **Fibu Erf.-Journal**.</span><span class="sxs-lookup"><span data-stu-id="5ee53-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="5ee53-106">Anschliessend ordnen Sie die externen Konten in der Gehaltsabrechnungsdatei den jeweiligen Sachkonten zu.</span><span class="sxs-lookup"><span data-stu-id="5ee53-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="5ee53-107">Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen entsprechend der Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="5ee53-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="5ee53-108">Weitere Informationen finden Sie unter [Gehaltsabrechnungstransaktionen importieren](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="5ee53-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="5ee53-109">Mit der Ceridian-Gehaltsabrechnungserweiterung können Sie die Importgehaltsabrechnungstransaktionen Services Ceridian HR/Payroll (USA) und Ceridian PowerPay (Kanada) importieren.</span><span class="sxs-lookup"><span data-stu-id="5ee53-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ee53-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ee53-110">See Also</span></span>

<span data-ttu-id="5ee53-111">[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="5ee53-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="5ee53-112">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5ee53-112">Finance</span></span>](finance.md)  
<span data-ttu-id="5ee53-113">[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5ee53-113">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]