---
title: Verwalten von Verbindlichkeiten| Microsoft Docs
description: "Überblick darüber, wie Ihnen Financials hilft, Verbindlichkeiten inklusive Kreditorenzahlungen, Gläubiger, Schulden und geschuldete Beträge zu verwalten."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-financials
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 859647435fe3a418761f67c9067314939c734519
ms.contentlocale: de-ch
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a>Verwalten von Verbindlichkeiten
[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] hat alles, was Sie brauchen, um Ihre Verbindlichkeiten effektiv zu verwalten.  

## <a name="payments"></a>Zahlungen
Es ist einfach, Zahlungen zu priorisieren, Gebühren für überfällige Zahlungen zu bezahlen und Skonto für frühzeitige Zahlungen zu berücksichtigen.

Sie können Zahlungen in einem Fibu Erf.-Journal erfassen und anschliessend drucken und überprüfen, bevor das Zahlungsausgangs Erf.-Journal gedruckt wird.

Eine Zahlung kann mit der entsprechenden Rechnung beim Buchen der Zahlung oder auch erst nach dem Buchen der Zahlung ausgeglichen werden. Mit dem Feld **Ausgleichsmethode** für den Kreditor (auf der **Kreditorenkarte**) wird festgelegt, ob ein manueller Ausgleich erforderlich ist oder ob der Ausgleich automatisch vorgenommen wird. Die Verwendung des manuellen Ausgleichs von Transaktionen ist immer möglich. Ist jedoch als Ausgleichsmethode für den Kreditor die Option **Saldomethode** festgelegt, und es wird kein Beleg für den Zahlungsausgleich angegeben, wird die Zahlung mit dem ältesten offenen Posten für den Kreditor ausgeglichen.

## <a name="suggest-vendor-payments"></a>Zahlungsvorschlag
[!INCLUDE[d365fin](includes/d365fin_md.md)] kann verschiedene Zahlungen an Kreditoren vorschlagen, wie Zahlungen, die in Kürze fällig sind, oder Zahlungen, bei denen ein Rabatt verfügbar ist. Der Zahlungsvorschlag kann einen bestimmten Betrag berücksichtigen, der für Zahlungen zur Verfügung steht und die Möglichkeit, einen Rabatt für fristgerechte Zahlung zu erhalten.

## <a name="issue-checks"></a>Schecks ausstellen
[!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie Schecks an Kreditoren manuell und elektronisch erstellen. Sie machen beides im Fenster **Zlg.-Ausg. Buch.-Blätter**, in dem Sie auch Schecks annullieren und Scheckposteneinträge anzeigen können.

## <a name="export-payments-to-a-bank-file"></a>Zahlungen in eine Bankdatei exportieren
Wenn Sie bereit sind, Zahlungen an Ihre Kreditoren im Fenster **Zahlung Buch.-Blatt** vorzunehmen, können Sie eine Datei mit den Zahlungsinformationen aus den Buch.-Blattzeilen exportieren. Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten.

Wenn Sie keine Erf.-Journalzeile für eine exportierte Zahlung buchen möchten, weil Sie beispielsweise eine Bestätigung erwarten, dass die Transaktion von der Bank verarbeitet wurde, können Sie die Erf.-Journalzeile einfach löschen. Falls Sie später eine Buch.-Blattzeile erstellen, um den Restbetrag der gebuchten Rechnung zu bezahlen, zeigt das **Exportierter Betrag gesamt**-Feld, wie viel des Zahlungsbetrags bereits exportiert wurde. Detaillierte Informationen über die exportierte Summe können Sie auch finden, indem Sie die Schaltfläche **Posten im Kreditübertragungsjournal** auswählen, um Einzelheiten zu Dateien der exportierten Zahlung anzuzeigen.

Wenn Sie abwarten, um Zahlungen zu buchen, bis die Bank bestätigt, dass Transaktionen verarbeitet wurden, gibt es zwei Möglichkeiten zu vermeiden, dass, Zahlungen für fällige Belege versehentlich erneut exportieren werden.  

* In einem Zahlungsausgangs-Buch.-Blatt mit vorgeschlagenen Zahlungszeilen, können Sie entweder nach der **In Zahlungsdatei exportiert**-Spalte oder nach **Exportierter Betrag gesamt** sortieren, und dann Zahlungsvorschläge für offene Rechnungen, für die bereits Zahlungen geleistet wurden und für die Sie keine Zahlungen leisten möchten, löschen.

    **Hinweis** Möglicherweise müssen Sie diese Spalten der Liste hinzufügen. Weitere Informationen finden Sie unter [Benutzer-Personalisierung](ui-user-personalization.md).  
* Alternativ können Sie in der Stapelverarbeitung **Zahlungsvorschläge für Kreditoren**, in der Sie festlegen, welche Zahlungen in das Zahlungsausgangs Buch.-Blatt einzufügen sind, das Kontrollkästchen **Exportierte Zahlungen überspringen** aktivieren, wenn Sie keine Buch.-Blattzeilen für Zahlungen einfügen möchten, die bereits exportiert wurden.

## <a name="see-also"></a>Siehe auch
[Zahlungsformen](finance-payment-methods.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

