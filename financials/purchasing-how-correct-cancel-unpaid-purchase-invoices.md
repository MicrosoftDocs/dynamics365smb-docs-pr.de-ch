---
title: "Ändern oder Löschen einer unbezahlten Einkaufsrechnung| Microsoft Docs"
description: "Erklärt, wie automatisch eine Einkaufsgutschrift korrigiert, abgebrochen oder rückgängig gemacht wird und eine gebuchte Einkaufsrechnung erstellt wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 53800a9fe42934807c551e81098eda768f4f1542
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a>Vorgehensweise: Ändern oder Löschen einer unbezahlten Einkaufsrechnung
Sie können eine bezahlte Einkaufsrechnung korrigieren oder abbrechen. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn Sie den Kauf früh im Bestellvorgang ändern möchten.

Wenn Sie bereits für Produkte auf der gebuchten Einkaufsrechnung bezahlt haben, können Sie diese aus der gebuchten Einkaufsrechnung selbst nicht korrigieren oder stornieren. Stattdessen müssen Sie eine Einkaufsgutschrift manuell erstellen, um den Einkauf zu stornieren, optional verwaltet mit einer Einkaufsreklamation. Weitere Informationen finden Sie unter [Vorgehensweise: Einkaufsretouren verarbeiten oder Stornieren](purchasing-how-process-purchase-returns-cancellations.md).

Im Fenster **Geb. Einkaufsrechnung** können Sie die Schaltfläche **Korrigieren** oder **Stornieren** wählen. Wenn Sie eine gebuchte Einkaufsrechnung korrigieren oder stornieren, wird sie in allen Sach- und Inventurposten angewendet, die erstellt wurden, als die erste Einkaufsrechnung gebucht wurde. Dadurch wird die gebuchte Einkaufsrechnung in Ihren Finanzdatensätzen storniert und verlässt die gebuchte Korrektureinkaufsgutschrift für Ihr Protokoll. Nachfolgend wird die Verwendung von **Korrigieren** und **Stornieren** beschrieben.

## <a name="to-correct-a-posted-purchase-invoice"></a>Gebuchte Einkaufsrechnung korrigieren
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die gebuchte Einkaufsrechnung, die Sie korrigieren möchten.  

    > [!NOTE]  
>   Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Einkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.
3. Im Fenster **Gebuchte Einkaufsrechnung** wählen Sie **Korrekt** aus.

    Eine neue Verkaufsrechnung mit den gleichen Informationen wird erstellt, auf dem Sie die Korrektur machen können. Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md). Das Feld **Storniert** am Anfang gebuchten Einkaufsrechnung wird auf **Ja** geändert.

    Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu annullieren.
4. Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Einkaufsgutschrift anzuzeigen, die die gebuchte Einkaufsrechnung annulliert.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Gebuchte Einkaufsrechnung stornieren
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die gebuchte Einkaufsrechnung, die Sie stornieren möchten.

    > [!NOTE]  
>   Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Einkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.
3. Im Fenster **Gebuchte Einkaufsrechnung** wählen Sie **Stornieren** aus.

    Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu annullieren. Das Feld **Storniert** am Anfang gebuchten Einkaufsrechnung wird auf **Ja** geändert.
4. Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Einkaufsgutschrift anzuzeigen, die die gebuchte Einkaufsrechnung annulliert.

## <a name="see-also"></a>Siehe auch
[Einkauf](purchasing-manage-purchasing.md)  
[Vorgehensweise: Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

