---
title: "Zahlungen tätigen| Microsoft Docs"
description: Zahlungen vornehmen
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f6721c0359b4499a597b349a280afb56818a1f28
ms.contentlocale: de-ch
ms.lasthandoff: 05/04/2017


---
# <a name="make-payments"></a>Zahlungen vornehmen
Wenn Sie Zahlungen an Kreditoren leisten, buchen Sie die jeweiligen Zahlungszeilen im **Zahlungsausgangs-Erfassungsjournal**-Fenster. Verwenden Sie zum Suchen fälliger Zahlungen im Zahlungsausgangs Buch.-Blatt die Funktion **Zahlungsvorschlag**. Darüber hinaus können Sie sich mithilfe des Berichts **Kreditor - Saldo nach Perioden** einen Überblick über die fälligen Zahlungen verschaffen.

Im Zahlungsausgangs-Erfassungsjournal können Sie Computerschecks drucken sowie ausgestellte Schecks erfassen. Wenn Sie **Computer Scheck** im Feld **Bankkontozahlungsart** wählen, dann müssen alle Posten für Schecks gedruckt werden, damit die Erfassungsjournalzeilen gebucht werden können.

Wenn Zahlungen gebucht werden, exportieren Sie sie in eine Bankdatei für den Upload zu Ihrer Bank zur Verarbeitung.

Nachdem die Zahlungen in Ihrer Bank getätigt wurden, müssen Sie diese in ihre entsprechenden offenen Kreditorenposten ausgleichen. Sie können dies manuell oder über den Import in eine Bankkontoauszugsdatei und das Automatische Ausgleichen der Zahlungen durchführen. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

| Aktion | Informationen |
| --- | --- |
| Verwenden Sie die Funktion, um Kreditorenzahlungen entsprechend gewählten Kriterien, wie Fälligkeitsdatum, Skontoeignung und Ihrer Liquidität vorzuschlagen. |[Vorgehensweise: Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md) |
| Stellen Sie Schecks für Zahlungen entweder als Ausdruck oder als Computer Schecks aus. Annullieren Sie Schecks vor oder nach dem Buchen. |[So gehts: Arbeiten mit Schecks](payables-how-work-checks.md) |
| Um sicherzustellen, dass Ihre Bank nur Schecks und Beträge freigibt, können Sie ihr eine Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält. |[Erneuter Positive Pay-Export in Datei](finance-how-positive-pay.md) |
|Exportzahlungen aus dem **Zahlungsausgangs Buch.-Blatt** in eine Bank archivieren, das Sie für Ihre Bank für das Verarbeiten hochladen, einschließlich EFT (elektronischer Geldtransfer) in Nordamerika. |[Vorgehensweise: Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a>Siehe auch
[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]  

