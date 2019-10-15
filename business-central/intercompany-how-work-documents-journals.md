---
title: Buchen Sie Intercompany-Belege und Buch.-Blätter | Microsoft Docs
description: Verwenden von Intercompanybelegen zum Buchen der Transaktionen zwischen Intercompanypartnern
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0b53d1af23051ae2ac5f54a921e8fca36263d777
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300027"
---
# <a name="work-with-intercompany-documents-and-journals"></a>Arbeiten mit Intercompany-Belegen und -Erfassungsjournalen
Intercompanybelege bzw. -Erf.-Journale werden zum Buchen der Transaktionen zwischen Intercompanypartnern verwendet. Wenn Sie einen Intercompanybeleg oder eine Erf.-Journalzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

Für Verkaufsaufträge und Einkaufsbelege stellt der IC-Partnercode auf den entsprechenden Debitor oder Kreditor sicher, dass alle Aufträge und Rechnungen, die Transaktionen mit diesen Unternehmen generiert haben, entsprechende Belege in dem Partnerunternehmen, werden mit dem Ergebnis des Ausgleichs die richtigen Konten.

Für Intercompany-Fibu Erfassungsjournalzeilen müssen Sie nicht die Konten für einen einzelnen Satz von Büchern angeben, sondern einfach die ID des Partnerunternehmens. Entsprechende Intercompany-Fibu-Erfassungsjournalzeilen daraufhin werden erstellt, die - sobald sie gebucht wurden - im Kontenabschluss beider Mandanten, die an einer Transaktion beteiligt sind, resultieren.

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a>Einen Intercompanyauftrag ausfüllen und senden:
Aufträge, Bestellungen und Rücksendungen können vor der Buchung gesendet werden. Rechnungen und Gutschriften können jedoch erst gesendet werden, nachdem sie gebucht sind.

Im Folgenden wird beschrieben, wie ein Intercompanyauftrag ausgefüllt und gesendet wird. Die gleichen Schritte gelten auch für Intercompanybestellungen und Reklamationen und Intercompanyrechnungen auf Rechnungen und Gutschriften.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.  
2. Um neue Verkaufsaufträge zu erstellen, wählen Sie **Neu**. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Stellt sicher, dass der Debitor ein Intercompany-Partner ist.
5. Um den Verkaufsauftrag zu senden, bevor Sie ihn buchen, wählen Sie die **IC Verkaufsauftrag senden** Aktion aus.

> [!NOTE]
> Wenn Sie Schritt 4 ausführen, wird der Verkaufsauftrag auf den Intercompany-Ausgang verschoben, wo er später gebucht werden kann. Weitere Informationen finden Sie unter [Verwalten des IC-Eingangs und Ausgangs](intercompany-how-manage-intercompany-inbox.md).

## <a name="to-fill-in-and-post-an-intercompany-journal"></a>Intercompany-Erfassungsjournale ausfüllen und buchen:
Wenn Sie einen Intercompany-Fibu-Erf.-Journalzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Intercompany allgemeines Buch.Blatt** ein, und wählen dann den zugehörigen Link aus.  
2. Öffnet das entsprechende Fibu-Erf.-Journal Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)
3. Füllen Sie die Felder je nach Bedarf aus.
4. Geben Sie im Feld **IC Partner-Fibukontonr.** das IC-Fibukonto ein, auf das der Betrag beim Partnerunternehmen gebucht wird.

    > [!NOTE]
    > Das Feld muss auf einer Zeile mit einem Bank- bzw. Fibukonto im Feld **Kontonr.** oder **Gegenkontonr.** ausgefüllt werden.  
5. Wählen Sie die Aktion **Buchen** aus.

Die entsprechenden Posten werden im Unternehmen gebucht und ein Erf.-Journal mit den entsprechenden Posten werden in den Intercompanyausgang erstellt, die Sie an das Partnerunternehmen senden können. Weitere Informationen finden Sie unter [Verwalten des IC-Eingangs und Ausgangs](intercompany-how-manage-intercompany-inbox.md).

## <a name="see-also"></a>Siehe auch
[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)A  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
