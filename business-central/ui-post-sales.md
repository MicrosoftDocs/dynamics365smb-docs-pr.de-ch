---
title: Verkaufsbelege buchen | Microsoft Docs
description: Erfahren Sie mehr über die verschiedenen Buchungsfunktionen zum Buchen von Verkaufsbelegen und wie Sie gebuchte Belege aktualisieren können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 12/03/2020
ms.author: edupont
ms.openlocfilehash: fa2830aeb62fe6acea5f8e3879c678e9d8407fb4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760331"
---
# <a name="posting-sales"></a>Verkäufe buchen

Unter dem Menü **Buchen** in einem Verkaufsbeleg auswählen können Sie zwischen den folgenden Buchungsfunktionen auswählen:

* **Veröffentlichen**
* **Buchen und neu**
* **Buchen und senden**
* **Buchungsvorschau**
* **Stapelbuchung**
* **Testbericht**

> [HINWEIS!] Bei Kundenaufträgen werden auch Optionen für die Vorauszahlungsfunktion angezeigt. Weitere Informationen finden Sie unter [Vorauszahlungen in Rechnung stellen](finance-invoice-prepayments.md). 

Wenn Sie alle Zeilen ausgefüllt und alle Daten des Verkaufsauftrags eingegeben haben, können Sie ihn buchen. Dies erstellt eine Lieferung und eine Rechnung.

Wenn eine Verkaufsbestellung gebucht wird, werden das Debitorenkonto, die Fibuposten und die Lagerposten aktualisiert.

Für jeden Verkaufsauftrag wird ein Verkaufsposten in der Tabelle **Fibuposten** erstellt. Darüber hinaus wird ein Posten in der Tabelle **Kreditorenposten** erzeugt und ein Sachposten im entsprechenden Einkaufskonto. Zusätzlich kann das Buchen in einem MWST.-Posten und einem Fibuposten für den Rabattbetrag resultieren. Ob ein Posten für Rabatt gebucht wird, hängt von den Einstellungen im Feld **Rabattbuchung** auf der Seite **Debitoren & Verkauf Einr.** ab.

Für jede Zeile des Verkaufsauftrags wird ein Lagerposten in der Tabelle **Lagerposten** erzeugt (wenn die Verkaufszeilen Artikelnummern enthalten) oder es wird ein Fibuposten in der Tabelle **Fibuposten** erzeugt (wenn die Verkaufszeilen Fibukonten enthalten). Zusätzlich dazu werden Verkaufsaufträge immer in den Tabellen **Verkaufslieferkopf** und **Verkaufsrechnungskopf** gespeichert.

> [!IMPORTANT]  
> Wenn Sie einen Auftrag buchen, können Sie sowohl einen Lieferschein als auch eine Rechnung erzeugen. Dies kann gleichzeitig oder unabhängig voneinander getan werden. Sie können auch eine Teillieferung und eine Teilrechnung erzeugen, indem Sie die Felder **Zu liefernde Menge** und/oder **Zu fakturierende Menge** in den jeweiligen Zeilen des Verkaufsauftrags ausfüllen, bevor Sie buchen. Beachten Sie, dass Sie keine Rechnung ausstellen können, solange die entsprechende Lieferung nicht erfolgt ist. Bevor Sie also die Fakturierung durchführen können, müssen Sie einen Lieferschein erstellt oder die Funktion zur gleichzeitigen Lieferung und Fakturierung gewählt haben.

Sie können entweder buchen oder buchen und senden. Wenn Sie die Option wählen, zu buchen und zu senden, wird eine PDF-Datei generiert, die Sie dann senden können. Sie können auch die Funktion **Stapelbuchen** wählen, mit der Sie mehrere Aufträge gleichzeitig buchen können. Weitere Informationen finden Sie unter [Mehrere Belege gleichzeitig bereitstellen ](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Anzeigen von Posten

Wenn die Buchung vollständig ist, werden die gebuchten Verkaufszeilen aus der Bestellung entfernt. Eine Meldung erscheint, die Ihnen mitteilt, dass die Buchung vollständig ist. Im Anschluss können Sie die gebuchten Posten auf den verschiedenen Seiten einsehen, die gebuchte Posten enthalten, einschliesslich **Debitorenposten**, **Fibuposten**, **Lagerposten**, **Lagerplatzposten**, **Geb. Verkaufsrechnung**.  

In den meisten Fällen können Sie Posten von der betroffenen Karte oder dem betroffenen Beleg aus öffnen. Auf der Seite **Debitorenkarte** wählen Sie beispielsweise die Aktion **Posten** aus.

## <a name="editing-ledger-entries"></a>Bearbeiten von Posten

Sie können bestimmte Felder in gebuchten Einkaufsbelegen bearbeiten, z. B. die **Pakettrackingnr.** Feld eingetragen. Weitere Informationen finden Sie unter [Gebuchte Belege bearbeiten](across-edit-posted-document.md). Bei kritischeren Feldern, die sich auf den Überwachungspfad auswirken, müssen Sie die Buchung stornieren oder rückgängig machen. Weitere Informationen finden Sie unter [Erf.-Journalbuchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Mehrere Belege gleichzeitig buchen](ui-batch-posting.md)  
[Gebuchte Belege bearbeiten](across-edit-posted-document.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Ändern oder Löschen einer unbezahlten Verkaufsrechnung](sales-how-correct-cancel-sales-invoice.md)  
[Suchen von Seiten und Informationen mit Wie möchten Sie weiter verfahren](ui-search.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]