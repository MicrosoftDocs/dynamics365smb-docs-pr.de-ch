---
title: "Einrichten von Verkaufschancen für Verkaufsprozesse und Prozess-Stufen| Microsoft Docs"
description: Beschreibt, wie Verkaufsstufen, vom ersten Kontakt bis zum Schliessen definiert, einen Verkaufsprozess erstellt und diesen zu Verkaufschancen in Finance and Operations, Business edition zuweist.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ecff2e9e0705055a514f1726b3223f8196300cb6
ms.contentlocale: de-ch
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Einrichten von Verkaufsprozessen für Verkaufschancen und Prozess-Stufen
Damit die Verkaufschancen verwendet werden kann, müssen zunächst Verkaufsprozesse sowie Verkaufsprozess-Stufen eingerichtet werden. Ein Verkaufsprozess setzt sich aus einer Reihe von Schritten zusammen, die vom ersten Kontakt bis zu einem Verkaufsabschluss reichen. Jeder Stufe kann bestimmten Bedingungen haben, die erfüllen sein müssen (z. B. eine Verkaufsofferte), bevor eine Verkaufschance in die nächste Stufe gehen kann. Sie können auch festlegen, ob eine Stufe übersprungen werden kann. Verkaufsprozesse können in beliebiger Anzahl eingerichtet werden. Gleiches gilt auch für die Anzahl der Verkaufsprozess-Stufen, die innerhalb eines Verkaufsprozesses eingerichtet werden.

Das Implementieren des Verkaufsprozesses für Verkaufschancen umfasst das Einrichten des Verkaufsprozesscodes, das Definiert der verschiedenen Stufen des Zyklus, und das Zuweisen des Zyklus zu den Verkaufschancen. Durch Zuweisen der relevanten Aktivität der Verkaufschance oder Aufgaben kann auch ein Teil des Einrichtens eines Verkaufsprozesses sein.

Dieses Thema beschreibt auch Entscheidungsträgern als Einrichtungsaufgaben und die Aktivitäten und wie Aufgaben zu den Aktionen zugewiesen werden. Weitere Informationen finden Sie unter "Aktivitäten mit Aufgaben" einrichten.

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Um Verkaufschancen-Zykluscodes einzurichten:
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufzyklus** ein. Wählen Sie dann den zugehörigen Link aus. Das **Verkaufsprozesse**-Fenster wird geöffnet und führt alle vorhandenen Verkaufsprozesse auf.
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Wiederholen Sie diese Schritte, um weitere Verkaufsprozesse einzurichten. Nachdem Sie Verkaufsprozesse für Verkaufschancen eingerichtet haben, können Sie die verschiedenen Stufen innerhalb jedes Prozesses einrichten.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Verkaufsprozessstufe der Verkaufschance definieren
1. Wählen Sie im Fenster **Verkaufsprozesse** den Verkaufsprozess für Verkaufschancen aus, für den Sie Stufen einrichten möchten, und wählen Sie dann die Aktion **Stufen**. Das Fenster **Verkaufsprozess-Stufen** wird geöffnet.
2. Klicken Sie auf **Neu**, um eine neue Stufe für den Verkaufsprozess einzugeben.

Wiederholen Sie diese Schritte, um beliebig viele Stufen innerhalb des Verkaufsprozesses einzurichten.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Eine Verkaufsprozessstufe zu einer Verkaufschance zuordnen
Nachdem Sie die Stufe des Verkaufprozesses hinzugefügt haben, können Sie Verkaufschancen hinzufügen und dann die Stufe des Verkaufprozesses zu Verkaufschancen hinzufügen, indem Sie das Feld **Verkaufsprozesscode** verwenden. Weitere Informationen finden Sie unter [Erstellen von Verkaufschancen](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Um Aktionen mit Aufgaben einzurichten
Sie können mehrere Aufgabe, zum Beispiel Tätigkeiten kombinieren, die jede einen Schritt darstellen in den Aktivitäten. Alle Schritte innerhalb einer Aktion sind durch ein Datenformular miteinander verbunden. Sie können Aktionen Verkaufschancen, Verkäufern bzw. den Kontakten zuweisen.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufzyklus** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus.
3. Im Inforegister **Zeilen** geben Sie die notwendigen Felder ein, um eine oder mehrere Aufgaben in der Aktivität zu definieren.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Um Aufgaben oder Aktionen von Aufgaben zu Verkaufschancen zuzuweisen
Wenn Sie eine Aufgabe eingerichtet haben, können Sie sie in einer Verkaufschance zuordnen und die Aktivität zuweisen, zu der die Aufgabe gehört.

> [!NOTE]  
>   Diese Vorgehensweise beschreibt, wie Sie Aktivitätsaufgaben zu Verkaufschancen zuweisen. die Schritte sind ähnlich, wenn Sie Verkäufer und den Kontakten Aufgaben zuordnen.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Chancen** ein und wählen den zugehörenden Link aus.
2. Wählen Sie eine Chance und wählen Sie dann die Aktion **Aufgaben** aus.
3. Wählen Sie im Fenster **Aufgabenliste** die Aktion **Aufgabe erstellen**.
4.  Füllen Sie im Fenster **Aufgabe erstellen** die Felder wie benötigt aus.

    Beachten Sie im Feld **Verkaufschance**, dass es automatisch der Verkaufschance zugewiesen wird.
5. Wählen Sie die Schaltfläche **OK** aus.
6. Im **Aufgabenlisten**-Fenster wählen Sie die Verkaufschance und dann die **Aktivität zuweisen**-Aktion aus.
7. Im Fenster **Aktivität zuweisen** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.

## <a name="see-also"></a>Siehe auch
[Verarbeiten von Verkaufschancen](marketing-processing-sales-opportunities.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

