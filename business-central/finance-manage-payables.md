---
title: Verwalten von Verbindlichkeiten| Microsoft Docs
description: Überblick darüber, wie Sie Verbindlichkeiten inklusive Kreditorenzahlungen, Gläubiger, Schulden und den fälligen Saldo verwalten.
services: project-madeira
documentationcenter: ''
author: bholtorf
manager: edupont
editor: ''
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 04/01/2019
ms.author: bholtorf
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: f7556b204403f0abdb6361a0e1650b90e58810e1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238891"
---
# <a name="managing-payables"></a>Verwalten von Verbindlichkeiten
[!INCLUDE[d365fin](includes/d365fin_md.md)] hat alles, was Sie brauchen, um Ihre Verbindlichkeiten effektiv zu verwalten.  

## <a name="payments"></a>Zahlungen
Es ist einfach, Zahlungen zu priorisieren, Gebühren für überfällige Zahlungen zu bezahlen und Skonto für frühzeitige Zahlungen zu berücksichtigen.

Sie können Zahlungen in einem Fibu Erf.-Journal erfassen und anschliessend drucken und überprüfen, bevor das Zahlungsausgangs Erf.-Journal gedruckt wird.

Eine Zahlung kann mit der entsprechenden Rechnung beim Buchen der Zahlung oder auch erst nach dem Buchen der Zahlung ausgeglichen werden. Mit dem Feld **Ausgleichsmethode** für den Kreditor (auf der **Kreditorenkarte**) wird festgelegt, ob ein manueller Ausgleich erforderlich ist oder ob der Ausgleich automatisch vorgenommen wird. Die Verwendung des manuellen Ausgleichs von Transaktionen ist immer möglich. Ist jedoch als Ausgleichsmethode für den Kreditor die Option **Saldomethode** festgelegt, und es wird kein Beleg für den Zahlungsausgleich angegeben, wird die Zahlung mit dem ältesten offenen Posten für den Kreditor ausgeglichen.

## <a name="suggest-vendor-payments"></a>Zahlungsvorschlag
[!INCLUDE[d365fin](includes/d365fin_md.md)] kann verschiedene Zahlungen an Kreditoren vorschlagen, wie Zahlungen, die in Kürze fällig sind, oder Zahlungen, bei denen ein Rabatt verfügbar ist. Der Zahlungsvorschlag kann einen bestimmten Betrag berücksichtigen, der für Zahlungen zur Verfügung steht und die Möglichkeit, einen Rabatt für fristgerechte Zahlung zu erhalten.

## <a name="issue-checks"></a>Schecks ausstellen
[!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie Schecks an Kreditoren manuell und elektronisch erstellen. Sie machen beides auf der Seite **Zlg.-Ausg. Buch.-Blätter**, in dem Sie auch Schecks annullieren und Scheckposteneinträge anzeigen können.

## <a name="export-payments-to-a-bank-file"></a>Zahlungen in eine Bankdatei exportieren
Wenn Sie bereit sind, Zahlungen an Ihre Kreditoren auf der Seite **Zahlung Erf.-Journal** vorzunehmen, können Sie eine Datei mit den Zahlungsinformationen aus den Erfassungsjournalzeilen exportieren. Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten.

Wenn Sie keine Erf.-Journalzeile für eine exportierte Zahlung buchen möchten, weil Sie beispielsweise eine Bestätigung erwarten, dass die Transaktion von der Bank verarbeitet wurde, können Sie die Erf.-Journalzeile einfach löschen. Falls Sie später eine Buch.-Blattzeile erstellen, um den Restbetrag der gebuchten Rechnung zu bezahlen, zeigt das **Exportierter Betrag gesamt**-Feld, wie viel des Zahlungsbetrags bereits exportiert wurde. Detaillierte Informationen über die exportierte Summe können Sie auch finden, indem Sie die Schaltfläche **Posten im Kreditübertragungsjournal** auswählen, um Einzelheiten zu Dateien der exportierten Zahlung anzuzeigen.

Wenn Sie abwarten, um Zahlungen zu buchen, bis die Bank bestätigt, dass Transaktionen verarbeitet wurden, gibt es zwei Möglichkeiten zu vermeiden, dass Zahlungen für fällige Belege versehentlich erneut exportieren werden.  

* In einem Zahlungsausgangs-Buch.-Blatt mit vorgeschlagenen Zahlungszeilen, können Sie entweder nach der **In Zahlungsdatei exportiert**-Spalte oder nach **Exportierter Betrag gesamt** sortieren, und dann Zahlungsvorschläge für offene Rechnungen, für die bereits Zahlungen geleistet wurden und für die Sie keine Zahlungen leisten möchten, löschen.

    **Hinweis** Möglicherweise müssen Sie diese Spalten der Liste hinzufügen. Weitere Informationen finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).  
* Alternativ können Sie in der Stapelverarbeitung **Zahlungsvorschläge für Kreditoren**, in der Sie festlegen, welche Zahlungen in das Zahlungsausgangs Buch.-Blatt einzufügen sind, das Kontrollkästchen **Exportierte Zahlungen überspringen** aktivieren, wenn Sie keine Buch.-Blattzeilen für Zahlungen einfügen möchten, die bereits exportiert wurden.

## <a name="see-also"></a>Siehe auch
[Zahlungsformen](finance-payment-methods.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
