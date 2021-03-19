---
title: Dient zum Einrichten mehrerer Zinssätze.
description: Sie können Zinsrechnungen mit mehreren Zinssätzen für eine bestimmte Periode berechnen. Die Zinsberechnung ist für alle finanziellen Belastungen, nur mit Veränderung des Zinssatzes für eine bestimmte Periode ähnlich.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 96098ca669dd5001f334cf464d8e3a37de5dbf03
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387288"
---
# <a name="set-up-multiple-interest-rates"></a><span data-ttu-id="e8320-104">Dient zum Einrichten mehrerer Zinssätze.</span><span class="sxs-lookup"><span data-stu-id="e8320-104">Set Up Multiple Interest Rates</span></span>
<span data-ttu-id="e8320-105">Mehrere Zinssätze werden für verschiedene Perioden für gestundete Zahlungen in den Geschäftstransaktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8320-105">Multiple interest rates are used for different periods for delayed payments in trade transactions.</span></span> <span data-ttu-id="e8320-106">Beispielsweise zeigt eine Regierung den maximalen Zinsen, der für einen Verbraucher erhoben wird.</span><span class="sxs-lookup"><span data-stu-id="e8320-106">For example, a government specifies the maximum interest to be levied for a consumer.</span></span> <span data-ttu-id="e8320-107">Dieser Zinssatz kann zweimal jährlich geändert werden am 1. Januar und 1. Juli.</span><span class="sxs-lookup"><span data-stu-id="e8320-107">This interest rate can be changed twice a year on 01 January and 01 July.</span></span> <span data-ttu-id="e8320-108">Der Zinssatz zwischen Unternehmen (B2B) wird von beiden Parteien vereinbart und dort ist keine Begrenzung zu dieser Debitorengruppe.</span><span class="sxs-lookup"><span data-stu-id="e8320-108">The interest rate between businesses (B2B) is agreed by the parties and there is no limit to that customer group.</span></span> <span data-ttu-id="e8320-109">Der angekündigte Kurs ist normalerweise vier Prozent mehr als die normalen Bankzinsen.</span><span class="sxs-lookup"><span data-stu-id="e8320-109">The announced rate is usually four percent more than the normal bank interest.</span></span>

<span data-ttu-id="e8320-110">Wenn Sie Zinskonditionen und Mahnmethoden für verspätete Zahlungen einrichten, können Sie mehrere Zinssätzen angeben, damit die Strafgebühr aus verschiedenen Zinssätzen in verschiedenen Perioden berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e8320-110">When you create finance charge terms and reminder terms, for delayed payment penalty, you can specify multiple interest rates so that the penalty fee is calculated from different interest rates in different periods.</span></span> <span data-ttu-id="e8320-111">Weitere Informationen finden Sie unter [Offene Salden eintreiben](receivables-collect-outstanding-balances.md)</span><span class="sxs-lookup"><span data-stu-id="e8320-111">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>

## <a name="to-set-up-multiple-interest-rates"></a><span data-ttu-id="e8320-112">Einrichten mehrerer Zinssätze.</span><span class="sxs-lookup"><span data-stu-id="e8320-112">To set up multiple interest rates</span></span>  
1.  <span data-ttu-id="e8320-113">Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Zinskonditionen** ein, und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="e8320-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e8320-114">Auf der Seite **Zinskonditionen** wählen Sie den gewünschten Finanzausdruck, und wählen die Aktion **Zinssätze**.</span><span class="sxs-lookup"><span data-stu-id="e8320-114">On the **Finance Charge Terms** page, select the required finance term, and then choose the **Interest Rates** action.</span></span>  
3.  <span data-ttu-id="e8320-115">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="e8320-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="e8320-116">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e8320-116">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="e8320-117">Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Mahnmethoden** ein und wählen Sie dann den entsprechenden Link.</span><span class="sxs-lookup"><span data-stu-id="e8320-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="e8320-118">Auf der Seite **Mahnbestimmungen** wählen Sie die gewünschte Mahnbestimmung und wählen die Aktion **Stufen** aus.</span><span class="sxs-lookup"><span data-stu-id="e8320-118">On the **Reminder Terms** page, select the required reminder term, and then choose the **Levels** action.</span></span>  
7.  <span data-ttu-id="e8320-119">Auf der Seite **Mahnstufen** wählen Sie das Feld **Zins berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="e8320-119">On the **Reminder Levels** page, select the **Calculate Interest** field.</span></span>  

<span data-ttu-id="e8320-120">Wenn Sie eine Zinsrechnung registrieren, wird deren Registrierung die Zinsrechnungen mit mehreren Zinssätzen während eines bestimmten Zeitraums anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e8320-120">When you issue a finance charge memo, the memo shows the finance charges with multiple interest rates for a specific time period.</span></span> <span data-ttu-id="e8320-121">Die Mahnung enthält ausserdem die Kontaktdetails des Debitors, des Unternehmens, das die Mahnung ausgibt, den Zusatzbetrag und den Gesamtbetrag.</span><span class="sxs-lookup"><span data-stu-id="e8320-121">The memo also contains the contact details of the customer, the company issuing the memo, the additional amount, and the total amount.</span></span> <span data-ttu-id="e8320-122">Der Eröffnungsposten der Zinsrechnung wird fett angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e8320-122">The opening entry on the memo is displayed in bold.</span></span> <span data-ttu-id="e8320-123">Die Zinsrechnungen werden mit verschiedenen Zinssätzen für eine bestimmte Periode berechnet und werden nach dem Eröffnungsposten der Mahnung gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e8320-123">The finance charges are calculated with multiple interest rates for a specific time period and are printed after the opening entry of the memo.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e8320-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8320-124">See Also</span></span>  
[<span data-ttu-id="e8320-125">Einziehen von Restbeträgen</span><span class="sxs-lookup"><span data-stu-id="e8320-125">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="e8320-126">Finanzen einrichten</span><span class="sxs-lookup"><span data-stu-id="e8320-126">Setting Up Finance</span></span>](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]