---
title: Zahlungsformen einrichten| Microsoft Docs
description: "Sie können Zahlungsmethoden nutzen, z.B. Banküberweisung, Kasse oder Paypal, um festzulegen, wie eine Rechnung bezahlt wird."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 11/22/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 8cac52a1cdd4e614c6e2ef8c027e5cf499926f9d
ms.contentlocale: de-ch
ms.lasthandoff: 11/26/2018

---
# <a name="defining-payment-methods"></a>Zahlungsformen definieren
Zahlungsmethoden definieren die Art, wie Sie es vorziehen, dass Debitoren Sie zahlen und wie Sie den Kreditoren bezahlen können. Die Methode kann für jeden Debitor oder Kreditor variieren. Beispiele für typische Zahlungsformen sind **Bankkonten**, **Bargeld**, **Check** oder **Konto**. 

Sie können eine Zahlungsmethode Debitoren und Kreditoren zuweisen, sodass dasselbe Verfahren  immer auf Verkaufs- und Einkaufsbelegen verwendet wird, die Sie für sie einrichten. Bei Bedarf können Sie die Methode im Einkaufs- und Verkaufsbeleg ändern. Wenn Sie beispielsweise eine bestimmte Einkaufsrechnung in bar anstatt mit Scheck bezahlen möchten. Dies verändert nicht die standardmässige Zahlungsform, die dem Kreditor zugeordnet ist.

Die gleichen Zahlungsformen werden für Einkaufs- und Verkaufsbelege verwendet. Beispielsweise wird eine_cash_ Zahlungsform verwendet, wenn Sie Zahlungen leisten und wenn Sie den Wareneingang erhalten. [!INCLUDE[d365fin](includes/d365fin_md.md)] weiss, dass wenn Sie eine Verkaufsrechnung erstellen, Sie eine Zahlung erwarten und das Gegenteil der Einkaufsrechnungen ist. 

Gutschriften für Reklamationen sind jedoch Ausnahmen, da Geld entgegengesetzt fliesst, von Ihnen an Ihren Kunden und von Ihrem Lieferanten an Sie. Daher wird eine standardmässige Zahlungsform nicht den Gutschriften zugeordnet. Es gibt eine Problemumgehung, wenn Sie Zahlungsfristen des Debitors oder Kreditors angegeben haben. Auch wenn das **Rechnungsrab. Zahl. Verk. im Zinsrechnung** Feld nicht für dies beabsichtigt ist, wenn Sie das Feld **Zahlungsbedingungen** auswählen, wird eine standardmässige Zahlungsform hinzugefügt, wenn Sie eine Gutschrift erstellen.

## <a name="to-set-up-a-payment-method"></a>So richten Sie eine Zahlungsmethode ein
[!INCLUDE[d365fin](includes/d365fin_md.md)] enthält mehrere Zahlungsformen, die Geschäfte häufig verwenden. Sie können so viele Zeilen hinzufügen, wie Sie benötigen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Zahlungsvmethode** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>So weisen Sie einem Kreditor eine Zahlungsmethode zu
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") geöffnet wird. Geben Sie **Debitor** oder **Verkäufer** ein und wählen Sie den zugehörigen Link aus.
2. Im **Zahlungsform** Feld wählen Sie die Methode, die Sie für den Debitor oder Kreditor standardmässig verwenden möchten.

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

