---
title: Wie man Kommissionierungen in Arbeitsblättern plant
description: Erfahren Sie, wie Zeilen in Versandbelegen auf Kommissionierarbeitsblättern für Lagermitarbeiter verfügbar gemacht werden können.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/13/2021
ms.author: edupont
ms.openlocfilehash: 667aa2702d064e44b9b52dc167e2372f98d7944f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530421"
---
# <a name="plan-picks-in-worksheets"></a>Kommissionierungen in Arbeitsblättern bearbeiten

Wenn Ihr Lager so eingerichtet ist, dass sowohl die Kommissionier- als auch die Versandabwicklung erforderlich ist, können Sie Zeilen in den Versandbelegen anstelle von Kommissionieranweisungen auf Kommissionierarbeitsblättern verfügbar machen.  

> [!NOTE]  
> Wenn bereits Kommissionieranweisungen erstellt wurden und Sie diese zu einer Kommissionieranweisung kombinieren möchten, müssen Sie die einzelnen Kommissionierungen löschen. Die Zeilen, die kommissioniert werden sollen, können jetzt im Kommissionierarbeitsblatt aufgelistet werden.  

Auf der Seite **Kommissionierarbeitsblätter** können Sie Kommissionierlisten einrichten, die den Mitarbeitern beim Sammeln von Artikeln im Lager helfen. Die Seite zeigt die in Crossd.-Lagerplätzen verfügbaren Mengen an, was für die Planung von Arbeitseinsätzen in Crossd.-Situationen nützlich ist. [!INCLUDE[prod_short](includes/prod_short.md)] wird immer zuerst eine Entnahme aus einem Crossd.-Lagerplatz vorschlagen. Die Zeilen im Arbeitsblatt können aus mehreren Quellbelegen stammen. Sie können beispielsweise aus mehr als einem Verkaufsauftrag stammen. 

> [!NOTE]  
> Die Kommissionierung für einen Verkaufsautrag, der die mit dem betreffenden Verkaufsauftrag montiert werden, folgt denselben Schritten wie die reguläre Kommissionierung für den Warenausgang, die in diesem Thema beschrieben ist. Jedoch kann die Anzahl der Kommissionierzeilen pro zu liefernder Menge n:1 sein, da die Kommissionierung für die Komponenten, nicht für den Montageartikel erfolgt.  
>
> Die Kommissionierzeilen werden für den Wert im Feld **Restmenge** in den Zeilen des Montageauftrags erstellt, der mit der Verkaufsauftragszeile verknüpft ist, die geliefert wird. Dadurch ist sichergestellt, dass alle Komponenten in einer Aktion kommissioniert werden. Weitere Informationen finden Sie unter [Verkaufen von Lagerartikeln in Programmfertigungs-Flow](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)  
>
> Allgemeine Informationen über das Kommissionieren von Komponenten für Montageaufträge, einschliesslich von Situationen, in denen der Montageartikel nicht mit einer Verkaufslieferung fällig ist, finden Sie unter [Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="sorting-lines-on-a-pick-worksheet"></a>Sortieren von Zeilen auf einem Kommissionierarbeitsblatt

Sie können Positionen nach Artikel, Regalnummer, Quelldokument, Fälligkeitsdatum oder Ziel sortieren. Nachfolgend finden Sie einige Verwendungsbeispiele für Sortierung.

* Wenn Sie nach Fälligkeitsdatum sortieren, können Sie wählen, alle Zeilen zu löschen, ausser denen, die sofort beachtet werden müssen. Die weniger dringenden Zeilen werden nicht wirklich gelöscht, sondern nur in den **Kommissionierarbeitsblatt** zurückgeschickt. Wenn Sie die Kommissionierung erzeugen, wurden die Zeilen bereits nach Fälligkeitsdatum sortiert und Sie können die Kommissionierung einem Mitarbeiter zuordnen.
* Wenn Ihre Lagerplätze so nummeriert sind, dass sie dem physischen Layout Ihres Lagers entsprechen, kann das Sortieren von Zeilen nach Lagerplatznummer die Kommissionierung für mehrere Sendungen gleichzeitig erleichtern. 
* Wenn Sie das Bin-Ranking verwenden, kann das Sortieren nach Rang einige Zeit sparen. 
* Sie können nach Zielort sortieren, sodass Sie Bestellungen pro Kunde zusammenstellen und versenden können.

## <a name="to-plan-picks-in-the-worksheet"></a>So planen Sie Kommissionierungen im Arbeitsblatt:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Kommissionierarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die **Logistikbeleg holen** Aktion aus.  
3. Wählen Sie die Warenausgänge, für die Sie eine Kommissionierung vorbereiten möchten. Sie können die Zeilen sortieren, aber die Sortierung wird nicht auf die Auswahlanweisung angewendet. Sie können auch einige der Zeilen löschen, um eine effektivere Kommissionierung zu erzielen. Wenn es z. B. mehrere Zeilen mit Artikeln in Crossd.-Lagerplätzen gibt, möchten Sie möglicherweise eine Kommissionierung für alle Zeilen erzeugen, die mit all diesen Zeilen zusammenhängen. Die zugeordneten Artikel werden ausgeliefert (gemeinsam mit anderen Artikeln im Warenausgang) und die Crossdocklagerplätze haben wieder Platz für neue ankommende Artikel.  
4. Wählen Sie die Aktion **Kommissionierung erstellen** aus, und füllen Sie die Seite **Kommissionierung erstellen**. Die Sortierung, die Sie hier anfordern, sortiert die Kommissionierzeilen, die Sie erstellen. Sie können z. B. eine Kommissionierung für jede Zone erstellen und die Zeilen innerhalb jeder Kommissionierung nach der Lagerplatzpriorität sortieren.  
5. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Lager-Kommissionierungen** ein und wählen Sie dann den zugehörigen Link. Die Seite **Lagerkommissionierungen** wird geöffnet.  
6. Die Kommissionierung finden Sie durch Auswählen der Kommissionierung mit der höchsten Nummer.  
7. Bei Bedarf können Sie einen anderen Benutzer zuweisen oder die Zeilen anders sortieren.  
8. Wählen Sie die Aktion **Drucken** aus, um die Kommissionierungsanweisungen zu drucken.  
9. Nachdem Sie die Kommissionierung durchgeführt haben, wählen Sie die **Registrieren** Aktion aus.  

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/pick-ship-items-warehouse/)

## <a name="see-also"></a>Siehe auch 

[Logistik](warehouse-manage-warehouse.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
