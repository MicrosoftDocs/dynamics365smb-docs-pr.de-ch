---
title: Verstehen, wie Einkaufsbelege gebucht werden | Microsoft Docs
description: Erfahren Sie mehr über die verschiedenen Buchungsfunktionen zum Buchen von Einkaufsbelegen und wie Sie gebuchte Belege aktualisieren können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0fccda42a69cd1d1d7129380518890fac5b8986c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315098"
---
# <a name="posting-purchases"></a>Einkäufe buchen
Wenn Sie die Schaltfläche **Gruppe Buchen** in einem Einkaufsbeleg auswählen, können Sie zwischen den folgenden Buchungsfunktionen auswählen:

* **Veröffentlichen**
* **Buchungsvorschau**
* **Buchen und Drucken**
* **Testbericht**
* **Stapelbuchung**

Wenn Sie die Zeilen der Einkaufsbestellung ausgefüllt haben, können Sie sie buchen, d. h., eine Lieferung und eine Rechnung erzeugen.

Wenn eine Einkaufsbestellung gebucht wird, werden das Kreditorenkonto, die Fibuposten und die Lagerposten aktualisiert.

Für jede Einkaufsbestellung wird ein Einkaufsposten in der Tabelle **Fibuposten** erstellt. Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Fibuposten im entsprechenden Einkaufskonto. Zusätzlich kann das Buchen in einem MWST-Posten und einem Fibuposten für den Rabattbetrag resultieren. Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** auf der Seite **Kreditoren & Einkauf Einrichtung** ab.

Für jede Einkaufsbestellungszeile wird ein Lagerposten in der Tabelle **Lagerposten** erstellt (wenn die Einkaufszeilen Artikelnummern enthalten) oder es wird ein Fibuposten in der Tabelle **Fibuposten** erstellt (wenn die Einkaufszeilen eine Fibukontonummer enthalten). Zusätzlich werden Einkaufsbestellungen immer in den Tabellen **Einkaufslieferkopf** und **Einkaufsrechnungskopf** erfasst.

Bevor Sie buchen, können Sie einen Testbericht ausdrucken, der alle Daten der Einkaufsbestellung und etwaige Fehler enthält. Um den Bericht zu drucken, wählen Sie **Buchen** und wählen **Testbericht** aus.

> [!IMPORTANT]  
>   Wenn Sie eine Bestellung buchen, können Sie sowohl eine Lieferung als auch eine Rechnung erstellen. Dies kann gleichzeitig oder unabhängig voneinander durchgeführt werden. Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Zu liefernde Menge** und/oder **Zu fakturierende Menge** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen. Beachten Sie, dass Sie keine Rechnung für Mengen erstellen können, die noch nicht geliefert wurden. Das bedeutet, dass Sie vor der Fakturierung eine Lieferung gebucht haben müssen oder Sie müssen "Liefern und Fakturieren" wählen.

Sie können entweder buchen oder buchen und drucken. Wenn Sie sich entscheiden, zu buchen und zu drucken, wird ein Bericht gedruckt, wenn der Auftrag gebucht wird. Sie können auch die Funktion **Stapelbuchen** wählen, mit der Sie mehrere Aufträge gleichzeitig buchen können. Weitere Informationen finden Sie unter [Mehrere Belege gleichzeitig bereitstellen ](ui-batch-posting.md).

Wenn die Buchung vollständig ist, werden die gebuchten Einkaufszeilen aus der Bestellung entfernt. Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist. Im Anschluss können Sie die gebuchten Posten auf den verschiedenen Seiten einsehen, die gebuchte Posten enthalten (**Kreditorenposten**, **Fibuposten**, **Lagerposten**, **Lagerplatzposten**, **Einkaufsrechnung**).

Sie können bestimmte Felder in gebuchten Einkaufsbelegen bearbeiten, z. B. das Feld **Zahlungsreferenz**. Weitere Informationen finden Sie unter [Gebuchte Belege bearbeiten](across-edit-posted-document.md).

## <a name="see-also"></a>Siehe auch
[Gebuchte Belege bearbeiten](across-edit-posted-document.md)  
[Mehrere Belege gleichzeitig buchen](ui-batch-posting.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Journale und Belege buchen](ui-post-documents-journals.md)  
[Ändern oder Löschen einer unbezahlten Einkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Suchen von Seiten und Informationen mit Wie möchten Sie weiter verfahren](ui-search.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
